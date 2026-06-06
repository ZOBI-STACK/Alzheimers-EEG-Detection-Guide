# CHAPTER 2: FUNDAMENTALS OF EEG SIGNALS

## 2.1 What is EEG?

### 2.1.1 Definition

Electroencephalography (EEG) is a non-invasive neuroimaging technique that measures electrical activity of the brain using electrodes placed on the scalp. It records the voltage fluctuations resulting from ionic currents within neurons.

**Key Characteristics:**
- Measures: Electrical potentials (in microvolts, μV)
- Temporal resolution: 1 millisecond (1000 Hz typical)
- Non-invasive: Surface electrodes only
- Direct measurement: Neural electrical activity
- Dynamic: Captures real-time brain function

### 2.1.2 Historical Development

- **1924**: Hans Berger records first human EEG
- **1935**: First clinical EEG machine
- **1950s**: Standardization of electrode placement
- **1970s**: Digital EEG systems introduced
- **2000s**: Advanced signal processing and AI
- **2020s**: Portable and wearable EEG devices

---

## 2.2 How EEG Works

### 2.2.1 Physiological Basis

**Neuronal Electrical Activity:**

1. **Single Neuron Activity**
   - Resting potential: -70 mV (inside cell)
   - Action potential: +30 mV depolarization
   - Synaptic potentials: Small voltage changes
   - Ion channels (Na+, K+, Ca2+, Cl-) control membrane potential

2. **Population Recording**
   - EEG records synchronized activity of 100,000+ neurons
   - Thousands of neurons firing synchronously = measurable signal
   - Asynchronous activity cancels out
   - Pyramidal neurons = main source (parallel orientation)

### 2.2.2 Signal Generation

**Electrical Field Formation:**
```
Individual Neurons (10-100 μV)
    ↓
Neural Populations (1,000-10,000 neurons)
    ↓
Synchronized Activity
    ↓
Electrical Field (10-100 μV detected at scalp)
    ↓
Electrode Recording
    ↓
Amplification (1,000-10,000x)
    ↓
EEG Signal (1-100 μV recorded)
```

---

## 2.3 EEG Electrode Placement (10-20 System)

### 2.3.1 Standard Montage

The **10-20 System** is the international standard for electrode placement.

**Naming Convention:**
- **First letter**: Brain region (F=Frontal, C=Central, P=Parietal, T=Temporal, O=Occipital)
- **Second letter**: Hemisphere (z=Central, Odd=Left, Even=Right)

**Common 10-20 Electrode Locations:**

```
        Nz
    Fp1   Fp2
    F7  F3  Fz  F4  F8
    A1  T3  C3  Cz  C4  T4  A2
    T5  P3  Pz  P4  T6
    O1  Oz  O2
```

---

## 2.4 EEG Frequency Bands

### 2.4.1 Delta Band (0.5-4 Hz)
- Deep sleep, coma, anesthesia
- **AD Marker**: Increased during wakefulness = pathological

### 2.4.2 Theta Band (4-8 Hz)
- Drowsiness, light sleep, memory consolidation
- **AD Marker**: Increased theta = cognitive slowing

### 2.4.3 Alpha Band (8-12 Hz)
- Relaxed wakefulness, eyes closed
- **AD Marker**: DECREASED alpha = hallmark of Alzheimer's

### 2.4.4 Beta Band (12-30 Hz)
- Active thinking, problem solving, attention
- **AD Marker**: Reduced beta power

### 2.4.5 Gamma Band (30-100 Hz)
- Consciousness, attention, perception
- **AD Marker**: Reduced gamma in AD

**Visual Summary:**
```
Frequency | Band    | Normal State          | AD Marker
0-4 Hz    | Delta   | Deep sleep           | ↑ Increased
4-8 Hz    | Theta   | Drowsiness          | ↑ Increased
8-12 Hz   | Alpha   | Relaxation          | ↓ DECREASED (Key)
12-30 Hz  | Beta    | Active thinking     | ↓ Decreased
30-100 Hz | Gamma   | Consciousness       | ↓ Decreased
```

---

## 2.5 EEG Acquisition Process

### 2.5.1 Standard Acquisition Parameters

- **Sampling rate**: 500 Hz (minimum 250 Hz)
- **High-pass filter**: 0.5-1 Hz
- **Low-pass filter**: 70 Hz
- **Notch filter**: 50/60 Hz (power line)
- **Recording duration**: 10-30 minutes
- **State**: Resting with eyes closed

---

## 2.6 EEG Artifacts

### 2.6.1 Common Artifacts

| Artifact | Source | Amplitude | Removal |
|----------|--------|-----------|---------|
| Eye Blink | Ocular | 100-500 μV | ICA |
| Eye Movement | Ocular | 50-200 μV | ICA |
| Muscle (EMG) | Jaw/Neck | 100+ μV | Filtering, ICA |
| Power Line | Electrical | Variable | Notch filter |
| Motion | Movement | 100+ μV | Artifact rejection |
| Sweat | Skin | Slow drift | Re-apply |
| Electrode Pop | Contact loss | Large transient | Re-check |

### 2.6.2 Artifact Removal Methods

1. **Visual Inspection** - Manual marking and rejection
2. **Automated Detection** - Threshold-based identification
3. **ICA (Independent Component Analysis)** - Most effective
4. **Filtering** - Frequency-based removal
5. **Regression** - EOG/EMG signal removal

---

## 2.7 EEG Changes in Alzheimer's Disease

### 2.7.1 Key EEG Biomarkers

**Most Sensitive Markers:**
1. **Alpha slowing** - Peak frequency shifts from 10 Hz to 8 Hz
2. **Theta/Alpha ratio** - Increases with disease severity
3. **Posterior alpha loss** - Loss of occipital dominance
4. **Reduced connectivity** - Decreased synchronization

### 2.7.2 Disease Progression Pattern

```
Normal EEG:
  Peak: 10-11 Hz (alpha)
  Pattern: Posterior dominant, reactive

MCI EEG:
  Peak: 8-9 Hz (alpha slowing)
  Pattern: Subtle posterior reduction
  Increase: Theta power

Mild AD:
  Peak: 7-8 Hz (marked slowing)
  Pattern: Loss of posterior dominance
  Increase: Theta and delta

Moderate-Severe AD:
  Peak: 5-6 Hz (severe slowing)
  Pattern: Generalized slowing, no reactivity
  Dominant: Delta and theta rhythms
```

---

**Next: Chapter 3 - System Requirements**