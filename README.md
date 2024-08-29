# PhishInsightX
This repo is the research study behind the phishing detection model and techniques for evasion by attackers.

### PhishIntention by lindsey98
    https://github.com/lindsey98/PhishIntention

### **1. Experiment Dataset**

- **[25K Benign Webpage Dataset](https://drive.google.com/file/d/1ymkGrDT8LpTmohOOOnA2yjhEny1XYenj/view) + [25K CRP Phishing Webpage Dataset](https://drive.google.com/file/d/12ypEMPRQ43zGRqHGut0Esq2z5en0DH4g/view):**
  - **Source:** Phishpedia dataset (filtered to include only CRP websites).
  - **Purpose:** Used to train models for distinguishing between benign and CRP phishing websites. These datasets form the core of the phishing detection experiment by providing balanced samples from both categories.
  - **Reference:** See Table 1 of the Phishpedia dataset.

- **[3049 Misleading Legitimacy Dataset](https://drive.google.com/file/d/1xmB_P6I9BwnNYGJb7yeN-o2A1fMlX3Oh/view):**
  - **Source:** Collected in one week (from Apr 9, 2021, to Apr 16, 2021) from Alexa top30k - top50k, with human verification based on 3 conditions defined in Section 9.1.
  - **Purpose:** This dataset is used to evaluate the model's robustness against adversarial attacks by attempting to make phishing pages appear legitimate.

### **2. CRP Transition Locator (Hybrid) Evaluation Set**

- **[3310 Phishing Non-CRP Webpage Dataset](https://drive.google.com/drive/folders/1n8-tTOThFUaSw89TY1-CWmexKx3wPaH9):**
  - **Source:** Phishpedia dataset (non-CRP pages sampled).
  - **Purpose:** Used to evaluate the CRP transition locator by testing it on phishing pages that do not contain CRPs.
  - **Reference:** See Table 1 of the Phishpedia dataset.

- **[1003 Wild Benign Non-CRP Webpage Dataset](https://drive.google.com/file/d/1TeSUMr_GOeHbm_HrBmaOLbUflqzp1smk/view):**
  - **Source:** Main pages collected online from 1k well-known brands.
  - **Purpose:** Used to test the CRP transition locator on benign pages without CRPs.

### **3. CRP Transition Detector (Deep Learning Part)**

- **[1210 Test Set](https://drive.google.com/drive/folders/1CQbhX0xab2QW1TfROmmmtgqmiuC_yHTI):** (445 non-CRP phishing pages + 765 non-CRP benign pages)
  - **Source:** Sampled from Phishpedia dataset.
  - **Purpose:** Used as a test set for evaluating the deep learning-based CRP transition detector.

- **[4843 Training Set](https://drive.google.com/drive/folders/1CQbhX0xab2QW1TfROmmmtgqmiuC_yHTI):** (1774 non-CRP phishing pages + 3069 non-CRP benign pages)
  - **Source:** Sampled from Phishpedia dataset.
  - **Purpose:** Used as a training set for the CRP transition detector.

- **[10K Pre-Training Set](https://drive.google.com/drive/folders/1bUU5jIv3Zq8UEIswLFUVMDxN43zQmeLk):**
  - **Source:** 10k websites with pasted CRP buttons, all from benign websites, with some data repeated due to different CRP button placements.
  - **Purpose:** Used for pre-training the CRP transition detector.

### **4. CRP Classifier and AWL Detector**

- **[901 Test Set](https://drive.google.com/drive/folders/1HYiNBIGpBns4dqphRgiD2FF5F1WMG0RR):**
  - **Source:** Sampled from Phishpedia dataset.
  - **Purpose:** Used for testing the CRP classifier and AWL detector, labeled with layout and CRP class.

- **[8109 Training Set](https://drive.google.com/drive/folders/1HYiNBIGpBns4dqphRgiD2FF5F1WMG0RR):**
  - **Source:** Sampled from Phishpedia dataset.
  - **Purpose:** Used for training the CRP classifier and AWL detector, labeled with layout and CRP class.

### **5. OCR-Aided Siamese Model**

- **[2000 Test Set](https://drive.google.com/drive/folders/14-kxVSgq7f0NcVZ4UlHVvJxZXjduH_eV):**
  - **Source:** 2000 logos cropped from 1k benign and 1k phishing pages.
  - **Purpose:** Used to test the OCR-aided Siamese model's ability to recognize and match logos.

- **[3061 Training Set](https://drive.google.com/drive/folders/1IZu1yGnMm0uHC-3pMZBkdNTsk3H499V2):**
  - **Source:** Logo target list from the Phishpedia dataset, including 277 brand logos, also used in real deployment for reference logo matching.
  - **Purpose:** Used for training the OCR-aided Siamese model.

- **[167,140 Pre-Training Set](https://drive.google.com/drive/folders/1PTA24UTZcsnzXPN1gmV0_lRg3lMHqwp6):**
  - **Source:** Logo2k+ dataset from the AAAI'20 paper.
  - **Purpose:** Pre-training the OCR-aided Siamese model to enhance logo recognition and matching capabilities.

### Phishpedia by lindsey98
    https://github.com/lindsey98/Phishpedia
### **These model does not trained on any datasets but 30k phishing benchmark dataset, each website is annotated with its URL, HTML, screenshot, and target brand:**
   - **[Link](https://drive.google.com/file/d/12ypEMPRQ43zGRqHGut0Esq2z5en0DH4g/view)**
   - **[Targetlist Dataset 181 protected brands, Link to download](https://drive.google.com/file/d/1zxvXFKpLx816VfaGFISL6tod-zSEc6hY/view?usp=sharing)**
   - **[Phishing Dataset 29496 phishing sites, Link to download:](https://drive.google.com/file/d/12ypEMPRQ43zGRqHGut0Esq2z5en0DH4g/view?usp=sharing)**
   - **[Benign Dataset 30649 benign sites, Link to download:](https://drive.google.com/file/d/1yORUeSrF5vGcgxYrsCoqXcpOUHt-iHq_/view?usp=sharing)**
   - **[Labelled Logo Dataset 30649 benign dataset with ground-truth logo labels, Link to download:](https://drive.google.com/file/d/1yORUeSrF5vGcgxYrsCoqXcpOUHt-iHq_/view?usp=sharing)**
   - **[Link1](https://drive.google.com/file/d/1bH3Yp6K1B37B_sS_MNMz7yvYcOhOu-J8/view?usp=sharing)**
   - **[link2](https://drive.google.com/file/d/1u56I0IHBgM9glNJl2wcLfaihp1L_U7eD/view?usp=sharing)**

### Phishing_detection by Fafal-abnir
    https://github.com/fafal-abnir/phishing_detection
   - **[Dataset](https://github.com/fafal-abnir/phishing_detection/blob/master/dataset.csv)**
   - **[Extract Features from it](https://github.com/fafal-abnir/phishing_detection/blob/master/feature_extraction.py)**

### Phishing-Website-Detection-by-Machine-Learning-Techniques by shreyagopal
   - **1.Benign_list_big_final.csv: This file has list of legitimate urls. The total count is 35,300. The source of the dataset is University of New Brunswick, [(https://www.unb.ca/cic/datasets/url-2016.html.])**

   - 2.online-valid.csv: This file is downloaded from the opensource service called PhishTank. This service provide a set of phishing URLs in multiple formats like csv, json etc. that gets updated hourly. To download the latest data: https://www.phishtank.com/developer_info.php.

   - 3.legitimate.csv: This file has the extracted features of the 5000 legitimate URLs which are randonmly selected from the '1.Benign_list_big_final.csv' file.

   - 4.phishing.csv This file has the extracted features of the 5000 phishing URLs which are randonmly selected from the '2.online-valid.csv' file.

   - 5.urldata.csv This file is nothing but a combination of the above two files. It contains extracted features of 10,000 URLs both legitimate & phishing.
