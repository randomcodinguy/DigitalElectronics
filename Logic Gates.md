**Logic Gates are the basic building blocks of any digital system. They are of three types:**
- **Basic Gates:** AND, OR, NOT
- **Universal Gates:** NAND, NOR
- **Special Gates:** XOR, XNOR

### --> Basic Gates

Basic gates are the fundamental building blocks used to design and construct more complex logical circuits. AND, OR, and NOT gate are called as basic gate as we can design a Boolean of any complexity with combination of these gates.
#### A: AND Gate

##### 1: Logic Symbol
![Imgur](https://i.imgur.com/25BfSLy.png)
Output (Y) = A * B * C or ABC

##### 2: Truth Table
Truth Table is a table, which consists all the possible input combinations along with their corresponding outputs

| A | B | C | Output |
| ---- | ---- | ---- | ---- |
| 0 | 0 | 0 | 0 |
| 0 | 0 | 1 | 0 |
| 0 | 1 | 0 | 0 |
| 0 | 1 | 1 | 0 |
| 1 | 0 | 0 | 0 |
| 1 | 0 | 1 | 0 |
| 1 | 1 | 0 | 0 |
| 1 | 1 | 1 | 1 |

#### B: OR Gate

##### 1: Logic Symbol
![Imgur](https://i.imgur.com/E6GD1rf.png)
Output (Y) = A + B + C

##### 2: Truth Table 
| A | B | C | Output |
| ---- | ---- | ---- | ---- |
| 0 | 0 | 0 | 0 |
| 0 | 0 | 1 | 1 |
| 0 | 1 | 0 | 1 |
| 0 | 1 | 1 | 1 |
| 1 | 0 | 0 | 1 |
| 1 | 0 | 1 | 1 |
| 1 | 1 | 0 | 1 |
| 1 | 1 | 1 | 1 |

#### C: NOT Gate

##### 1: Logic Symbol
Takes a single input and gives a single output
![Imgur](https://i.imgur.com/rNgsbqt.png)
Output (Y) = ~A

##### 2: Truth Table
| A | Output |
| ---- | ---- |
| 0 | 1 |
| 1 | 0 |
**NOTE:** If two NOT Gate are connected in series you can remove them, as ~(~(A)) = A, therefore it will not change any functionality.

### --> Universal Gates
#### A: NAND Gate
It is AND Gate followed by a NOT Gate. NAND outputs 1 if any of the input is 0. 
We can design the 3 Basic Gates using NAND Gate, and we have already discussed that it is possible to design a Boolean function of any complexity using Basic Gates. So we can conclude now that using only NAND Gate we can design a Boolean function of any complexity, so NAND Gate is called Universal Gate. 
##### 1: Logic Symbol
![Imgur](https://i.imgur.com/hrkXqGf.png)
Output (Y) = ~(ABC)

##### 2: Truth Table

| A   | B   | C   | ABC | Output |
| --- | --- | --- | --- | ------ |
| 0   | 0   | 0   | 0   | 1      |
| 0   | 0   | 1   | 0   | 1      |
| 0   | 1   | 0   | 0   | 1      |
| 0   | 1   | 1   | 0   | 1      |
| 1   | 0   | 0   | 0   | 1      |
| 1   | 0   | 1   | 0   | 1      |
| 1   | 1   | 0   | 0   | 1      |
| 1   | 1   | 1   | 1   | 0      |
**NOTE:** All the above discussion about NAND Gate is also valid for NOR Gate, so NOR Gate is also called Universal Gate

##### 3: NAND as Universal Gate
- ###### NAND as NOT Gate: 
	![Imgur](https://i.imgur.com/In32i0V.png)


- ###### NAND as AND Gate:
	![Imgur](https://i.imgur.com/p1AvqCn.png)

- ###### NAND as OR Gate:
	![Imgur](https://i.imgur.com/lmskCXD.png)
	OR = A + B
	=~(~(A + B))
	=~(~A * ~B)                       {By DeMorgan's Law ~(A + B) = (~A * ~B)}
	
- **NOTE:** AB + CD can be done using minimum 3 NAND Gates

#### B: NOR Gate
OR gate followed by NOT Gate

##### 1: Logic Symbol
![Imgur](https://i.imgur.com/Gb7D8qr.png)
Output(Y) = ~(A + B)

##### 2: Truth Table

| A   | B   | C   | A + B + C | Output |
| --- | --- | --- | --------- | ------ |
| 0   | 0   | 0   | 0         | 1      |
| 0   | 0   | 1   | 1         | 0      |
| 0   | 1   | 0   | 1         | 0      |
| 0   | 1   | 1   | 1         | 0      |
| 1   | 0   | 0   | 1         | 0      |
| 1   | 1   | 0   | 1         | 0      |
| 1   | 1   | 1   | 1         | 0      |
##### 3: NOR as Universal Gate
- ###### NOR as NOT Gate:
	![Imgur](https://i.imgur.com/OD9YQlJ.png)
- ##### NOR as AND Gate:
	![Imgur](https://i.imgur.com/1tMLGt4.png)
- ##### NOR as OR Gate
	![Imgur](https://i.imgur.com/h1JCXJ4.png)
- **NOTE:** (A+B)(C+D) can be done using minimum 3 NOR Gates

### --> Special Purpose Gates

#### A: EXOR Gate
Exclusive OR Gate

##### 1: Logic Symbol
![Imgur](https://i.imgur.com/yqTzIJd.png)
Output(Y) = ~AB+~BA

##### 2: Truth Table

| A   | B   | ~AB+~BA | Output |
| --- | --- | ------- | ------ |
| 0   | 0   | 0       |        |
| 0   | 0   | 1       |        |
| 0   | 1   | 1       |        |
| 0   | 1   | 1       |        |
| 1   | 0   | 1       |        |
| 1   | 1   | 1       |        |
| 1   | 1   | 1       |        |
