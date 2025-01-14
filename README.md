# Student Study Insights - Case Study

# Overview
This project demonstrates my approach to analyzing lead data for an educational consultancy. The dataset and scenarios have been recreated for demonstration purposes and do not include any proprietary or confidential information.

# Dataset
The dataset consists of 8 columns and 4382 rows:

|Column        |Description |
| ---------- | ----------------------------------   | 
|Name                    |Identifier for each lead (anonymized) |
| Source                 | Source of the lead (e.g., online, referral) |
| Nationality            |Country of origin of the lead |
| Study                  | Type of study program |
| Destination            | Desired country for study |
| State/City of Domicile | Geographic location of the lead |
| Course(s) of Interest  | Academic courses the lead is interested in |
| Intake                 | Desired intake period for the study program |

# Business Requirements
The analysis addresses the following business questions:
### Descriptive Analysis
1. Identify the top 3 common subject areas among disqualified leads.
2. Highlight the most common study destinations and courses of interest among disqualified leads.
3. Identify additional data fields that could improve analysis.
   
### Visualization
1. Bar chart of the distribution of Nationalities (and states).
2. Heatmap showing the relationship between Nationalities and Courses of Interest.

### Insights
1. Identify one major trend in the data and discuss its potential business impact.
   
### Recommendations
1. Suggest one actionable strategy to reduce disqualified leads and improve overall lead quality.

# Analysis Section
In this case study, I conducted a thorough analysis of a dataset involving leads for an educational consultancy. My approach included:

## Data Cleaning and Preprocessing:
Upon importing the data into Power Query in Power BI, I identified several inconsistencies in the entries due to the survey responses. To ensure the data was clean and suitable for analysis, I performed the following steps:
#### Splitting Columns with Multiple Entries:
Columns such as "State/City of Domicile," "Destination," "Source," and "Course of Interest" contained multiple values in a single cell. I split these columns into individual ones to isolate each entry, making the dataset more manageable and analyzable.
#### Replacing and Filling Columns:
I replaced any missing or inconsistent entries in these columns with appropriate values, ensuring uniformity across the dataset.
#### Trimming Whitespace:
After splitting the columns, I applied trimming to remove any leading or trailing whitespace from the data. This helped to eliminate formatting inconsistencies that could impact the accuracy of future analyses.
#### Unpivoting:
To ensure the data was in a long format suitable for analysis, I unpivoted relevant columns, which transformed the dataset into a more analysis-friendly structure.
#### Removing Duplicates:
After cleaning and ensuring consistency across the columns, I removed duplicate rows to ensure the data was unique and didn’t skew analysis results.
#### Categorizing Courses of Interest & Source:
##### Courses of Interest 
To streamline the analysis, I added a custom column using M Code in Power Query to categorize the "Courses of Interest" into broader categories. For example:
1. Healthcare: Courses related to health, medicine, medical fields, and pharmacy.
2. Technology & Computing: Courses involving computer science, software, data, AI, IT, etc.
3. Business & Management: Courses like MBA, management, marketing, administration, etc.
This categorization enabled easier aggregation and analysis of trends across different subject areas.

![image](https://github.com/user-attachments/assets/53d3ea85-630b-4400-9f0d-4151f63d71af)

##### Source
Additionally, I categorized the "Source" field into broader groups based on the platform or origin of the leads:
1. Social media platforms such as LinkedIn, Twitter/X, Instagram, and YouTube were grouped under "Social Media."
2. Referrals from people like friends, family, brother, and mother were categorized under "Referral."
3. Paid Marketing: Sources such as "Paid Marketing", "Email", and "SMS" were grouped under the category "Paid Marketing" to simplify the analysis of marketing channels with paid efforts.
4. Web/Online: Sources like "Google" and "Web" were categorized under "Web/Online" to group online-related sources together.
5. Others: Any remaining sources that did not fit into the above categories were grouped under "Others" to avoid incomplete or ambiguous entries.
This helped identify patterns in how leads were generated and provided a clearer view of the data.

![image](https://github.com/user-attachments/assets/dca49166-a277-4a6c-a54b-f5f1796194d7)

### Descriptive Analysis:
- After cleaning and preparing the dataset for analysis; we have a total of  3395 leads
#### 1. Identify the top 3 common subject areas among disqualified leads
Among the categorised courses of interest, "Others" ranks the highest for disqualified leads followed by:
1. Business & Management: A significant portion of leads are interested in business-related degrees.
2. Technology & Computing: There is strong interest in fields like computer science, software engineering, and data science.
3. Healthcare: Many leads are also pursuing healthcare-related courses such as nursing and medicine.

![image](https://github.com/user-attachments/assets/18a98154-8f1d-45d0-aa9d-19e7b2bcd54c)

#### 2. Top 5 most common study destinations among these leads.
The most preferred destinations are Canada, UK, USA, France, and Ireland their global appeal for education and diverse program offerings.

![image](https://github.com/user-attachments/assets/09b71b78-d4e2-428e-a77c-785227e4be40)


#### 3. Top 5 nationalities across disqualified leads:
66% of disqualified leads are from Nigeria, highlighting a significant geographic trend. 
![image](https://github.com/user-attachments/assets/e00bb7a3-c8d8-45a2-92d0-8f47edeff4f0)


#### 4. Top 5 states across disqualified leads:
Lagos had the highest number of leads across the different states.

![image](https://github.com/user-attachments/assets/d31ccfa4-0beb-4c38-a1e2-c8286f60929c)

#### 5. An heatmap exploring the relationship between nationality and courses of interest, providing insight into trends across different regions.
The data reveals a significant distribution of course preferences among leads from Nigeria.
![image](https://github.com/user-attachments/assets/2805b6d3-23d1-4cf9-9739-ec20c57698ce)

#### 6. Intake
About 68% of the disqualified leads were looking at the Sep 24 and Jan 25 session
![image](https://github.com/user-attachments/assets/426dfcf3-8c63-4675-b3f8-ea5d4d4e1149)

#### 7. Top 5 Source of Information
Based on the insights gotten from the categrised data, majority of the leads came from various kinds of sources grouped under "Others" while a significant percentage came from "WakaDoctor" and "Social Media".
![image](https://github.com/user-attachments/assets/682dd6aa-27f1-4eb5-9d1b-5d6b7dafb2ea)

#### 8. Recommendations for Improving Data Collection and Analysis of Disqualified Leads:
Education Level:
- Including the current education level in the data collection process would help identify trends regarding which academic backgrounds are most often disqualified.This data can be used to tailor programme offerings and funding options to better suit leads with specific educational backgrounds, potentially reducing disqualification rates.
- Data Quality – Standardised Responses: Standardising the survey form by using dropdown options instead of free-text input would ensure more consistent and controlled responses.
For example, providing a predefined list of states for respondents to choose from can improve data accuracy and streamline analysis.
Controlled responses reduce errors during data processing and enhance the reliability of insights derived from the data.
- 

