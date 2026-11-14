# Skild AI Open-Sources Steel: A Faster Physics Engine for Scalable Robot Learning

![Robot arm in workshop](https://cdn.pixabay.com/photo/2023/07/22/03/37/ai-generated-8142626_640.jpg)
*Image from Pixabay under free Content License. Source: [Pixabay](https://pixabay.com/illustrations/ai-generated-automated-workshop-8142626/)*

On November 9, 2026, Skild AI open-sourced Steel, a GPU-accelerated rigid-body physics solver developed in collaboration with NVIDIA. Integrated into the open-source Newton physics engine, Steel is designed specifically for the diverse, contact-rich simulations required to train general-purpose robotic systems. Early benchmarks show substantial gains over existing tools, particularly when simulating mixtures of different robots and tasks simultaneously.<grok type="render_inline_citation" citation_id="85" />

The release addresses a core bottleneck in embodied AI research: generating enough high-quality physical experience at scale. While locomotion can often be trained on many copies of the same robot, manipulation and generalist skills require millions of varied scenarios involving different morphologies, objects, and contact dynamics.

## Performance Advantages

Across 20 robot-learning benchmarks, Steel delivered a geometric-mean 3.8× throughput improvement over PhysX when each engine ran at its best measured batch size, and it was faster on 19 of the 20 tasks. On heterogeneous batches that mix different robots and tasks, the advantage reached up to 13×. Memory usage was also lower—roughly 62% less in mixed-task tests according to Skild’s measurements.<grok type="render_inline_citation" citation_id="86" />

Independent testing by other groups has corroborated the gains. One evaluation integrating Steel into Isaac Lab 3.0 on an RTX PRO 6000 Blackwell confirmed strong speedups across standard tasks and demonstrated that Steel could sustain far more parallel industrial robot cells (up to 8× in one machine-tending setup) before hitting memory or stability limits.

Steel’s architecture uses a per-environment layout that avoids padding every environment to the largest robot or contact set present. This design is particularly well-suited to the heterogeneous workloads that arise when training foundation models for robotics.

## Integration and Availability

Steel is available as `newton.solvers.SolverSteel` inside the Newton engine and is intended to work with NVIDIA Isaac Lab. The code is Apache 2.0 licensed, allowing commercial use, modification, and redistribution. Skild also released a WebGPU implementation and an interactive playground so researchers and developers can experiment directly in a browser.

The solver can be combined with Newton’s other capabilities. For example, a rigid robot arm can be simulated with Steel while flexible objects such as cables use Newton’s VBD solver, enabling more complete scene simulation without switching engines.

## Context in Robotics Foundation Models

Skild AI has been building an “omni-bodied” robot brain capable of controlling different embodiments with minimal additional training. Earlier work with NVIDIA leveraged Cosmos foundation models, Isaac Sim, and Isaac Lab to generate large-scale training data from human video, teleoperation, and simulation. Steel is a direct enabler of that strategy by making diverse parallel simulation more efficient.

The timing aligns with broader industry interest in physical AI. NVIDIA has continued to expand its robotics software stack, and multiple labs are exploring whether general-purpose models can be applied to robots with the help of improved simulation and data pipelines. Faster, more scalable simulation reduces the cost of generating the contact-rich experience that pure real-world data collection cannot provide at sufficient volume.

## Implications for the Field

By open-sourcing a high-performance solver, Skild and NVIDIA lower the barrier for academic and commercial teams that want to train more generalist policies. Researchers can now more easily run large heterogeneous batches, explore self-play or other post-training methods, and iterate on environments without being as constrained by simulation throughput.

Limitations remain. Stiff contact modeling and certain sensor support features still require careful tuning for some manipulation workloads. Real-world transfer continues to depend on domain randomization, accurate system identification, and real-robot data. Nonetheless, the measured speedups represent a meaningful step toward the simulation scale needed for foundation-model-level robotics training.

## Looking Ahead

Steel’s release is part of a larger trend of open infrastructure for physical AI. As coding agents and research tools make it easier to generate new simulation environments automatically, the ability to run those environments efficiently becomes a critical differentiator. Teams that adopt improved solvers can explore more design space and generate more diverse training data in the same compute budget.

Skild has indicated that Steel is intended as a shared foundation and is accepting contributions. Further integration with Isaac Lab and additional community benchmarks will clarify long-term performance characteristics and identify remaining gaps.

In the near term, the combination of open high-throughput simulation, improving foundation models, and growing real-world deployment data is expected to accelerate progress on dexterous manipulation and multi-robot systems. Steel provides one concrete piece of that infrastructure.

## Sources and References

1. Skild AI GitHub: steel repository (November 9, 2026). https://github.com/skild-ai/steel
2. Skild AI: Steel: Scaling Simulation Across Robots, Tasks, and Worlds. https://www.skild.ai/steel
3. NVIDIA Blog coverage of Skild AI collaboration (prior related work). https://blogs.nvidia.com/blog/skild-ai-s1-physical-ai/
4. Independent benchmarks and community reports confirming performance (November 2026).
5. OpenReview paper draft: Steel: Simulation for Generalist Robot Learning.

*Article compiled from public announcements, repository documentation, and contemporaneous technical reports. Images sourced from Pixabay under free license.*