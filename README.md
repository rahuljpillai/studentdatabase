# studentdatabase
 Student Database Management System using the powerful trio of HTML, CSS, and JavaScript.

To get started, we will first need to create a basic HTML file. In this file, we will include the main structure for our Student Database Management System.


After creating the files just paste the following codes into your file. Make sure to save your HTML document with a .html extension, so that it can be properly viewed in a web browser.


Here's a breakdown of each section:

**STEP 1**


1. <!DOCTYPE html>: This declaration defines the document type and version of HTML being used, which in this case is HTML5.


2. <html lang="en">: This is the opening tag for the HTML document. The lang attribute is set to "en," indicating that the content of the page is in English.


3. <head>: The <head> section contains metadata about the web page, including information that is not displayed on the web page itself. Here's what's inside it:


<meta charset="UTF-8">: This meta tag specifies the character encoding for the document, which is set to UTF-8, a widely used character encoding for displaying text on the web.
<meta name="viewport" content="width=device-width, initial-scale=1.0">: This meta tag is often used for making web pages responsive on different devices. It sets the initial scale to 1.0 and ensures that the page's width matches the device's width.
<title>Student Database Management System</title>: This sets the title of the web page, which is displayed in the browser's title bar or tab.
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css" integrity="...">: This line links to an external stylesheet, which is used to apply styles (such as fonts and icons) to the web page. It uses the Font Awesome library for icons.
<link rel="stylesheet" href="styles.css">: This line links to another external stylesheet called "styles.css," which contains additional styles for the web page.

4. <body>: The <body> section contains the visible content of the web page. Here's what's inside it:


5. <div class="container">: This <div> element is used to create a container for the page's content, dividing it into two columns (left and right).


6. <div class="left">: This is a div that represents the left column of the page.


<h1>Student Registration</h1>: This is a top-level heading, indicating the title of the left column, related to student registration.
<form id="record-form">: This is a form element with the ID "record-form." It contains several form input elements.
<input type="text" id="name" placeholder="Name" required>: This is a text input field for entering a name, marked as required.
<input type="number" id="age" placeholder="Age" required>: This is a numeric input field for entering age, also marked as required.
<input type="text" id="email" placeholder="Email" required>: This is a text input field for entering an email address, marked as required.
<button type="submit">Add Record</button>: This is a submit button used to submit the form.
<input type="hidden" id="edit-index" value="-1">: This is a hidden input field with the ID "edit-index" and a default value of "-1." It's used for some JavaScript functionality.

7. <div class="right">: This is a div that represents the right column of the page.


<h2>Records</h2>: This is a level-two heading, indicating the title of the right column, which is related to displaying records.
<table>: This element represents an HTML table, which is used for displaying tabular data.
<thead>: This is the table header section, containing column headers.
<tr>: This represents a table row.
<th>Name</th>, <th>Age</th>, <th>Email</th>, <th>Edit</th>, <th>Delete</th>: These are table header cells, specifying the column names for the table.
<tbody id="record-list"></tbody>: This is the table body section, which is initially empty. It has an ID of "record-list," for JavaScript to populate with data later.

8. <script src="script.js"></script>: This line includes an external JavaScript file called "script.js," which is used to add interactivity and functionality to the web page.


This is the basic structure of our Student Database Management System using HTML, and now we can move on to styling it using CSS.


**STEP 2**

Step 2 (CSS Code):

Once the basic HTML structure of the Student Database Management System is in place, the next step is to add styling to the system using CSS.


Next, we will create our CSS file. In this file, we will use some basic CSS rules to style our management system.Let me break down what each part of the code does:


1. body: This section sets some basic styles for the entire webpage's body.


font-family: Specifies the font to be used for text content within the body. It uses Arial as the first choice and a generic sans-serif font as a fallback.
display: Makes the body a flex container, allowing its children to be flex items.
justify-content and align-items: These properties center the content both horizontally and vertically within the body.
height: Sets the height of the body to 100% of the viewport height (100vh), making sure the content fills the entire viewport.

2. .container: This section defines styles for an element with the class "container."


display: Makes the container a flex container.
flex-wrap: Allows the container's content to wrap onto a new line if it overflows its width.
max-width: Sets a maximum width of 900 pixels for the container.
margin: Centers the container horizontally by setting left and right margins to "auto."
border: Adds a 1-pixel solid border around the container with a light gray color (#ccc).
padding: Adds 20 pixels of padding inside the container.
box-shadow: Applies a subtle box shadow for a visual effect.

3. .left and .right: These sections style two elements with classes "left" and "right," presumably located inside the container.


flex: Both elements are given a flex value of 1, which means they will share an equal amount of available space within the container.
padding: Adds 10 pixels of padding inside both elements.
.right also has border-left to create a vertical divider line between the left and right elements.


5. table: This section styles all HTML tables on the page.


width: Makes tables span the full width of their parent container.
border-collapse: Collapses the borders of table cells into a single border for a cleaner appearance.

6. th and td: These sections style table headers (th) and table data cells (td) within tables.


border: Adds a 1-pixel solid border around cells with a light gray color (#ccc).
padding: Adds 8 pixels of padding within cells.
text-align: Aligns text within cells to the left.

7. th: Styles table header cells with a light gray background color (#f2f2f2) to visually distinguish them.


8. Styles for input elements (input[type='text'] and input[type='number']):


Sets the width to 80% of their parent container.
Adds padding and margin to give some spacing and styling.
Adds a 1-pixel solid border with rounded corners for input elements.

9. Styles for buttons (button):


Adds padding, background color, text color, and rounded corners.
Removes the default button border.
Changes the cursor to a pointer on hover.
On hover, the background color of the button changes.

10. .deleteButton: Styles an element with the class "deleteButton," a button for deletion.


Centers the text within the element.

11. i: Styles <i> elements, typically used for icons.


Adds margin and sets the font size.
Changes the cursor to a pointer.

12. #yesBtn:hover and #noBtn:hover: Styles the "yes" and "no" buttons with specific IDs when they are hovered over.


Changes the text color to red for "yes" and green for "no" when hovered.

This will give our Student Database Management System an upgraded presentation. Create a CSS file with the name of styles.css and paste the given codes into your CSS file. Remember that you must create a file with the .css extension.

**STEP 3**


Finally, we need to create a function in JavaScript. Let's break down the code and explain its functionality step by step:


1. The code starts by selecting various HTML elements by their IDs using document.getElementById(). These elements are assigned to variables for later use. These elements include a form (recordForm) for adding or updating records, input fields for name, age, and email, a list element (recordList) for displaying records, and an input field (editIndexInput) that presumably stores the index of the record being edited.


2. It initializes an empty array called records by attempting to retrieve data from the browser's local storage. If there are records stored in local storage, they are parsed from JSON format into a JavaScript array. If there are no records or if local storage is empty, it initializes records as an empty array.


3. The isDuplicateName() function checks if a record with a given email already exists in the records array. It returns true if a duplicate email is found, and false otherwise.


4. The displayRecords() function is responsible for rendering the records in the HTML table (recordList). If there are records, it creates a table row for each record, including buttons for editing and deleting records. If there are no records, it displays a message saying "No Record Found."


5. An event listener is added to the recordForm element to handle form submissions. When the form is submitted, it prevents the default form submission behavior (which would cause the page to reload). It then retrieves the values entered by the user for name, age, and email, as well as the editIndex (index of the record being edited) from the editIndexInput.


6. It checks if all the required fields (name, age, and email) are filled out. If not, it does nothing. Otherwise, it checks if the email already exists in the records array (in the case of adding a new record). If it's a duplicate and the editIndex is -1 (indicating a new record), it shows an alert and returns without adding a duplicate.


7. If it's a new record, it adds it to the records array. If it's an edit, it updates the existing record in the records array.


8. The localStorage is updated with the current records array, which is serialized to JSON format.


9. The input fields are cleared, and the displayRecords() function is called to refresh the displayed records.


10. There are also functions for editing a record, deleting a record, confirming a delete action, and resetting a delete action. These functions are used to handle user interactions with the records in the HTML table.


11. Finally, the displayRecords() function is called initially to display any existing records when the page loads.


Create a JavaScript file with the name script.js and paste the given codes into your JavaScript file and make sure it's linked properly to your HTML document so that the scripts are executed on the page. Remember, you’ve to create a file with .js extension.
