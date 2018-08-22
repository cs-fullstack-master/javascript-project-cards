# javascript-project-cards

Use the variable below to give two players a static set of cards. Display the number each player gets and tell us who is the winner. Keep up with how many points each player gets after the five rounds.

Extra Credit: Create a reset button and randomly generate a new deck of cards each time. You can use the function below the card deck variable.

```javascript
const deck = [    { Value: 6, Suit: 'h' },
    { Value: 9, Suit: 'd' },
    { Value: 2, Suit: 'h' },
    { Value: 9, Suit: 'h' },
    { Value: 14, Suit: 'h' },
    { Value: 6, Suit: 'c' },
    { Value: 2, Suit: 'd' },
    { Value: 9, Suit: 's' },
    { Value: 12, Suit: 'h' },
    { Value: 10, Suit: 'c' },
    { Value: 14, Suit: 'c' },
    { Value: 7, Suit: 'd' },
    { Value: 3, Suit: 's' },
    { Value: 8, Suit: 'd' },
    { Value: 12, Suit: 's' },
    { Value: 7, Suit: 's' },
    { Value: 7, Suit: 'c' },
    { Value: 14, Suit: 'd' },
    { Value: 11, Suit: 'c' },
    { Value: 10, Suit: 's' },
    { Value: 11, Suit: 'd' },
    { Value: 4, Suit: 'd' },
    { Value: 2, Suit: 's' },
    { Value: 7, Suit: 'h' },
    { Value: 14, Suit: 's' },
    { Value: 10, Suit: 'h' },
    { Value: 5, Suit: 'c' },
    { Value: 12, Suit: 'c' },
    { Value: 6, Suit: 's' },
    { Value: 5, Suit: 's' },
    { Value: 12, Suit: 'd' },
    { Value: 4, Suit: 'h' },
    { Value: 11, Suit: 'h' },
    { Value: 13, Suit: 'c' },
    { Value: 5, Suit: 'h' },
    { Value: 6, Suit: 'd' },
    { Value: 13, Suit: 's' },
    { Value: 13, Suit: 'd' },
    { Value: 8, Suit: 'c' },
    { Value: 4, Suit: 's' },
    { Value: 13, Suit: 'h' },
    { Value: 2, Suit: 'c' },
    { Value: 8, Suit: 's' },
    { Value: 10, Suit: 'd' },
    { Value: 3, Suit: 'c' },
    { Value: 3, Suit: 'h' },
    { Value: 11, Suit: 's' },
    { Value: 8, Suit: 'h' },
    { Value: 9, Suit: 'c' },
    { Value: 5, Suit: 'd' },
    { Value: 3, Suit: 'd' },
    { Value: 4, Suit: 'c' } ];
    
var player1Deck = [];
var player2Deck = [];

player1Deck = deck.slice();
player2Deck = player1Deck.splice(1, 26);
```

Generate a new set of cards with the code below:
```javascript
var deck = new Array();
var suits = ["s", "d", "c", "h"];
var values = ["2", "3", "4", "5", "6", "7", "8", "9", "10", "11", "12", "13", "14"];

for(var i = 0; i < suits.length; i++)
{
    for(var x = 0; x < values.length; x++)
    {
        var card = {Value: values[x], Suit: suits[i]};
        deck.push(card);
    }
}

for (var i = 0; i < 1000; i++)
{
    var location1 = Math.floor((Math.random() * deck.length));
    var location2 = Math.floor((Math.random() * deck.length));
    var tmp = deck[location1];

    deck[location1] = deck[location2];
    deck[location2] = tmp;
}
```
