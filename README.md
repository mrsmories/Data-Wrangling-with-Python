# Data-Wrangling-with-Python
Victoria Solutions Project Week 2

##Dataset 1:

Objective:  Use Python libraries such as pandas, numpy, and matplotlib to clean data formatting and structure and create visualizations to identify statistical outliers.

Method:  I used 2 different datasets for the project, the first following the example given by the project guidelines.  That example was a quite small dataset that I deliberately created with extra spaces, formatting errors, and duplicates.
	Step 1:  use method isna() to look for Null values in the data and the method .duplicated() to look for duplicate entries
	Step 2: Cleaning- strip data in all columns of extra white spaces.  Take the ‘Name’ column and make it Title case.  Fill the Null value in the ‘Age’ column with the median age from the set and drop the duplicate entry.  Also the values entered in the ‘Country’ column needed to be unified in format.

##Dataset 2 

Method:  Since the first dataset was so short, I wanted more in depth practice with data in that style of “customer data”.  Unfortunately the dataset I found did not present lots of opportunities for visualization or statistical analysis.  Some would have been possible but seemed unnecessary after looking at the data frame info.

The ‘Member ID’ column consisted of an email that came with inconsistencies.  Null values occurred in columns that had to do with the addresses for each member so that is the primary where some changes are made.

Step 1-Data Types:  All rows contained string values to begin with.  ‘Membership end date’ was put into date format for ease of future manipulations or calculations.  ‘Member type’ had only 6 different options for each member so that column was converted into category data for calculation speed.

Step 2-Clean String Data:  The email addresses used as ‘Member ID’s were cleaned of white spaces and cast as all lower case.  The ‘Last Name’ and ‘First Name’ columns were cleaned of white spaces and put in Title case.

tep 3-Clean Columns:   This dataset appears to be a concatenation of member data for the Global Logistics Assoc. as evidenced by the ‘New Address’ column.  ‘New Address’ is a concatenation of ‘Street’ and ‘Apt/Ste/Unit’.  All columns were stripped of white spaces and the columns ‘Street’ and ‘Apt/Ste/Unit/ were dropped.  ‘New Address’ was renamed to ‘Address’
For certain countries like the Netherlands the alphanumeric zip code was included inside the ‘City’ column before the city name.  Those characters were extracted and moved to ‘Zip Code’ to make the formatting uniform across all address columns
