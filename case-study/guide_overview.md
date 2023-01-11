# Overview: Responsible Design and Implementation of AI
The following points are from the [The Alan Turing Institute's guide for responsible design and implementation of AI systems](https://www.turing.ac.uk/sites/default/files/2019-06/understanding_artificial_intelligence_ethics_and_safety.pdf).   

AI ethics is a set of values, principles, and techniques that employ widely accepted standards of right and wrong to guide moral conduct in the development and use of AI technologies.   

The field of AI ethics has largely emerged as a response to the range of individual and societal harms that the misuse, abuse, poor design, or negative unintended consequences of AI systems may cause. The potential harms of AI include:  
- Reproducing and amplifying patterns of marginalization and discrimination that exist in society  
- Complicating the designation of responsibility in algorithmically generated outcomes, potentially harming the autonomy and violating the rights of affected individuals  
- Producing non-transparent, unexplainable, or unjustifiable results in some cases  
- Posing threats to privacy in both design and development processes and deployment  
- Reducing the need for human-to-human interaction, leading to isolation and disintegration of social connections  
- Being used to manipulate or deceive people  
- Creating negative unintended consequences, such as environmental harm or job displacement  
- Being used to perpetrate or enable harm, such as through cyber attacks or misuse of autonomous weapons  

When implementing an ethical AI governance architecture, we must ensure that AI projects are:  
- Ethically permissible by considering the impacts they may have on the wellbeing of affected stakeholders and communities
- Fair and non-discriminatory by accounting for their potential to have discriminatory effects on individuals and social groups, by mitigating biases that may influence their outputs, and by being aware of the issues surrounding fairness that come into play at every phase of the design and implementation process
- Worthy of public trust by guaranteeing to the extent possible the safety, accuracy, reliability, security, and robustness of their products
- Justifiable by prioritizing both the transparency of the process by which they are designed and implemented, and the transparency and interpretability of their decisions and behaviours  

We call this governance architecture an **ethical platform**. It will take three building blocks to make such an ethical platform possible:  
1. **Reflect using the SUM Values** (Respect, Connect, Care, Protect) to provide a framework for ethical values and evaluate the ethical permissibility of the project
2. **Act using the FAST Track Principles** (Fairness, Accountability, Sustainability, Transparency) to ensure the project is bias-mitigating, non-discriminatory, responsible, trustworthy and fair
3. **Justify using the PBG Framework** (Pocess-Based Governance) to operationalize the SUM Values and FAST Track Principles, ensuring end-to-end transparency and accountability
All building blocks should be considered through human-centred implementation protocols and practices.

All definitions will be described within the context of the following AI project lifecycle:  
**Problem Formulation > Data Extraction and Acquisition > Data Preprocessing > Modelling, Testing and Validation > Deploy, Monitor and Reassess**   

### Reflect: SUM Values
These values should orient you in deliberating about the ethical permissibility of a prospective AI project. They should also provide you with a framework of concepts to consider
the ethical impacts of an AI system across the design, use, and monitoring lifecycle.
- **Respect** the dignity of individual persons by safeguarding their autonomy, their power to express themselves, and their right to be heard, and supporting their abilities to flourish and fully develop themselves  
- **Connect** with each other sincerely, openly, and inclusively, prioritising diversity, participation, and inclusion in the design, development, and deployment processes of AI innovation
- **Care** for the wellbeing of all stakeholders by designing and deploying AI systems to foster and cultivate their welfare, minimising the risks of misuse or abuse, and prioritising safety
- **Protect** the priorities of social values, justice, and social equity by prioritising social welfare, public interest, utilitarianism and the consideration wider impact  

### Act: FAST Track Principles
#### Fairness
Consider the principle of **discriminatory non-harm** as a minimum required threshold of fairness, ensuring that AI systems:
1. Are trained and tested on properly representative, relevant, accurate, and
generalisable datasets (Data Fairness)
2. Have model architectures that do not include target variables, features,
processes, or analytical structures
which are unreasonable, morally objectionable, or unjustifiable (Design
Fairness)
3. Do not have discriminatory or inequitable impacts on the lives of the people
they affect (Outcome Fairness)
4. Are deployed by users sufficiently trained to implement them responsibly and
without bias (Implementation Fairness)  

Self Assessment:
1. Identify the fairness and bias mitigation dimensions that apply to the specific
stage under consideration
2. Scrutinise how your particular AI project might pose risks or have unintended
vulnerabilities in each of these areas
3. Correct any existing problems that have been identified,
strengthen areas of weakness that have possible discriminatory consequences, and take
proactive bias-prevention measures   

#### Accountability
Data processing that is aligned with [Principle 6 of the GOV.UK Data Ethics Framework](https://www.gov.uk/government/publications/data-ethics-framework/data-ethics-framework-2020) and following an **accountability-by-design** approach:   
AI systems must be designed to facilitate end-to-end: **answerability** (who is accountable, with clear justification) and **auditability** (how the designers and implementers of AI systems are to be held accountable).   
This requires both **responsible humans-in-the-loop** across the entire design and implementation chain as well as **activity monitoring protocols** that enable end-to-end oversight and review.     
Involving both:
- **Anticipatory Accountability**: defined prior to implementation, bolstering soundness of design/implementation processes and thereby more effectively pre-empting possible harms
- **Remedial Accountability**: including comprehensive auditability regimes, transparent design/use practices, decision rationale, explicability of model results, and explanation of the ethical permissibility  

#### Sustainability
Conduct a **Stakeholder Impact Assessment** (SIA) which should be considered at Problem Formulation (initial assessment), Pre-Implementation (review and public consultation) and Reassessment (reflect and rectify). It should cover the following questions:
1. Identifying Affected Stakeholders
    - Who are the stakeholders that this AI project is most likely to affect? 
    - What groups of these stakeholders are most vulnerable? How might the project negatively impact them?
2. Goal-Setting and Objective-Mapping
    - How are you defining the outcome (the target variable) that the system is optimising for? Is this a fair, reasonable, and widely acceptable definition? 
    - Does the target variable (or its measurable proxy) reflect a reasonable and justifiable translation of the project’s objective into the statistical frame? 
    - Is this translation justifiable given the general purpose of the project and the potential impacts that the outcomes of its implementation will have on the communities involved? 
3. Possible Impacts on the Individual
    - How might the implementation of your AI system impact the abilities of affected stakeholders to make free, independent, and well-informed decisions about their lives? How might it enhance or diminish their autonomy?
    - How might it affect their capacities to flourish and to fully develop themselves?
    - How might it do harm to their physical or mental integrity? Have risks to individual health and safety been adequately considered and addressed?
    - How might it infringe on their privacy rights, both on the data processing end of designing the system and on the implementation end of deploying it 
4. Possible Impacts on Society and Interpersonal Relationships 
    - How might the implementation of your AI system adversely affect each stakeholder’s fair and equal treatment under the law? Are there any aspects of the project that expose vulnerable communities to possible discriminatory harm?
    - Have the values of civic participation, inclusion, and diversity been adequately considered in articulating the purpose and setting the goals of the project? If not, how might these values be incorporated into your project design?
    - Does the project aim to advance the interests and well-being of as many affected individuals as possible? Might any disparate socioeconomic impacts result from its deployment?
    - Have you sufficiently considered the wider impacts of the system on future generations and on the planet as a whole?  

A technically sustainable AI system focuses on improving:
- **Accuracy and Performance Metrics**: confidence depends on problems inherent in modeling a chaotic and changing reality, including noise in data, missing features, and changes in input data over time
- **Reliability**: measure of consistency, ensuring that system behaves as intended and adheres to specifications
- **Security**: protection of system from unauthorized modification or damage, ensuring that it remains functional and accessible to authorized users and keeps confidential information secure
- **Robustness**: ability of system to function reliably and accurately under harsh conditions, including adversarial attacks, perturbations, and undesirable reinforcement learning behavior    

This requires careful forethought into how to construct a system that accurately and dependably operates in accordance with its designers’ expectations even when confronted with unexpected changes, anomalies, and perturbations. Building an AI system that meets these safety goals also requires rigorous testing, validation, and re-assessment as well as the integration of adequate mechanisms of oversight and control into its real-world operation.

Risks relating to accuracy and reliability:  
- **Concept Drift**: model accuracy and reliability can be compromised by changes in the underlying data distribution that the model was trained on
- **Brittleness**: machine learning systems may have difficulty processing unfamiliar events and scenarios and may make unexpected mistakes, especially in safety-critical applications

Risks relating to security and robustness: 
- **Adversarial Attacks**: maliciously modifying input data to induce incorrect predictions or misclassification, which can have serious consequences for safety-critical applications ([toolbox]( https://github.com/IBM/adversarialrobustness-toolbox))
- **Data Poisoning**: compromising data sources at collection and pre-processing stage to induce trained AI system into curated misclassification, systemic malfunction, and poor performance
- **Data Procurement**: obtaining data from potentially unreliable or questionable sources, such as the internet, social media, or the Internet of Things, or through third-party data curation processes  
- **Misdirected Reinforcement Learning Behavior**: risk that a reinforcement learning system will determine a reward-optimizing course of action that is harmful to people, because the system lacks context-awareness and common sense

Safety risks in an AI project depend on various factors such as the algorithm and machine learning techniques being used, the type of application in which they are being deployed, the provenance of the data, the objective specification, and the problem domain. It is best practice to consider safety at every stage of the AI project lifecycle, including testing, validating, verifying, and monitoring the safety of the system and performing AI safety self-assessments. These self-assessments should evaluate the team's design and implementation practices in relation to the safety objectives of accuracy, reliability, security, and robustness. They should be logged and subject to review and re-assessment.

#### Transparency
Involves the interpretability and justifiability of the processes and outcomes of an AI system, including the clarification and intelligibility of its decision-making and the demonstration of its ethical permissibility, fairness, and trustworthiness. The three critical tasks for designing and implementing transparent AI are:
1. **Process Transparency**: Demonstrate that ethical permissibility, non-discrimination/fairness, and safety/public trustworthiness were considered throughout the design and implementation of the AI system. This includes creation of the **PBG Framework**.
    - Maintaining strong regimes of professional and institutional transparency
    - Having a clear and accessible PBG Framework
    - Establishing a well-defined auditability trail in your PBG Framework through robust activity logging protocols that are consolidated digitally in a process log
2. **Outcome Transparency**: Provide a clear, understandable explanation of how and why the AI system made a specific decision or behaved in a certain way, taking into account societal factors and relationships. This includes:
    - Formal or logical explanations 
    - Explanations of the technical rationale
    - Clarification of the socially meaningful content from outcomes
    - Moral justification

Transparency also involves designing a sufficiently interpretable AI system:
1. Look first to context, potential impact, and domain-specific need when determining the interpretability requirements of your project  
2. Draw on standard interpretable techniques when possible  
3. When considering the use of ‘black box’ AI systems, you should:  
    - Thoroughly weigh up impacts and risks  
    - Consider the options available for supplemental interpretability tools that will ensure a level of semantic explanation which is both domain appropriate and consistent with the design and implementation of safe, fair, and ethical AI (internal, post-hoc explanation, counterfactual explanation and supplimental infrastructure)  
    - Formulate an interpretability action plan that includes a clear articulation of explanatory strategies, a succint formulation of an explanation delivery strategy, a detailed timeframe evaluation  
4.  Think about interpretability in terms of the capacities of human understanding   

### Human-centred Implementation Protocols and Practices
The demand for sensitivity to human factors should inform your approach to devising delivery and implementation processes from start to finish -  context will be critical in this. By understanding your use case well and by drawing upon solid domain knowledge, you will be better able to define roles and relationships. You will better be able to train the users and implementers of your system. And, you will be better able to establish an effectual implementation platform, to clarify content, and to facilitate understanding of outcomes for users and affected stakeholders alike. The steps are as follows:
1. Consider aspects of application type and domain context to define roles and determine user needs 
    - Assess which communities will be most affected by the AI system and prioritise the needs of the most disadvantaged when thinking about providing explanations
    - Define all the roles that will potentially be involved at the delivery stage of your AI project
2. Define delivery relations and map delivery processes
    - Assess the possible relationships between the defined roles that will have significant bearing on your project’s implementation
    - Build a map of the delivery process, accounting for the needs, roles, and relationships of relevant actors with the principle goal to translate statistically expressed results into humanly significant reasons and to translate algorithmic outputs into socially meaningful outcomes
3. Build an ethical implementation platform
    - Train ethical implementation so that implementers can:
        - Rationally evaluate and critically assess the logic and rationale behind the outputs of the AI systems
        - Convey and communicate their algorithmically assisted decisions to the individuals affected by them in plain language
        - Apply the conclusions reached by the AI model to a more focused consideration of the particular social circumstances and life context of the decision subject and other affected parties
        - Treat the inferences drawn from the results of the model’s computation as evidentiary contributions to a broader, more rounded, and coherent understanding of the individual situations of the decision subject and other affected parties
        - Weigh the interpretive understanding gained by integrating the model’s insights into this rounded picture of the life context of the decision subject against the greater purpose and societal objective of the algorithmically assisted assessment
        - ustify the ethical permissibility, the discriminatory non-harm, and the public trustworthiness both of the AI system’s outcome and of the processes behind its design and use 
    - Make your implementation platform a relevant part and capstone of the sustainability track of your project
    - Provide a model sheet to implementers and establish protocols for implementation reporting
    - Foster outcome understanding through dialogue
