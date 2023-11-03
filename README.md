import java.util.Scanner;
import java.util.InputMismatchException;
public class SquareRootProg {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter the number: ");

        try{

        int  num = sc.nextInt();
            if(num < 0){
                throw new ArithmeticException("can't enter -ve value.");
            }
            double squareRoot = Math.sqrt(num);
            System.out.println(squareRoot);

        } catch (ArithmeticException e) {
            throw new RuntimeException(e);
        } catch (InputMismatchException e){
            System.out.println("Invalid Input");
        } finally {
            sc.close();
        }
    }
}
