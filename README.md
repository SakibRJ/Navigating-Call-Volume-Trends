# Navigating Call Volume Trends: Uncovering Patterns & Progression


## Project Description
Customer Experience (CX) Analytics is a process that allows businesses to understand their customers' interactions and experiences with their products or services. It involves the collection, analysis, and interpretation of customer data to gain insights into customer behaviour, preferences, and expectations. This data-driven approach helps businesses improve their customer service, enhance their product offerings, and make informed business decisions.

This project explores the domain of Customer Experience (CX) analytics, with a particular emphasis on the inbound calling team within an organization. The dataset spans a period of 23 days and includes various attributes such as the agent’s name and ID, queue time (the duration a customer waits before connecting with an agent), call time, call duration, and call status (whether the call was abandoned, answered, or transferred). The objective is to conduct a comprehensive analysis of CX patterns, with a focus on the inbound calling team, in order to achieve the outlined goals and enhance the overall customer experience, ultimately fostering customer loyalty and advocacy for the business.



###  Objectives
- Average Call Duration: Determining the average duration of all incoming calls received by agents for each time bucket.

- Call Volume Analysis: Total number of calls received for each time bucket/each hour.

- Manpower Planning: Propose a plan for manpower allocation during each time bucket (from 9 am to 9 pm) to reduce the abandon rate to 10%.

- Night Shift Manpower Planning: Assuming that for every 100 calls that customers make between 9 am and 9 pm, they also make 30 calls at night between 9 pm and 9 am. Propose a manpower plan for each time bucket throughout the Night, keeping the maximum abandon rate at 10%.



#### Assumptions Available for Adoption: An agent works for 6 days a week; On average, each agent takes 4 unplanned leaves per month; An agent's total working hours are 9 hours, out of which 1.5 hours are spent on lunch and snacks in the office. On average, an agent spends 60% of their total actual working hours (i.e., 60% of 7.5 hours) on calls with customers/users. The total number of days in a month is 30.
![Image](https://github.com/user-attachments/assets/4d6b6fe0-e911-45ba-ad15-53d5ccfffac4)

#### *For a more detailed and in-depth overview of the business objectives, please refer to the 'Business_Req_Document_Call_Volume.docx 


### Approach/Steps followed 
#### #Understanding the data & planning accordingly. Additionally, the most important step i.e., Data cleaning and preparing the data:

- No of rows: 1,17,988
- No of Columns: 13
- Cells containing N/A = 34,198 in Agent_name; N/A= 34,198 in Agent_id
- No of blank Cells: wrapped_by columns = 47,877.
#### 34198 N/A cells in Agent_Name, Agent_id Column along with Wrapped_by column having blanks were replaced by “Abondaned_Call” tag (As the Call_Status Column indicated.)
- Recognize the feature of the dataset using Descriptive Statistics
#### Remaining 13679 cells in wrapped by column were replaced by Statistical Descriptive Values (Mode) that happend to be 'Agent'
![Image](https://github.com/user-attachments/assets/25ec5ced-ee6b-435f-bbdc-04c7f1a2692c)

#### #Insights: Analysing the data to extract meaningful insights and Visualizing key factors for clear and concise communication.

- Average Call Duration:
Simply created a Pivot table that shows the time bucket and Call_duration in Seconds (Average).
Added a filter to the Pivot containing only Answered + Transferred Calls (Transferred calls are again Answered Calls before being transferred).

Output:

![Image](https://github.com/user-attachments/assets/783d68e8-0137-4139-a075-fdd661421211)

![Image](https://github.com/user-attachments/assets/15f92e98-e075-4ced-a316-5c3f0c2549ec)

Key Observations from the Bar Graph:

#The average call duration of a call is 197 seconds.

#The progress moves much faster during 12 to 3pm as the average time is reduced by 5-10secs.

#Moreover most of the agents are consuming almost similar amout of time to cater the cilent; this shows consistency among the agents throughout the day.

- Call Volume Analysis:
Plotted a pivot for this analysis where the 1st row contains time 'bucket' and the 2nd 'ringing' column count values.

Output:
![Image](https://github.com/user-attachments/assets/1a07f8ce-cd45-4a86-9700-2c1b53d93a36)

![Image](https://github.com/user-attachments/assets/fb63c08a-4aca-4514-9cbb-8ea6a855b08f)

Key Observations from the Bar Graph:

#Majority of the call are received from 10am to 12pm.

#While 11-12pm is the busiest hour for the day.

#A trend can be noticed in the call where initially the call volume is larger until 12pm and decreases gradually untill 9pm.

#8pm to 9pm is the hour where one can expect least amount of inbound calls

- Manpower Planning:
Basically we had had two task here:
1. Man power required 9am to 9pm
2. Reduce abandon call rate to 10%


From The BRD we had 'Assumptions Available for Adoption' from the same we managed to calculate the below data:

![Image](https://github.com/user-attachments/assets/5bf0a07f-832f-4a95-8cb8-5595f65f5857)


Later calculated Abondoned and Answered calls per time_bucket along with Grand total for 23 Days

![Image](https://github.com/user-attachments/assets/8c6f6159-5d77-4588-875d-40448bd59fe1)

From the above data we calculated data for 'Calls/day' (Mentioned below)

![Image](https://github.com/user-attachments/assets/b50f7b26-6c43-486c-bced-7cf895c17c9d)

#Total Calls/Day was calculated by dividing Grand_Total/23 days.

#Calls Answered/Day that have 10% tolerance; was calculated by 0.9*Total_Calls/Day.

#Agents or Man power required per day were calculated by Calls_Answered/Day(90%) / 18. (As each agent can handle 18 calls per hour.

#We then plotted a bar chart for our abandoned call rates and Man Power required for each time bucket.

Output:

![Image](https://github.com/user-attachments/assets/c63d01ca-26d8-4545-b38b-2e5e1153b751)

![Image](https://github.com/user-attachments/assets/8d256d88-7bef-4ea3-bdf8-5a1ec19b5dc2)

Key Observations:

#Our analysis reveals that the percentage of abandoned calls is notably higher in the early morning and late evening, which could be attributed to various factors.

#We observe that between 10 AM and 1 PM, a significant number of agents is required to handle client needs, as indicated by the previous graphs. For more info kindly refer the file 'MAIN_Call_Volume_Trend_Analysis.xlsx'.

### Note: Night shift manpower planning, along with a comparison of current and required resources to achieve 90% call coverage, has been outlined in the 'MAIN_Call_Volume_Trend_Analysis.xlsx.' Additionally, a comprehensive report titled 'MAIN_Call_Volume_Trend_Analysis_Report.pdf' has been uploaded, which presents an in-depth analysis of key insights, trends, and patterns observed in the data. The report also highlights actionable conclusions and recommendations for enhancing efficiency and customer experience. Please refer to these documents for a more thorough understanding of the CX analysis and to guide decision-making moving forward.


### #Key Findings and Insights: The key highlights of data patterns and trends are summarized below (More details on these can be found in the 'MAIN_Call_Volume_Trend_Analysis_Report.pdf').

- The average call duration with a client is 197 seconds, with most agents handling similar call durations, indicating consistency throughout the day.
- Calls are predominantly received between 10 am and 12 pm, with 11 am to 12 pm being the busiest hour.
- Each agent handles an average of 82 calls per day, equating to 18 calls per hour.
- Abandoned calls are more frequent in the early morning and late evening, which could be attributed to various factors.
- Night shift analysis indicates higher agent requirements during the first two hours, with a decline until 5 am, followed by a significant increase in demand after 5 am (refer to the Excel sheet for further details).
