# py33
py3


def read_and_modify_file(input_filename, output_filename):
    try:
        # Read the file content
        with open(input_filename, 'r') as input_file:
            content = input_file.read()
        
        # Modify the content (example: convert to uppercase)
        modified_content = content.upper()

        # Write the modified content to a new file
        with open(output_filename, 'w') as output_file:
            output_file.write(modified_content)
        
        print(f"File has been successfully modified and saved as '{output_filename}'.")

    except FileNotFoundError:
        print(f"Error: The file '{input_filename}' was not found.")
    except IOError:
        print(f"Error: An I/O error occurred while processing the file '{input_filename}'.")

def main():
    # Ask the user for the filename
    input_filename = input("Enter the filename to read from: ")
    output_filename = input("Enter the name of the file to save the modified content: ")
    
    # Call the read_and_modify_file function
    read_and_modify_file(input_filename, output_filename)

if __name__ == "__main__":
    main()



    Explanation:
Function: read_and_modify_file(input_filename, output_filename)

Reads the content from input_filename.
Modifies the content (in this example, converts it to uppercase).
Writes the modified content to output_filename.
Handles potential errors like file not found or I/O issues.
Main program:

Asks the user for input and output filenames.
Calls the function to read and modify the file.
Error Handling:
If the file does not exist (FileNotFoundError), it will print an error message.
If there is an I/O error (for example, permission issues), it will handle it using IOError.
Example Output:
If the user enters:

Input Filename: input.txt
Output Filename: output.txt
If the input.txt file exists and the program runs successfully, it will modify the content (e.g., convert it to uppercase) and save it in output.txt. If any error occurs (like if the file doesn't exist), it will notify the user.
