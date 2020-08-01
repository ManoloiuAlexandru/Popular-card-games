A widely used way to run Python code is through an interactive session. To start a Python interactive session, just open a command-line or terminal and then type in python and the name of the script and then hit Enter.For you to run these programs you need to have Python 3.7  on your PC and you don't need to have any extra packages installed.

# Popular-games and Small projects
In this repository you can find implementation of popular games and small projects in Python.

----------------------------------------------------------------------------------------------------------------------------------------
  ## Cards-war:
  
  The objective of the game is to win all of the cards.The deck is divided evenly among the players, giving each a down stack. In unison, each player reveals the top card of their deck—this is a "battle"—and the player with the higher card takes both of the cards played and moves them to their stack. Aces are high, and suits are ignored. If the two cards played are of equal value, then there is a "war". Both players place the next card of their pile face down (some variants have three face down cards) and then another card face-up. The owner of the higher face-up card wins the war and adds all the cards on the table to the bottom of their deck. If the face-up cards are again equal then the battle repeats with another set of face-down/up cards. This repeats until one player's face-up card is higher than their opponent's. [Wikipedia](https://en.wikipedia.org/wiki/War_(card_game))
  
  *Implementation*</br>
  The implementation is in Python and it is using basic Object Oriented concepts. The class card is used to define an object that has the 2 attributes of a normal card:
  - number
  - card_type
  
  The class player has 4 attributes: 
  - name=name of the player
  - nr_card= gives the number of the card
  - cards= gives the card that the player has in his hands
  - war_hand= is a list that is used when war is happening.
  
  *Gameplay*</br>
The player can select if he wants to play or simulate a game. While he is playing informations of who and with what card the hand was won. In this game it does not matter who starts but who has the bigger card at the end of the hand, in this game there can't be a draw.

***Note: In the war game the deck is build so it can split the cards easy.***

----------------------------------------------------------------------------------------------------------------------------------------
  ## Sedma:
  
  Sedma is a Czech 4-card trick-and-draw game played by four players in fixed partnerships with a 32-card Bohemian-pattern pack. Card suits do not play a role in this game, and there is no ranking order. A trick is won by the last player to play a card of the same rank as the card led. [Wikipedia](https://en.wikipedia.org/wiki/Sedma)
  
  *Implementation*</br>
  The implementation is in Python. It is using the same OOP principles as the cards-war game. The class card is used to define an object that has the 2 attributes of a normal card: 
  - number
  - card_type 
  
  The class player has 4 attributes:
  - name= name of the player
  - nr_card= gives the number of the cards
  - cards= gives the card that the player has in his hands 
  - points= that increase with one everytime you get an A(15) or a 10. 
  
  While the game is going messages about what card you should play and who won the current hand and how many cards are left in the deck. Also the card class has overloaded the equal operator because you need to remove cards from hand and also keep a track of them. 
  
  *Gameplay*</br>
  The idea of the game is that player 1 starts with the card that appears most often in his hand. If the opposing player does not have a card with the same number the first player takes the cards and process repeats. Otherwise, if his opponent has the card with the same number then player 1 must give a card of the same number or let player 2 take the cards, in this way player 2 starting the next hand. When switching to the oppsoite player the variable "switched" changes it's value from 1 to 0 or from 0 to 1.

----------------------------------------------------------------------------------------------------------------------------------------
  ## Hangman:
  
  Hangman is a paper and pencil guessing game for two or more players. One player thinks of a word, phrase or sentence and the other(s) tries to guess it by suggesting letters, within a certain number of guesses. [Wikipedia](https://en.wikipedia.org/wiki/Hangman_(game))

  *Implementation*</br>
  The implementations are in Python and C++. They are using the OOP principles. The class hungman is used to define the word that the player has to guess. In order to get the word that the player has to guess the program uses the Python library "random" and takes a word from the list_of_words, which is a list. The C++ program is using the function [srand()](http://www.cplusplus.com/reference/cstdlib/srand/) to get the random word form the list. The hungman class has another static variabile and that is "full_word" which is used to see if the player has found the word or not, the initial value of this variable is 0, the chances to 1 when to player finds the word. 
  
  The second class is player which has 5 filds: 
  - the life, which means the number of tryes that the player has, if this value gets to 0 and the player dosen't guess the word until then the game is over
  - the name, which is used to get the name of the player,
  - the list_of_used_letters, which is used to store all the letters that the player has tryed until now, this is used so that the player will not lose lives if he uses more then once a letter. 
  - the good_letters, that is used when a letter that the player has introduce is in the word that he is looking for. 
  - the player_option, that is determined after a qestion and says if the player wants to know the first and the last letters or none of them.
  
  *Gameplay*</br>
  The games start after the player introduces his/her name and choices what type of game he/she wants: 1 if the player wants to see the first and the last letter of the word or 2 if the player dosen't want to see any of the letters, then presses a random letter on the keyboard. The game ends when the player is out of lifes or if he finds the word. 
  
  ***Note: The C++ file is similar to the Python one in variables,functions and methods.***
    
 ---------------------------------------------------------------------------------------------------------------------------------------
  ## BlackJack:
  
  Blackjack is the American variant of a globally popular banking game known as Twenty-One. It is a comparing card game between one or more players and a dealer, where each player in turn competes against the dealer. Players do not compete against each other. It is played with one or more decks of 52 cards, and is the most widely played casino banking game in the world. The objective of the game is to beat the dealer in one of the following ways:

  Get 21 points on the player's first two cards (called a "blackjack" or "natural"), without a dealer blackjack;
  Reach a final score higher than the dealer without exceeding 21; 
  or
  Let the dealer draw additional cards until their hand exceeds 21 ("busted").
  
   [Wikipedia](https://en.wikipedia.org/wiki/Blackjack)
  
  *Implementation*</br>
  The implementations are in Python and C++. It is using the same OOP principles as the cards-war game. The class card is used to define an object that has the 2 attributes of a normal card and a specific attribute: 
  - number
  - card_type 
  - hidden= this attribute is for the dealer part, BlackJack has a rule: the dealer will have 2 cards in the start as the player but only one is shown. 
  
  The class player has 4 attributes: 
  - name= name of the player
  - cards= gives the cards that the player has in his hands
  - hand_value= that increase with the number on the card
  - money= this is the money that the player has at the start. 
  
  ***Note: The C++ file is similar to the Python one in variables,functions and methods. C++ card class as == operator overloaded.***
  
  *Gameplay*</br>
  The game begins with the player geting 2 cards and the dealer get 2 cards. The player will see his cards and the dealer's unhidden card. Then the player will be asked to bet a number, if he bets a number bigger then he's money he will be asked to bet less money. 
  The game then is simple after the bet he will be asked if he wants to "stand" or if he wants to "hit". The "stand" option means that the if the dealer will have the hand_value<17 the dealer will draw cards until it gets over or equal to 17, then he's hand value will be calculated, with the player's class method "calculate_hand", then using the function "win_or_lose", which will check who won and return 1 if the player won, 2 if it is a draw or 0 if the dealer won. After we see who won the player will recive his bet * 2 back. If the player selects "hit" this will give him a new card. If with the new card he goes over 21 he lost, if the hand_value <21 he will have to choice again if he wants to "hit" or "stand", the game will end when he is out of money.
  
 ---------------------------------------------------------------------------------------------------------------------------------------
## Binary Tree Friends:
  
  In computer science, a binary tree is a tree data structure in which each node has at most two children, which are referred to as the left child and the right child. A recursive definition using just set theory notions is that a (non-empty) binary tree is a tuple (L, S, R), where L and R are binary trees or the empty set and S is a singleton set. Some authors allow the binary tree to be the empty set as well. [Wikipedia](https://en.wikipedia.org/wiki/Binary_tree)
  
  *Implementation*</br>
  The implementation is in Python and it is using Object Oriented concepts. The class BinaryTree is used to define an object that has the 3 attributes of a node in a Binary Tree:
    - right=node to the right
    - left=node to the left
    - data=data from the node
    
  *How it Works*</br>
  The methods add_to_left and add_to_right are use to add data to the left and to the right of node, that is passed as argument. The method get_person_that_talked traverse the tree on the right to check to who the node had talked to and returns a list that contains these nodes. The get_person_to_talk_to makes the same thing as the last method but this time is traversing the tree on the left side. The method talk calls the last 2 methods then pickes a random person from the left side and put it on the right side, this means that  the person has talked to that person so it won't be picked again. At the end the method return the new formed tree. 
  
  ***Note: the script is trying to follow the [Single responsibility principle](https://en.wikipedia.org/wiki/Single_responsibility_principle)***
    
----------------------------------------------------------------------------------------------------------------------------------------
  ## Xml_compare_field:
  
  Extensible Markup Language (XML) is a markup language that defines a set of rules for encoding documents in a format that is both human-readable and machine-readable. The World Wide Web Consortium's XML 1.0 Specification of 1998 and several other related specifications—all of them free open standards—define XML.[Wikipedia](https://en.wikipedia.org/wiki/XML)
  
  *Implementation*</br>
    The implementation is in Python and it is using Object Oriented concepts. The class CompareFile is used to define an object that has the 2 attributes:
    - file_for_compare=the file from where the data is taken for comparing
    - file_to_compare=the file to compare the data
  
  *How it Works*</br>
    The method create_dict_file_for_compare creates a dictionary, a python data structure, that contains all the data that we want to compare. The method create_dict_file_to_compare dose the same thing but for the other file. The method get_dict_of_specific_item_from_dict_file_for_compare tkae the specific field from the XML. The method compare_specific_field create a dictionary for the fields that we want to compare that has as keys the parameter "key_for_compare". Finaly the method find_and_compare_element takes as parameters:
     - item= the item that we want to compare
     - dict_of_elements= the dictionary that we use to compare the data
     - key_for_compare= when the dictionary is made the the values of the dictionary must be stored under a specific key that is uniqe for each field. That key is passed by you if there are more fileds that are uniqe.
     If one element has more fields then his corespondent then that element will be use to check if all the the field of the oter element are the same. It will be more efficent if it will be the other way around but then we will not know what fields are missing.
     
  ***Note:
    The work above is if you want to compare 2 XML files at work/school or just you need to compare the files. 
    The script is trying to follow the [Single responsibility principle](https://en.wikipedia.org/wiki/Single_responsibility_principle)***
