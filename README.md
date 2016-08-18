# sample1
codes

hey folks,
This is a code of service lane.

import java.io.*;
import java.util.*;

public class Solution {

    public static void main(String[] args) {
        /* Enter your code here. Read input from STDIN. Print output to STDOUT. Your class should be named Solution. */
        Scanner sc=new Scanner(System.in);
        int number=sc.nextInt();
        int testCase=sc.nextInt();
        int entryToLane,exitFromLane;
        int min=0;
        
        int[] width= new int[number];
        for(int iter=0;iter<number;iter++){
            width[iter]=sc.nextInt();
        }
        
        for(int iter=0;iter<testCase;iter++){
            entryToLane=sc.nextInt();
            exitFromLane=sc.nextInt();
            
            if(entryToLane<=exitFromLane && entryToLane>=0){
                min=width[entryToLane];
                for(int k=entryToLane+1;k<=exitFromLane;k++){
                    if(width[k]<min){
                        min=width[k];
                    }
                }
            }
            
            System.out.println(min);
        }
    }
}
