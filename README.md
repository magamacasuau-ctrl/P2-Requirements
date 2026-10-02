# Student Activity Score System

# Function to calculate the average
def calculate_average(score1, score2, score3):
    return (score1 + score2 + score3) / 3


# Function to determine the student's status
def determine_status(average):
    if average >= 90:
        return "Excellent"
    elif average >= 75:
        return "Passed"
    else:
        return "Failed"


# Ask how many students will be processed
while True:
    number_of_students = int(input("Enter number of students (minimum 3): "))

    if number_of_students >= 3:
        break
    else:
        print("Please enter at least 3 students.")


# Process each student
for student in range(1, number_of_students + 1):

    print("\n-----------------------------")
    print("Student", student)
    print("-----------------------------")

    # Ask for student's name
    name = input("Enter student's name: ")

    # Ask for activity scores
    activity1 = float(input("Enter Activity 1 score: "))
    activity2 = float(input("Enter Activity 2 score: "))
    activity3 = float(input("Enter Activity 3 score: "))

    # Calculate average using the function
    average = calculate_average(activity1, activity2, activity3)

    # Determine status using the function
    status = determine_status(average)

    # Display results
    print("\n===== STUDENT RESULT =====")
    print("Name:", name)
    print("Activity 1:", activity1)
    print("Activity 2:", activity2)
    print("Activity 3:", activity3)
    print("Average:", round(average, 2))
    print("Status:", status)
