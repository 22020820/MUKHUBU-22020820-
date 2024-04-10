# MUKHUBU-22020820-import java.util.Scanner;

public class CompoundInterestCalculator {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter the principal amount: ");
        double principal = scanner.nextDouble();

        System.out.print("Enter the interest rate (in percentage): ");
        double rate = scanner.nextDouble();

        System.out.print("Enter the time period (in years): ");
        double time = scanner.nextDouble();

        System.out.print("Enter the number of times interest is compounded per year: ");
        int n = scanner.nextInt();

        double amount = calculateCompoundInterest(principal, rate, time, n);
        System.out.println("Compound Interest: " + amount);
    }

    public static double calculateCompoundInterest(double principal, double rate, double time, int n) {
        double amount = principal * Math.pow(1 + (rate / (n * 100)), n * time);
        return amount - principal;
    }
}
