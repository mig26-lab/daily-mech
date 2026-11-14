# GENTO Unveils 21-Degree-of-Freedom Dexterous Hand Used with NVIDIA GR00T 2

![Robotic hand interacting with technology](https://cdn.pixabay.com/photo/2026/04/20/18/48/18-48-11-393_640.jpg)
*Image from Pixabay under free Content License. Source: [Pixabay](https://pixabay.com/photos/robotics-artificial-intelligence-10237767/)*

At CoRL 2026, GENTO presented a new 750-gram dexterous robotic hand featuring 21 degrees of freedom and high-precision force control. The hand has been used by NVIDIA to demonstrate its GR00T 2 world-action model performing two-handed food-preparation tasks, highlighting progress in both hardware dexterity and foundation-model control for manipulation.

The announcement adds to a cluster of recent advances in robot hands and embodied AI models. Reliable fine manipulation remains one of the harder barriers to broader humanoid and dual-arm deployment; improvements in both the physical hardware and the models that drive it are therefore closely watched.

## Hardware Specifications and Design Goals

GENTO’s hand weighs approximately 750 grams and provides 21 degrees of freedom. It emphasizes low torque requirements (on the order of 0.02 Newton-meters in certain joints) while aiming for precise force and position control suitable for delicate and multi-step tasks. The design prioritizes practicality for research and demonstration platforms rather than heavy industrial payloads.

The hand was shown in the context of NVIDIA’s GR00T 2 launch materials. GR00T 2 is an open world-action model built on NVIDIA Cosmos that has been demonstrated assembling objects and performing bimanual tasks such as scooping granola. Pairing a high-DoF hand with a generalist model allows researchers to explore zero-shot or few-shot transfer of skills learned from video or simulation into physical two-handed work.

## Connection to Broader Model and Hardware Trends

NVIDIA has been advancing robotics foundation models alongside its simulation and compute stack. GR00T 2 builds on prior work and is part of a wider ecosystem that includes Isaac Lab updates and partnerships with robot makers. Demonstrations that combine third-party dexterous hardware with these models help illustrate the potential for more modular, interoperable robotics systems.

Similar progress is occurring elsewhere. Other groups have released tactile sensing modules, open-source tactile AI models, and higher-DoF hands. Google DeepMind’s Gemini Robotics 2.5 work has included multi-fingered hands on Apptronik platforms for industrial kitting. The common theme is that better end-effectors and better models are advancing in parallel.

GENTO’s contribution focuses on a lightweight, high-DoF hand that can be integrated into existing research and demonstration setups. Its use with GR00T 2 provides a concrete example of how specialized hardware can showcase the capabilities of a generalist action model.

## Implications for Manipulation Research and Deployment

High-degree-of-freedom hands enable richer contact interactions and more human-like grasp strategies, which are useful for tasks that fixed or low-DoF grippers handle poorly. At the same time, controlling such hands reliably requires capable perception, planning, and low-level control—precisely the areas that world-action and vision-language-action models are targeting.

Successful demonstrations of two-handed food preparation or similar tasks suggest that the combination of improved hardware and foundation models is reducing the gap between controlled lab settings and more varied real-world manipulation. Remaining challenges include robustness to object variation, long-horizon reliability, and the cost and complexity of the hardware itself.

## Looking Ahead

As more high-DoF hands become available and foundation models continue to improve at physical reasoning and control, researchers and developers gain additional tools for studying and deploying dexterous manipulation. GENTO’s CoRL 2026 presentation and its pairing with NVIDIA GR00T 2 illustrate one practical path: specialized hardware that lets generalist models express a wider range of skills.

Future work will likely focus on tighter integration, larger-scale data collection with such hands, and evaluation on standardized manipulation benchmarks. Progress on both the mechanical and algorithmic sides will determine how quickly dexterous, two-handed robots move from demonstration platforms into production and service environments.

## Sources and References

1. The Robotics Media: 21 Degrees of Freedom, 0.02 Newton-Meters: Inside GENTO's New Robot Hand (November 14, 2026).
2. Reporting on NVIDIA GR00T 2 launch and demonstrations at CoRL 2026 (November 2026).
3. NVIDIA materials on GR00T 2 as an open world-action model built on Cosmos.
4. Broader coverage of dexterous hands, tactile sensing, and VLA models from DeepMind, Apptronik, and other groups (2026).
5. CoRL 2026 conference context and related robotics hardware announcements.

*Article compiled from public announcements and contemporaneous reporting. Images sourced from Pixabay under free license.*