# pseudocode
# Display library main menu

Display "Welcome to the Library!"
Display "Please enter your username:"
username = Read user's input

# Loop until user exits
While True:
    Display "Library Menu:"
    Display "1. List available books"
    Display "2. Borrow a book"
    Display "3. Return a book"
    Display "0. Exit"
    
    # Read user's menu choice
    menu_choice = Read user's input
    
    # List available books
    If menu_choice == 1:
        books = Get list of available books with quantity
        Display "Available Books:"
        For each book in books:
            Display book.title, book.author, book.quantity
    
    # Borrow a book
    Else If menu_choice == 2:
        books = Get list of available books with quantity
        Display "Available Books:"
        For each book in books:
            Display book.title, book.author, book.quantity
        Display "Enter the number of the book you want to borrow:"
        book_choice = Read user's input
        If book_choice is not a valid book number or the book is not available:
            Display "Invalid book choice. Please choose again."
        Else:
            book = Get book details for book_choice
            Borrow book
            Display "You have borrowed", book.title
    
    # Return a book
    Else If menu_choice == 3:
        borrowed_books = Get list of borrowed books with quantity
        Display "Borrowed Books:"
        For each book in borrowed_books:
            Display book.title, book.author, book.quantity
        Display "Enter the number of the book you want to return:"
        book_choice = Read user's input
        If book_choice is not a valid book number or the book is not borrowed:
            Display "Invalid book choice. Please choose again."
        Else:
            book = Get book details for book_choice
            Return book
            Display "You have returned", book.title
    
    # Exit program
    Else If menu_choice == 0:
        Display "Thank you for using the Library. Goodbye!"
        Exit program
        
    # Invalid choice
    Else:
        Display "Invalid menu choice. Please choose again."
