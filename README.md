Cellular_automaton_model_of_Banded_vegetation
=============================================

Environmental Modelling course: Final Project

This document discusses the development of a terrame model based on the paper of 
D. L. Dunkerley  with a title  “Banded vegetation: development under uniform rainfall 
from a simple cellular automaton model”.
In his paper,  D. L. Dunkerley  describes  a  cellular automata  model which simulates 
the  development  of  banded  vegetation  in  semi-arid  and  arid  landscapes  like
Chihuahuan  Desert  of  Mexico.    A  simple  cellular  automata  model  is  developed  to 
simulate  that  water  distribution  mechanism  like  absorption  and  evaporation  can 
develop  a  banded  vegetation  distribution. This  model  is  simple  without  take  under 
consideration the climatic change or external disturbance.
The point of our  research  is to develop the same or an  approximately  similar  model 
based on the paper of D. L. Dunkerley.

Rules of cellular automata model
Our approach is to create a cellular automata model based on the follow rules:
1.Tessellation of 2500 cells (50x50).
2.100 mm yearly rain is distributed uniformly to all cells,
3.Plant cells share 10% of their water with the down slope cells and absorb the 
rest.
4.Bare cells share (90% of rain + whole run-on water) and absorb 10% of rain 
water.
5.Cells with moisture less than 1.2-3.5 times the annual rainfall becomes bare 
cells.
6.Cells with moisture levels of 0.6-1.2 times the annual rainfall becomes plant 
cells.
7.In iterations plant cells dried out to 10 mm and bare cells dried out totally.

Development of cellular automata model
The next steps were followed for the development of our model.
1.Creation of a 50x50 CellularSpace
2.Fill of the CellularSpace with bare and plant cells. The distribution is random.
3.Use of the strategy = “3x3”. This strategy consider us neighbours only the down
slope cells and is  useful  in our case as the water is flowing from to top to the 
bottom. 
4.For each cell of the CellularSpace the code check if the cell is bare or plant.
5.The  system  treated  like  a  run  on,  run  off  system.  The  amount  of 
running  off  water  is  calculated for  every  plant  and  bare  cell  separately.  In  this 
way the observed water of each cell is calculated as: Observed = run on – run off.

Finally, the value of the observed water is compared to the moisture limited values.

6.After of every iteration,  plant cells dried out to 10 mm and bare cells dried out 
totally.
