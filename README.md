# Sentinel SIEM Behavioural Threat Detection using Machine Learning

## Security Analytics & Detection Engineering Project

Modern organisations generate enormous volumes of authentication telemetry through Security Information and Event Management (SIEM) platforms such as Microsoft Sentinel. Within large enterprise environments, these authentication logs contain valuable indicators of potentially malicious activity, including compromised accounts, credential misuse, and abnormal access behaviour.

Traditional SIEM detection mechanisms rely heavily on static rule-based alerts. While effective for identifying known attack signatures, rule-based approaches often struggle to detect subtle behavioural anomalies hidden within high-volume authentication data.

This project investigates how behavioural analytics and machine learning techniques can be applied to SIEM authentication logs in order to enhance threat detection capabilities within modern Security Operations Centres (SOCs).

The system developed in this research builds a complete threat detection pipeline that transforms raw authentication telemetry into behavioural intelligence capable of identifying suspicious login activity and abnormal user access patterns.

The project integrates several core components of modern cybersecurity analytics:

• SIEM telemetry analysis using Microsoft Sentinel authentication logs  
• Behavioural feature engineering to model user login behaviour  
• Statistical anomaly detection techniques  
• Machine learning based behavioural modelling  
• Temporal activity and session behaviour analysis  
• Simulated adversarial attack injection for detection validation  

Rather than relying purely on predefined detection rules, this system focuses on identifying deviations from normal behavioural baselines. By analysing authentication patterns over time, the model can highlight suspicious login activity that may indicate compromised accounts, brute-force attempts, or anomalous access behaviour.

This repository documents the full implementation of the threat detection pipeline, including data preprocessing, behavioural feature engineering, anomaly detection modelling, and validation using simulated adversarial activity.


---

## Project Objectives

The primary objective of this project is to demonstrate how behavioural analytics and machine learning can enhance SIEM-based threat detection by analysing authentication telemetry at scale.

The research aims to:

• Analyse authentication log data collected from Microsoft Sentinel  
• Develop behavioural features that model user login patterns  
• Apply anomaly detection techniques to identify abnormal authentication behaviour  
• Evaluate detection effectiveness through simulated attack scenarios  
• Demonstrate how behavioural analytics can complement traditional SIEM detection rules  

By combining SIEM telemetry with data science techniques, the project illustrates how modern security monitoring environments can improve visibility into suspicious authentication activity and potential security threats.


---

## Key Capabilities Demonstrated

This project demonstrates several capabilities relevant to modern cybersecurity and detection engineering roles:

• SIEM log analysis and security telemetry investigation  
• Authentication log processing and enrichment  
• Behavioural feature engineering for cybersecurity analytics  
• Statistical anomaly detection in security data  
• Machine learning based threat detection  
• Security event pattern analysis  
• Simulated attack validation within security datasets  

Together, these components form a behavioural threat detection framework designed to assist Security Operations Centres in identifying suspicious authentication behaviour within large volumes of SIEM log data.

---

## Threat Detection System Architecture

The detection framework developed in this project follows a structured security analytics pipeline designed to transform raw SIEM authentication telemetry into actionable behavioural threat intelligence.

Rather than relying solely on rule-based detection mechanisms, the system analyses authentication behaviour patterns across users, devices, and time in order to identify anomalous login activity that may indicate potential security threats.

The architecture consists of multiple analytical layers which progressively transform raw security telemetry into behavioural detection signals.

---

### Detection Pipeline Overview

The complete detection workflow can be summarised as follows:

Microsoft Sentinel Authentication Logs  
↓  
Log Extraction and Dataset Preparation  
↓  
Data Preprocessing and Normalisation  
↓  
Behavioural Feature Engineering  
↓  
Statistical and Machine Learning Anomaly Detection  
↓  
Simulated Attack Injection for Validation  
↓  
Threat Detection Analysis and Evaluation

Each stage of this pipeline performs a specific role in transforming large volumes of SIEM telemetry into meaningful detection insights.

---

### Stage 1 — Log Collection

Authentication telemetry was collected from Microsoft Sentinel, focusing primarily on Azure Active Directory SigninLogs. These logs record authentication events across users, devices, and IP addresses and provide detailed information regarding login attempts within an organisation’s identity infrastructure.

The dataset contains authentication attributes including:

• User identity information  
• Source IP addresses  
• Authentication timestamps  
• Device and client details  
• Authentication outcomes  
• Location and session data  

These logs provide the raw telemetry required to analyse authentication behaviour and detect suspicious access patterns.

---

### Stage 2 — Log Extraction and Dataset Preparation

Raw SIEM log data was exported and converted into structured datasets suitable for analysis within a Python-based data science environment.

During this stage:

• Relevant authentication fields were extracted  
• Unnecessary or incomplete records were removed  
• Timestamp formats were standardised  
• Data structures were prepared for further analysis  

The resulting datasets formed the foundation for the behavioural modelling pipeline.

---

### Stage 3 — Data Preprocessing

Before behavioural analysis could be performed, the authentication dataset required extensive preprocessing to ensure data consistency and analytical accuracy.

This stage included:

• Timestamp normalisation and datetime conversion  
• Sorting authentication events chronologically  
• Handling missing or incomplete log entries  
• Data type correction and formatting  
• Preparation of fields required for behavioural feature extraction  

These preprocessing steps ensured that authentication events could be accurately analysed across time-based behavioural patterns.

---

### Stage 4 — Behavioural Feature Engineering

Feature engineering plays a critical role in behavioural anomaly detection. Rather than analysing raw authentication logs directly, additional behavioural indicators were derived to model typical user login activity.

Examples of engineered features include:

• Login frequency metrics for individual users  
• Session gap calculations measuring time between login events  
• Temporal login patterns across hours and days  
• Source IP activity patterns  
• Authentication behaviour consistency indicators  

These behavioural attributes allow the system to model baseline authentication behaviour and identify deviations from normal patterns.

---

### Stage 5 — Anomaly Detection Models

Once behavioural features were constructed, statistical and machine learning techniques were applied to identify authentication events that deviate significantly from normal activity patterns.

Anomaly detection methods were used to analyse behavioural outliers within the dataset, highlighting login events that may represent suspicious activity.

The models analyse behavioural indicators such as:

• Unusually high login frequency  
• Abnormal session timing behaviour  
• Sudden changes in authentication patterns  
• Irregular access activity from user accounts  

Authentication events that significantly deviate from established behavioural baselines are flagged as potential anomalies requiring further investigation.

---

### Stage 6 — Simulated Attack Injection

To evaluate the effectiveness of the anomaly detection framework, simulated malicious authentication activity was introduced into the dataset.

These simulated events represent common attack behaviours such as:

• Rapid repeated login attempts  
• Abnormal authentication timing  
• Suspicious login patterns  

By injecting controlled adversarial activity into the dataset, the system's ability to detect behavioural anomalies could be assessed under realistic threat scenarios.

---

### Stage 7 — Threat Detection Analysis

The final stage of the pipeline analyses detected anomalies to determine whether they represent potentially malicious activity.

Detected anomalies are examined within the broader behavioural context of user authentication activity to evaluate their significance as potential security events.

This analysis demonstrates how behavioural anomaly detection techniques can assist Security Operations Centres by highlighting suspicious authentication behaviour that may otherwise remain hidden within large volumes of SIEM telemetry.

---

---

## Technology Stack and Analytical Environment

The threat detection framework developed in this project integrates SIEM telemetry analysis with data science and machine learning techniques. The system was implemented using a combination of security monitoring technologies and Python-based analytical tools designed to process, analyse, and model authentication behaviour within large volumes of SIEM log data.

The analytical workflow was constructed to simulate a realistic security analytics environment similar to those used within modern Security Operations Centres (SOCs).

---

### Security Monitoring Platform

**Microsoft Sentinel (SIEM Platform)**

Microsoft Sentinel was used as the primary Security Information and Event Management (SIEM) platform within this project. Sentinel provides large-scale log ingestion, security telemetry aggregation, and advanced monitoring capabilities across identity infrastructure and cloud environments.

Authentication telemetry analysed within this project was derived from **Azure Active Directory SigninLogs**, which capture detailed records of authentication events occurring across users, devices, and network locations.

These logs provide critical visibility into authentication behaviour and are widely used within enterprise SOC environments for monitoring identity-based threats such as credential misuse and account compromise.

---

### Data Analysis Environment

**Python Data Science Ecosystem**

All log analysis, preprocessing, feature engineering, and anomaly detection modelling were implemented using Python within a Jupyter Notebook environment. This environment enabled iterative data exploration, behavioural modelling, and machine learning experimentation across large authentication datasets.

The Python data science ecosystem provided flexible tools for analysing SIEM telemetry and constructing behavioural detection models.

---

### Core Python Libraries

The following Python libraries were used throughout the project:

**Pandas**

Pandas was used for structured data manipulation and log analysis. Authentication datasets exported from Microsoft Sentinel were processed using Pandas DataFrames, allowing efficient filtering, transformation, and aggregation of large volumes of authentication records.

Key operations included:

• Log parsing and dataset cleaning  
• Timestamp conversion and temporal sorting  
• Feature generation from authentication events  
• Aggregation of behavioural activity metrics  

---

**NumPy**

NumPy was used to support numerical operations and statistical calculations required for behavioural feature engineering and anomaly detection modelling.

---

**Scikit-learn**

Scikit-learn provided the machine learning framework used to implement anomaly detection algorithms and behavioural modelling techniques applied to the authentication dataset.

These models were used to analyse deviations from normal login behaviour and identify potential anomalous activity patterns.

---

**Matplotlib and Data Visualisation Tools**

Visualisation tools were used to analyse authentication behaviour patterns and assist in identifying anomalies within login activity. Visual inspection of authentication trends helped support the interpretation of model outputs and behavioural detection results.

---

### Development Environment

**Jupyter Notebook**

All analytical workflows were developed within Jupyter Notebook environments. This allowed the project to combine code execution, data exploration, visualisation, and documentation within a single research workflow.

The notebook-based workflow also enabled step-by-step development of the detection pipeline, including preprocessing, feature engineering, anomaly detection modelling, and attack simulation experiments.

---

### Dataset Infrastructure

The datasets used within this project consist of enriched authentication telemetry derived from Microsoft Sentinel log exports.

Key datasets include:

• Enriched SigninLogs authentication datasets  
• Behaviourally engineered login datasets  
• Simulated attack datasets used for model validation  

These datasets formed the foundation for behavioural modelling and threat detection experiments conducted throughout the project.

---

---

## Technology Stack and Analytical Environment

The threat detection framework developed in this project integrates SIEM telemetry analysis with data science and machine learning techniques. The system was implemented using a combination of security monitoring technologies and Python-based analytical tools designed to process, analyse, and model authentication behaviour within large volumes of SIEM log data.

The analytical workflow was constructed to simulate a realistic security analytics environment similar to those used within modern Security Operations Centres (SOCs).

---

### Security Monitoring Platform

**Microsoft Sentinel (SIEM Platform)**

Microsoft Sentinel was used as the primary Security Information and Event Management (SIEM) platform within this project. Sentinel provides large-scale log ingestion, security telemetry aggregation, and advanced monitoring capabilities across identity infrastructure and cloud environments.

Authentication telemetry analysed within this project was derived from **Azure Active Directory SigninLogs**, which capture detailed records of authentication events occurring across users, devices, and network locations.

These logs provide critical visibility into authentication behaviour and are widely used within enterprise SOC environments for monitoring identity-based threats such as credential misuse and account compromise.

---

### Data Analysis Environment

**Python Data Science Ecosystem**

All log analysis, preprocessing, feature engineering, and anomaly detection modelling were implemented using Python within a Jupyter Notebook environment. This environment enabled iterative data exploration, behavioural modelling, and machine learning experimentation across large authentication datasets.

The Python data science ecosystem provided flexible tools for analysing SIEM telemetry and constructing behavioural detection models.

---

### Core Python Libraries

The following Python libraries were used throughout the project:

**Pandas**

Pandas was used for structured data manipulation and log analysis. Authentication datasets exported from Microsoft Sentinel were processed using Pandas DataFrames, allowing efficient filtering, transformation, and aggregation of large volumes of authentication records.

Key operations included:

• Log parsing and dataset cleaning  
• Timestamp conversion and temporal sorting  
• Feature generation from authentication events  
• Aggregation of behavioural activity metrics  

---

**NumPy**

NumPy was used to support numerical operations and statistical calculations required for behavioural feature engineering and anomaly detection modelling.

---

**Scikit-learn**

Scikit-learn provided the machine learning framework used to implement anomaly detection algorithms and behavioural modelling techniques applied to the authentication dataset.

These models were used to analyse deviations from normal login behaviour and identify potential anomalous activity patterns.

---

**Matplotlib and Data Visualisation Tools**

Visualisation tools were used to analyse authentication behaviour patterns and assist in identifying anomalies within login activity. Visual inspection of authentication trends helped support the interpretation of model outputs and behavioural detection results.

---

### Development Environment

**Jupyter Notebook**

All analytical workflows were developed within Jupyter Notebook environments. This allowed the project to combine code execution, data exploration, visualisation, and documentation within a single research workflow.

The notebook-based workflow also enabled step-by-step development of the detection pipeline, including preprocessing, feature engineering, anomaly detection modelling, and attack simulation experiments.

---

### Dataset Infrastructure

The datasets used within this project consist of enriched authentication telemetry derived from Microsoft Sentinel log exports.

Key datasets include:

• Enriched SigninLogs authentication datasets  
• Behaviourally engineered login datasets  
• Simulated attack datasets used for model validation  

These datasets formed the foundation for behavioural modelling and threat detection experiments conducted throughout the project.

---

---

## Anomaly Detection and Threat Modelling

Following the construction of behavioural indicators from the authentication dataset, anomaly detection techniques were applied in order to identify authentication events that deviate significantly from established behavioural patterns.

The objective of this stage was to determine whether statistical and machine learning methods could successfully identify suspicious authentication behaviour within SIEM telemetry without relying solely on predefined detection rules.

Rather than searching for known attack signatures, anomaly detection focuses on identifying events that fall outside normal behavioural distributions. Within authentication datasets, such deviations may represent compromised accounts, automated login attempts, credential misuse, or other forms of abnormal access activity.

The anomaly detection framework therefore evaluates authentication behaviour relative to behavioural baselines derived during the feature engineering stage.

---

### Behavioural Anomaly Detection Approach

The anomaly detection strategy implemented in this project is based on the principle that legitimate user behaviour tends to follow relatively stable patterns over time. When authentication behaviour deviates significantly from these patterns, the activity may represent a potential security risk.

Behavioural anomaly detection therefore involves three primary steps:

• Constructing behavioural baselines from historical authentication activity  
• Measuring deviations between observed activity and expected behaviour  
• Flagging statistically unusual activity patterns for further analysis  

This approach allows the detection system to highlight suspicious events that would be difficult to identify using static rule-based detection mechanisms alone.

---

### Statistical Anomaly Identification

Statistical analysis techniques were first used to identify unusual behavioural patterns within the authentication dataset.

By analysing the distribution of behavioural features such as login frequency and session timing, the system can identify authentication events that fall outside normal statistical ranges.

Examples of statistical indicators used during anomaly detection include:

• Authentication events occurring far outside normal login timing distributions  
• Abnormally short session intervals between authentication attempts  
• Unusual spikes in login activity associated with specific user accounts  

These statistical deviations provide early indicators of potentially suspicious authentication behaviour.

---

### Machine Learning Based Detection

In addition to statistical analysis, machine learning techniques were applied to model authentication behaviour and identify anomalies within the dataset.

Machine learning models are particularly well suited to behavioural analysis because they can analyse complex relationships between multiple behavioural features simultaneously.

Within this project, the anomaly detection models evaluate behavioural indicators such as:

• login frequency patterns  
• session timing behaviour  
• authentication event clustering  
• temporal login distributions  

By analysing these behavioural signals together, the model can identify authentication events that differ significantly from expected user behaviour patterns.

Events that exhibit strong behavioural deviations are flagged as potential anomalies requiring further investigation.

---

### Behavioural Outlier Detection

The output of the anomaly detection stage consists of authentication events identified as behavioural outliers within the dataset.

These outliers represent login activity that deviates from established behavioural baselines and may indicate suspicious authentication behaviour.

Examples of behavioural outliers may include:

• unusually rapid authentication attempts within short time intervals  
• login behaviour occurring at highly irregular times  
• sudden increases in authentication frequency for a given account  
• authentication activity inconsistent with historical user behaviour  

While not all anomalies represent malicious activity, behavioural outlier detection provides an effective mechanism for identifying events that warrant further security investigation.

---

### Detection Interpretation

The anomalies identified by the detection models were analysed in order to determine whether they represented realistic threat scenarios.

This analysis considered the broader behavioural context surrounding flagged authentication events, including user activity patterns and session behaviour.

Through this evaluation process, the project demonstrates how anomaly detection techniques can assist Security Operations Centres by highlighting suspicious authentication behaviour hidden within large volumes of SIEM telemetry.

---

---

## Attack Simulation and Detection Validation

In order to evaluate the effectiveness of the behavioural anomaly detection framework, simulated malicious authentication activity was introduced into the dataset. This stage of the project was designed to test whether the detection pipeline could successfully identify abnormal login behaviour representing realistic attack scenarios.

Testing detection systems using simulated adversarial behaviour is an important step in validating cybersecurity analytics models. Without such validation, it is difficult to determine whether anomaly detection results represent meaningful security signals or simply statistical irregularities.

The attack simulation stage therefore introduces controlled authentication anomalies into the dataset and evaluates whether the detection models successfully flag these events as behavioural outliers.

---

### Purpose of Attack Simulation

The primary objective of the attack simulation stage is to evaluate the detection system under conditions that resemble real-world security threats.

Specifically, the simulation stage aims to:

• introduce abnormal authentication patterns into the dataset  
• replicate behavioural characteristics associated with malicious login attempts  
• evaluate whether anomaly detection models successfully identify these events  
• analyse how detection results correspond to simulated threat scenarios  

This validation step demonstrates whether the behavioural detection framework can successfully detect suspicious authentication activity within SIEM telemetry.

---

### Simulated Authentication Attack Patterns

Several forms of suspicious authentication behaviour were simulated in order to test the detection system. These patterns represent behaviours commonly observed during credential-based attacks targeting enterprise identity systems.

Examples of simulated attack patterns include:

• rapid repeated login attempts within short time intervals  
• abnormal spikes in authentication frequency  
• authentication activity occurring at unusual times  
• irregular session timing behaviour inconsistent with normal user activity  

By introducing these abnormal behavioural patterns into the dataset, the system can be tested against realistic authentication attack scenarios.

---

### Dataset Injection Process

Simulated attack events were inserted into the enriched authentication dataset used during behavioural modelling. These events were designed to produce abnormal feature values within the engineered behavioural indicators, such as unusually small session gaps or sudden spikes in login frequency.

Once the modified dataset was created, the anomaly detection pipeline was executed on the full dataset, allowing the models to analyse both normal and simulated malicious authentication behaviour.

This process allowed the project to evaluate whether the detection system could successfully distinguish anomalous activity from legitimate authentication patterns.

---

### Detection Evaluation

Following the injection of simulated attack behaviour, the anomaly detection models were used to analyse the authentication dataset and identify behavioural outliers.

Detection results were then examined to determine whether the simulated attack events were successfully flagged as anomalous authentication behaviour.

This evaluation stage demonstrates how behavioural analytics can identify suspicious login activity that deviates significantly from expected user behaviour patterns.

---

### Security Analytics Implications

The results of the attack simulation demonstrate the potential value of behavioural anomaly detection within SIEM environments. By analysing deviations in authentication behaviour rather than relying exclusively on static detection rules, the system is capable of identifying suspicious activity patterns that may otherwise remain hidden within large volumes of log data.

This approach reflects the growing role of behavioural analytics and machine learning within modern Security Operations Centres, where analysts increasingly rely on advanced detection techniques to identify subtle indicators of compromise within enterprise telemetry.

---
---

## Detection Results and Analytical Findings

Following the construction of behavioural indicators and the application of anomaly detection models, the authentication dataset was analysed to identify behavioural outliers that deviated significantly from normal user activity patterns.

The objective of this stage was to determine whether the behavioural modelling and anomaly detection framework could successfully identify authentication events that exhibited unusual characteristics when compared to the broader dataset.

The results demonstrate how behavioural analysis of SIEM authentication telemetry can reveal suspicious activity patterns that may otherwise remain hidden within large volumes of log data.

---

### Identification of Behavioural Anomalies

The anomaly detection models identified a subset of authentication events that deviated significantly from established behavioural baselines. These anomalies were identified through analysis of engineered behavioural indicators such as session timing patterns, login frequency metrics, and temporal access behaviour.

Authentication events flagged by the detection system exhibited characteristics including:

• unusually rapid sequences of authentication attempts  
• abnormal session intervals between login events  
• sudden increases in login activity for specific user accounts  
• authentication behaviour occurring outside typical temporal patterns  

These deviations represent behavioural outliers that may indicate suspicious authentication activity.

---

### Behavioural Pattern Analysis

Further analysis of detected anomalies revealed that abnormal authentication activity often manifests as deviations across multiple behavioural indicators simultaneously.

For example, certain flagged authentication events displayed a combination of:

• extremely short session gaps between login attempts  
• unusually high login frequency within short time intervals  
• temporal access behaviour inconsistent with historical user activity  

Such combinations of behavioural deviations strengthen the likelihood that the detected events represent suspicious activity rather than normal user behaviour.

---

### Detection of Simulated Attack Behaviour

The detection system was also evaluated using datasets containing simulated authentication attack patterns introduced during the attack simulation stage.

Analysis of the detection outputs indicated that many of the injected anomalous authentication events were successfully identified as behavioural outliers by the anomaly detection models.

These results demonstrate that behavioural detection techniques can successfully highlight authentication activity patterns consistent with simulated attack scenarios.

---

### Analytical Insights

The findings from the anomaly detection experiments highlight several important observations regarding authentication behaviour within SIEM telemetry datasets.

First, legitimate user authentication behaviour tends to exhibit relatively stable patterns over time, particularly in terms of login timing and frequency. This stability allows behavioural baselines to be constructed with reasonable reliability.

Second, anomalous authentication behaviour often appears as sudden deviations from these established patterns, particularly in the form of rapid login attempts or irregular access timing.

Finally, behavioural anomaly detection provides an effective mechanism for identifying suspicious authentication activity that may not trigger traditional rule-based detection alerts.

---

### Implications for Security Monitoring

The results of this project demonstrate how behavioural analytics and machine learning techniques can enhance threat detection capabilities within SIEM environments.

By analysing deviations from normal authentication behaviour, security monitoring systems can highlight suspicious activity patterns that may represent potential indicators of compromise.

Such techniques can complement traditional rule-based detection approaches and provide Security Operations Centres with additional analytical tools for identifying emerging threats within enterprise authentication telemetry.

---
