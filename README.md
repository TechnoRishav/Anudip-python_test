# Anudip-python_test

# Python program to calculate compound interest

# Function to calculate compound interest
def calculate_compound_interest(principal_amount, annual_rate, time_period):
    """
    This function calculates compound interest using the formula:
    A = P * (1 + R/100)^T
    Where:
    A = Final amount
    P = Principal amount
    R = Annual interest rate
    T = Time in years

    :param principal_amount: The initial amount of money (Principal)
    :param annual_rate: The annual interest rate in percentage
    :param time_period: The time period in years
    :return: Compound interest and final amount
    """
    # Calculate final amount using the compound interest formula
    final_amount = principal_amount * (1 + annual_rate / 100) ** time_period

    # Compound interest is the difference between final amount and principal amount
    compound_interest = final_amount - principal_amount

    return compound_interest, final_amount

# Main block to execute the program
if __name__ == "__main__":
    # Input principal amount, annual interest rate, and time period
    principal = float(input("Enter the principal amount: "))
    rate = float(input("Enter the annual interest rate (in %): "))
    time = float(input("Enter the time period (in years): "))

    # Call the function to calculate compound interest
    interest, total_amount = calculate_compound_interest(principal, rate, time)

    # Output the results
    print("\nResults:")
    print(f"Principal Amount: {principal}")
    print(f"Annual Interest Rate: {rate}%")
    print(f"Time Period: {time} years")
    print(f"Compound Interest: {interest:.2f}")
    print(f"Total Amount after {time} years: {total_amount:.2f}")

# Input
Principal: 1000
Annual Interest Rate: 5
Time Period: 2

# Output
Results:
Principal Amount: 1000.0
Annual Interest Rate: 5.0%
Time Period: 2 years
Compound Interest: 102.50
Total Amount after 2 years: 1102.50
