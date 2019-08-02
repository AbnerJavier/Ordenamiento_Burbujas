//# Ordenamiento_Burbujas
package burbuajs;

import java.util.Scanner;

public class Burbuajs {
    public static void main(String[] args) {
        int n;
        Scanner sc = new Scanner (System.in);
        System.out.println("De que tamaño quiere su arreglo: ");
        n = sc.nextInt();
        int array[] = new int[n];
        for(int con=0;con<array.length;con++)
        {
            System.out.println("Ingrese dato "+(con+1));
            array[con] = sc.nextInt();
        }
        int aux, i, j;
        boolean swapped = false;
        do
        {
            swapped = false;
        for(i=1;i<array.length;i++)
            {
                if(array[i] < array[i-1])
                {
                    aux = array[i-1];
                    array[i-1] = array[i];
                    array[i] = aux;
                    swapped = true;
                }
            }
        }while(swapped == true);
        System.out.println("\n\nMétodo de Burbujas");
        for(j = 0;j<array.length;j++)
        {
            System.out.println(array[j]);
        }
    }
    
}
