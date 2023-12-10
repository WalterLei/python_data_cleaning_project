# python_data_cleaning_project

Project Description
Data cleaning is an important skill for data engineers, encompassing reading, modifying, splitting, and storing data. These abilities are highly sought after by businesses worldwide and continue to grow in demand.

In this notebook, I will apply my data-cleaning skills to process information about marketing campaigns run by a bank.

I will demonstrat my skills to modify values, add new features, convert data types, and save data into multiple files.

You have been asked to work with a bank to clean the data they collected as part of a recent marketing campaign, which aimed to get customers to take out a personal loan. They plan to conduct more marketing campaigns going forward so would like you to ensure it conforms to the specific structure and data types that they specify so that they can then use the cleaned data you provide to set up a PostgreSQL database, which will store this campaign's data and allow data from future campaigns to be easily imported.

They have supplied you with a csv file called "bank_marketing.csv", which you will need to clean, reformat, and split the data, saving three final csv files. Specifically, the three files should have the names and contents as outlined below:

client.csv
column	data type	description	cleaning requirements
client_id	integer	Client ID	N/A
age	integer	Client's age in years	N/A
job	object	Client's type of job	Change "." to "_"
marital	object	Client's marital status	N/A
education	object	Client's level of education	Change "." to "_" and "unknown" to np.NaN
credit_default	bool	Whether the client's credit is in default	Convert to boolean data type
mortgage	bool	Whether the client has an existing mortgage (housing loan)	Convert to boolean data type

campaign.csv
column	data type	description	cleaning requirements
client_id	integer	Client ID	N/A
number_contacts	integer	Number of contact attempts to the client in the current campaign	N/A
contact_duration	integer	Last contact duration in seconds	N/A
previous_campaign_contacts	integer	Number of contact attempts to the client in the previous campaign	N/A
previous_outcome	bool	Outcome of the previous campaign	Convert to boolean data type
campaign_outcome	bool	Outcome of the current campaign	Convert to boolean data type
last_contact_date	datetime	Last date the client was contacted	Create from a combination of day, month, and a newly created year column (which should have a value of 2022);
Format = "YYYY-MM-DD"

economics.csv
column	data type	description	cleaning requirements
client_id	integer	Client ID	N/A
cons_price_idx	float	Consumer price index (monthly indicator)	N/A
euribor_three_months	float	Euro Interbank Offered Rate (euribor) three-month rate (daily indicator)	N/A

