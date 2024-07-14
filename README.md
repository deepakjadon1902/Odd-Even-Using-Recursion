import java.util.Scanner;
public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int N = scanner.nextInt();
        scanner.close();

        printOddDecreasing(N);
        printEvenIncreasing(1, N);
    }
    private static void printOddDecreasing(int n) {
        if (n > 0) {
            if (n % 2 != 0) {
                System.out.println(n);
            }
            printOddDecreasing(n - 1);
        }
    }
    private static void printEvenIncreasing(int current, int max) {
        if (current <= max) {
            if (current % 2 == 0) {
                System.out.println(current);
            }
            printEvenIncreasing(current + 1, max);
        }
    }
}
