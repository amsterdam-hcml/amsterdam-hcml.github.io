# Project

**Report submission deadline: December 10, 2026 EOD.**  
**Presentation submission deadline: December 14, EOD**.

**Objective:**  
This project challenges you to put human-centred ML (HCML) into practice. With your group you will choose a research topic related to HCML and design an experiment to evaluate the effectiveness of an intervention in that context. The project involves understanding the problem space, evaluating appropriate baselines, designing an intervention, and performing human evaluation whilst keeping in mind a human-centred perspective, considering potential impacts from an AI, ethical, and social-good perspective.

The grade of the project will be based on a written report, presentation, and an oral evaluation.

## Project Setup:

A key part of a human-centred approach concerns navigating and taking into account a wide variety of beliefs, priorities, and interests. To put this into practice, the entire class will be divided into two groups, each working on a project. To structure the work for a setup with such large groups, we define four teams per group, each consisting of 5-6 students:

1. Stakeholders  
   * In charge of setting the requirements, reviewing literature, and coordinating the writing.  
2. Auditors  
   * In charge of running the quantitative baselines and critically reflecting on the project approach and its impacts.  
3. Integrators  
   * In charge of implementing and evaluating human-centred algorithmic intervention.  
4. Evaluators  
   * In charge of designing, implementing, and performing the human evaluation.

During the first week of the course students will be, based on their input, assigned to a group and a team. Further details on what is expected from each team are provided below.

### 1\. **Stakeholders**

Each group is assigned a topic and dataset. As Stakeholders, you turn this into a concrete project: you decide what matters, to whom, and how the group will know whether it succeeded. You also keep the project coherent across the four teams.

* Stakeholder analysis: Identify who is involved in or affected by the ML system. This includes direct users, people about whom the system makes decisions, data subjects, domain experts, and the organisation deploying it. For each, consider their interests, how much influence they have, and where their interests conflict. Adopt their perspectives in how you make decisions throughout the project. Make sure the interests of the stakeholders are consistently represented.  
* Requirements: Translate stakeholders interests into a prioritised list of requirements. Include human-centred requirements such as fairness, transparency, privacy, and human effort, alongside task performance. Make requirements measurable where possible, so the other teams can test against them. When requirements conflict, document the trade-off you chose and who gains or loses from it.  
* Literature review: Review prior work on the task, existing baselines, relevant HCML techniques, and how similar systems have been evaluated with humans.  
* Coordination and writing: Set up the report structure, the timeline, and the hand-over moments between teams. Make sure the final report is consistent and that each requirement can be traced to where it was addressed and how it was evaluated.

**Team specific deliverables**: abstract, introduction, related work, and paper checklist sections of the report.

### 2\. **Auditors**

The auditors establish the quantitative reference point for the project and act as its internal critic. Their role is to question whether the system, and the project itself, actually serve the stakeholders.

**Baselines**. Together with the Stakeholders, select appropriate baselines: at least one simple baseline and two existing approaches from literature. Define the evaluation protocol (data splits, metrics, random seeds) and share it with the Integrators early, so that the intervention can be evaluated under exactly the same conditions. Report results with variance across runs.

**Audit**. Analyse the baselines and the human-centred intervention from a human-centred perspective in relation to the underlying problem. This could involve (but not limited to):

- **Impact of human effort:** Evaluate the efficiency of the technique in terms of human labelling or feedback requirements, considering annotator burden or adaptability to experts.  
- **Fairness and bias:** Consider potential biases in the data or the technique's impact on different user groups, ensuring equitable access to applications.  
- **Interpretability:** Analyse how well the technique's results can be explained to non-technical stakeholders involved in the HCML application.  
- **Data and documentation**: Examine how the data was collected and labelled, label quality, and what is missing or underrepresented. Document this, for example as a datasheet for the dataset and a model card for the baselines.

**Critical reflection**. Reflect on the project approach as a whole. Do the chosen metrics actually capture the Stakeholders’ requirements? Whose perspectives are missing? What assumptions does the problem framing make? How could the system fail or be misused?

Discuss the potential social impact of your chosen HCML technique within the context of your dataset and task. Consider how it could improve existing or contribute to new solutions, how it benefits the human users, and what harms it could cause.

**Team specific deliverables**: the data description, results (excluding the Integrators results), and discussion sections of the report.

### 3\. **Integrators**

Select a human-centred technique that aligns with your project’s ambitions and the Stakeholders’ requirements. Examples include active learning, interactive or human-in-the-loop learning, learning from human feedback or preferences, learning to defer to humans, and fairness-aware learning. Justify your choice based on the requirements and the literature.

Design an experiment to evaluate the chosen technique and compare its performance against the baseline(s):

* **Hypothesis**: Decide for yourselves what you expect the intervention to improve, and on which requirement.  
* **Fair comparison**: Use the Auditors’ evaluation protocol (same splits, metrics, and seeds), and report variance across runs.  
* **Beyond accuracy**: Compare on the human-centred dimensions the intervention targets, such as the number of labels needed, the quality of explanations, or performance on subgroups.  
* **Simulated humans**: Where the technique needs human input that is not available at scale, simulate it (for example, an oracle based on ground-truth labels, or a noisy oracle). State clearly what the simulation assumes.  
* **Ablations**: Where possible, show which components of the intervention are responsible for the effect.

Report negative or mixed results honestly. A well-documented intervention that does not beat the baseline is still a valid result.

**Team specific deliverables**: methodology and results (complementing the parts done by the Auditors) sections of the report.

### 4\. **Evaluators**

You are tasked with designing a user study that uses human evaluation to assess the performance of the proposed system as compared against existing baselines. This will involve defining user personas, selecting appropriate evaluation methods, and considering factors like user needs, usability, and potential biases. To avoid depending on other groups, you may (and probably should) design and test the human evaluation first using a simulated (i.e., [Wizard of Oz](https://en.wikipedia.org/wiki/Wizard_of_Oz_experiment)) setup.

To design a user study you need to think about both **how** and **why** a user would want to use the system. This concerns their motivation and end-goal for using the system, but also very practically how they would expect to interface with the system. For example, if your user persona describes a non-technical person, then they cannot be expected to submit compute jobs to a cluster and then parse terminal output. For further information on scenarios see [here](https://ocw.tudelft.nl/wp-content/uploads/2_RossonCarrollSBDforHandbook2002.pdf).

As part of the human evaluation design you should:

- **Define User Personas:** Develop at least two user personas that represent the target users of the ML system. Each persona should include details such as:  
    
  - Demographics (age, gender, location)  
  - Technical skills and experience with technology  
  - Goals and motivations for using the ML application (as scenarios)  
  - Potential challenges or concerns they might have with the system


  These personas do not have to cover all possible users of the system, however, at least one of them should be a more typical user based on your expectations.


- **Propose Evaluation Design:** Propose a user study design that incorporates relevant evaluation methods to assess the human-centred ML system. Possible designs include, and may involve one or more from:  
    
  - **Surveys:** Design a survey to gather user feedback on their experience with the ML application. This could cover aspects like ease of use, satisfaction with results, and trust in the system's outputs.  
  - **Task Completion Rates:** Outline a set of tasks that users would need to complete using the ML application. Measure the time taken and success rate for these tasks to assess usability and efficiency, as well as other relevant metrics to your project.  
  - **User Interviews:** Plan a series of semi-structured interviews with users to gain in-depth qualitative insights. Focus on understanding user needs, expectations, and any challenges they encounter while interacting with the ML system.  
  - **A/B Testing**: Design a setup in which you have two versions of the application which are meaningfully different in some dimension (related to the human-centred perspective of your project). Compare how users engage with each version  
* **Develop the Study interface**: You build the experimental interface that participants use. Start with a Wizard of Oz version, then replace the wizard with the Integrators’ model once it is delivered. The interface should match how your personas would realistically use the system. To compare against the baseline, plan for two versions of the interface (or one interface that can switch between the two systems).  
* **Check Ethics and consent**: Before running the study, obtain ethics approval through the university’s procedure for research with human participants, and plan time for it. Prepare an informed consent form.

**Team specific deliverables**: human evaluation and conclusion sections of the report.

## **Deliverables:**

### Report

The report will be structured as a research paper, following the [NeurIPS template](https://media.neurips.cc/Conferences/NeurIPS2026/Formatting_Instructions_For_NeurIPS_2026.zip), and the same paper formatting instructions:

All submissions must be in PDF format, and in a single PDF file include, in this suggested order

1. The submitted paper content  
2. Paper references  
3. Appendices containing any other supporting textual information e.g. proofs, experimental details (code and data will be submitted in a separate file).  
4. The [NeurIPS paper checklist](https://neurips.cc/public/guides/PaperChecklist)

As you will be directly handing in a final version, **the page limit is ten pages of content**. Additional pages containing references, optional technical appendices, and mandatory paper checklist do not count as content pages.

Expected sections in the paper are:

- Abstract  
- Introduction  
- Related Work  
- Data  
- Methodology  
- Results  
- Human Evaluation  
- Discussion (with impact and limitations subsections)  
- Conclusion  
- References  
- (Optional) Appendix  
- Paper Checklist

At the end of the abstract include a link to a Github repository with the relevant code from the project.

**Submission deadline: December 10, 2026 EOD**

### Presentations

Each group gives three presentations during the project. Every team contributes, and the presentation should reflect the project as a whole rather than four separate reports.

#### Week 3: Topic and approach (November 13\) \[Duration: 20 minutes \+ 10 minutes Q&A per group\]

Introduce your assigned topic and explain how your group plans to approach it. Cover:

- **Topic and context:** The task, the dataset, and who is involved in or affected by the system.  
- **Human-centred concerns:** The key stakeholders, their interests and conflicts, and your prioritised requirements.  
- **Critical reflection:** Initial concerns about the data, the problem framing, and potential harms, and what you want to keep an eye on throughout the project.  
- **Approach:** Your chosen baselines, the human-centred technique you plan to use, a first outline of the user study (including your personas), and how the teams' work fits together.

The aim is to get early feedback on your direction, so present open questions and choices you are unsure about.

#### Week 5: Progress (November 27\) \[Duration: 20 minutes \+ 10 minutes Q&A per group\]

Show where the project stands and what you have learned so far. Cover:

- **Progress per team:** For example, finalised requirements, first baseline results, the state of the intervention, and the study design and Wizard of Oz prototype.  
- **Changes:** What has changed since week 3, and why.  
- **Risks and next steps:** Open issues, dependencies between teams, and your plan for the remaining weeks.

Keep this presentation short and focused. Its main purpose is to catch problems while there is still time to adjust.

#### Week 8: Final (December 15\)  \[Duration: 45 minutes per group, plus team discussions\]

On behalf of the whole team present the full project and its outcomes, not everybody has to present. Cover:

- **Problem and requirements:** A brief recap of the topic, stakeholders, and requirements.  
- **Results:** The comparison between the intervention and the baselines, the audit findings, and the outcomes of the human evaluation.  
- **Requirements check:** To what extent the requirements are met, and how you know.  
- **Reflection:** Limitations, social impact, and what you would do differently.

**The slidedeck for the final presentation should be submitted on Canvas December 14, EOD**.

### Team discussions \[Duration: 20 minute \+ 10 minutes Q\&A per team\]

Following the final presentations, we will have a discussion between each of the two teams of the groups. In the following order:

1. Stakeholders  
2. Auditors  
3. Integrators  
4. Evaluators

Each discussion will involve 20 minutes of discussion between the teams, followed by 10 minutes Q\&A led by the course lecturers. During the discussion:

- Respond to other teams' observations and results by questioning or supporting their findings  
- Ensure everyone in the team contributes  
- You cannot "win" this discussion \- the goal is to jointly understand both projects better.

## **Grading:**

The project grade is composed of three components: Report (35%), Presentation (35%), Discussion (30%), together the project makes up 50% of the course grade.

The report will be evaluated based on:

* Fulfilment of responsibilities (20%)  
* Problem-solving and decision-making (30%)  
* Coherence and cross-team connections (15%)  
* Clarity of writing (15%)  
* One of, depending on role:  
  * Stakeholders: Requirements and project framing (20%)  
  * Auditors: Evaluation and audit (20%)  
  * Integrators: Experimental design (20%)  
  * Evaluators: Validity of the human evaluation (20%)

Full report rubric: [Canvas](https://canvas.uva.nl/courses/59847/files/16241043?module_item_id=3085418)

The presentations will be evaluated based on: 

* Presentation of content and understanding (30%)  
* Evidence and human-centred reflection (30%)  
* Clarity and delivery (20%)  
* Responses to questions (20%)

Full presentation rubric: [Canvas](https://canvas.uva.nl/courses/59847/files/16241045?module_item_id=3085419)

The discussions will be evaluated based on:

* Clarity and accuracy of group’s discussion contributions (40%)  
* Critical Reflection and Insight (30%)  
* Professionalism and Collegiality (15%)  
* Active participation in discussion (15%)

Full discussion rubric: [Canvas](https://canvas.uva.nl/courses/59847/files/16241047?module_item_id=3085420)