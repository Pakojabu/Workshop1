# Workshop1
Console program for making tasks
Dla nagłówka Please select an option: wybieramy kolor ConsoleColors.BLUE.

Opcje które mają być dostępne to:

add
remove
list
exit

Dla uproszczenia możemy je umieścić w tablicy typu String. 
Wywołaj metodę w metodzie main programu.
Metoda pobierająca dane z pliku
W metodzie main jako pierwszą wywołaj metodę, która z załączonego pliku tasks.csv wczyta dane do tablicy

static String[][] tasks;

Musisz skorzystać z odpowiedniej pętli do przetwarzania wierszy. Za pomocą metody split klasy String, możesz podzielić wiersz na poszczególne jego elementy.

Rozmiar tablicy musisz określić na podstawie ilości wierszy w pliku

Pobieranie wybranej akcji
Za pomocą klasy Scanner pobierz od użytkownika, jaka opcja programu ma zostać wywołana. W zależności od wybranej opcji wywołasz konkretną metodę. Możesz wykorzystać poniższy snippet:

switch (input) {
    case "add":
        addTask();
        break;
// other options
    default:
        System.out.println("Please select a correct option.");
}


Dodawanie zadania
Po wybraniu opcji add użytkownik zostanie odpytany o szczegóły zadania.



Następnie zadanie ma zostać dodane do tablicy tasks. Zwróć uwagę że konieczne będzie każdorazowe zwiększanie rozmiaru tablicy, możesz w tym celu skorzystać z metody:

Arrays.copyOf(tasks, tasks.length + 1);

Listowanie zadań
Po wybraniu opcji list wyświetl wszystkie zadania aktualnie znajdujące się w tablicy tasks.



Usuwanie zadania
Po wybraniu opcji remove odpytaj użytkownika o numer w tablicy, który należy usunąć.



Następnie usuń wskazany element z tablicy.

Możesz w tym celu wykorzystać metodę remove klasy ArrayUtils z załączonej biblioteki.

Usuwanie zadania — walidacja
Sprawdzaj poprawność wprowadzonej informacji:

czy jest to wartość liczbowa
czy jest większa równa 0
Sprawdzanie czy wartość nie jest większa niż rozmiar tablicy możesz przeprowadzić łapiąc odpowiedni wyjątek.



Jeżeli wartość nie jest poprawna, wyświetl komunikat i pobierz dane ponownie.

Zakończenie programu
Po wybraniu opcji exit dane z tablicy mają zostać zapisane do pliku tasks.csv zastępując całą dotychczasową zawartość znajdującą się w pliku. Zakończ działanie programu. Wyświetl komunikat w kolorze czerwonym.

