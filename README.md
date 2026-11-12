## FINE3300-2026-A2-Shiva-Moslemin-Asl

# Project Overview

This project is a Canadian inflation calculator. The program reads monthly Consumer Price Index (CPI) data from `cpi_data.csv` and calculates the equivalent cost of goods or services between two months.

The project uses Pandas to read and filter the data, NumPy for calculations and input validation, and Matplotlib to create a graph. The code is saved in `inflation_calc.ipynb`.

The dataset is available through the [Bank of Canada Inflation Calculator](https://www.bankofcanada.ca/rates/related/inflation-calculator/).

# Shiva's Inflation Calculator

I created a calculator that allows the user to:

- Enter a positive price and two dates using `YYYY-MM` format
- Check that the price is valid and both months exist in the dataset
- Calculate the equivalent price and total percentage change
- Display the number of years, average annual inflation rate, and CPI values
- Print prices with currency identifiers, dollar signs, commas, and two decimal places

# CPI Graph

![Canadian CPI and annual inflation](cpi_graph.png)

The graph displays CPI on the left axis and year-over-year percentage change on the right. The dotted line represents the base level of 2002 = 100.

The CPI increased substantially over time. Inflation fluctuated, with elevated rates during the 1970s and early 1980s and another increase in the early 2020s.

# Sample Output

Using CAD $100, January 2020, and January 2025:

```text
Original price in 2020-01: CAD $100.00
Equivalent price in 2025-01: CAD $117.91
Total percentage change: 17.91%
Number of years: 5.00
CPI for 2020-01: 136.8
CPI for 2025-01: 161.3
Average annual inflation rate: 3.35%
```

# How to Run

1. Download and extract the repository, then open its folder in VS Code.
2. Install the Microsoft Python and Jupyter extensions.
3. Install the required packages in the terminal if they are not already installed:

   ```bash
   python3 -m pip install pandas numpy matplotlib ipykernel
   ```

4. Open `inflation_calc.ipynb`, select a Python kernel, and run the cells in order.
5. Enter the price without dollar signs or commas and both dates when prompted.

Keep `cpi_data.csv` in the same folder as the notebook. Rerun the calculator cell to try different inputs.