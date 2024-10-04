//**task-2**//
import java.io.PrintStream;
import java.util.Scanner;

public class task2 {
   public task2() {
   }

   public static void main(String[] var0) {
      Scanner var1 = new Scanner(System.in);
      System.out.print("Enter the number of subjects: ");
      int var2 = var1.nextInt();
      int[] var3 = new int[var2];
      int var4 = 0;

      for(int var5 = 0; var5 < var2; ++var5) {
         System.out.print("Enter marks obtained in subject " + (var5 + 1) + " (out of 100): ");
         var3[var5] = var1.nextInt();
         var4 += var3[var5];
      }

      double var8 = (double)var4 / (double)var2;
      char var7;
      if (var8 >= 90.0) {
         var7 = 'A';
      } else if (var8 >= 80.0) {
         var7 = 'B';
      } else if (var8 >= 70.0) {
         var7 = 'C';
      } else if (var8 >= 60.0) {
         var7 = 'D';
      } else {
         var7 = 'F';
      }

      System.out.println("\n--- Results ---");
      System.out.println("Total Marks: " + var4 + " out of " + var2 * 100);
      PrintStream var10000 = System.out;
      Object[] var10002 = new Object[]{var8};
      var10000.println("Average Percentage: " + String.format("%.2f", var10002) + "%");
      System.out.println("Grade: " + var7);
      var1.close();
   }
}

