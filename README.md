# Fifa-2021-Data-Cleaning

# Introduction
I participated in the data cleaning challenge on the Twitter space. This was an opportunity given to Data Analysts to improve on their data cleaning skill. My previous projects data were either clean or semi clean, that is the main reason why I participated in the #datacleaning challenge as this was a messy dataset. This was to improve on my cleaning skill and learn from others. 

# About the Data
The FIFA 21 dataset was gotten from the Kaggle website https://www.kaggle.com/datasets/yagunnersya/fifa-21-messy-raw-dataset-for-cleaning-exploring, It was a raw and messy csv data which contained 18979 rows and 77 columns. The dataset contained information about football players which included their IDs, Names, Height, Weight, best positions, Wages, Value and so on

# Data Transformation
Before the data was transformed, I noticed the data had special characters, I then changed the file Origin from Western European (Windows) to Unicode (UTF8) as seen below. Thereafter, I proceeded to transform the data.
![Before and After UTF-8](https://user-images.githubusercontent.com/128192166/226180938-4c8ee300-f25b-45f0-8df1-4389ce8381bc.PNG)

# Data Observation After Importing
1.	White Spaces
2.	Wrong data types
3.	Irrelevant data columns
4.	Incorrect values 
5.	Null Entries

# Data Cleaning Process
Power Query Editor was used for the data cleaning. After importing the data, the whitespaces were removed using the Trim function.
![white spaces](https://user-images.githubusercontent.com/128192166/226182364-7ad18141-ad2c-4f64-ab9c-d0ba4c25fbca.PNG)

 I started the data cleaning process from the first column to avoid omitting any column.
# ID Column
I changed the data type from whole number to text as IDs are unique and will not be used for calculation
![ID](https://user-images.githubusercontent.com/128192166/226182870-a94f1f0e-e695-4e6d-a454-6528b49a9961.PNG)

# Name Column
The names were correct except one which had special character as name initial. I used replace value function to change it to the correct initial
![Name](https://user-images.githubusercontent.com/128192166/226183814-1201e4f8-7b17-43c6-849b-c6b7ca9ff5c9.PNG)

# PhotoUrl and PlayerUrl Columns
Both columns were removed as they are Metadata. Metadata gives information about other Data, these were informations I already had.
![image](https://user-images.githubusercontent.com/128192166/226183966-0dec5177-905f-4e5d-8e92-a8916cdfdd88.png)

# Overall And Potential Rating Columns
Both column data types were changed to percentage (%) as required by the data dictionary and the names were written out in full for better understanding.

![OVA](https://user-images.githubusercontent.com/128192166/226184308-f94d71d8-56fd-45f8-bc87-216e791d8ecc.PNG)

# Contract Column
On the raw data there were different contract which were ungrouped. I created a new column(Agreement) and grouped the contracts accordingly. I also separated the start and end dates. The Contract duration was also calculated.
![Contract](https://user-images.githubusercontent.com/128192166/226185544-fd1207f0-01d5-4913-8035-f168bb453ebf.PNG)

# Height Column
The measurement for the height in the raw data were in cm, feet and inches, they needed to be in the same measurement which is cm. I first converted the feet to inches (feet*12 = Inches), added both inches together before converting to cm (0.393701*inch = cm).
![Height](https://user-images.githubusercontent.com/128192166/226185685-2115a1ef-dd3d-4a86-81ff-471992e98279.PNG)

# Weight Column
The measurements for weight were inially in kg and lbs. I converted kg to lbs to have a uniform measurement.
![weight](https://user-images.githubusercontent.com/128192166/226185818-8445b07f-8a21-40e7-a8bd-482457c50e01.PNG)

# Value, Wages and Release Clause Columns
The M and K were replaced with 1000000 and 1000 respectively, € was removed and data type was changed to currency $

![value before](https://user-images.githubusercontent.com/128192166/226186560-103dfcfd-94fd-4a33-bb83-dc2dbf0397ec.PNG)
![Value After](https://user-images.githubusercontent.com/128192166/226186576-82d15e79-79c2-4e80-926b-48b38419f891.PNG)


# W/F, SM and IR Columns
The special character (★) was removed, the abbreviated headings were written out in full for better understanding. The data type was changed from text to whole number to aid calculation during visualisation.

![SM before](https://user-images.githubusercontent.com/128192166/226186778-5ded53c2-6a58-40d5-a312-ffe23adeac2e.PNG)
![SM After](https://user-images.githubusercontent.com/128192166/226186812-00e798bf-4224-4798-a413-92a0a3ebbd58.PNG)

# Hits
This column had some values that ended with K, they were replaced with 1000 using multiplication.

![Hits](https://user-images.githubusercontent.com/128192166/226186938-ae9e4710-7dd6-4faf-80eb-80579a2de3c0.PNG)


Other columns that were not mentioned above were all clean. The data was closed and loaded in Excel after cleaning.
![image](https://user-images.githubusercontent.com/128192166/226186992-51283558-43bb-4a28-a310-83473b2e5f0a.png)

# Conclusion
Participating in this challenge has really improved my data cleaning skill because before a reliable visualisation is generated, the data cleaning has to be accurate.

I am open to reviews.








