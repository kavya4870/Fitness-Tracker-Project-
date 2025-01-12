# Fitness-Tracker-Project-
A simple Python program to track steps and calculate calories burned.
# Usage: Users can record their steps, view their fitness summary, and exit the program.
Source code:
class FitnessTracker:
    def __init__(self, name):
        # Initialize the user's name, steps, and calories burned
        self.name = name
        self.steps = 0
        self.calories_burned = 0
  def record_steps(self, steps):
        # Update steps and calculate calories burned
        self.steps += steps
        self.calories_burned += steps * 0.05  # Assuming 1 step burns 0.05 calories
 def display_summary(self):
        # Display the user's fitness summary
        print(f"\n{self.name}'s Fitness Summary:")
        print(f"Total Steps: {self.steps}")
        print(f"Calories Burned: {self.calories_burned:.2f} calories")
# Main program
if __name__ == "__main__":
    user_name = input("Enter your name: ")
    user_tracker = FitnessTracker(user_name)
while True:
        # Display menu options
        print("\nOptions:")
        print("1. Record Steps")
        print("2. Display Summary")
        print("3. Exit")
# Get user choice
        choice = input("Enter your choice (1/2/3): ")
 if choice == "1":
            try:
                # Record steps
                steps_recorded = int(input("Enter the number of steps: "))
                if steps_recorded < 0:
                    print("Steps cannot be negative. Please enter a positive number.")
                else:
                    user_tracker.record_steps(steps_recorded)
                    print("Steps recorded successfully!")
            except ValueError:
                print("Invalid input. Please enter a valid number of steps.")
        elif choice == "2":
            # Display the fitness summary
            user_tracker.display_summary()
        elif choice == "3":
            # Exit the program
            print("Exiting the fitness tracker. Goodbye!")
            break
else:
            # Handle invalid menu choice
            print("Invalid choice. Please enter 1, 2, or 3.")
![image](https://github.com/user-attachments/assets/beb584b1-f4f8-46eb-b938-ec4c6fa19b36)
