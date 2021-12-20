- 👋 Hi, I’m @Hovo00
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
Hovo00/Hovo00 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
#include <iostream>

struct Student {
   const char* name;
   int group ;
   int* grades;
   Student(const char* Name, int Group, int* Grades):name(Name), group(Group), grades(Grades){
       std::cout<<"lox";
   }
};

int main()
{
    int n;
    std::cout<<"Write amoun of students \n";
    std::cin>>n;
    char Name[100];
    int Group;
    int Grades[9];
    Student** studptr = nullptr;
    for(int i = 0; i < n; ++i){
        std::cout<<"Stud"<<i<<"'s name ";
        std::cin>>Name;
        std::cout<<"Stud"<<i<<"'s group ";
        std::cin>>Group;
        
        std::cout<<"Stud"<<i<<"'s average points \n";
        for(int j = 0; j < 10; ++j){
            std::cin>>Grades[j];
        }
        

        studptr[i] = new Student(Name, Group, Grades);
    }
  
    
}
