# Microsoft Unveils MAI Code 2 and Code 2 Flash at Ignite, Targeting Everyday Coding at a Fraction of Rivals' Cost

![Source code displayed on a computer screen](https://cdn.pixabay.com/photo/2016/11/19/14/00/code-1839406_1280.jpg)

*Image credit: Pixabay – free to use under the Pixabay Content License.*

Microsoft used its Ignite 2026 conference on November 17 to launch **MAI Code 2** and **MAI Code 2 Flash**, two in-house coding models built for routine enterprise software work. The pitch is simple: near-frontier coding quality at a small fraction of the price charged by OpenAI and Anthropic, according to [Microsoft AI](https://microsoft.ai/news/introducing-mai-code-2-and-mai-code-2-flash/). The two models are part of a broader set of seven new MAI models Microsoft announced at the event, per its [Ignite overview](https://microsoft.ai/news/microsoft-ignite-2026/).

## Two Models, Two Jobs

- **MAI Code 2** targets the heavier side of everyday work: taking code to production, deep debugging, multi-file implementation, repository-wide reasoning and UI work. Microsoft says it is also tuned for dashboards, visualizations and visual coding.
- **MAI Code 2 Flash** is built for high-volume tasks such as code explanations, targeted edits, routine fixes and rapid iteration.

Both are available in **GitHub Copilot**. Code 2 Flash is also in a limited-access preview in **Microsoft Foundry**.

## The Performance Claims

Microsoft averaged results across four benchmarks it says reflect the everyday enterprise tasks it sees in GitHub Copilot: DeepSWE 1.1, Terminal-Bench 2.1, SWE-Atlas and FrontierCode v1.1. On that basis, it says MAI Code 2 delivers **98% of GPT-6.1 Sol's performance at 40% of the cost**, and **96% of Claude Opus 5.5's performance at 5% of the cost**.

[InfoWorld](https://www.infoworld.com/article/4250152/microsoft-launches-mai-code-2-models-to-challenge-openai-and-anthropic-in-ai-coding.html) breaks down the numbers:

| Model | Avg. pass rate | Avg. cost per task |
|---|---|---|
| MAI Code 2 | 63.2% | $0.309 |
| GPT-6.1 Sol | 64.1% | $0.761 |
| Claude Opus 5.5 | 65.3% | $6.306 |

Individually, MAI Code 2 scored 73.2% on DeepSWE 1.1, 84.6% on Terminal-Bench 2.1, 43.1% on SWE-Atlas and 52% on FrontierCode v1.1.

For the smaller model, Microsoft compared MAI Code 2 Flash with GPT-6 Luna and Claude Haiku 5.5 across three benchmarks. Flash averaged 61%, ahead of GPT-6 Luna at 55.1% and Haiku 5.5 at 53.9%, at an average cost of $0.052 per task versus $0.080 and $0.319, per InfoWorld.

## Read the Fine Print

Two caveats matter:

1. **Promotional pricing.** Microsoft's cost comparisons use MAI's 50% promotional price, as its own [footnotes](https://microsoft.ai/news/introducing-mai-code-2-and-mai-code-2-flash/) state. At full price, the cost gap narrows, though it remains large against Opus 5.5.
2. **Microsoft's own harness.** DeepSWE 1.1, Terminal-Bench 2.1 and SWE-Atlas were run on MSBench, Microsoft's internal evaluation platform, using the GitHub Copilot CLI without subagents. FrontierCode scores and costs come from Artificial Analysis.

## Pricing

According to GitHub pricing cited by [InfoWorld](https://www.infoworld.com/article/4250152/microsoft-launches-mai-code-2-models-to-challenge-openai-and-anthropic-in-ai-coding.html):

| Model | Promo input / cached / output (per 1M tokens, until May 17, 2027) | Standard input / cached / output |
|---|---|---|
| MAI Code 2 | $0.50 / $0.025 / $2.50 | $1.00 / $0.05 / $5.00 |
| MAI Code 2 Flash | $0.05 / $0.005 / $0.25 | $0.10 / $0.01 / $0.50 |

## Why It Matters

- **Microsoft is reducing its dependence on partners.** Shipping first-party models inside GitHub Copilot gives Microsoft more control over cost and margins in its most important developer product.
- **"Good enough" is becoming the competitive frontier.** Most coding requests are routine. A model that is a few points behind the leader but many times cheaper can win the bulk of everyday traffic.
- **Model routing becomes the default.** Teams can send hard problems to frontier models and route routine edits to cheaper ones such as Code 2 Flash.

The launch also landed the same day as OpenAI's GPT-6.2 release, underlining how quickly prices for capable coding models are falling.

**Helpful tip:** If you use GitHub Copilot, try MAI Code 2 Flash for small edits and explanations while the promotional price lasts, and compare the review time it saves against your current default model before switching larger workflows.

## Sources and References

1. Microsoft AI – "MAI Code 2 and Code 2 Flash: Everyday coding at scalable prices" (November 17, 2026): https://microsoft.ai/news/introducing-mai-code-2-and-mai-code-2-flash/
2. Microsoft AI – "Seven new world class models at scalable price-performance" (Ignite 2026): https://microsoft.ai/news/microsoft-ignite-2026/
3. InfoWorld – "Microsoft launches MAI Code 2 models to challenge OpenAI and Anthropic in AI coding" (November 18, 2026): https://www.infoworld.com/article/4250152/microsoft-launches-mai-code-2-models-to-challenge-openai-and-anthropic-in-ai-coding.html
4. Pixabay image (ID 1839406), Pixabay Content License: https://cdn.pixabay.com/photo/2016/11/19/14/00/code-1839406_1280.jpg

*Note: Benchmark and cost figures are as reported by Microsoft and use its promotional pricing unless otherwise stated.*
