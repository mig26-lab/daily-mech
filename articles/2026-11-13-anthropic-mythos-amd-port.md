# Anthropic’s Mythos Ports Claude to AMD GPUs in Three Days

**Published: November 13, 2026**

![AI hardware and chip technology](https://cdn.pixabay.com/photo/2025/02/11/05/55/ai-generated-9398115_640.jpg)
*Image from Pixabay (free under Pixabay Content License)*

## Introduction

During its IPO roadshow, Anthropic revealed that its frontier model Mythos enabled Claude to run on AMD MI355X GPUs in approximately three days, with almost no human intervention. Traditional approaches to bringing up a new chip platform had previously required dozens of engineers and six to twelve months. Claude itself ported or wrote nearly 100% of the necessary kernels.

The claim appeared in a roadshow video and associated slides, with co-founder and Chief Compute Officer Tom Brown describing the multi-chip strategy. Anthropic has emphasized treating compute across AWS Trainium, Google TPUs, Nvidia GPUs, and now AMD as a fungible pool.

## The Technical Achievement

The three-day timeline specifically refers to achieving useful prompt-processing performance for one Anthropic model on AMD’s MI355X GPUs (CDNA 4 architecture). Footnotes in the materials clarify the scope, distinguishing it from a full production bring-up of every workload. Nonetheless, the speed represents a roughly 60- to 120-fold acceleration compared with historical internal experience.

Key reported elements:
- Mythos handled the majority of kernel development and porting
- Minimal human guidance after initial connection of the model to the hardware
- AMD CEO Lisa Su reportedly confirmed that planned engineering support from AMD was not needed
- Anthropic now runs Claude across four major chip families

| Metric                        | Traditional Approach     | With Mythos          |
|-------------------------------|--------------------------|----------------------|
| Time to Useful Performance    | 6–12 months             | ~3 days             |
| Engineering Effort            | Dozens of engineers     | Almost none         |
| Kernel Work                   | Manual                  | ~100% by Claude     |
| Scope (per footnote)          | Full platform           | Prompt processing   |

## Strategic Context and Implications

This demonstration supports Anthropic’s multi-vendor compute strategy, reducing dependence on any single chip supplier and Nvidia’s CUDA ecosystem in particular. The company has a larger agreement with AMD involving up to 2 GW of MI450-series systems and potential equity investment. Rapid hardware portability could improve negotiating leverage and resilience as AI infrastructure scales.

The timing coincides with Nvidia’s own leadership transition following Jensen Huang’s resignation. Faster AI-assisted hardware onboarding may accelerate the erosion of software moats that have long favored incumbent chip platforms.

## Broader Significance

While independent verification of the exact performance and completeness is limited, the episode illustrates a growing capability: frontier models assisting in their own deployment and infrastructure work. Similar self-improving or self-porting behaviors, if sustained, could compress the engineering cycles that currently bottleneck AI infrastructure expansion.

## Conclusion

Anthropic’s claim that Mythos ported Claude to AMD hardware in days rather than months highlights both the practical progress of AI coding agents and the strategic value of multi-chip flexibility. As more labs adopt similar approaches, the competitive dynamics of AI hardware supply are likely to shift.

## Sources and References

1. Anthropic IPO roadshow video and slides (November 2026)
2. The Decoder: Anthropic says AI is eroding Nvidia’s CUDA lead
3. FourWeekMBA analysis of the AMD bring-up slide and footnotes
4. Reporting from Crypto Briefing, OfficeChai, and other outlets citing Tom Brown’s comments
5. Related Anthropic–AMD partnership announcements

**Helpful Tip:** When assessing hardware portability claims, always review footnotes for the precise scope of “running” or “useful performance,” as full production equivalence can take longer.
