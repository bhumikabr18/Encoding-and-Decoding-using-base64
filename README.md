# Encoding-and-Decoding-using-base64
This is my first git repository
Author - Bhumika



import base64
def encode_base64(data):
    #convert string to bytesand then encode
    encoded_bytes = base64.b64encode(data.encode('utf-8'))
    encoded_str = encoded_bytes.decode('utf-8')
    return encoded_str
def decode_base64(encoded_data):
    #convert base64 string back to bytes and then decode
    decoded_bytes = base64.b64decode(encoded_data)
    decoded_str = decoded_bytes.decode('utf-8')
    return decoded_str
def main():
    while true:
          print("choose an option:")
          print("1. encode to base64")
          print("2. decode from base64")
          print("3. exit")

           choice = input("Enter your choice (1/2/3): ")

        if choice == '1':
            user_input = input("Enter the string/number to encode: ")
            encoded_result = encode_base64(user_input)
            print(f"Encoded Base64: {encoded_result}")
        elif choice == '2':
            encoded_input = input("Enter the Base64 encoded string to decode: ")
            try:
                decoded_result = decode_base64(encoded_input)
                print(f"Decoded string: {decoded_result}")
            except Exception as e:
                print(f"Error decoding: {e}")
        elif choice == '3':
            print("Exiting the program.")
            break
        else:
            print("Invalid choice. Please try again.")

# Call the main function directly
main()
