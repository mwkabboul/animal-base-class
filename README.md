# animal-base-class
#pragma once

#ifndef animal_h
#define animal_h

#include <iostream>
#include <string>
using namespace std;

class animal {

public:
	animal(char=20, int=20);
	~animal();
	void getaniamlname(){ return animalname; }

	void getanimalage() { return animalage; }

	virtual void print() {
		cout << "\nanimal print";
	};

private:

	int age(int);
	char name(int);
};


#endif
  #ifndef dog_h
  #define dog_h
  #include <iostream>
  using namepsace std;
  
class dog : public animal {

public:
	dog(char=20, int=20, int=15);
	~dog();
		;	virtual void print() {
		animal::print();
		cout << "\ndog print";
	}



private:
	int breed(char);
};
  #endif
  
  #ifndef cat_h
  #define cat_h
  #include <iostream>
  class cat : public animal {

public:
	cat(int=20, char=20, int=15, int=10);
	~cat();
	virtual void print() {
		animal::print();
		cout << "\ncat print";


private:
	int pawsize(int);
	int color(char);



	};
  #endif
  
  
#ifndef fish_h
  #define fish_h
  #include <iostream>
  usingnamespace std;
	class fish : public animal{
		fish(int = 20, char = 20, int = 10, int = 15);
		~fish();


	private:
		int gillcapacity(int);
		int swimspeed(int);
  };
  #endif
  
  animal.cpp
  
  #include "animal.h"
#include <iostream>
using namespace std;


animal::animal(char an, int aa) { //default constructor for animal
	cout << "\nanimal created";
	animalname = an;
	animalage = aa;
}

animal::~animal() {  //default destructor for animal
	cout << "animal destroyed";
}
virtual void printanimal(animal* animal) {
	animal->print();
  
  dog.cpp
  
  #include "dog.h"
#include <iostream>
using namespace std;


dog::dog(int aa, int an, int b) :animal(aa, an) {
	cout << "\ndog created";
	breed = b;
}

dog::~dog() {
	cout << "dog destroyed";

}
virtual void printanimal(dog* animal) {
	dog->print();
  
  
  cat.cpp
  #include "cat.h"
#include <iostream>
using namespace std;


cat::cat(int aa, int an, int c, int p) :animal(aa, an) {
	cout << "\ncat created";
	pawsize = p;
	color = c;
}

cat::~cat() {
	cout << "cat destroyed";
}

virtual void printanimal(cat* animal) {
	cat->print();
}
  
  fish.cpp
  #include "fish.h"
#include <iostream>
using namespace std;

fish::fish(int aa, int an, int gc, int ss) :animal(aa, an) {
	cout << "\nfish created";
	gillcapacity = gc;
	swimspeed = ss;
}

fish::~fish() {
	cout << "fish destroyed";
  
  
  
