Total Sales Volume = SUM('BMW'[Sales_Volume])
Total Revenue = SUM('BMW'[Price_USD])
Average Price = AVERAGE('BMW'[Price_USD])
Net Sales By Region = CALCULATE(SUM('BMW Project'[Net Sales]), ALLEXCEPT('BMW Project','BMW Project'[Region]))