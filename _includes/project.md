# Project (40%)

**Submission deadline: December 12, 2025 EOD**

**Objective:**  
This project challenges you to explore the practical application of human-centred ML (HCML) techniques. With your group you will choose a research topic related to HCML and design an experiment to evaluate the effectiveness of a chosen technique on a dataset. The focus will be on analysing the technique's performance and limitations from a human-centred perspective, considering its potential impact from an AI, ethical, and social-good perspective.

The grade of the project will be based on a presentation and oral evaluation.

## Project Setup:

### 1. **Research Topic Selection:**

Choose a research topic related to HCML, aim to align the chosen technique with the problem being solved. For example:

- **Learning from Crowdsourcing:** Useful for gathering and incorporating noisy labels from human annotators in cases of disagreement or challenging labeling tasks.
- **Reinforcement Learning from Human Feedback (RLHF):** Fine-tuning or training a model through human-provided feedback when a certain alignment is desired. 
- **Machine Teaching**: An existing ML pipeline can be evaluated or improved through Machine Teaching by data filtering or data augmentation, when understanding the data can help you achieve that bit of extra performance.
- **Active Learning:** Can be used to identify the most informative data points for human annotation, useful for tasks that rely on experts.  
- **Interactive Learning**: In a zero-shot classification scenario the user may be able to identify the correct class based on a few instances.

### 2. **Human Evaluation Design**

To really consider the human aspects, you are tasked with designing the user study first. As such, you will design a user study for evaluating a chosen ML application from a human-centred perspective. This will involve defining user personas, selecting appropriate evaluation methods, and considering factors like user needs, usability, and potential biases.

To design a user study you need to think about both **how** and **why** a user would want to use the system. This concerns their motivation and end-goal for using the system, but also very practically how they would expect to interface with the system. For example, if your user persona describes an non-technical person, then they cannot be expected to submit compute jobs to a cluster and then parse terminal output. For further information on scenarios see [here](https://ocw.tudelft.nl/wp-content/uploads/2_RossonCarrollSBDforHandbook2002.pdf).

As part of the human evaluation design you should:

- **Define User Personas:** Develop two user personas that represent the target users of the ML system. Each persona should include details such as:  
     
   - Demographics (age, gender, location)  
   - Technical skills and experience with technology  
   - Goals and motivations for using the ML application (as scenarios)  
   - Potential challenges or concerns they might have with the system

  These two personas do not have to cover all possible users of the system, however, at least one of them should be a more typical user based on your expectations.

- **Propose Evaluation Design:** Propose a user study design that incorporates relevant evaluation methods to assess the human-centred aspects of the ML system. Consider including at least two methods from the following:  
     
   - **Surveys:** Design a survey to gather user feedback on their experience with the ML application. This could cover aspects like ease of use, satisfaction with results, and trust in the system's outputs.  
   - **Task Completion Rates:** Outline a set of tasks that users would need to complete using the ML application. Measure the time taken and success rate for these tasks to assess usability and efficiency.  
   - **User Interviews:** Plan a series of semi-structured interviews with users to gain in-depth qualitative insights. Focus on understanding user needs, expectations, and any challenges they encounter while interacting with the ML system.  
   - **A/B Testing**: Design a setup in which you have two versions of the application which are meaningfully different in some dimension (related to human-centred perspective). Describe the versions and what measures you will use.

You do not have to actually implement the human evaluation, but try to design it as if you would.

### 3. **Experimental Design:**

Select a specific technique within your chosen research topic. Design an experiment to evaluate the chosen technique on a dataset and compare the performance of your chosen technique against a reasonable baseline (e.g., majority voting for crowdsourcing, random acquisition for active learning).

The aim of the assignment is not to literally reproduce an existing paper. The chosen technique should not have been applied to that dataset yet (you don't have to exhaustively check all literature for this, but it should not be a typical approach for this dataset). You can choose an existing paper and use their approach as the baseline and compare it to a human-centred technique. Potential other experiments are (non-exhaustive list):

- Compare models for modeling noisy labelers—pooling (e.g., Dawid-Skene vs Pooled concensus, or (weighted) Majority voting)
- For active learning, one could examine how two or more acquisition functions behave under certain noise patterns or in a (greedy) batch setting. 
- See where the performance of behavior cloning breaks down as the state space grows in size. 
- Compare the performance of reinforcement learning from human feedback (RLHF) using an increasing number of ranked data points (e.g. pairs vs triplets vs quadruplets, etc). 
- Experiment with RLHF under noisy rankings and/or implement a model of the noisy labelers. 
- Experiment with a semi-supervised version of active learning, RLHF, behavior cloning, etc.

### 4. **Human-Centred Analysis:**

Analyse the results of your experiment, considering the human-centred aspects of the chosen technique in relation to the problem underlying the dataset. This could involve:

- **Impact of human effort:** Evaluate the efficiency of the technique in terms of human labelling or feedback requirements, considering annotator burden or adaptability to experts.  
- **Fairness and bias:** Consider potential biases in the data or the technique's impact on different user groups, ensuring equitable access to applications.  
- **Interpretability:** Analyse how well the technique's results can be explained to non-technical stakeholders involved in the HCML application.

Discuss the potential social impact of your chosen HCML technique within the context of your dataset and task. Consider how it could improve existing or contribute to new solutions, and how it benefits the human users.

### 5. **Deliverables:**  
   - Presentation slide deck with at least the following 7 slides:  
     - Title slide (with names of group members and project title); you can add a teaser figure or project summary here.  
     - Slide on the chosen dataset and its relevance; what are the user needs?  
     - Slide on the human evaluation scenario; what is the scenario and what are the user personas?
     - Slide on the human evaluation design itself; how would you evaluate the system in a user study?
     - Slide on the experimental design, baseline comparison, and the steps taken to make the experiment human-centred.  
     - Slide with the experimental results including comparison to baseline.
     - Summary of the findings, with a focus on human-centred aspects (efficiency, fairness, interpretability) and potential social impact.  
     - **The slidedeck should be submitted on Canvas December 12, EOD**.  
   - Oral evaluation (on December 16):  
     - In a 20 minute session you will briefly (7-10 minutes) pitch your project, using the slide deck.  
     - A Q\&A will follow your pitch focused on probing your understanding of the project and the individual contributions.

**Requirements**:

- Presentation should be submitted as a single PDF (16:9 aspect ratio).  
- Maximum 10 slides.  
- Oral presentation maximum 10 minutes.

**Grading Rubric:**

- Slides clarity (10%)  
- Pitch clarity (10%)  
- Experimental Setup and Execution (40%)  
- Accuracy and clarity during Q\&A (40%)