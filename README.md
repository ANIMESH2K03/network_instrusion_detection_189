# UNSW-NB15 Network Intrusion Detection

Binary network intrusion detection pipeline built on the **UNSW-NB15** dataset (`0` = Normal, `1` = Attack) as an **MCA final-year PBL (Project-Based Learning)** project. The pipeline explores network traffic patterns and attack distributions, avoids target leakage by excluding `attack_cat` from feature inputs, trains and tunes multiple classical ML models with stratified cross-validation, evaluates performance on a held-out test set, and persists the fitted pipeline for reuse.

---

## Project Overview

* **Task:** Binary classification of network flow records (`label`: `0` for normal traffic, `1` for attack traffic).
* **Dataset:** UNSW-NB15 (standard train/test split with network flow, protocol, service, byte/packet, and connection features).
* **Leakage Prevention:** `attack_cat` (and any non-feature identifiers/targets) are excluded from model features so predictions rely strictly on traffic telemetry rather than fine-grained attack labels.
* **Models Evaluated:**
  * Logistic Regression
  * Decision Tree Classifier
  * Random Forest Classifier
