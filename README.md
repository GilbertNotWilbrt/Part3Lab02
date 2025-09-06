Sorry I wasn't able to commit and push on my PC, I think I might've messed up the files.
So here is my README directly inputted into GitHub

Project: better-ticket-machine
Authors: David Barnes and Michael Kölling

This project is part of the material for the book

   Objects First with Java - A Practical Introduction using BlueJ
   Seventh edition
   David J. Barnes and Michael Kölling
   Pearson Education

It is discussed in chapter 2.

Purpose of project: To illustrate conditional statements.
How to start this project: Create one or more TicketMachine objects.

#47

Balance before insertMoney: 0
After: 300 or whatever you put in insertMoney

Whenever you insert a 0 in insertMoney it pops up the error message:
"Use a positive amount rather than: 0"

#48

When I put the 0, the error code no longer shows up.

#49

public void insertMoney(int amount) {
if (amount <= ) {
System.out.prinln(“Use a positive amount rather than: ” + amount);
}
else {
balance = balance + amount;
}

#50

This boolean field in the Circle controlled visibility (true for visible, false for invisible)
It was well suited since the visibility only has 2 states.

#51

The better printTicket, only prints a ticket if enough money is inserted.
It only adds the ticket price to total, and substracts it from balance.
The naive version doesn't do that.

#52

It is possible to go on without the else part, but it just wouldn't print
the block attached to else whenever you have less than the ticket costs in the machine.

#53

No, it cannot become negative when printing a ticket, as the printTicket method
only substracts the ticket price if current balance is >= the price.
This makes sure the remaining balance is always positive or zero.

#54

* for multiplication, / for division, % for module, ++ for incrementing, and -- or decrementing values.
 
#55 

int saving = price * discount;

#56

double mean = total / count

#57

public void affordable(int budget) {
    if(price > budget) {
        System.out.println("Too expensive);
    } else {
        System.out.println("Just right");
    }
}

#58

public void affordable(int budget) {
    if(price > budget) {
        System.out.println("Too expensive; your budget is " + budget + " cents");
    } else {
        System.out.println("Just right");
    }
}

#59

In the original code, it returns the current balance first, then resets it.
In the modified code, it returns the amount inserted then returns 0.

#60

It doesn't compile as nothing can appear after a return statement within the
same block.

#61

This version declares a local variable price instead of assigning value to field,
so the price field remains 0 while local variable disappear after constructor ends.

#62

public int emptyMachine() {
    int amountInMachine = total; 
    total = 0;                   
    return amountInMachine;      
}

#63

public void printTicket(){
    int amountLeftToPay = price - balance;
    
    if(amountLeftToPay <= 0) {
        System.out.print.ln("###############");
        System.out.print.ln(" The BlueJ Line");
        System.out.print.ln(" Ticket");
        System.out.print.ln("# " + price + " cents.");
        System.out.print.ln("###############");
        System.out.println();
        
        total = total + price;
        balance = balance - price;
        
    } else { 
        System.out.print.ln("You must insert at least " + amountLeftToPay + " more cents.");
    }
}
