import java.util.HashMap;
import java.util.Scanner;

class BankAccount {
    private String accountNumber;
    private String holderName;
    private double balance;

    public BankAccount(String accountNumber, String holderName, double balance) {
        this.accountNumber = accountNumber;
        this.holderName = holderName;
        this.balance = balance;
    }

    public void deposit(double amount) {
        if (amount > 0) {
            balance += amount;
            System.out.println("₹" + amount + " deposited successfully.");
        } else {
            System.out.println("Invalid amount!");
        }
    }

    public void withdraw(double amount) {
        if (amount > 0 && amount <= balance) {
            balance -= amount;
            System.out.println("₹" + amount + " withdrawn successfully.");
        } else {
            System.out.println("Insufficient balance or invalid amount!");
        }
    }

    public void displayBalance() {
        System.out.println("Account Balance: ₹" + balance);
    }
}

public class BankManagement {
    public static void main(String[] args) {
        HashMap<String, BankAccount> accounts = new HashMap<>();
        Scanner sc = new Scanner(System.in);

        while (true) {
            System.out.println("\n1. Create Account\n2. Deposit\n3. Withdraw\n4. Check Balance\n5. Exit");
            System.out.print("Choose an option: ");
            int choice = sc.nextInt();
            sc.nextLine();

            switch (choice) {
                case 1:
                    System.out.print("Enter Account Number: ");
                    String accNum = sc.nextLine();
                    System.out.print("Enter Holder Name: ");
                    String name = sc.nextLine();
                    accounts.put(accNum, new BankAccount(accNum, name, 0));
                    System.out.println("Account created successfully!");
                    break;
                case 2:
                    System.out.print("Enter Account Number: ");
                    accNum = sc.nextLine();
                    if (accounts.containsKey(accNum)) {
                        System.out.print("Enter Amount: ");
                        double amount = sc.nextDouble();
                        accounts.get(accNum).deposit(amount);
                    } else {
                        System.out.println("Account not found!");
                    }
                    break;
                case 3:
                    System.out.print("Enter Account Number: ");
                    accNum = sc.nextLine();
                    if (accounts.containsKey(accNum)) {
                        System.out.print("Enter Amount: ");
                        double amount = sc.nextDouble();
                        accounts.get(accNum).withdraw(amount);
                    } else {
                        System.out.println("Account not found!");
                    }
                    break;
                case 4:
                    System.out.print("Enter Account Number: ");
                    accNum = sc.nextLine();
                    if (accounts.containsKey(accNum)) {
                        accounts.get(accNum).displayBalance();
                    } else {
                        System.out.println("Account not found!");
                    }
                    break;
                case 5:
                    System.out.println("Exiting...");
                    sc.close();
                    return;
                default:
                    System.out.println("Invalid choice! Try again.");
            }
        }
    }
}
