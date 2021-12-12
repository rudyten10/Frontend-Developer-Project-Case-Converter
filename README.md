# Frontend-Developer-Project-Case-Converter

Description
You can convert the text into different cases, excellent! Now let's add the ability to save the changed text as a .txt file!

Objectives
Add one more button to the page. Assign the save-text-file id to it. Add another event handler for the button.

When the button is clicked, you should get the text in the textarea element and generate the text.txt file. The resulting file should contain the text from the textarea element.

Here is a code snippet that shows how you can implement it:

function download(filename, text) {
  let element = document.createElement('a');
  element.setAttribute('href', 'data:text/plain;charset=utf-8,' + encodeURIComponent(text));
  element.setAttribute('download', filename);

  element.style.display = 'none';
  document.body.appendChild(element);

  element.click();

  document.body.removeChild(element);
}

// Start file download.
download("hello.txt","This is the content of my file :)");
Example
Example 1: an example of your app
![image](https://user-images.githubusercontent.com/94325541/145732373-bd8b3e26-73e9-4897-9bad-99ec5a4242d4.png)
