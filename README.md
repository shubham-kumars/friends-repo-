// solution-3.js
const book1 = new Book("JavaScript Basics", "John Doe", Book.generateISBN(), 5);
const book2 = new Book("Advanced JavaScript", "Jane Smith", Book.generateISBN(), 3);
const book3 = new Book("Web Development", "Alice Brown", Book.generateISBN(), 2);

// Create a new Library instance
const library = new Library();

// Add books to the library
library.addBook(book1);
library.addBook(book2);
library.addBook(book3);

// Display all books in the library
console.log("All Books in the Library:");
library.displayBooks();

// Search for books by title or author
console.log("\nSearch for books with the keyword 'JavaScript':");
const searchResults = library.searchBooks("JavaScript");
searchResults.forEach(book => console.log(book.title));

// Remove a book from the library
console.log("\nRemoving book:", book1.title);
library.removeBook(book1.isbn);

// Display all books after removal
console.log("\nBooks in the Library after removal:");
library.displayBooks();
