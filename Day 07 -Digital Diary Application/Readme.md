# 📓 Day 7: Digital Diary Application
## 💡 Task Overview:
In this task, you will create a Digital Diary that offers the following functionalities:

📂 User Authentication: Signup, login, and logout features.
📖 Diary Management: Add, view, update, and delete diary entries.
💾 Persistent Data Storage: Store each user's diary entries in .txt files, ensuring that data is available across sessions.
## 🛠️ Steps and Instructions:
### 🔑 User Authentication:

Implement a signup feature that allows new users to create an account. Each user should have their own file for diary entries.
Implement a login feature, allowing existing users to access their diary. A user’s diary file will be loaded upon login.
Add a logout feature that securely exits the current session and returns the user to the main menu.
### 📖 Diary Entries:

Add Entry: Allow users to create new diary entries. Each entry should have a title and content, and it should be timestamped.
Update Entry: Users can update existing diary entries by specifying the entry's title.
Delete Entry: Allow users to delete entries by providing the title of the entry they wish to remove.
List Entries: Display all entries along with their timestamps and content.
### 🗂️ File Management:

Store each user's diary in a separate .txt file, with the filename based on the user’s username.
Implement logic to read and write entries to these files, ensuring persistent svtorage between sessions.
### 🧑‍💻 Object-Oriented Programming:

Create a DiaryEntry class that represents each diary entry with attributes like title, content, and timestamp.
Implement methods to add, update, delete, and list entries.
### 🔄 Main Menu:

After login, display a diary menu with the following options:
Add Entry
Update Entry
Delete Entry
List Entries
Log Out
### 🛠️ Error Handling:

Ensure that the application handles invalid input gracefully, such as incorrect login credentials or non-existing entries for updating/deleting.
### ✅ Task Checklist:
 Implement user signup and login functionality 🔑.
 Create diary entries with a title, content, and timestamp 📅.
 Update, delete, and list diary entries 📖.
 Store data persistently in .txt files 💾.
 Handle invalid inputs and exceptions 🚨.
### 📤 Submission:
Complete the notebook with all the required code and explanations.
Ensure the code runs correctly and diary functionalities work as expected.
Submit your completed project with clear comments in the code explaining each section.
