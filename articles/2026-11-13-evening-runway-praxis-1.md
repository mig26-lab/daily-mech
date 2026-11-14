# Runway Releases Praxis-1 Open Weights: Advancing Accessible Robot Control from Video Pretraining

![Robotics Technology](https://cdn.pixabay.com/photo/2024/06/12/06/06/robot-8824474_1280.jpg)
*Humanoid robot image from Pixabay*

On November 11, 2026, Runway made its Praxis-1 world action model available with open weights under the Apache 2.0 license, including for commercial use. Originally introduced in September for select partners, the release now provides weights, inference code, and fine-tuning tools on GitHub, Hugging Face (with LeRobot support), and via vLLM-Omni.

## Model Architecture and Performance

Praxis-1 is a roughly 27-billion-parameter mixture-of-experts diffusion transformer. It predicts future video frames and robot actions jointly, leveraging large-scale video pretraining from Runway’s world models. Given camera observations, robot state, and a task instruction, it outputs coordinated motion.

On NVIDIA’s RoboLab-120 simulation benchmark (1,200 episodes of tabletop tasks), it achieved 46.2% success—the highest among world action models and open-weight robot foundation models. This outperformed FLUX 3 Action (42.9%), Cosmos3 Nano (36.8%), and π0.5 (28.0%). Launch partners including Noble Machines, Standard Bots, and Ultra have run it on humanoids, industrial arms, and warehouse robots.

## Implications for Robotics Development

Open weights lower barriers for researchers and companies to adapt the model to new hardware via fine-tuning or LoRA. Checkpoints cover base models plus DROID (single-arm) and YAM (bimanual) variants. This approach builds on video understanding of physical dynamics to accelerate skill transfer across embodiments.

While not topping the overall RoboLab-120 leaderboard (where some frontier-model agents score higher), it leads its category and demonstrates progress in generalist robot policies. The Apache 2.0 license supports both research and commercial deployment, subject to any separate encoder licenses.

## Broader Trend

The release aligns with growing open-source momentum in physical AI, complementing efforts from Google DeepMind (Gemini Robotics), NVIDIA (GR00T), and others. By making video-trained action models accessible, Runway enables faster experimentation on real robots, potentially accelerating practical deployments in factories, warehouses, and beyond.

Developers can start adapting it immediately. Hosted inference is also available on Runway’s Reactor platform. This marks a significant step toward democratizing advanced robot control technology.

**Sources and References**
- Runway official announcement: Praxis-1 Is Now Available (November 11, 2026)
- Runway research post and technical report on video pretraining to robot control
- The Robot Report coverage
- AlphaSignal and Servospace analyses of benchmarks
- Hugging Face and GitHub repositories for weights and code

*Images sourced from Pixabay under free license for use.*
