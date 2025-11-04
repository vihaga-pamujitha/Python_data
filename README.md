# read_binary.py

def read_binary_file(filename):
    """Reads and prints the first few bytes of a binary file."""
    try:
        with open(filename, 'rb') as file:
            data = file.read(64)  # Read first 64 bytes
            print("First 64 bytes:")
            print(data)
    except FileNotFoundError:
        print(f"Error: The file '{filename}' was not found.")
    except Exception as e:
        print(f"An error occurred: {e}")

if __name__ == "__main__":
    filename = "program.exe"  # Replace with your .exe file name
    read_binary_file(filename)

