#include <iostream>
#include <string>

//Видалитии останню букву з рядка
void pop_back(std::string& str) {
    // Перевіряємо, чи рядок не пустий
    if (!str.empty()) {
        // Якщо рядок не пустий, видалити останній символ
        str.pop_back();
    }
}

// Перегрузка оператора += для додавання рядка до іншого рядка
std::string& operator+=(std::string& lhs, const std::string& rhs) {
    lhs.append(rhs); // Додати 'rhs' до кінця 'lhs'
    return lhs;      // Повернути посилання на ліву шнягу
}

int main() {
    std::string s = "Hello";
    pop_back(s); // Видалити останній символ з рядка
    std::cout << s << std::endl; // Виведе "Hell"

    std::string a = "Hello";
    std::string b = " World";
    a += b; // Додати 'b' до 'a'
    std::cout << a << std::endl; // Виведе "Hello World"

    return 0;
}
