# BenefitCloud
Take home for data processing and pipelining.
Plan-name mapping approach:
For the plan name mappings of 19 unique plans to 6 standardized plans, I manually assigned each plan using a dictionary where the 19 unique were the keys and the 6 standard were the values. This was the most straighforward approach after much troubleshooting with creating mapping logic. 
Data-cleaning logic:
For the data cleaning I took a very iterative approach to ensuring each column fit the necessary standards. This involved making several addional columns to the dataframe for ease of use in intermediary processes. After generating the data the ssn were normalized using regex, the names concatenated, and new columns created for the new mapped plan names. 
NaN:
There were no unmapped rows or invalid data due to the synthetic data being perfect. I also verified that each plan name was mapped by counting all the NaN entries. In a real scenario I would fill missing data with suitable dummy data for pipelining and make note of it to revist the original data source.
Assumptions:
Due to the fake data library I used, the dates were already in the right format. Otherwise I would likely need the datetime library to standardize all date columns. I also used my own logic to decide what plan should map to what when the plan name is non-descriptive. Addiotionally I made assumptions on what the coverage levels should be. 
