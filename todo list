class Task:
    def _init_(self, description, priority, due_date):
        self.description = description
        self.priority = priority
        self.due_date = due_date
        self.completed = False

class ToDoList:
    def _init_(self):
        self.tasks = []

    def add_task(self, task):
        self.tasks.append(task)

    def remove_task(self, task):
        self.tasks.remove(task)

    def mark_completed(self, task):
        task.completed = True

    def display_tasks(self):
        for task in self.tasks:
            status = "✓" if task.completed else " "
            print(f"{status} {task.description} (Priority: {task.priority}, Due: {task.due_date})")

def main():
    todo_list = ToDoList()

    while True:
        print("\n--- To-Do List ---")
        print("1. Add Task")
        print("2. Remove Task")
        print("3. Mark Task as Completed")
        print("4. Display Tasks")
        print("5. Exit")

        choice = input("Enter your choice: ")

        if choice == "1":
            description = input("Enter task description: ")
            priority = input("Enter task priority (high/medium/low): ")
            due_date = input("Enter due date (DD-MM-YYYY): ")
            task = Task(description, priority, due_date)
            todo_list.add_task(task)
            print("Task added successfully!")

        elif choice == "2":
            description = input("Enter task description to remove: ")
            matching_tasks = [task for task in todo_list.tasks if task.description == description]
            if matching_tasks:
                todo_list.remove_task(matching_tasks[0])
                print("Task removed successfully!")
            else:
                print("Task not found.")

        elif choice == "3":
            description = input("Enter task description to mark as completed: ")
            matching_tasks = [task for task in todo_list.tasks if task.description == description]
            if matching_tasks:
                todo_list.mark_completed(matching_tasks[0])
                print("Task marked as completed!")
            else:
                print("Task not found.")

        elif choice == "4":
            todo_list.display_tasks()

        elif choice == "5":
            print("Exiting. Have a productive day!")
            break

if _name_ == "_main_":
    main()
