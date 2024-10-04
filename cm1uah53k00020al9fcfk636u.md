---
title: "The IISc Memristor: A Revolution in Computing and AI Accelerators"
datePublished: Fri Oct 04 2024 05:32:53 GMT+0000 (Coordinated Universal Time)
cuid: cm1uah53k00020al9fcfk636u
slug: the-iisc-memristor-a-revolution-in-computing-and-ai-accelerators
canonical: https://hackernoon.com/the-iisc-memristor-the-dawn-of-a-new-era-in-computing-and-ai-accelerators
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1728019836616/f68ca90a-9ad4-45e0-ac81-7e8bf91df416.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1728019931267/c45d157e-52bf-46c6-8528-73f05aae9292.png
tags: neuromorphic-computing, energy-efficiency, iisc, memristor, ai-accelerators, new-era-in-computing, disrupting-gpus

---

![](https://miro.medium.com/v2/resize:fit:700/0*4A7VXHgOUQuGLY3P.png align="left")

First published on:

[The IISc Memristor: The Dawn of a New Era in Computing and AI Accelerators | HackerNoon](https://hackernoon.com/the-iisc-memristor-the-dawn-of-a-new-era-in-computing-and-ai-accelerators)

## **A New Era in Computation**

A team of researchers at the Indian Institute of Science, Bangalore have just created a revolutionary prototype of a computing paradigm that could shake (and replace) the foundations of modern computing — starting with **the transistor and the GPUs**!

The **Von Neumann architecture and its infamous Bottleneck** on which all our computing systems are built will become obsolete if this revolutionary model can scale.

This technology, called **neuromorphic computing** (computing that mimics the brain), uses **memristors** (a foundation device that can access multiple levels of state at once = to be precise, 16,500+ states in the groundbreaking novel prototype) **to blow the acceleration of even quantum computing out of the park.**

Basically:

**A team of researchers at the Indian Institute of Science (IISc) has achieved a revolutionary breakthrough in artificial intelligence, potentially changing the global technology landscape. They have developed a brain-inspired computing platform with the potential to make AI significantly faster, more efficient, and accessible to a wider population.**

This groundbreaking platform utilizes a molecular film capable of storing and processing data in an astounding 16,500 conductance states, dwarfing the limitations of traditional digital computers restricted to just two states. This radical departure from conventional computing paradigms allows for significantly faster and more energy-efficient processing of complex AI algorithms, particularly matrix multiplication, which forms the backbone of most AI applications.

The implications of this discovery are far-reaching. It paves the way for bringing complex AI tasks, such as training Large Language Models (LLMs), currently confined to resource-intensive data centers, **to personal devices like laptops and smartphones.** This democratization of AI technology could empower individuals and smaller organizations with powerful AI tools, fostering innovation across various fields.

Moreover, this entirely homegrown Indian innovation positions the nation as a leading force in AI hardware development. With its potential to revolutionize industrial, consumer, and strategic applications, this breakthrough aligns perfectly with India’s Semiconductor Mission, promising significant economic and technological advancement. **The world is on the brink of an AI revolution, and this time, India is leading the charge.**

To know more, let’s start with the basics.

### **The Von Neumann Bottleneck**

The Von Neumann architecture (image from Wikimedia)

![](https://miro.medium.com/v2/resize:fit:700/0*1iPIZOYQwvt_4S82.png align="left")

The **Von Neumann Architecture bottleneck**, often referred to as the **Von Neumann bottleneck**, is a limitation arising from the way traditional computer systems based on this architecture handle data. Here’s a breakdown targeted to a computer scientist:

### **Von Neumann Architecture Overview**

The Von Neumann architecture consists of four key components:

1. **Central Processing Unit (CPU)** — The core unit that performs computations.
    
2. **Memory (RAM)** — Where instructions and data are stored.
    
3. **Input/Output (I/O) System** — Handles interaction with external devices.
    
4. **Bus** — Communication pathways that connect the CPU, memory, and I/O systems.
    

One fundamental aspect of this architecture is that both instructions (program code) and data share the same memory space and use the same communication bus.

### **The Bottleneck**

The Von Neumann bottleneck arises because the CPU and memory must communicate over the same bus to fetch both data and instructions. This creates a **sequential processing bottleneck**, as only one transaction can occur at a time (either fetching an instruction or fetching data). The limitation becomes more pronounced as processing power (CPU) increases, but the memory access speed does not keep up, causing the CPU to spend more time idle, waiting for instructions or data to arrive.

### **Key Bottleneck Aspects:**

1. **Instruction Fetch and Data Fetch Conflict**: Since both program instructions and data share the same memory, the CPU cannot access both simultaneously. If the program needs data while executing an instruction, the CPU must wait for the next bus cycle to fetch it.
    
2. **Memory Latency**: Even though modern CPUs are extremely fast, memory access speeds have not scaled at the same rate. As a result, CPUs often stall while waiting for data, leading to wasted clock cycles.
    
3. **Bandwidth Limitation**: The bus bandwidth, which defines how much data can be transmitted between the CPU and memory at once, limits the overall throughput. This becomes a critical bottleneck when dealing with large data sets or complex computations.
    

### **Performance Implications:**

1. **Underutilization of CPU**: The CPU, though capable of executing instructions at very high speeds, is often underutilized because it spends time waiting for memory operations to complete. This mismatch between processing power and memory access speed creates inefficiencies.
    
2. **Increased Latency**: Program execution can be delayed due to the sequential nature of instruction and data fetching. This delay worsens with the growing complexity of applications and data-intensive processes.
    

### **Mitigations:**

1. **Cache Memory**: Modern architectures introduce cache memory (L1, L2, L3) to store frequently accessed data and instructions closer to the CPU, reducing the need to access slower main memory frequently.
    
2. **Pipelining**: Breaking down instruction execution into multiple stages (fetch, decode, execute, etc.) allows overlapping of instruction processing to some extent, increasing CPU throughput.
    
3. **Memory Interleaving and Out-of-Order Execution**: Techniques like memory interleaving and allowing the CPU to execute instructions out-of-order based on data availability help alleviate the bottleneck by optimizing memory access patterns.
    

In essence, the Von Neumann bottleneck highlights the performance constraint in conventional computer systems, where the throughput of instruction and data transfers is limited by the shared bus between the CPU and memory. As processors get faster, this limitation has become more noticeable, driving innovations in computer architecture to mitigate its effects.

So, control, data, and input/output signals have to travel via memory pathways called buses and while the processor is very fast, memory transfer is not, data transfer is I/O bound and hence even slower.

**This is the reason that GPUs came into prominence.**

**By utilizing massive parallelism in the processors, GPUs operate in parallel by default and deal with data in AI almost independently of the central processor, and speed up AI data operations by 4 orders of magnitude.**

But now, we have a new kid on the block.

**Neuromorphic Computing.**

A novel, brain-inspired, intrinsically parallel architecture that had little commercial viability — until last week.

![](https://miro.medium.com/v2/resize:fit:700/0*Pym3dZ1sBkVnsqNi.png align="left")

# **The IISc Neuromorphic Computing Memristor Breakthrough**

Neuromorphic computing is an exciting area of technology that aims to replicate how the human brain processes information. Instead of using traditional silicon-based computers that operate on binary systems (0s and 1s), neuromorphic computing mimics the brain’s structure and function, allowing for more efficient and powerful data processing.

## **What is Neuromorphic Computing?**

**In simple terms, neuromorphic computing involves creating computer systems that work like our brains.** The human brain processes information using networks of neurons and synapses, which communicate through electrical signals. Neuromorphic systems use similar principles but are built with specialized hardware that can adapt and learn from experiences, much like how we learn from our environment.

## **The Breakthrough at IISc**

Researchers at the Indian Institute of Science (IISc) in Bengaluru have recently made a groundbreaking advancement in neuromorphic computing by developing **a platform that can store and process data in an astonishing 16,500 different states within a molecular film.** This is a significant leap from traditional computers, which are limited to just two states (high and low conductance) for data processing and storage.

### **How They Did It**

**The IISc team created a memristor, a type of semiconductor device that mimics the brain’s neural networks.** This device uses a metal-organic film to track the movement of molecules and ions, allowing it to access many more memory states than conventional computers. They developed a custom circuit board capable of measuring extremely small voltages, enabling them to pinpoint these various states accurately.

This innovative approach allows the neuromorphic platform to perform complex calculations, such as matrix multiplication, much faster and with less energy than traditional digital computers. **For example, they successfully recreated NASA’s “Pillars of Creation” image using minimal energy and time compared to what would typically be required by supercomputers.**

### **Challenges Overcome**

The researchers faced several challenges, including:

* **Precision Measurement:** Developing a system that could accurately measure tiny voltage changes was crucial. They designed new equipment that could detect voltages as small as a millionth of a volt.
    
* **Energy Efficiency:** Traditional computing systems consume a lot of energy, especially for AI tasks. The new platform drastically reduces energy consumption, making it much more efficient.
    
* **Scalability:** While the initial tests were successful, scaling the technology for broader applications remains a challenge. The team plans to expand their memristor arrays to larger configurations.
    

### **Possible Ramifications**

The implications of this breakthrough are significant:

1. **Democratizing AI:** This technology could enable complex AI tasks to be performed on personal devices like laptops and smartphones, rather than relying on large data centers. This shift could make powerful AI tools more accessible to everyone.
    
2. **Energy Savings:** Businesses that rely on high-speed computing, such as finance and tech companies, could see reduced energy costs and faster data processing capabilities.
    
3. **Advancements in AI:** With faster and more efficient computing, advancements in artificial intelligence and machine learning could accelerate, leading to smarter applications and tools.
    
4. **Global Leadership:** This breakthrough positions India as a potential leader in AI hardware development, contributing to the global tech landscape.
    

## **The Mind-Boggling Implications of this Discovery**

![](https://miro.medium.com/v2/resize:fit:700/0*wmAg2OSDWJd063sp.png align="left")

**Matrix Multiplication can be performed in a single step.**

This is huge. Matrix and vector multiplication is the heart of AI today — specifically speaking Generative AI. Instead of multiplying term by term, if the entire multiplication of even 64x64 matrics could be done in parallel in one step — that would be a step forward like nothing ever seen — yet. And if the system could scale to 512x512 or even 1024x1024 (though challenges remain — we’ll address that) **all of Nvidia’s chips would be obsolete. I realize that’s a massive claim — but it’s just the facts.**

**Power consumption is decreased 460x from digital computers**

Where GPUs require megawatts of electricity even weekly, this system produced a HPC application with millionths of a single volt. In fact, the biggest innovation in the research paper is the exceptionally fine-grained control over very small volt rates — which are instrumental in producing the 16,520 conductance states, each of which can hold data. **This could be the answer to the energy consumption problem and the future of green computing for AI hardware.**

**Edge Computing could have AI Accelerators Soon**

Neuromorphic systems as powerful as the Hopper architectures from Nvidia could be deployed on edge devices like IOT, mobiles, budget laptops and phablets. This has massive implications for artificial intelligence of the Edge — immense calculations and sophisticated processing could be possible with devices in the palm of your hand. **No more necessity for even 8 VRAM GPUs!**

**SLMs could reach the largest LLM performance**

Who needs Elon Musk’s Colossus supercomputer cluster when SLMs could soon be performing at the level of LLMs soon (with a complete rewrite in memristor technology)? Scale could become a problem of the past. Quantum computing promised HPC but is still in experimental stages. **In this neuromorphic computing discovery, we have a greater speedup than quantum computing which already has a real-world prototype!**

**System-on-a-Chip (SoC) could be all we need for computers**

The researchers at IISc plan to produce a complete hardware-based architecture that could scale this 64x64 prototype massively. If that happens, costs will reduce drastically, all input could be audio-based, and the display could be a powerful projector on any surface you want. **The very notion of a computer will take a quantum leap**. But don’t hold your breath — **the rough timeline is three years** (very rough)**.**

## **The Advantages of the IISc Memristor Prototype**

### **Speedup Potential**

1. **Parallel Processing Capabilities:** Neuromorphic systems can perform many operations simultaneously due to their massively parallel architecture. Each neuron in a neuromorphic chip can execute different functions at the same time, theoretically allowing neuromorphic devices to handle as many tasks as there are neurons. **This parallelism can lead to substantial speed improvements for tasks that are inherently parallelizable, such as those found in machine learning and AI applications.**
    
2. **Event-Driven Computation**: **Unlike traditional processors that operate on a clock cycle, neuromorphic systems utilize event-driven computation.** This means that neurons only activate when they receive input spikes, which can lead to faster processing times as only the relevant parts of the system consume power and process data at any given moment.
    
3. **Reduced Latency:** By co-locating memory and processing, **neuromorphic computing avoids the von Neumann bottleneck, where data transfer between separate memory and processing units slows down computation.** This integrated approach can result in lower latency and faster response times for complex computations.
    

### **Power Gains**

1. **Energy Efficiency:** **Neuromorphic computing systems are designed to be highly energy-efficient.** Research indicates that they can be four to sixteen times more energy-efficient than traditional AI systems running on conventional hardware. For instance, Intel’s Loihi chip demonstrated this efficiency while processing large neural networks.
    
2. **Low Power Consumption:** The human brain operates on about 20 watts, which is significantly less than what current SOTA processors require for similar tasks. Neuromorphic systems can achieve comparable cognitive tasks with much lower energy budgets, **making them suitable for edge computing applications where power is limited.**
    
3. **Idle Power Consumption:** In neuromorphic systems, most of the neurons remain idle until activated by an event, leading to dramatically lower overall power consumption during non-active periods. **This contrasts sharply with traditional processors, which often consume power continuously even when idle.**
    

## **Applications of Memristor Technology**

### **1\. Artificial Intelligence and Machine Learning**

Memristors can be integrated into neural networks to create highly efficient and adaptable AI systems. **Their ability to store and process information simultaneously allows for faster learning and inference, making them ideal for applications in deep learning and real-time decision-making.**

### **2\. Edge Computing AI**

Memristors enable AI processing directly on edge devices, reducing the need for cloud computing. This capability allows for faster response times and lower energy consumption, **crucial for applications in autonomous vehicles, drones, and smart sensors.**

### **3\. Brain-Machine Interfaces (BMIs)**

Memristor technology can facilitate direct communication between the human brain and external devices. This could lead to advanced BMIs that allow for seamless interaction with machines, **potentially enhancing capabilities in rehabilitation, assistive technologies, and even cognitive enhancement.**

### **4\. Internet of Things (IoT)**

Memristors can significantly improve the efficiency of IoT devices by enabling local data processing. This reduces bandwidth usage and enhances privacy by minimizing data transmission to central servers. **Applications include smart homes, industrial automation, and environmental monitoring systems.**

### **5\. Self-Powered AI Systems**

**When combined with energy harvesting technologies, memristor-based systems can operate independently of traditional power sources**. This self-powered capability is particularly useful for remote sensors and devices deployed in challenging environments, such as disaster zones or deep-sea explorations.

### **6\. Advanced Robotics**

The integration of memristors into robotic systems could enhance their learning capabilities and adaptability. **Robots could learn from their environments in real-time**, improving their performance in tasks ranging from manufacturing to healthcare.

### **7\. Real-Time Data Analytics**

**Memristors can process large volumes of data quickly and efficiently, making them suitable for applications in big data analytics.** This could transform industries such as finance, healthcare, and telecommunications by enabling faster insights and decision-making.

### **8\. Neuromorphic Computing**

Memristors are essential for developing neuromorphic computing systems that mimic the brain’s architecture. This technology promises to overcome the limitations of traditional computing, **enabling more efficient processing of complex tasks like pattern recognition and sensory processing.**

## **Simply Explained**

![](https://miro.medium.com/v2/resize:fit:700/0*o6mTrPuHHTD_vtU4.png align="left")

In a standard computer, the memory and the processing units are separate.

This leads to a bottleneck in data transfer, which wastes CPU cycles.

In neuromorphic computing, each memristor is a unit of processing and memory combined.

This means that there is no segregation between data and compute.

And all memristors are connected.

This is parallel processing of the very highest order.

Standard computers use a concept called **Single Instruction, Multiple Data, also known as SIMD**.

Supercomputers using parallel computing have **Multiple Instructions, Multiple Data, also known as MIMD.**

Memristor-based Neuromorphic Computing requires a new term: **Decentralized Instructions, Decentralized Data — DIDD — a term I coined just now.**

These systems require a new kind of thinking an a new class of algorithms.

**Every memristor should have a part of the data and a parallel programming language that is decentralized.**

This system should work on its own, event-driven, and reach its goal performing intrinsically parallel operations.

For example:

Linear Algebra can be performed in single steps using Kirkhoff’s law and Ohm’s law.

What do I mean by that?

## **How Linear Algebra Works on the IISc Prototype**

Kirchhoff’s Law and Ohm’s Law enable linear algebra operations in the IISc memristor prototype.

### **Memristor Crossbar Array**

The IISc memristor prototype uses a grid called a crossbar array. In this grid, memristors are placed at the points where the rows and columns meet. This setup allows the system to perform important mathematical operations, specifically matrix-vector multiplication.

### **Ohm’s Law and Kirchhoff’s Law**

1. **Input Voltages:** The system applies voltages to the rows (called wordlines). These voltages represent the numbers in a vector that we want to multiply.
    
2. **Memristor Conductances:** Each memristor has a property called conductance, which represents the values in a matrix (the weights). The conductance tells us how much current will flow through the memristor when a voltage is applied.
    
3. **Ohm’s Law:** Ohm’s Law states that the current flowing through a device (like a memristor) is equal to the voltage across it multiplied by its conductance. This means that if we know the voltage and conductance, we can find out how much current flows.
    
4. **Kirchhoff’s Law:** Kirchhoff’s Current Law says that the total current entering a point (like where several memristors connect) must equal the total current leaving that point. In this case, it helps us add up all the currents from the memristors in a column.
    
5. **Output Currents:** The currents that come out of each column represent the results of multiplying the vector by the matrix.
    

### **Importance for Linear Algebra**

Using these laws allows the IISc memristor prototype to perform important calculations:

1. **Matrix-Vector Multiplication:** The system can multiply a matrix by a vector very efficiently without moving data around
    
2. **Matrix-Matrix Multiplication**: By using multiple input vectors at once, it can also multiply two matrices together.
    
3. **Dot Product:** The system can calculate the dot product of two vectors by using one vector as input and treating the other as weights in the memristors.
    
4. **Matrix Inversion:** It can help solve systems of equations by performing matrix inversion operations.
    
5. **Other Calculations:** It can also perform other important calculations used in machine learning and data analysis.
    

Obviously, all these capabilities position this prototype as a clear low-cost alternative to GPUs, one that is also environmentally friendly.

**Which means:**

## **Memristors Can Disrupt GPUs**

Memristors have the potential to disrupt traditional GPU architectures **(and thus Nvidia)** in several ways:

### **Speed and Efficiency**

* Memristors can perform computations directly in memory, without needing to move data between separate memory and processing units. This eliminates a major bottleneck that slows down GPUs.
    
* Memristor crossbar arrays can perform billions of calculations in parallel, much faster than GPUs which process calculations sequentially.
    
* Memristors switch states very quickly, in as little as 85 picoseconds, enabling fast computation speeds.
    

### **Energy Efficiency**

* Memristors consume very little power, as little as 10 femtojoules per state change. They also use no power when idle.
    
* This makes memristors much more energy-efficient than GPUs, which have high power consumption, especially when running large AI models.
    
* The energy efficiency of memristors is especially important for running AI on battery-powered devices like phones and sensors.
    

### **Scalability**

* Memristor crossbar arrays can be easily scaled up by adding more rows and columns.
    
* This allows handling larger AI models and datasets compared to GPUs, whose performance doesn’t scale as well.
    
* Memristors can also be stacked in 3D, enabling very dense and compact AI accelerators.
    

### **Neuromorphic Computing**

* The structure and function of memristor crossbars is similar to biological neural networks in the brain.
    
* This enables neuromorphic computing approaches that mimic brain-like learning and adaptation in AI systems.
    
* GPUs are not well-suited for this type of brain-inspired computing.
    

**Memristors offer major advantages in speed, efficiency, scalability and neuromorphic capabilities compared to GPUs.**

**This makes them a promising alternative for accelerating AI workloads, especially on resource-constrained devices.**

## **Challenges That Still Remain**

The IISc prototype memristor-based device will face several challenges as it develops and moves toward real-world use.

Some of them are:

### **1\. Material Issues**

* **Compatibility:** The materials used in memristors may not work well with current computer chip technology (CMOS), making it hard to integrate them into existing systems.
    
* **Variability:** Memristors can behave differently from one device to another and even in the same device over time. This inconsistency can make them unreliable.
    

### **2\. Device Performance**

* **Analog Behavior:** Memristors may not always perform accurately in their analog functions, which could affect how well they represent the connections (weights) in neural networks.
    
* **Power Consumption:** While memristors are generally energy-efficient, it’s still a challenge to keep their power use low while maintaining good performance.
    

### **3\. Circuit-Level Problems**

* **Scaling Issues:** As memristor arrays get larger, problems like voltage drops (IR drop) and unwanted current paths (sneak paths) can occur, making it harder to manage the array.
    
* **Read/Write Efficiency**: Developing effective circuits for reading and writing data in memristors is necessary to improve their performance.
    

### **4\. Modeling and Simulation**

* **Complexity in Modeling:** Better models are needed to accurately predict how memristors will behave at a larger scale. Current models may not capture all the details needed for real applications.
    

### **5\. System Integration**

* **General Computing Operations:** Creating a complete system that can perform various tasks like data processing and learning is needed for using memristors in neural networks effectively.
    
* **Training Accuracy:** Ensuring that neural networks trained with memristors are accurate requires developing suitable learning methods and network designs.
    

## **Conclusion**

In conclusion, the IISc memristor prototype represents a groundbreaking advancement in computing technology.

With its potential to perform complex calculations faster and more efficiently than traditional systems, it opens up exciting possibilities for the future of artificial intelligence and machine learning.

However, challenges remain for the team before they can achieve any of these lofty goals.

From material compatibility and performance consistency to integration with existing systems, overcoming these hurdles will be crucial for the successful adoption of memristors.

As researchers continue to innovate and refine this technology, we stand on the brink of a new era in computing.

Imagine a world where devices can learn and adapt quickly while using minimal energy.

The journey of memristor technology is just beginning, and its impact could reshape how we think about computing.

The future is bright, and the possibilities are endless.

Keep an eye on this space!

![](https://miro.medium.com/v2/resize:fit:700/0*Gq_4dGzppT711aVm.jpeg align="left")

# **References**

1. Indian Institute of Science (iisc.ac.in) [https://iisc.ac.in/events/neuromorphic-platform-presents-huge-leap-forward-in-computing-efficiency/](https://iisc.ac.in/events/neuromorphic-platform-presents-huge-leap-forward-in-computing-efficiency/) IISc researchers develop a brain-inspired computing platform enabling faster, energy-efficient AI, potentially revolutionizing the field.
    
2. IISC SCIENTISTS REPORT COMPUTING BREAKTHROUGH — NammaKPSC -[https://nammakpsc.com/affairs/iisc-scientists-report-computing-breakthrough/](https://nammakpsc.com/affairs/iisc-scientists-report-computing-breakthrough/) This article discusses the IISc breakthrough in neuromorphic computing, highlighting the development of a memristor that mimics brain functions.
    
3. Indian scientists develop ‘Brain on a Chip’ tech, say can democratise AI — Times of India (indiatimes.com) — [https://timesofindia.indiatimes.com/science/indian-scientists-develop-brain-on-a-chip-tech-say-can-democratise/articleshow/113277241.cms](https://timesofindia.indiatimes.com/science/indian-scientists-develop-brain-on-a-chip-tech-say-can-democratise/articleshow/113277241.cms) Indian researchers create a “brain on a chip” technology that can store and process data in 16,500 states, revolutionizing AI and computing.
    
4. International Researchers Move the Needle on Memristor Technology  
    [https://www.allaboutcircuits.com/news/international-researchers-move-the-needle-on-memristor-technology/  
    ](https://www.allaboutcircuits.com/news/international-researchers-move-the-needle-on-memristor-technology/)This article discusses recent advancements in memristor technology and its implications for AI and neuromorphic computing.
    
5. Memristor Technology and Applications: An Overview  
    [https://www.semanticscholar.org/paper/Memristor-Technology-and-Applications:An-Overview-Shahsavari/892d413c06d7554812d6fbf1d03027b470305000  
    ](https://www.semanticscholar.org/paper/Memristor-Technology-and-Applications:An-Overview-Shahsavari/892d413c06d7554812d6fbf1d03027b470305000)This paper provides an overview of memristors, focusing on their properties and applications in emerging VLSI circuits.
    
6. Memristor Report  
    [https://fb-ti.gi.de/fileadmin/FB/TI/user\_upload/Memristor\_Report-2019-06-27.pdf  
    ](https://fb-ti.gi.de/fileadmin/FB/TI/user_upload/Memristor_Report-2019-06-27.pdf)A detailed report on advancements in memristor technology, including applications in neuromorphic computing and resistive switching.
    
7. AI-Driven Memristor-Based Microchip Design: A Comprehensive Study  
    [https://www.intechopen.com/chapters/1169274  
    ](https://www.intechopen.com/chapters/1169274)This chapter reviews AI-driven memristor-based microchips and their implications for computing applications.
    
8. Recent Advances in In-Memory Computing: Exploring Memristor and Memtransistor Arrays with 2D Materials  
    [https://www.ncbi.nlm.nih.gov/pmc/articles/PMC10876512/  
    ](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC10876512/)This article explores the use of memristors and memtransistors in in-memory computing, focusing on 2D materials.
    
9. The Ouroboros of Memristors: Neural Networks Facilitating Memristor Programming  
    [https://arxiv.org/html/2403.06712v1  
    ](https://arxiv.org/html/2403.06712v1)This document discusses the integration of memristors in neural networks for enhanced programming and computational capabilities.
    
10. Advances in Memristor-Based Neural Networks  
    [https://www.frontiersin.org/journals/nanotechnology/articles/10.3389/fnano.2021.645995/full  
    ](https://www.frontiersin.org/journals/nanotechnology/articles/10.3389/fnano.2021.645995/full)This article explores the design and applications of memristor-based neural networks, emphasizing their potential in various computing fields.
    
11. Memristors — From In‐Memory Computing, Deep Learning Acceleration, and Spiking Neural Networks to the Future of Neuromorphic and Bio‐Inspired Computing  
    [https://onlinelibrary.wiley.com/doi/full/10.1002/aisy.202000085  
    ](https://onlinelibrary.wiley.com/doi/full/10.1002/aisy.202000085)This paper discusses memristors’ role in in-memory computing and their future in neuromorphic and bio-inspired computing applications.
    

[  
](https://medium.com/tag/computing-revolution?source=post_page-----79da43e5b358--------------------------------)