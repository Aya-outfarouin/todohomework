# todohomework
Data Storage
The program stores tasks in a plain text file named tasks.txt. Each task is recorded in the following format:
<DUE DATE> - [<STATUS>] <TASK DESCRIPTION>
<DUE DATE> is the due date of the task.
<STATUS> is either [ ] for incomplete tasks or [x] for completed tasks.
<TASK DESCRIPTION> is the description of the task.
This format allows easy reading, searching, and modification using common Unix text processing tools.

Code Organization
The code is organized into several functions, each responsible for a specific task management operation. Here's a brief overview of the main functions:

show_usage(): Displays the usage instructions and available options for the script.

add_task(task, due_date): Adds a new task to the tasks.txt file.

Checks if both task description and due date are provided.
Appends the task to the file in the specified format.
list_tasks(): Lists all tasks with line numbers for easy reference.

list_tasks_by_day(date): Lists tasks for a specific date, separating completed and uncompleted tasks.

Uses grep to filter tasks by date and status.
search_task_by_title(title): Searches for tasks containing a specific title substring.

Uses grep to find matching tasks.
delete_task(task_id): Deletes a task by its ID.

Uses sed to delete the specific line from the file.
update_task(task_id, new_task, new_date): Updates an existing task with a new description and due date.

Constructs a new line and replaces the old one using sed.
mark_task(task_id): Marks a task as completed by updating its status.

Reads the specific line, changes its status to [x], and writes it back.
Running the Program
Ensure the script is executable:

chmod +x script_name.sh

Run the script with appropriate options:

To add a task:
./script_name.sh add "Buy groceries" "2024-06-02"
To list all tasks:
./script_name.sh list
To list tasks for a specific date:
./script_name.sh listday "2024-06-02"
To search for a task by title:
./script_name.sh search "groceries"
To delete a task by ID:
./script_name.sh delete 1
To update a task by ID:
./script_name.sh update 1 "Buy milk and bread" "2024-06-03"
To mark a task as completed:
./script_name.sh mark 1
This program provides a simple yet effective way to manage tasks using a plain text file, leveraging basic Unix text processing tools to perform various operations. The use of line numbers for task IDs ensures easy identification and manipulation of specific tasks.






