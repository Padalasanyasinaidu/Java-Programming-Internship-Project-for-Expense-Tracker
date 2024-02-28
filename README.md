import java.io.*;
import java.util.*;

class Expense {
    String date;
    String category;
    double amount;

    public Expense(String date, String category, double amount) {
        this.date = date;
        this.category = category;
        this.amount = amount;
    }

    // Additional methods if needed
}

class ExpenseTracker {
    private List<Expense> expenses;
    private String currentUser;

    public ExpenseTracker(String currentUser) {
        this.currentUser = currentUser;
        this.expenses = new ArrayList<>();
    }

    public void addExpense(String date, String category, double amount) {
        Expense expense = new Expense(date, category, amount);
        expenses.add(expense);
    }

    public void displayExpenses() {
        for (Expense expense : expenses) {
            System.out.println("Date: " + expense.date + ", Category: " + expense.category + ", Amount: " + expense.amount);
        }
    }

    // Additional methods for sorting, filtering, and category-wise summation

    // File handling methods for saving and loading data
}

public class Main {
    public static void main(String[] args) {
        // Example usage:
        ExpenseTracker expenseTracker = new ExpenseTracker("User123");

        // User adds expenses
        expenseTracker.addExpense("2024-02-23", "Groceries", 50.0);
        expenseTracker.addExpense("2024-02-24", "Utilities", 100.0);

        // Display all expenses
        expenseTracker.displayExpenses();

        // Save and load data to/from files
        // Implement user interface (UI) as per your needs
    }
}
