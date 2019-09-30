01. Doing some practice on Jupyter/Anaconda I've built a X-Wing 2.0 (miniatures game) simulator. It is a brief code that simulates thousands of X-Wing 2.0 shots or battles to study some tactical decissions. 1/11

02. First, shooting analysis. This is the average damage in an attack, attack dice vs defense dice. Of course, it can be built without simulations with simple probability analysis. 2/11

03. Now, real results. Focus vs evasion. If the attacker has 1 dice defender has to evade. In other cases (up to 4 defender dice) it is better to focus (and it is more flexible) 3/11

04. Attacking, focus or target lock? Amazingly Focus is better than Target in all cases I've simulated.  4/11

05. I have made also some "full battle" simulations. The model is quite simple. It assumes that all ships can fire all enemies always. So manoeouvres, critical damage or obstacles are not considered.  5/11

06. In the introductory box (two TIEs vs 1 X-Wing) Imperials have an important advantage. They shall win 60% of times. 6/11


07. Initiative has a certain influence in victory probability, due to the "kill first" factor. First to shoot can win up to 10% chance of winning the battle. Which means that many theoretical encounters finish with both sides being killed in the same turn. 7/11


08. Of course number is importante and several small ships can beat a bigger one. In the simulations 3 TIEs win 45% times against Millenium Falcon, but 4 TIEs win 85% of simulations. 8/11


09. Attack is better than defense. A fleet of 3-2 ships beats an equivalent fleet of 2-3 58% of battles, and the ratio grows with fleet size. 9/11


10. Is it better to attack first the strongest ship or the weakest ship? Go first for the less defended, more damaging ship. If both factors oppose, prime damage: go for the most heavily armed ship. The difference is 4-14% of winning probability. 10/11


11. Full code is here: https://github.com/zorzano/XWingSimulator . Please test and improve it. Pull requests are welcome. CC  #xwing #miniatures @MetropolisCnter @genxoficial @genxcarranza @FFGames  11/11



Some notes on the code:

attack() simulates a single attack and the corresponding defense. 

battle() simulates a full battle between two lists of ships. Each ship is a tuple formed by: (initiative, attack, defense, strength). Each fleet focus all attack in the last ship of the enemy list. Once destroyed they will attack the next one.

Text cells explain whatever we learn with the code.