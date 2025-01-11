# 🌍 Global Air Connectivity Data Pipeline

## ✈️ **Project Description**

The **Global Air Connectivity Data Pipeline** is a data integration project designed for a travel analytics startup. Its goal is to analyze global air links and better understand connectivity between airports worldwide.

Using **Talend Studio**, this pipeline automates the ingestion, cleaning, transformation, and enrichment of datasets on airports and air routes. The processed data is prepared for advanced analytics by storing it in a database or exporting it to CSV files.

---

## 🔑 **Key Features**
- **Data Ingestion**: Automates the import of raw datasets from public sources like GitHub.
- **Data Cleaning**: Handles missing data, removes unnecessary spaces, and validates critical fields.
- **Data Transformation**: Joins and enriches airport and route data to provide detailed insights.
- **Database Integration**: Loads the final output into a database for advanced analytics.
- **Environment Configuration**: Supports development, testing, and production environments via context variables.

---

## 🚀 **Pipeline Workflow**

### **1. Ingestion**
- Reads the raw datasets (`airports.dat` and `routes.dat`) using Talend Studio.
- Ensures data is correctly parsed and ready for processing.

### **2. Cleaning and Quality Checks**
- Filters rows with missing or invalid data (e.g., missing coordinates).
- Cleans text fields like `City` and `Country`.
- Outputs cleaned data to `Cleaned-Airports.csv` and rejected rows to `Rejected-Rows.csv`.

### **3. Transformation and Enrichment**
- Joins `Cleaned-Airports.csv` and `routes.dat` to enrich route data with airport details.
- Outputs enriched data to `Joined-Flights.csv`.

### **4. Database Integration**
- Loads the final enriched data into a database table called `flights_enriched`.
- Handles database errors gracefully with logging and error handling.

---

## 📂 **Project Structure**

```plaintext
├── jobs/
│   ├── Job_1_IngestFiles/        # Reads and verifies raw datasets
│   ├── Job_2_CleanData/          # Cleans and validates the airport data
│   ├── Job_3_TransformAndJoin/   # Enriches route data with airport details
│   ├── Job_4_LoadIntoDB/         # Loads data into a database
├── outputs/
│   ├── Cleaned-Airports.csv      # Cleaned airport data
│   ├── Rejected-Rows.csv         # Rows with invalid or missing values
│   ├── Joined-Flights.csv        # Final enriched route data
├── LICENSE                       # MIT License
├── README.md                     # Documentation
```
## 🔧 Setup and Installation

### Requirements
- **Talend Studio**: For job development and execution.
- **Java JDK**: Required for Talend Studio.
- **Database**: PostgreSQL, MySQL, or other supported databases.
- **Git**: For version control.

### Steps
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/global-air-connectivity-data-pipeline.git
   ```

2. Extract the tar file containing project assets:

```bash
tar -xvf Flight_Pipeline_Project.tar -C /path/to/your/project
```

Replace /path/to/your/project with the directory where the files should be extracted.





---

🚀 Project Steps

1. Open the project in Talend Studio.


2. Extract the tar file:

Ensure Flight_Pipeline_Project.tar contains all required configurations, datasets, or other dependencies.

Use the command provided above to extract it to the appropriate project directory.



3. Configure context variables for your environment:

context.inputDirectory

context.outputDirectory

context.db_host, context.db_user, etc.



4. Run each job sequentially in the proper order to complete the pipeline.



This Markdown structure is formatted for use in a README file or similar documentation.


## 🚀 Project Steps

1. **Open the project** in Talend Studio.
2. **Configure context variables** for your environment:
   - `context.inputDirectory`
   - `context.outputDirectory`
   - `context.db_host`, `context.db_user`, etc.
3. **Run each job sequentially** in the proper order to complete the pipeline.

---

## 🌟 Outputs

- **Cleaned-Airports.csv**:  
  Contains validated airport data with no missing coordinates or IATA codes.

- **Rejected-Rows.csv**:  
  Includes rows with missing or invalid data.

- **Joined-Flights.csv**:  
  Enriched air route data with airport details.

---

## 🌐 Technologies Used

- **Talend Studio**: ETL tool for building data integration pipelines.
- **Java**: Backend runtime for Talend Studio.
- **Databases**: PostgreSQL or MySQL for storing enriched data.

---

## 📜 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
