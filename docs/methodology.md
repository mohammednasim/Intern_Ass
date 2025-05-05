# Methodology for Scoring Compound V2 Wallets

## Overview
The goal of this project is to build a credit scoring model for wallets interacting with the Compound V2 protocol based on their transaction behavior.

## Data Processing
The raw data provided contains records for various transactions including deposits, withdrawals, borrows, repayments, and liquidations. The data was cleaned and flattened to extract key details, including wallet ID, event type, transaction amount, and timestamps.

## Feature Engineering
We derived several features from the transaction data:
- Count of each type of event per wallet (deposits, withdraws, borrows)
- Total transaction amounts for each wallet per event type
- Normalized features to ensure equal weight distribution across different types of transactions

## Credit Scoring
The final credit score is calculated as a weighted sum of normalized features:
- 40% based on total deposits
- 30% based on total withdrawals
- 30% based on total borrows

Scores are scaled between 0 and 100, with higher scores reflecting more responsible wallet behavior.

## Conclusion
The credit scoring model was designed to highlight wallets that interact responsibly with the protocol. The model is highly customizable, allowing for further tuning and feature additions.
