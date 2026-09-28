//practical-Assignments
#include<iostream>
using namespace std;
class student 
{
   int rollno,marks;
   string name;
   public : 
       student(int r, int m, string n)
       {
         rollno = r;
         marks = m;
         name = n;
       }
       student(student &s)
       {
         rollno = s.rollno; 
         marks = s.marks;
         name = s.name;
        }
        void display()
        {
           cout << " STUDENT DETAILS " <<endl;
           cout << " NAME : " << name <<endl;
           cout << " ROLL NO.: " << rollno <<endl;
           cout << " MARKS : " << marks <<endl;
        }
};
int main()
{
  student s1(1, 85, "krishna"); 
  student s2(s1);

  s2.display();
  return 0;
  }
