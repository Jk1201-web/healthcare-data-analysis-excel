# healthcare data analysis excel
Cleaned and analyzed 10,000 hospital admission records in Excel using lookup tables and pivot tables to explore patient demographics, conditions, billing and length of stay.
# Healthcare Dataset Analysis

Data cleaning and analysis of a hospital admissions dataset in Excel (`Clean.xlsx`).

## Project Overview

| Metric | Value |
|---|---|
| Patient records | 10,000 |
| Unique patient names | 9,378 |
| Columns | 22 |
| Admission period | 30 Oct 2018 – 30 Oct 2023 |
| Hospitals | 8,639 |
| Doctors | 9,416 |
| Total billing | $255,168,068 |
| Average billing per admission | $25,517 |
| Average length of stay | 15.6 days |
| Average patient age | 51.5 years |

## Workbook Structure

| Sheet | Description |
|---|---|
| `healthcare_dataset` | Cleaned data (10,000 records) with added columns: Department, Length of Stay, Year, Month, Stay Category |
| `lookup` | Reference tables: condition → department, admission type → priority, blood type category, test result → follow-up action |
| `Analysis` | Pivot tables and summary counts |

## Key Numbers

### Patients
- **Gender:** Female 5,075 (50.8%) · Male 4,925 (49.2%)
- **Age:** min 18 · median 52 · max 85
- **Blood types:** all eight types are almost evenly split (1,238 – 1,275 patients each)
  - Most common: AB- (1,275) · Least common: A- (1,238)

### Medical Conditions

| Condition | Patients | Department |
|---|---|---|
| Asthma | 1,708 | Pulmonology |
| Cancer | 1,703 | Oncology |
| Hypertension | 1,688 | Cardiology |
| Arthritis | 1,650 | Orthopedics |
| Obesity | 1,628 | *(none assigned)* |
| Diabetes | 1,623 | Endocrinology |

### Admissions

| Admission Type | Priority | Patients |
|---|---|---|
| Urgent | Medium | 3,391 |
| Emergency | High | 3,367 |
| Elective | Low | 3,242 |

### Length of Stay

| Category | Days | Patients |
|---|---|---|
| Short Stay | 1 – 5 | 1,592 |
| Medium Stay | 6 – 10 | 1,714 |
| Long Stay | 11 – 30 | 6,694 (66.9%) |

### Test Results and Follow-Up

| Test Result | Follow-Up Action | Patients |
|---|---|---|
| Abnormal | Doctor Consultation | 3,456 |
| Inconclusive | Repeat Test | 3,277 |
| Normal | Routine check-up | 3,267 |

### Medications

| Medication | Patients |
|---|---|
| Penicillin | 2,079 |
| Lipitor | 2,015 |
| Ibuprofen | 1,976 |
| Aspirin | 1,968 |
| Paracetamol | 1,962 |

### Billing by Insurance Provider

| Provider | Patients | Total Billing | Avg per Admission | Max Bill |
|---|---|---|---|---|
| Cigna | 2,040 | $52,340,172 | $25,657 | $49,936 |
| Aetna | 2,025 | $52,321,795 | $25,838 | $49,996 |
| Blue Cross | 2,032 | $52,125,859 | $25,652 | $49,958 |
| United Healthcare | 1,978 | $50,250,468 | $25,405 | $49,995 |
| Medicare | 1,925 | $48,129,775 | $25,002 | $49,986 |

### Billing by Condition

| Condition | Total Billing | Avg per Admission |
|---|---|---|
| Cancer | $43,493,081 | $25,539 |
| Asthma | $43,412,014 | $25,417 |
| Hypertension | $42,534,281 | $25,198 |
| Diabetes | $42,295,568 | $26,060 |
| Obesity | $41,873,532 | $25,721 |
| Arthritis | $41,559,592 | $25,188 |

### Admissions per Year

| Year | Admissions | Total Billing |
|---|---|---|
| 2018 | 303 | $7,523,125 |
| 2019 | 1,973 | $50,098,774 |
| 2020 | 2,044 | $52,776,410 |
| 2021 | 2,063 | $52,427,472 |
| 2022 | 2,001 | $51,682,471 |
| 2023 | 1,616 | $40,659,815 |

> 2018 and 2023 are partial years (data runs from 30 Oct 2018 to 30 Oct 2023).

## Data Cleaning Notes

- Rows with missing values were checked: the 10,000 data records have no empty cells except **Department** for Obesity.
- 0 duplicate rows and 0 negative lengths of stay.
- **Length of Stay** = Discharge Date − Date of Admission.
- **Department** is assigned through the `lookup` sheet. Obesity has no matching department, so its 1,628 records show `#N/A` in the pivot table.
- Billing amounts range from $1,000 to $49,996.

## Tools

- Microsoft Excel (formulas, lookup tables, pivot tables)

## Author

*Add your name and links here.*
