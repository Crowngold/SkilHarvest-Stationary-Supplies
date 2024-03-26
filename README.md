# SkilHarvest-Stationary-Supplies

## Google Query Functions
Query dunctions are used to manipulate and extract data in Google sheets.

### QUERY FUNCTION SYNTAX
  ```
      = QUERY (data, query, [headers])
  ```

The "= QUERY" function has 3 defined parameters;
1. Data: is defined as the range of data that needs to be analyzed
2. Query: is defined as the way data is processed, always enclosed in quotations.
3. Header: is defined as the optimal number for when you need to indicate the number of header rows in your data.

## Dataset Description

The dataset Skilharvest Stationary supplies shows the sales items, sales rep, region of sales, month and year of sales, order date and sales.
My aim is to query the data using the query function and extract some important details from the dataset. The dataset overview as sown in Google sheet is displayed below;
![](https://github.com/Crowngold/SkilHarvest-Stationary-Supplies/blob/main/SKILHARVEST%20DATASET.jpg)


### TASKS
1. Show sales of binder items and pencil in 2015.
2. Show sales in Central and East region in 2014.
3. Show sales in August and September 2014.
4. Show sales of items that start with 'Pen', include their region, sales rep and year.
5. Show sales of items that start with 'sk', include their region, sales rep and year.

## Data Extraction

### TASK 1 SOLUTION
```
    =QUERY(A:H, "SELECT C,F,H WHERE (C='Binder' or C='Pencil') AND F=2015",1)
```
![](https://github.com/Crowngold/SkilHarvest-Stationary-Supplies/blob/main/TASK%201.jpg)



### TASK 2 SOLUTION
```
    =QUERY(A:H, "SELECT A,B,F WHERE (A='Central' OR A='East') AND F=2014",1)
```
![](https://github.com/Crowngold/SkilHarvest-Stationary-Supplies/blob/main/TASK%202.jpg)
### TASK 3 SOLUTION
```
    =QUERY(A:H, "SELECT A,B,E,F,H WHERE (E='Aug' OR E='Sep') AND F=2014",1)
```

### TASK 4 SOLUTION
```
    =QUERY(A:H, "SELECT A,B,C,F,H WHERE C LIKE 'Pen%'",1)
```

### TASK 5 SOLUTION
```
    =QUERY(A:H, "SELECT A,B,C,F,H WHERE C LIKE '%sk'",1)
```
