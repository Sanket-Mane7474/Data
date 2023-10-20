Assignment 1.1
one
	apple
	banana
	cat
	dog
	elephant
two
	fish
	gun
	horse
	ice cream
three
	jelly
	kit kat
	lolipop
	marshmallow
four
	new
	oppo
	vivo
	china
/home -> mkdir EVERYONE
 



 



 

Create a file with every user (whoami >> username.txt)

 




oppo -> primary group change -> one
vivo -> primary group change -> two
 

jelly,kitkat, lolipop, marshmallow -> add these users to sudo group

 

fish,gun -> add these users to one group as well (secondary group)

   
 










Assignment 1:
1. In your home directory, create sets of empty practice files 
•	Create 6 files with names of the form songsX.mp3.
•	Create 6 files with names of the form snapX.jpg.
•	Create 6 files with names of the form filmX.avi.
In each set, replace X with the numbers 1 through 6.
 
 
2. From your home directory,
•	Move songs file into your Music subdirectory.
•	Move snap file into your Pictures subdirectory.
•	Move your movie files into Videos subdirectory  
 
 
3. Create 3 subdirectories for organizing your files named friends,family,work
 

4. Copy files (all types ) containing numbers 1 and 2 to the friends folder.
    Copy files (all types) containing numbers 3 and 4 to the family folder.
    Copy files (all types) containing numbers 5 and 6 to the work folder.
 


 


 




Assignment-2

6. Delete all files in family subdirectory.

7. Delete friends subdirectory

 



8. Create user tom , bob , sam , prince

9. Create Group dac , dbda ,ditiss

10. add user
	
	Tom in dac
	Bob in dbda
	Sam in ditiss
 


11. login as prince and create iacsd directory  in /tmp and create 4 files in iacsd with name project-1 project-2 upto 4

 


12. assign permissions to project files as below

	Project-1 – tom should be owner of this

	Project-2 – dac should be owner of this
Project-3 --- others should not have any permission but tom should have rw    access
	Project-4 – dm nbda group should have rwx permissions.

 
 
 







Assignment 4
1) Write a shell script tp print 
•	your are logged in as which user
•	in which directory you are
•	and in which terminal you are working
•	total number of files and directories in current directory

 

2).Write a shell script to create a menu driven program for adding, deletion or finding a record in a database. Database should have the field like rollno, name, semester and marks of three subjects. Last option of the menu should be to exit the menu.

#!/bin/bash
# creating a menu with the following options
echo "SELECT YOUR FAVORITE FRUIT";
echo "1. Apple"
echo "2. Grapes"
echo "3. Mango"
echo "4. Exit from menu "
echo -n "Enter your menu choice [1-4]: "

# Running a forever loop using while statement
# This loop will run until select the exit option.
# User will be asked to select option again and again
while :
do

# reading choice
read choice

# case statement is used to compare one value with the multiple cases.
case $choice in
  # Pattern 1
  1)  echo "You have selected the option 1"
      echo "Selected Fruit is Apple. ";;
  # Pattern 2
  2)  echo "You have selected the option 2"
      echo "Selected Fruit is Grapes. ";;
  # Pattern 3
  3)  echo "You have selected the option 3"
      echo "Selected Fruit is Mango. ";;    
  # Pattern 4
  4)  echo "Quitting ..."

      exit;;
  # Default Pattern
  *) echo "invalid option";;
  
esac
  echo -n "Enter your menu choice [1-4]: "
done
 








3) Write a Linux shell script to accept 10 number and tell how many are +tive, -tive and zero.
  


4) Write a shell script to accept five number and display max and min value. 

 
 

 



5) Write a script to find out String is palindrome or not. 
 
 


 6) Write a shell script to print given number’s sum of all digits (eg. If number is 123, then it’s sum of all digits will be 1+2+3=6

 
 

7) Create a script to 
	Create user , Delete user , Create group , delete Group using case
 





Loop Assignment

1. Shell Script to display the first 10 natural numbers.
Expected Output :
1 2 3 4 5 6 7 8 9 10

solution:
for((i=1;i<=10;i++))
do
echo $i
done

 


2. Shell Script to compute the sum of the first 10 natural numbers.
Expected Output :
The first 10 natural number is :
1 2 3 4 5 6 7 8 9 10
The Sum is : 55

sol:
sum=0
for((i=1;i<=10;i++))
do
 sum=$((sum+i))
done
echo "The sum is: "$sum

 



3. Shell Script to display n terms of natural numbers and their sum.
Test Data : 7
Expected Output :
The first 7 natural number is :
1 2 3 4 5 6 7
The Sum of Natural Number upto 7 terms : 28

Sol:
read -p "Enter value of n: " n
echo "First $n natural number is :"
sum=0
for((i=1;i<=n;i++))
do
echo -n " "$i
sum=$((sum+i))
done
echo " "
echo "The Sum of Natural Number upto $n terms :" $sum

 



4. Shell Script to read 10 numbers from the keyboard and find their sum and average.
Test Data :
Input the 10 numbers :
Number-1 :2
...
Number-10 :2
Expected Output :
The sum of 10 no is : 55
The Average is : 5.500000

Sol:
echo "Input 10 Numbers: "
sum=0
for((i=1;i<=10;i++))
do 
read -p "Number- $i :" n$i
sum=$((sum+i))
done
echo "The sum of 10 no is :" $sum
n=10
echo "The avg of 10 no is:" `expr $sum / $n`

 




5. Shell Script to display the cube of the number up to an integer.
Test Data :
Input number of terms : 5
Expected Output :
Number is : 1 and cube of the 1 is :1
Number is : 2 and cube of the 2 is :8
Number is : 3 and cube of the 3 is :27
Number is : 4 and cube of the 4 is :64
Number is : 5 and cube of the 5 is :125

Sol:

read -p "Enput number of terms: " n 
for((i=1;i<=n;i++))
do
cube=$((i*i*i))
echo "Number is : $i and cube of the $i is: " $cube
done

 






6. Shell Script to display the multiplication table for a given integer.
Test Data :
Input the number (Table to be calculated) : 15
Expected Output :
15 X 1 = 15
...
...
15 X 10 = 150

Sol:
read -p "Input the number (Table to be calculated) :" n 
for((i=1;i<=10;i++))
do
echo "$n x $i = " $((n*i))
done

 





7. Shell Script to display the multiplier table vertically from 1 to n.
Test Data :
Input upto the table number starting from 1 : 8
Expected Output :
Multiplication table from 1 to 8
1x1 = 1, 2x1 = 2, 3x1 = 3, 4x1 = 4, 5x1 = 5, 6x1 = 6, 7x1 = 7, 8x1 = 8
...
1x10 = 10, 2x10 = 20, 3x10 = 30, 4x10 = 40, 5x10 = 50, 6x10 = 60, 7x10 = 70, 8x10 = 80

Sol:
read -p "Input upto the table number starting from " n1
read -p "to " n2
echo "Multiplication table from $n1 to $n2"
for((i=n1;i<=n2;i++))
do
for((j=1;j<=10;j++))
do
echo -n "$i x $j "= $((i*j))
echo -n ","
done
echo " "
done

 




8. Shell Script to display the n terms of odd natural numbers and their sum.
Test Data
Input number of terms : 10
Expected Output :
The odd numbers are :1 3 5 7 9 11 13 15 17 19
The Sum of odd Natural Number upto 10 terms : 100

Sol:
read -p "Input number of terms : " n
echo -n "The odd numbers are: "
sum=0
for((i=1;i<=n;i++))
do
if [ $(expr $i % 2) -ne 0 ]
then
echo -n " "$i
sum=$((sum+i))
fi
done
echo " "
echo "The Sum of odd Natural Number upto $n terms : " $sum

 


9. Shell Script to display a pattern like a right angle triangle using an asterisk.
The pattern like :

*
**
***
****

Sol:
for((i=1;i<=4;i++))
do
for((j=i;j>=1;j--))
do
echo -n "*"
done
echo " "
done

 




10. Shell Script to display a pattern like a right angle triangle with a number.
The pattern like :

1
12
123
1234

Sol:
for((i=1;i<=4;i++))
do
for((j=1;j<=i;j++))
do
echo -n "$j"
done
echo " "
done

 


11. Shell Script to make such a pattern like a right angle triangle with a number which will repeat a number in a row.
The pattern like :

 1
 22
 333
 4444

Sol:
for((i=1;i<=4;i++))
do
for((j=1;j<=i;j++))
do
echo -n "$i"
done
echo " "
done








12. Shell Script to make such a pattern like a right angle triangle with the number increased by 1.
The pattern like :
   1
   2 3
   4 5 6
   7 8 9 10
Sol:
count=0
for((i=1;i<=4;i++))
do
for((j=0;j<i;j++))
do
echo -n "$((count+1))"
count=$((count+1))
echo -n " "
done
echo " "
done
 


















Exercise Solution

1. Write a Shell Script to find maximum between two numbers.
Sol:
echo "Enter 2 numbers: "
read -r n1 n2
if [ $n1 -gt $n2 ]
then
    echo "$n1 is greater than $n2"
else
    echo "$n2 is greater than $n1"
fi
 


2. Write a Shell Script to find maximum between three numbers.

echo "Enter 3 numbers: "
read -r n1 n2 n3
if [ $n1 -gt $n2 && $n1 -gt $n3 ]
then
    echo "$n1 is the gretest number"
elif [ $n2 -gt $n3 ]
then
    echo "$n2 is the greatest number"
else
    echo "$n3 is the greatest number"
fi
 


3. Write a Shell Script to check whether a number is negative, positive or zero.

Sol:
read -p "Enter a number " num 
if [ $num == 0 ]
then
echo "You have entered zero"
elif [ $num -gt 0 ]
then
echo "You have entered positive number"
else
echo "You have entered negative number"
fi
 


4. Write a Shell Script to check whether a number is divisible by 5 and 11 or not.

read -p "Enter a number: " num 
if [ $((num%5)) -eq 0 ]
then 
    if [ $((num%11)) -eq 0 ]
    then
    echo "Number is divisible 5 and 11"
    else
    echo "Number is not divisible by 5 and 11"
    fi
fi

 

OR

read -p "Enter a number: " num 
if [ $((num%5)) -eq  0 ] && [ $((num%11)) -eq 0 ]
then 
echo "Number is divisible 5 and 11"
else
echo "Number is not divisible by 5 and 11"
fi


 


5. Write a Shell Script to check whether a number is even or odd.

read -p "Enter a number: " num 
if [ $((num%2)) -eq  0 ]
then 
echo "$num is even number"
else
echo "$num is odd number"
fi
 

6. Write a Shell Script to check whether a year is leap year or not.

Sol:
read -p "Enter value of Year: " year 
if [ $((year%4)) -eq  0 ]
then 
    if  [ $((year%100)) -ne 0 ] || [ $((year%400)) -eq 0 ]
    then
        echo "$year is a leap year"
    fi
else
    echo "$year is not a leap year"
fi

 








7. Shell Script to print number between 1 to 10 in character format using switch-case.

Sol:
a=1
while [ $a -le 10 ]
do
    case $a in
        1) echo "One" ;;
        2) echo "Two" ;;
        3) echo "Three" ;;
        4) echo "Four" ;;
        5) echo "Five" ;;
        6) echo "Six" ;;
        7) echo "Seven" ;;
        8) echo "Eight" ;;
        9) echo "Nine" ;;
        10) echo "Ten" ;;
        *) echo "Invalid" ;;    
    esac 
    ((a++))
done
 


8. Shell Script to accept id from user to confirm department using switch-case.

read -p "Enter id: " id 
case $id in 
    10) echo "Id is $id and department is Accounting" ;;
    20) echo "Id is $id and department is Sales" ;;
    30) echo "Id is $id and department is Tax" ;;
     *) echo "Invalid Id" ;;
esac

 


9. Shell Script to check password is correct or incorrect using switch-case.

Sol:
read -p "Enter password: " password
len=${#password}
case $len in 
    8) echo "Correct password" ;;
    9) echo "Correct password" ;;
   10) echo "Correct password" ;;
    *) echo "Incorrect password !!" ;;
esac
    
 


10. Shell Script to print day of week using switch-case.

Sol:
for i in {1..7}
do
case $i in 
    1) echo "Monday" ;;
    2) echo "Tuesday" ;;
    3) echo "Wednesday" ;;
    4) echo "Thursday" ;;
    5) echo "Friday" ;;
    6) echo "Saturday" ;;
    7) echo "Sunday" ;;
    *) echo "Invalid choice" ;;
esac
done

 


11. Shell Script to create calculator using switch-case.

Sol:
echo "Enter 2 numbers: "
read n1 n2
echo -e "1.Add 2.Sub 3.Mul 4.Div"
read -p "Enter your choice: " choice
case $choice in 
    1) a=$((n1+n2))
       echo "Addition : "$a ;;
    2) a=$((n1-n2))
       echo "Substraction : "$a ;;
    3) a=$((n1*n2))
       echo "Multiplication : "$a ;;
    4) a=$((n1/n2))
       echo "Division : "$a ;;
    *) echo "Invalid choice" ;;
esac

 










