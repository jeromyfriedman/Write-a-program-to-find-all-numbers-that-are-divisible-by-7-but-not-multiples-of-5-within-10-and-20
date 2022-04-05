# Write-a-program-to-find-all-numbers-that-are-divisible-by-7-but-not-multiples-of-5-within-10-and-20
Using a for . loop
package vn.viettuts.baitap;
 
import java.util.ArrayList;
import java.util.List;
 
public class Bai01 {
     public static void main(String[] args) {
         List<Integer> list = new ArrayList<Integer>();
         for (int i = 10; i < 201; i++) {
             if ((i % 7 == 0) && (i % 5 != 0)) {
                 list.add(i);
             }
         }
         // display the list on the screen
         showList(list);
     }
 
     public static void showList(List<Integer> list) {
         if (list != null && !list.isEmpty()) {
             int size = list.size();
             for (int i = 0; i < size - 1; i++) {
                 System.out.print(list.get(i) + ", ");
             }
             System.out.println(list.get(size - 1));
         }
     }
}
