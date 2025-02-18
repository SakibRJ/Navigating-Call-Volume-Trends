# Navigating Call Volume Trends: Uncovering Patterns & Progression


## Project Description
Customer Experience (CX) Analytics is a process that allows businesses to understand their customers' interactions and experiences with their products or services. It involves the collection, analysis, and interpretation of customer data to gain insights into customer behavior, preferences, and expectations. This data-driven approach helps businesses improve their customer service, enhance their product offerings, and make informed business decisions.

This project explores the domain of Customer Experience (CX) analytics, with a particular emphasis on the inbound calling team within an organization. The dataset spans a period of 23 days and includes various attributes such as the agent’s name and ID, queue time (the duration a customer waits before connecting with an agent), call time, call duration, and call status (whether the call was abandoned, answered, or transferred). The objective is to conduct a comprehensive analysis of CX patterns, with a focus on the inbound calling team, in order to achieve the outlined goals and enhance the overall customer experience, ultimately fostering customer loyalty and advocacy for the business.



###  Objectives
- Manpower Planning: Propose a plan for manpower allocation during each time bucket (from 9 am to 9 pm) to reduce the abandon rate to 10%.

- Night Shift Manpower Planning: Assuming that for every 100 calls that customers make between 9 am and 9 pm, they also make 30 calls at night between 9 pm and 9 am. Propose a manpower plan for each time bucket throughout the Night, keeping the maximum abandon rate at 10%.

- Average Call Duration: Determining the average duration of all incoming calls received by agents for each time bucket.

- Call Volume Analysis: Total number of calls received for each time bucket/each hour.


#### Assumptions Available for Adoption: An agent works for 6 days a week; On average, each agent takes 4 unplanned leaves per month; An agent's total working hours are 9 hours, out of which 1.5 hours are spent on lunch and snacks in the office. On average, an agent spends 60% of their total actual working hours (i.e., 60% of 7.5 hours) on calls with customers/users. The total number of days in a month is 30.
![Image](https://github.com/user-attachments/assets/4d6b6fe0-e911-45ba-ad15-53d5ccfffac4)

#### *For a more detailed and in-depth overview of the business objectives, please refer to the 'Business_Req_Document_Call_Volume.docx 


### Approach/Steps followed 
#### Analysis:
Understanding the data & planning accordingly. Additionally, the most important staep i.e., Data cleaning and preparing the data.

- No of rows: 1,17,988
- No of Columns: 13
- Cells containing N/A = 34,198 in Agent_name; N/A= 34,198 in Agent_id
- No of blank Cells: wrapped_by columns = 47,877.
#### 34198 N/A cells in Agent_Name, Agent_id Column along with Wrapped_by column having blanks were replaced by “Abondaned_Call” tag (As the Call_Status Column indicated.)
- Recognize the feature of the dataset using Descriptive Statistics
#### Remaining 13679 cells in wrapped by column were replaced by Statistical Descriptive Values (Mode) that happend to be 'Agent'
![Image](https://github.com/user-attachments/assets/25ec5ced-ee6b-435f-bbdc-04c7f1a2692c)







2. Insights: Analysing the data to extract meaningful insights.
3. Visualization: Visualizing key factors for clear and concise communication.
4. Conclusion: Drawing conclusions with key highlights of data patterns and trends.


