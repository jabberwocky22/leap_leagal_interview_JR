## LEAP Dev NextJS Take Home Test

This is a very basic Book Store with static data and simple CRUD support.

Push this up to a public Github repository please. We will assess both code and commits in order to discern how you approach problem-solving.

Please do not use AI in any way, shape, or form.

---

Please implement the following:

1. Use a component library to make the UI and UX more appealing and user friendly.

[Explain here why you chose the one you did]

2. Implement dark mode that includes a switcher to go back to light mode.

3. Deleting a book displays a JavaScript alert. Replace this with modern UX.

4. Add a rating system that goes up to 5 stars.

5. There is a bug in the code. Find it and fix it.

[Explain here what the bug was and how you fixed it]

A:  The bug I found is that when updating book details, it remained old data instead of updated data.
    So I went through the codebase and invested the update function, what I got is -
    when we set book data, we used `book.id === selectedBook?.id ? { ...updatedBook, ...book } : book`,
    which is wrong because object spread syntax merges the properties from left to right,
    eg: { ...A, ...B } will spread A first and then overwrites the same properties using value in B,
    so { ...updatedBook, ...book } actually means the updated data will be overwritted by the old data.

Good luck and have fun!
