task-1.sh
#!/bin/bash
for com in ls pwd date
do
	echo "Command : "$com
	echo "Output"
	$com
done

task-2.sh
#!/bin/bash
for num in {0..100..5}
do
	echo $num
done

task-3.sh
#!/bin/bash
read -p "Enter your cgpa : " cg
read -p "Is there any drop in any course?yes/no : " drop
read -p "did you complete more than 41 credit?yes/no : " credit
read -p "Is there any grade lower than B+?yes/no :" grade
if [ $(echo "cg>=3.75" | bc -l)==1 ] && [ $drop == "no" ] && [ $credit == "yes" ] && [ $grade == "no" ]
then 
	echo "Elligible"
else
	echo "Not Elligible"
fi

task-4.sh
#!/bin/bash
read -p "Enter an Integer number : " n
if [ `expr $n % 2` == 0 ]
then 
	echo "EVEN"
else	
	echo "ODD"
fi

task-5.sh
#!/bin/bash
read -p "Enter a character : " char
if [ $char == 'A' ] || [ $char == 'E' ] || [ $char == 'I' ] || [ $char == 'O' ] || [ $char == 'U' ] || [ $char == 'a' ] || [ $char == 'e' ] || [ $char == 'i' ] || [ $char == 'o' ] || [ $char == 'u' ]
then
	echo "$char is a Vowel"
else
	echo "$char is a Consonant"
fi

task-6.sh
#!/bin/bash
read -p "Enter your age :" age
if [ $age -ge 18 ]
then
	echo "legal voter"
else
	echo "not a legal voter"
fi

task-7.sh
#!/bin/bash

read -p "Enter username : " user
read -sp "Enter your password : " pass
echo ""
echo -e "\nGive your login credentials"
read -p "username : " u
read -sp "password : " p

echo $pass
if [ $user == $u ] && [ $pass == $p ]
then
	echo "password is correct"
else
	echo "usename or password is incorrect"
fi	

task-8.sh
#!/bin/bash
read -p "1st number : " n1
read -p "2st number : " n2
echo "press 1 Add" 
echo "press 2 Sub" 
echo "press 3 Mul" 
echo "press 4 Div" 
echo "press 5 Mod"
read op
case $op in 
	1)
		echo "Addition"
		sum=$(bc<<<"$n1+$n2")
		echo $sum
	;;
	2) 
		echo "Subtraction"
		sub=$(bc<<<"$n1-$n2")
		echo $sub
	;;
	3) 
		echo "Multiplication"
		mul=$(bc<<<"$n1*$n2")
		echo $mul
	;;
	4) 
		echo "Division"
		div=$(bc<<<"$n1/$n2")
		echo $div
	;;
	5) 
		echo "Mod"
		mod=$(bc<<<"$n1%$n2")
		echo $mod
	;;
	*) 
		echo "operation invalid"
esac

task-9.sh
#!/bin/bash
read -p "Enter your name : " n
echo "press an interger value" 
read op
case $op in 
	1)
		if [ $n == 'rifat' ]
		then
			echo "$n your are a gamer"
		else
			echo "$n your are not a gamer"
		fi
	;;
	2) 
		echo "$n you are a otaku"
	;;	
	*)
		echo "$n you are a Normal human"
	;;
esac
