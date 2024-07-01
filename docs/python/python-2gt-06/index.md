---
tags:
  - python
  - seconde
---
# Boucles finies ```#!python for```

!!! coeur "parcourir une progression d'entiers"

	L'instruction ```#!python range()``` renvoie une progression d'entiers :
	
	- ```#!python range(fin)``` renvoie **la progression croissante de ```fin``` entiers consécutifs** partant de ```0``` jusqu'à ```fin-1```.
	- ```#!python range(debut, fin)``` renvoie **la progression croissante de ```fin-debut``` entiers consécutifs** partant de ```debut``` jusqu'à ```fin-1```.
	- ```#!python range(debut, fin, pas)``` renvoie la progression d'entiers : ```debut```, ```debut+pas```, ```debut+2*pas``` , ```debut+3*pas``` etc. **strictement inférieurs à** ```fin```.

!!! example "```#!python range()```"
	Les plus courantes :
	
	- ```#!python range(5)``` renvoie **la progression de ```5``` entiers consécutifs** :  ```0```, ```1```, ```2```, ```3```, ```4```, (et pas  ```5``` )
	- ```#!python range(3,8)``` renvoie **la progression de ```8-3=5``` entiers consécutifs** :  ```3```, ```4```, ```5```, ```6```, ```7```, ( et pas  ```8``` )
	
	Plus rares :
	
	- ```#!python range(10,5,-1)``` renvoie la progression décroissante des entiers : ```10```, ```9```, ```8```, ```7```, ```6``` ( et pas  ```5``` )
	- ```#!python range(-3,6,2)``` renvoie la progression croissante des entiers : ```-3```, ```-1```, ```1```, ```3```, ```5``` ( et pas  ```7``` )


!!! coeur "parcourir une progression d'entiers" 

	L'instruction ```#!python for ... in ...``` parcourt la progression et permet d'exécuter de manière répétée un bloc indenté :
	 
	```python title="syntaxe d'une boucle finie" linenums='1'
	for entier in  range(<paramètres de la progression>) :  	# (1)!
		action1() 
		action2(entier)  	# (2)!
	action3() 		# (3)! 
	```

	1. :warning: Le ```#!python in``` et les deux points sont obligatoires

	2. :warning: ```action1()``` et ```action2()``` sont exécutées pour chaque nouvelle valeur de ```entier```

	3. :warning: ```action3()``` sera faite après la fin des répétitions.
	
	
!!! example "Exemples"
	
	Les lignes indentés suivants l'instruction ```#!python for``` sont les lignes de la boucles.
	
	La variable signalée après l'instruction ```for``` est un **indice**, on utilise parfois la lettre ```i```.
	
	
	Essayer chacun des exemples
	
	=== "```#!python range(fin)```"
		
		La boucle de la ligne 1 réalise 3 boucles, et celle de la ligne 7 en fait 5.
		
		On utilise ```end=""``` pour supprimer le retour de ligne par défaut de l'instruction ```#!python print()```.
		
        {{ IDEv('example01a', ID='example01a', MAX_SIZE=18, TERM_H=12) }} 
	
	=== "```#!python range(debut,fin)```"
		
		L'indice ```i``` de la boucle de la ligne 1 prend les valeurs $1$, $2$, $3$ et enfin $4$.
		
		L'indice ```j``` de la boucle de la ligne 6 prend les valeurs $3$, $4$, $5$ et enfin $6$. 
		
        {{ IDEv('example01b', ID='example01b', MAX_SIZE=18, TERM_H=12) }} 
	
	=== "```#!python range(debut,fin,pas)```"
		
		En précisant le paramètre ```pas```, on peut produire des progressions d'entiers non consécutifs, ou bien décroissant !
		
        {{ IDEv('example01c', ID='example01c', MAX_SIZE=18, TERM_H=12) }} 
		


```#!python True```