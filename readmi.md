### **README for Patient Management System**

# Introduction
This is a simple Patient Management System written in C++ that helps a clinic efficiently manage patient data. The system supports adding patient details, displaying patient queues, handling emergency and non-emergency patients, searching by mobile number, and saving/loading patient data from a file. The system prioritizes emergency patients.

# Data Structures Used
1. queue<patient>
    * Used to maintain separate queues for emergency and non-emergency patients.

2. unordered_map<long long, patient>
    * Used for quick lookup of patient details using their mobile number.

3. ofstream and ifstream
    * Used to save and load patient data from a CSV file (patients.csv).

# Explanation
Key Features:

1. Add Patient:
    * Takes user input for patient details.
    * Validates inputs like blood group and age.
    * Differentiates between emergency and non-emergency cases.
    * Saves the data to a CSV file for persistence.

2. Take Patient to Doctor:
    * Fetches the next patient from the emergency queue if available.
    * If no emergency patient exists, fetches the next regular patient.

3. Display All Patients:
    * Lists all patients currently in the system, categorized as emergency and non-emergency.

4. Show Current Queue:
    * Displays the current waiting queue for emergency and non-emergency patients, with their order.

5. Search by Mobile Number:
    * Finds a patient by their mobile number using the unordered_map for fast lookups.

6. Persistence:
    * Automatically loads patient data from the file upon starting the program.
    * Saves new entries to the file as they are added.

# Sample Output
----Welcome----

CLINIC MENU
[1] Add patient
[2] Take patient to Doctor
[3] Display list of all patients
[4] Show current queue
[5] Search patient by mobile number
[6] Exit
Please enter your choice: 1

Enter Patient details
First Name: John
Last Name: Doe
Blood Group (A+, A-, B+, B-, O+, O-, AB+, AB-): O+
Gender (m/f/o): m
Age: 32
Mobile Number: 9876543210
Emergency? (1 for yes, 0 for no): 0
What's troubling you?: Fever
Patient Added
Press Enter to continue...

# File Description
* main.cpp: Contains the program code.
* patients.csv: Stores patient details persistently.

# Conclusion
This Patient Management System is an effective way to manage and prioritize patient data in a clinic. Its use of queues and file persistence ensures smooth operation even after program restarts.