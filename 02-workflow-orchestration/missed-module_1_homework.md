
Questions
Question 1. Data Loading
Once the dataset is loaded, what's the shape of the data?

266,855 rows x 20 columns

I kept 19 columns because I dropped 'ehail_fee'

output.shape

Question 2. Data Transformation
Upon filtering the dataset where the passenger count is greater than 0 and the trip distance is greater than zero, how many rows are left?

139,370 rows

data.shape[0]

Question 3. Data Transformation
Which of the following creates a new column lpep_pickup_date by converting lpep_pickup_datetime to a date?

data['lpep_pickup_date'] = data['lpep_pickup_datetime'].dt.date

Question 4. Data Transformation
What are the existing values of VendorID in the dataset?

1 or 2

print(data["vendor_id"].unique())

Question 5. Data Transformation
How many columns need to be renamed to snake case?

4
data.rename(columns = {'VendorID': "vendor_id",  'RatecodeID': 'ratecode_id', 'PULocationID': 'pu_location_id', 'DOLocationID':'do_location_id'}, inplace=True)


Question 6. Data Exporting
Once exported, how many partitions (folders) are present in Google Cloud?

96

gsutil ls gs://proven-catcher-411305-mago-demo/gtd_2020_final_qtr_partition_by_date |wc  -l


