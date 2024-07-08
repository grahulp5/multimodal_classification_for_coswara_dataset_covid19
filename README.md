# multimodal_classification_for_coswara_dataset_covid19
This advanced Large Language Model (LLM) classification is one of its types that works with Audio and textual data (metadata) to classify available data into finding healthy vs unhealthy while taking other diseases and audio collected from Coswara into account.

The Github link and data link with the full article are below:
Article (Coswara): [https://www.nature.com/articles/s41597-023-02266-0]([url](https://www.nature.com/articles/s41597-023-02266-0))
Github link: [https://github.com/iiscleap/Coswara-Data]([url](https://github.com/iiscleap/Coswara-Data))

About the Project Coswara:
Project Coswara by the [Indian Institute of Science]([url](https://www.iisc.ac.in/)) (IISc) Bangalore attempts to build a diagnostic tool for COVID-19 based on respiratory, cough, and speech sounds. The project is in the data collection stage now. It requires the participants to provide a recording of breathing sounds, cough sounds, sustained phonation of vowel sounds, and a counting exercise which takes around 5-7 minutes of your time. No personally identifiable data is collected from the participants.
Coswara: A respiratory sounds and symptoms dataset for remote screening of SARS-CoV-2 infection

Key points to remember about the Dataset:

1.	The dataset contains diverse respiratory sounds and rich meta-data.
  * Timeframe: Recorded between April 2020 and February 2022 
  *	2635 individuals 
  *	1819 SARS-CoV-2 negative, 674 positives, and 142 recovered subjects

2.	The respiratory sounds contained nine sound categories associated with variants of breathing, cough, and speech. 
  *	These correspond to breathing (breathing deep and breathing shallow), cough (coughing deep and coughing shallow), sustained vowel phonation (three different vowels), and continuous   speech (counting from 1 to 20 at a normal and fast pace).
  *	These sound recordings were released without the application of lossy compression standards.
  *	To validate the audio files that were collected using the crowd-sourced web link, the human annotators listened to all the sound recordings and marked the quality in a scale of 0–2. 
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
  https://www.nature.com/articles/s41597-023-02266-0/tables/3
  *	COVID-19 test status: The participants provided information on their COVID-19 status by classifying themselves into one of the three categories, namely, COVID-19 negative (non-COVID), positive (COVID), and recovered categories. If the participant belonged to a positive or recovered category, they further provided the date of the last COVID-19 test conducted and the kind of test (RAT or RT-PCR).

4.	This study is the first of its kind to manually annotate the audio quality of the entire dataset (amounting to 65 hours) through manual listening.

About the files:
1. There are 4 Files (2 Python notebooks and 2 requirements files for each Python file). The requirement files are the instructions on how to run the files.
2. 

