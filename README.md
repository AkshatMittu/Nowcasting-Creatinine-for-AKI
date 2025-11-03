## Nowcasting Serum Creatinine for Acute Kidney Injury (AKI)

This project develops a **time-aware nowcasting model** to estimate *current* serum creatinine levels for ICU patients — reducing unnecessary blood draws while maintaining accurate AKI detection.

---

### Overview
Serum creatinine is a key indicator of kidney health. Traditional methods forecast future values, which may change with treatment.  
Our approach **nowcasts** the *current but unmeasured* value using:
- Demographics
- Prior labs and vitals
- Time gaps between measurements

**Dataset:** [MIMIC-III Clinical Database Demo](https://physionet.org/content/mimiciii-demo/1.4/)

---

### Model & Results
We used **XGBoost** and a **Neural Network (PyTorch)** for binary classification of creatinine stages.

| Metric | XGBoost | Neural Net |
|:-------|:---------|:-----------|
| Accuracy | 94.17% | ~92% |
| Macro AUROC | 0.992 | — |
| Micro AUROC | 0.995 | — |

Ablation studies confirmed the importance of time-aware and abnormality features. We also tried using Neural-ODE for irregular timestamped data.

---

### Project Structure
├── data/

├── main.py

├── requirements.txt

├── utils/

└── README.md

Please run the following commands:

```bash
pip install -r requirements.txt
python main.py
```

### Team
- Akshat Dasula (GitHub: AkshatDasula/AkshatMittu)
- Anjali Vemula (GitHub: VemulaAnjali)


