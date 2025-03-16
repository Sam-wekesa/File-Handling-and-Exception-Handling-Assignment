def modify_file():
    # Ask user for filename
    filename = input("Enter the filename to read: ")

    try:
        # Open the file for reading
        with open(filename, "r") as file:
            content = file.read()

        # Modify content (e.g., convert to uppercase)
        modified_content = content.upper()

        # Write modified content to a new file
        new_filename = "modified_" + filename
        with open(new_filename, "w") as new_file:
            new_file.write(modified_content)

        print(f"File modified successfully! Saved as {new_filename}")

    except FileNotFoundError:
        print("Error: The file does not exist. Please check the filename.")
    except IOError:
        print("Error: Unable to read the file.")

# Run the function
modify_file()
# File-Handling-and-Exception-Handling-Assignment
