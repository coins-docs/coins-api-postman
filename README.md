# Coins API Postman Collection

A comprehensive Postman collection for Coins Public API, including spot trading, convert, fiat, wallet, and other essential endpoints.

## 📋 API Modules Overview

This Postman collection contains 11 main modules with complete API coverage:

### 1. Spot Trading
- **My Trades** (`myTrades`) - Query user's trading history
- **Trade Fee** (`tradeFee`) - Get trading fee information
- **Test Order** (`order_test`) - Test order creation (no actual execution)
- **New Order** (`order_new`) - Create new trading orders
- **Order Details** (`order_detail`) - Query specific order details
- **Open Orders** (`openOrders`) - Get current unfilled orders
- **Cancel Order** (`order_cancel`) - Cancel specific orders
- **Cancel All Orders** (`order_cancelAll`) - Cancel all open orders
- **Order History** (`order_history`) - Query historical orders
- **Cancel Replace Order** (`order_cancelReplace`) - Cancel and replace orders

### 2. Convert
- **Get Supported Trading Pairs** (`get-supported-trading-pairs`) - Query supported conversion pairs
- **Get Quote** (`get-quote`) - Get conversion quotes
- **Accept Quote** (`accept-quote`) - Accept quotes and execute conversion
- **Query Order History** (`query-order-history`) - Query conversion order history

### 3. Fiat
- **Support Channel** (`support-channel`) - Query supported fiat channels
- **Details** (`details`) - Get fiat order details
- **History** (`history`) - Query fiat transaction history
- **Cash Out** (`cash_out`) - Execute fiat withdrawal operations

### 4. General
- **Exchange Info** (`exchangeInfo`) - Get exchange basic information
- **Pairs** (`pairs`) - Get all available trading pairs
- **Ping** (`ping`) - Test API connectivity
- **Time** (`time`) - Get server current time

### 5. Invoice
- **Create Invoice** (`invoices`) - Create new payment invoices
- **Get Invoices** (`get_invoices`) - Query invoice information
- **Cancel Invoice** (`invoices-cancel`) - Cancel specific invoices

### 6. Listen (WebSocket)
- **Get Listen Key** (`get_listen_key`) - Get WebSocket listen key
- **Update Listen Key** (`put_listen_key`) - Update listen key validity
- **Delete Listen Key** (`delete_listen_key`) - Delete listen key

### 7. Market Data
- **Average Price** (`avgPrice`) - Get average price for trading pairs
- **Depth** (`depth`) - Get market depth data
- **Klines** (`klines`) - Get K-line/candlestick data
- **24hr Ticker** (`ticker_24hr`) - Get 24-hour price change statistics
- **Book Ticker** (`ticker_bookTicker`) - Get best bid/ask prices
- **Price Ticker** (`ticker_price`) - Get latest trading prices
- **Recent Trades** (`trades`) - Get recent trade records

### 8. P2P Transfer
- **Crypto Accounts** (`crypto_accounts`) - Get cryptocurrency account information
- **P2P Transfer** (`p2p_transfer`) - Execute peer-to-peer transfers
- **Query Transfer** (`query_transfer`) - Query transfer records

### 9. Payment
- **Payment Request** (`payment_request`) - Create new payment requests
- **Get Payment Request** (`get_payment_request`) - Query payment request information
- **Cancel Payment Request** (`cancel_payment_request`) - Cancel payment requests
- **Payment Request Reminder** (`payment_request_reminder`) - Send payment reminders

### 10. Sell Order
- **New Sell Order** (`sellorder_new`) - Create new sell orders
- **Query Sell Order** (`sellorder_query`) - Query sell order information
- **Query by ID** (`sellorder_query_by_id`) - Query sell order by specific ID
- **Validate Field** (`validate-field`) - Validate order fields
- **Payout Outlets** (`payout-outlets`) - Get available payout outlets
- **Payout Outlet Categories** (`payout-outlet-categories`) - Get payout categories
- **Payout Outlet Fees** (`payout-outlet-fees`) - Get payout fees information

### 11. Wallet
- **Account** (`account`) - Get account information
- **Config Get All** (`config_getall`) - Get all wallet configurations
- **Deposit Address** (`deposit_address`) - Get deposit addresses
- **Deposit History** (`deposit_history`) - Query deposit history
- **Withdraw History** (`withdraw_history`) - Query withdrawal history
- **Withdraw Apply** (`withdraw_apply`) - Apply for withdrawals

### 12. Sub Account
- **Create** (`create`) - Create sub-accounts
- **Asset** (`asset`) - Get sub-account assets
- **List** (`list`) - List all sub-accounts
- **Universal Transfer** (`universal-transfer`) - Execute universal transfers
- **Universal Transfer History** (`universal-transfer-history`) - Query transfer history
- **Sub to Master** (`sub-to-master`) - Transfer from sub to master account
- **Sub History** (`sub-history`) - Query sub-account history
- **IP Restriction** (`ip-restriction`) - Get IP restrictions
- **Add IP Restriction** (`add-ip-restriction`) - Add IP restrictions
- **Delete IP Restriction** (`delete-ip-restriction`) - Delete IP restrictions

## 🚀 Quick Start

### 1. Import Collection
Download the `coins-api-postman.postman_collection.json` file and import it to your Postman workspace.

### 2. Environment Setup
Create a new environment in Postman and set the following variables:

#### Required Variables
- `host`: `https://api.pro.coins.ph`
- `apikey`: Your API key
- `secret`: Your API secret

#### Optional Variables (for specific modules)
- `merchant_apikey`: Required for Invoice API
- `merchant_secret`: Required for Invoice API
- `subApiKey`: Required for Sub Account API
- `subSecret`: Required for Sub Account API

### 3. Authentication
Most endpoints require HMAC-SHA256 signature authentication. The collection includes pre-request scripts that automatically:
- Generate timestamps
- Create query strings
- Calculate HMAC-SHA256 signatures
- Set authentication headers

## 📝 Usage Notes

### Signature Authentication
The collection automatically handles signature generation for authenticated endpoints using pre-request scripts that:
1. Extract request parameters
2. Generate timestamp
3. Create signature string
4. Calculate HMAC-SHA256 hash
5. Set required headers

### Rate Limiting
Please be aware of API rate limits and implement appropriate delays between requests when needed.

### Error Handling
Check response status codes and error messages for troubleshooting. Common issues include:
- Invalid signatures
- Expired timestamps
- Missing required parameters
- Insufficient permissions

## 🔧 Environment Variables Reference

| Variable | Description | Required For |
|----------|-------------|--------------|
| `host` | API base URL | All endpoints |
| `apikey` | Your API key | Authenticated endpoints |
| `secret` | Your API secret | Authenticated endpoints |
| `merchant_apikey` | Merchant API key | Invoice endpoints |
| `merchant_secret` | Merchant API secret | Invoice endpoints |
| `subApiKey` | Sub-account API key | Sub-account endpoints |
| `subSecret` | Sub-account API secret | Sub-account endpoints |

## 📚 API Documentation

For detailed API documentation, please refer to the official Coins API documentation.

## 🤝 Contributing

Feel free to submit issues and enhancement requests!

## 📄 License

This collection is provided as-is for educational and development purposes.
