# The Why, What and How of Artificial General Intelligence Chip Development

Alex James, IEEE Senior Member 

Abstract—The AI chips increasingly focus on implementing neural computing at low power and cost. The intelligent sensing, automation, and edge computing applications have been the market drivers for AI chips. Increasingly, the generalisation, performance, robustness, and scalability of the AI chip solutions are compared with human-like intelligence abilities. Such a requirement to transit from application-specific to general intelligence AI chip must consider several factors. This paper provides an overview of this cross-disciplinary field of study, elaborating on the generalisation of intelligence as understood in building artificial general intelligence (AGI) systems. This work presents a listing of emerging AI chip technologies, classification of edge AI implementations, and the funnel design flow for AGI chip development. Finally, the design consideration required for building an AGI chip is listed along with the methods for testing and validating it. 

Index Terms—Artificial General Intelligence, AI hardware, Edge AI, AI chips 

# I. INTRODUCTION

HE quest for building an artificial brain developed the field of computers and artificial intelligence. The machine that could mimic human intelligence has been proven to be a hard problem. Most of the general intelligence problems are AI-hard [1] and require the rethinking of AI architectures and hardware if artificial general intelligence (AGI) chip were to be developed. 

The weak-AI [2] is defined as those AI systems that are designed for specific applications. For example, the task of face recognition and detection is a weak-AI task. The same AI system cannot be used for another application without retraining and at a time can only process a handful of tasks. Most of the current AI systems attempt weak AI problems. There is a lot of practical use and application of the weak-AI systems, and they are the first step towards realizing general intelligence. 

In contrast, the strong AI systems [3]–[5] aim to overcome the limitations of weak-AI by incorporating general intellectual abilities. The environmental awareness and innate knowledge, along with learning abilities enable understanding of various rules, policies, social behavior to ethical aspects. This target abilities make the best benchmark known today for strong AI systems to be that of human intelligence. 

The competition to build an AGI system in a machine is largely approached in algorithmic and software ways using traditional digital computers and servers [3], [4], [6], [7]. The 

A. P. James is a Professor of AI and Electronics at Centre for Artificial General Intelligence and Neuromorphic Systems, Kerala University of Digital Sciences, Innovation and Technology (KUDSIT), and the in-charge of the Maker Village - Indian Institute of Information Technology and Management, Kerala. Email: apj@ieee.org 

recent approaches such as using $Z ^ { * }$ -numbers [8] provides an architectural and algorithmic framework for realising realtime perception, and attention functions. Such approaches are relatively easier to translate to digital systems, while the analog/mixed-signal implementations could require extensive hardware design investigations. Building autonomous AGI machines even with existing low power AI chips would require complex interface electronics, high computing capacity, and infrastructure. Suppose, we would like to build a robot as a football player that has AGI capability. The primary concerns would be that of energy efficiency, real-time response times, fast decision making skills, and agility. Increasingly, many such functions are achievable with biomimicry and sensing control circuits, however, they do not match up with equivalent energy efficiency, robustness, generalisation ability and adaptive behaviour of biological systems. 

The energy-efficient AI chips build by mimicking neural networks and with many emerging devices have shown promising results [9]–[13]. Most, if not all, AI chips on the market today including those aim towards early AGI natives are good at solving one or other weak-AI problems, at much lower energy and on-chip area compared to serverbased alternatives. Since the processing is done within the edge devices, the response times improve and it becomes closer to being suitable for real-time use. However, they do not address the issue of general intelligence in hardware, and often address this question today from a philosophical and algorithmic perspective. In this process, the AI chip is often seen as having an accelerator or speed role [14], rather than seeing it as the primary building block for general intelligence. 

This paper presents a critical overview of the emerging field of hardware AI focusing on developing AGI chips. The origin of general intelligence is presented relative to the understanding of intelligence from a cross-disciplinary perspective. The concept of edge intelligence, followed by the development approaches for AGI chip and how it can be tested, is proposed. This work’s primary goal is to bring in a convergence of important ideas from AI research that can be useful for AGI chip development. We ask the questions of Why and What to connect the theory of intelligence with that of AI hardware, placing this as building principle blocks of AGI chips. The question of How aims to uncover the practical aspect of designing, testing, and validating the AGI chips when developed. 

The paper is organized into nine sections. Section II introduces the concept of intelligence and its linkages to building AI machines. Section III gives an overview of edge AI differentiating and categorizing it based on functional executions of AI operations. Section IV and V provides insight into 

building blocks for an AGI system. Section VI introduces a law of funnel design in AGI chip. Section VII proposes how AGI chips can be tested, Section VIII provides discussion and classification of AGI development. In summary, Sections II-III addresses the question of Why and What, while the Section IV-VIII addresses the question of How in AGI chip development. Finally, Section IX provides the main conclusions. 

# II. TOWARDS INTELLIGENCE IN HARDWARE

This section aims to provide a broader context and meaning of intelligence inspired by human brain understanding (Section IIA-B). Further, the transition of intelligence understanding useful for AGI is reflected through the recent efforts on implementing AI chips and emerging hardware systems (Section IIC-D). 

# A. Definition of Intelligence

Different definitions of intelligence exists today in the literature. There are variations in the way intelligence is perceived by one scientific community to another, with no formal definition that is universally accepted. In context of machine intelligence, Legg and Hutter’s [15] definition - ”Intelligence measures an agent’s ability to achieve goals in a wide range of environments.” - stand-out as a prominent one that in essence defines intelligence as an agent’s ability to perform a set of task and achieve goals in a diverse set of environments. 

The agent can be implemented in the form of a software or hardware or more likely a combination of both in AI hardware perspective. Such agents if they were to survive diverse challenges would need the ability to reason, plan, solve problems, think abstractly, comprehend complex ideas, learn quickly and learn from experience. In essence these agents will require the ability to sense, react and respond to the environmental conditions. This would mean, the agent should be able to generalise, understand and act upon a wide range of situations, typical of intelligent decision making capability of humans. This form of general intelligence originates from the ability to comprehend and survive in diverse set of environmental conditions. Further, individual tasks can be executed in logic operations and rules programmable with minimalist learning. In cognitive studies, the idea of generality and purpose drive intelligence map to the theory of fluid and crystallized intelligence (as explained in chapter five of the book [16]), while, holding a deeper link and connection to the ideas of mind. There are two floating ideas of mind, (1) being bounded by evolution that makes it very deterministic and with limited ability to learn, and (2) being an unbounded general purpose system that can learn and solve any problem (see pp. 89 in [17]). 

The agents ability to perform a set of tasks are relatively easier to quantify and evaluate in AI studies, that can be implemented as application driven assessments. On the other hand, the idea of generality however, is unbounded by the conditions presented to the intelligent system, and are harder to quantify and evaluate. 

# B. Understanding Intelligence

There are in totality three different yet broad approaches that have been followed in the past to understand intelligence. They are, (1) based on the principle of evolution, (2) that of philosophy of generality, and (3) as a result of studies in developmental and cognitive psychology. 

1) Evolution-driven intelligence: The idea that intelligence is evolution driven (as explained in [18], [19]), and general theory on that ability to solve a problem is derived from the task specific adaptions [20] makes it a compelling case for machine intelligence. As pointed out in [20] (pp. 514) - ”then any genetic mutation that equips its carrier to think and reason would be selected for and could evolve as a domain-specific adaptation in order to solve novel, nonrecurrent problems”, this, in essence, one can think this as divide and conquer approach where a complex task is divided into several subtasks, allowing domain specific evolution. If an AI system can solve each sub-task individually, it is assumed that it can solve the cumulatively resulting complex task. 

In terms of AI hardware, this can be considered as a modular approach to build higher form of intelligence. For example, each AI circuit block within a chip could be fine-tuned to solve a specific problem such as image recognition, object recognition, and speech recognition. Several such blocks together forms an AI chip that can then collectively solve a complex problem that make use of multi-modal analysis and decisions performed by individual blocks. The task specific adaptations in this case would need memory and rules to make it work, which should be provided by humans. The idea of learning in this case is highly simplified to specific tasks under strict constraints. This idea is in firm alignment with that of the Minsky’s view of AI (for example chapter 3-4 in [21]), in explaining language processing and semantic understanding. Where the science of building AI was coupled to the set of tasks the humans program it to do. Hence, indirectly mapping the human skills and knowledge to a deterministic and organised representations of rules and memory becomes the norm. 

2) Generalisation-driven intelligence: The idea of generalisation gives a bigger importance to adaptation and learning. In this approach, the intelligence development is envisioned as the ability of the system to learn new tasks, and solve problems that are unknown previously to the system. The pioneers like Turing, McCarthy and Papert were first few to extensively envision the generalisation view of intelligence [21], [22]. This is pointed out by McCarthy during the 1971 Turing Award Lecture [22] ”In my opinion, getting a language for expressing general commonsense knowledge for inclusion in a general database is the key problem of generality in AI”. 

Until the development of machine learning and deep learning systems, the evolutionary-driven intelligence dominated the field of AI. In present times, there is hardly any disagreement on the need to approach AI through learning and assess its ability to adapt to unknown problems. However, the immediate requirements in the AI industry are task specific applications, that often do not need high generalisation ability. 

The inculcation of many ideas from the past support towards this. The foremost from the AI literature is the ancient idea 

of Tabula Rasa [23], where the mind is considered as a blank slate, and anything can be written on it that is enriched by experiences in time. An untrained neural network can be considered as a ’Tabula Rasa’ in the sense that it can be trained to perform a given task through weight updating algorithms. Although, it may make sense to establish this correlation, it is an incorrect assumption given the various progress in the developmental studies related to intelligence contrast this. 

3) Human intelligence: Several studies from developmental psychology point out that both evolution and blank slate only approach to intelligence is wrong. Instead, the mind is capable of high degree of generality, not limited by innate skills and capable to acquire new skills throughout the life. At the same time, our cognitive abilities are specialised by evolution that is driven by biological priors and evolutionary limitations that dismantle ’blank slate’ theories as well. 

The fact that humans are capable of excelling in specific tasks and skills compared to many other animals are a testament to this. Understanding human cognitive priors are essential to developing human like intelligent forms. 

There are several priors that help humans perform intelligent tasks [24]. They can be grouped as: 

1) Motor-sensory priors: These are motor-sensory skills that humans are born with such as ability to move, react and respond to sensory inputs. The reflexes such as vestibulo-ocular reflex is a good example of this, where the head movements coordinate strongly with the eye movements. 

2) Meta-learning priors: These are the underlying strategies what define how we learn any tasks. For example, the idea of functional modularity, hierarchical information processing, spatio-temporal information coding, decoding and organisation can be classified under this. 

3) Knowledge priors: These priors gives a broader sense of the environment around us. For example, the shapes of objects, innate indication about space and depth, innateness of numbers, sense of time, and sense of social intuitions. 

The development of AI hardware that cater to only motorsensory priors such as using sensors and responses helps to imitate an artificial human body without general intelligence abilities. While, meta-learning priors form the key aspects of intelligence that enable learning and help solve problems, AI chips today make use of various forms of meta-learning priors, and are in constant effort to identifying newer and efficient learning implementations. In contrast, the knowledge priors help assess the AI chip implementations against human like intelligent tasks. The AI chips that could potentially include programmed number of knowledge priors could trick the specific test to show human like intelligence ability, however, they do not represent general intelligence, and such system should not considered as AGI systems. 

# C. From General Intelligence to AGI

AGI aims to embed general intelligence abilities in machines and are also known as ’full AI’ or ’strong AI’ systems [4], [5], [25]. There is no evidence of practical strong AI 

systems that exist today that matches fully with human like intelligence, although there have been active attempts to build libraries and software (e.g. see [26]) to build such systems. While, these software and libraries are essential to progress the AGI, they alone cannot achieve physical compactness and energy efficiency required for such complex systems. This is where, AGI chip development becomes important, where either they become supportive tool as an accelerator to algorithms or that can have innate priors embedded within its hardware. 

The knowledge priors are extensively used in testing AGI algorithms, by giving and comparing human-like challenges to AGI system. Examples include: (1) testing the AGI system by making it take a university program and obtaining a degree, (2) testing the ability of the AGI to perform in a job, (3) testing the ability of AGI system to make a coffee, and (4) perform Turing test [5], [27]–[30]. 

The AGI system should be able to solve ’AI-hard’ problems [31], [32], that would require the use of natural language processing, computer vision, and understand images, emotions, and environment. With the current state of the art AI system, solving an AI-hard problem requires the assistance of humans in addition to the acceleration provided by computing machines. 

Majority of AI methods aim to mimic the functional and/or structural behavior of the neural networks. The functional understanding of brain is emulated through knowledge representation, statistical models and complex networks. Mimicking biology driven human intelligence will require the application of the concepts of feedback and feedforward propagation of information, and integration of sensing mechanisms, along with meta-learning priors and knowledge functions specific to tasks. 

The brain is considered as the benchmark system for AGI research. There are many approaches in neuromorphic computation that aim for achieving energy efficiency and performance benchmarks of the brain [33], [34]. The performance of the AI systems has considerably improved due to the availability of high-performance computers and excessive capturing of labeled data. As more and more sensors are connected to the devices, the volume, veracity, and velocity of data increase. The deep learning architectures [35] can use the data to arrive at improved classification and recognition accuracy. 

# D. AI Hardware

The neuromorphic computing is inspired by the information processing in a human brain by mimicking the operation principle and structure of the neurons and synapses (Figure 1 (a)). Low power intelligent information processing is a key concept in neuromorphic computing inspired by the human brain which performs complex processing tasks consuming nearly $2 0 \mathrm { ~ W ~ }$ of power. The first task-specific neuromorphic systems have been developed for specific applications, such as object recognition or prediction of specific data. The second generation of the neuromorphic systems is moving towards the tasks corresponding to human cognition, like adaptation and interpretation of the unknown information, and a final goal of building strong AI systems [36], [37]. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-03-22/63b2b94d-c20b-4c10-b6e5-2ee4374abaf4/eab0c0e96ec66150961193a6631ba5365caf9b27633263071ca79545f6083568.jpg)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-03-22/63b2b94d-c20b-4c10-b6e5-2ee4374abaf4/1c7ca5fde8de807463b740c21c1ef24e56c1fba99f63f8343f5623aa763847b5.jpg)



(c)



ReRAM-based systems


![image](https://cdn-mineru.openxlab.org.cn/result/2026-03-22/63b2b94d-c20b-4c10-b6e5-2ee4374abaf4/55e6316b8e8b7bbc8175570560f7a915dc2f8976b9da28507c8cbde03c07eff9.jpg)



(d)



Fig. 1. An overview of hardware on-chip neural networks. (a) shows the key benchmarks for AI chip, (b) illustration of in-memory computing and applications, (c) SNN concept, (d) crossbar with ReRAM for implementing a layer of neural network.


1) Neuromorphic systems: There are numerous practical implementations of neuromoprhic chips. Some examples are HICANN, HICANN-X [38], SyNAPSE [39], SpiNNaker, SpiNNaker-2 [40], True North [41], Neurogrid [42], IFAT [43], ROLLS [44], DYNAP-SEL [45], Loihi [46] and SBNN [47]. Besides, CMOS devices have gained popularity in the recent years, and its practical realisation is also on the raise. 

The development of neuromorphic computing and architectures is facilitated by the scaling of the transistors and development of the emerging technologies, such as ReRAMs, PCMs, and STT-RAM, allowing to increase the density of the devices on-chip and reduce the power consumption [48]. Neuromorphic computing involves the acceleration of traditional computing architectures and the development of low power AI chips useful for edge devices and near-sensor processing (Figure 1 (b)). The acceleration of traditional architectures includes various accelerators, like spike-based processors [49], and in-memory computing architectures [50]. 

Among the emerging devices for building AI hardware, the class of non-volatile memory memristive devices stands out, as they have useful properties that mimic the neuron’s electrical behavior [51]. When a stimulus voltage pulses with a constant magnitude and time period are applied across the memristors over a period of time, the current output drops, indicating that there is an adaptive behavior. This correlates with single-neuron behavior, as it resembles neurons being able to learn a stimulus. Multiple memristor neurons can be 

arranged in a crossbar architecture [52], [53] and the voltage difference across the devices carefully tuned, to emulate a spiking neural network [54], [55]. Several configurations of the crossbar architectures are possible to emulate various known artificial neural networks such as multi-layered perceptron, deep neural network, convolutional neural network, long shortterm memory, and generative adversarial networks. 

The non-idealities of CMOS-memristive/emerging devices based crossbar systems include the scalability issues and leakage currents, non-linearity during programming, variabilities in resistive levels, limited number of stable resistive states, aging issues, drifting of resistive levels, device failures, endurance issues and limited lifetime of real memristive devices [56]– [58]. These make real-time learning with emerging devices to be a nontrivial task. This also implies the need to have smarter ways to train, program, and implement algorithms. 

2) Digital neural chips: The digital neural chips are the most established AI chip implementations for practical use. The synaptic nodes become purely digital when the ’multiply and accumulate’ (MAC) operation is implemented using digital logic. Some of the implementations are Diannao [59], Dadiannao [60], Pudiannao [61], Shidiannao [62], Eyeriss [63], EIE [64], Origami [65], Envision [66], TPU [67], Tesla, DPU, Q4MobilEye, Parker, S32V234, and Myriad 2 [68]. A distinct from CPU and GPU chips that are controlled by software algorithms, the digital neural chips uses dedicated hardware units for accelerating neural computations. 

The hardware performance of digital neural chips is assessed based on MAC operations per second (i.e. two floating point operations), throughput and clock frequency. Only about $10 \%$ of area in the chip is occupied by neurons, while the rest is occupied by memory units and control circuits. 

3) Other emerging systems: The carbon nanotube (CNT) along with thin film transistor (TFT) has been used to build synapsis. It is also feasible to fabricate 3D architecture of CNT TFTs logic with vertical metal oxide memristors (as non volatile memory (NVM)) and silicon logic [69], [70]. This approach show the possibility to have high package densities that could be used to scale up the neural network implementations. Another option is the use of semiconducting nanowires that demonstrate NVM properties [71]. 

Another post-CMOS strategy that is upcoming is the use of quantum computing. Recently, researchers started developing Noisy Intermediate Scale Quantum (NISQ) chips that aim to have 50-100 qubits [72]. The possibility for quantum chips to run several operations in parallel, inspire the design for quantum neural network. Attempts are made to build quantum neural network using silicon fabrication techniques, implemented on a NISQ chip with 170 control parameters in 2-by-5-millimeter area [73]. 

# III. EDGE AI CHIPS

# A. Integrated Edge AI Platforms

The intelligence at edge has been a major driver in the recent development of AI chips. Table 1 shows a collection of most popular hardware solutions for edge AI implementation available in the market today. Most, if not all, of the commercial solutions of Edge AI hardware, are based on digital and mixedsignal logic and include concepts of in-memory computing and parallel computations for speeding up the MAC operations. Like any hardware computing solutions, the AI chips differentiate in terms of performance issues resulting from memory bandwidth, multiple I/O channels, memory architecture, modularity and scalability of the computing/embedded AI architecture, parallel and pipelined architectures, and ability to easily map AI architectures into AI chips. 

Current research in neuromorphic computing and neural chips focuses on spiking neural networks and spike-based systems [74], probabilistic computing [75], [76] and ReRAM based networks (Figure 1 (c)). Such systems involve the development of analog and mixed-signal architectures which can also be useful for near-sensor processing, rather than being purely digital based designs. Spike-based systems rely on the spike-timing-dependent plasticity (STDP) principle of the neural computations [77]. The good examples of SNNbased chips are TrueNorth by IBM and Loihi by Intel. Probabilistic computing relies on the fundamentals of uncertainty and noise in the natural data processing. ReRAMbased networks mostly focus on the crossbar-based multiply and accumulate operations, while accelerating the processing with analog domain computation using low-power emerging devices. The advantages of such systems are small on-chip area, high-density computations, and low power consumption. However, the ReRAM based neuromorphic systems suffer 

from endurance and robustness issues, limited precision, and device variability as the technology is relatively new. Also, the development and fabrication cost of such a system can be high, as the technology has not become mature yet. 

The ability of the chips to handle large scale neural network architectures vary. As the number of neurons and layers in the architectures increases, it becomes challenging to run inference problems in real-time. Mainly, optimization of an architecture for a general-purpose AI hardware is not an easy problem, as the optimal configuration varies from one problem to another. Another well-known problem is that with an increase in architecture size, there is an increased need to store the weights and perform MAC computations. Almost, all general-purpose AI hardware is limited in both memory and computations, that limit and prevent implementation of large scale neural networks. 

# B. Types and purpose

The Edge AI and Edge computing are not the same. The purpose of edge computing systems is to off-load the computing from a cloud to devices on edge. In contrast, Edge AI is a subclass of edge computing that focuses on providing AI functions to the edge devices. The edge devices having AI functions can lead to faster real-time computations, saves energy, consume lesser bandwidth, and can improve the security of intelligent data processing. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-03-22/63b2b94d-c20b-4c10-b6e5-2ee4374abaf4/fd4adc03d727f8f0068a293da04e92581f1f6896ce7af199c9b906d4d460ca72.jpg)



Fig. 2. Edge AI implementation categories


There are different possibilities for have edge AI implemented as shown in Fig. 2. This can be classified in hardware contexts as: (1) On-device intelligence, (2) Near-device intelligence, and (3) Far-device intelligence. 

1) On-device intelligence: On-device intelligence can be defined as the set of methods that embed neural networks within the sensors and processing units. This can be a singlechip or multi-chip solution. A good example of this is inpixel processing or in general in-sensor processing, where the sensors contain neural circuits that enable them to perform intelligent operations. Another example is a smart camera, where the sensor and co-processor can be separate units, 


TABLE I POPULAR COMMERCIAL SOLUTION AVAILABLE FOR EDGE AI HARDWARE


<table><tr><td rowspan="2">Solution</td><td colspan="5">Specification</td></tr><tr><td>Processor</td><td>Memory</td><td>Power</td><td>Speed</td><td>Size</td></tr><tr><td>Coral Dev Board</td><td>TPU</td><td>1GB RAM + 8BG flash memory</td><td>0.5W per TOPS (2 TOPS per W), USB (5V)</td><td>4 TOPS</td><td>48mm×40mm×5mm</td></tr><tr><td>Jetson TX2</td><td>Embedded GPU</td><td>8 GB RAM + 32 GB Flash Memory</td><td>7.5-15W</td><td>1.3 TFLOPS</td><td>87mm×50 mm</td></tr><tr><td>Jetson Nano</td><td>Embedded GPU</td><td>4 GB RAM + 16 GB Flash Memory</td><td>5-10 W</td><td>0.5 TFLOPs</td><td>69.6mm×45mm</td></tr><tr><td>Intel Movidius Neu-ral Compute Stick</td><td>High Performance VPU (vision processing unit)</td><td>1 GB RAM + 4GB Flash memory</td><td>1W</td><td>The USB3 interface- Super Speed (5 Gbps) or High Speed (480 Mbps) modes</td><td>72.5mm×27mm×14 mm</td></tr><tr><td>Raspberry Pi 4</td><td>Quad core 64-bit ARM-Cortex A72</td><td>1, 2 and 4GB LPDDR4 RAM options</td><td>3.4 watts</td><td>1.5GHz</td><td>85.6mm × 56.5mm</td></tr><tr><td>OpenMV Cam</td><td>low power camera board for visual data processing</td><td>512KB RAM + 2 MB Flash Memory</td><td>Consumes 100 mA while idle and 140 mA when pro-cessing images, 3.3V</td><td>480 MHz</td><td>45mm×36mm×30mm</td></tr><tr><td>SparkFun Edge De-velopment Board</td><td>32-bit ARM Cortex-M4F processor</td><td>384KB SRAM + 1MB Flash Memory</td><td>6uA/MHz, 1.8V - 3.6V</td><td>48MHz CPU clock, 96MHz with TurboSPOT</td><td>40.6mm× 40.6mm× 8.9mm,</td></tr><tr><td>BeagleBone AI</td><td>2x ARM Cortex-A15</td><td>1 GB RAM + 16 GB Flash Memory</td><td>Power up under 100mA (500mW), USB type-C 5 volt, 2.5 amp</td><td>1.5GHz</td><td>45mm×36mm×30mm</td></tr><tr><td>Versal VC1902 ACAP Board</td><td>Versal VC1902</td><td>DDR4 UDIMM 8GB, LPDDR4 Component 8GB</td><td>12V Wall Adapter and ATX PCIe 8pin (6+2) Connector</td><td>33 to 133 peak TOPS (for INT8 and INT16 operations), or 8 TFLOPS for FP32 operations</td><td>190mm×241mm</td></tr></table>

however, the camera is a single device that performs both sensing and processing. 

2) Near-device intelligence: The near-device intelligence hardware performs intelligent computations outside of the device, but they are physically near to the device. In these devices, sensed data is stored and basic computations performed with the device. However, the intelligent processing is done in another device that is close to the sensing device. A common example is the drones with camera, that collect the images and send them to a near-by processing station. The processing station performs intelligent processing on images trying to identify objects, and perform real-time segmentation and tracking. 

3) Far-device intelligence: The far-device intelligence hardware is a cloud or server-based systems where intelligent data processing occurs away from the sensing device. The device senses the real-time signals and then transmits it for further processing in a remote server. In this system, some basic edge AI processing can be done, while the higher-level abstractions and complex processing are performed in a highperformance computing platform. 

# IV. RECIPES TO BUILD AGI CHIP BLOCKS

Incorporating various priors (as defined in Section II) are important to build AGI chips that resemble human intelligence. There are many possible approaches to arrive at AGI chip capability. At the highest level, each neural block of the chip should be trainable and configurable in many different functions. None of the AI chips today puts together the different cognitive priors required for mimicking human-like general intelligence. Following are the main practical high level concepts that need to go in the design of AGI chips: (1) Ability to reconfigure the connectivity between neurons, neural network layers and that of neural system, (2) Randomness in the strength of connections and weight assignments to incorporate generality, (3) Presence of various types and forms of feedback and feedforward networks connections, and (4) 

different ways of learning the networks. Collectively, these high-level concepts should aim to embed the cognitive priors such as neuro-sensory, learning and knowledge as part of the built-in-test for the chip. 

# A. Reconfigurability

The ability of the brain to reconfigure is based on several factors [78], [79]. Often memories and events are strongly linked to the ability to forget, store, and filter information. The reconfigurability is time-dependent and dynamic and depends on input stimuli. 

Consider the connectivity strength between any two nodes $\{ n _ { 1 } , n _ { 2 } \}$ as $c$ then, any input stimuli $s _ { 1 }$ can influence the change in the state of connection from $c ( t _ { 1 } )$ to $c ( t _ { 2 } )$ , however, not necessarily changing the network decision $d _ { o }$ . Any change in the network decision $d _ { o }$ due to the change in input stimuli $s _ { 1 }$ implies that the neural network learns a new behavior. There can be a direct or indirect relationship between the stimuli and the ability of the network to be reconfigured. The flexibility of the network to be reconfigured offers the development of multiple network structures from the same common blocks. 

The memories and computations co-exist in neural networks [80], [81]. Unless the reconfiguration of the network is possible in an easy manner, it will be difficult to encode the input stimuli and capture the variations of the encoded stimuli within the network. A fully connected network would involve a connection between the neuron within the layer and between the layers. The connections will also be fed back to the neuron within the same layer and will connect to the neurons in the previous layers. The ability to connect, disconnect, and reconnect the neurons can define the architecture, and the memory functions of the network. 

# B. Randomness

It is understood that as the brain learns stimuli over a period of time, it shows stronger functional connections while having 

a decrease in randomness within the networks [82]. In contrast, it has been seen in artificial neural networks that random dropouts can benefit learning, and improve the robustness of the networks [83]–[85]. The amount of randomness can have a major impact on the learning ability of the networks. As the randomness increases, the learning will take a longer time, while it also helps to understand newer information. The number of weights in a network is limited, having a percentage of weights exhibiting random variations alters the connectivity and decision space of the neural network. It is very well understood that a young brain develops fully connected networks and gradually lose those connections as learning occurs [86]–[88]. As aging occurs to the brain, they become exposed to various rewiring of the brain and become less efficient [89]. The randomness in the brain is also attributed to the ability of humans to be creative [90]– [92]. It can be assumed that the ability to randomly rewire the parts of the brain to process newer information makes the information processing in the brain robust even with a reduced efficiency as the aging occur. 

The randomness also occurs in the input encoding of the stimuli, the neuron thresholds, and the charge-conductance mechanisms. As each neuron has minor variation in size, volume and structure, they respond differently to the same input stimuli yet makes the overall architecture robust for learning new information, providing evidence to the importance of randomness in the intelligent design. Analogous to this, the in-memory computing [50], and analog computing [93] often naturally observe randomness in the artificial neurons, drawing similarities to the biological neurons. The dot-product computation implemented as multiply and accumulate operation with crossbar architecture [53] is a good example of this. The weighted summation of input voltages when reading as output currents in the crossbar often has errors, resulting from the conductance variations of the crossbar nodes or that from the leakage currents and parasitic effects of the switches. While these errors exist, the crossbar along with activation functions in a neural network architecture compensates for these errors. The errors can be compensated by tuning the conductance of the nodes, and robustness improved by adjusting the thresholds and shape of activation functions. 

# C. Role of feedback and feedforward loops

Both feedback and feedforward networks exist in the human brain [94]–[97]. The studies in the past have argued for the feedforward networks to play a major role in the prediction mechanisms, while the feedback to be important to generalisation and learning abilities. Inferences and decisions often require information processing through the layered neural networks in the shortest possible time. It should be noted that all information-processing mechanisms in the human brain are dynamic and real-time. Once an inference is made, some forms of actions follow; needless to say even inaction is an action. The actions are also influenced by various cognitive priors, and the interplay between the feedback and feedforward networks are essential. As such most neural networks that contribute to intelligence in the brain are recurrent, stochastic, dynamic, and deep. 

It can be also argued that the number of feedback and feedforward networks in the human brain far exceeds than that of other animals. As the density of neurons increases, they lead to many different possible combinations for feedbacks, which contributes to the higher holistic sensing ability of the humans - be it vision, speech, smell, or touch. Although many animals have one or other heightened forms of senses, humans can collectively use different senses to build awareness. The selfawareness originates from the basic responses of the senses and the perception of the world that is mentally visualized. Feedbacks in this sense, are essential for building newer learning priors and knowledge paths. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-03-22/63b2b94d-c20b-4c10-b6e5-2ee4374abaf4/c905adef1a19928780cf6b47b22b6d88e4720b6bb2b4f054464f7708aebe749e.jpg)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-03-22/63b2b94d-c20b-4c10-b6e5-2ee4374abaf4/c066aa32178817f958c87bbd7f9a0fb0b5b0c3ecf7dfaf025e88b662da1679ae.jpg)



Fig. 3. Increasing complexity with increasing sensory feedbacks and decisions


Figure 3 shows the overall high-level structure of the realtime neural system that mimics general intelligence. The AGI system should be able to integrate the motor-sensory priors that are basic senses humans are used to and be able to sense and extract the features through neural encoding mechanisms. The sensory neurons after processing the stimuli send it to a series of neural networks that have feedback and feedforward networks. The local decisions from information obtained from each of the senses are further processed by the network of decision networks that construct the memories and have the ability to fuse the information to make meaningful conclusions. The neurons that uses such meta-learning priors are considered as the building blocks, and as the information processing navigates through to the decision networks, the mechanisms become complex giving form and structure to the captured information. The robustness and generality of such a system is assessed using knowledge priors, that helps to qualitatively compare the performance of the AGI with that of human like intelligence. 

# D. Learning

Learning is essential for human survival [98], [99]. For surviving the challenges posed by the changing environment, setting a high level of motivation and reward is important [100], [101]. Rewards and goals drive the learning process and often help to become efficient. In artificial neural networks, the rewards are set as part of the objective function, with a 

reduction in error as a way to make better decisions. The weights of the neural network connections are updated or changed based on the final output errors, which are propagated from one side of the network layer to another. The reduction in the errors can be achieved by updating and readjusting the weights from one layer to another layer. This type of learning can be achieved in several different ways and algorithms, and cumulatively comes in the broader definition of meta-learning ability. 

The brains are unique [102] and the learning process in the human brain is still not fully understood. Every part of the brain has a function, however, when a part of the brain becomes damaged, very often some other part of the brain compensates for that loss. This is possibly due to the high level of interconnection between the neurons across the brain, which gives many possibilities of translating biological metalearning into different forms of learning algorithm. 

It can be also noted that the nature of experiences and inputs that the brain receives has a lot to do with the intelligence abilities [103]. The highly plastic nature of the brain allows for this, whereby, learning occurs in real-time and is always online. The learning responds to previous memories, events, and updates the inferences based on the newer experiences. Eventually, the outcomes are tied to events making the learning algorithms change the expectations on objectives over a period. 

Not one learning algorithm would be sufficient. The skill attainment would require the presence of mind that requires extensive use of working memory. The way the updates are done in working memory is not the same as that requiring creative forms of expressions and those involving executing the functions. It will be important to note in the design of AGI systems that one universal algorithm for learning might not be the solution, instead, the learning needs to be addressed at the level of the neuron, neural networks, and network of systems in different ways. 

# E. Scalability

The biological neurons are known to be on the scale of billions [104]. The neurons in the brain architecture consist of complex connections between the neurons enhancing the functional purpose. The artificial neurons if it was to be useful would require an architecture that is scalable both structurally as well as functionally. 

Almost all the hardware devices and materials used for building neurons have electrical and cost limitations [105], [106]. The ability to replicate a module from one to another is an important aspect of hardware design. Often a hierarchical approach to design helps to reduce the complexity of troubleshooting and also helps to bring out the designs faster. It can, therefore, be taken as an important principle in the scalability design of the neural network. However, most neural networks are fully connected within a layer and between the layers, which makes signal propagation and electromagnetic issues important for neural network designs. 

While a weak AI chip is focused on solving problems with one type of neural network, an AGI chip aims to incorporate generalisation that can emulate multiple neural networks and 

functions. The aim of such AGI chips is to be fully reconfigurable such that various neural blocks can be configured to obtain specific neural functions and learning approaches such as convolutional neural networks for object recognition from images or long short term memories for processing and predicting the weather using time series data. Collectively, they may be binded by global learning mechanisms and fusion strategies. 

# V. ARCHITECTURE BLOCKS FOR AGI CHIP

The functional properties outlined in Section IV are required to put together the AGI chip design. Extreme parallelism, hierarchy, and modularity is a key aspect to speed up the design of the AI chips. Assuming these properties are taken care of from an algorithmic and hardware perspective, we list the main hardware blocks that form an AGI processor core. 

Various blocks of possible AGI chip is shown in Fig. 4. The system assumes that all signals from the sensors are timedependent and have natural variations to it. 

# A. Encoding and fusion cores

The signals are in analog or digital form or in combinations of it. The Spatio-temporal block performs the probabilistic encoding of the input signals. The encoding can be implemented with a variety of techniques such as Spatial Pooler in HTM, LSTM, SNN encoding, etc. When passed through a set of encoders, the signal can be fused using a feature fusion core. The commonly used feature fusion approaches include wavelet-based fusion, concatenation, weighted addition, or the multiplication of features or using a neural network to combine the feature combination. 

# B. Low-level cores

The sensory core and motion core forms the low-level cores required for the chip. The sensory core identifies the nature of the input signals as belonging to the five known human senses. The sensory encoded signals from haptics sensors, olfactory sensors, gustatory sensors, speech and vision sensors, and vestibular sensors would be processed with this sensory core. These low level features could be processed in parallel to further encode and extract most relevant parts of the signals. It also builds the attention features required to focus on objects or regions of signals needed for an application. For example, recognizing a human’s activity in a scene requires the attention of that specific human and activities as identified through visual and audio cues. The motion core is necessary to build the low-level visual features, capture the depth of the scene, build the visual perception of surroundings, and capture the sensory signals’ changes with respect to time. 

# C. Learning cores

The logic core, math core, memory core, motor control core, and policy/rules core take part in the learning of features and fine-tuning the predictions. The implementation of various learning algorithms, such as backpropagation, evolutionary 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-03-22/63b2b94d-c20b-4c10-b6e5-2ee4374abaf4/fb7cf721bb3be6783ca8cf5f8cc2715f6d8585e57715da2a316c346368680a5d.jpg)



Fig. 4. The block diagram of a AGI processor core.


computations, and optimisation requires modules for accelerating mathematical and logical computations. In an online learning scenario, it is required to control the sensor feedback, such as in images to adjust the zoom, direction, and view angles, which is done using a motor control core. The intermediary variables, interrupt routines, and temporary storage is handled by the memory core, which can also be used as an in-memory computing unit. The memory core consists of both non-volatile memories for in-memory computations and volatile memories for dynamic storage. The policy and rules core keeps track of the conditions required for training the AGI system. Since an AGI system can have multiple learning algorithms and multiple neural network implementations running in parallel for different applications, it becomes essential to keep track of rules and policies specific to a given application. 

The learning core can be used for implementing higher level cognitive tasks such as for natural language processing, affective and psychological reasoning. The cognitive processing tasks are computationally expensive and uses the combinations of maths, logic, memory and rules, which can be accelerated with AGI learning cores. Since many of the higher level cognitive tasks extensively uses large amounts of data for training the models, multiple AGI processor cores will be required. Furthermore, processors with multiple AGI cores will be a natural extension to implement ever increasing demands of higher level cognitive tasks. 

# D. Decisions cores

Most real-time AGI applications acquire signals from multiple sensors, which require processing across numerous neural networks. The decisions from various sensory processing networks, such as visual cues, audio cues, etc, require consolidation through a decision fusion core, followed by taking appropriate actions for learning or inference. The action core will further process the decisions to send signals to indicate the execution of a set of actions required for the specific application. 

# E. Timing core

The timing core organises the information flow in a sequenced order relating to events detected by the decision 

core. The timing core is responsible for the AGI clock and is subjective to the actual time. In other words, the time is subjective to the succession of events that occur during a period of time for a given application. The sequencing process can be done by using custom made algorithms supported by learning cores and decision cores. 

The AGI processor core from the heart of the hardware for AGI system helps accelerate the algorithmic response in real-time implementations. Multiple cognitive priors and related algorithms can be implemented with such cores. Like a general-purpose computing processor, the AGI core can be used in complex computer architecture with multiple AGI cores to achieve high parallelism levels. Several possibilities of higher-level architectures from a hardware standpoint is shown in [107], which can be one of the possible ways to implement with the proposed AGI processor cores. 

# VI. AGI CHIP DESIGN - A LOT OF ROOM AT TOP AND BOTTOM

# A. Funnel design flow

As the push towards meeting Moore’s law becomes challenging and costly, the question of alternative devices and computing architecture grows [108], [109]. It has been time and again quoted from the device perspective that there is “plenty of room at the bottom” [110] and from the systems side “plenty of room at the top” [111]. This phenomenon is reflected in the usage of “more than Moore’s law”. This leaves us with a funnel design flow as shown in Fig 5. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-03-22/63b2b94d-c20b-4c10-b6e5-2ee4374abaf4/3d5beade70f89082599b46ce5a672ad940be47fad56462376d615d51f05aeef5.jpg)



Fig. 5. The funnel design flow for AGI Chip


There are many new devices that over the years have shown promising results for designing and implementing AI chips. Some of the alternatives to CMOS based design include FDMOS, Carbon nano-tube transitors, and FinFETs, and those that can reduce computations for neural design include memristive crossbars with ReRAM, STTRAM, etc [71]. Devices take many years of development to mature and cost a significant amount of capital investments. Due to this reason, even if there are many promising devices only very few make it through eventually to industrial use. However, it should 

be noted that the search for the perfect device that remains stable, reliable, which is easy to fabricate and is compatible with popular integration processes continues as the aims to pack more and more functionalities continue. This has also opened up the field of quantum devices and computing as an integral part of neural chip designs of the future. 

The rigidity in the design and innovation is higher when designing standard cells, both for digital as well as analog circuits. Any performance errors in the standard cells will have a high impact on the reliable functioning of the neural chips. It’s at this stage that the engineering fine-tuning and innovation steps in through a difficult path. On one side, the circuit designers would need to be aware of the device level issues, and on the other side, be able to build reliable neural blocks that can withstand the test of time. Many standard cells are used to build basic neural circuit blocks such as dotproduct computation, activation functions, and programming logic. The neural circuit block also includes efficient designs of memory and state transitions between the neural network layers. Several neural circuit blocks are required to build neural system blocks such as convolutional layers, hierarchical temporal memories, and long short term memories. And a large combination of neural system blocks is required for building AGI chip targeted at general intelligence applications. The aim of such AGI chips will be to ultimately match the wide spectrum of human intelligence, leave plenty of room for innovation, development, and applications. 

# B. Automation of chip design

The design of the chips can be a time-consuming task. Automating the design flow is an important task to speed up the design to the manufacturing process, and for reducing the overall cost for developing an AGI chip [112]. Currently, in the digital chip market, there are numerous tools for automating the ASIC design flow [113] that can be used for developing an AGI chip. Currently, in the digital chip market, there are a number of commercial tools available for translating the high-level codes to digital logic. The translations of mapping the logic to hardware come with different efficiency and depend on the optimization methods used and technology under consideration. 

Analog design automation is, however, much more challenging than digital design automation. The device parasitics, process technology, signal integrity issues, and thermal effects can significantly impact the overall design of the analog circuit. It takes a high level of skill to analyze through each of the issues and come up with a robust solution for given process technology. The design that works for a particular transistor node size does not more often work in a lower node size. This makes the analog design challenging than digital design. One approach used for automating the analog design for AI is evolutionary optimization methods [114], [115]. This is an open area of research and requires various levels of optimization to ensure the selection of optimal hardware blocks for an AI processor design. For example, in the case of emerging devices for analog AI chip design, the variability in the devices will be much higher than traditional CMOS based designs. This 

means the design automation for emerging analog AI chips [115] such as using crossbar requires to consider multiple objective functions to arrive at an optimal design. As the size of the networks increases the search to find the optimal design becomes challenging both at the schematic and physical design levels. 

# VII. HOW TO TEST AGI CHIPS?

An AI chip that implements AGI requires to be tested to ensure that general intelligence functionality is achieved. This can be done by testing the AGI chip in a real-time application involving conversations that enable performing a Turning test. The ability of the AGI chips to provide general intelligence in tasks that humans could do well is indeed a well-known task. Likewise, it can be argued that the general intelligence tasks may or may not work successfully for humans is also equally important. 

There are several aspects to test the effectiveness of the AGI chip. The use of knowledge priors assist in testing and comparing the AGI chip functions with that of human intelligence. Some of the functional test that addresses knowledge priors are outlined using algorithmic and philosophical approaches as shown in [116]–[118]. Beyond functional tests, the AGI chips also would need to undergo electrical tests for ensuring hardware reliability. This can be grouped into functional, and electrical tests, to test the AGI chip and the AGI system build with it. Obviously, such system can be a combination of software and hardware routines, with core aspects of AGI functions implemented on the hardware. The example set of tests that broadly covers aspects of intelligence priors to chip performance are proposed below: 

# A. Functional test 1: Dating test - conversation game

The process of two humans engaging in a romantic date, and the ability to have an engaging conversation is a mark of general intellectual ability. AGI system should be able to consider effectively following factors:(1) make a wise selection of dating activities, (2) engage and communicate effectively, and (3) politeness and manners should have adhered. 

AGI system will be presented as a real human using a chatbot or virtual reality platform. The date will be introduced to the AGI bot as a real human and asked to rate the AGI on three of the factors. As long as the human is able to find the AGI bot personality attractive, and ask for another date to meet in person, it will mark as a success. The test can be repeated with several individuals to validate the strength of AGI. 

# B. Functional test 2: Sports commentary test - vision game

General intelligence allows humans to follow rules and make practical estimations based on a situation. This is very common during a sports game. There are certain rules to follow, and at the same time, improvisation is often required to win the game. When we watch a sports game, we often make use of the majority of cognitive functions such as hearing, language interpretations, decision rules, estimations, 

and extensively use human vision. In this task, the AGI system should be able to: (1) recognize the sports through visual and auditory means, (2) be able to understand the rules and guidelines, and (3) engage the viewers through a wide set of conversations. 

The viewers should not be able to recognize the difference between human commentary and AGI commentary. The judgment of who passes the test will be based on cross-validating the human judgment across several human subjects. 

# C. Functional test 3: Mentalist test - emotion game

Humans are good at reading gestures and behavior of the other humans, and use those cues to predict the thoughts. The mentalist theories suggest that the ability to read another person’s mind is a natural process and can start very early in humans. Many subtle emotions are invariably understood by the human mind and are often expressed through emotional gestures. In this task, the AGI system should be able to: (1) understand gestures from visions, (2) be able to read emotional details through various senses, and (3) be able to guess the thoughts of a human being and be ethically sensitive about it. 

The mentalist test could be the ultimate test for the AGI system. If the AGI system could predict the thoughts of humans using the known senses, it will be able to uncover and prove many theories of intelligence. Ultimately, such a system will be considered superior to human general intelligence, thereby resulting in singularity. At the same time, the AGI system should act ethically and not reveal the personal details without breaching the privacy and permission of the individual. Such systems could be possible with the help of additional sensing capabilities such as reading the electromagnetic signals of the brain or that involving heat signature, which are not effectively possible with human senses. 

# D. Electrical test 1: Architecture robustness

The electrical noise, device parasitics, process variations, and signal integrity issues can affect the overall performance of the designed chip. Any such variations will result in signal loss, and the design methods used will have a major impact on the robustness of the chip. 

The AGI architecture would need to be tested for the following: (1) stability against security attacks by adversarial manipulation of the signals within the chip, (2) sensitivity, specificity, and accuracy the architecture relative to the signal changes within the chip during the inference outcomes, and (3) robustness of architecture in application to multiple problems. 

The general intelligence nature of the AGI chip should not be affected by natural variations in input signals. While noise in the signal can be manipulated by an external force, the system is allowed to be tricked, at the same level of accuracy as that of the human brain. 

# E. Electrical test 2: Chip reliability

The reliability of the chip requires extensive analysis and testing for functional accuracy under extreme situations in which the chip will be used. As AGI chip will be required 

more often in real-time settings, it will be important to have built-in systems for in-chip and in-system monitoring, run-time checking, and built-in self-test. 

The AGI chips would need to be reconfigured more often than a regular weak-AI chip. This means fault tolerance and error-correcting mechanisms would need to be incorporated within the chip. The AGI chip reliability would need to be tested for the following: (1) thermal, electromagnetic and mechanical stress, and resulting benchmarks on the failure rate, (2) ability to compensate for the failures and have various built-in tests, and (3) the reliability of packaging and system integration for multi-chip communications. 

The AGI chips would need to be integrated into realtime electronic devices under various applications such as in robotics, satellites, automotive industry, and mobiles. This would mean the packaging of the chips becomes important to robotics, automotive industry, and mobiles, in improving the reliability when exposed to realistic and harsh environmental conditions. The practical applications warrant that the chip would have a high endurance allowing it to be reused from one device to another. 

# VIII. DISCUSSION AND FUTURE DIRECTIONS

There are several open problems in AGI chip design and implementations. Some of those include (1) reliability and reconfigurability of the chip, (2) architecture design and scalability, (3) compatibility with older devices, (4) 3D integration challenges, (5) low power design challenges on multi-chip systems, (6) energy, area, and speed efficiency, (7) biocompatibility and multisensor integration issues, (8) design and test automation, and (9) functional integration of multiple cognitive prior blocks required for AGI. 

AI-trusted computing such as in drug discovery, medicine, health services, governments, and chemistry, opens up several opportunities for AGI chips. Law enforcement uses face detection and recognition, biometric matching, and tracking extensively. The extensive use of AI has led to the questions of ethics and politics of AI. Many corporate and governmental bodies started to used AI approaches to perform market analysis, monitor activities, understand user behavior, and develop policies for better management. 

AGI chips can be used to build ethically and socially aware AI, that can be integrated into human society without having apocalyptic fears about AI. The AGI could eventually be part of the solutions for providing better services, and judgments such as in automation of services in government or politics or courts. Another emerging possibility is to integrate the AGI chip with that of the neural networks of the brain. The biointerface, human-AGI interactions, and cyborg applications can lead to collective intelligence abilities, to enhance human intelligence abilities. 

Figure 6 shows the four stages of AI chip development. Currently we are in AI 1.0 stage, with a major focus on specific applications. In the second stage of AI, the focus will be on building general intelligence chips, that could assist humans further in solving difficult social and ethical questions. The third stage could witness collective form of 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-03-22/63b2b94d-c20b-4c10-b6e5-2ee4374abaf4/36a96d342d855ddc40b00cc056e968fc0789e927934801bb88748b0df623241b.jpg)



Fig. 6. The future landscape in AI chip development


AGI, where the intelligence will expand in applications and complexity, currently not imagined by humans. The fourth stage and beyond, would see the integration of AGI chip with human brain, and ultimately allow humans to access all forms of electronic signals, and senses available to machines. 

# IX. CONCLUSION

This paper presented an overview of the emerging field of artificial general intelligence from a hardware perspective. The AGI systems, in general, have been considered extremely difficult to build, and more often the researchers gave up on the idea of building a realistic AGI. The AI hardware support for building the AGI system has been limited and has been proven to be a difficult problem even for a weak AI system. The development of algorithms and systems should be complemented with different types of AGI chips. Emulating the brain networks through cognitive priors without a full understanding of the brain mechanisms, also have been the major bottleneck in this area. Nonetheless, with the rapid progress in the AI-driven design methodologies and the emergence of new devices offers possibility for building fullfledged AGI chips. It is required to bridge the knowledge gap between the brain sciences, psychology, computing, materials psychology, computing, materials, and electrical engineering among several other fields to address the questions of AGI systems. Building AGI chips could be an efficient way to create energy-efficient real-time neural computations and include accelerated collaborative intelligence to compete with the general intelligence capabilities of the human brain. While humans are limited by the number of sensory mechanisms that support the general intelligence, the machines could have a major advantage in using a wide range of sensing abilities such as reading electromagnetic signals and visual spectrum that is not accessible by the human brain, that can redefine the way we use and apply AI technologies. 

# REFERENCES



[1] R. V. Yampolskiy, “Turing Test as a Defining Feature of AI-Completeness,” in Studies in Computational Intelligence. Springer Berlin Heidelberg, 2013, pp. 3–17. [Online]. Available: https: //doi.org/10.1007%2F978-3-642-29694-9 1 





[2] J. Kim, “The Problem of Distinction Between ‘weak AI’ and ‘strong AI’,” Journal of The Society of philosophical studies, vol. 117, pp. 111–137, jun 2017. [Online]. Available: https: //doi.org/10.23908%2Fjsps.2017.06.117.111 





[3] P. Voss, “Essentials of General Intelligence: The Direct Path to Artificial General Intelligence,” in Artificial General Intelligence. Springer Berlin Heidelberg, pp. 131–157. [Online]. Available: https://doi.org/10.1007%2F978-3-540-68677-4 4 





[4] C. Pennachin and B. Goertzel, “Contemporary Approaches to Artificial General Intelligence,” in Artificial General Intelligence. Springer Berlin Heidelberg, pp. 1–30. [Online]. Available: https: //doi.org/10.1007%2F978-3-540-68677-4 1 





[5] E. Yudkowsky, “Levels of Organization in General Intelligence,” in Artificial General Intelligence. Springer Berlin Heidelberg, pp. 389–501. [Online]. Available: https://doi.org/10.1007% 2F978-3-540-68677-4 12 





[6] B. Goertzel, “OpenCogPrime: A cognitive synergy based architecture for artificial general intelligence,” in 2009 8th IEEE International Conference on Cognitive Informatics. IEEE, jun 2009. [Online]. Available: https://doi.org/10.1109%2Fcoginf.2009.5250807 





[7] V. G. Red’ko, “The Natural Way to Artificial Intelligence,” in Artificial General Intelligence. Springer Berlin Heidelberg, pp. 327–351. [Online]. Available: https://doi.org/10.1007%2F978-3-540-68677-4 10 





[8] R. Banerjee and S. K. Pal, $^ { \mathrm { 4 6 } } Z ^ { \ast }$ -numbers, data structures, and thinking in machine-mind architecture,” IEEE Transactions on Emerging Topics in Computational Intelligence, vol. 4, no. 5, pp. 686–695, 2020. 





[9] L. Camunas-Mesa, B. Linares-Barranco, and T. Serrano-Gotarredona, ˜ “Neuromorphic Spiking Neural Networks and Their Memristor-CMOS Hardware Implementations,” Materials, vol. 12, no. 17, p. 2745, aug 2019. [Online]. Available: https://doi.org/10.3390%2Fma12172745 





[10] A. M. Zyarah, N. Soures, and D. Kudithipudi, “On-Device Learning in Memristor Spiking Neural Networks,” in 2018 IEEE International Symposium on Circuits and Systems (ISCAS). IEEE, may 2018. [Online]. Available: https://doi.org/10.1109%2Fiscas.2018.8351813 





[11] E. Gale, B. de Lacy Costello, and A. Adamatzky, “Spiking in Memristor Networks,” in Handbook of Memristor Networks. Springer International Publishing, 2019, pp. 767–789. [Online]. Available: https://doi.org/10.1007%2F978-3-319-76375-0 27 





[12] M. Itoh and L. Chua, “Memristor Cellular Automata and Memristor Discrete-Time Cellular Neural Networks,” in Handbook of Memristor Networks. Springer International Publishing, 2019, pp. 1289–1361. [Online]. Available: https://doi.org/10.1007%2F978-3-319-76375-0 47 





[13] J. Pei, L. Deng, S. Song, M. Zhao, Y. Zhang, S. Wu, G. Wang, Z. Zou, Z. Wu, W. He et al., “Towards artificial general intelligence with hybrid tianjic chip architecture,” Nature, vol. 572, no. 7767, pp. 106–111, 2019. 





[14] Y. Chen, Y. Xie, L. Song, F. Chen, and T. Tang, “A survey of accelerator architectures for deep neural networks,” Engineering, vol. 6, no. 3, pp. 264–274, 2020. 





[15] S. Legg, M. Hutter et al., “A collection of definitions of intelligence,” Frontiers in Artificial Intelligence and applications, vol. 157, p. 17, 2007. 





[16] R. B. Cattell, Intelligence: Its structure, growth and action. Elsevier, 1987. 





[17] E. S. Spelke and K. D. Kinzler, “Core knowledge,” Developmental science, vol. 10, no. 1, pp. 89–96, 2007. 





[18] L. McNally, S. P. Brown, and A. L. Jackson, “Cooperation and the evolution of intelligence,” Proceedings of the Royal Society B: Biological Sciences, vol. 279, no. 1740, pp. 3027–3034, 2012. 





[19] R. Dunbar, “Machiavellian intelligence. social expertise and the evolution of intellect in monkeys, apes, and humans: Edited by richard byrne & andrew whiten. oxford: Clarendon press (1988). pp. $\mathbf { \dot { x } } \mathbf { i } \mathbf { v } + 4 1 3$ . price£ 50 hardback,£ 25 paperback,” 1989. 





[20] S. Kanazawa, “General intelligence as a domain-specific adaptation.” Psychological review, vol. 111, no. 2, p. 512, 2004. 





[21] M. Minsky and S. A. Papert, “Artificial intelligence progress report,” no. AIM-252, pp. 1–136, 1972. 





[22] J. McCarthy, “Generality in artificial intelligence,” Communications of the ACM, vol. 30, no. 12, pp. 1030–1035, 1987. 





[23] A. E. Lawson, “The acquisition of biological knowledge during childhood: cognitive conflict or tabula rasa?” Journal of research in science teaching, vol. 25, no. 3, pp. 185–199, 1988. 





[24] E. Versace, A. Martinho-Truswell, A. Kacelnik, and G. Vallortigara, “Priors in animal and artificial intelligence: where does learning 





begin?” Trends in cognitive sciences, vol. 22, no. 11, pp. 963–965, 2018. 





[25] T. C. Bates, “The General Factor of Intelligence: How General Is It?” Intelligence, vol. 30, no. 6, pp. 577–578, nov 2002. [Online]. Available: https://doi.org/10.1016%2Fs0160-2896%2802%2900144-7 





[26] B. Goertzel, C. Pennachin, and N. Geisweiller, “The opencog framework,” in Engineering General Intelligence, Part 2. Springer, 2014, pp. 3–29. 





[27] “When Put to the Test AI Enthusiasm Exceeds AI Knowledge,” may 2019. [Online]. Available: https://doi.org/10.1287%2Flytx.2019.03.23n 





[28] E. Neufeld and S. Finnestad, “In defense of the Turing test,” AI & SOCIETY, feb 2020. [Online]. Available: https://doi.org/10.1007% 2Fs00146-020-00946-8 





[29] J. R. Searle, “The Turing Test: 55 Years Later,” in Parsing the Turing Test. Springer Netherlands, 2009, pp. 139–150. [Online]. Available: https://doi.org/10.1007%2F978-1-4020-6710-5 10 





[30] J. Togelius, “General Intelligence and Games in General,” in Playing Smart. The MIT Press, 2019. [Online]. Available: https: //doi.org/10.7551%2Fmitpress%2F11723.003.0012 





[31] A. J. Andreotta, “The hard problem of AI rights,” AI & SOCIETY, may 2020. [Online]. Available: https://doi.org/10.1007% 2Fs00146-020-00997-x 





[32] R. Cummins and J. L. Pollock, “Artificial intelligence and hard problems: The expected complexity of problem solving,” in Philosophy and AI. The MIT Press, 1995. 





[33] J. Zhu, T. Zhang, Y. Yang, and R. Huang, “A comprehensive review on emerging artificial neuromorphic devices,” Applied Physics Reviews, vol. 7, no. 1, p. 011312, mar 2020. [Online]. Available: https://doi.org/10.1063%2F1.5118217 





[34] K. Roy, A. Jaiswal, and P. Panda, “Towards spike-based machine intelligence with neuromorphic computing,” Nature, vol. 575, no. 7784, pp. 607–617, nov 2019. [Online]. Available: https: //doi.org/10.1038%2Fs41586-019-1677-2 





[35] S. Sengupta, S. Basak, P. Saikia, S. Paul, V. Tsalavoutis, F. Atiah, V. Ravi, and A. Peters, “A review of deep learning with special emphasis on architectures applications and recent trends,” Knowledge-Based Systems, vol. 194, p. 105596, apr 2020. [Online]. Available: https://doi.org/10.1016%2Fj.knosys.2020.105596 





[36] B. Voorhees, “GA¶del’s Theorem and Strong AI: Is Reason Blind?” ˜ in Metadebates on Science. Springer Netherlands, 1999, pp. 43–62. [Online]. Available: https://doi.org/10.1007%2F978-94-017-2245-2 4 





[37] R. Kwok, “Three ways to build a strong AI-training pipeline,” Nature, apr 2019. [Online]. Available: https://doi.org/10.1038% 2Fd41586-019-01250-2 





[38] S. A. Aamir, Y. Stradmann, P. Muller, C. Pehle, A. Hartel, A. Gr ¨ ubl, ¨ J. Schemmel, and K. Meier, “An accelerated lif neuronal network array for a large-scale mixed-signal neuromorphic architecture,” IEEE Transactions on Circuits and Systems I: Regular Papers, vol. 65, no. 12, pp. 4299–4312, 2018. 





[39] J. M. Cruz-Albrecht, T. Derosier, and N. Srinivasa, “A scalable neural chip with synaptic electronics using cmos integrated memristors,” Nanotechnology, vol. 24, no. 38, p. 384011, 2013. 





[40] J. Partzsch, S. Hoppner, M. Eberlein, R. Sch ¨ uffny, C. Mayr, D. R. ¨ Lester, and S. Furber, “A fixed point exponential function accelerator for a neuromorphic many-core system,” in 2017 IEEE International Symposium on Circuits and Systems (ISCAS). IEEE, 2017, pp. 1–4. 





[41] A. S. Cassidy, R. Alvarez-Icaza, F. Akopyan, J. Sawada, J. V. Arthur, P. A. Merolla, P. Datta, M. G. Tallada, B. Taba, A. Andreopoulos et al., “Real-time scalable cortical computing at 46 giga-synaptic ops/watt with˜ $1 0 0 \times$ speedup in time-to-solution and˜ $1 0 0 { , } 0 0 0 \times$ reduction in energy-to-solution,” in SC’14: Proceedings of the International Conference for High Performance Computing, Networking, Storage and Analysis. IEEE, 2014, pp. 27–38. 





[42] B. V. Benjamin, P. Gao, E. McQuinn, S. Choudhary, A. R. Chandrasekaran, J.-M. Bussat, R. Alvarez-Icaza, J. V. Arthur, P. A. Merolla, and K. Boahen, “Neurogrid: A mixed-analog-digital multichip system for large-scale neural simulations,” Proceedings of the IEEE, vol. 102, no. 5, pp. 699–716, 2014. 





[43] J. Park, S. Ha, T. Yu, E. Neftci, and G. Cauwenberghs, “A 65k-neuron 73-mevents/s 22-pj/event asynchronous micro-pipelined integrate-andfire array transceiver,” in 2014 IEEE Biomedical Circuits and Systems Conference (BioCAS) Proceedings. IEEE, 2014, pp. 675–678. 





[44] G. Indiveri, F. Corradi, and N. Qiao, “Neuromorphic architectures for spiking deep neural networks,” in 2015 IEEE International Electron Devices Meeting (IEDM). IEEE, 2015, pp. 4–2. 





[45] N. Qiao and G. Indiveri, “Scaling mixed-signal neuromorphic processors to 28 nm fd-soi technologies,” in 2016 IEEE Biomedical Circuits and Systems Conference (BioCAS). IEEE, 2016, pp. 552–555. 





[46] M. Davies, N. Srinivasa, T.-H. Lin, G. Chinya, Y. Cao, S. H. Choday, G. Dimou, P. Joshi, N. Imam, S. Jain et al., “Loihi: A neuromorphic manycore processor with on-chip learning,” IEEE Micro, vol. 38, no. 1, pp. 82–99, 2018. 





[47] G. K. Chen, R. Kumar, H. E. Sumbul, P. C. Knag, and R. K. Krishnamurthy, “A 4096-neuron 1m-synapse 3.8-pj/sop spiking neural network with on-chip stdp learning and sparse weights in 10-nm finfet cmos,” IEEE Journal of Solid-State Circuits, vol. 54, no. 4, pp. 992– 1002, 2018. 





[48] D. Ielmini and S. Ambrogio, “Emerging neuromorphic devices,” Nanotechnology, vol. 31, no. 9, p. 092001, 2019. 





[49] E. Kousanakis, A. Dollas, E. Sotiriades, I. Papaefstathiou, D. N. Pnevmatikatos, A. Papoutsi, P. C. Petrantonakis, P. Poirazi, S. Chavlis, and G. Kastellakis, “An Architecture for the Acceleration of a Hybrid Leaky Integrate and Fire SNN on the Convey HC-2ex FPGA-Based Processor,” in 2017 IEEE 25th Annual International Symposium on Field-Programmable Custom Computing Machines (FCCM). IEEE, apr 2017. [Online]. Available: https://doi.org/10.1109%2Ffccm.2017.51 





[50] K. S. Mohamed, “Near-Memory/In-Memory Computing: Pillars and Ladders,” in Neuromorphic Computing and Beyond. Springer International Publishing, 2020, pp. 167–186. [Online]. Available: https://doi.org/10.1007%2F978-3-030-37224-8 6 





[51] W. Cai and R. Tetzlaff, “Synapse as a Memristor,” in Memristor Networks. Springer International Publishing, 2014, pp. 113–128. [Online]. Available: https://doi.org/10.1007%2F978-3-319-02630-5 7 





[52] I. Vourkas and G. C. Sirakoulis, “Modeling Memristor–Based Circuit Networks on Crossbar Architectures,” in Handbook of Memristor Networks. Springer International Publishing, 2019, pp. 973–1004. [Online]. Available: https://doi.org/10.1007%2F978-3-319-76375-0 34 





[53] “Modeling Memristor-Based Circuit Networks on Crossbar Architectures,” in Memristor Networks. Springer International Publishing, 2014, pp. 505–535. [Online]. Available: https://doi.org/10. 1007%2F978-3-319-02630-5 23 





[54] D. Querlioz, O. Bichler, and C. Gamrat, “Simulation of a memristorbased spiking neural network immune to device variations,” in The 2011 International Joint Conference on Neural Networks. IEEE, jul 2011. [Online]. Available: https://doi.org/10.1109%2Fijcnn.2011. 6033439 





[55] N. Zheng and P. Mazumder, “Learning in Memristor Crossbar-Based Spiking Neural Networks Through Modulation of Weight-Dependent Spike-Timing-Dependent Plasticity,” IEEE Transactions on Nanotechnology, vol. 17, no. 3, pp. 520–532, may 2018. [Online]. Available: https://doi.org/10.1109%2Ftnano.2018.2821131 





[56] K. V. Pham and K.-S. Min, “Non-Ideal Effects of Memristor-CMOS Hybrid Circuits for Realizing Multiple-Layer Neural Networks,” in 2019 IEEE International Symposium on Circuits and Systems (ISCAS). IEEE, may 2019. [Online]. Available: https://doi.org/10.1109%2Fiscas. 2019.8702519 





[57] S. Zhang, G. L. Zhang, B. Li, H. H. Li, and U. Schlichtmann, “Agingaware Lifetime Enhancement for Memristor-based Neuromorphic Computing,” in 2019 Design Automation & Test in Europe Conference & Exhibition (DATE). IEEE, mar 2019. [Online]. Available: https://doi.org/10.23919%2Fdate.2019.8714954 





[58] O. Krestinskaya, A. Irmanova, and A. P. James, “Memristive Non-Idealities: Is there any Practical Implications for Designing Neural Network Chips?” in 2019 IEEE International Symposium on Circuits and Systems (ISCAS). IEEE, may 2019. [Online]. Available: https://doi.org/10.1109%2Fiscas.2019.8702245 





[59] T. Chen, Z. Du, N. Sun, J. Wang, C. Wu, Y. Chen, and O. Temam, “Diannao: A small-footprint high-throughput accelerator for ubiquitous machine-learning,” ACM SIGARCH Computer Architecture News, vol. 42, no. 1, pp. 269–284, 2014. 





[60] T. Luo, S. Liu, L. Li, Y. Wang, S. Zhang, T. Chen, Z. Xu, O. Temam, and Y. Chen, “Dadiannao: A neural network supercomputer,” IEEE Transactions on Computers, vol. 66, no. 1, pp. 73–88, 2016. 





[61] D. Liu, T. Chen, S. Liu, J. Zhou, S. Zhou, O. Teman, X. Feng, X. Zhou, and Y. Chen, “Pudiannao: A polyvalent machine learning accelerator,” ACM SIGARCH Computer Architecture News, vol. 43, no. 1, pp. 369– 381, 2015. 





[62] Z. Du, R. Fasthuber, T. Chen, P. Ienne, L. Li, T. Luo, X. Feng, Y. Chen, and O. Temam, “Shidiannao: Shifting vision processing closer to the sensor,” in Proceedings of the 42nd Annual International Symposium on Computer Architecture, 2015, pp. 92–104. 





[63] Y.-H. Chen, T. Krishna, J. S. Emer, and V. Sze, “Eyeriss: An energyefficient reconfigurable accelerator for deep convolutional neural networks,” IEEE journal of solid-state circuits, vol. 52, no. 1, pp. 127–138, 2016. 





[64] S. Han, X. Liu, H. Mao, J. Pu, A. Pedram, M. A. Horowitz, and W. J. Dally, “Eie: efficient inference engine on compressed deep neural network,” ACM SIGARCH Computer Architecture News, vol. 44, no. 3, pp. 243–254, 2016. 





[65] L. Cavigelli, D. Gschwend, C. Mayer, S. Willi, B. Muheim, and L. Benini, “Origami: A convolutional network accelerator,” in Proceedings of the 25th edition on Great Lakes Symposium on VLSI, 2015, pp. 199–204. 





[66] B. Moons, R. Uytterhoeven, W. Dehaene, and M. Verhelst, “14.5 envision: A 0.26-to-10tops/w subword-parallel dynamic-voltage-accuracyfrequency-scalable convolutional neural network processor in 28nm fdsoi,” in 2017 IEEE International Solid-State Circuits Conference (ISSCC). IEEE, 2017, pp. 246–247. 





[67] N. P. Jouppi, C. Young, N. Patil, D. Patterson, G. Agrawal, R. Bajwa, S. Bates, S. Bhatia, N. Boden, A. Borchers et al., “In-datacenter performance analysis of a tensor processing unit,” in Proceedings of the 44th Annual International Symposium on Computer Architecture, 2017, pp. 1–12. 





[68] D. Moloney, B. Barry, R. Richmond, F. Connor, C. Brick, and D. Donohoe, “Myriad 2: Eye of the computational vision storm,” in 2014 IEEE Hot Chips 26 Symposium (HCS). IEEE, 2014, pp. 1–18. 





[69] M. M. Shulaker, G. Hills, R. S. Park, R. T. Howe, K. Saraswat, H.-S. P. Wong, and S. Mitra, “Three-dimensional integration of nanotechnologies for computing and data storage on a single chip,” Nature, vol. 547, no. 7661, pp. 74–78, 2017. 





[70] M. A. Zidan, J. P. Strachan, and W. D. Lu, “The future of electronics based on memristive systems,” Nature Electronics, vol. 1, no. 1, pp. 22–29, 2018. 





[71] V. K. Sangwan and M. C. Hersam, “Neuromorphic nanoelectronic materials,” Nature nanotechnology, pp. 1–12, 2020. 





[72] Y. Ding and F. T. Chong, “Quantum computer systems: Research for noisy intermediate-scale quantum computers,” Synthesis Lectures on Computer Architecture, vol. 15, no. 2, pp. 1–227, 2020. 





[73] J. Carolan, M. Mohseni, J. P. Olson, M. Prabhu, C. Chen, D. Bunandar, M. Y. Niu, N. C. Harris, F. N. Wong, M. Hochberg et al., “Variational quantum unsampling on a quantum photonic processor,” Nature Physics, vol. 16, no. 3, pp. 322–327, 2020. 





[74] C. Sung, H. Hwang, and I. K. Yoo, “Perspective: A review on memristive hardware for neuromorphic computation,” Journal of Applied Physics, vol. 124, no. 15, p. 151903, oct 2018. [Online]. Available: https://doi.org/10.1063%2F1.5037835 





[75] Teh, Chan, Hsu, and Loe, “Probabilistic neural-logic networks,” in International Joint Conference on Neural Networks. IEEE, 1989. [Online]. Available: https://doi.org/10.1109%2Fijcnn.1989.118401 





[76] C. Myers and I. Aleksander, “Learning algorithms for probabilistic neural nets,” Neural Networks, vol. 1, p. 205, jan 1988. [Online]. Available: https://doi.org/10.1016%2F0893-6080%2888%2990242-0 





[77] J. SjA¶str ˜ A¶m and W. Gerstner, “Spike-timing dependent plasticity,” ˜ Scholarpedia, vol. 5, no. 2, p. 1362, 2010. [Online]. Available: https://doi.org/10.4249%2Fscholarpedia.1362 





[78] R. F. Betzel and D. S. Bassett, “Multi-scale brain networks,” NeuroImage, vol. 160, pp. 73–83, oct 2017. [Online]. Available: https://doi.org/10.1016%2Fj.neuroimage.2016.11.006 





[79] M. G. Puxeddu, J. Faskowitz, R. F. Betzel, M. Petti, L. Astolfi, and O. Sporns, “The modular organization of brain cortical connectivity across the human lifespan,” NeuroImage, p. 116974, may 2020. [Online]. Available: https://doi.org/10.1016%2Fj.neuroimage. 2020.116974 





[80] A. Destexhe and E. Marder, “Plasticity in single neuron and circuit computations,” Nature, vol. 431, no. 7010, pp. 789–795, oct 2004. [Online]. Available: https://doi.org/10.1038%2Fnature03011 





[81] C. K. Machens, “Building the Human Brain,” Science, vol. 338, no. 6111, pp. 1156–1157, nov 2012. [Online]. Available: https://doi.org/10.1126%2Fscience.1231865 





[82] D. J. A. Smit, M. Boersma, H. G. Schnack, S. Micheloyannis, D. I. Boomsma, H. E. H. Pol, C. J. Stam, and E. J. C. de Geus, “The Brain Matures with Stronger Functional Connectivity and Decreased Randomness of Its Network,” PLoS ONE, vol. 7, no. 5, p. e36896, may 2012. [Online]. Available: https://doi.org/10.1371%2Fjournal. pone.0036896 





[83] A. Poernomo and D.-K. Kang, “Biased Dropout and Crossmap Dropout: Learning towards effective Dropout regularization in convolutional neural network,” Neural Networks, vol. 104, pp. 60–67, 





aug 2018. [Online]. Available: https://doi.org/10.1016%2Fj.neunet. 2018.03.016 





[84] B. Ko, H.-G. Kim, and H.-J. Choi, “Controlled dropout: A different dropout for improving training speed on deep neural network,” in 2017 IEEE International Conference on Systems Man, and Cybernetics (SMC). IEEE, oct 2017. [Online]. Available: https://doi.org/10.1109%2Fsmc.2017.8122736 





[85] H. Wang, W. Yang, Z. Zhao, T. Luo, J. Wang, and Y. Tang, “Rademacher dropout: An adaptive dropout for deep neural network via optimizing generalization gap,” Neurocomputing, vol. 357, pp. 177–187, sep 2019. [Online]. Available: https://doi.org/10.1016%2Fj. neucom.2019.05.008 





[86] K. Supekar, M. Musen, and V. Menon, “Development of Large-Scale Functional Brain Networks in Children,” NeuroImage, vol. 47, p. S109, jul 2009. [Online]. Available: https://doi.org/10.1016%2Fs1053-8119% 2809%2970984-x 





[87] V. Menon, “Large-Scale Functional Brain Organization,” in Brain Mapping. Elsevier, 2015, pp. 449–459. [Online]. Available: https: //doi.org/10.1016%2Fb978-0-12-397025-1.00024-5 





[88] M. Mittner, “Functional Integration of Large-Scale Brain Networks,” Journal of Neuroscience, vol. 33, no. 48, pp. 18 710–18 711, nov 2013. [Online]. Available: https://doi.org/10.1523%2Fjneurosci. 4084-13.2013 





[89] S. Achard and E. Bullmore, “Efficiency and Cost of Economical Brain Functional Networks,” PLoS Computational Biology, vol. 3, no. 2, p. e17, feb 2007. [Online]. Available: https://doi.org/10.1371%2Fjournal. pcbi.0030017 





[90] S. Sequeira, “Randomness and creativity,” Trends in Neurosciences, vol. 24, no. 12, p. 694, dec 2001. [Online]. Available: https: //doi.org/10.1016%2Fs0166-2236%2800%2902081-6 





[91] B. STANISH, “The Underlying Structures and Thoughts About Randomness and Creativity,” The Journal of Creative Behavior, vol. 20, no. 2, pp. 110–114, jun 1986. [Online]. Available: https://doi.org/10.1002%2Fj.2162-6057.1986.tb00425.x 





[92] I. I. Gorban, “Determinism Uncertainty, Randomness, and Hyperrandomness,” in Randomness and Hyper-randomness. Springer International Publishing, sep 2017, pp. 181–195. [Online]. Available: https://doi.org/10.1007%2F978-3-319-60780-1 11 





[93] “Analog Computing,” in Reversible Computing. Wiley-VCH Verlag GmbH & Co. KGaA, nov 2010, pp. 113–130. [Online]. Available: https://doi.org/10.1002%2F9783527633999.ch5 





[94] R. Seidler, D. Noll, and G. Thiers, “Feedforward and feedback processes in motor control,” NeuroImage, vol. 22, no. 4, pp. 1775–1783, aug 2004. [Online]. Available: https://doi.org/10.1016% 2Fj.neuroimage.2004.05.003 





[95] J. F. Mejias, J. D. Murray, H. Kennedy, and X.-J. Wang, “Feedforward and feedback frequency-dependent interactions in a large-scale laminar network of the primate cortex,” Science Advances, vol. 2, no. 11, p. e1601335, nov 2016. [Online]. Available: https://doi.org/10.1126%2Fsciadv.1601335 





[96] T. P. Lillicrap and A. Santoro, “Backpropagation through time and the brain,” Current Opinion in Neurobiology, vol. 55, pp. 82–89, apr 2019. [Online]. Available: https://doi.org/10.1016%2Fj.conb.2019.01.011 





[97] T. P. Lillicrap, A. Santoro, L. Marris, C. J. Akerman, and G. Hinton, “Backpropagation and the brain,” Nature Reviews Neuroscience, vol. 21, no. 6, pp. 335–346, apr 2020. [Online]. Available: https://doi.org/10.1038%2Fs41583-020-0277-3 





[98] S. Snigdha and G. Prieto, “Exercise Enhances Cognitive Capacity in the Aging Brain,” in Physical Activity and the Aging Brain. Elsevier, 2017, pp. 161–172. [Online]. Available: https://doi.org/10. 1016%2Fb978-0-12-805094-1.00016-2 





[99] J. C. Peven, C. M. Stillman, and K. I. Erickson, “The Influence of Physical Exercise on Cognitive Aging,” in Cognitive Changes and the Aging Brain. Cambridge University Press, dec 2019, pp. 245–263. [Online]. Available: https://doi.org/10.1017%2F9781108554350.016 





[100] J. P. O'Doherty and R. J. Dolan, “The role of human orbitofrontal cortex in reward prediction and behavioral choice: insights from neuroimaging,” in The Orbitofrontal Cortex. Oxford University Press, oct 2006, pp. 265–284. [Online]. Available: https://doi.org/10.1093% 2Facprof%3Aoso%2F9780198565741.003.0010 





[101] R. J. Beninger, Dopamine and reward-related learning. Oxford University Press, sep 2018. [Online]. Available: https://doi.org/10. 1093%2Foso%2F9780198824091.003.0002 





[102] G. Miller, “Why Are You and Your Brain Unique?” Science, vol. 338, no. 6103, pp. 35–36, oct 2012. [Online]. Available: https://doi.org/10.1126%2Fscience.338.6103.35 





[103] B. Kolb, Brain Plasticity and Behavior. Psychology Press, jun 2013. [Online]. Available: https://doi.org/10.4324%2F9780203773765 





[104] R. Carter, The Brain Book: An Illustrated Guide to Its Structure, Functions, and Disorders. Dorling Kindersley Ltd, 2019. 





[105] Kudithipudi, Merkel, and Kurinec, “Neuromorphic devices and circuits,” in Nano-CMOS and Post-CMOS Electronics: Devices and Modelling. Institution of Engineering and Technology, pp. 337–356. [Online]. Available: https://doi.org/10.1049%2Fpbcs029e ch12 





[106] D. Wouters, “From Emerging Memory to Novel Devices for Neuromorphic Systems: Consequences for the Reliability Requirements of Memristive Devices,” in 2019 IEEE International Reliability Physics Symposium (IRPS). IEEE, mar 2019. [Online]. Available: https://doi.org/10.1109%2Firps.2019.8720523 





[107] A. P. James, “Towards strong ai with analog neural chips,” in 2020 IEEE International Symposium on Circuits and Systems (ISCAS), 2020, pp. 1–5. 





[108] J. Shalf, “The future of computing beyond Moore’s Law,” Philosophical Transactions of the Royal Society A: Mathematical Physical and Engineering Sciences, vol. 378, no. 2166, p. 20190061, jan 2020. [Online]. Available: https://doi.org/10.1098%2Frsta.2019. 0061 





[109] F. Schwierz and J. J. Liou, “Status and Future Prospects of CMOS Scaling and Moore's Law - A Personal Perspective,” in 2020 IEEE Latin America Electron Devices Conference (LAEDC). IEEE, feb 2020. [Online]. Available: https://doi.org/10.1109%2Flaedc49063. 2020.9073539 





[110] R. P. Feynman, “There’s plenty of room at the bottom,” California Institute of Technology, Engineering and Science magazine, 1960. 





[111] C. E. Leiserson, N. C. Thompson, J. S. Emer, B. C. Kuszmaul, B. W. Lampson, D. Sanchez, and T. B. Schardl, “Therea??s plenty of room at ˆ the top: What will drive computer performance after moorea??s law?” ˆ Science, vol. 368, no. 6495, 2020. 





[112] T. Brandon, B. Cockburn, and D. Elliott, “HDL2GDS: a fully automated ASIC digital design flow,” in Canadian Conference on Electrical and Computer Engineering 2005. IEEE. [Online]. Available: https://doi.org/10.1109%2Fccece.2005.1557272 





[113] Y. Uguen and E. Petit, “PyGA: a Python to FPGA compiler prototype,” in Proceedings of the 5th ACM SIGPLAN International Workshop on Artificial Intelligence and Empirical Methods for Software Engineering and Parallel Computing Systems - AI-SEPS 2018. ACM Press, 2018. [Online]. Available: https://doi.org/10.1145%2F3281070.3281072 





[114] K. Hakhamaneshi, N. Werblun, P. Abbeel, and V. Stojanovic, “BagNet: Berkeley Analog Generator with Layout Optimizer Boosted with Deep Neural Networks,” in 2019 IEEE/ACM International Conference on Computer-Aided Design (ICCAD). IEEE, nov 2019. [Online]. Available: https://doi.org/10.1109%2Ficcad45719.2019.8942062 





[115] O.Krestinskaya, K. Salama, and A. P. James, “Automating Analog AI Chip Design with Genetic Search,” Advanced Intelligent Systems, 2020. 





[116] D. Monett, C. W. Lewis, and K. R. Thorisson, “Introduction to the ´ jagi special issue on defining artificial intelligence commentaries and author’s response,” Journal of Artificial General Intelligence, vol. 11, no. 2, pp. 1–100, 2020. 





[117] P. Wang and B. Goertzel, Theoretical foundations of artificial general intelligence. Springer, 2012, vol. 4. 





[118] J. Hernandez-Orallo, ´ The measure of all minds: evaluating natural and artificial intelligence. Cambridge University Press, 2017. 



![image](https://cdn-mineru.openxlab.org.cn/result/2026-03-22/63b2b94d-c20b-4c10-b6e5-2ee4374abaf4/29a56d27445e9b6a9a316242d2a760714da79c1480e2638279e7f15b6e7703f6.jpg)


A. P. James works in the area of AI hardware and imaging systems. He completed his Ph.D. from Queensland Micro-and Nanotechnology Centre, Griffith University, Queensland, Australia. He is currently a Full Professor at the School of Electronic Systems and Automation, Kerala University of Digital Sciences, Innovation and Technology (KUDSIT), and the in-charge of the Maker Village - Indian Institute of Information Technology and Management, Kerala, one of the largest electronics incubator facilities in India, funded by the Government of 

India and Government of Kerala. He is a member of IEEE CASS technical committee on Nonlinear Circuits and Systems. He was the founding chair of IEEE CASS Kerala chapter and was a member of IET Vision and Imaging Network. He has authored more than $1 5 0 +$ peer-reviewed publications in the area of AI hardware, algorithms and imaging systems. He is a mentor to several tech startups and co-founded companies in machine learning and computer vision. He has been an active reviewer to top journals and conferences such as IEEE ISCAS, IEEE ICECS, Nature Electronics, TCAS1, TCAS2, TVLSI, TCAD, TCyb, TEC, TIP etc. He was an editorial board member of Information Fusion (2010-2014), HCIS, and currently serving associate editor of IEEE Access, and IEEE Transactions on Circuits and System 1 (2018-present) journal. He is a Senior Member of IEEE, Life Member of ACM, Senior Fellow of HEA and Fellow of BCS. 