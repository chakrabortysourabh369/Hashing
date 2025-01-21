# Hashing
Hashing data structure.

/*import java.util.*;
 class hashing {

    int BUCKET;
    ArrayList<LinkedList<Integer>>table;
    
    hashing(int b){

         BUCKET=b;
         table=new ArrayList<LinkedList<Integer>>();
         for(int i=0;i<b;i++)
            table.add(new LinkedList<Integer>());
          }
          void insert(Integer k)
          {
            int i= k % BUCKET;
            table.get(i).add(k);
          }

          boolean search(Integer K) 
          {

            int i=K % BUCKET;
            return table.get(i).contains(K);
           }
               void delete(Integer K)
               {

                int i=K%BUCKET;
                 table.get(i).remove(K);
               } 
}

               class sourabh{
              public static void main(String args[]){

                hashing mh=new hashing(7);
                mh.insert(10);
                mh.insert(20);
                mh.insert(15);
                mh.insert(7);
                System.out.println(mh.search(10));
                mh.delete(15);
                System.out.println(mh.search(15));
              }
}

//   (1).HashSet functions       1.add()  2.contains()     3.Iterator<>   

import java.util.*;
class hashing{

         public static void main(String args[]){

          HashSet<String> h=new HashSet<String>();

          h.add("gfg");
          h.add("courses");
          h.add("ide");

          System.out.println(h);
          System.out.println(h.contains("gfg"));

          //hasNext()    //i.next()

          Iterator<String> i=h.iterator();

          while(i.hasNext()){

            System.out.println(i.next() + " ");
          }

         }
}

  //       4.remove()           5.size()         6.isEmpty()
import java.util.*; 

class hashing 
{ 
    public static void main(String[]args) 
    { 
        HashSet<String> h = new HashSet<String>(); 

        
        h.add("gfg"); 
        h.add("courses"); 
        h.add("ide"); 

      
        System.out.println(h.size());
        
        h.remove("ide");
        System.out.println(h.size());
        
        for(String s: h)
        {
            System.out.print(s+" ");
        }
        
        
        
        System.out.println("\n"+h.isEmpty());
        
    } 
} 

   // HashMap functions   1.put  2.size()   3.iterations(Entry<>,entrySet)

import java.util.*;
class hashing{

  public static void main(String args[]){

    HashMap<String , Integer> m=new HashMap<>();
 
    //add elements to Map
    m.put("gfg",10);
    m.put("courses",15);
    m.put("ide",20);

    //print size and content

    System.out.println(m);
    System.out.print(m.size());

    
    for(Map.Entry<String ,Integer> e:m.entrySet()){
           System.out.println(e.getKey() +" " + e.getValue());
    }
  }
}   

//program 1. count of distinct elements 

  import java.util.*;
  class hashing{
    public static void main(String args[]){
      int arr[]={10,20,30,40,50,50,40};
      int n=arr.length;
               HashSet <Integer>h =new HashSet<>();
               for(int i=0;i<n;i++){
                      h.add(arr[i]);
               }
               int size=h.size();
               System.out.println(size);

    }
}

  //program 2: frequency of elements(HashMap)

  import java.util.*;
  class hashing{
              
    public static void main(String args[]){
      int arr[]={10,20,30,40,50,50,40};
      int n=arr.length;
      HashMap<Integer,Integer> h=new HashMap<>();
      for(int x:arr)
         {

          //getOrDefault(x,0)->key,default value

          h.put(x,h.getOrDefault(x,0)+1);
         }
          for(Map.Entry<Integer,Integer> e:h.entrySet()){
            System.out.println(e.getKey() +"," +e.getValue() );

          }
    }          
  }
  //program 3.Print the intersection of two unsorted arrays

  import java.util.*;
  class hashing{
              
    public static void main(String args[]){
      int a[]={10,20,30,40,50};
      int b[]={10,50};
      int n=a.length, m=b.length;

      HashSet<Integer>h=new HashSet<>();
      for(int i=0;i<m;i++)
      h.add(b[i]);

      for(int i=0;i<n;i++)
       if(h.contains(a[i]))
       {
        System.out.println(a[i]);
       }
      }
    }

    //program 4.Union of two unsorted arrays
    import java.util.*;
     class hashing{
              
    public static void main(String args[]){
      int a[]={10,20,30,40,50,60};
      int b[]={10,50};
      int n=a.length, m=b.length;

      HashSet<Integer>h=new HashSet<>();
      for(int i=0;i<n;i++){
      h.add(a[i]);}

      for(int i=0;i<m;i++){
       h.add(b[i]);}

       int size=h.size();
       System.out.println(size);

       for(int x:h){
        System.out.println(h);
       }
      }
    }

    //program 5. Pair with given sum in unsorted array 

    import java.util.*;
    class hashing{

      public static void main(String args[]){

        int arr[]={8,3,4,2,5};
        int sum=6;

        HashSet<Integer> h=new HashSet<Integer>();

        for(int i=0;i<arr.length;i++){

          if(h.contains(sum-arr[i])){
            System.out.println("true " + i);
          }

          else{
            h.add(arr[i]);
          }
        }
      }
    }

    //program 6. Subarray with zero sum 

    import java.util.*;
    class hashing{

      public static void main(String args[]){

        int arr[]={-3,4,-3,-1,1};
        int pre_sum=0;

        HashSet<Integer> h=new HashSet<>();

        for(int i=0;i<arr.length;i++){
          pre_sum+=arr[i];
          if(h.contains(pre_sum)){
            System.out.println("true");
            break;
          }
          else{
            h.add(pre_sum);
          }
        }
        if(pre_sum==0)System.out.println("true");
      }
    }  

    //program 7. Subarray with given sum

    import java.util.*;
    class hashing {

      public static void main(String args[]){
        int arr[]={5,8,6,12,3,1};
        int sum=22;
        HashSet <Integer> h=new HashSet<>();
        int pre_sum=0;

        for(int i=0;i<arr.length;i++){

          //calculating pre_sum
          pre_sum+=arr[i];
          if(pre_sum==sum)
          System.out.println("true");

          if(h.contains(pre_sum-sum))
          System.out.print("true");

          else{
            h.add(pre_sum);
          }
        }
      }
    } 

    //program :8 Longest Subarray for given sum

    import java.util.*;
    class hashing{

      public static void main(String args[]){

        int arr[]={3,1,0,1,8,2,3,6};
        int sum=5; 
        HashMap <Integer,Integer> m=new HashMap<Integer,Integer>();
        int pre_sum=0;   //try to initialize things separetly
        int res=0;
  
        for(int i=0;i<arr.length;i++){
          pre_sum+=arr[i];
          if(pre_sum==sum){
            res=res+1;
          }

          //In HashMap (containsKey) 

          if(m.containsKey(pre_sum)==false){
              m.put(pre_sum,i);
          }

          if(m.containsKey(pre_sum-sum)){

            res=Math.max(res,i-m.get(pre_sum-sum)); //To get the location m.get
          }
        }
        System.out.println(res);
      }
    }*/

    //program 9: Longest subarray with equal 0's & 1's.
    





   
                



