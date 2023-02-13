# Lab Report 3

**Grep example 1**

``
[cs15lwi23auj@ieng6-203]:skill-demo1-data:467$ grep -rl "pickles"
written_2/travel_guides/berlitz1/WhereToJapan.txt
written_2/travel_guides/berlitz2/Beijing-WhereToGo.txt
written_2/travel_guides/berlitz2/California-WhereToGo.txt
``


Here we are looking for the file that contains the word "pickles" in /written_2/

``
[cs15lwi23auj@ieng6-203]:skill-demo1-data:484$ grep -rl "symmetrical"
written_2/non-fiction/OUP/Kauffman/ch10.txt
written_2/non-fiction/OUP/Rybczynski/ch3.txt
written_2/travel_guides/berlitz1/WhereToEdinburgh.txt
written_2/travel_guides/berlitz1/WhereToFrance.txt
...
``

Here we are using the command to find files that contain "symmetrical". 

The command-line option we are using is -rl. This command is a very useful one because it allows the user to scan all files within a directory and find a specific instance of the string they are asking for. Then, because of the -rl, the system returns all files that contain the string they were looking for. 

For this command, I actually aleady knew it prior to this class so there is no source for me to refrence.

**Grep example 2**

``
[cs15lwi23auj@ieng6-203]:skill-demo1-data:496$ grep -w "Hollywood" written_2/non-fiction/OUP/Castro/chV.txt
The vaquero was the early Hispano cowboy and the antecedent of the Hollywood cowboy. Horses and cattle were brought to New Spain by the Spaniards. When Hernán Cortés landed on the eastern shore of Mexico, he had with him sixteen horses and at least three breeds of cattle. Cattle breeding was a tradition hundreds of years old in Spain, and Cortés brought this tradition to Mexico and eventually to the Southwest. The Spaniards introduced the system of el rancho, with vaqueros being the workers who herded the cattle and conducting cattle drives. Vaca means “cow” and a vaquero is “one who works with cows.” The Spanish mission padres recognized this labor and conscripted mestizos (mixed-race people), Indians, and Mexicans to take care of the cattle. It was these individuals who developed the system, equipment, practices, and traditions that have lasted these past few hundred years. The Anglo cowboy learned everything about cattle from the vaquero.
The Mexican vaquero was a laborer, a peon who was used by the missionaries to ride the horses and take care of the cattle. So it was the culture of the vaquero that became the basis for the romantic cowboy of Hollywood. The ensemble, equipment, and clothing of the vaquero evolved through the years as a combination of Spanish leather and regional indigenous fabrics. He always wore a sombrero with a wide brim, a leather chaqueta (jacket), tight-fitting knee-length sotas (breeches), and botas (leather leggings) for protection. The vaquero also wore iron spurs, like those worn by the Conquistadores, which are still worn to this day. The various styles of saddles, from the Moorish to the Spanish war saddle, eventually changed when the vaqueros began making their own saddles, more suitable for riding hard and for quick mounting and dismounting.
``

In this instance, I used the word Hollywood using the -w command.

``
[cs15lwi23auj@ieng6-203]:skill-demo1-data:497$ grep -w "Horses" written_2/non-fiction/OUP/Castro/chV.txt
The vaquero was the early Hispano cowboy and the antecedent of the Hollywood cowboy. Horses and cattle were brought to New Spain by the Spaniards. When Hernán Cortés landed on the eastern shore of Mexico, he had with him sixteen horses and at least three breeds of cattle. Cattle breeding was a tradition hundreds of years old in Spain, and Cortés brought this tradition to Mexico and eventually to the Southwest. The Spaniards introduced the system of el rancho, with vaqueros being the workers who herded the cattle and conducting cattle drives. Vaca means “cow” and a vaquero is “one who works with cows.” The Spanish mission padres recognized this labor and conscripted mestizos (mixed-race people), Indians, and Mexicans to take care of the cattle. It was these individuals who developed the system, equipment, practices, and traditions that have lasted these past few hundred years. The Anglo cowboy learned everything about cattle from the vaquero.
``

Here I used Horses as the string.

In both instances, I used the -w command. The -w allows the user to find whole words instances of their desired string in .txt files. The -w command does not work in directories. If a match is found, it returns the text in which the string was found in highlighted red. Unfortunately you can not see the highlight, but rest assured it is red in the terminal. This command is case sensitive and if the word is encompassed in another word, like "apple" and "pineapple", it will not refrence the "pineapple" as a valid word. 

I used chatGPT in order to find this command, and the sources it refrenced is [Linux guide]https://linux.die.net/man/1/grep . 


**Grep example 3**

``
[cs15lwi23auj@ieng6-203]:skill-demo1-data:498$ grep -c "Horses" written_2/non-fiction/OUP/Castro/chV.txt
1
[cs15lwi23auj@ieng6-203]:skill-demo1-data:499$ grep -c "Hollywood" written_2/non-fiction/OUP/Castro/chV.txt
2
``

Here are two examples back to back. In this instance, the -c command allows the user to return the number of times the string was found. Horses was found once, whereas Hollywood was found twice. This is useful in the case where you want to see how many times a word as been repeated. However the drawback is that it does not refrence where it was found in lines. 

I used chatGPT in order to find this command, and the sources it refrenced is [Linux guide]https://linux.die.net/man/1/grep . 

**Grep example 4**

``
[cs15lwi23auj@ieng6-203]:skill-demo1-data:500$ grep -i "HOllyWooD" written_2/non-fiction/OUP/Castro/chV.txt
The vaquero was the early Hispano cowboy and the antecedent of the Hollywood cowboy. Horses and cattle were brought to New Spain by the Spaniards. When Hernán Cortés landed on the eastern shore of Mexico, he had with him sixteen horses and at least three breeds of cattle. Cattle breeding was a tradition hundreds of years old in Spain, and Cortés brought this tradition to Mexico and eventually to the Southwest. The Spaniards introduced the system of el rancho, with vaqueros being the workers who herded the cattle and conducting cattle drives. Vaca means “cow” and a vaquero is “one who works with cows.” The Spanish mission padres recognized this labor and conscripted mestizos (mixed-race people), Indians, and Mexicans to take care of the cattle. It was these individuals who developed the system, equipment, practices, and traditions that have lasted these past few hundred years. The Anglo cowboy learned everything about cattle from the vaquero.
The Mexican vaquero was a laborer, a peon who was used by the missionaries to ride the horses and take care of the cattle. So it was the culture of the vaquero that became the basis for the romantic cowboy of Hollywood. The ensemble, equipment, and clothing of the vaquero evolved through the years as a combination of Spanish leather and regional indigenous fabrics. He always wore a sombrero with a wide brim, a leather chaqueta (jacket), tight-fitting knee-length sotas (breeches), and botas (leather leggings) for protection. The vaquero also wore iron spurs, like those worn by the Conquistadores, which are still worn to this day. The various styles of saddles, from the Moorish to the Spanish war saddle, eventually changed when the vaqueros began making their own saddles, more suitable for riding hard and for quick mounting and dismounting.
``

Here i'm using -i to find the word Hollywood. Notice the case-sensitive-ness of the word i used.

``
[cs15lwi23auj@ieng6-203]:skill-demo1-data:501$ grep -i "CoWBoY" written_2/non-fiction/OUP/Castro/chV.txt
Vaqueros (Cowboys)
The vaquero was the early Hispano cowboy and the antecedent of the Hollywood cowboy.
...
```

Here I used the word Cowboys as my second example. Similarly notice the capitualization of the string in the command. 

Whereas -w finds whole words and IS case- sensitive, -i is not case-senstive and finds the word even if it is encumbered in another word. This also means that no matter how I typed my word, it will find it. This is particularly useful in the case where my first word is both the first word of a sentence, and when it is not. It is also will find my word even if its a part of another word, like "holly" is found in "hollywood". 

I used chatGPT in order to find this command, and the sources it refrenced is [Linux guide]https://linux.die.net/man/1/grep . 


