# JAVA
DSA Preparation Journey
<b>Data Structures & Algorithms Practice Repository</b><br> ☕ Java | 🧠 Problem Solving | 💻 Interview Preparation

<h1>📘 Curious Freaks – DSA Sheet</h1>

<h1>Basic</h1>

<h2>1.Even or odd</h2>

<p>
  class Solution {
    static boolean isEven(int n) {
        if(n%2==0){
            return true;
        }
    return false;
    }
}
</p>

<h1>Arrays</h1>
<h2>Basic traversal</h2>
<h2>Find the maximum and minimum element in array</h2>


  class Solution {
    public ArrayList<Integer> getMinMax(int[] arr) {
       int min=Integer.MAX_VALUE;
       int max=Integer.MIN_VALUE;
       ArrayList<Integer> list=new ArrayList<>();
       for(int i=0;i<arr.length;i++){
           if(arr[i]<min){
               min=arr[i];
           }
           if(arr[i]>max){
               max=arr[i];
           }
       }
       list.add(min);
       list.add(max);
       return list;
    }
}



<h2>2.Find third largest element in array</h2>

<p>
  class Solution {
    int thirdLargest(int arr[]) {
        // code here
       int n=arr.length;
       if(n<3){
           return -1;
       }
       Arrays.sort(arr);
       int num=arr.length-3;
       return arr[num];
    }
}
</p>

<h2>3.Find missing number in array</h2>

<p>
  class Solution {
    int missingNum(int arr[]) {
       long n=arr.length+1;
       long sum=0;
       for(int i=0;i<arr.length;i++){
           sum=sum+arr[i];
       }
       long formula=n*(n+1)/2;
       long total=(long)formula-sum;
       return (int)total;
    }
}
</p>

<h2>4.Sort 0s, 1s and 2s</h2>

<p>
  class Solution {
    public void sort012(int[] arr) {
        // code here
        int st=0,mid=0,end=arr.length-1;
       while(mid<=end){
           if(arr[mid]==0){
               int temp=arr[st];
               arr[st]=arr[mid];
               arr[mid]=temp;
            st++;
           mid++;
           }
           else if(arr[mid]==1){
              mid++;
           }
           else if(arr[mid]==2){
               int tempp=arr[mid];
               arr[mid]=arr[end];
               arr[end]=tempp;
               end--;
           }
       }
    }
}
</p>

<h1>5.</h1>


```java
public class Main {
    public static void main(String[] args) {
        int[] arr = {4, 2, 1, 5};
        Arrays.sort(arr);
        
        for(int num : arr){
            System.out.print(num + " ");
        }
    }
}
```
