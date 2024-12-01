# Donguler-odev-java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Kullanıcıdan sayı al
        System.out.print("Bir sayı giriniz: ");
        int number = scanner.nextInt();

        int sum = 0;
        int count = 0;

        // 0'dan girilen sayıya kadar olan sayılar için döngü
        for (int i = 0; i <= number; i++) {
            if (i % 3 == 0 && i % 4 == 0) { // 3 ve 4'e tam bölünen sayılar
                sum += i; // sayıyı toplama ekle
                count++; // sayıyı bir arttırır
            }
        }
        // ortalama hesaplama
        if (count > 0) {
            double average = (double) sum / count;
            System.out.println("3 ve 4'e tam bölünen sayıların ortalaması: " + average);
        } else {
            System.out.println("3 ve 4' e tam bölünen herhangi bir sayı yok.");
        }
        scanner.close();
    }
}
