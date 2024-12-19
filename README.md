# Student Study Insights - Case Study

# Overview
This project demonstrates my approach to analyzing lead data for an educational consultancy. The dataset and scenarios have been recreated for demonstration purposes and do not include any proprietary or confidential information.

# Dataset
The dataset consists of 8 columns:

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
### Analysis
In this case study, I conducted a thorough analysis of a dataset involving leads for an educational consultancy. My approach included:

### Data Cleaning and Preprocessing:
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

#### Descriptive Analysis:
##### Identify the top 3 common subject areas among disqualified leads
###### Top 3 Common Subject Areas:
1. Business & Management: A significant portion of leads are interested in business-related degrees.
2. Technology & Computing: There is strong interest in fields like computer science, software engineering, and data science.
3. Healthcare: Many leads are also pursuing healthcare-related courses such as nursing and medicine.

![image](https://github.com/user-attachments/assets/18a98154-8f1d-45d0-aa9d-19e7b2bcd54c)

##### Most common study destinations and courses of interest among these leads to identify potential patterns.
###### Most common study destinations
The most preferred destinations are Canada, UK, USA, France, and Ireland their global appeal for education and diverse program offerings.

![image](https://github.com/user-attachments/assets/bc7ff6d7-2281-4e73-89d9-a214234113a9)

Highlighted any missing or incomplete data that could be helpful for future analysis, such as specific demographic details or additional behavioral data points.
###### Additional data fields for analysis:
Lead Status/Qualification Reason: Adding a column that explains why a lead was disqualified can provide deeper insights into which factors are causing disqualifications. It can also help to tailor the marketing and lead qualification processes.
Education Level: Including current educational level would also help identify what certain academic backgrounds are more likely to be qualified leads.

#### Visualization:
The distribution of nationalities  states, showcasing the diversity of leads.

![image](https://github.com/user-attachments/assets/14e76e1d-875c-4557-a02c-d0cd297dafa6)

The distribution of states, showcasing the diversity of leads.

![image](https://github.com/user-attachments/assets/ad20766f-4be8-487b-8da5-7745f694fb2d)

Developed a heatmap to explore the relationship between nationality and courses of interest, providing insight into trends across different regions.

![image](https://github.com/user-attachments/assets/2805b6d3-23d1-4cf9-9739-ec20c57698ce)

