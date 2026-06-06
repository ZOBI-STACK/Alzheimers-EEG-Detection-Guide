# CHAPTER 1: PROJECT OVERVIEW

## 1.1 Introduction to Alzheimer's Disease

### 1.1.1 Definition

Alzheimer's Disease (AD) is a progressive, neurodegenerative disorder that primarily affects the cerebral cortex and hippocampus. It is the most common form of dementia, accounting for 60-80% of all dementia cases. The disease is characterized by progressive cognitive decline, memory loss, and behavioral changes that eventually lead to complete loss of cognitive functions.

### 1.1.2 Historical Context

- **1901**: Dr. Alois Alzheimer first described the disease
- **1910**: The disease was officially named "Alzheimer's Disease"
- **1984**: First genetic link discovered (APOE4 gene)
- **2003**: Amyloid Hypothesis becomes dominant theory
- **2023**: Lecanemab approved as first disease-modifying treatment

### 1.1.3 Epidemiology

**Current Statistics:**
- **World Prevalence**: 50 million people living with dementia (2020)
- **USA**: 6.5 million people with Alzheimer's Disease
- **Europe**: 10+ million people affected
- **Annual Cost**: $305 billion globally (2020)
- **Mortality Rate**: 3rd leading cause of death in USA (after heart disease and cancer)

**Age-related Incidence:**
- **65-74 years**: 3% prevalence
- **75-84 years**: 17% prevalence
- **85+ years**: 32% prevalence

### 1.1.4 Risk Factors

**Non-Modifiable Risk Factors:**
- Age (increases after 65)
- Genetics (APOE4 gene)
- Family history
- Head trauma history

**Modifiable Risk Factors:**
- Cognitive inactivity
- Physical inactivity
- Smoking
- Hypertension
- High cholesterol
- Diabetes
- Depression
- Poor sleep quality
- Social isolation

### 1.1.5 Pathophysiology

**Key Pathological Features:**

1. **Amyloid-Beta (Aβ) Accumulation**
   - Forms plaques between neurons
   - Disrupts neural communication
   - Triggers inflammatory response

2. **Tau Protein Tangles**
   - Hyperphosphorylated tau proteins
   - Form neurofibrillary tangles
   - Damage microtubules

3. **Neuroinflammation**
   - Glial cell activation
   - Release of pro-inflammatory cytokines
   - Neuronal death and atrophy

4. **Synaptic Dysfunction**
   - Loss of synaptic connections
   - Reduced neurotransmitters (acetylcholine)
   - Impaired plasticity

---

## 1.2 Understanding MCI (Mild Cognitive Impairment)

### 1.2.1 Definition

Mild Cognitive Impairment (MCI) is an intermediate stage between normal aging and dementia. Individuals with MCI experience noticeable cognitive decline beyond normal aging but maintain the ability to perform daily activities.

### 1.2.2 Diagnostic Criteria for MCI

**Core Features:**
1. Cognitive complaint from patient or informant
2. Cognitive impairment (documented on testing)
3. Preserved general cognition
4. Intact activities of daily living
5. Not meeting criteria for dementia

### 1.2.3 Subtypes of MCI

1. **Amnestic MCI (aMCI)** - Primary memory impairment
2. **Non-Amnestic MCI (naMCI)** - Other cognitive domains affected
3. **Single Domain vs. Multiple Domain** - Affects progression rates

---

## 1.3 Why EEG is Used Instead of MRI/PET

### 1.3.1 Comparison

| Aspect | EEG | MRI | PET |
|--------|-----|-----|-----|
| Cost | $ | $$$$ | $$$$ |
| Portability | Yes | No | No |
| Real-time | Yes | No | No |
| Spatial Resolution | Poor | Excellent | Fair |

### 1.3.2 EEG Advantages

- **Cost-effective**: $5,000-$50,000 equipment vs. $500k+ for MRI
- **Accessible**: Can be used in clinics, homes, portable
- **Functional**: Detects electrophysiological changes
- **Non-invasive**: No radiation, no contraindications
- **Repeatable**: Safe for frequent monitoring

---

## 1.4 Research Problem and Objectives

### 1.4.1 Problem Statement

Despite advances in neurology, early diagnosis of Alzheimer's Disease remains challenging. Most diagnoses are made at moderate-to-severe stages when irreversible neuronal damage has already occurred, limiting treatment effectiveness.

**Solution Approach**: Develop an automated, objective, cost-effective method using machine learning on EEG signals for early detection.

### 1.4.2 Primary Research Objectives

1. Develop ML pipeline for EEG analysis
2. Implement deep learning models
3. Achieve ≥95% classification accuracy
4. Create production-ready application
5. Validate clinical applicability

---

## 1.5 Project Scope

### 1.5.1 Included

- Public EEG datasets (ADNI, OASIS, PhysioNet)
- 3 classes: Normal, MCI, Alzheimer's
- Signal processing and feature extraction
- 6 ML + 5 DL models
- Flask web application
- Cloud deployment

### 1.5.2 Excluded

- Brain imaging (MRI, PET) integration
- Genetic analysis
- Clinical validation with new patients
- Mobile app development
- Real-time continuous monitoring

---

## 1.6 Expected Outcomes

### 1.6.1 Technical Outcomes

- Classification accuracy ≥95%
- Sensitivity ≥90%
- Specificity ≥90%
- AUC ≥0.95

### 1.6.2 Deliverables

1. Data processing pipeline
2. Trained ML/DL models
3. Performance metrics
4. Software application
5. Comprehensive documentation
6. Research paper
7. Thesis document

---

## 1.7 Real-World Applications

### 1.7.1 Clinical Applications

1. **Screening in Primary Care**
   - Cost: $200-500 vs. $2,000+ for MRI
   - Time: 30 minutes vs. weeks for appointments
   - Accessibility: Office-based vs. specialty centers

2. **Monitoring in Specialist Clinics**
   - Track disease progression
   - Monitor treatment response

3. **Telemedicine Applications**
   - Home-based EEG monitoring
   - Remote patient assessment
   - Continuous monitoring with wearables

### 1.7.2 Public Health Applications

- Population screening in elderly care facilities
- Large-scale epidemiological studies
- Preventive medicine programs
- Healthcare cost reduction

---

**Next: Chapter 2 - Fundamentals of EEG Signals**