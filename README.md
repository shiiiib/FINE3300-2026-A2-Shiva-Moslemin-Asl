## FINE3300-2026-A2-Shiva-Moslemin-Asl

## Project Overview

This project uses monthly Canadian Consumer Price Index (CPI) data to create a graph and calculate the equivalent cost of a purchase between two given years.

The notebook contains two separate code blocks. The first creates the graph, while the second runs the calculator using an `InflationCalculator` class.

The project uses Pandas to organize data, NumPy for numerical calculations and validation, and Matplotlib for graphing.

Data is available through the [Bank of Canada Inflation Calculator](https://www.bankofcanada.ca/rates/related/inflation-calculator/).

## Project Files

- `inflation_calc.ipynb` — Contains the CPI graph and inflation calculator.
- `cpi_data.csv` — Contains the Canadian CPI data used by the notebook.
- `CPI_Graph.png` — Displays the CPI and annual inflation graph.
- `README.md` — Contains the project description, instructions, graph, and sample output.

## CPI Graph

![Canadian CPI and annual inflation](CPI_Graph.png)

The graph uses the full monthly dataset. CPI appears on the left axis, and year-over-year percentage change appears on the right. The dotted line marks the base level of 2002 = 100.

Consumer prices increased substantially over time. Inflation fluctuated, with elevated rates during the 1970s and early 1980s and another increase in the early 2020s.

## Shiva's Inflation Calculator

The `InflationCalculator` class reads the CSV, extracts the years, and keeps the last available monthly observation from each year.

The user enters a positive price and two years. The calculator:

- Accepts prices with commas, spaces, and decimal places
- Checks that the price is valid and both years exist
- Uses the CPI from December when available, as it reflects the most recent CPI of that year (or would use the latest available month for an incomplete year)
- Displays the equivalent price, total percentage change, elapsed years, annual inflation rate, and selected CPI months
- Formats prices with currency identifiers, dollar signs, commas, and two decimal places

The annual rate uses the actual time between the selected CPI months. Identical years produce no price change and an annual rate of N/A.

## How to Run

1. Download and extract the repository, then open the folder in VS Code.
2. Install the Microsoft Python and Jupyter extensions.
3. Install the required packages in the terminal:

   ```bash
   python3 -m pip install pandas numpy matplotlib ipykernel
   ```

4. Open `inflation_calc.ipynb` and select a Python kernel.
5. Run the graph cell to display the graph and save `CPI_Graph.png`.
6. Run the calculator cell and enter the requested price and years.

Keep `cpi_data.csv` beside the notebook. Enter prices without dollar signs. Rerun the calculator cell for another calculation.
