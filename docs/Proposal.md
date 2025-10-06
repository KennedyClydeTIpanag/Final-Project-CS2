# 📌 Project Proposal (Draft)

## 📝 Project Title  
# HOSPITAL RECORD SCANNER

## 🎯 Project Objectives  
Objective 1: To organize the medical records of the patients.

Objective 2: To provide healthcare profesionals with easy access to each patient's medical history.

Objevtive 3: To analyze trends across patients (e.g, common diagnoses, medication given, frequency of visits)


## 🔍 Problem Statement  
A hospital records 4 patient's visit date, diagnosis, treatment, the doctor that treated them, and the doctor's notes on each of them. Symptoms of each patient seem to come back after a certain amount of time after the treatment. Solving this would lead to less frequent visits from the sick and less loss of resources. If we don't solve this problem then this can lead to delayed care, medication errors, and poor health outcomes. This pattern is shown in the dataset, where each patient has multiple visits for the same condition.

## ⚙️ Planned Features  
Feature #1 : EHR - The EHR (Electronic Health Record) is for organizing medical records, storing them, etc. This feature is basically for managing the medical records.

Feature #2 : Charts - Gives a visual interpretation for the data.

Feature #3 : Storage for the data - Data is saved. When deleted, you still have to access another storage to permanently delete it. If the decision is to not delete it permanently, then the data can still be restored. Corrupted data can be restored since this feature serves as a backup storage too.

Feature #4 : Security - When these security measures are implemented, it lessens the risk of corruption (if possible, it can be restored by feature #3) and invasion of a patient's privacy.

Feature #5 : Analytics - It is what collects and analyzes the data.

## ⌨️ Planned Inputs and Outputs  

- **Inputs**  
  - Medical staff will enter details such as; patient names, appointment dates, visit notes, or test results when updating a patient’s health record.
    
  - When someone wants to see a trend or summary, they might type in which patient percentage, what date range, or which kind of health data to view, like what age group has the most patients of this sickness from the last year.
 

- **Outputs**  
  - Users will see organized and up-to-date patient charts, like an overview page summarizing a patient’s history, recent doctor’s notes, and ongoing care plans all in one place.
    
  - The system will provide clear charts showing changes in health data over time, for instance, a graph of blood sugar levels, so doctors and patients can spot trends quickly.
    

## 🧠 Logic Plan  
Pseudocode:

START
import JSON
DECLARE hospitaldata, nameinput, nameindata, visitdetails, appointmentdates, notes, tests
with open('hospital.json', 'r') as file:
  hospitaldata = json.load(file)
INPUT nameinput
FOR stuff IN hospitaldata
  IF stuff['nameindata'] == nameinput THEN
    SET visitdetails TO item['visits']
    SET appointmentdates TO visitdetails['visit_date']
    SET notes TO visitdetails['notes']
    SET tests TO visitdetails['diagnosis']
  ENDIF
ENDLOOP

END



## 📂 GitHub Repository Link  
https://github.com/KennedyClydeTIpanag/Final-Project-CS2

