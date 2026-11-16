![Robot hand interacting with objects](https://cdn.pixabay.com/photo/2025/01/26/01/04/robot-9359999_640.png)
*Image: Robotic hand illustration. Source: Pixabay (wolfofart), free under Pixabay Content License.*

# LingBot-Touch: Robbyant Open-Sources a Unified Tactile Model for Dexterous Robot Hands

**Published: November 15, 2026**

Vision has dominated robotics progress for years, but touch remains a critical missing sense for reliable manipulation of everyday objects. On November 10, 2026, Robbyant—the embodied AI unit within Ant Group—open-sourced LingBot-Touch, a tactile foundation model that converts signals from different sensor types into a shared representation usable by robot control policies. Pre-trained on nearly 5,000 hours of real tactile data, the model has demonstrated meaningful gains in task success across multiple hands and policies.

### The Heterogeneous Sensor Problem

Tactile sensors come in several incompatible forms: magnetic, visuotactile (optical), and piezoresistive. Data collected on one type rarely transfers cleanly to another, forcing teams to retrain or redesign pipelines for each hardware platform. LingBot-Touch addresses this with a JEPA-style architecture centered on a shared Haptic Transformer. It predicts latent representations from spatiotemporal tactile context, producing plug-and-play tokens that can be fed into existing action models.

The pre-training corpus includes approximately 4,983 hours of recordings, 464,000+ episodes, and over a billion frames from both human-worn tactile gloves and teleoperated robot hands. This mix helps the model learn generalizable features rather than sensor-specific quirks.

### Measured Gains on Real Tasks

Robbyant evaluated the model on 26 real-world manipulation tasks using two dexterous hands (Sharpa Wave and XHand) and four action policies (LingBot-VLA, π0.5, Diffusion Policy, and T-Rex). Adding LingBot-Touch features improved average success rates by roughly 14 to 26 percentage points compared with no-touch baselines. In one highlighted example—unscrewing a bottle cap with T-Rex controlling a Sharpa Wave hand—success rose from 56.25% without touch to 62.5% with raw sensor signals and 90% with LingBot-Touch representations.

The lightweight LingBot-Touch-Tiny variant contains only about 5.3–5.46 million parameters and adds less than 0.2% to the size of the host action models, supporting high-frequency inference inside control loops. Cross-hardware transfer was also demonstrated: the model worked on an XHand magnetic sensor type that was not present in the original pre-training set (magnetic data had come from human gloves).

### Broader Implications for Physical AI

Reliable touch perception is essential for tasks involving force modulation, slip detection, deformable objects, and fine assembly. Combined with advances in vision-language-action models (such as Gemini Robotics 2.5) and world-action models, unified tactile representations reduce the data and engineering burden of giving robots a sense of touch. The Apache 2.0 release of code and weights lowers the barrier for researchers and companies to experiment and integrate tactile feedback.

Challenges remain, including the need for more independent replications, performance across wider object sets and environmental conditions, and seamless fusion with vision and force-torque sensing. Nevertheless, open tactile foundation models mark a practical step toward robots that can handle the variability of real industrial and household environments without exhaustive per-task programming.

**Helpful tips:**
- When evaluating tactile systems, compare success rates with and without the representation model on the same sensors and tasks.
- Lightweight encoders (a few million parameters) are more practical for real-time control than large models.
- Open-source releases enable rapid testing across different robot hands—prioritize platforms with documented cross-sensor transfer.

### Sources and References
- Robbyant LingBot-Touch technical page, GitHub repository (Robbyant/lingbot-touch), and arXiv preprint.
- Coverage from Robotics & Automation News, Humanoids Daily, Pandaily, The Robotics Media, and CellCog on training data, architecture, and evaluation results (November 10–15, 2026).
- Reported metrics: ~5,000 hours pre-training, 14–26 percentage point gains on 26 tasks, 90% bottle-cap example.

*Results are as reported by Robbyant and summarized in independent coverage; further third-party validation is expected.*
