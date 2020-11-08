# Payment Providers
Payment Providers are possible services to pay an order, for example Paypal or IOTA.

## IOTA 

### PaymentRequest
```json
- address: String
- amount: int
// for what they payment is
- comment: String  // -> another body?
- timestamp
- timeout: int
```