# Gemini Robotics 2.5 Achieves 96% Success on Mercedes-Benz Production Lines

**Published: November 13, 2026**

![Humanoid robot in industrial warehouse setting](https://cdn.pixabay.com/photo/2026/03/14/02/39/tungart7-robot-10172923_640.jpg)
*Image from Pixabay (free under Pixabay Content License)*

## Introduction

Google DeepMind announced Gemini Robotics 2.5 on November 10, 2026, describing it as its most capable vision-language-action (VLA) model to date. The model significantly improves robot dexterity, reliability, and speed for real-world physical tasks. The standout demonstration involved Apptronik’s Apollo 2 humanoid robots performing automotive kitting on live Mercedes-Benz production lines with a reported 96% success rate.

This proof-of-concept took place at facilities in Kecskemét, Hungary, and Sindelfingen, Germany. The robots sorted metal automotive brackets from bulk bins into sequenced trays required by each vehicle on the assembly line—a repetitive yet critical task that traditionally requires human workers.

## Technical Advances

Gemini Robotics 2.5 is a VLA model that maps visual input and language instructions directly to motor commands. DeepMind evaluated it across more than 200 distinct tasks, reporting success-rate improvements of 30% to 100% over previous baselines, with tasks completed 20% to 30% faster.

Key improvements include:

- Greater dexterity with everyday tools and delicate/flexible objects
- Better reliability in unstructured environments
- Enhanced safety around obstacles (+33% safe completions) and nearby people (+43%)
- Stronger resistance to jailbreak-style unsafe requests (new ASIMOV-Jailbreak benchmark released)

In the Mercedes pilot, an embodied-reasoning model (Gemini Robotics ER) tracked the overall workflow while Gemini Robotics 2.5 controlled the arms and hands. The Apollo 2 configuration used a five-finger SharpaWave hand with 22 degrees of freedom.

| Metric                        | Reported Result                  |
|-------------------------------|----------------------------------|
| Tasks Evaluated               | >200                             |
| Success Rate Gain             | 30–100% vs. prior baselines     |
| Speed Improvement             | 20–30% faster                   |
| Mercedes Kitting Success      | 96%                              |
| Safety (near people)          | +43%                             |

## Industry Impact and Partnerships

Apptronik CEO Jeff Cardenas noted that the models improved dramatically in weeks of post-training and transferred to the Mercedes lines with minimal drop-off. Mercedes-Benz has previously invested in Apptronik, signaling growing automaker interest in humanoid assistance for monotonous preparation work so technicians can focus on complex assembly.

This aligns with broader trends: logistics firms such as GXO are exploring large-scale deployments of Apptronik humanoids (reports of up to 1,000 units), and other manufacturers including ASUS (Gallop humanoid) and various Chinese firms are accelerating factory humanoid programs. DeepMind is rolling the model out to robotics partners rather than releasing it publicly.

## Challenges and Outlook

While the 96% figure is impressive, independent details on sample size, cycle time versus humans, and exact failure modes remain limited. Real-world reliability still requires extensive site-specific data and safety validation. Nonetheless, the combination of foundation-model intelligence with physical embodiment marks a notable step toward practical industrial humanoids.

## Conclusion

Gemini Robotics 2.5 demonstrates that large vision-language-action models can deliver production-relevant performance on active factory floors. The Mercedes-Benz pilot with Apollo 2 provides concrete evidence that humanoids can handle high-volume kitting tasks at scale. As more manufacturers pilot and deploy these systems, the economics of human-robot collaboration on the factory floor are likely to shift rapidly.

## Sources and References

1. Google DeepMind Blog: Gemini Robotics 2.5: Accelerating Physical Intelligence (November 10, 2026)
2. Robotics 24/7 and Humanoids Daily reporting on the Mercedes pilot
3. Unite.AI, DataStudios, and other industry coverage
4. Apptronik statements via DeepMind announcement
5. Related robotics news: GXO plans, ASUS Gallop, and funding rounds (Agile Robots, etc.)

**Helpful Tip:** For manufacturers evaluating humanoids, request detailed cycle-time and failure-mode data beyond headline success rates before scaling pilots.
