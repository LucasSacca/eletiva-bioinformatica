# 🧬 Lung Cancer Somatic Mutation Analysis (NGS Pipeline)

## 📌 Project Overview

This project was developed as part of an **elective course in Biomedical Engineering** and focuses on the end-to-end analysis of next-generation sequencing (NGS) data from a lung tumor biopsy.

The objective is to simulate a real clinical genomics workflow — from raw sequencing data to clinical interpretation and reporting — enabling precision oncology decision-making.

---

## 🧬 Clinical Case

* **Patient**: Male, 65 years old
* **History**: Long-term smoker
* **Symptoms**: Persistent cough, weight loss, chest pain
* **Family history**: Positive for cancer

The patient was referred for a **somatic mutation panel** to investigate genetic alterations associated with lung cancer and guide personalized treatment.

---

## 🎯 Objectives

This project includes the following goals:

1. Design a complete bioinformatics pipeline
2. Process raw sequencing data (FASTQ → results)
3. Identify somatic variants (SNVs and indels)
4. Perform clinical interpretation using curated databases
5. Generate a clinical-style report for medical decision-making

---

## ⚙️ Pipeline Overview

The analysis workflow includes:

### 1. Quality Control

* Assessment of raw reads (e.g., FastQC)

### 2. Pre-processing

* Adapter trimming and quality filtering

### 3. Alignment

* Mapping reads to the human reference genome

### 4. Post-processing

* Sorting, indexing, duplicate marking

### 5. Variant Calling

* Identification of somatic variants (SNVs/indels)

### 6. Variant Annotation

* Functional and clinical annotation

### 7. Variant Filtering

* Selection of clinically relevant mutations

### 8. Clinical Interpretation

* Cross-referencing with:

  * OncoKB
  * COSMIC
  * OMIM

---

## 🧪 Key Results

The analysis identified **two clinically actionable mutations**:

### 🔬 EGFR p.L858R

* Activating mutation in a receptor tyrosine kinase
* Strongly associated with **non-small cell lung cancer (NSCLC)**
* Indicates sensitivity to EGFR-targeted therapies

### 🔬 BRAF p.V600E

* Constitutive activation of MAPK/ERK signaling pathway
* Also associated with NSCLC and other cancers
* Targetable with BRAF/MEK inhibitor combinations

These findings are consistent with known oncogenic drivers and provide relevant therapeutic opportunities.

📄 Detailed clinical interpretation available in:
👉 `laudo.md` 

---

## 💊 Therapeutic Implications

Based on the detected variants:

* **EGFR inhibitors**: Osimertinib, Erlotinib, Gefitinib
* **BRAF-targeted therapy**:

  * Dabrafenib + Trametinib
  * Encorafenib + Binimetinib

---

## 📁 Data Availability

Due to file size limitations, raw sequencing data is not hosted in this repository.

🔗 Download files here:

https://drive.google.com/file/d/18KCnpWgmfrKlwfSnldrta6pTmRQmKIJ3/view?usp=sharing

https://drive.google.com/file/d/11fPvzmRhJJSjrG0XJKh1xH0T3F0defPz/view?usp=sharing

https://drive.google.com/file/d/19BLK-_l_dAy7yA88H4durQSK_CNkA0iE/view?usp=sharing

Format:

* `.fastq.gz` (compressed sequencing reads)

---

## ▶️ How to Run the Pipeline

To execute this pipeline locally, you must first download the required input files and correctly configure the environment.

### 📁 Required Input Files

Place the following files in your execution directory:

* `Chr7-reference.fasta.gz`
* `caso3-tumor-pulmonar_R1.fastq.gz`
* `caso3-tumor-pulmonar_R2.fastq.gz`

---

### ⚙️ Environment Configuration

Before running the pipeline, you must update the configuration cells in the notebook:

1. Open the main `.ipynb` file
2. Locate **Cell 1 and Cell 2 (environment configuration)**
3. Modify the file paths to match your local directory

Example:

```python
reference_genome = "/your/path/Chr7-reference.fasta.gz"
fastq_r1 = "/your/path/caso3-tumor-pulmonar_R1.fastq.gz"
fastq_r2 = "/your/path/caso3-tumor-pulmonar_R2.fastq.gz"
```

⚠️ If these paths are not correctly configured, the pipeline will not detect the input files.

---

### ▶️ Running the Analysis

After configuration:

1. Execute the notebook sequentially
2. Monitor outputs at each step (QC, alignment, variant calling)
3. Final results will include variant identification and interpretation

---

### 💡 Notes

* Ensure all input files are in `.gz` format
* No need to unzip — tools can read compressed files directly
* File paths must be absolute or correctly referenced

---


## 📊 Outputs

* Variant Call Format (VCF) file
* Annotated variant table
* List of actionable mutations
* Clinical report (`laudo.md`)

---

## 🧠 Interpretation Approach

Variants were evaluated considering:

* Gene function and oncogenic relevance
* Mutation type and predicted impact
* Evidence from curated cancer databases
* Clinical actionability and available therapies

---

## ⚠️ Disclaimer

This project is intended for **educational purposes only** and does not replace professional medical diagnosis or treatment.

---

## 👨‍🔬 Authors

* Lucas
* Julia

---

## 📚 References

* OncoKB: https://www.oncokb.org
* COSMIC: https://cancer.sanger.ac.uk
* OMIM: https://www.omim.org

---
