# Stone_Paper_Scissor
package com.company;
import java.util.*;
public class challenge {
    public static void main(String args[])
    {
        int b=3;//upperbond 3 never include
        Random r=new Random();
        Scanner sc=new Scanner(System.in);
        int i=0;
        int a=0,c=0,d=0,e=0;//a(0->rock,1->paper,2->siecer),b(0->rock,1->paper,2->siecer) d=user input e=random input
        System.out.println("Enter Your name to accept challenge");
        String se = sc.nextLine();
        System.out.println("Challenge Accepted");
        System.out.println(se+" VS System");
        while(i<5) {
            a = r.nextInt(b);
            c=sc.nextInt();
            //output logic
            System.out.print("System input -> ");
            if(a==0)
            {
                System.out.println("Rock");
            }else if(a==1)
            {
                System.out.println("Paper");
            }else if(a==2)
            {
                System.out.println("Scissor");
            }

            System.out.print(se+" input -> ");
            if(c==0)
            {
                System.out.println("Rock");
            }else if(c==1)
            {
                System.out.println("Paper");
            }else if(c==2)
            {
                System.out.println("Scissor");
            }

            //Main Logic
            if((a==0 && c==0)||(a==1 && c==1)||(a==2 && c==2))
            {

            }else if(a==0 && c==1)
            {
                d++;
            }else if(a==0 && c==2)
            {
                e++;
            }else if(a==1 && c==0)
            {
                e++;
            }else if(a==1 && c==2)
            {
                d++;
            }
            else if(a==2 && c==0)
            {
                d++;
            }else if(a==2 && c==1)
            {
                e++;
            }

            //System.out.println(a);
            System.out.println("System Points -> "+e);
            System.out.println(se+" Points -> "+d);


            i++;
        }
        if(e>d)
        {
            System.out.println("\n");
            System.out.println("System wins");
            System.out.println("Best of Luck for Next Time");
        }else if(e==d)
        {
            System.out.println("\n");
            System.out.println("Draw");
            System.out.println("Please Try again");
        }else if(e<d)
        {
            System.out.println("\n");
            System.out.println(se+" wins");
        }
    }
}
