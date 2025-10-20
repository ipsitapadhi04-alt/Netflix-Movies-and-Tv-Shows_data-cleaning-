# Netflix-Movies-and-Tv-Shows_data-cleaning-
In this project, I analyzed the Netflix Movies and TV Shows dataset to perform end-to-end data cleaning and preprocessing using Python and Pandas. The objective was to convert a raw dataset—containing missing values, duplicates, inconsistent data types, and unstructured text—into a clean, well-formatted, and analysis-ready dataset.

This repository showcases my step-by-step workflow executed in Google Colab, where I applied structured data transformation techniques to refine over 8,800 records for further analysis and visualization.

🧭 Steps Performed
1️⃣ Loading the Data

Imported the dataset (.csv) into Google Colab using files.upload()
Loaded it into a pandas DataFrame using pd.read_csv()
Verified basic structure using df.info() and df.head()

2️⃣ Handling Missing and Duplicate Data

Checked for missing values and dropped unwanted or null records
Removed duplicate entries to maintain data integrity

3️⃣ Data Type Conversion

Converted date_added to proper datetime format using:
df['date_added'] = pd.to_datetime(df['date_added'], errors='coerce')


Converted release_year to a datetime (year-only) format:
df['release_year'] = pd.to_datetime(df['release_year'], format='%Y', errors='coerce')

4️⃣ Renaming Columns

Standardized column names to clean, consistent, and analysis-friendly versions:
df.columns = df.columns.str.lower().str.strip().str.replace(' ', '_').str.replace('-', '_')


📊** Result Summary**

Metric	Value
Rows (after cleaning)	5,332
Columns	12
Date Columns	date_added, release_year
Clean Naming	✅ All lowercase, underscore-separated
Missing Values	Removed/Handled

🚀 Next Steps
Handle missing categorical values (e.g., director, country)
Explore data through EDA — trends by year, content type, and country
Visualize insights using Matplotlib / Seaborn / Power BI

💡 Tools Used
Python
Pandas (Excel can also be used)
Google Colab
