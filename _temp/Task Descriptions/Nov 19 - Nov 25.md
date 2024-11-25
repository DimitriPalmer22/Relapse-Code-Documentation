Research: Hashset

- <https://www.youtube.com/watch?v=XkRke_5_TFs&ab_channel=TeddySmith>
- <https://www.youtube.com/watch?v=xP7F8DmYNNg&ab_channel=C%23interviewquestions>

Research: Stacks

- <https://www.youtube.com/watch?v=KInG04mAjO0&ab_channel=BroCode>
- <https://www.youtube.com/watch?v=HXt-q8bMeP4&ab_channel=tutorialsEU-C%23>

Research: Queues

- <https://www.youtube.com/watch?v=4MQwKvsGCms&pp=ygUIYyMgcXVldWU%3D>
- <https://www.youtube.com/watch?v=nqXaPZi99JI&t=109s&pp=ygUIYyMgcXVldWU%3D>

### Project: "To-Do Task Manager with Smart Task Organization"

**Goal:** Build a console-based task manager that uses `HashSet`, `Stack`, and `Queue` to manage tasks effectively, while following the **Single Responsibility Principle (SRP)**.

### **Instructions**

#### **Overview**

You will build a C# console application that allows users to:

1. Add tasks to a to-do list.
2. View the list of all tasks.
3. Mark a task as completed.
4. Undo task completions (using a `Stack` to track recently completed tasks).
5. Organize urgent tasks to be processed in the order they were added (using a `Queue`).
6. Prevent duplicate task entries by storing tasks in a `HashSet`.

#### **Features To Implement**

1. **Task Storage**: Use a `HashSet<string>` to store unique tasks.
2. **Task Completion History**: Use a `Stack<string>` to allow users to undo completed tasks.
3. **Urgent Task Queue**: Use a `Queue<string>` to manage urgent tasks in the order they are added.

### **Step-by-Step Instructions**

1. **Set Up the Project**:
    
    - Create a new console project in Visual Studio or your favorite C# IDE.
    - Name the project `TaskManager`.
2. **Create a `TaskManager` Class**:  
    This class should have the following responsibilities:
    
    - Manage the list of tasks using a `HashSet<string>`.
    - Provide methods to add tasks, mark tasks as completed, and view tasks.
3. **Create a `TaskHistory` Class**:  
    This class should:
    
    - Use a `Stack<string>` to track completed tasks for undo functionality.
    - Provide methods to mark tasks as completed and undo task completion.
4. **Create a `UrgentTaskManager` Class**:  
    This class should:
    
    - Use a `Queue<string>` to manage urgent tasks.
    - Provide methods to add urgent tasks and process them in order.

