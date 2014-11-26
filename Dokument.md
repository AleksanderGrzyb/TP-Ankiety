# Podsumowanie prezentacji projektu “System ankiet mobilnych”
Jacek Jankowski i Aleksander Grzyb

## Cel  projektu
	
Celem projektu jest stworzenie aplikacji webowej oraz mobilnej, która umożliwi tworzenie  i wysyłanie anonimowych ankiet do docelowych odbiorców. Taki system pozwala w bardzo intuicyjny i prosty sposób przeprowadzenie ankiety oraz analizę opinii publicznej.

## Zasada działania systemu

Kroki niżej opisują proces przeprowadzenia ankiety w naszym systemie.

### Strony zleceniodawcy

1. Zleceniodawca ankiety rejestruje się w aplikacji webowej.
2. W tej aplikacji zleceniodawca tworzy ankietę poprzez specjalnie do tego przygotowane narzędzia. Narzędzia te umożliwiają tworzenie:
  * Pytań jednokrotnego lub wielokrotnego wyboru.
  * Pytań otwartych.
  * Pytań, w których odpowiedzi trzeba ustawić w pasującej kolejności.
  * Pytań, w których dane stwierdzenie ocenia się wartością numeryczną lub ilością gwiazdek.
3. Zleceniodawca wybiera grupę docelową ankiety (albo parę grup docelowych dla jednej ankiety) oraz termin wypełnienia ankiety.
4. Zleceniodawca ustala system premiowy (ilość punktów za wypełnienie ankiety) dla odbiorcy.
5. Zleceniodawca zleca ankietę. System automatycznie wysyła ankietę na telefony komórkowe grupy docelowej, którą wybrał zleceniodawca.
6. W trakcie trwania ankiety zleceniodawca po zalogowaniu się w aplikacji webowej ma możliwość analizowania wyników już wypełnionych ankiet. Wyniki przedstawione są poprzez wykresy, które w przejrzysty sposób prezentują najważniejsze informacje.
7. Po ukończeniu ankiety zleceniodawca po zalogowaniu się w aplikacji webowej ma możliwość zobaczenia szczegółowych wyników przeprowadzonej ankiety.

### Strona odbiorcy

1. Odbiorca instaluje aplikację mobilną.
2. Po zainstalowaniu aplikacji odbiorca wpisuje informacje o sobie (np. wiek, miejsce zamieszkania, czy płeć).
3. Odbiorca otrzymuje powiadomienie z aplikacji jeżeli jest dostępna ankieta do wypełnienia.
4. Za pomocą intuicyjnego interfejsu odbiorca w szybki i dokładny sposób wypełnia ankietę przeznaczoną dla niego.
5. Po prawidłowym wypełnieniu ankiety odbiorca dostaje punkty (ilość punktów za wypełnioną ankietę ustala zleceniodawca), które dodają się do jego konta.

## Plan biznesowy

Żeby zachęcić odbiorcę do dobrowolnego wypełniania ankiet, zleceniodawca ankiety ustala ilość punktów za wypełnienie ankiety. Docelowo zebrane punkty za wypełnienie ankiet odbiorca może zamienić na pieniądze, które będą wpłacane na jego konto (ta funkcja jest docelowa i nie będzie w naszej zaprezentowanej aplikacji). Pieniądze dla odbiorcy będą pochodziły od zleceniodawcy, który musi zapłacić za zlecenie ankiety. 

## Technologia

System składa się z dwóch podsystemów:

* Aplikacji mobilnej na platformę iOS.
* Aplikacji webowej dostępnej z poziomu przeglądarki.

Poniżej opiszę technologie jakie będziemy używać tworząc te dwie aplikacje.

### Aplikacja mobilna

Aplikacja mobilna będzie napisana w języku Objective-C w środowisku programistycznym Xcode. Do zaprogramowania interfejsu będą służyć frameworki, które znajdują się w iOS SDK, który jest specjalnie stworzony do programowania aplikacji mobilnych na system iOS. Oprócz iOS SDK aplikacja będzie korzystać z zewnętrznych frameworków, które ułatwią komunikację z serwerem oraz przyspieszą proces tworzenia interfejsu.

### Aplikacja webowa

Aplikacja webowa będzie napisana w języku Python wykorzystując framework Django. Wyniki ankiet będą przedstawione za pomocą bibliotek Pandas i Matplotlib.


