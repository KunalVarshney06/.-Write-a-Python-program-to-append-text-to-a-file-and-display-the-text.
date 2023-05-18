# .-Write-a-Python-program-to-append-text-to-a-file-and-display-the-text.
def append_text_to_file(file_path, text):
    try:
        with open(file_path, 'a') as file:
            file.write(text + '\n')
        print("Text appended successfully.")
    except IOError:
        print("An error occurred while writing to the file.")

def display_file_contents(file_path):
    try:
        with open(file_path, 'r') as file:
            contents = file.read()
            print("File contents:")
            print(contents)
    except FileNotFoundError:
        print("File not found.")
    except IOError:
        print("An error occurred while reading the file.")

# Example usage
file_path = 'path/to/your/text/file.txt'  # Replace with the actual file path
text_to_append = "This is the new text to append"
append_text_to_file(file_path, text_to_append)
display_file_contents(file_path)
