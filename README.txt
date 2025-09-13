Отличия языков при работе со списком
Работа со списками на разных языках отличается наличием срезов (у python) и более простым синтаксисом. На c++ нет встроенных срезов, необходимо использовать циклы. У java также отсутствуют срезы, используются циклы и классы


Пример программы на python
# Работа со строкой
str_1 = "AaBbCcDd"
print("Только заглавные:", str_1[::2])
print("Только строчные:", str_1[1::2])

# Работа со списком
li = ['a', '1', 'b', '2', 'c', '3']
letters = li[0::2]
digits = li[1::2]

del li  # удаляем исходный список

print("Буквы:", letters)
print("Цифры:", digits)



Пример программы на c++
#include <iostream>
#include <vector>
#include <string>
using namespace std;

int main() {
    // Работа со строкой
    string str = "AaBbCcDd";
    string upper, lower;
    for (int i = 0; i < str.size(); i++) {
        if (i % 2 == 0) upper += str[i];
        else lower += str[i];
    }
    cout << "Только заглавные: " << upper << endl;
    cout << "Только строчные: " << lower << endl;

    // Работа со списком
    vector<string> li = {"a", "1", "b", "2", "c", "3"};
    vector<string> letters, digits;
    for (int i = 0; i < li.size(); i++) {
        if (i % 2 == 0) letters.push_back(li[i]);
        else digits.push_back(li[i]);
    }

    // вывод
    cout << "Буквы: ";
    for (auto &ch : letters) cout << ch << " ";
    cout << endl;

    cout << "Цифры: ";
    for (auto &ch : digits) cout << ch << " ";
    cout << endl;

    return 0;
}

Пример программы на java
public class Main {
    public static void main(String[] args) {
        // Работа со строкой
        String str = "AaBbCcDd";
        StringBuilder upper = new StringBuilder();
        StringBuilder lower = new StringBuilder();

        for (int i = 0; i < str.length(); i++) {
            if (i % 2 == 0) upper.append(str.charAt(i));
            else lower.append(str.charAt(i));
        }
        System.out.println("Только заглавные: " + upper);
        System.out.println("Только строчные: " + lower);

        // Работа со списком
        String[] li = {"a", "1", "b", "2", "c", "3"};
        StringBuilder letters = new StringBuilder();
        StringBuilder digits = new StringBuilder();

        for (int i = 0; i < li.length; i++) {
            if (i % 2 == 0) letters.append(li[i]).append(" ");
            else digits.append(li[i]).append(" ");
        }

        System.out.println("Буквы: " + letters);
        System.out.println("Цифры: " + digits);
    }
}



Отличия языков при работе со стеком
В отличие от Python и Java, в с++ нельзя напрямую посмотреть весь стек, только верхний элемент через top().

Пример программы на python
stack = []  # создаём пустой стек

stack.append(10)  # push
stack.append(20)
stack.append(30)

print("Стек:", stack)

top = stack.pop()  # pop
print("Сняли:", top)
print("Стек после pop:", stack)



Пример программы на java
import java.util.Stack;

public class Main {
    public static void main(String[] args) {
        Stack<Integer> stack = new Stack<>();

        stack.push(10);
        stack.push(20);
        stack.push(30);

        System.out.println("Стек: " + stack);

        int top = stack.pop();
        System.out.println("Сняли: " + top);
        System.out.println("Стек после pop: " + stack);
    }
}


Пример программы на c++
#include <iostream>
#include <stack>
using namespace std;

int main() {
    stack<int> st;

    st.push(10);
    st.push(20);
    st.push(30);

    cout << "Верхний элемент: " << st.top() << endl;

    st.pop();  // удалить верхний
    cout << "После pop верхний элемент: " << st.top() << endl;

    return 0;
}


