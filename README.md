# pizzaboi
Plz review thx bb

#include <iostream>
#include <cmath>
using namespace std;

int main() {
   int numPeople = 0;       // Note: initial number of people
   int numPeople2 = 0;      // Note: people left after larges are ordered
   int numPeople3 = 0;      // Note: People left after mediums are ordered
   int largePizzas = 0;
   int mediumPizzas = 0;
   int smallPizzas = 0;
   int pricePaid = 0.0;
   double totalPizzaArea = 0.0;
   double pizzaPerGuest = 0.0;
   double subTotal = 0.0;   // Note: price before tip added
   double tip = 0.0;
   double totalPrice = 0.0;
   const double PI = 3.14159265;
   const double LARGE_RADIUS = 10.0;
   const double MEDIUM_RADIUS = 8.0;
   const double SMALL_RADIUS = 6.0;
   const double LARGE_PIZZA_PRICE = 14.68;
   const double MEDIUM_PIZZA_PRICE = 11.48;
   const double SMALL_PIZZA_PRICE = 7.28;
   
   cout << "Please enter the number of guests: ";
   cin  >> numPeople;
   cout << endl;
   
   largePizzas = numPeople / 7;
   
   numPeople2 = numPeople % 7;
   mediumPizzas = numPeople2 / 3;
   
   numPeople3 = numPeople2 % 3;
   smallPizzas = numPeople3;
   
   cout << largePizzas << " large pizzas, " << mediumPizzas << " medium pizzas, and " 
   << smallPizzas << " small pizzas will be needed." << endl;
   
   cout << endl;
   
   totalPizzaArea = ((PI * pow(LARGE_RADIUS,2)) * largePizzas) + ((PI * pow(MEDIUM_RADIUS,2)) * mediumPizzas) 
   + ((PI * pow(SMALL_RADIUS,2)) * smallPizzas);
   pizzaPerGuest = totalPizzaArea / numPeople;
   
   cout << "A total of " << totalPizzaArea << " square inches of pizza will be purchased (" 
   << pizzaPerGuest << " per guest)." << endl;
   
   cout << endl;
   
   cout << "Please enter the tip as a percentage (i.e. 10 means 10%): ";
   cin  >> tip;
   cout << endl;
   
   subTotal = (largePizzas * LARGE_PIZZA_PRICE) + (mediumPizzas * MEDIUM_PIZZA_PRICE) + (smallPizzas * SMALL_PIZZA_PRICE);
   totalPrice = subTotal * ((tip / 100) +1);
   pricePaid = round(totalPrice);
   
   cout << "The total cost of the event will be: $" << pricePaid << endl;
   
   return 0;
   
}
   
   
