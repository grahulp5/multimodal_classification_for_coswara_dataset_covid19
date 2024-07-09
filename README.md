# multimodal_classification_for_coswara_dataset_covid19
This advanced Large Language Model (<i>LLM</i>) classification is one of its types that works with Audio and textual data (<i>metadata</i>) to classify available data into finding healthy vs unhealthy while taking other diseases and audio collected from Coswara into account.

The Github link and data link with the full article are below:
* Article (Coswara): [https://www.nature.com/articles/s41597-023-02266-0](https://www.nature.com/articles/s41597-023-02266-0)
* Github link: [https://github.com/iiscleap/Coswara-Data](https://github.com/iiscleap/Coswara-Data)

About the Project Coswara:
Project Coswara by the [Indian Institute of Science](https://www.iisc.ac.in/) (IISc) Bangalore attempts to build a diagnostic tool for COVID-19 based on respiratory, cough, and speech sounds. The project is in the data collection stage now. It requires the participants to provide a recording of breathing sounds, cough sounds, sustained phonation of vowel sounds, and a counting exercise which takes around 5-7 minutes of your time. No personally identifiable data is collected from the participants.
Coswara: A respiratory sounds and symptoms dataset for remote screening of SARS-CoV-2 infection

About the Coswara Dataset:

1.	The dataset contains diverse respiratory sounds and rich meta-data.
  * Timeframe: Recorded between April 2020 and February 2022 
  *	2635 individuals 
  *	1819 SARS-CoV-2 negative, 674 positives, and 142 recovered subjects

2.	The respiratory sounds contained nine sound categories associated with variants of breathing, cough, and speech. 
  *	These correspond to breathing (<i>breathing deep and breathing shallow</i>), cough (<i>coughing deep and coughing shallow</i>), sustained vowel phonation (<i>three different vowels</i>), and continuous speech (<i>counting from 1 to 20 at a normal and fast pace</i>).
  *	These sound recordings were released without the application of lossy compression standards.
  *	To validate the audio files that were collected using the crowd-sourced web link, the human annotators listened to all the sound recordings and marked the quality on a scale of 0–2 (<i>2 being the best quality and 0 being poor</i>). 
  *	Description of the sound categories in the Coswara dataset:

| Sound Category    | Collected Sound Sample | Description                                                    |
|-------------------|-------------------------|----------------------------------------------------------------|
| Breathing     | Breathing-shallow       | Few cycles of inspiration and expiration without exertion on the lungs |
|                   | Breathing-deep          | Few cycles of inspiration and expiration with exertion on the lungs    |
| Cough         | Cough-shallow           | Few bouts of (induced) cough without exertion on lungs                |
|                   | Cough-heavy             | Few bouts of (induced) cough with exertion on lungs                   |
| Vowel Phonation| Vowel-[u]               | Sustained phonation of vowel-[u] (as in the word boot)                |
|                   | Vowel-[i]               | Sustained phonation of vowel-[i] (as in the word beet)                |
|                   | Vowel-[æ]               | Sustained phonation of vowel-[æ] (as in the word bat)                 |
| Speech        | Counting-normal         | Counting numbers from 1 to 20 in normal pace                          |
|                   | Counting-fast           | Counting numbers from 1 to 20 at a fast pace                            |

 

3.	The rich metadata contained demographic information associated with age, gender, and geographic location, as well as health information relating to the symptoms, pre-existing respiratory ailments, comorbidity, and SARS-CoV-2 test status.
  *	Demographics data: The participants provided demographic information like age, gender, country, and location information in terms of province. Further, they also indicated whether they were proficient in English and whether they had a face mask during the recording. The smoking status was also recorded.
  *	Symptom data: Description of the meta-data collected and released as part of the Coswara dataset:
  [https://www.nature.com/articles/s41597-023-02266-0/tables/3](https://www.nature.com/articles/s41597-023-02266-0/tables/3)
  *	COVID-19 test status: The participants provided information on their COVID-19 status by classifying themselves into one of the three categories, namely, COVID-19 negative (non-COVID), positive (COVID), and recovered categories. If the participant belonged to a positive or recovered category, they further provided the date of the last COVID-19 test conducted and the kind of test (<i>RAT or RT-PCR</i>).

4.	This study is the first of its kind to manually annotate the audio quality of the entire dataset (<i>amounting to 65 hours</i>) through manual listening.

About the files:
1. There are 4 Files (<i>2 Python notebooks and 2 requirements files for each Python file</i>). The requirement files are the instructions on how to run the files.
2. The Data folder contains the required data for analysis. <code>Extracted_data</code> and <code>Labels</code> are required for <code>Multimodal_Classification.ipynb</code> that is Audio and the actual Multimodal code. <code>Metadata_analysis_data</code> is required for <code>Metadata_analysis.ipynb</code> which contains EDA and Machine Learning models on metadata (<i>text data</i>).
3. The requirements for the <code>Multimodal_Classification.ipynb</code> (<i>audio file</i>) is in <code>requirements_Multimodal_Classification.txt</code> and for the <code>Metadata_analysis.ipynb</code> (<i>text file</i>) is in <code>Requirements_info_metadata.docx</code>.
4. Additionally, information about metadata columns can be found in <code>data_description.xlsx</code>

About the results (<i>Inferences</i>):
1. A DenseNet201 Model with LSTM Model was utilized for audio data and a simple DenseNet model for metadata was combined to train the multimodal.
2. The results from the above model produced a 51% accuracy score.
3. Below is the classification report from the Multimodal:
   
| Class               | Precision | Recall | F1-Score | Support |
|---------------------|-----------|--------|----------|---------|
| neg_no_illness      | 0.6606    | 0.6792 | 0.6698   | 212     |
| neg_with_illness    | 0.2000    | 0.1778 | 0.1882   | 45      |
| pos_asymp_mild      | 0.3014    | 0.3492 | 0.3235   | 63      |
| pos_mod             | 0.1875    | 0.1111 | 0.1395   | 27      |
| **Accuracy**        |           |        | 0.5101   | 347     |
| **Macro Avg**       | 0.3374    | 0.3293 | 0.3303   | 347     |
| **Weighted Avg**    | 0.4988    | 0.5101 | 0.5032   | 347     |

4. The overall results provided good results and room for improvement for the model.

Contributors: You can tag [Rahul Gupta](https://www.linkedin.com/in/rahul-gupta-a31749166/) and [Cherielyn Caquilala](https://github.com/cheryeleen) as lead contributors to the Multimodal classification for this project.

Other citations:
Coswara - A Database of Breathing, Cough, and Voice Sounds for COVID-19 Diagnosis ([https://arxiv.org/abs/2005.10548](https://arxiv.org/abs/2005.10548))

