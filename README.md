# 7pz1_2
# Практична робота №1_2
**Виконав:** студент групи 4 СОМ Хованець Мар’яна (Варіант № 5)

## Завдання.
**Завдання:** Розробити консольну програму «Система обліку замовлень» для служби доставки або інтернет-магазину. Програма повинна зберігати номер замовлення, кількість елементів та вартість замовлення, демонструючи роботу зі звичайними змінними, вказівниками та функціями[cite: 3].

### 💻 Код програми:
```cpp
#include <iostream>

using namespace std;

void updateCost(int count, double* ptrCost) {
    if (count == 1) {
        *ptrCost = *ptrCost + 80;
    }
}

int main() {
    cout << "Система: Магазин одягу" << endl;

    int orderNumber = 526;
    cout << "Номер замовлення: " << orderNumber << endl;
    cout << "Адреса orderNumber: " << &orderNumber << endl;

    int* ptrOrder = &orderNumber;
    cout << "Адреса через вказівник: " << ptrOrder << endl;
    cout << "Значення через вказівник: " << *ptrOrder << endl;

    *ptrOrder = 150;
    cout << "Новий номер замовлення: " << orderNumber << endl;

    int quantity = 1;
    cout << "\nКількість елементів: " << quantity << endl;
    cout << "Адреса quantity: " << &quantity << endl;

    int* quantityPtr = &quantity;
    cout << "Адреса через quantityPtr: " << quantityPtr << endl;
    cout << "Значення через quantityPtr: " << *quantityPtr << endl;

    double orderCost = 3200.0;
    cout << "\nПочаткова вартість: " << orderCost << " грн" << endl;

    updateCost(quantity, &orderCost);
    cout << "Фінальна вартість (з урахуванням кількості): " << orderCost << " грн" << endl;

    return 0;
}


<img width="1276" height="609" alt="image" src="https://github.com/user-attachments/assets/af7f2adb-3913-4bf4-8b21-a5b7d6f187c8" />
