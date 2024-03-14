# help-shopkeeper
You are developing a program for a shopkeeper to calculate the total bill for a customer's purchase. The shop sells three different types of products: books, electronics, and clothing. Each type of product has a different tax rate applied. Write a program that takes the type of product and the purchase amount as input, calculates the total bill including tax, and displays it to the customer.

Tax Rates: Books: 5% Electronics: 12% Clothing: 8%
def calculate_total_bill(product_type, purchase_amount):
    tax_rates = {"books": 0.05, "electronics": 0.12, "clothing": 0.08}
    tax_rate = tax_rates.get(product_type, 0)
    total_bill = purchase_amount * (1 + tax_rate)
    return round(total_bill, 2)

def main():
    product_type = input().lower()
    purchase_amount = float(input())
    total_bill = calculate_total_bill(product_type, purchase_amount)
    print(total_bill)

if __name__ == "__main__":
    main()

