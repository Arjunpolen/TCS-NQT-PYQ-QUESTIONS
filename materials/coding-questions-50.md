# 50 Coding Questions

## 1. Check Even or Odd

```java
import java.util.*;
class Main{
public static void main(String[] args){
Scanner sc = new Scanner(System.in);
int n = sc.nextInt();
System.out.println(n % 2 == 0 ? "Even" : "Odd");
}
}
```

## 2. Check Prime Number

```java
import java.util.*;
class Main{
public static void main(String[] args){
Scanner sc = new Scanner(System.in);
int n = sc.nextInt();
boolean prime = true;
if(n <= 1) prime = false;
for(int i = 2; i <= Math.sqrt(n); i++){
if(n % i == 0){
prime = false;
break;
}
}
System.out.println(prime ? "Prime" : "Not Prime");
}
}
```

## 3. Factorial of a Number

```java
import java.util.*;
class Main{
public static void main(String[] args){
Scanner sc = new Scanner(System.in);
int n = sc.nextInt();
long fact = 1;

for(int i = 1; i <= n; i++)
fact *= i;
System.out.println(fact);
}
}
```

## 4. Fibonacci Series (First N Terms)

```java
import java.util.*;
class Main{
public static void main(String[] args){
Scanner sc = new Scanner(System.in);
int n = sc.nextInt();
int a = 0, b = 1;
for(int i = 1; i <= n; i++){
System.out.print(a + " ");
int c = a + b;
a = b;
b = c;
}
}
}
```

## 5. Reverse a Number

```java
import java.util.*;
class Main{
public static void main(String[] args){
Scanner sc = new Scanner(System.in);
int n = sc.nextInt();
int rev = 0;
while(n != 0){
rev = rev * 10 + n % 10;
n /= 10;
}
System.out.println(rev);
}
}
```

## 6. Check Palindrome Number

```java
import java.util.*;
class Main{
public static void main(String[] args){
Scanner sc = new Scanner(System.in);
int n = sc.nextInt();
int temp = n, rev = 0;
while(n != 0){
rev = rev * 10 + n % 10;
n /= 10;
}
System.out.println(temp == rev ? "Palindrome" : "Not Palindrome");

}
}
```

## 7. Armstrong Number

```java
import java.util.*;
class Main{
public static void main(String[] args){
Scanner sc = new Scanner(System.in);
int n = sc.nextInt();
int temp = n, sum = 0;
while(n != 0){
int digit = n % 10;
sum += digit * digit * digit;
n /= 10;
}
System.out.println(temp == sum ? "Armstrong" : "Not Armstrong");
}
}
```

## 8. Sum of Digits

```java
import java.util.*;
class Main{
public static void main(String[] args){
Scanner sc = new Scanner(System.in);
int n = sc.nextInt();
int sum = 0;
while(n != 0){
sum += n % 10;
n /= 10;
}
System.out.println(sum);
}
}
```

## 9. Largest of Three Numbers

```java
import java.util.*;
class Main{
public static void main(String[] args){
Scanner sc = new Scanner(System.in);
int a = sc.nextInt(), b = sc.nextInt(), c = sc.nextInt();
int max = Math.max(a, Math.max(b, c));
System.out.println(max);
}
}
```

## 10. GCD of Two Numbers

```java
import java.util.*;
class Main{
public static void main(String[] args){
Scanner sc = new Scanner(System.in);
int a = sc.nextInt(), b = sc.nextInt();
while(b != 0){
int temp = b;
b = a % b;
a = temp;
}
System.out.println(a);
}
}
```

## 11. LCM of Two Numbers

```java
import java.util.*;
class Main{
public static void main(String[] args){
Scanner sc = new Scanner(System.in);
int a = sc.nextInt(), b = sc.nextInt();
int x = a, y = b;
while(y != 0){
int temp = y;
y = x % y;
x = temp;
}
int gcd = x;
int lcm = (a * b) / gcd;
System.out.println(lcm);
}
}
```

## 12. Check Leap Year

```java
import java.util.*;
class Main{
public static void main(String[] args){
Scanner sc = new Scanner(System.in);
int year = sc.nextInt();
if((year % 4 == 0 && year % 100 != 0) || (year % 400 == 0))
System.out.println("Leap Year");
else
System.out.println("Not Leap Year");
}
}
```

## 13. Count Vowels and Consonants

```java
import java.util.*;
class Main{
public static void main(String[] args){

Scanner sc = new Scanner(System.in);
String str = sc.nextLine().toLowerCase();
int vowels = 0, consonants = 0;
for(char ch : str.toCharArray()){
if(Character.isLetter(ch)){
if("aeiou".indexOf(ch) != -1)
vowels++;
else
consonants++;
}
}
System.out.println("Vowels: " + vowels);
System.out.println("Consonants: " + consonants);
}
}
```

## 14. Reverse a String

```java
import java.util.*;
class Main{
public static void main(String[] args){
Scanner sc = new Scanner(System.in);
String str = sc.nextLine();
String rev = "";
for(int i = str.length() - 1; i >= 0; i--)
rev += str.charAt(i);
System.out.println(rev);
}
}
```

## 15. Check Anagram

```java
import java.util.*;
class Main{
public static void main(String[] args){
Scanner sc = new Scanner(System.in);
String s1 = sc.nextLine();
String s2 = sc.nextLine();
char[] a = s1.toCharArray();
char[] b = s2.toCharArray();
Arrays.sort(a);
Arrays.sort(b);
System.out.println(Arrays.equals(a,b) ? "Anagram" : "Not Anagram");
}
}
```

## 16. Remove Duplicates from String

```java
import java.util.*;
class Main{
public static void main(String[] args){
Scanner sc = new Scanner(System.in);

String str = sc.nextLine();
String result = "";
for(char ch : str.toCharArray()){
if(result.indexOf(ch) == -1)
result += ch;
}
System.out.println(result);
}
}
```

## 17. Find Second Largest in Array

```java
import java.util.*;
class Main{
public static void main(String[] args){
Scanner sc = new Scanner(System.in);
int n = sc.nextInt();
int[] arr = new int[n];
for(int i = 0; i < n; i++)
arr[i] = sc.nextInt();
int first = Integer.MIN_VALUE, second = Integer.MIN_VALUE;
for(int num : arr){
if(num > first){
second = first;
first = num;
} else if(num > second && num != first){
second = num;
}
}
System.out.println(second);
}
}
```

## 18. Linear Search

```java
import java.util.*;
class Main{
public static void main(String[] args){
Scanner sc = new Scanner(System.in);
int n = sc.nextInt();
int[] arr = new int[n];
for(int i = 0; i < n; i++)
arr[i] = sc.nextInt();
int key = sc.nextInt();
boolean found = false;
for(int num : arr){
if(num == key){
found = true;
break;
}
}
System.out.println(found ? "Found" : "Not Found");
}
}
```

## 19. Binary Search (Sorted Array)

```java
import java.util.*;
class Main{
public static void main(String[] args){
Scanner sc = new Scanner(System.in);
int n = sc.nextInt();
int[] arr = new int[n];
for(int i = 0; i < n; i++)
arr[i] = sc.nextInt();
int key = sc.nextInt();
int low = 0, high = n - 1;
boolean found = false;
while(low <= high){
int mid = (low + high) / 2;
if(arr[mid] == key){
found = true;
break;
}
else if(arr[mid] < key)
low = mid + 1;
else
high = mid - 1;
}
System.out.println(found ? "Found" : "Not Found");
}
}
```

## 20. Bubble Sort

```java
import java.util.*;
class Main{
public static void main(String[] args){
Scanner sc = new Scanner(System.in);
int n = sc.nextInt();
int[] arr = new int[n];
for(int i = 0; i < n; i++)
arr[i] = sc.nextInt();
for(int i = 0; i < n-1; i++){
for(int j = 0; j < n-i-1; j++){
if(arr[j] > arr[j+1]){
int temp = arr[j];
arr[j] = arr[j+1];
arr[j+1] = temp;
}
}
}
for(int num : arr)
System.out.print(num + " ");
}
}
```

## 21. Selection Sort

```java
import java.util.*;
class Main{
public static void main(String[] args){
Scanner sc = new Scanner(System.in);
int n = sc.nextInt();
int[] arr = new int[n];
for(int i=0;i<n;i++) arr[i]=sc.nextInt();
for(int i=0;i<n-1;i++){
int minIndex=i;
for(int j=i+1;j<n;j++){
if(arr[j]<arr[minIndex])
minIndex=j;
}
int temp=arr[i];
arr[i]=arr[minIndex];
arr[minIndex]=temp;
}
for(int num:arr)
System.out.print(num+" ");
}
}
```

## 22. Insertion Sort

```java
import java.util.*;
class Main{
public static void main(String[] args){
Scanner sc=new Scanner(System.in);
int n=sc.nextInt();
int[] arr=new int[n];
for(int i=0;i<n;i++) arr[i]=sc.nextInt();
for(int i=1;i<n;i++){
int key=arr[i];
int j=i-1;
while(j>=0 && arr[j]>key){
arr[j+1]=arr[j];
j--;
}
arr[j+1]=key;
}
for(int num:arr)
System.out.print(num+" ");
}
}
```

## 23. Matrix Addition

```java
import java.util.*;
class Main{
public static void main(String[] args){
Scanner sc=new Scanner(System.in);

int r=sc.nextInt(), c=sc.nextInt();
int[][] a=new int[r][c];
int[][] b=new int[r][c];
int[][] sum=new int[r][c];
for(int i=0;i<r;i++)
for(int j=0;j<c;j++)
a[i][j]=sc.nextInt();
for(int i=0;i<r;i++)
for(int j=0;j<c;j++)
b[i][j]=sc.nextInt();
for(int i=0;i<r;i++){
for(int j=0;j<c;j++){
sum[i][j]=a[i][j]+b[i][j];
System.out.print(sum[i][j]+" ");
}
System.out.println();
}
}
}
```

## 24. Transpose of Matrix

```java
import java.util.*;
class Main{
public static void main(String[] args){
Scanner sc=new Scanner(System.in);
int r=sc.nextInt(), c=sc.nextInt();
int[][] a=new int[r][c];
for(int i=0;i<r;i++)
for(int j=0;j<c;j++)
a[i][j]=sc.nextInt();
for(int j=0;j<c;j++){
for(int i=0;i<r;i++){
System.out.print(a[i][j]+" ");
}
System.out.println();
}
}
}
```

## 25. Count Frequency of Element in Array

```java
import java.util.*;
class Main{
public static void main(String[] args){
Scanner sc=new Scanner(System.in);
int n=sc.nextInt();
int[] arr=new int[n];
for(int i=0;i<n;i++) arr[i]=sc.nextInt();
int key=sc.nextInt();

int count=0;
for(int num:arr){
if(num==key) count++;
}
System.out.println(count);
}
}
```

## 26. Check if Array is Sorted

```java
import java.util.*;
class Main{
public static void main(String[] args){
Scanner sc=new Scanner(System.in);
int n=sc.nextInt();
int[] arr=new int[n];
for(int i=0;i<n;i++) arr[i]=sc.nextInt();
boolean sorted=true;
for(int i=0;i<n-1;i++){
if(arr[i]>arr[i+1]){
sorted=false;
break;
}
}
System.out.println(sorted ? "Sorted" : "Not Sorted");
}
}
```

## 27. Merge Two Arrays

```java
import java.util.*;
class Main{
public static void main(String[] args){
Scanner sc=new Scanner(System.in);
int n1=sc.nextInt();
int[] a=new int[n1];
for(int i=0;i<n1;i++) a[i]=sc.nextInt();
int n2=sc.nextInt();
int[] b=new int[n2];
for(int i=0;i<n2;i++) b[i]=sc.nextInt();
int[] merged=new int[n1+n2];
for(int i=0;i<n1;i++)
merged[i]=a[i];
for(int i=0;i<n2;i++)
merged[n1+i]=b[i];
for(int num:merged)
System.out.print(num+" ");
}

}
```

## 28. Find Missing Number (1 to N)

```java
import java.util.*;
class Main{
public static void main(String[] args){
Scanner sc=new Scanner(System.in);
int n=sc.nextInt();
int[] arr=new int[n-1];
for(int i=0;i<n-1;i++) arr[i]=sc.nextInt();
int total=n*(n+1)/2;
int sum=0;
for(int num:arr) sum+=num;
System.out.println(total-sum);
}
}
```

## 29. Count Words in a String

```java
import java.util.*;
class Main{
public static void main(String[] args){
Scanner sc=new Scanner(System.in);
String str=sc.nextLine().trim();
if(str.isEmpty()){
System.out.println(0);
} else {
String[] words=str.split("\\s+");
System.out.println(words.length);
}
}
}
```

## 30. Remove All Spaces from String

```java
import java.util.*;
class Main{
public static void main(String[] args){
Scanner sc=new Scanner(System.in);
String str=sc.nextLine();
str=str.replaceAll(" ","");
System.out.println(str);
}
}
```

## 31. Find Duplicate Elements in Array

```java
import java.util.*;
class Main{
public static void main(String[] args){
Scanner sc = new Scanner(System.in);
int n = sc.nextInt();
int[] arr = new int[n];
for(int i=0;i<n;i++) arr[i]=sc.nextInt();
for(int i=0;i<n;i++){
for(int j=i+1;j<n;j++){
if(arr[i]==arr[j]){
System.out.print(arr[i]+" ");
break;
}
}
}
}
}
```

## 32. Move All Zeros to End

```java
import java.util.*;
class Main{
public static void main(String[] args){
Scanner sc=new Scanner(System.in);
int n=sc.nextInt();
int[] arr=new int[n];
for(int i=0;i<n;i++) arr[i]=sc.nextInt();
int index=0;
for(int i=0;i<n;i++){
if(arr[i]!=0){
arr[index++]=arr[i];
}
}
while(index<n){
arr[index++]=0;
}
for(int num:arr)
System.out.print(num+" ");
}
}
```

## 33. Rotate Array Right by 1 Position

```java
import java.util.*;
class Main{
public static void main(String[] args){
Scanner sc=new Scanner(System.in);
int n=sc.nextInt();
int[] arr=new int[n];
for(int i=0;i<n;i++) arr[i]=sc.nextInt();
int last=arr[n-1];

for(int i=n-1;i>0;i--){
arr[i]=arr[i-1];
}
arr[0]=last;
for(int num:arr)
System.out.print(num+" ");
}
}
```

## 34. Check Palindrome String

```java
import java.util.*;
class Main{
public static void main(String[] args){
Scanner sc=new Scanner(System.in);
String str=sc.nextLine();
String rev="";
for(int i=str.length()-1;i>=0;i--)
rev+=str.charAt(i);
System.out.println(str.equals(rev) ? "Palindrome" : "Not
Palindrome");
}
}
```

## 35. Count Number of Digits

```java
import java.util.*;
class Main{
public static void main(String[] args){
Scanner sc=new Scanner(System.in);
int n=sc.nextInt();
int count=0;
while(n!=0){
n/=10;
count++;
}
System.out.println(count);
}
}
```

## 36. Sum of Elements in Array

```java
import java.util.*;
class Main{
public static void main(String[] args){
Scanner sc=new Scanner(System.in);
int n=sc.nextInt();
int[] arr=new int[n];
int sum=0;
for(int i=0;i<n;i++){

arr[i]=sc.nextInt();
sum+=arr[i];
}
System.out.println(sum);
}
}
```

## 37. Find Minimum Element in Array

```java
import java.util.*;
class Main{
public static void main(String[] args){
Scanner sc=new Scanner(System.in);
int n=sc.nextInt();
int[] arr=new int[n];
for(int i=0;i<n;i++) arr[i]=sc.nextInt();
int min=arr[0];
for(int i=1;i<n;i++){
if(arr[i]<min)
min=arr[i];
}
System.out.println(min);
}
}
```

## 38. Pattern Printing (Right Triangle)

Input: 4
Output:
*
**
***
****

```java
import java.util.*;
class Main{
public static void main(String[] args){
Scanner sc=new Scanner(System.in);
int n=sc.nextInt();
for(int i=1;i<=n;i++){
for(int j=1;j<=i;j++){
System.out.print("*");
}
System.out.println();
}
}
}
```

## 39. Power of a Number

```java
import java.util.*;
class Main{

public static void main(String[] args){
Scanner sc=new Scanner(System.in);
int base=sc.nextInt();
int exp=sc.nextInt();
int result=1;
for(int i=1;i<=exp;i++)
result*=base;
System.out.println(result);
}
}
```

## 40. Decimal to Binary

```java
import java.util.*;
class Main{
public static void main(String[] args){
Scanner sc=new Scanner(System.in);
int n=sc.nextInt();
String binary="";
while(n>0){
binary=(n%2)+binary;
n/=2;
}
System.out.println(binary);
}
}
```

## 41. Binary to Decimal

```java
import java.util.*;
class Main{
public static void main(String[] args){
Scanner sc = new Scanner(System.in);
String binary = sc.next();
int decimal = 0;
int power = 0;
for(int i = binary.length()-1; i >= 0; i--){
if(binary.charAt(i) == '1'){
decimal += Math.pow(2, power);
}
power++;
}
System.out.println(decimal);
}
}
```

## 42. Check Perfect Number

```java
import java.util.*;

class Main{
public static void main(String[] args){
Scanner sc = new Scanner(System.in);
int n = sc.nextInt();
int sum = 0;
for(int i = 1; i <= n/2; i++){
if(n % i == 0)
sum += i;
}
System.out.println(sum == n ? "Perfect" : "Not Perfect");
}
}
```

## 43. Strong Number

```java
import java.util.*;
class Main{
public static int factorial(int n){
int fact = 1;
for(int i = 1; i <= n; i++)
fact *= i;
return fact;
}
public static void main(String[] args){
Scanner sc = new Scanner(System.in);
int n = sc.nextInt();
int temp = n, sum = 0;
while(n != 0){
int digit = n % 10;
sum += factorial(digit);
n /= 10;
}
System.out.println(temp == sum ? "Strong" : "Not Strong");
}
}
```

## 44. Count Even and Odd Numbers in Array

```java
import java.util.*;
class Main{
public static void main(String[] args){
Scanner sc = new Scanner(System.in);
int n = sc.nextInt();
int[] arr = new int[n];
int even = 0, odd = 0;
for(int i=0;i<n;i++){
arr[i]=sc.nextInt();
if(arr[i]%2==0)
even++;

else
odd++;
}
System.out.println("Even: " + even);
System.out.println("Odd: " + odd);
}
}
```

## 45. Find Intersection of Two Arrays

```java
import java.util.*;
class Main{
public static void main(String[] args){
Scanner sc=new Scanner(System.in);
int n1=sc.nextInt();
int[] a=new int[n1];
for(int i=0;i<n1;i++) a[i]=sc.nextInt();
int n2=sc.nextInt();
int[] b=new int[n2];
for(int i=0;i<n2;i++) b[i]=sc.nextInt();
for(int i=0;i<n1;i++){
for(int j=0;j<n2;j++){
if(a[i]==b[j]){
System.out.print(a[i]+" ");
break;
}
}
}
}
}
```

## 46. Check Substring

```java
import java.util.*;
class Main{
public static void main(String[] args){
Scanner sc=new Scanner(System.in);
String str=sc.nextLine();
String sub=sc.nextLine();
if(str.contains(sub))
System.out.println("Substring Present");
else
System.out.println("Substring Not Present");
}
}
```

## 47. Remove Specific Character from String

```java
import java.util.*;
class Main{
public static void main(String[] args){
Scanner sc=new Scanner(System.in);
String str=sc.nextLine();
char ch=sc.next().charAt(0);
str=str.replace(Character.toString(ch),"");
System.out.println(str);
}
}
```

## 48. Sum of Prime Numbers up to N

```java
import java.util.*;
class Main{
public static boolean isPrime(int n){
if(n<=1) return false;
for(int i=2;i<=Math.sqrt(n);i++){
if(n%i==0) return false;
}
return true;
}
public static void main(String[] args){
Scanner sc=new Scanner(System.in);
int n=sc.nextInt();
int sum=0;
for(int i=2;i<=n;i++){
if(isPrime(i))
sum+=i;
}
System.out.println(sum);
}
}
```

## 49. Reverse Words in a Sentence

```java
import java.util.*;
class Main{
public static void main(String[] args){
Scanner sc=new Scanner(System.in);
String str=sc.nextLine();
String[] words=str.split(" ");
for(int i=words.length-1;i>=0;i--){
System.out.print(words[i]+" ");
}
}
}
```

## 50. Two Sum Problem

```java
import java.util.*;
class Main{
public static void main(String[] args){
Scanner sc=new Scanner(System.in);
int n=sc.nextInt();
int[] arr=new int[n];
for(int i=0;i<n;i++) arr[i]=sc.nextInt();
int target=sc.nextInt();
for(int i=0;i<n;i++){
for(int j=i+1;j<n;j++){
if(arr[i]+arr[j]==target){
System.out.println(i+" "+j);
return;
}
}
}
System.out.println("No Pair Found");
}
}
```
/*
Problem: Matrix Reverse Diagonal Consistency

Description:
You are given a matrix of size M × N.

Each group of elements that lie on the same diagonal from top-right to bottom-left
is considered a diagonal group.

These diagonals are formed by grouping elements having the same value of:
i − j = constant

Task:
- Group elements based on diagonals (i − j)
- Check if all elements in every diagonal are equal
- If YES → return sum of first row
- If NO  → return product of first row

Input Format:
First line: M N
Next M lines: N integers each

Output Format:
Print a single integer

Example:
Input:
3 3
6 4 2
7 2 1
2 5 3

Output:
48

Explanation:
Diagonal [6,2,5] not equal → condition fails
First row = [6,4,2]
Product = 48
*/

import java.util.*;
class Main{
public static void main(String[] args){
Scanner sc=new Scanner(System.in);
int m=sc.nextInt();
int n=sc.nextInt();

int[][] mat=new int[m][n];
for(int i=0;i<m;i++){
for(int j=0;j<n;j++){
mat[i][j]=sc.nextInt();
}
}

boolean flag=true;
HashMap<Integer,Integer> map=new HashMap<>();

for(int i=0;i<m;i++){
for(int j=0;j<n;j++){
int key=i-j;
if(!map.containsKey(key)){
map.put(key,mat[i][j]);
}else{
if(map.get(key)!=mat[i][j]){
flag=false;
}
}
}
}

int result=1;

if(flag){
result=0;
for(int j=0;j<n;j++){
result+=mat[0][j];
}
}else{
for(int j=0;j<n;j++){
result*=mat[0][j];
}
}

System.out.println(result);
}
}
/*
Problem: Stock Availability Score

Description:
You are given stock IDs with their quantities and a list of queries.

You need to calculate a score based on availability.

Rules:
- qty = 2 → +3
- qty = 1 → +2
- qty = 0 → -2
- not present → -6

Input Format:
First line: N
Next N lines: stockID quantity
Next line: Q
Next line: Q stock IDs

Output Format:
Print final score

Example:
Input:
3
101 2
102 1
103 0
4
101 102 999 103

Output:
-3

Explanation:
101 → +3
102 → +2
999 → -6
103 → -2
Total = -3
*/

import java.util.*;
class Main{
public static void main(String[] args){
Scanner sc=new Scanner(System.in);

int n=sc.nextInt();
HashMap<Integer,Integer> map=new HashMap<>();

for(int i=0;i<n;i++){
int id=sc.nextInt();
int qty=sc.nextInt();
map.put(id,qty);
}

int q=sc.nextInt();
int score=0;

for(int i=0;i<q;i++){
int id=sc.nextInt();

if(map.containsKey(id)){
int qty=map.get(id);
if(qty==2) score+=3;
else if(qty==1) score+=2;
else if(qty==0) score-=2;
}else{
score-=6;
}
}

System.out.println(score);
}
}
