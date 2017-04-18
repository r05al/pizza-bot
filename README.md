# pizza-bot
Order :pizza: From Slack

## Exercise 7: Submit an Order

* Ask users to confirm their order. You should include the address and the type of pizza they ordered.
* Users should accept or decline using message buttons.
* If the user accepts, place an order with Dominos, if they decline send them a farewell message.
* If you place an order, print the order ID.
* Run npm test and fix all problems that you find. 

## Resources

* [Botkit docs and source](https://github.com/howdyai/botkit)
* [Skellington docs and source](https://github.com/Skellington-Closet/skellington)
* [PizzaPI docs](http://riaevangelist.github.io/node-dominos-pizza-api/)
* [PizzaPI source](https://github.com/RIAEvangelist/node-dominos-pizza-api)
* [Slack Message Buttons](https://api.slack.com/docs/message-buttons)

## Concepts

### Ending Conversations

It turns out to end a conversation, you just don't need a next step and Botkit will let it end naturally. There's no special code to write; conversations will time out eventually.

## Helpful Hints

### Constructing an Order

You will need to create a `pizzapi.Order` object. This will require a `storeID`, a `deliveryMethod`, and a `customer` Object. The customer only needs to have an `address` field. You can't pass items in to the `Order` constructor, you'll need to add those separately. Finally you'll need to `place` the order.

### Don't worry! You won't really get a pizza!

The `Order` object requires payment information for `place` to succeed, so to really place an order you would need to ask users for their credit card information. If you were to build the credit card into this conversation this for yourself, you might think about pulling the whole conversation into a direct message (we used public conversations for simple collaboration). If you wanted to make this bot publicly available, you would have to worry about PCI compliance (a thing you have to get to handle other people's credit cards). But hey, if you just wanna do it for yourself go for it!

## Next Exercise

Holy smokes! We did it! We wrote a bot that will ask people what kind of pizza they want, where the want it from, and where they want it delivered! Give yourself a well deserved pat on the back :smile:

In the next exercise, we're going to talk about what you could do next! 

Next Exercise: https://github.com/SparkPost/pizza-bot/tree/08-next-steps

