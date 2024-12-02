# Project (30%)

**Submission deadline: December 16, 2024 EOD**

**Objective:**  
This project challenges you to explore the practical application of a human-centred ML (HCML) technique. With your group you will choose a research topic related to HCML and design an experiment to evaluate the effectiveness of a chosen technique on a dataset. The focus will be on analysing the technique's performance and limitations from a human-centred perspective, considering its potential impact on the users of your proposed system.

The grade of the project will be based on a presentation and oral evaluation.

**Project Setup:**

1. **Research Topic Selection:**

Choose a research topic related to HCML, aim to align the chosen technique with the problem being solved. For example:

- **Active Learning:** Can be used to identify the most informative data points for human annotation, useful for tasks that rely on experts.  
- **Learning from Crowdsourcing:** Useful for gathering and incorporating noisy labels from human annotators in cases of disagreement or challenging labeling tasks.
- **Reinforcement Learning from Human Feedback (RLHF):** Fine-tuning or training a model through human-provided feedback when a certain alignment is desired. 
- **Machine Teaching**: An existing ML pipeline can be evaluated or improved through Machine Teaching by data filtering or data augmentation, when understanding the data can help you achieve that bit of extra performance.
- **Interactive Learning**: In a zero-shot classification scenario the user may be able to identify the correct class based on a few instances.

2. **Experimental Design:**

Select a specific technique within your chosen research topic. Design an experiment to evaluate the chosen technique on a dataset and compare the performance of your chosen technique against a reasonable baseline (e.g., majority voting for crowdsourcing, random acquisition for active learning).

The aim of the assignment is not to literally reproduce an existing paper. The chosen technique should not have been applied to that dataset yet (you don't have to exhaustively check all literature for this, but it should not be a typical approach for this dataset). You can choose an existing paper and use their approach as the baseline and compare it to a human-centred technique. Potential other experiments are:

- Compare models for modeling noisy labelers—pooling (e.g., Dawid-Skene vs Pooled concensus, or (weighted) Majority voting)
- For active learning, one could examine how two or more acquisition functions behave under certain noise patterns or in a (greedy) batch setting. 
- See where the performance of behavior cloning breaks down as the state space grows in size. 
- Compare the performance of reinforcement learning from human feedback (RLHF) using an increasing number of ranked data points (e.g. pairs vs triplets vs quadruplets, etc). 
- Experiment with RLHF under noisy rankings and/or implement a model of the noisy labelers. 
- Experiment with a semi-supervised version of active learning, RLHR, behavior cloning, etc.

3. **Human-Centred Analysis:**

Analyse the results of your experiment, considering the human-centred aspects of the chosen technique in relation to the problem underlying the dataset. This could involve:

- **Impact of human effort:** Evaluate the efficiency of the technique in terms of human labelling or feedback requirements, considering annotator burden or adaptability to experts.  
- **Fairness and bias:** Consider potential biases in the data or the technique's impact on different user groups, ensuring equitable access to applications.  
- **Interpretability:** Analyse how well the technique's results can be explained to non-technical stakeholders involved in the HCML application.

Discuss the potential social impact of your chosen HCML technique within the context of your dataset and task. Consider how it could improve existing or contribute to new solutions, and how it benefits the human users.

4. **Deliverables:**  
   - Presentation slide deck with 5 slides:  
     - Title slide (with names of group members and project title); you can add a teaser figure or project summary here.  
     - Slide on the chosen dataset and its relevance; what are the user needs?  
     - Slide on the experimental design, baseline comparison, and the steps taken to make the experiment human-centred.  
     - Slide with the experimental results including comparison to baseline.
     - Summary of the findings, with a focus on human-centred aspects (efficiency, fairness, interpretability) and potential social impact.  
     - **The slidedeck should be submitted on Canvas December 16, EOD**.  
   - Oral evaluation (on December 18):  
     - In a 20 minute session you will briefly (7-10 minutes) pitch your project, using the slide deck.  
     - A Q\&A will follow your pitch focused on probing your understanding of the project and the individual contributions.

**Requirements**:

- Presentation should be submitted as a single PDF (16:9 aspect ratio).  
- Maximum 5 slides.  
- Oral presentation maximum 10 minutes.

**Grading Rubric:**

- Slides clarity (10%)  
- Pitch clarity (10%)  
- Experimental Setup and Execution (40%)  
- Accuracy and clarity during Q\&A (40%)

