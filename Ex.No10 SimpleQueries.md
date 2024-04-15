# Ex.No: 10  Logic Programming –  Simple queries from facts and rules
### DATE: 15/04/2024                                                                          
### REGISTER NUMBER : 212221040187
### AIM: 
To write a prolog program to find the answer of query. 
###  Algorithm:
 Step 1: Start the program <br> 
 Step 2: Convert the sentence into First order Logic  <br> 
 Step 3:  Convert the sentence into Horn clause form  <br> 
 Step 4: Add rules and predicates in a program   <br> 
 Step 5:  Pass the query to program. <br> 
 Step 6: Prolog interpreter shows the output and return answer. <br> 
 Step 8:  Stop the program.

### Task 1:
Construct the FOL representation for the following sentences <br> 
1.	John likes all kinds of food.  <br> 
2.	Apples are food.  <br> 
3.	Chicken is a food.  <br> 
4.	Sue eats everything Bill eats. <br> 
5.	 Bill eats peanuts  <br> 
   Convert into clause form and Prove that John like Apple by using Prolog. <br> 
### Program:
```
likes(mani,X):-easygame(X).
indoorgame(tabletennis).
easygame(X):-indoorgame(X).
hard(boxing).
likes(john,X):-food(X).
food(apple).
food(vegetable).
eats(bill,peanuts).
eats(sue,X):-eats(bill,X).
alive(bill).
```


### Output:
![image](https://github.com/yuvaraj-csk/AI_Lab_2023-24/assets/134052574/8dff69c6-5488-49b0-bfe5-cd792e8123db)


### Task 2:
Consider the following facts and represent them in predicate form: <br>              
1.	Steve likes easy courses. <br> 
2.	Science courses are hard. <br> 
3. All the courses in Have fun department are easy <br> 
4. BK301 is Have fun department course.<br> 
Convert the facts in predicate form to clauses and then prove by resolution: “Steve likes BK301 course”<br> 

### Program:
```
likes(steve,X):-
     easycourse(X).
hard(sciencecourse).
easycourse(X):-
    course(X,dept(havefun)).
course(bk301,dept(havefun)).
```


### Output:
![image](https://github.com/yuvaraj-csk/AI_Lab_2023-24/assets/134052574/c19beb77-a3d6-4874-b3a6-e95df866b039)


### Task 3:
Consider the statement <br> 
“This is a crime for an American to sell weapons to hostile nations. The Nano , enemy of America has some missiles and its missiles were sold it by Colonal West who is an American” <br> 
Convert to Clause form and prove west is criminal by using Prolog.<br> 
### Program:
```
criminal(X):-
	american(X),
	weapon(Y),
	hostile(Z),
	sells(X,Y,Z).

weapon(Y):-
    missile(Y).

hostile(Z):-
    enemy(Z,X).

sells(west,Y,nano):-
    missile(Y),
	owns(nano,Y).

missile(m).
owns(nano,m).
enemy(nano,america).
american(west).
```


### Output:
![image](https://github.com/yuvaraj-csk/AI_Lab_2023-24/assets/134052574/d5e31439-9ac2-4a37-8d59-1feb311a6979)



### Result:
Thus the prolog programs were executed successfully and the answer of query was found.
