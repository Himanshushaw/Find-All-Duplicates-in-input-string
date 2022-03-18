# Find-All-Duplicates-in-input-string
Code in java

import java.util.*;
public class MyClass {
    static void findDupls(String str){
        //create hashmap with character , Integer
        HashMap<Character,Integer> count=new HashMap<Character,Integer>();
        
        //first time store the element as initialize the count as 1
        for(int i=0;i<str.length();i++){
            if(!count.containsKey(str.charAt(i))){
                count.put(str.charAt(i),1);
            }
            //if already exist the increment the count with 1
            else{
                count.put(str.charAt(i),count.get(str.charAt(i)) +1);
            }    
        }
        
        for(Map.Entry map: count.entrySet()){
            int val=((int)map.getValue());
            char key=(char)map.getKey();
            //if value is > 1
            if(val>1){
            System.out.println(key +" count is :"+val);
            }
        }
        
        
        
    }

public static void  main(String[] args){
    String str="geeksforgeeks";
    findDupls(str);
}    
    }
