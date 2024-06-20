#include <iostream>
#include <string>

class Student {
private:
std::string name;
int age;
double averageGrade;
std::string group;
std::string city;

public:
Student(std::string n, int a, double ag, std::string g, std::string c)
: name(n), age(a), averageGrade(ag), group(g), city(c) {}
void setName(std::string n) {
    name = n;
}

std::string getName() {
    return name;
}

void setAge(int a) {
    age = a;
}

int getAge() {
    return age;
}

void setAverageGrade(double ag) {
    averageGrade = ag;
}

void setGroup(std::string g) {
    group = g;
}

std::string getGroup() {
    return group;
}

void setCity(std::string c) {
    city = c;
}

std::string getCity() {
    return city;
}

void printInfo() {
    std::cout << "Студент: " << name << std::endl;
    std::cout << "Возраст: " << age << std::endl;
    std::cout << "Средняя оценка: " << averageGrade << std::endl;
    std::cout << "Группа: " << group << std::endl;
    std::cout << "Город проживания: " << city << std::endl;
}

void evaluateGrade() {
    if (averageGrade > 8.0) {
        std::cout << "Отличник" << std::endl;
    } else if (averageGrade >= 6.0) {
        std::cout << "Хорошист" << std::endl;
    } else {
        std::cout << "Троечник" << std::endl;
    }
}
};

int main() {
Student s1("Виктория", 23, 8.5, "ОБП-32309МОгдри", "Омск");
Student s2("Эдуард", 21, 7.2, "ОБП-32309МОгдри", "Омск");
s1.printInfo();
s1.evaluateGrade();

s2.printInfo();
s2.evaluateGrade();

return 0;
}
