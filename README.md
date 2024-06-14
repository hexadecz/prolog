This is a small project of a family tree and gender check 



-[Rules]
Brother(x,y) x has the same parent as y and both are males.
Grandparent(x,y) y is the grandfather of x which means that y is the father of z and z is the father of x.
-[Facts]
Parent(x,y)  x is the parent of y.
Male(x) x is male
Female(x) x is female
--------------------------------------

Program:
parent(ziad,ahmed).
parent(mouhamed,yasser).
parent(ehab,ahmed).
parent(mouhamed,amr).
parent(ahmed,mouhamed).
male(ziad).
male(mouhamed).
male(ahmed).
male(omar).
male(ehab).
female(nour).
female(salma).
female(zeina).
female(farida).
female(noha).
grandparent(X,Z):-
    parent(X,Y),
    parent(Y,Z).
brother(X,Y):-
    male(X),
    male(Y),
    parent(X,Z),
    parent(Y,Z).

