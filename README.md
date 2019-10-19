# Zadania

## Podstawy

3. Napisać funkcję `minmax(elements)` zwracającą jednocześnie minimum oraz maksimum wartości
    znajdujących się w `elements`.

4. Napisać funkcję `validate(pesel)`, która zwraca wartość logiczną `True`, jeżeli podany
    na wejście pesel posiada poprawną sumę kontrolną.
 
1. Napisać funkcję `cumulative_sum(numbers)`, przyjmującą jako argument ciąg liczb. 
Funkcja ta powinna zwracać listę sum częściowych, tzn. listę składającą się z następujących wartości:
   - `numbers[0]`
   - `numbers[0] + numbers[1]`
   - `numbers[0] + numbers[1] + numbers[2]`
   - ...
   - `numbers[0] + numbers[1] + ... + numbers[N-1]`
 
   gdzie `N` to rozmiar danych wejściowych. Dla przykładu `cumulative_sum([1, 2, 3, 4])` powinno
   zwrócić listę `[1, 3, 6, 10]`. Jaka jest złożoność obliczeniowa Twojego algorytmu?
   
5. Zaimplementować schemat [Hornera](https://pl.wikipedia.org/wiki/Schemat_Hornera).
 
4. Napisać funkcję `binary_search(sequence, x)` znajdującą indeks liczby `x` w
    podanym na wejściu ciągu `sequence`, przy założeniu, że ciąg ten jest wstępnie posortowany.
    W tym celu możemy wykorzystać tak zwane wyszukiwanie binarne. Idea jest prosta:
    - Zaczynamy od porównania szukanego elementu ze środkowym elementem tablicy.
      Jeśli są równe, to zwracamy bieżącą pozycję i kończymy pracę.
    - W przeciwnym razie środkowy element jest albo większy, albo mniejszy od szukanego.
      W pierwszym przypadku nasz element (o ile znajduje się wśród danych wejściowych)
      znajduje się w pierwszej połowie ciągu `sequence`. W drugim przypadku - w prawej.
    - Efektywnie zmniejszyliśmy więc o połowę zakres tablicy do przeszukania. Przedstawione
      wyżej rozumowanie możemy teraz zaaplikować to odpowiedniej połówki.
    - Powtarzamy aż do znalezienia elementu, albo do momentu w którym wyczerpiemy możliwości
      dalszego przeszukiwania.      
 
4. Napisać funkcję `merge(sequence1, sequence2)` scalającą dwa posortowane ciągi liczbowe.
    Przykładowo, `merge([-1, 0, 2], [-2, 1, 3])` powinno zwrócić listę `[-2, -1, 0, 1, 2, 3]`.
    
5. Napisać funkcję `find_peak(sequence)` zwracającą wierzchołek danej listy liczb. Wierzchołkiem
    nazywamy element listy, który jest większy od obydwu swoich sąsiadów (lub od jednego z nich,
    jeżeli jest to skrajny element). 
 
6. Napisać funkcję, która dla danej liczby całkowitej dodatniej `n` zwróci listę bitów w jej
    binarnym rozszerzeniu (zaczynając od najmłodszego bitu). Na przykład, dla liczby `13`
    wynikiem powinna być lista `[1, 0, 1, 1]`.

7. Napisać funkcję `fast_pow(base, exponent)` wyznaczający potęgę base<sup>exponent</sup> używając 
   potęgowania szybkiego.
   Zastanówmy się ile mnożeń wymaga obliczenie 2<sup>10</sup>? W naiwnej implementacji wykonalibyśmy
   ich 9. Możemy jednak zapisać nasze wyrażenie inaczej: 
   2<sup>10</sup> = 2<sup>2</sup> * 2<sup>8</sup>. Kolejne potęgi o wykładniku będącym potęgą
   dwójki możemy obliczyć z poprzednich potęg poprzez ich podniesienie do kwadratu.
   W tym prostym przykładzie musielibyśmy wykonać następujące operacje:
   1. Ustaw wynik na 1
   2. Oblicz 2<sup>2</sup> i przemnóż wynik przez otrzymaną liczbę.
   2. Oblicz 2<sup>4</sup> podnosząc do kwadratu 2<sup>2</sup>. Nie mnóż wyniku przez otrzymaną
      liczbę, ponieważ 2<sup>4</sup> nie występuje w przedstawionym wyżej rozkładzie.
   3. Oblicz 2<sup>8</sup> podnosząc do kwadratu 2<sup>4</sup>. Pomnóż wynik przez otrzymaną
      liczbę.
      
   W ogólności zaś, algorytm wygląda następująco:
   1. Ustaw wynik na 1
   2. Iteruj po kolejnych bitach (od najmłodszego) w rozwinięciu binarnym wykładnika.
      - Jeżeli dany bit jest równy 0, zastąp podstawę jej kwadratem.
      - Jeżeli dany bit jest równy 1, przemnóż wynik przez bieżącą wartość podstawy,
        a następnie zastąp podstawę jej kwadratem. 

3. Napisać funkcję `factorial` zwracającą silnię danej liczby. Przygotować zarówno rekurencyjną
   jak i iteracyjną implementację.
2. Napisać funkcję zwracającą n-ty wyraz ciągu Fibonacciego.
   Ciąg Fibonnacciego to ciąŋ zaczynający się od liczb 0 oraz 1, w którym każdy kolejny wyraz powstaje
   przez zsumowanie poprzednich dwóch wyrazów. Kilka początkowych wartości ciągu Fibonacciego:
   0, 1, 1, 2, 3, 5, 8, 13, 21, 34. Przygotować zarówno rekurencyjną jak i iteracyjną implementację.

3. Napisać generator produkujący kolejne wartości ciągu Fibonacciego.

4. Napisać funkcję `all_possible_strings(chars, length)` zwracającą listę wszystkich możliwych
   do ułożenia łańcuchów znaków o długości `length`, składających się ze znaków podanych jako
   wartość parametru `chars`. Na przykład `all_possible_strings(["a", "b"], 3)` powinno zwrócić
   listę zawierającą napisy `aaa`, `aab`, `aba`, `baa`, `bba`, `bab`, `abb`, `bbb`.
   
5. Przerobić funkcję z poprzedniego zadania na generator. 

4. Napisać funkcję `power_set(numbers)` zwracającą zbiór potęgowy danego zbioru liczb.
   Zbiór potęgowy danego zbioru to zbiór wszystkich podzbiorów tego zbioru. Na przykład,
   zbiór potęgowy zbioru `{1, 2, 3}` to zbiór {∅, {1}, {2}, {3}, {1, 2}, {2, 3}, {1, 3}, {1, 2, 3}}.

2. Napisać funkcję `gcd(a, b)` znajdującą największy wspólny dzielnik liczb `a` i `b`.
   Przygotować rekurencyjną oraz iteracyjną wersję.