# Create-a-simple-to-do-list-application-where-users-can-add-update-and-delete-tasks
tasks = []

def add_task(task):
    tasks.append(task)

def remove_task(task):
    tasks.remove(task)

def display_tasks():
    for i, task in enumerate(tasks, 1):
        print(f"{i}. {task}")

while True:
    print("\n1. Add Task")
    print("2. Remove Task")
    print("3. Display Tasks")
    print("4. Quit")
    choice = input("Enter your choice: ")

    if choice == '1':
        task = input("Enter the task: ")
        add_task(task)
    elif choice == '2':
        task = input("Enter the task to remove: ")
        remove_task(task)
    elif choice == '3':
        display_tasks()
    elif choice == '4':
        break
    else:
        print("Invalid choice. Please try again.")
