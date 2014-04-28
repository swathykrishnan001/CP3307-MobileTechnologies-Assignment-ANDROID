Construct a mobile App that runs on the Android platform and the iOS platform. The target audience for the App 
is children aged 7-10 years old. Functionally, the App is a puzzle game designed to be educational and fun. The 
game-play is a form of “guess the secret number”. 
 
With respect to the target audience, the general requirements of the App are: 
x Choose an appropriate visual metaphor; 
x The visual layout must be consistent and coherent; and 
x Use appropriate music and sound effects during game-play and game configuration. 
 
During game-play, the App presents the child with a series of virtual cards, each having a set of numbers. The 
numbers appear to be randomly selected, however they are chosen based on the rules of “complete finite 
sequences of integers” as describe next. 
 
A finite sequence of positive integers C {c1,...,cn} is complete if it can be used to make another finite 
sequence of positive integers P {p1,..., pm} such that: 
 
where ai is 0 or 1 
 
 
Reference: Honsberger, R. Mathematical Gems III. Washington, DC: Math. Assoc. Amer., 1985. 
 
For example, the binary sequence C {1, 2, 4}is complete for the sequence of numbers P {0,..., 7}. We can 
see this in the following table for the values of ai
: 
 
 
 
 
 
 
 
 
 
 
 
 
For the purpose of your mobile App, you will place the P-numbers on particular cards by using the table. The 
number of cards equals the number of columns in the table. For each card, a P-number is selected if it has a 1 in 
the corresponding C-column. For example, this table would generate 3 cards: 
 
 
card1 {1,3,5,7}
card2 {2,3,6,7}
card3 {4,5,6,7} 
 
We will limit ourselves to three (3) kinds of complete sequences: 1) binary numbers, 2) Fibonacci numbers, and 
3) prime numbers. 
 
The App is expected to support cards generated using the static ranges of: 1 – 10, 1 – 20, 1 – 50, and a dynamic 
range where the minimum value is [1 – 20] and the maximum value is greater than the minimum up to 100. 
 
 
C 
1 2 4 
P 
0 0 0 0 
1 1 0 0 
2 0 1 0 
3 1 1 0 
4 0 0 1 
5 1 0 1 
6 0 1 1 
7 1 1 1 
pi ai
i 1
n
¦ ciSchool of Business CP3307:03 Mobile Technology Page 9
 
The mobile App is expected to support three (3) guessing game modes: 
x Child-guess: 
o The child guesses the App’s secret number 
o The child can only see each card once in a sequence 
o Each card shows a “Yes/No” comment from the App letting the child know if the App’s secret 
number is on the card or not 
o After all cards have been seen, the child has one chance to guess the number correctly 
o If the child guessed correctly, the score details are added to the high-scores 
x App-guess: 
o The App guesses the child’s secret number 
o The child can swipe between any of the cards in any sequence 
o Each card has a “Yes/No” button so the child can tell if the App’s secret number is on the card 
o After all “Yes/No” selections have been made by the child, the App guesses the number (the 
guess is randomly correct 80% of the time) 
o If the App won, its score is recorded into high-scores table 
x Free-play 
o No scoring 
o The child is allowed to swipe between any of the cards 
o “Yes/No” information is not provided 
 
The App must store the high-scores using an SQLite database – directly in Android and via Core Data in iOS. 
The records in the database must contain the player name and the associated score. When the child views the 
high-scores, the data must be displayed by decreasing score value. You are free to decide what is the best way 
(and when) to allow the App to input the player name as long as it is consistent and coherent with the App’s 
overall UI design metaphor. 
