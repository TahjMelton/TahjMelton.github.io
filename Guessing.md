# Number Button Game
## Hit the button and guess what the random number is!
## This game is pretty simple! Press the RNG ( Random Number Generated) button to have the system pick a number and, you the player will guess between the values 1-10 since the system can't exceed that value. You get one try to guess the number no matter the results you will have to press the button again to retry. Any number taken in exceeding the value 10 however will be deemed as an error and will still give you the option to guess the same try.
```mermaid
flowchart TD
Start([ RNG Button Pressed])-->Ops([Value is generated])
Start-->A([User fills in blank for value]) 
Ops--> B(Value can't exceed 10)
A--> C(Values between 1-10)
B-->D(System error when value exceeds 10 from blank)
C-->E(Receives value past 10)
C-->F(Receives values within 10)
E--xG(Error: Value too high)
D--xG
B-->H(System success when value within 10)
H-->I(Green checkmark when correct value)
H-->J(Red X when incorrect value)
F-->K( When value is correct)
K-->I
F-->L(When value is incorrect)
L-->J
```
