# Tronscan USDT Parser Macro

This macro helps cryptocurrency investigators using **Tronscan** to filter transactions involving **USDT (Tether)** on the TRON blockchain and calculate the running balance for a specific Ethereum address (EOA). It is designed for use with **LibreOffice Calc** and can be integrated easily into your spreadsheets.

## Features
- **Filter transactions** to only include USDT transfers.
- **Sort transactions** by timestamp (ascending order).
- **Calculate running balance** for a specific address across filtered transactions.
- **Color coding**: Inbound transactions are highlighted in green, while outbound transactions are red.
- **Support for USDT**: Uses the TRON address for USDT transfers to filter and analyze the data.

## Prerequisites
- **LibreOffice Calc** (or OpenOffice Calc) installed.
- The macro was developed and tested utilizing LibreOffice Calc V.25.8.2.2

## Setup Instructions

1.  Obtain the CSV file for your target address. Go to Tronscan, query your address of interest, and navigate to the "Transfers" tab. Select the "Download CSV File" on the bottom left of the screen. There does not appear to be a stated limit to transaction count.
2.  Load your CSV export into LibreOffice Calc
3.  Open the macro editor and paste the provided macro code. (Tools > Macros > Edit Macros > Module 1). You can also create a seperate module for the macro (recommended)
4.  Run the Tronscan USDT Parser Macro. (Tools > Macros > Run Macro > select macro)
5.  You will be prompted to enter your Tron Target Address for calculating the running balance

The macro will filter the transactions of USDT tokens and compute the running balance for the target address.
The sheet will display the running balance and highlight inbound (green) and outbound (red) transactions.

## How it Works
- The macro will search for transactions involving **USDt** based on the USDt contract TRON address `TR7NHqjeKQxGTCi8q8ZY4pL8otSzgjLj6t`.
- It will filter out non-USDT transactions.
- The transactions are then **sorted by timestamp** in ascending order.
- A **running balance** will be calculated for the target Ethereum address based on the filtered transactions.
- The results will be shown directly in the spreadsheet with each row colored based on whether the transaction is inbound (green) or outbound (red).


## Example Output
After running the macro, you’ll see:
- A new column labeled **Running Balance** will be added to the right of your data.
- Each transaction will be color-coded based on whether the amount is incoming or outgoing to the target address.

## License
See license file for information


