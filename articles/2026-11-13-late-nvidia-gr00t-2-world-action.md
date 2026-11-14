# NVIDIA GR00T 2: Teaching Robots New Skills by Watching Humans

**Published: November 13, 2026 | Late Update**

![Futuristic robotic hand reaching toward digital network](https://cdn.pixabay.com/photo/2023/10/21/12/35/ai-generated-8331364_1280.jpg)
*Image from Pixabay – free under the Pixabay Content License*

## Introduction

At the Conference on Robot Learning (CoRL) in Austin in early November 2026, NVIDIA unveiled GR00T 2, its next-generation open world-action model for robotics. Unlike traditional robot policies trained almost exclusively on robot teleoperation data, GR00T 2 is pretrained predominantly on human video and then adapts to new tasks and robot bodies with only a handful of demonstrations.

The model jointly predicts future video and the actions that produce it, allowing it to reason about physical outcomes before acting. A lighter Turbo variant can run onboard a Unitree G1 humanoid using its Jetson Thor computer.

## Training Data and Architecture

GR00T 2 was trained on a massive mixture that is roughly 92% human egocentric video (approximately 400,000 hours), with smaller amounts of handheld gripper data and actual robot teleoperation. A 100,000-hour open human video subset is already available on Hugging Face. The model is built on NVIDIA’s Cosmos video foundation models and contains roughly 2 billion parameters.

Key claimed results on 50 held-out tasks the target robot had never seen:

| Demonstrations | Average Success |
|----------------|-----------------|
| Zero-shot | ~40% (40 of 50 tasks completed at least once) |
| 1 demo | 71% |
| 5 demos | 95% |

Fine-tuning after five short demonstrations can take under 30 minutes on a single RTX 5090. The model has been shown performing dexterous tasks with 22-DoF hands, whole-body humanoid control, and long-horizon sequences such as assembling objects or packing.

## Why This Matters

Collecting robot data is expensive and slow. By learning primarily from abundant human video, GR00T 2 dramatically reduces the data bottleneck that has limited robot learning. Skills can transfer across different robot morphologies, and a reasoning model can direct the world-action model toward desired outcomes.

Partners including Foxconn, Siemens, and others are already evaluating or applying the system for factory automation and laundry handling. Weights and adaptation recipes are expected in December 2026, with code also scheduled for release then. NVIDIA positions the model as open, though exact licensing details for commercial use will matter once the full release arrives.

## Broader Context

GR00T 2 arrives alongside Isaac Lab 3.0 improvements and at a moment when multiple labs (Google DeepMind’s Gemini Robotics, Runway’s Praxis-1, and others) are releasing vision-language-action or world models. The common theme is that foundation models trained on large-scale video and human data are beginning to outperform specialized robotics stacks on many manipulation benchmarks.

## Conclusion

NVIDIA GR00T 2 represents a meaningful step toward robots that can acquire new physical skills the way humans do—by watching and then practicing briefly. If the claimed few-shot performance holds up under independent evaluation and real factory conditions, it could shorten deployment times for warehouse, manufacturing, and service robots from months to days. The December weights release will be the first real test of how widely the community can build on the work.

## Sources and References

1. NVIDIA GEAR research page – GR00T 2 (research.nvidia.com/labs/gear/gr00t-2/)
2. NVIDIA announcements at CoRL 2026 and associated blog posts
3. The Robot Report, Technology.org, RD World Online, and FourWeekMBA coverage (Nov 9–13, 2026)
4. Hugging Face Human-1M-100K dataset page
5. Partner mentions (Foxconn, Siemens, Nexuni)

**Helpful Tip:** When the weights drop in December, start with the provided few-shot adaptation recipes on a small set of your own tasks before scaling—the data efficiency is the real product.
