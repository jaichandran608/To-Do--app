# To-Do--app
from todo_manager import TodoManager

def main():
    todo = TodoManager()

    while True:
        print("\n--- To-Do List App ---")
        print("1. View tasks")
        print("2. Add task")
        print("3. Delete task")
        print("4. Clear all tasks")
        print("5. Exit")

        choice = input("Enter your choice: ")

        if choice == "1":
            todo.view_tasks()
        elif choice == "2":
            task = input("Enter the task: ")
            todo.add_task(task)
        elif choice == "3":
            num = int(input("Enter task number to delete: "))
            todo.delete_task(num)
        elif choice == "4":
            todo.clear_tasks()
        elif choice == "5":
            print("Goodbye!")
            break
        else:
            print("Invalid choice. Try again.")

if __name__ == "__main__":
    main()
