# Fibonacci-Sequence

def generate_fibonacci(limit):
    fibonacci_sequence = [0, 1]  # Initialize with the first two Fibonacci numbers
    
    while True:
        next_number = fibonacci_sequence[-1] + fibonacci_sequence[-2]
        if next_number > limit:
            break
        fibonacci_sequence.append(next_number)
    
    return fibonacci_sequence

# Input from the user
limit = int(input("Enter a positive integer: "))

if limit <= 0:
    print("Please enter a positive integer.")
else:
    fibonacci_result = generate_fibonacci(limit)
    print("Fibonacci sequence up to", limit, ":", fibonacci_result)

