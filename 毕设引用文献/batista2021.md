# Design Strategies for Integrating Artificial Intelligence into Systems Engineering Environment

Leandro Batista  
Computer Science and System Engineering  
Institut Polytechnique de Paris  
Palaiseau, France  
leandro-henrique.batista@ensta-paris.fr 

Abstract—The use of artificial intelligence capabilities for developing airborne safety-critical systems has been troublesome to the aerospace industry. This technology inserts new sources of non-determinism on process execution, increasing difficulty to ensure safety requirements. In this work, we evaluate the artificial intelligence capabilities for improving systems engineering methodology. From this analysis, we present design strategies to support the tool qualification process. The design strategies are a sound basis for applying artificial intelligence into the tools employed during the whole airborne systems life cycle. 

Keywords—Artificial Intelligence, Safety, DO-330 

# I. INTRODUCTION

The systems engineering (SE) paradigm represents the art of methodology used to develop complex systems. SE employs different techniques to build requirements, perform analysis, create traceability, and execute verification and validation tasks. It also empowers system architects during the whole product lifecycle ensuring quality and reducing the certification effort. On the other hand, current tools provide poor integration between the different technologies leading to a laborious data transformation process across the various product development phases. The SE ecosystem can capitalize on artificial intelligence-driven systems, widely used by consumer applications products, to step-up its capabilities and scalability. In this context, one of the main barriers to adopting new tools is the required qualification process. In developing complex systems in a highly regulated environment, the software applications must be qualified according to guidelines. Applications used by aerospace industries to build software according to DO-178C must follow the practices described in the RTCA DO-330 document. 

Given current regulations and emerging technologies, this paper opens a discussion on the operational needs of a large-scale platform for the application of model-based systems engineering. 

This paper proposes design strategies for a new tool architecture for a system engineering environment to operate large-scale projects. This research's objective is twofold: it will first identify the artificial intelligence capabilities for the next-generation platform, and secondly, it will evaluate how artificial intelligence applications can be integrated to reduce the tool validation effort. The concept developed by this research will drive tool design recommendations enabling the use of artificial intelligence-driven applications in a system engineering tooling ecosystem. 

The main result is a list of design strategies for integrating artificial intelligence applications into the SE tooling 

Bruno Monsuez  
Computer Science and System Engineering  
Institut Polytechnique de Paris  
Palaiseau, France  
bruno.monsuez@ensta-paris.fr 

ecosystem. These design recommendations aim to help the tool qualification process according to DO-330 guidelines. 

# II. MODEL-BASED SYSTEMS ENGINEERING

Systems engineering is the industry's de-facto standard framework for the creation of complex and highly integrated systems. Since its origins, the systems engineering culture has grown, and several tools and frameworks have been in use in several industries. 

In recent years a substantial effort has been directed towards implementing a new paradigm for the practice of systems engineering discipline. The model-based systems engineering (MBSE) leverages the lessons learned by the model-driven development (MDD), model-based design (MBD), and software engineering techniques. 

The main goal of MBSE is to create a framework that enables the deployment of a single source of truth for all stakeholders. Traditionally, ensuring that all systems engineers have access to the same model is the most common technique to implement the MBSE paradigm. This is a natural choice since MBSE is an extension of MDD techniques. 

To understand MDD tools' success, we need to acknowledge that the software industry has a more uniform vocabulary and stricter semantics. A more precise language allows the use of code generators and simulation techniques. 

In this paper, we aim to create a conceptual framework capable of implementing the core vision of MBSE and unleash the value added by artificial intelligence applications. We employ an abstract methodology for designing a conceptual system engineering framework. 

# III. MBSE ABSTRACT METHOD

A primary MBSE abstract method sets the foundation concepts allowing the assessment of the traditional MBSE approach. The idea is to be generic enough to be tool agnostic. 

The MBSE approach aims to build a single source of truth for all stakeholders during the whole system lifecycle. The abstract method comprises four interconnected components: data model, processes, roles, and tools, as illustrated in Fig. 1. 

The data model captures all the concepts that are needed to achieve the final goal. We can also call it domain knowledge mapping. The subject matter experts usually construct it. It could be designated as a knowledge database, for example. This database contains all concepts and relationships necessary to perform all systems engineering activities. The data model refers to this collection of ideas 

with no link to any specific tool and without any particular implementation definition. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-03-22/28b9bb51-d193-4cca-a176-c299a0a6cea2/c911d9bc63301373a563989de751830debb139dbe575084b34b78981d62252ca.jpg)



Fig. 1. Abstract Systems Engineering method


The processes are a collection of activities that are performed to manipulate a given data model. Those activities could be decomposed into smaller steps to encapsulate and avoid complexity. These processes must also include describing how the data model is populated, updated, and deleted. 

The roles define the accountability assigned to the actors responsible for executing the processes and changing the data model. In other words, the action of modifying a specific set of data using a defined process requires an identified responsibility. For this reason, we assign strict permissions to particular roles. These roles can be allocated to any actor, including people or a piece of a software agent. 

The tools are used to reduce, automate or eliminate activities during the product lifecycle. The tools are designed to prevent human errors, enforce standardization initiatives to achieve better quality and cost reduction. 

# IV. TOOL QUALIFICATION

The development and certification of safety-critical systems require the use of standards. In the case of software used in embedded systems in a safety-critical environment, the manufacturers need to comply with guidelines provided by DO-178C [8]. This standard defines design assurance levels where the number of objectives increases with the level of criticality. This standard provides guidelines for the development and verification of software. 

The DO-330 [9] guides software tool qualification. It should be employed in a joint effort with DO-178C. According to DO-178C, the criteria to check if a tool needs to be qualified is: 

- Criteria 1: A tool whose output is part of the resulting software and thus could insert an error 

- Criteria 2 - A tool that automates verification process(es) and thus could fail to detect an error, and whose output is used to justify the elimination or reduction of: 

a. Verification process(es) other than that automated by the tool, or 

b. Development process(es) that could have an impact on the airborne software 

- Criteria 3 - A tool that could fail to detect an error within the scope of its intended use. 

The choice of the TQL is closely related to the intended use of the tool. If the generated output is embedded into the flying software, then the qualification level depends on the embedded software design assurance level (DAL). On the other hand, if the tool is used to replace or assist systems engineers during formal verification or development processes, then the qualification level can be TQL4 or TQL5, according to the software DAL. If the tool could lead to unidentified mistakes, then it is automatically classified as TQL5. TABLE I. defines the TQL according to software DAL and tool criteria. 

If the software tool matches any of the criteria above, it shall be qualified according to guidelines provided by DO-330. The tool qualification level is derived from TABLE I. According to the software's design assurance level and the criteria asserted by the tool to be developed, the qualification level is defined. 

TABLE II. shows the number of objectives for each tool qualification level. The number of objectives is a monotone measure of the total lifecycle cost of a tool in the function of the TQL level. From this observation emerges the need for a platform capable of running applications with different TQL levels. 


TABLE I. TOOL QUALIFICATION LEVEL DETERMINATION


<table><tr><td rowspan="2">Software Level</td><td colspan="3">Criteria</td></tr><tr><td>1</td><td>2</td><td>3</td></tr><tr><td>A</td><td>TQL 1</td><td rowspan="2">TQL 4</td><td rowspan="4">TQL 5</td></tr><tr><td>B</td><td>TQL 2</td></tr><tr><td>C</td><td>TQL 3</td><td rowspan="2">TQL 5</td></tr><tr><td>D</td><td>TQL 4</td></tr></table>


TABLE II. OBJECTIVES OF DO-330


<table><tr><td>TQL</td><td>Number of Objectives</td><td>Number of Objectives with Independence</td></tr><tr><td>1</td><td>76</td><td>35</td></tr><tr><td>2</td><td>74</td><td>22</td></tr><tr><td>3</td><td>70</td><td>5</td></tr><tr><td>4</td><td>38</td><td>2</td></tr><tr><td>5</td><td>15</td><td>2</td></tr></table>

The tool qualification process is deeply interconnected to the software lifecycle processes. As we can see in Fig. 2 and TABLE I. Based on the input from DO-178C, the need for a tool qualification is defined. When the tool meets all the processes requirements, it can be delivered and used by any software developed under DO-178C. 

# V. ARTIFICIAL INTELLIGENCE CAPABILITIES

This section presents a review of selected artificial intelligence capabilities and their potential applications to systems engineering. This list is not intended to be exhaustive. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-03-22/28b9bb51-d193-4cca-a176-c299a0a6cea2/916ff144386747e416c9fc65574021c230334d54a48f8110e3a2421c0827782c.jpg)



Fig. 2. The interface between DO-178C and DO-330


# A. Speech synthesis

Speech synthesis performs the reverse operation of speech recognition. It transforms computer text into spoken language. This capability is used in call centers, people with disabilities. The techniques used to implement speech synthesis also use artificial intelligence [4][5]. 

# B. Speech recognition

Speech recognition is a set of techniques that converts the spoken language into computer text. There are several algorithms used to perform this task. The most commons are Hidden Markov Chains and Neural Networks [2][3]. Several applications use speech recognition, such as Home assistants, telephony, in-car systems. 

# C. Automatic Summarization

Artificial intelligence techniques have also been used to create a summary from an original set of artifacts. The initial collection can contain video, sound, text, and any other data source. This capability can be employed to summarize a soccer game, a legal proceeding, or a book[6]. 

# D. Statistical Classification

Classification is the capability of categorizing data into different groups. It is also known as clustering, where the input data is divided into classes. This capability can be included in a more generic domain called Pattern Recognition. These techniques are applied in computer vision applications such as video tracking and hand-writing recognition [10] [14]. 

# E. Recommendation systems

Online retailers extensively employ recommendation systems. These algorithms can predict the best combination of products to be offered to the clients based on user behavior. These algorithms are also used to generate multimedia playlists and content on social media [11]. 

# F. Virtual Assistants

A virtual assistant is software that can perform tasks based on commands or questions. They are implemented using a chatbot capable of textual interaction. Another category is the home assistant devices that are controlled by voice. Online customer service companies employ the chatbot version. The home assistant device is designed to be installed at home, and it is becoming very popular with several manufacturers competing in this market [12]. 

# G. Virtual Reality

The use of artificial intelligence vastly improves virtual reality. It can be used to perform social simulations, emulate people's behavior, and create a virtual environment for gaming experiences. This capability is primarily used by the video game industry, education, and training. 

# H. Building domain ontology

The domain ontology contains a structured map of concepts of a discipline. There several algorithms capable of mining concepts and creating an integrated ontology. This knowledge graph provides reasoning capabilities and establishes a chart used to infer relationships between data. A search engine uses this to improve its results [13]. 

# VI. MBSE PLATFORM OPERATIONAL NEEDS

In this section, we list the primary operational needs for an integrated MBSE platform. 

# A. Support to multiple TQL applications running in the same platform

In the road to implement the single source of truth, the platform shall process data with different qualification levels. In the MBSE approach, it is expected to manipulate data from various sources. Some of them will be dealing with the generation of software code that will be onboard and requires a TQL1, for example. On the other hand, many other applications manage less critical information and will be 

qualified as TQL5. To build an integrated model, the platform must be able to run applications with different TQL. 

In TABLE II, we have several objectives in the function of the TQL level. We can assume that an application's total life cost should be a monotone function of the number of qualification objectives. This assumption drives the need for selecting the appropriate qualification level that ensures the safety and low cost simultaneously. The most straightforward solution also leads to a design capable of running multiple TQL applications concurrently. 

# B. Support qualified modular applications

Different applications need to be updated during the system lifecycle, or new capabilities need to be added to the current platform. This could be due to new regulations or to a new, improved methodology. For every modification in the platform, we have to ensure that it is fully qualified. To reduce the cost and time needed for the entire platform qualification, we can employ a modular approach where each application has its lifecycle. This strategy would drastically reduce the time and cost of the platform as the whole qualification. We also expect agility in finding and fixing bugs even for the large-scale platform. 

# C. Support to an interconnected federation of models

A single model approach is not scalable for use in real-world applications. It is more realistic to allow multiple models that are aggregated into an interconnected federation of models. To ensure a single source of truth, the platform must allow traceability between models. 

# D. Support to heterogeneous vocabularies

Experts from different domains use different modeling languages to formalize their knowledge about the system. The support to multiple vocabularies and languages is a stringent need for large-scale applications. 

# E. Support to processes via interoperability standards

The data manipulation process needs to be standardized and machine-readable. This ensures that different actors follow the same approach across the whole organization. The methods must define a maturity scale of the data manipulated, guaranteeing the appropriate actor role. 

# VII. DESIGN STRATEGIES

This section presents some design strategies that leverage commercial technologies to reduce the cost and impact on tool qualification effort. These design strategies aim to guide a conceptual platform design allowing artificial intelligence applications to be used by systems engineering methodologies. These design strategies are chosen to drive a conceptual architecture capable of fulfilling the operational needs discussed in section VI. 

# A. Moving towards cloud applications

Running tools in the cloud solves some of the problems encountered by traditional software tools. Installing software into personal PCs requires rigorous control of the environment version and its dependencies. In the cloud, the environment configuration control is centralized, and it is ensured that all users access the same environment. Another advantage is related to scalability. In traditional systems, when the number of users increases rapidly, users usually 

experience slow tools. When the demand suddenly rises in a cloud environment, the cloud can allocate more clusters to cope with this surge peak in usage. 

It is possible to adjust the number of instances in the workload's function using containerized cloud applications. Let's suppose that we have a surge in the number of users performing the same operation in the platform in a given moment. As an example, this could be the code generation action using a TQI.1 application. When the platform detects a surge in the workload, it can deploy more instances of the same application to increase demand. App2 illustrates this in Fig. 3. This would prevent the users from experiencing slow platform performance and thus lead to more productivity. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-03-22/28b9bb51-d193-4cca-a176-c299a0a6cea2/73803cfa7f9c75a604a10a17c8a6e62d7b5129bb7680c96268978d254a2822d8.jpg)



Fig. 3. Heterogeneous applications running in the cloud


# B. Running microservices

Microservices is a collection of loosely coupled services. Each microservice is responsible for a small and specific task inside the platform. This technique employs modular applications to reduce complexity and reduce the cost of changes and improvements. This way, it makes it easier to deploy new patches and functionalities 

Using microservices also enables scalability in periods of significant traffic by deploying several instances of the same application. Another important aspect is the possibility to execute tools with different qualification levels in the platform. 

It is also essential to notice that each microservice runs in an independent environment having its own memory space and operational system. This observation makes it possible to execute applications with different TQL on the same platform. In Fig. 3, we have App1 qualified as TQL5 and App2 qualified as TQL1. 

This strategy will have a massive impact on tool qualification effort. Using containerized microservices, we can create a modular qualification plan where each application has its independent life cycle. In this way, new functionality can be added or updated without impacting the other microservices. This strategy ensures that the tool qualification process is performed at the microservice level. 

# C. Building a multi-level knowledge graph

Algorithms that perform knowledge curation can be automatic, semi-automatic, or manual. In a large-scale platform, all three algorithms must be used. Non-qualified applications can employ an automatic data model. The semi-automatic algorithms can be employed for TQL5. And the manual selection could be utilized for TQL1 to TQL4. 

# D. Improve the platform using behavior data

In current web platform tools, all user data is analyzed to improve the existing software. In this sense, the user's behavior is employed to find new opportunities to fix and improve the tool itself. 

This concept is closely related to the training technique employed by the majority of artificial intelligence algorithms. A user interface, for example, could be optimized based on the most frequent actions performed by the users. 

# VIII. CONCEPTUAL ARCHITECTURE

This section will present an architecture concept proposal. Taking the design strategies as guiding principles, we propose a conceptual platform. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-03-22/28b9bb51-d193-4cca-a176-c299a0a6cea2/2a58035e327a0ae65975aa0670bd00f95850799724efe010e38b70e41c98b0fa.jpg)



Fig. 4. Conceptual Architecture - High-level view


In Fig. 4, we present a high-level layered representation. On the bottom, we represent all data sources that will interact with the platform. We include the data source, the users, 

computers, manufacturing machines, products in operation, public data on the Internet. 

The first layer, the data translation layer (DTL), is responsible for acquiring and translating the data from a large variety of sources. As an example, the source could be a video recorder or a microphone. The DTL would acquire the data from the equipment and translate it into a semi-structured format. 

The data is then made available for the applications running on the computer support application (CSA) layer. This layer is responsible for getting the translated data and processing them according to a specific domain's rules. The capabilities identified in section V are implemented in this layer, as illustrated by Fig. 5. For example, the CSA could run a speech recognition in an audio signal and store the identified text. This layer can also execute machine vision algorithms to identify specific objects in a recorded video. 

The third layer is called the methodology process application (MPA) layer. This layer implements all routines related to the defined organizational process framework. It includes applications to perform all everyday tasks used by the systems engineers. In Fig. 5, we have an example of possible services to be executed by the MPA. 

The systems engineering application (SEA) layer is responsible for implementing all SE Handbook processes [19]. For example, we have requirements, safety, traceability applications defined in Fig. 5. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-03-22/28b9bb51-d193-4cca-a176-c299a0a6cea2/b72a953a8a8db17a517ffbcd1ef0c48c23b9c9baa4a011b68e7db38a46cfd295.jpg)



Fig. 5. Conceptual Architecture


On the top layer, we have the enterprise excellence application (EEΛ) layer. This level is concerned with overall business performance such as sales, program management, supply chain, as exemplified in Fig. 5. 

The vertical layer is called the multi-level data model (MDM). It is the backbone of all applications providing a map for reasoning and rules for model creation and validation. The MDM is responsible for delivering the 

common data-model for all applications. It is also responsible for collecting the necessary data to update itself. 

# IX. CONCLUSION

In this paper, we have investigated the current artificial intelligence capabilities. They are pervasive in an extensive range of applications. Artificial intelligence capabilities can radically improve the systems engineering landscape. We have also investigated the tool qualification requirements and guidelines using the DO-178C and DO-330 as references. These guidelines provide clear guidance for tool qualification. 

In this paper, we also derived operational needs for a large-scale platform. We discussed in detail the need for running applications with different TQL concurrently. We also discussed the need to support applications with an independent lifecycle for ensuring agility and low platform qualification cost. Last, we have created a modular design capable of unleashing the strength of artificial intelligence applications. 

For future work, we want to explore other tool operational needs related to the different conceptual layers. We also want to capture use cases and scenarios for the platform. These scenarios can be an effective way to evaluate the proposed design. 

# ACKNOWLEDGMENT

Brazilian National Research Council (CNPq) funded the research that led to this article under grant 204962/2014-5. 

# REFERENCES



[1] L. Batista and O. Hammami, "Capella based system engineering modeling and multi-objective optimization of avionics systems," 2016 IEEE International Symposium on Systems Engineering (ISSE), Edinburgh, 2016, pp. 1-8, DOI: 10.1109/SysEng.2016.7753127. 





[2] L. R. Rabiner, "A tutorial on hidden Markov models and selected applications in speech recognition," in Proceedings of the IEEE, vol. 77, no. 2, pp. 257-286, Feb. 1989, DOI: 10.1109/5.18626. 





[3] G. Hinton et al., "Deep Neural Networks for Acoustic Modeling in Speech Recognition: The Shared Views of Four Research Groups," in IEEE Signal Processing Magazine, vol. 29, no. 6, pp. 82-97, Nov. 2012, DOI: 10.1109/MSP.2012.2205597. 





[4] K. Tokuda, T. Yoshimura, T. Masuko, T. Kobayashi and T. Kitamura, "Speech parameter generation algorithms for HMM-based speech synthesis," 2000 IEEE International Conference on Acoustics, Speech, and Signal Processing. Proceedings (Cat. No.00CH37100), Istanbul, Turkey, 2000, pp. 1315-1318 vol.3, DOI: 10.1109/ICASSP.2000.861820. 





[5] F. Seide, G. Li, X. Chen and D. Yu, "Feature engineering in Context-Dependent Deep Neural Networks for conversational speech 





transcription," 2011 IEEE Workshop on Automatic Speech Recognition & Understanding, Waikoloa, HI, 2011, pp. 24-29, DOI: 10.1109/ASRU.2011.6163899. 





[6] A. Ekin, A. M. Tekalp and R. Mehrotra, "Automatic soccer video analysis and summarization," in IEEE Transactions on Image Processing, vol. 12, no. 7, pp. 796-807, July 2003, DOI: 10.1109/TIP.2003.812758. 





[7] J. Marques and A. Marques da Cunha, "COTS tool qualification using RTCA DO-330: Common pitfalls," 2017 IEEE/AIAA 36th Digital Avionics Systems Conference (DASC), St. Petersburg, FL, 2017, pp. 1-6, DOI: 10.1109/DASC.2017.8102031. 





[8] RTCA, DO-178C Software Considerations in Airborne Systems and Equipment Certification, Radio Technical Commission for Aeronautics, 2011. 





[9] RTCA, DO-330 Software Tool Qualification Consideration, 2011. 





[10] K. He, X. Zhang, S. Ren, and J. Sun, "Deep Residual Learning for Image Recognition," 2016 IEEE Conference on Computer Vision and Pattern Recognition (CVPR), Las Vegas, NV, 2016, pp. 770-778, DOI: 10.1109/CVPR.2016.90. 





[11] Y. Koren, R. Bell and C. Volinsky, "Matrix Factorization Techniques for Recommender Systems," in Computer, vol. 42, no. 8, pp. 30-37, Aug. 2009, DOI: 10.1109/MC.2009.263. 





[12] B. R. Ranoliya, N. Raghuwanshi, and S. Singh, "Chatbot for university-related FAQs," 2017 International Conference on Advances in Computing, Communications and Informatics (ICACCI), Udupi, 2017, pp. 1525-1530, DOI: 10.1109/ICACCI.2017.8126057. 





[13] J. N. K. Liu, Y. He, E. H. Y. Lim and X. Wang, "A New Method for Knowledge and Information Management Domain Ontology Graph Model," in IEEE Transactions on Systems, Man, and Cybernetics: Systems, vol. 43, no. 1, pp. 115-127, Jan. 2013, DOI: 10.1109/TSMCA.2012.2196431. 





[14] S. Mitra and T. Acharya, "Gesture Recognition: A Survey," in IEEE Transactions on Systems, Man, and Cybernetics, Part C (Applications and Reviews), vol. 37, no. 3, pp. 311-324, May 2007, DOI: 10.1109/TSMCC.2007.893280. 





[15] A. Borgh, "Guidelines for Development of Operational Requirements for Model Checking Tools," 2019 Integrated Communications, Navigation, Surveillance Conference (ICNS), Herndon, VA, USA, 2019, pp. 1-10, DOI: 10.1109/ICNSURV.2019.8735266. 





[16] B. Monsuez and M. Nakhle, "Applying SafeComp, a Formal Integrated System Modeling Framework, to the Design of a Steam Generator Controller," 2019 4th International Conference on System Reliability and Safety (ICSRS), Rome, Italy, 2019, pp. 554-560, DOI: 10.1109/ICSRS48664.2019.8987732. 





[17] BPM+ Health and the OMG Healthcare Domain Task Force, 2020. FIELD GUIDE TO SHAREABLE CLINICAL PATHWAYS VERSION 2.0. [online] Available at: <https://www.bpm-plus.org/healthcare-and-bpmn.htm> [Accessed 14 June 2020]. 





[18] HL7 - Health Level Seven International, 2020. FHIR - Fast Healthcare Interoperability Resources. [online] Available at: <http://hl7.org/fhir/> [Accessed 14 June 2020]. 





[19] INCOSE Systems Engineering Handbook (SE Handbook). [Online]. Available: https://www.incoe.org/products-and-publications/sehandbook. [Accessed: 23-Jul-2020]. 

