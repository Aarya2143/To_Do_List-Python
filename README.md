# TO_DO_LIST__PYTHON 
## CODE :

def display_menu():

    print("\nTo-Do List Application")
    print("1.View to-do list")
     print("2.Add a new task")
    print("3.Remove a task")
    print("4.Exit")
def view_tasks(tasks):

    if not tasks:
        print("Your to-do list is empty.")
    else:
        print("\nYour to-do list:")
        for idx, task in enumerate(tasks, 1):
            print(f"{idx}. {task}")

def add_task(tasks):

    task = input("Enter the new task: ")
    tasks.append(task)
    print(f'Task "{task}" has been added to your to-do list.')

def remove_task(tasks):

    view_tasks(tasks)
    if tasks:
        try:
            task_num = int(input("Enter the number of the task to remove: "))
            if 1 <= task_num <= len(tasks):
                removed_task = tasks.pop(task_num - 1)
                print(f'Task "{removed_task}" has been removed from your to-do list.')
            else:
                print("Invalid task number.")
        except ValueError:
            print("Please enter a valid number.")
def main():

    tasks = []
    while True:
        display_menu()
        choice = input("Choose an option: ")
        if choice == "1":
            view_tasks(tasks)
        elif choice == "2":
            add_task(tasks)
        elif choice == "3":
            remove_task(tasks)
        elif choice == "4":
            print("Exiting the application. Goodbye!")
            break
        else:
            print("Invalid choice. Please try again.")
if __name__ == "__main__":

    main()
    
## Algorithm :
- start
- Creating to do list choose option "2"
- For view to do list choose option "1"
- Delete task from list choose option "3"
- Choose option "4" for exit.
- Exit

## Outputs
- Actual "TO DO LIST" scenario:
  
  ![INTERN](https://github.com/user-attachments/assets/119130e7-3825-4079-a647-4d54e8ba46ab)

- Adding tasks into to do list:
  
  ![INTERN2](https://github.com/user-attachments/assets/5404852f-e37a-4488-85e4-54f48950d5d0)

- View task's in to do list:
  
  ![Screenshot 2024-08-11 113008](https://github.com/user-attachments/assets/f5a0fdd3-5f5a-4701-a936-26104f79d7a1)

- Remove task from to do list:
  
  ![task 3](https://github.com/user-attachments/assets/43747305-a848-4f58-a95e-47612462473f)

- Take exit from to do list:
  ![exit](https://github.com/user-attachments/assets/548cbc5f-f8b4-4ee1-a650-09da6b1cea3f)


