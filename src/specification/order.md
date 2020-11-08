# Order

```javascript=
    {
      // A Unique Identitfier of the shop as DID
      shopId: DataTypes.INTEGER,
      orderStatus: OrderStatuses,
      createdAt: DataTypes.DATE,
      offer: {
          // this can be a list of all kind of products or services.
      },
      payment: {
          // Currency symbol. For ex.: USD, EUR
          currency: String,
          total: Number,
          available_types: Array<PaymentTypes>
      }
    },
```


## OrderStatuses
  - Created
  - Accepted
  - Declined
  - Finished


## PaymentTypes
  - CreditCard
  - PayPal
  - Cash
  - CryptoCurrency


  ## Order Flow

  Alice sells something online. She creates a new Product in the ANNA applications and choose only IOTA as payment provider.

  1. just A product need to created

  2. This product is public reachable.

  3. Alice needs to distribute the product link.

  4. Bob clicked on the link and want to buy it.

  5. An offer will be created.

    - 1. prepares an offer object
    - 2. sign the offer object with bobs private key
    - 3. encrypt the offer object with alice public key
    - 4. Send the offer to alice

6. Alice fetches new offers and accepts bobs offer

7. Alice acceps the payment, through sending a payment request to bob.
