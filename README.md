let Book_NFTs = [];

function mintBook(title, author, genre, publicationYear, ISBN) {
    const book = {
        title: title,
        author: author,
        genre: genre,
        publicationYear: publicationYear,
        ISBN: ISBN
    };
    Book_NFTs.push(book);
    console.log("Minted: " + title);
}

function listBooks() {
    console.log("\n");
    for (let i = 0; i < Book_NFTs.length; i++) {
        const book = Book_NFTs[i];
        console.log(`Title: ${book.title}`);
        console.log(`Author: ${book.author}`);
        console.log(`Genre: ${book.genre}`);
        console.log(`Publication Year: ${book.publicationYear}`);
        console.log(`ISBN: ${book.ISBN}`);
        console.log("\n");
    }
}

function getTotalBooks() {
    return Book_NFTs.length;
}

mintBook("1984", "George Orwell", "Dystopian", 1949, "978-0451524935");
mintBook("To Kill a Mockingbird", "Harper Lee", "Fiction", 1960, "978-0061120084");
mintBook("The Great Gatsby", "F. Scott Fitzgerald", "Tragedy", 1925, "978-0743273565");
mintBook("Pride and Prejudice", "Jane Austen", "Romance", 1813, "978-1503290563");
listBooks();

const totalBooks = getTotalBooks();
console.log("Total No of Books: " + totalBooks);
