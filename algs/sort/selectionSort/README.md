# Сортировка выбором

### 1)Описание алгоритма
Дана коллекция A = {a1, a2, a3, ... , an}, размера n. Необходимо упорядочить массив по возрастанию. Данный алгоритм берет ai элемент и сравнивает его со всеми элементами от i + 1 до n.

Данный алгоритм имеет сложность O(n^2).

### 2)Реализация на C++
```c++
void selectionSort(std::vector<int>& vect)
{
    int tmp;

    for(int i = 0; i < vect.size(); i++)
    {
        for(int j = i; j < vect.size(); j++)
        {
            if(vect[i] > vect[j])
            {
                tmp = vect[i];
                vect[i] = vect[j];
                vect[j] = tmp;
            }
        }
    }
}
```