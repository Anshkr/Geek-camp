Task App
This project is a simple web-based task management app. It allows users to add tasks dynamically to a list. The app uses HTML, CSS, and JavaScript to handle user interactions and update the task list in real-time.

Features
Users can input tasks using a form.
When the form is submitted, the task is added to a table.
Task additions occur dynamically without reloading the page.
Project Structure
HTML
The HTML structure includes:

A form with a text input to allow users to add tasks.
A table where tasks are displayed as they are added.
JavaScript
Event Listener: Listens for form submissions and prevents the default page reload behavior.
Task Addition: Dynamically creates and appends a new table row with the task entered in the input field.
Code Explanation
HTML
The HTML <table> has an empty <tbody> where tasks will be appended. The task input form is located after the table.
html
Copy code
<table>
  <thead>
    <tr>
      <th>Task Name</th>
    </tr>
  </thead>
  <tbody id="tasks">
  </tbody>
</table>
The form contains a text input for the user to enter a task and a submit button to add the task.
html
Copy code
<form>
  <input type="text" name="task" id="task-input">
  <button type="submit">Add Task</button>
</form>
JavaScript
A JavaScript event listener waits for the form submission, retrieves the task from the input, and appends it as a new table row.
javascript
Copy code
document.querySelector('form').addEventListener('submit', function(e) {
  e.preventDefault();  // Prevents form from submitting normally
  var task = document.querySelector('#task-input').value;  // Gets task input
  var tasks = document.querySelector('#tasks');  // Targets the tasks table body
  var newTask = document.createElement('tr');  // Creates a new row
  newTask.innerHTML = '<td>' + task + '</td>';  // Adds the task to the new row
  tasks.appendChild(newTask);  // Appends the new row to the table
});
How to Use
Open the index.html file in your web browser.
Enter a task into the input field and click "Add Task."
The task will appear in the table below.
Requirements
A modern web browser supporting HTML5 and JavaScript.
License
This project is open-source. You are free to use, modify, and distribute it.
