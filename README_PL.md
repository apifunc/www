+ [Wersja angielska - EN](https://www.apifunc.com/)

# [APIfunc](https://www.apifunc.com)

![apifunc-logo.png](https://logo.apifunc.com/apifunc-logo.png)

https://github.com/apifunc

## Projekt APIfunc jest wspierany przez [API Foundation](https://apifoundation.com)

We started in 2018 with few concepts but one idea: fastest development.
Now, in 2020 we are giving solutions:

+ [APIexec - executor library for shell scripts](https://www.apiexec.com)
+ [APIcra - shell scripts libraries](https://www.apicra.com)
+ [APIunit - definition of application, CI, CD](https://www.apiunit.com)
+ [APIbuild - build process definition, focused on quality, versioning](https://www.apibuild.com)
+ [APIsql - bazy danych, zapytania, modele](https://www.apisql.com)
+ [APIfunc - rozwiązania dla FaaS](https://www.apifunc.com)



## Czym jest APIfunc?

Celem tego rozwiązania jest przygotowanie srodowiska do wykonania kodu jednej prostej funkcji dla dowolnego języka programowania z listy:
+ javascript/nodeJS
+ python
+ php
+ ...

## Kod

Funkcja powinna zawierać nazwe, parametry w formacie tekstowym, wynik jest przetwarzany do postaci JSON


## Usługa FaaS

Bazą jest usługa Serwera, obecnie może to być synchroniczna WSGI, asynchroniczne platformy Twisted i Tornado, lub po prostu NodeJS.

+ Serwer WSGI
+ Twisted, Tornado
+ NodeJS


## Serwer WSGI
Serwer WSGI pozwala uruchamiać kilka wątków jednocześnie, co umożliwia równoległe obsługiwanie zapytań, jednak nie można uruchamiać tysięcy wątków.  Gdy ich pula się wyczerpie to kolejne zapytanie zostanie wstrzymane, mimo że mikrousługa nie wykonuje żadnych operacji i czeka na odpowiedź innej usługi w tle.


## Twisted

W kodzie opartym na platformie Twisted wykorzystywane są funkcje zwrotne wstrzymujące i wznawiające pracę podczas przygotowywania odpowiedzi na zapytanie.  
Ten model skraca okresy bezczynności procesu, a aplikacja może obsługiwać tysiące zapytań.  
Nie oznacza to, że szybciej odpowiada na zapytania, a że jeden proces może odbierać więcej jednoczesnych zapytań i odpowiadać na nie w miarę otrzymywania niezbędnych danych.

