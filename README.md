# Comp-10.6

import java.util.concurrent.TimeUnit;
public class Comp106 {

    public static void main(String[] args) throws InterruptedException{
		final int LINE=5,SPACE=10;
        String[] list= new String[LINE];
        for(int i=0;i<LINE;i++){
            list[i]="";
            for(int j=0;j<(int)(Math.random()*LINE)+1;j++)
            list[i]+="-";
            }
       //random list created
        for (String list1 : list) {
            System.out.println(list1);
            }
        
        for(int i=0;i<list.length-1;i++){
            for(int p=0;p<SPACE;p++){
                System.out.println("");
                }
            //sleep
            TimeUnit.SECONDS.sleep(1);
            String tem;
            int min=i;
            for(int j=i+1;j<list.length;j++){
                if(list[min].compareTo(list[j])>0){
                    min=j;
                }
            }
            tem=list[i];
            list[i]=list[min];
            list[min]=tem;
           
            for(int p=0;p<list.length;p++){
                System.out.println(list[p]);
            if(p!=list.length-1&p==i)
                } 
           
           
        }
        //new line and output
        for(int p=0;p<SPACE;p++){
                System.out.println("");
                } 
        for (String list1 : list){
            System.out.println(list1);
            }
       
       
       
    }
    
}
