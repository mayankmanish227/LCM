//# LCM
import java.util.*;
import java.io.*;

public class HelloWorld
{

     public static void main(String []args)throws IOException
     {
        Scanner sc=new Scanner(System.in);
         List<Integer> li=new ArrayList<>();
         int q=0;
        while(sc.hasNext())
        {
            li.add(sc.nextInt());
        }
        Collections.sort(li);
        int i=1;
        int j=li.get(0);
        while(i==1)
        {
            int count=0;
            for(int k=0;k<li.size();k++)
            {
                if(j%li.get(k)==0)
                {
                    count++;
                }
                else
                {
                    j++;
                }
            }
            if(count==li.size())
            {
                break;
            }
        }
        System.out.print(j);
     }
}
