# Java-Programming


import java.util.ArrayList;
import java.util.Arrays;
import java.util.Collections;

public class XOR {
    public static void main(String[] args) {
        int a[] ={2,1,2,2};
        ArrayList<Integer>al=new ArrayList<>();
        int k=2;
        int p=a.length-k;
        boolean a1=false,a2=false;
        for(int i=k;i<p;i++) {
            a1 = true;
            a2 = true;
            for (int j = (i - k); j < k; j++) {
                if (a[j] < a[j + 1]) {
                    a1 = false;
                    break;
                }
            }
            System.out.println(a1 + " " + i);

            for (int l = k + 1; l < i + k; l++) {
                if (a[l] > a[l + 1]) {
                    a2 = false;
                    break;
                }
            }
            System.out.println(a2 + " " + i);
            if (a1 && a2) {
                al.add(i);
            }
        }
        a1=true;
        for(int i=p-k;i<k;i++)
        {
            if(a[i]<a[i+1])
            {
                a1=false;
                break;
            }
        }
        if(a1)
        {
            al.add(p);
        }
    Collections.sort(al);
        System.out.println(al);
    }

}
