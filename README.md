class Task:
 
    def __init__(self,title,description,deadline,completed=True):
        self.title=title
        self.description=description
        self.deadline=deadline
        self.completed=completed
 
    def __int__(self):
        status = "Зроблено" if self.completed else "Не зроблено"
 
class TaskManager:
 
    def __init__(self,task):
        add_task(task)
        self.tasks.append(task)
        print(f"Завдання '{task.title}' додано.")
 
    def delete_task(self,task_title):
        for task in self.task:
            self.tasks.remove(task)
            print(f"Завдання '{task_title}' видалено.")
            return
        print(f"Завдання '{task_title}' не знайдено.")
 
    def  mark_task_completed(task_title):
        for task in self.task:
            if task.title == task_title:
             task.completed = True
            print(f"Завдання '{task_title}' позначено як виконане.")
            return
            print(f"Завдання  '{task_title}' не знайдено.")
 
    def show_tasks(self):
        if not self.task:
            print("Список завдань порожній")
            return
        for i, task in enumerate(self.tast,1):
            print(f"{1}. {task}")
 
    def menu():
 
        while True:
            print("\n Меню:")
            print("1 Додати завдання")
            print("2 Видалити завдання")
            print("3 Позначити завдання як виконане")
            print("4 Переглянути всі завдання")
            print("5 Вийти")
 
            choice = input(" Виберіть дію (1-5): ")
 
            if choice == "1":
                title = input(" Введіть назву завдання: ")
                description = input(" Введіть опис завдання: ")
                deadline = input(" Введіть дедлайн (дата): ")
                task = Task(title, description, deadline)
                manager.add_task(task)
 
            elif choice == "2":
                title = input(" Введіть назву завдання для видалення: ")
                manager.delete_task(title)
 
            elif choice == "3":
                title = input(" Введіть назву завдання для позначення як виконане: ")
                manager.mark_task_completed(title)
 
            elif choice == "4":
                manager.show_tasks()
 
            elif choice == "5":
                print("До побачення!")
                break
 
            else:
                print(" Невірний вибір, спробуйте ще раз!")
        if __init__ == "__menu__":
menu()
manager = TaskManager()
