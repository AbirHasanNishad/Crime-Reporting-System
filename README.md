# Crime-Reporting-System
# Simple Crime Reporting System

# Define a list to store reports
crime_reports = []


# Function to file a new crime report
def file_report():
    print("\n--- File a Crime Report ---")

    # Get input from the user for the report details
    reporter_name = input("Enter Reporter's name: ")
    crime_type = input("Enter the type of crime which you want to Report: ")
    location = input("Enter the location of the crime: ")
    description = input("Enter a brief description of the incident: ")

    # Store the report in a dictionary format
    report = {
        "reporter_name": reporter_name,
        "crime_type": crime_type,
        "location": location,
        "description": description
    }

    # Add the report to the list of reports
    crime_reports.append(report)
    print("\nReport filed successfully!")


# Function to view all crime reports
def view_reports():
    print("\n--- Crime Reports ---")

    # Check if there are any reports
    if not crime_reports:
        print("No reports available.")
    else:
        # Loop through and print each report
        for i, report in enumerate(crime_reports, start=1):
            print(f"\nReport {i}")
            print(f"Reporter Name: {report['reporter_name']}")
            print(f"Crime Type: {report['crime_type']}")
            print(f"Location: {report['location']}")
            print(f"Description: {report['description']}")


# Main program loop
def main():
    while True:
        print("\n--- Crime Reporting System ---")
        print("1. File a new report")
        print("2. View all reports")
        print("3. Exit")

        choice = input("Enter your choice (1, 2, or 3): ")

        if choice == '1':
            file_report()
        elif choice == '2':
            view_reports()
        elif choice == '3':
            print("Exiting the system. Goodbye!")
            break
        else:
            print("Oh no!! Wrong choice. Please enter 1, 2, or 3.")


# Run the main program loop
main()
