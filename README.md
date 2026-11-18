# Physical AI: glossary, reading list and numbers

I am Max Versace. I have spent about 25 years building brains for machines: first in a lab at Boston University, then at Neurala, now at Analog Devices. People keep asking me what Physical AI means, what to read, and which numbers matter. So I wrote it down.

This repository is a copy of three pages from my site, in formats that are easy to reuse:

| File | What it is | Original page |
|---|---|---|
| [`glossary.csv`](glossary.csv) | 26 terms in plain words | [https://maxversace.com/physical-ai-glossary](https://maxversace.com/physical-ai-glossary) |
| [`numbers.csv`](numbers.csv) | 7 numbers, each with its source | [https://maxversace.com/physical-ai-in-numbers](https://maxversace.com/physical-ai-in-numbers) |
| Reading list (below) | Twelve papers, in the order they were written | [https://maxversace.com/physical-ai-reading-list](https://maxversace.com/physical-ai-reading-list) |

The pages on the site are the ones I keep up to date. Start here: [https://maxversace.com/physical-ai](https://maxversace.com/physical-ai).

This is my personal work. Views are my own and do not represent my employer.

## Glossary

**[Physical AI](https://maxversace.com/physical-ai-glossary#physical-ai)**. Artificial intelligence that perceives, learns and acts in the physical world, inside a machine with a body, sensors, motors and a limited power budget. A chatbot can take a few seconds to answer and nothing bad happens. A robot arm, a drone or a rover cannot.

**[Physical intelligence](https://maxversace.com/physical-ai-glossary#physical-intelligence)**. What a machine has to understand to get things done in the real world: where things are, how they move, what happens if it pushes, grabs or lets go. Animals have it long before they have language. Most AI today has it the other way around.

**[Embodied AI (embodied intelligence)](https://maxversace.com/physical-ai-glossary#embodied-ai)**. AI that learns and acts through a body. The body is not a detail: it gives the system constant feedback and punishes bad predictions right away. The term comes from robotics and cognitive science, and it overlaps almost completely with Physical AI.

**[Edge AI](https://maxversace.com/physical-ai-glossary#edge-ai)**. AI that runs on the device itself (a camera, a phone, a robot) instead of a data center. I like to say that Edge AI is not a place, it is a constraint: what counts is how much latency, power, memory and connectivity you can afford.

**[Latency](https://maxversace.com/physical-ai-glossary#latency)**. The delay between sensing something and acting on it. For a chatbot, a second is fine. For a robot catching a falling glass, a tenth of a second is already too late. In Physical AI, latency is part of the spec.

**[Sim2Real (simulation to reality)](https://maxversace.com/physical-ai-glossary#sim2real)**. Training a robot in a simulated world, then running it in the real one. Simulation is cheap and safe, and you can run a thousand experiments overnight. The catch is the gap: leave friction or sensor noise out of the simulator and the robot becomes a champion of a world that does not exist.

**[Digital twin](https://maxversace.com/physical-ai-glossary#digital-twin)**. A virtual copy of a real machine, factory or environment, kept up to date with data from the real thing. In robotics it is used to test and train before touching the hardware.

**[World model](https://maxversace.com/physical-ai-glossary#world-model)**. A model, learned from data, that predicts what will happen next in the world, including what happens if the machine takes a certain action. Brains do this all the time. It lets a robot try things in its head before trying them with its arm.

**[Robot foundation model](https://maxversace.com/physical-ai-glossary#robot-foundation-model)**. A large model trained on data from many robots and many tasks, meant to be a general starting point for new robots and new jobs, the way large language models are for text.

**[Vision-language-action (VLA) model](https://maxversace.com/physical-ai-glossary#vla)**. A model that takes camera images and an instruction in plain language ("put the cup on the shelf") and outputs the robot’s movements directly. It is the current favorite recipe for general-purpose robots.

**[Teleoperation](https://maxversace.com/physical-ai-glossary#teleoperation)**. A person driving a robot remotely, often to collect examples of how a task should be done. A lot of today’s robot training data comes from people wearing headsets and moving robot arms by hand.

**[Dexterous manipulation](https://maxversace.com/physical-ai-glossary#dexterous-manipulation)**. Handling objects with fingers the way people do: turning a key, folding a shirt, picking a raspberry without crushing it. It is one of the hardest open problems in robotics, because it mixes vision, touch and very fast control.

**[Sensor fusion](https://maxversace.com/physical-ai-glossary#sensor-fusion)**. Combining signals from several sensors (cameras, touch, sound, motion, position) into one picture of what is going on. No single sensor is reliable all the time. Together they can be.

**[Humanoid robot](https://maxversace.com/physical-ai-glossary#humanoid)**. A robot with a human-like shape: two legs, two arms, a head. The shape fits a world built for people. But a human shape does not mean a human mind... building the brain is the hard part, not the body.

**[Continual learning (lifelong learning)](https://maxversace.com/physical-ai-glossary#continual-learning)**. Learning new things over time, one at a time, without retraining from scratch and without losing what was learned before. Animals do it from birth. For most AI it is still an open problem, and for machines in the field it is a daily need.

**[Catastrophic forgetting](https://maxversace.com/physical-ai-glossary#catastrophic-forgetting)**. What happens when a neural network learns something new and, in the process, wipes out what it knew before. You learned a new face this morning and you still remember your mother’s. Many networks cannot say the same.

**[Backpropagation](https://maxversace.com/physical-ai-glossary#backpropagation)**. The standard way to train deep networks: measure the error at the output and send corrections backward through every layer. It works very well in a data center. It is heavy, slow and hungry, which makes it a poor fit for learning on a small device.

**[Adaptive Resonance Theory (ART)](https://maxversace.com/physical-ai-glossary#art)**. A family of brain models, started by Stephen Grossberg in the 1970s and developed with Gail Carpenter, in which learning happens only when what comes in from the senses matches what the brain expects. That match-first rule is what lets the system learn new things without erasing old ones.

**[Mismatch negativity](https://maxversace.com/physical-ai-glossary#mismatch-negativity)**. A dip in the brain waves (EEG) that shows up roughly a tenth to a quarter of a second after something unexpected, like an odd tone in a series of identical ones. It is a visible trace of the brain’s prediction being wrong.

**[Neuromorphic computing](https://maxversace.com/physical-ai-glossary#neuromorphic)**. Chips and systems designed to work like nervous systems: many simple units, memory sitting next to computation, activity only when something happens. The name goes back to Carver Mead in the late 1980s. The promise is a lot of intelligence on very little power.

**[Spiking neural network](https://maxversace.com/physical-ai-glossary#snn)**. A neural network whose units talk through short pulses (spikes), like real neurons, instead of continuous numbers. If nothing changes, nothing fires and almost no energy is spent.

**[Spike-timing-dependent plasticity (STDP)](https://maxversace.com/physical-ai-glossary#stdp)**. A learning rule found in real synapses: if one neuron fires just before another, the connection between them gets stronger; if it fires just after, weaker. It uses only local information, which makes it a natural fit for hardware.

**[Memristor](https://maxversace.com/physical-ai-glossary#memristor)**. An electronic component whose resistance depends on the current that has flowed through it, so it remembers its past. Proposed by Leon Chua in 1971 and built at HP Labs in 2008. It behaves a little like a synapse, which is why we used it for brain-inspired hardware.

**[In-memory computing](https://maxversace.com/physical-ai-glossary#in-memory-computing)**. Doing the computation where the data is stored, instead of shuttling data back and forth between memory and processor. That shuttling is where much of a computer’s energy goes. Brains never had the problem: synapses store and compute in the same place.

**[Biological intelligence](https://maxversace.com/physical-ai-glossary#biological-intelligence)**. The kind of intelligence that evolved in animals. It runs on very little energy, learns all the time from a handful of examples, and exists to keep a body alive in a world that keeps changing. It is the benchmark I measure AI against: a squirrel on a few nuts a day still beats most robots.

**[Leaky integrator](https://maxversace.com/physical-ai-glossary#leaky-integrator)**. The simplest useful model of a neuron: it adds up its inputs over time, and the total slowly leaks away when nothing new arrives. I promised no equations, so this is the only one: dx/dt = −Ax + I, where x is the activity, I the input and A how fast it leaks. Most models of spiking neurons start here.

## Numbers

| Number | What it is | Source |
|---|---|---|
| About 20 watts | The energy budget of the human brain. The same paper notes that the computer it was typed on needed 80 watts. | [Balasubramanian, “Brain power”, PNAS, 2021](https://pmc.ncbi.nlm.nih.gov/articles/PMC8364152/) |
| 86 billion | Neurons in the human brain, with about as many non-neuronal cells. | [Herculano-Houzel, PNAS, 2012](https://pmc.ncbi.nlm.nih.gov/articles/PMC3386878/) |
| 415 TWh | Electricity used by data centres worldwide in 2024, about 1.5% of global consumption. | [IEA, Energy and AI, 2025](https://www.iea.org/reports/energy-and-ai/executive-summary) |
| About 945 TWh | Projected data centre consumption in 2030: more than double. | [IEA, Energy and AI, 2025](https://www.iea.org/reports/energy-and-ai/executive-summary) |
| 542,000 | Industrial robots installed worldwide in 2024. | [IFR, World Robotics 2025](https://ifr.org/ifr-press-releases/news/global-robot-demand-in-factories-doubles-over-10-years) |
| 4,664,000 | Industrial robots operating in factories worldwide in 2024, up 9% on the year before. | [IFR, World Robotics 2025](https://ifr.org/ifr-press-releases/news/global-robot-demand-in-factories-doubles-over-10-years) |
| 54% | China’s share of the robots installed in 2024. | [IFR, World Robotics 2025](https://ifr.org/ifr-press-releases/news/global-robot-demand-in-factories-doubles-over-10-years) |

## Reading list

I never send people the latest paper. I send them the old ones... the questions were asked decades ago, mostly by people looking at brains and at stubborn robots. Twelve papers, in the order they were written. Only one is mine.

- **[1987: A massively parallel architecture for a self-organizing neural pattern recognition machine](https://doi.org/10.1016/S0734-189X(87)80014-2)**. Carpenter & Grossberg, Computer Vision, Graphics, and Image Processing. The first full Adaptive Resonance Theory network. The question it asks is still the one I care about most: how does a system keep learning new things without erasing the old ones? The answer here is to learn only when the input matches what the network expects.
- **[1989: Catastrophic Interference in Connectionist Networks: The Sequential Learning Problem](https://doi.org/10.1016/S0079-7421(08)60536-8)**. McCloskey & Cohen, Psychology of Learning and Motivation. Two psychologists teach a network its additions one set at a time, and watch the earlier ones fall apart. The paper gave the problem its name. Thirty-seven years later it is still on the to-do list.
- **[1990: Neuromorphic electronic systems](https://doi.org/10.1109/5.58356)**. Mead, Proceedings of the IEEE. Carver Mead makes the case for building electronics the way nervous systems are built. Read it for the argument about energy… it has aged very well.
- **[1991: Intelligence without representation](https://doi.org/10.1016/0004-3702(91)90053-M)**. Brooks, Artificial Intelligence. Rodney Brooks argues that you get to intelligence by building complete creatures that act in the real world, one simple layer of behavior at a time. Half the field was annoyed. The robots worked.
- **[1995: Why there are complementary learning systems in the hippocampus and neocortex](https://doi.org/10.1037/0033-295X.102.3.419)**. McClelland, McNaughton & O’Reilly, Psychological Review. Why does the brain have a fast learner and a slow one? Because one system cannot do both jobs without tripping over itself. This is the biology behind what engineers now call replay.
- **[1999: Predictive coding in the visual cortex](https://doi.org/10.1038/4580)**. Rao & Ballard, Nature Neuroscience. Higher visual areas predict what lower areas should be seeing, and only the errors travel upward. If you want one paper on the brain as a prediction machine, this is the one I hand out.
- **[2008: Spikes, synchrony, and attentive learning by laminar thalamocortical circuits](https://doi.org/10.1016/j.brainres.2008.04.024)**. Grossberg & Versace, Brain Research. The one I co-wrote, so discount accordingly. It is a model of how the layers of the cortex and the thalamus work together to decide when to learn and when to hold still. Long, and not a beach read.
- **[2017: Overcoming catastrophic forgetting in neural networks](https://doi.org/10.1073/pnas.1611835114)**. Kirkpatrick et al., PNAS. The paper that put forgetting back on the agenda of deep learning. The idea: find the connections that mattered for the old task and make them harder to change.
- **[2017: Domain Randomization for Transferring Deep Neural Networks from Simulation to the Real World](https://arxiv.org/abs/1703.06907)**. Tobin et al., IROS 2017. A lovely trick. Make the simulator look wrong in thousands of different ways (colors, lights, textures) and the real world becomes just one more variation.
- **[2018: World Models](https://arxiv.org/abs/1803.10122)**. Ha & Schmidhuber, arXiv. An agent learns a small model of its world and then practices inside it. Brains rehearse too. Short, clear, and with pictures.
- **[2023: RT-2: Vision-Language-Action Models Transfer Web Knowledge to Robotic Control](https://arxiv.org/abs/2307.15818)**. Brohan et al., arXiv. Take a model trained on images and text from the web and have it output robot actions. This is where “vision-language-action” became the recipe everybody talks about.
- **[2023: Open X-Embodiment: Robotic Learning Datasets and RT-X Models](https://arxiv.org/abs/2310.08864)**. Open X-Embodiment Collaboration, arXiv. Many labs pool the data from their very different robots and train one model on all of it. The interesting result is that robots can learn from other robots’ experience.

If you have one evening: Brooks (1991), then McCloskey and Cohen (1989), then RT-2 (2023).

## More

- [Physical AI: what it is and why it matters](https://maxversace.com/physical-ai)
- [Continual learning for robots](https://maxversace.com/continual-learning-for-robots)
- [Physical AI vs generative AI](https://maxversace.com/physical-ai-vs-generative-ai)
- [Physical AI vs embodied AI vs robotics](https://maxversace.com/physical-ai-vs-embodied-ai-vs-robotics)
- [Physical AI FAQ](https://maxversace.com/physical-ai-faq)
- [My publications](https://maxversace.com/publications)

## How to cite

Versace, M. (2026). *Physical AI Glossary*. https://maxversace.com/physical-ai-glossary

You are welcome to quote and reuse this material. Please credit Max Versace and link to the original page. If you think a term or a paper is missing, open an issue or [tell me](https://maxversace.com/contact-max-versace).
