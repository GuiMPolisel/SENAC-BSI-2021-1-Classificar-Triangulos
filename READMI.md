import java.util.Scanner;

public class main {    
    public static void main(String[] args){
        float num1, num2, num3, A, B, C;
        Scanner leitor = new Scanner(System.in);

        System.out.print("Dado os lados"+"\n");

        System.out.print("Primeiro número: ");
        num1 = leitor.nextInt();

        System.out.print("Segundo número: ");
        num2 = leitor.nextInt();

        System.out.print("Terceiro número: ");
        num3 = leitor.nextInt();

        if( ( num1 > num2 && num1 > num3 ) && ( num2 > num3 ) ) { 
            A = num1;
            B = num2;
            C = num3;
        }if( ( num1 > num2 && num1 > num3 ) && ( num3 > num2) ) { 
            A = num1;
            B = num3;
            C = num2;
        }if( ( num2 > num1 && num2 > num3 ) && ( num1 > num3 ) ) { 
            A = num2;
            B = num1;
            C = num3;
        }if( ( num2 > num1 && num2 > num3 ) && ( num3 > num1 ) ) { 
            A = num2;
            B = num3;
            C = num1;
        }if( ( num3 > num1 && num3 > num2 ) && ( num1 > num2 ) ) { 
            A = num3;
            B = num1;
            C = num2;           
        }else { 
            A = num3;
            B = num2;
            C = num1;
        }

         if(2*A == B + C){
            System.out.print("Triângulo Equilátero. ");
        }else if(A*A > B*B + C*C){
            System.out.print("Triângulo Escaleno. ");
        }else if(A*A < B*B + C*C){
            System.out.print("Triângulo Isósceles.  ");
        }else{
            System.out.print("Não forma triângulo. ");
        }       
    }

}
