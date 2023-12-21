# subtask1
# Initialize variables
n = 0
s = 0
m = float('inf')  # Set initial minimum to positive infinity for comparison
a = 0

# Process the sequence
while True:
    try:
        # Read the next number
        x = int(input("Enter a natural number (-1 to terminate): "))

        # Check if the sequence should terminate
        if x == -1:
            break

        # Update variables
        n += 1
        s += x

        # Update minimum (m) if needed
        m = min(m, x)

    except ValueError:
        print("Invalid input. Please enter a valid natural number.")

# Check if n is 0 and set m and a to -1
if n == 0:
    m = -1
    a = -1
else:
    # Calculate mean (a)
    a = s / n

# Output results
print(f"Count (n): {n}")
print(f"Sum (s): {s}")
print(f"Minimum (m): {m}")
print(f"Mean (a): {a}")
