![image](https://cdn-mineru.openxlab.org.cn/result/2026-03-22/9e8e7a45-a998-426a-b85b-ec6639a97212/bfa84c81afb11064fd062ac3e8485e0cc6a307d264aa2743d236e00eeaa6560d.jpg)


# Edge Artificial Intelligence Chips for the Cyberphysical Systems Era

Hiroshi Fuketa and Kunio Uchiyama, National Institute of Advanced Industrial Science and Technology, Japan 

Artificial intelligence (AI) chips draw much attention for cyberphysical systems since AI chips are promising to realize edge AI computing. We introduce the chip architecture that enables energy-efficient computing and design tools for AI chips. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-03-22/9e8e7a45-a998-426a-b85b-ec6639a97212/fa3a1bb3a75e8f4bced67b09012ee4216fc248af1b3f358df086a4a5d54ea613.jpg)


he dramatic progress of artificial intelligence (AI) in recent years is mainly the result of advances in deep learning (DL) algorithms. DL-based AI is used now in a wide variety of applications, such 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-03-22/9e8e7a45-a998-426a-b85b-ec6639a97212/9081c336459bd5fb977c3a9ca4d15b8068a4ac558167bccca04857589a10e2a3.jpg)


as image recognition and machine translation. However, it is reported that the amount of computation required to run these algorithms has been exponentially increasing, with a 3.4-month doubling time since 2012.1 Therefore, AI chips, which can compute DL algorithms more efficiently compared to conventional CPUs and GPUs, have been drawing much attention. [In this column, we use “AI chips” as a generic term for DL accelerators, and hence the following two types of implementations for AI chips are considered: 1) independent large-scale integrations, including Google’s tensor pro-

cessing unit, and 2) intellectual property (IP) cores, such as the neural engine in Apple’s A series system on chip.] 

For example, Google and Amazon have been developing original AI chips for their own data centers. These chips are called cloud AI chips, and they are used for training deep neural network (DNN) models as well as for inference using DNN models when the amount of computation is too large 

for edge devices. However, for cyberphysical system (CPS) applications, such as autonomous driving and factory automation (Figure 1), it is critical to conduct AI processing on edge devices since performing the work on cloud servers entails overhead related to the communication time between the edge and the cloud and the power that is consumed, which is often a crucial factor in CPSs. Therefore, “edge AI chips” that enable AI processing on edge devices are demanded for CPSs. For example, Tesla recently developed an original edge AI chip for autonomous driving. One of the most important requirements for edge AI chips is energy efficiency since edge device power budgets are usually severe. Therefore, various processor architectures to perform DL algorithms on edge devices with high energy efficiency have been recently proposed. 

In this column, we describe the architecture of edge AI chips, and we introduce tools that help engineers design such edge AI chips. We mainly focus on image recognition tasks, which are required in typical CPS applications such as autonomous driving and factory automation. 

# AI CHIP ARCHITECTURE FOR ACHIEVING HIGH ENERGY EFFICIENCY

# Architecture suitable for

# computation in neural networks

A DNN consists of many stacked layers of neural networks. As a typical neural network architecture, Figure 2 shows a fully connected (FC) neural network and a convolutional neural network (CNN). In the FC version, the output activations are calculated by the weighted sum of the input activations [Figure 2(a)]. As the number of input and output activations increases, a large amount of memory capacity and 

bandwidth for weights and computation is required. On the other hand, a CNN is often used for image recognition tasks. CNNs consist of multiple 

filters, and the output feature map is calculated by sliding those filters in the input feature map, as represented in Figure 2(b). 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-03-22/9e8e7a45-a998-426a-b85b-ec6639a97212/e11f34640eea47240fe7557a2daf07606af4b8fe16e40b4db4fe907f49555c00.jpg)



(a)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-03-22/9e8e7a45-a998-426a-b85b-ec6639a97212/24c9818ac7d4db3f190c79add3e5c683fa808908a45cf532443703fcc308d3f6.jpg)



Data Center


![image](https://cdn-mineru.openxlab.org.cn/result/2026-03-22/9e8e7a45-a998-426a-b85b-ec6639a97212/10b98f1ca6e2f04ca9d3cac48bb4fe289b18cdaaa521216b7f6ed951644c61b1.jpg)



Cloud AI Chip



• Training and Inference



• High Performance



(b)



FIGURE 1. AI chips for (a) the edge and (b) the cloud in CPSs.


![image](https://cdn-mineru.openxlab.org.cn/result/2026-03-22/9e8e7a45-a998-426a-b85b-ec6639a97212/de754773530d1520440d2e06f8c4ebe05204fe7d6519a52aae767727be116aa6.jpg)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-03-22/9e8e7a45-a998-426a-b85b-ec6639a97212/ca46d846acc6d7ec315408c0873a1036dd7f5cd7ad22c05b05ae2866340b2b32.jpg)



(a)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-03-22/9e8e7a45-a998-426a-b85b-ec6639a97212/d6f4a69fffdf7ebfc9efe9b1691f141f65a188abbdfddceba1843eba5ea0fc3e.jpg)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-03-22/9e8e7a45-a998-426a-b85b-ec6639a97212/af91ca0643512311199dae6dd1677984bca821b3624ed19e844a903ef9143f81.jpg)



(c)



(d)



FIGURE 2. (a) and (b) The network architecture and (c) and (d) a form of parallelization to accelerate the computation of neural networks2 (a) FC, (b) CNN, (c) the temporal architecture (GPU), and (d) the spatial architecture (AI chip). RF: register file; ALU: arithmetic logic unit; CTRL: control circuit.


The FC and CNN calculation methods are described at the bottom of Figure 2(a) and (b). As indicated by these equations, the calculations mainly consist of multiply and accumulate (MAC) operations. It is well known that the performance of MAC operations can be improved by parallelization. In common GPUs, massive arithmetic logic units (ALUs) are implemented based on the temporal architecture,2 as in Figure 2(c), and operate in parallel, which makes it possible to perform MAC operations fast. Therefore, GPUs are widely used for DNN processing. 

Another form of parallelization is the spatial architecture (dataflow processing),2 as depicted in Figure 2(d). In this architecture, processing elements 

(PEs) are organized in tiles, and each one consists of an ALU, a register file (RF), and a control circuit. In the temporal architecture [Figure 2(c)], the ALU reads the input data from and writes the calculation result back to the shared RF, whereas in the spatial architecture [Figure 2(d)], data (activations, weights, and partial sums) can be moved from one PE to another, which reduces the memory access energy requirement. For example, the values of filters (weights) are used many times for computation in a CNN, as in Figure 2(b). The memory access can be reduced by 1) storing these values to the RF in a PE and reusing them and 2) transferring partial sums from one PE to another. This makes 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-03-22/9e8e7a45-a998-426a-b85b-ec6639a97212/b66ed2552633cf88323cefd6021499998bbe5aa2d7cdaddc4f1795064b64b9f0.jpg)



(a)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-03-22/9e8e7a45-a998-426a-b85b-ec6639a97212/51129aeed9cfdf31053f3070d64a0cc2de3d5b183e44833b382a7f590e883c53.jpg)



(b)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-03-22/9e8e7a45-a998-426a-b85b-ec6639a97212/7ef877aa4d7e1e0200a15e1352e7aeef20b99a59941ffcbc006261e52089f187.jpg)



FIGURE 3. (a) The energy efficiency of edge AI chips. (b) The implementation of a MAC unit. INT: integer; BNN: binarized neural network.


computation more energy efficient, and hence the spatial architecture is suitable for edge AI chips. 

# Reducing computational precision

The most effective way to improve energy efficiency is to reduce computational precision. For common computational tasks, 32-bit floating point (FP32) precision is usually used. In contrast, it is well known that the degradation of computational accuracy is ignorable for DNN tasks (training and inference), even if a lower precision than FP32 is used. For training, 16-bit FP (FP16) precision is often used, and hence many GPUs currently support FP16. In addition, recent studies show the possibility of reducing the computational precision to 8–9 bits for multiplication.3,4 

On the other hand, a further reduction of the computational precision is feasible for the inference. For example, Guo et al.5 reported that the image recognition accuracy deteriorates by less than $3 \%$ , even if the computational precision is altered to an 8-bit integer from FP32. At this time, the computation energy is significantly reduced; the energy of the 8-bit integer adder and multiplier is 1/30 and 1/19 times smaller than that of the FP32 adder and multiplier, respectively.6 This means that reducing the computational precision is very attractive to attain high energy efficiency. Therefore, many edge AI chips that support the low-precision format of a 4/8/16-bit integer have recently been developed since edge AI computing mainly focuses on the inference, as detailed in Figure 1. Figure 3(a) presents the power dissipation of edge AI chips as a function of the performance [in tera operations per second (TOPS)], with their energy efficiency (TOPS/W). By reducing the computational precision to a 4/8-bit integer, a high energy efficiency of several TOPS/W can be achieved. 

Recently, many researchers have explored a more aggressive reduction of the computational precision to 1 bit (binary), which is the lowest that is 

possible. Neural networks with a 1-bit precision are called binarized neural networks (BNNs).7 In BNNs, a single XNOR gate is substituted for a multiplier, and a population counter that tallies the number of ones in an input word is used as an accumulator [as shown in Figure 3(b)], which makes the implementation of the MAC unit much simpler. Thus, extremely high energy efficiency can be achieved by a BNN. For example, Intel developed an AI chip dedicated to BNNs and demonstrated that a significantly high energy efficiency of 617 TOPS/W can be achieved.8 However, one of the disadvantages of BNNs is that the networks’ inference accuracy degrades due to the reduction of the computational precision, especially for complicated tasks. For instance, the inference accuracy when using BNNs deteriorates by only $1 \%$ compared to FP32 precision for the “CI-FAR10” small photo classification task, whereas the accuracy worsens by $1 6 \%$ for the more complicated “ImageNet” image classification task.7,9 A practical solution for this issue is to optimize the computational precision at each layer of a neural network. This makes it possible to achieve both high accuracy and energy efficiency. 

# DESIGN TOOLS FOR EDGE AI CHIPS

Almost all engineers develop DL algorithms by using Python. On the other hand, AI chips are usually devised through a hardware description language, such as Verilog. It is desirable to more easily or automatically create hardware optimized for DL algorithms written in Python. Thus, various design tools for AI chips have recently been developed. As examples, we will describe two tools that focus on developing field-programmable gate array (FPGA)-based edge AI chips. 

1. Vitis AI: Xilinx has been developing the Vitis AI development environment for its own FPGA products. Vitis AI supports major DNN frameworks written 

in Python, such as TensorFlow and PyTorch, and offers various tools that optimize DNN models for hardware implementations, such as 1) pruning, which reduces the model parameters (the number of weights), with a minimal impact on accuracy, and 2) quantization, which lessens the computational precision, from FP32 to the 8-bit integer. 

2. GUINNESS: This is a graphical user interface-based framework that provides bitstream generation for a Xilinx FPGA. One of the advantages of GUIN-$\tt N E S S ^ { 1 0 }$ is that it supports BNNs (the details were explained in the previous section), which enables more energy-efficient computing. 

Please note that these tools target FPGAs only. One of the reasons is that, currently, the research and development of DL algorithms are mainly conducted by software engineers. FPGAs are appropriate devices for those engineers to use to try to accelerate DL algorithms on custom hardware since the cost of the FPGA development environment, i.e., design tools and the evaluation board, is reasonable. 

lthough FPGAs are easy to use, their performance and energy efficiency are less than those of application-specified integrated circuits (ASICs). Thus, ASICs for AI are preferable under performance- and power-constrained situations. In particular, ASICs offer the most efficient solution in application domains such as edge computing in CPSs, on which we mainly focused in this column, in terms of power, performance, and cost. However, expensive design environments, such as electronic design automation tools, IPs, and emulators, are required to design AI ASICs, which is a big hurdle for start-ups and small enterprises. To overcome this 

hurdle, for example, the AI chip design center11 funded by the Japanese government provides a design and verification environment for accelerating the development of AI chips in that country. Through such measures, it is expected that various edge AI chips will be developed in the near future, which will promote the growth of CPSs. 

# REFERENCES



1. “AI and compute.” OpenAI. https://openai.com/blog/ai-and -compute/ (accessed Nov. 19, 2020). 





2. V. Sze, Y. Chen, T. Yang, and J. S. Emer, “Efficient processing of deep neural networks: A tutorial and survey,” Proc. IEEE, vol. 105, no. 12, pp. 2297–2329, 2017. doi: 10.1109/ JPROC.2017.2761740. 





3. N. Wang, J. Choi, D. Brand, C.-Y. Chen, and K. Gopalakrishnan, “Training deep neural networks with 8-bit floating point numbers,” in Proc. NeurIPS, 2018, pp. 7675–7684. 





4. S. O’uchi et al., “Image-classifier deep convolutional neural network training by 9-bit dedicated hardware to realize validation accuracy and energy efficiency superior to the half precision floating point format,” in Proc. 2018 IEEE Int. Symp. Circuits Syst. (ISCAS), pp. 1–5. doi: 10.1109/ ISCAS.2018.8350953. 





5. K. Guo et al., “From model to FPGA: Software-hardware co-design for efficient neural network acceleration,” in Proc. 2016 IEEE Hot Chips 28 Symp. (HCS), pp. 1–27. doi: 10.1109/ HOTCHIPS.2016.7936208. 





6. S. Han, “Efficient methods and hardware for deep learning,” Stanford University, Stanford, CA, 2017. [Online]. Available: http:// cs231n.stanford.edu/slides/2017/ cs231n_2017_lecture15.pdf 





7. M. Courbariaux et al., “Binarized neural networks: Training neural networks with weights and activations constrained to $+ 1$ or −1,” 2016. [Online]. Available: arXiv:1602.02830 





8. P. C. Knag et al., “A 617TOPS/W All Digital Binary Neural Network 





Accelerator in 10nm FinFET CMOS,” in Proc. 2020 IEEE Symp. VLSI Circuits, pp. 1–2. doi: 10.1109/ VLSICircuits18222.2020.9162949. 





9. M. Rastegari et al., “XNOR-Net: ImageNet classification using binary convolutional neural networks,” 2016. [Online]. Available: arXiv:1603.05279 





10. H. Nakahara, H. Yonekawa, T. Fujii, M. Shimoda, and S. Sato, “GUIN-NESS: A GUI based binarized deep neural network framework for software programmers,” IEICE Trans. Inf. Syst., vol. E102.D, no. 5, pp. 1003–1011, 2019. doi: 10.1587/ transinf.2018RCP0002. 





11. AI Chip Design Center. (in Japanese). https://www.ai-chip-design-center.org (accessed Nov. 19, 2020). 





12. Y.-H. Chen, T. Krishna, J. Emer, and V. Sze, “Eyeriss: An energy-efficient reconfigurable accelerator for deep 





convolutional neural networks,” in Proc. IEEE Int. Conf. Solid-State Circuits (ISSCC), pp. 262–264, Feb. 2016. doi: 10.1109/ISSCC.2016.7418007. 





13. Google, Edge TPU, 2018. https:// cloud.google.com/edge-tpu (accessed Nov. 19, 2020). 





14. C. Lin et al., “7.1 A 3.4-to-13.3TOPS/W 3.6TOPS dual-core deep-learning accelerator for versatile AI applications in 7nm 5G smartphone SoC,” in Proc. 2020 IEEE Int. Solid-State Circuits Conf. (ISSCC), San Francisco, CA, 2020, pp. 134–136. doi: 10.1109/ ISSCC19947.2020.9063111. 





15. J. Lee, C. K im, S. Ka ng, D. Sh in, S. Kim, and H. Yoo, “UNPU: A 50.6TOPS/W unified deep neural network accelerator with 1b-to-16b fully-variable weight bit-precision,” in Proc. 2018 IEEE Int. Solid-State Circuits Conf. (ISSCC), San Francisco, CA, 



2018, pp. 218–220. doi: 10.1109/ ISSCC.2018.8310262. 

HIROSHI FUKETA is a senior researcher at the Device Technology Research Institute and AI Chip Design Open Innovation Laboratory, National Institute of Advanced Industrial Science and Technology, Tokyo, Japan. He is a Member of IEEE. Contact him at h-fuketa@aist.go.jp. 

KUNIO UCHIYAMA is an invited senior researcher at the AI Chip Design Open Innovation Laboratory, National Institute of Advanced Industrial Science and Technology, Tokyo, Japan. He is a Fellow of IEEE. Contact him at kunio.uchiyama@aist.go.jp. 

quidelines: 

suter.org/mch 

www.c thor.htm 

pervasiv details: 

Further somputer.org 

pervasive@comp erorg/pervast 

www.comp 

# Call Articles

sr Pervasive Compde latest IEEL-ible useful papers Onuasive, seeksaeiweddevelopmentsipaTopi peer-rewnd ubiquitous comput Stware mobllersrdware technology.Sttand nciudeture.real-world sens.stera initasetion human-computerudi nterestomsconsiderations,tiy aner:ument，scalability， secr 

Digital Object Identifier 10.1109/MC.2020.3045251 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-03-22/9e8e7a45-a998-426a-b85b-ec6639a97212/8c1608aca6fbe582dfaba077e3f09207d6b8638dbd7734d977f620640d94b4b5.jpg)
