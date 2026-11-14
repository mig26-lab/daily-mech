# ASUS Gallop Humanoid Begins Real Factory Work, Targets Commercial Availability in 2028

![Humanoid robot in modern warehouse](https://cdn.pixabay.com/photo/2026/03/14/02/39/tungart7-robot-10172923_640.jpg)
*Image from Pixabay under free Content License. Source: [Pixabay](https://pixabay.com/photos/robot-humanoid-warehouse-automation-10172923/)*

ASUS has detailed its first humanoid robot, Gallop, which is already learning a production task on one of the company’s own electronics manufacturing lines. Announced publicly around November 13, 2026, the robot is packing motherboard accessories—15 small parts per board, many in thin transparent bags—at a station designed for human workers. ASUS has set an ambitious target of 99.5% success within a 20-second cycle time, matching human pace.<grok type="render_inline_citation" citation_id="95" />

Unlike many humanoid demonstrations that focus on staged mobility or lab tasks, ASUS is emphasizing factory-proven reliability from the start. The program, which began in early 2026, operates under the Humanoid Robotics business unit within ASUS’s Physical AI Solutions Business Group.

## Design and Learning Approach

Gallop currently uses a fixed base with two arms for stationary pick-and-place work. It runs on a single NVIDIA Jetson AGX Thor computer. ASUS is developing its own dexterous hand with tactile sensing, which has not yet been integrated; a wheeled mobile base is also planned.

The robot learns through a combination of methods: head-camera footage of human workers performing the task, simulation, and VR teleoperation for guidance. Software is organized in four layers: a planner that interprets the scene and breaks work into steps, an AI supervisor that monitors progress and replans after failures, a skills layer for reaching/grasping/placing, and a low-level control layer that executes precise motions and stops on errors.

ASUS has stated that it starts from open AI models rather than training everything from scratch and focuses on making the robot reliable at existing human workstations rather than requiring custom infrastructure.

## Timeline and Commercial Plans

Customer pilots are planned for 2027, with a demonstration expected at Computex 2027. Market availability is targeted for the second half of 2028, initially for electronics manufacturing, with later expansion into hospitals and service environments. Co-CEO S.Y. Hsu has discussed the robot on CNBC, reinforcing the company’s commitment to physical AI.<grok type="render_inline_citation" citation_id="100" />

No pricing or full specifications have been released. The company has emphasized that a factory needs a robot that performs the job every day, not just once in a demo, and is measuring progress against that standard.

## Broader Humanoid Momentum

Gallop joins a growing set of humanoids moving into real industrial settings in late 2026. Logistics provider GXO has been reported as planning deployments of up to 1,000 Apptronik Apollo humanoids. Other manufacturers are testing units on production lines, and research continues on general-purpose models that can control robots with less specialized training.

NVIDIA’s GR00T 2 and related robotics foundation models, along with improved simulation tools, are supporting these efforts. The combination of capable onboard compute (such as Jetson Thor), better hands, and learning pipelines that mix human demonstration with simulation is making station-level tasks more tractable.

Challenges remain. Success rates on novel or slightly varied tasks, long-term reliability, safety certification, and total cost of ownership will determine how widely humanoids are adopted versus traditional automation. ASUS’s decision to validate first on its own line provides a controlled environment in which to collect data and iterate before external pilots.

## Implications

If Gallop reaches its reliability and cycle-time targets, it demonstrates that humanoid form factors can be applied to existing human workstations without major facility redesigns. This approach contrasts with systems that require dedicated cells or extensive fixturing. For electronics manufacturers facing labor constraints or seeking flexibility, such robots could address repetitive packing and assembly tasks.

The 2027–2028 timeline is realistic given the current state of the technology. Many companies are still in the pilot or limited-deployment phase. Real factory data from programs like Gallop will be valuable for the wider community, whether or not the specific hardware becomes widely available.

## Looking Ahead

ASUS plans to integrate its tactile hand and add mobility over the coming year. Progress updates against the 99.5%/20-second target will be the most useful metric. Broader industry interest in physical AI continues to rise, supported by advances in simulation, foundation models, and edge compute.

Gallop is one example of companies applying AI and robotics to their own operations first. Success would strengthen the case for humanoids in electronics manufacturing and potentially other sectors that share similar station-based work.

## Sources and References

1. ASUS Pressroom: Factory-Proven Physical AI: Why ASUS Is Building a Humanoid Robot (November 13, 2026). https://press.asus.com/blog/factory-proven-physical-ai-asus-gallop-humanoid-robot/
2. Humanoids Daily: ASUS Unveils Gallop, Its First Humanoid Robot, Already Packing Parts on Its Own Production Line (November 13, 2026). https://www.humanoidsdaily.com/news/asus-gallop-humanoid-robot-jetson-thor-2028
3. Unite.AI and other contemporaneous coverage of Gallop details (November 2026).
4. CNBC interview with ASUS Co-CEO on the humanoid program (November 2026).
5. Related industry reports on Apptronik, GXO, and humanoid deployments.

*Article compiled from public company statements and contemporaneous reporting. Images sourced from Pixabay under free license.*