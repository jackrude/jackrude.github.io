---
layout: project
type: project
image: images/micromouse.jpg
title: Blackjack
permalink: 
date: 2015
labels:
  - Programming
  - Java
summary: My team developed a working Blackjack poker game using Java and its GUIS.
---

<div class="ui small rounded images">
  <img class="ui image" src="../images/blackjack.jpeg">
  
</div>
My team designed and implemented a working Blackjack game using nothing but Java.  This was a class project for ICS 111 fall 2015 taught by professor Jason Leigh.  This project took approximately two weeks to finish.  Here is the initial contract and assignments for this project.

  ifferent background image and music for each casino/planet.

casino 1 100 credit minbet = 5

casino 2 500 credit minbet = 25

casino 3 2000 credit minbet = 100

casino 4 5000 credit minbet = 250

Moon casino  10000 credit minbet = 500


pervasive:
	credits 
	mute button




menu screen:
start button
	save button 
	load button

bet screen:
	casino name
	casino balance
	bet
	bet +
	bet -
	confirm bet

Play screen:
	dealer hand
	player hand
	hit
	stand
Win/loss/draw screen:
	dealer hand value
	player hand value
	You Win/You Lose/Draw
	Continue button

classes
Card.java // for kexeping track of card objects suit and number
Deck.java //deck objects for keeping track of the deck
BlackJack.java // the actuall black jack game. BlackJack.play() is the main function in the class. this class will return the result in the form of the string once play is complete.
Driver.java // the menu and background for the game. Will handle the credits that the player has and the credits for all the casinos. 
Screen.java // have arraylists of EZelements these are the screens. will have show screen and hide screen. 

Version 1.0

menu screen with start.
working bet screen.
blackjack with basic code.

Jack
make/find buttons/sounds for:
 bet screen
 play screen

Brandon
in depth logic for the blackjack.java:
eg. evaluate the value of a hand, check to see if a player busted
add to string method to card.java

Bobby
code background logic for Driver.java:
 bet screen
 play screen
 player credits




Version 2

at least 2 casinos
win/loss/draw screen
playing the game fully working.
main menu working.
saving/loading value


Version 3
5 casinos




Shared code:

	private static int evaluateHand(ArrayList<Card> hand){
		int sum = 0;
		int aceCount=0;
		for(int i =0; i<hand.size(); i++){
			if(hand.get(i).number()==1){
				aceCount++;
				
			}
			else{
				if(hand.get(i).number()>10){
					sum+=10;
						
				}
				else{
					sum+=hand.get(i).number();
						
					}
				}
			}
			if(aceCount==0){
				return sum;
			}
			for(int i = aceCount; i>0 ;i--){
				int newSum = i*11+sum+(aceCount-i);
				if (newSum<=21){
					sum = newSum;
					break;
				}
			}
			return sum;
		}




