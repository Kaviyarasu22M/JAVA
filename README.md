# JAVA
DSA Preparation Journey
<b>Data Structures & Algorithms Practice Repository</b><br> ☕ Java | 🧠 Problem Solving | 💻 Interview Preparation

<h1>📘 Curious Freaks – DSA Sheet</h1>

<h1>Basic</h1>

<h2>1.Even or odd</h2>

```
  class Solution {
    static boolean isEven(int n) {
        if(n%2==0){
            return true;
        }
    return false;
    }
}
```

<h1>Arrays</h1>
<h2>Basic traversal</h2>
<h2>Find the maximum and minimum element in array</h2>


  ```class Solution {
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
```


<h2>2.Find third largest element in array</h2>

```
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
```

<h2>3.Find missing number in array</h2>

```
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
```

<h2>4.Sort 0s, 1s and 2s</h2>

```
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
```

<h2>5.Check if two arrays are equal or not</h2>

```class Solution {
    public static boolean checkEqual(int[] a, int[] b) {
        int alen=a.length;
        Arrays.sort(a);
        Arrays.sort(b);
        for(int i=0;i<alen;i++){
            if(a[i]!=b[i]){
                return false;
            }
        }
        return true;
    }
}```

<h2>Rotate the array by 1</h2>

```class Solution {
    public void rotate(int[] arr) {
       int n=arr.length;
       int last=arr[n-1];
       for(int i=n-1;i>0;i--){
           arr[i]=arr[i-1];
       }
       arr[0]=last;
    }
}```

<h1>Two pointer</h1>

<h2>1.Find pair with given sum</h2>




