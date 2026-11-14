# Runway Releases Praxis-1: Open-Weight World Action Model for Robotics

**Published: November 13, 2026**

![Robot arms performing manipulation tasks](https://cdn.pixabay.com/photo/2024/03/22/06/06/ai-generated-8649016_640.png)
*Image from Pixabay (free under Pixabay Content License)*

## Introduction

On November 11, 2026, Runway made its Praxis-1 world action model publicly available with open weights under the Apache 2.0 license. The 27-billion-parameter mixture-of-experts diffusion transformer predicts both future video and robot actions, turning large-scale video pretraining into usable robot control policies. It is available on Hugging Face (with LeRobot support), GitHub, and via hosted inference.

Praxis-1 was first announced in September 2026 with select partners. The open release includes weights, inference code, and fine-tuning recipes (full and LoRA), permitting commercial use.

## Performance and Architecture

On NVIDIA’s RoboLab-120 simulation benchmark (1,200 episodes across 120 tabletop tasks), Praxis-1 achieved 46.2% success, ranking as the top world action model and the highest among open-source robot foundation models. It outperformed FLUX 3 Action (42.9%), Cosmos3 Nano (36.8%), and π0.5 (28.0%).

The model jointly predicts video chunks and approximately 1.6 seconds of robot actions. Video pretraining provides strong priors on object physics, motion, and task progress, which transfer to new robot embodiments via fine-tuning.

| Model              | Type                     | RoboLab-120 Success |
|--------------------|--------------------------|---------------------|
| Praxis-1           | World action             | 46.2%              |
| FLUX 3 Action      | World action             | 42.9%              |
| Cosmos3 Nano       | World action             | 36.8%              |
| π0.5               | Vision-language-action   | 28.0%              |

Early partners including Noble Machines, Standard Bots, and Ultra have run the model on humanoid, industrial-arm, and dual-arm platforms.

## Significance for the Robotics Community

Open-weight releases of capable robot foundation models remain relatively rare. By licensing under Apache 2.0 and providing full fine-tuning support, Runway lowers the barrier for researchers and companies to adapt a strong video-pretrained policy to their own hardware. The approach complements vision-language-action models (such as Google’s Gemini Robotics series) by emphasizing generative video understanding as a pathway to physical control.

Practical considerations include model size (roughly 54 GB for some checkpoints) and the need for embodiment-specific fine-tuning before real-world deployment. Simulation success does not automatically translate to production reliability.

## Broader Context

This release arrives amid rapid progress in industrial and humanoid robotics, including Gemini Robotics 2.5’s 96% success on Mercedes-Benz lines and new factory humanoids from ASUS and others. Open models like Praxis-1 can accelerate experimentation outside closed lab environments.

## Conclusion

Runway’s open release of Praxis-1 gives the robotics community a high-performing, commercially usable world action model grounded in video prediction. It represents a meaningful step toward more accessible foundation models for physical AI, though real-world generalization and safety validation remain essential next steps.

## Sources and References

1. Runway announcement: Praxis-1 Is Now Available (November 11, 2026)
2. Runway Research technical report on Praxis-1
3. The Robot Report and ServoSpace coverage of the open-weight release
4. NVIDIA RoboLab-120 leaderboard data
5. Hugging Face and GitHub repositories for weights and code

**Helpful Tip:** When fine-tuning open robot models like Praxis-1, start with the provided embodiment-specific checkpoints (DROID or YAM) and validate thoroughly in simulation before hardware trials.
