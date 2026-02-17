# 🌍 Real-Time Weather ETL Pipeline (Python & OpenWeather API)

**📌 Project Overview**

This project is a Python-based ETL (Extract, Transform, Load) pipeline designed to automate the collection and processing of real-time weather data. By integrating with the OpenWeatherMap API, the system fetches live meteorological data for a specific city, transforms raw technical units into human-readable formats, and exports the final dataset into a structured CSV file for further analysis.

<img width="1466" height="828" alt="image" src="https://github.com/user-attachments/assets/bfd3cb30-46a9-42b6-b094-c4ea481f0768" />


**🚀 Key Features**

Automated Data Extraction: Uses the requests library to interface with REST APIs and retrieve live JSON data.

Secure Credential Management: Implements best practices by reading API keys from a local credential.txt file instead of hardcoding sensitive information.

Data Transformation Logic: * Converts temperature from Kelvin to Fahrenheit.

Translates Unix timestamps (UTC) into local, human-readable date-time formats using the datetime library.

Structured Storage: Utilizes Pandas DataFrames to clean and organize data into a tabular format before exporting to a non-indexed CSV.

**🛠️ Technical Stack**

Language: Python 3.x

Libraries: * Pandas: For data manipulation and CSV generation.

Requests: For handling HTTP requests to the API.

JSON: For parsing API responses.

DateTime: For temporal data conversion.

API Source: OpenWeatherMap API

**📂 Project Structure**

main.py: The main script containing the ETL logic.

credential.txt: (User-provided) Stores the OpenWeather API key.

current_weather_data_Ahmedabad.csv: The generated output file containing processed data.

**⚙️ How It Works**

Extract: The script calls the OpenWeather API using a specific city query and API key.

Transform:

Raw JSON is parsed to extract temperature, humidity, wind speed, and pressure.

Mathematical formulas convert temperature units.

Timezone offsets are applied to calculate accurate local sunrise/sunset times.

Load: The cleaned data is wrapped into a Pandas DataFrame and saved as a .csv file, making it ready for BI tools like Tableau, PowerBI, or Excel.
