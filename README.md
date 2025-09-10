# Programming Assignment 3
## Problem 1
```py
import pandas as pd
```
Step 1: Importing the Pandas library is the most important step when coding scripts related to data structures; which Pandas specializes on.

```py
cars = pd.read_csv("cars.csv")
```
Step 2: Load the pre-existing csv file provided and set the file to the variable cars using the code "pd.read_csv" which tells the system to read the csv file in the parenthesis--in this case "cars.csv", and assign it to the variable cars. Note that it has to be in the same folder as the notebook file in order for it to read the csv file.

```py
cars

Model	mpg	cyl	disp	hp	drat	wt	qsec	vs	am	gear	carb
0	Mazda RX4	21.0	6	160.0	110	3.90	2.620	16.46	0	1	4	4
1	Mazda RX4 Wag	21.0	6	160.0	110	3.90	2.875	17.02	0	1	4	4
2	Datsun 710	22.8	4	108.0	93	3.85	2.320	18.61	1	1	4	1
3	Hornet 4 Drive	21.4	6	258.0	110	3.08	3.215	19.44	1	0	3	1
4	Hornet Sportabout	18.7	8	360.0	175	3.15	3.440	17.02	0	0	3	2
5	Valiant	18.1	6	225.0	105	2.76	3.460	20.22	1	0	3	1
6	Duster 360	14.3	8	360.0	245	3.21	3.570	15.84	0	0	3	4
7	Merc 240D	24.4	4	146.7	62	3.69	3.190	20.00	1	0	4	2
8	Merc 230	22.8	4	140.8	95	3.92	3.150	22.90	1	0	4	2
9	Merc 280	19.2	6	167.6	123	3.92	3.440	18.30	1	0	4	4
10	Merc 280C	17.8	6	167.6	123	3.92	3.440	18.90	1	0	4	4
11	Merc 450SE	16.4	8	275.8	180	3.07	4.070	17.40	0	0	3	3
12	Merc 450SL	17.3	8	275.8	180	3.07	3.730	17.60	0	0	3	3
13	Merc 450SLC	15.2	8	275.8	180	3.07	3.780	18.00	0	0	3	3
14	Cadillac Fleetwood	10.4	8	472.0	205	2.93	5.250	17.98	0	0	3	4
15	Lincoln Continental	10.4	8	460.0	215	3.00	5.424	17.82	0	0	3	4
16	Chrysler Imperial	14.7	8	440.0	230	3.23	5.345	17.42	0	0	3	4
17	Fiat 128	32.4	4	78.7	66	4.08	2.200	19.47	1	1	4	1
18	Honda Civic	30.4	4	75.7	52	4.93	1.615	18.52	1	1	4	2
19	Toyota Corolla	33.9	4	71.1	65	4.22	1.835	19.90	1	1	4	1
20	Toyota Corona	21.5	4	120.1	97	3.70	2.465	20.01	1	0	3	1
21	Dodge Challenger	15.5	8	318.0	150	2.76	3.520	16.87	0	0	3	2
22	AMC Javelin	15.2	8	304.0	150	3.15	3.435	17.30	0	0	3	2
23	Camaro Z28	13.3	8	350.0	245	3.73	3.840	15.41	0	0	3	4
24	Pontiac Firebird	19.2	8	400.0	175	3.08	3.845	17.05	0	0	3	2
25	Fiat X1-9	27.3	4	79.0	66	4.08	1.935	18.90	1	1	4	1
26	Porsche 914-2	26.0	4	120.3	91	4.43	2.140	16.70	0	1	5	2
27	Lotus Europa	30.4	4	95.1	113	3.77	1.513	16.90	1	1	5	2
28	Ford Pantera L	15.8	8	351.0	264	4.22	3.170	14.50	0	1	5	4
29	Ferrari Dino	19.7	6	145.0	175	3.62	2.770	15.50	0	1	5	6
30	Maserati Bora	15.0	8	301.0	335	3.54	3.570	14.60	0	1	5	8
31	Volvo 142E	21.4	4	121.0	109	4.11	2.780	18.60	1	1	4	2
```
Step 2.1: This part is optional but outputting the loaded csv file would be a great way to make sure that the code worked as intended.

```py
pd.concat([cars.head(), cars.tail()])

Model	mpg	cyl	disp	hp	drat	wt	qsec	vs	am	gear	carb
0	Mazda RX4	21.0	6	160.0	110	3.90	2.620	16.46	0	1	4	4
1	Mazda RX4 Wag	21.0	6	160.0	110	3.90	2.875	17.02	0	1	4	4
2	Datsun 710	22.8	4	108.0	93	3.85	2.320	18.61	1	1	4	1
3	Hornet 4 Drive	21.4	6	258.0	110	3.08	3.215	19.44	1	0	3	1
4	Hornet Sportabout	18.7	8	360.0	175	3.15	3.440	17.02	0	0	3	2
27	Lotus Europa	30.4	4	95.1	113	3.77	1.513	16.90	1	1	5	2
28	Ford Pantera L	15.8	8	351.0	264	4.22	3.170	14.50	0	1	5	4
29	Ferrari Dino	19.7	6	145.0	175	3.62	2.770	15.50	0	1	5	6
30	Maserati Bora	15.0	8	301.0	335	3.54	3.570	14.60	0	1	5	8
31	Volvo 142E	21.4	4	121.0	109	4.11	2.780	18.60	1	1	4	2
```
Step 3: Display the first and last fives rows of the resulting cars. We did this by using a Pandas command "cars.head()" for the first five, and "cars.tail()" for the last five, and at the same time, in order to output it seemlessly, we concatenate said outputs using "pd.concat".

## -----------------------------------------------------------------------------------------------
## Problem 2

```py
import pandas as pd
```
Step 1: Once again, the most important step in order to utilize the Pandas library, we must first load the library into our code.
```py
cars = pd.read_csv("cars.csv")
```
Step 2: Load the csv file named "cars.csv" and set its values to the variable "cars" using the Pandas commnad "pd.read_csv"

```py
cars

Model	mpg	cyl	disp	hp	drat	wt	qsec	vs	am	gear	carb
0	Mazda RX4	21.0	6	160.0	110	3.90	2.620	16.46	0	1	4	4
1	Mazda RX4 Wag	21.0	6	160.0	110	3.90	2.875	17.02	0	1	4	4
2	Datsun 710	22.8	4	108.0	93	3.85	2.320	18.61	1	1	4	1
3	Hornet 4 Drive	21.4	6	258.0	110	3.08	3.215	19.44	1	0	3	1
4	Hornet Sportabout	18.7	8	360.0	175	3.15	3.440	17.02	0	0	3	2
5	Valiant	18.1	6	225.0	105	2.76	3.460	20.22	1	0	3	1
6	Duster 360	14.3	8	360.0	245	3.21	3.570	15.84	0	0	3	4
7	Merc 240D	24.4	4	146.7	62	3.69	3.190	20.00	1	0	4	2
8	Merc 230	22.8	4	140.8	95	3.92	3.150	22.90	1	0	4	2
9	Merc 280	19.2	6	167.6	123	3.92	3.440	18.30	1	0	4	4
10	Merc 280C	17.8	6	167.6	123	3.92	3.440	18.90	1	0	4	4
11	Merc 450SE	16.4	8	275.8	180	3.07	4.070	17.40	0	0	3	3
12	Merc 450SL	17.3	8	275.8	180	3.07	3.730	17.60	0	0	3	3
13	Merc 450SLC	15.2	8	275.8	180	3.07	3.780	18.00	0	0	3	3
14	Cadillac Fleetwood	10.4	8	472.0	205	2.93	5.250	17.98	0	0	3	4
15	Lincoln Continental	10.4	8	460.0	215	3.00	5.424	17.82	0	0	3	4
16	Chrysler Imperial	14.7	8	440.0	230	3.23	5.345	17.42	0	0	3	4
17	Fiat 128	32.4	4	78.7	66	4.08	2.200	19.47	1	1	4	1
18	Honda Civic	30.4	4	75.7	52	4.93	1.615	18.52	1	1	4	2
19	Toyota Corolla	33.9	4	71.1	65	4.22	1.835	19.90	1	1	4	1
20	Toyota Corona	21.5	4	120.1	97	3.70	2.465	20.01	1	0	3	1
21	Dodge Challenger	15.5	8	318.0	150	2.76	3.520	16.87	0	0	3	2
22	AMC Javelin	15.2	8	304.0	150	3.15	3.435	17.30	0	0	3	2
23	Camaro Z28	13.3	8	350.0	245	3.73	3.840	15.41	0	0	3	4
24	Pontiac Firebird	19.2	8	400.0	175	3.08	3.845	17.05	0	0	3	2
25	Fiat X1-9	27.3	4	79.0	66	4.08	1.935	18.90	1	1	4	1
26	Porsche 914-2	26.0	4	120.3	91	4.43	2.140	16.70	0	1	5	2
27	Lotus Europa	30.4	4	95.1	113	3.77	1.513	16.90	1	1	5	2
28	Ford Pantera L	15.8	8	351.0	264	4.22	3.170	14.50	0	1	5	4
29	Ferrari Dino	19.7	6	145.0	175	3.62	2.770	15.50	0	1	5	6
30	Maserati Bora	15.0	8	301.0	335	3.54	3.570	14.60	0	1	5	8
31	Volvo 142E	21.4	4	121.0	109	4.11	2.780	18.60	1	1	4	2
```
Step 2.1: Again, this part is optional. But doing so will alow you to check if the code you entered had worked as intended.

### A. Display the first five rows with odd-numbered columns (columns 1, 3, 5, 7…) of cars.
```py
cars.iloc[[0, 1, 2, 3, 4],[0, 2, 4, 6, 8, 10]]

Model	cyl	hp	wt	vs	gear
0	Mazda RX4	6	110	2.620	0	4
1	Mazda RX4 Wag	6	110	2.875	0	4
2	Datsun 710	4	93	2.320	1	4
3	Hornet 4 Drive	6	110	3.215	1	3
4	Hornet Sportabout	8	175	3.440	0	3

```
Step 3: In order to display the first five rows in the given csv file, we must utilize the call ".iloc" which uses the index of every value in the list in order to locate it. For this instance, we used it to locate indices "0, 1, 2, 3, 4" for our first 5 rows. Meanwhile using the second part of the call we can also print the columns we need--which are odd-numbers columns. In order to do that we must input their specific index starting from the first column with an index of 0 "0, 2, 4, 6, 8, 10"

#### B. Display the row that contains the ‘Model’ of ‘Mazda RX4’.
```py
cars[0:1]

Model	mpg	cyl	disp	hp	drat	wt	qsec	vs	am	gear	carb
0	Mazda RX4	21.0	6	160.0	110	3.9	2.62	16.46	0	1	4	4

```
Step 4: In order to display certain row/s we can use the variable we assigned those values to and ranges. For my code, I used the 0:1, which locates among the rows which of them has the index of 0 to 1 excluding the row with index 1 assigned to it, and then print it.

#### C. How many cylinders (‘cyl’) does the car model ‘Camaro Z28’ have?

```py
cars.loc[[23], ["Model", "cyl"]]

	Model	cyl
23	Camaro Z28	8
```
Step 5: In order to print a specific column like in this case where we need to print the column with "cyl" on the specific row we are finding it for, we can use the code ".loc" which searches which columns have the same name as the one you inputted. They compare strings as opposed to ".iloc" which compares indices with each other in order ot find elements. Here I added the column where the model is assigned to so that it wouldn't be confused for any other row.

#### D. Determine how many cylinders (‘cyl’) and what gear type (‘gear’) do the car models ‘Mazda RX4 Wag’, ‘Ford Pantera L’ and ‘Honda Civic’ have.
```py
cars.loc[[1, 28, 18], ["Model", "cyl", "gear"]]

Model	cyl	gear
1	Mazda RX4 Wag	6	4
28	Ford Pantera L	8	5
18	Honda Civic	4	4
```
Step 6: Utilizing the code ".loc" can also output multiple columnns at the same time using strings instead of indices. Using this, we are able to print out the columns that contain the values of "Model", "cyl", and "gear".

# ------------------------------------------------------------------------------
