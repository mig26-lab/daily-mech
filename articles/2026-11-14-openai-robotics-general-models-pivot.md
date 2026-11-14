# OpenAI Disbands Standalone Robotics Team, Betting General Models Can Directly Control Robots

![Humanoid robot concept](https://cdn.pixabay.com/photo/2024/03/22/06/06/ai-generated-8649013_640.png)
*Image from Pixabay under free Content License. Source: [Pixabay](https://pixabay.com/illustrations/ai-generated-humanoid-robot-android-8649013/)*

On November 13, 2026, Fortune reported that OpenAI had disbanded its stand-alone robotics team. The company confirmed the reorganization when contacted. Robotics researchers moved under Chief Research Officer Mark Chen, while applied robotics and hardware teams joined the Applied organization reporting to President Greg Brockman. OpenAI described the change as an acceleration of robotics work rather than a retreat.

The strategic shift rests on the observation that frontier general-purpose models, particularly GPT-6 Astra, can be applied directly to robot control. Earlier in the year the company had explored paths that built on its video generation model Sora. Subsequent results with general models changed the calculus. An NVIDIA study cited in coverage showed a GPT-6 Astra-powered agent achieving 74.8% success on a simulated robotics manipulation benchmark, compared with 51% for the best specialized robot models tested.

## Background and Prior Robotics Efforts

OpenAI previously shut down a robotics effort around 2020, citing insufficient training data and the faster path to AGI through language models. It reconstituted robotics work in 2024. The company has stated it is developing its own humanoid robot and that CEO Sam Altman has targeted a first public demonstration in 2027. The recent reorganization occurred on short enough notice that OpenAI had already registered a booth at the Conference on Robot Learning (CoRL) in Austin; the booth was empty when reporters visited.

The company maintains that robotics remains part of its long-term vision. The reorganization concentrates talent on general models that can be applied across domains, including physical systems, rather than maintaining a parallel specialized robotics research track.

## Technical and Organizational Implications

If general models continue to outperform or match specialized robot controllers on key benchmarks, the economics of robotics development change. Companies may invest more in simulation, tool use, and closed-loop feedback harnesses that let frontier models drive hardware, and less in training entirely separate robot-specific policies from scratch. OpenAI’s move aligns with this view.

Challenges remain. Simulated success does not automatically translate to reliable real-world performance under contact-rich, long-horizon, or safety-critical conditions. Hardware integration, latency, and safety constraints still require engineering effort. OpenAI has not disclosed detailed real-world robot performance numbers for GPT-6 Astra beyond the cited simulation results.

The reorganization also affects partnerships. OpenAI previously collaborated with Figure AI; that partnership ended earlier, with Figure developing its own robot AI. OpenAI’s internal humanoid effort continues under the reorganized structure.

## Industry Context

Other organizations continue to pursue specialized robotics models. Google DeepMind released Gemini Robotics 2.5, reporting strong results on Mercedes-Benz production lines with Apptronik humanoids. NVIDIA, Agile Robots, and multiple humanoid makers maintain dedicated physical-AI stacks. OpenAI’s bet is that continued scaling and tool-use improvements in general models will narrow or reverse the gap.

The coming months will test whether the reorganization produces faster progress toward useful robots or whether specialized teams retain an advantage on embodied tasks. OpenAI’s public statements emphasize commitment; independent verification of real-world performance will be the decisive measure.

## Sources and References

1. Fortune exclusive: OpenAI disbands its stand-alone robotics team as its general models start running robots (November 13, 2026).
2. The Decoder and AI Chat Daily contemporaneous reporting on the reorganization and GPT-6 Astra simulation results (November 13–14, 2026).
3. OpenAI statements via Fortune on robotics remaining a core long-term goal and the 2027 demo target.
4. NVIDIA study results referenced in coverage comparing Astra-powered agents to specialized robot models.

*Article compiled from public reporting and company statements. Images sourced from Pixabay under free license.*