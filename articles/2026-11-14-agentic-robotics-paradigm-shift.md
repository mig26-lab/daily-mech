# Agentic Robotics: AI Agents Writing, Testing, and Refining Robot Programs Mark a Paradigm Shift

![Friendly humanoid robots](https://cdn.pixabay.com/photo/2024/03/09/17/27/ai-generated-8623019_640.jpg)
*Image: Friendly robot concepts from Pixabay (free under Pixabay Content License)*

Recent advances in AI are enabling a new approach to robotics called agentic robotics, where teams of AI agents generate, test, diagnose, and iteratively improve robot control programs. Led by UC Berkeley's Ken Goldberg in collaboration with NVIDIA, this method was highlighted at the Conference on Robot Learning (CoRL) 2026 and could accelerate the development of reliable industrial robots by reducing reliance on massive demonstration datasets.

## The Core Concept

Traditional robotics has followed two main paths: model-based, where engineers carefully program and tune behaviors, and model-free, involving large vision-language-action (VLA) models trained on extensive physical demonstration data. Agentic robotics offers a third way. Multi-agent LLM systems write structured, interpretable robot programs—often composing modular skills—largely offline. These are tested in simulation (using NVIDIA's Isaac framework), failures are diagnosed, and code is revised iteratively, sometimes with adversarial agents checking for flaws.

Goldberg, recently inducted into the National Academy of Engineering, describes it as a fundamental shift: instead of collecting vast data and hand-tuning every behavior, agents quickly generate and refine programs that humans can inspect, fine-tune, and verify. This leverages the strengths of frontier AI models for coding while producing human-readable code suitable for industrial reliability needs.

## Framework and Tools

The team introduced Graph-as-Policy (GaP), which decomposes tasks into skills such as object finding, grasp planning, and collision-free movement. Agents connect these into programs and rehearse them across variations in NVIDIA Isaac simulation. Open-source code and an industry-standard benchmark (VABAR - Variational Automation Benchmark for Agentic Robotics) for evaluating industrial tasks were released.

Examples include generating simulations and programs from short real-world videos (e.g., a robot wiping ink with a sponge) and refining based on failure videos. In testing, approaches achieved high success rates, up to 99% in some cases matching hand-engineered performance, far exceeding baseline imitation learning. Ambi Robotics, advised by Goldberg, applied related methods to parcel sorting, reportedly increasing capacity by over 15,000 packages per robot annually, now in 30% of its US fleet.

## Context and Potential Impact

This comes amid broader AI progress where agents handle complex multistep tasks in software. Applied to robotics, it addresses the data bottleneck and reliability challenges for industrial deployment, where high success rates and speed are essential. Goldberg notes that imitation learning has plateaued for industrial applications requiring reliability, while agentic methods turn programming into a scalable coding problem.

Presented at CoRL 2026 in Austin, with a dedicated workshop, the approach has drawn interest from industry, including evaluations by companies like Bosch. It complements other advances like Gemini Robotics 2.5 and open models such as Praxis-1, potentially enabling faster iteration on tasks from assembly to logistics.

## Challenges and Outlook

While promising, execution reliability is not yet at full industry levels for high-speed production (e.g., targets of 500 units per hour). Simulation-to-real transfer, handling edge cases, and ensuring safety remain critical. The open-source release invites broader experimentation.

## Conclusion

Agentic robotics represents a significant evolution in how robots are programmed, harnessing AI agents to accelerate development of capable, reliable systems. As demonstrated in early industrial applications and research results, it could help bridge the gap between lab prototypes and scalable real-world deployment, especially in manufacturing and logistics. Combined with ongoing progress in humanoid platforms and physical AI models, it contributes to a rapidly advancing robotics landscape in late 2026.

**Approximate word count: 650**

## Sources and References

1. Berkeley News, “Recent advances in AI are creating a 'paradigm shift' for robotics,” November 9, 2026.
2. UC Berkeley AUTOLab and NVIDIA Agentic Robotics project page and materials.
3. IEEE Spectrum coverage on agentic robotics at CoRL 2026.
4. The Deep View and Mindplex reports on the framework and Ambi Robotics application.
5. CoRL 2026 workshop on Agentic Robotics and related researcher updates.

*Image sourced from Pixabay under the free Pixabay Content License. Article based on publicly available research announcements and reporting as of November 14, 2026.*
