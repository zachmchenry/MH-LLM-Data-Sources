# Mental Health Datasets

## **IMHI Dataset**

**Description**: First multi-task instruction dataset for interpretable mental health analysis with 105K samples across 8 tasks[1](https://github.com/SteveKGYang/MentalLLaMA)[(https://www.medrxiv.org/content/10.1101/2024.12.29.24319755v1.full.pdf). Includes 10 test sets (19K samples) for depression detection, stress cause analysis, and wellness dimension identification

| **Component** | **Details** |
| --- | --- |
| **Data Sources** | Reddit, Twitter, SMS posts |
| **Annotations** | Weak labels (34K SWMH posts) + human annotations (IRF, MultiWD) |
| **Structure** | Instruction-tuning (query/response) + completion formats |
| **Key Tasks** | Depression/stress detection, cause analysis, risk factor identification |
| **Authors** | Tianlin Zhang, Shaoxiong Ji et al. (University of Manchester/AIST) |
| **Availability** | Publicly released training/test data for DR, dreaddit, SAD, MultiWD, IRF |
|  |  |

**Data Source** : Reddit, Twitter, SMS

**GitHub:**   [IMHI and MentaLLaMA](https://github.com/IMHI-MentalHealth/MentaLLaMA)

**Files Breakdown Table**:

| **Name** | **Task** | **Data Split** | **Data Source** | **Annotation** | **Released** |
| --- | --- | --- | --- | --- | --- |
| [DR](https://aclanthology.org/W18-5903/) | Depression detection | 1,003/430/405 | Reddit | Weak labels | Yes |
| [CLP](https://aclanthology.org/W15-1204/) | Depression detection | 456/196/299 | Reddit | Human annotations | Not yet |
| [dreaddit](https://aclanthology.org/D19-6213/) | Stress detection | 2,837/300/414 | Reddit | Human annotations | Yes |
| [SWMH](https://arxiv.org/abs/2004.07601) | Mental disorders detection | 34,822/8,705/10,882 | Reddit | Weak labels | Not yet |
| [T-SID](https://arxiv.org/abs/2004.07601) | Mental disorders detection | 3,071/767/959 | Twitter | Weak labels | Not yet |
| [SAD](https://dl.acm.org/doi/10.1145/3411763.3451799) | Stress cause detection | 5,547/616/684 | SMS | Human annotations | Yes |
| [CAMS](https://aclanthology.org/2022.lrec-1.686/) | Depression/suicide cause detection | 2,207/320/625 | Reddit | Human annotations | Not yet |
| loneliness | Loneliness detection | 2,463/527/531 | Reddit | Human annotations | Not yet |
| [MultiWD](https://github.com/drmuskangarg/MultiWD) | Wellness dimensions detection | 15,744/1,500/2,441 | Reddit | Human annotations | Yes |
| [IRF](https://aclanthology.org/2023.findings-acl.757/) | Interpersonal risks factors detection | 3,943/985/2,113 | Reddit | Human annotations | Yes |
- **The MentaLLaMA Paper:**
    
    [MentaLLaMA: Interpretable Mental Health Analysis on Social Media with Open-Source Instruction-Tuned LLMs](https://openreview.net/forum?id=KPq438T0uC)
    
- **The Evaluation Paper:**
    
    [Evaluation Paper (arXiv)](https://arxiv.org/abs/2304.03347)
    

---

## **MultiWD Dataset**

**Description**: Multi-label wellness dimension analysis based on Dunn's model (physical, emotional, social, etc.)

**Data Source**: Reddit

**GitHub** [MultiWD GitHub](https://github.com/drmuskangarg/MultiWD)

| **Component** | **Details** |
| --- | --- |
| **Data Sources** | 3,281 Reddit posts from r/depression and r/SuicideWatch |
| **Annotations** | Expert panel (clinical psychologist + NLP researchers) |
| **Class Balance** | Skewed distribution: Social/Emotional > Vocational/Spiritual |
| **Applications** | Early crisis detection, longitudinal wellness tracking |
| **Authors** | MSVPJ Sathvik, Muskan Garg (Mayo Clinic/Lakehead University) |
| **Availability** | Public on GitHub with 15K training samples |

**Files Breakdown Table**:

| **File** | **Description** | **Instances** |
| --- | --- | --- |
| train.csv | Training set (Reddit posts + labels) | 2,281 |
| dev.csv | Development/validation set | 500 |
| test.csv | Test set | 500 |
- **Primary Paper:**
    
    [MultiWD: Multi-label wellness dimensions in social media posts (Journal of Biomedical Informatics, 2024)](https://www.sciencedirect.com/science/article/abs/pii/S1532046424000042)
    
    [Alternate publisher link (PubMed)](https://pubmed.ncbi.nlm.nih.gov/38191011/)
    

---

## **IRF Dataset**

**Description**: Interpersonal risk factor analysis focusing on suicide prevention[4](https://aclanthology.org/2023.findings-acl.757.pdf)[9](https://arxiv.org/html/2406.12033v1).

| **Component** | **Details** |
| --- | --- |
| **Data Sources** | 3,522 Reddit posts |
| **Annotations** | Human-labelled explanations for TBe/PBu categories |
| **Structure** | CSV files with text, binary labels, and free-text explanations |
| **Key Metrics** | F1=0.76 using BERT-based models |
| **Authors** | Muskan Garg et al. (ACL Findings 2023) |
| **Availability** | Public on GitHub with train/val/test splits |

**Data Source**: Reddit

**GitHub**: [IRF GitHub](https://github.com/am-shb/irf-acl)

**Files Breakdown Table**:

| **File** | **Description** | **Samples** |
| --- | --- | --- |
| train.csv | Training set | 2,522 |
| val.csv | Validation set | 500 |
| test.csv | Test set | 500 |
- **Primary Paper:**
    
    [Iterative random forests to discover predictive and stable high-order interactions](https://www.pnas.org/doi/10.1073/pnas.1711236115)
    

---

## **C2D2 Dataset**

**Description**: Chinese cognitive distortion analysis with mental health correlations[3](https://aclanthology.org/2023.findings-emnlp.680/)[8](https://openreview.net/forum?id=NO5dc8Ljvj)[10](https://aclanthology.org/2023.findings-emnlp.680.pdf).

| **Component** | **Details** |
| --- | --- |
| **Data Sources** | 7,500 synthetic thoughts (450 life scenarios) |
| **Annotations** | Expert-supervised (7 distortion types) |
| **Extensions** | C2D2-E: Machine-translated English version |
| **Applications** | Enhanced mental disorder detection (+12% F1) |
| **Authors** | Bichen Wang et al. (Harbin Institute of Technology) |
| **Availability** | Restricted access via institutional request |

**Data Source**: Synthetic scenarios

**GitHub**: [C2D2 GitHub](https://github.com/bcwangavailable/C2D2-Cognitive-Distortion)

**Files Breakdown Table**:

| **File** | **Description** | **Samples** |
| --- | --- | --- |
| train.json | Training set (Chinese, cognitive distortions) | ~6,000 |
| dev.json | Validation set | ~750 |
| test.json | Test set | ~750 |
| c2d2-e.json | English extension (machine-translated) | Varies |


*Note: The C2D2 folder currently does not contain data, but data may be available via request to the authors.*

- **Primary Paper:**
    
    [C2D2 Dataset: A Resource for the Cognitive Distortion Analysis and Its Impact on Mental Health (EMNLP 2023)](https://aclanthology.org/2023.findings-emnlp.680/)


---

##Specialized Approaches for Mental Health Recognition

For mental health-specific applications, several specialized techniques have proven effective:

**Dual LoRA (Low-rank Adaptation):** This approach enables efficient fine-tuning of lightweight models specifically for mental health applications. MentalQLM, a model with only 0.5B parameters, demonstrated strong performance using this method
**Multi-task instruction tuning:** Training the model across multiple mental health-related tasks simultaneously improves its overall understanding of mental health contexts and language patterns


##Data Requirements for Mental Health Recognition

##Types of Datasets Needed

Training an LLM to recognize mental health issues requires specific types of data:


1.)Mental health instruction datasets: These contain question-answer pairs specifically designed for mental health assessment and recognition
2.) Classification datasets: These labeled datasets help the model identify various mental health conditions or symptoms from text2.
3.) Cognitive distortion datasets: These specialized collections help models recognize patterns of irrational thinking that may indicate mental health issues
4.) Social media text with mental health annotations: Real-world examples of how people express mental health concerns in their everyday communications


##Dataset Size Considerations

Research indicates that quality and diversity of data may be more important than sheer volume when fine-tuning for mental health applications:

- Fine-tuning LLMs on "a few hundred samples" across multiple datasets can already achieve favorable performance
- When data size is the same, fine-tuning on data with larger variation (more datasets and tasks) achieves better performance
- The Mental-Alpaca and Mental-FLAN-T5 models outperformed GPT-3.5 (25 times bigger) by 10.9% on balanced accuracy after proper fine-tuning


##Resources Required for Training

##Computing Infrastructure

The hardware requirements for LLM training depend on whether you're training from scratch or fine-tuning an existing model:

1.) Training from scratch:

- Full-sized models like GPT-3 require around 800GB of storage4.
- They may need 8-10 high-end GPUs (80GB+ each) running for months
- Estimated costs can range from $150,000 to $250,000 for hardware alone


2.) Fine-tuning an existing model:

-Much more feasible with significantly lower resource requirements.
-Can be accomplished with 1-4 GPUs depending on the base model size.
-Lightweight models (0.5B parameters) have shown strong performance for mental health applications2.


##Time and Cost Considerations

Training duration and costs are determined by several factors:


1.) Model size: Larger models require more computational resources and take longer to train
2.) Data volume: Following the "Chinchilla" scaling law, optimal training uses roughly 20 tokens of data per parameter in the model
3.) Fine-tuning approach: Domain-specific fine-tuning (like for mental health) can be achieved in days or weeks rather than the months required for training from scratch
4.) Training strategy: Efficient approaches like LoRA (Low-Rank Adaptation) significantly reduce computational requirements by only updating a small subset of model parameters

For most business applications seeking mental health recognition capabilities, fine-tuning an existing open-source model is the most practical approach. This can be accomplished with a budget in the tens of thousands rather than millions of dollars, and in weeks rather than months


##Achieving 95% Accuracy in Mental Health Recognition

###Measurement Challenges

Achieving 95% accuracy in mental health recognition presents unique challenges:


1.) Nuanced language: Mental health expressions can be subtle. For example, "I'm fine" might mask depression, while "I can't breathe" could signal anxiety rather than a physical issue
2.) Balanced metrics: Traditional accuracy measures can be misleading for imbalanced data common in mental health. "Balanced accuracy," which considers performance across all classes, provides a more realistic assessment
3.( Multi-faceted evaluation: A single accuracy number is insufficient; models must be evaluated on sensitivity, specificity, and risks of false positives/negatives6


##Approaches to Improve Accuracy

Several techniques have proven effective for improving mental health recognition accuracy:


1.) Multi-dataset fine-tuning: Training across diverse datasets improves generalizability across different expressions and contexts of mental health issues
2.) Domain-specific instruction tuning: Creating mental health-specific instructions and examples significantly improves model performance for this specialized domain
3.) Expert validation: Having mental health professionals review and validate model outputs during training helps identify and correct subtle misunderstandings
4.) Red-flag language detection: Specific training to recognize cognitive distortions and warning signs in text has shown accuracy comparable to clinically trained human raters


##Ethical Considerations and Best Practices

###Risks in Mental Health Applications

Deploying LLMs for mental health recognition carries significant responsibilities:


1.) Risk of harm: A poorly calibrated model could miss signs of suicidal ideation or escalate a crisis through inappropriate responses

2.) Misdiagnosis potential: Issues of low reliability can lead some individuals to be misdiagnosed or to pursue inappropriate interventions

3.) Privacy and data sensitivity: Mental health data is deeply personal and requires stringent privacy protections beyond standard data practices


##Best Practices for Responsible Development

To develop mental health recognition capabilities responsibly:


1.) Human-in-the-loop oversight: Maintain human expert involvement throughout development and deployment

2.) Robust testing across demographics: Ensure the model performs consistently across different age groups, genders, ethnicities, and socioeconomic backgrounds

3.) Clear limitation disclosure: Be transparent about what the model can and cannot do, particularly in clinical contexts6.

4.) Continuous monitoring: Establish ongoing evaluation mechanisms to identify and address emerging biases or performance issues
