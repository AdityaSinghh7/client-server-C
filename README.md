# Stock Analysis Tool in C

## Overview
This project implements a client-server architecture in C to perform stock analysis. The client application sends commands to the server to retrieve stock prices, calculate maximum profits over a given period, and list available stocks.

## Files
- `client.c`: The client program that connects to the server, sends commands, and processes responses.
- `server.c`: The server program that listens for connections, processes commands, and sends back the computed data.
- `MSFT.csv`: CSV file containing historical stock data for Microsoft (MSFT).
- `TSLA.csv`: CSV file containing historical stock data for Tesla (TSLA).

## Functionality
- **Prices**: Fetches the stock prices for specific dates.
- **MaxProfit**: Calculates the maximum profit that could have been made between two dates by buying at a low price and selling at a high price.
- **List**: Lists the stocks available for querying.

## Usage
1. Compile the client and server programs:
   ```
   gcc client.c -o client
   gcc server.c -o server
   ```
2. Start the server:
   ```
   ./server <port number>
   ```
3. Run the client, connecting to the server:
   ```
   ./client <server IP> <port number>
   ```
## Example Commands

1. Fetch price for MSFT on 2021-03-15:
   ```
   Prices MSFT 2021-03-15
   ```
2. Calculate maximum profit for TSLA between 2021-01-01 and 2021-12-31:
   ```
   MaxProfit TSLA 2021-01-01 2021-12-31
   ```
3. List all available stocks:
   ```
   List
   ```
