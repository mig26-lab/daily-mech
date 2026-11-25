# "Obtain Shell Access": Amazon Says Hackers' Cairn AI Agents Found and Exploited a Zero-Day in 11 Minutes

![Hooded figure at a computer illustrating cyber security threats](https://cdn.pixabay.com/photo/2017/10/14/17/18/hacker-2851143_1280.jpg)

*Image credit: Pixabay (ID 2851143), free to use under the Pixabay Content License. Illustrative image.*

A one-line instruction, "obtain shell access," was all a suspected Chinese-nexus threat actor needed to send a team of autonomous AI agents after university servers in East Asia. According to [Amazon Threat Intelligence](https://aws.amazon.com/blogs/security/chinese-nexus-actors-cairn-ai-agents-found-a-zero-day-on-their-own/), the agents went on to discover a previously unknown vulnerability in an open-source medical imaging AI tool and used it to take full root control of a server, with almost no human steering. The case, published November 20 and widely reported this week, is one of the clearest public examples yet of AI agents finding and exploiting a zero-day on their own.

## How Amazon Found It

On September 10, 2026, Amazon's researchers came across a publicly reachable server running **Cairn**, an open-source autonomous AI penetration-testing framework. It had no authentication, which exposed the operator's project settings, prompts and the agents' output. That history showed a roughly **48-hour campaign beginning September 8**, aimed at IP addresses tied to universities in East Asia outside mainland China, per the [AWS Security Blog](https://aws.amazon.com/blogs/security/chinese-nexus-actors-cairn-ai-agents-found-a-zero-day-on-their-own/). The operator wrote prompts in simplified Chinese and set the model to China Standard Time, [Ars Technica](https://arstechnica.com/security/2026/11/amazon-says-hackers-ai-agents-found-and-exploited-0-day-with-little-human-input/) reports.

## The Zero-Day in 11 Minutes

The successful attack targeted **MONAI Label**, an open-source tool for AI-assisted annotation of medical images that is part of the NVIDIA-backed Project MONAI, as identified by [SecurityWeek](https://www.securityweek.com/amazon-china-linked-hackers-ai-agents-exploited-medical-software-zero-day/). The agents:

1. Identified the application's framework and mapped its API endpoints.
2. Found an upload endpoint with a filename parameter and tested it for **path traversal**.
3. Went from API mapping to writing arbitrary files on the server in about **11 minutes**.
4. In a later session, wrote a Python reverse shell into `sitecustomize.py`, a file Python loads automatically at startup.
5. Triggered a training API endpoint to start a new Python process, which loaded the payload and opened a **root shell**.

Amazon assessed "with high confidence" that the flaw was a true zero-day because it had no fix, issue, advisory or prior mention anywhere. Authentication in MONAI Label is off by default, so anyone who can reach the server could exploit it, [SecurityWeek](https://www.securityweek.com/amazon-china-linked-hackers-ai-agents-exploited-medical-software-zero-day/) notes.

Only after that did the human step back in, handing the agents a proxy into a second university network that ran the same software. Amazon infers that server had already been compromised with the same bug.

## Where the Agents Failed

The report is just as telling about what did not work. According to [Amazon](https://aws.amazon.com/blogs/security/chinese-nexus-actors-cairn-ai-agents-found-a-zero-day-on-their-own/):

- Against an open Redis server, the agents spent about **16 hours** and **148 sequential actions** trying replication abuse, sandbox escapes, config-file writes, memory corruption and Log4Shell, then pivoted through an SSRF bug in a Qdrant instance to spray credentials at PostgreSQL and SSH. **None succeeded.**
- In a separate six-hour operation, they mined faculty directories, lab sites and academic papers to build about **80 real usernames**, then tried more than **30,000 credential combinations** across SSH, an admin dashboard, network storage, a VPN and a campus portal. **No login worked.**

In other words, well-configured systems held. The win came from a classic bug in a niche research tool, as [Hardware Busters](https://hwbusters.com/news/cairn-ai-agents-needed-11-minutes-to-find-a-monai-label-zero-day-and-cisa-has-now-flagged-it-as-exploited/) points out.

## Patch Status

Amazon notified the MONAI Label maintainers, who shipped a fix and a GitHub security advisory; [BleepingComputer](https://www.bleepingcomputer.com/news/security/hackers-use-autonomous-ai-tool-cairn-to-find-zero-day-take-over-server/) reports the update landed on November 18. On November 23, CISA added the flaw to its Known Exploited Vulnerabilities catalog and gave federal agencies until **November 26** to patch, an unusually short window, per [Hardware Busters](https://hwbusters.com/news/cairn-ai-agents-needed-11-minutes-to-find-a-monai-label-zero-day-and-cisa-has-now-flagged-it-as-exploited/). Amazon also worked with a government partner to warn the affected universities, which were not AWS customers.

## Why It Matters

- **Speed now favors attackers.** Agents can probe, adapt and exploit faster than a human analyst can review alerts.
- **The skill floor is dropping.** A short goal and a list of IP addresses replaced the expert work of choosing each step.
- **Open-source research tools are soft targets.** Niche AI and science apps often ship with authentication off and run on exposed lab servers.
- **Basic hygiene still works.** Strong credentials and patched, locked-down services defeated thousands of automated attempts.

Amazon's advice to defenders is to prioritize **high-confidence detections that trigger automated responses**, with humans overseeing outcomes rather than reviewing every action.

**Helpful tip:** If your lab or team runs MONAI Label, update it now, turn on authentication, and keep it off the public internet. More broadly, inventory any AI or research tools listening on public IPs, since those are exactly what autonomous agents scan for.

## Sources and References

1. AWS Security Blog – "Chinese-nexus actor's Cairn AI agents found a zero-day on their own" (November 20, 2026): https://aws.amazon.com/blogs/security/chinese-nexus-actors-cairn-ai-agents-found-a-zero-day-on-their-own/
2. Ars Technica – "Amazon says hackers' AI agents found and exploited 0-day with little human input" (November 24, 2026): https://arstechnica.com/security/2026/11/amazon-says-hackers-ai-agents-found-and-exploited-0-day-with-little-human-input/
3. SecurityWeek – "Amazon: China-Linked Hackers' AI Agents Exploited Medical Software Zero-Day" (November 21, 2026): https://www.securityweek.com/amazon-china-linked-hackers-ai-agents-exploited-medical-software-zero-day/
4. BleepingComputer – "Hackers use autonomous AI tool Cairn to find zero-day, take over server" (November 2026): https://www.bleepingcomputer.com/news/security/hackers-use-autonomous-ai-tool-cairn-to-find-zero-day-take-over-server/
5. Hardware Busters – "Cairn AI Agents Needed 11 Minutes to Find a MONAI Label Zero-Day, and CISA Has Now Flagged It as Exploited" (November 24, 2026): https://hwbusters.com/news/cairn-ai-agents-needed-11-minutes-to-find-a-monai-label-zero-day-and-cisa-has-now-flagged-it-as-exploited/
6. Pixabay image (ID 2851143), Pixabay Content License: https://pixabay.com/photos/hacker-cyber-security-network-2851143/
