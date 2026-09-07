# 🌤️ UiPath Weather Data Automation

A UiPath automation project that retrieves weather temperature data for selected Egyptian governorates from Google and stores the collected results in an Excel workbook.

## 📌 Project Overview

This project demonstrates how **UiPath** can be used to automate web data extraction and data entry into Excel.

The automation searches Google for the weather information of selected Egyptian governorates, extracts the current temperature, and stores the results in an Excel file.

## 🎯 Objectives

- Automate Google weather searches using UiPath.
- Extract temperature information from Google search results.
- Process multiple Egyptian governorates.
- Use separate workflows for each governorate.
- Pass extracted values between workflows using **Arguments**.
- Store the collected weather data in an Excel workbook.

## 📍 Governorates

The automation currently handles:

- Alexandria
- Cairo
- Luxor
- Port Said

## ⚙️ Workflow Structure

```text
Main.xaml
│
├── GetAlexandriaWeather.xaml
├── GetCairoWeather.xaml
├── GetLuxorWeather.xaml
└── GetPortSaidWeather.xaml
```

### Main.xaml

The main workflow controls the execution of the automation and invokes the individual governorate workflows.

### Governorate Workflows

Each workflow:

1. Opens Google.
2. Searches for the weather of the specified governorate.
3. Extracts the temperature.
4. Returns the temperature to `Main.xaml` using an Output Argument.

Example:

```text
out_Temperature → alexTemperature
```

## 📊 Output

The collected temperatures are stored in an Excel workbook in a structured format:

| Governorate | Temperature |
|---|---|
| Alexandria | Temperature |
| Cairo | Temperature |
| Luxor | Temperature |
| Port Said | Temperature |

## 🛠️ Technologies Used

- **UiPath Studio**
- **UiPath Web Automation**
- **Google Search**
- **Excel Workbook**
- **UiPath Arguments & Variables**

## 🔄 Automation Flow

```text
Start
  ↓
Open Google
  ↓
Search Governorate Weather
  ↓
Extract Temperature
  ↓
Pass Temperature Using Output Argument
  ↓
Return to Main Workflow
  ↓
Write Data to Excel
  ↓
Next Governorate
  ↓
End
```

## 💡 Key UiPath Concepts Demonstrated

- Workflow modularization
- Invoke Workflow File
- Input/Output Arguments
- Variables
- Web UI Automation
- Data Extraction
- Excel Workbook activities
- Sequential automation

## 👨‍💻 Author

**Maged Mohammed Abdalkader**

---

⭐ This project was created as a practical UiPath automation project to demonstrate web automation, data extraction, workflow modularization, and Excel data handling.
