# README

## This is the test task description

### SUMMARY

**Using Rails 7 and Bootstrap 5 create an app which will allow users to add, edit, and delete simple notes**

### Task detailed description

1. Using Devise gem, add registration and sign in functionality, and add a header with "Sign In" and "Sign Out" links, as well as the full name of the user.

2. Add a label "N notes" in the center of the header, where N is a count of notes.

3. In the main section of the page, add a grid with the following columns:
   - Line number (#),
   - Note text
   - Author name,
   - Create date, and
   - Delete button (trash icon).

4. All columns, except for the note column, should have a fixed width.

5. Author column displays the user's first name and a tooltip with their full name.

6. Date column displays the date of note creation and a tooltip with the time of creation.

7. Delete column displays a trash icon with a tooltip saying "Delete". When clicked, show a confirmation popup saying "Are you sure?".
   - Use Hotwire to delete the note without refreshing the page, causing the corresponding row to disappear.
   - Trash icon if current user is the author of the note, in another case use some different icon with tooltip 'you can delete only your own note'

8. If a user is signed in, add a row to the end of the grid with a text input field with the placeholder "WRITE A NEW NOTE". Customize the appearance as desired, such as converting the text to uppercase.

9. After making changes in the input field, automatically save the note in the database and display a new row in the table with the corresponding data in the columns.
   - Use Hotwire to achieve this without refreshing the page. If a note is successfully saved, display a message indicating the successful saving.

10. The width of the table should be no more than 640px and no less than 300px. If the screen width is greater than 860px, move the title to the right of the table.

11. Add pagination with 5 rows per page for the grid. The new note input row should not be counted as one of the 5 notes, and should be visible on every note page.

12. Provide test coverage for the application using RSpec.

13. Deploy the application to a hosting environment.

## DB structure
```
    users
---------------------------
id        | email
---------------------------
bigserial | text
---------------------------

    notes
---------------------------
id        | user_id | body
---------------------------
bigserial | bigint  | text
---------------------------
```
