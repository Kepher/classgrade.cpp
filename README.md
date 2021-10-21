# classgrade.cpp
This a c plus plus program that uses a while loop to read grades from a user ad prints their average values.
/*A simple C++ code I wrote recently,File Name:classgrades.cpp
Author: Kepher Otieno.
Twitter:@KepherOtieno1
Date: 21-10-2021
Language: C++ programming language.
Purpose: To write a c++ program that uses while loop to read a sequence of grades (till -1 is entered ), 
and prints the average*/
#include <iostream>
using namespace std;

int main() {
  bool seenEndOfInput;
  int sum, numOfStudents;
  int curr;
  double average;
  std::cout << "------CLASS AVERAGE GRADES------\n";
  std::cout<<"Please enter the grades separated by space:"<<endl; // enter grades Of Students: 72 85 67 96 -1.
  
  std::cout<<"Please end the sequence by typing -1"<<endl; // -1 ends the sequence of grades.
  sum = 0;
  numOfStudents = 0;
  seenEndOfInput = false;
  while(seenEndOfInput == false){
    std::cin>>curr;
    if(curr == -1){
      seenEndOfInput = true;
    }
    else{
      sum += curr;
      numOfStudents++;
    }
  }
  average = (double)sum / (double)numOfStudents;
  std::cout<<"The class average is  "<<average<<endl;
  
return 0;
}
