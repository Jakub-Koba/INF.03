# 1.1. Podstawowe informacje
---

[1] Każda ze stron dostępnych w internecie jest zwykłym dokumentem tekstowym, który można stworzyć przy użyciu dowolnego edytora tekstu.
[2] Teksty dostępne na stronie internetowej są otoczone znacznikami (tagami), czyli elementami języka ==HTML== (ang. `HyperText Markup Language`), za pomocą którego tworzy się strony WWW.

[3] Dokumenty HTML to pliki tekstowe, które zawierają proste polecenia dotyczące składu tekstu, a także dynamiczne odnośniki do innych dokumentów oraz obiekty postscriptowe, preformatowane i multimedialne (animacje, dźwięki, sekwencje wideo). Dokumenty te są przesyłane w sieci w postaci źródłowej - dopiero przeglądarka internetowa dostępna na komputerze użytkownika interpretuje kod strony, dzięki temu możliwe jest uniezależnienie się od systemu operacyjnego i komputera, na którym wyświetlana jest strona.

[4] Dokumenty HTML można przygotować, korzystając z dowolnego edytora tekstu. Edytory możemy podzielić następująco:
- Edytory tekstowe - umożliwiają bezpośrednią pracę z kodem HTML. Często są wyposażone w dodatkowe funkcje, np. automatyczne wstawiane znacznika zamykającego, sprawdzanie składni języka HTML, proste dodawanie atrybutów, łatwe tworzenie formularzy, tabel i ramek.
- Edytory graficzne - umożliwiają pracę w trybie WYSIWYG (ang. `What You See Is What You Get`). Pozwalają na tworzenie stron bez wpisywania kodu źródłowego.
#### 1.1.1. Podstawowe pojęcia
---
[5] ==Strona internetowa== - dokument utworzony w języku HTML lub XHTML, zapisany w pliku i umieszczony na serwerze, odczytywany na komputerze użytkownika za pomocą przeglądarki internetowej.

[6] ==Witryna internetowa== - zbiór stron internetowych powiązanych tematycznie i umieszczonych na jednym serwerze, stanowiący rodzaj serwisu informacyjnego.

[7] ==Portal internetowy== - serwis informacyjny zawierający informacje na różne tematy, zwykle wyposażony w dodatkowe funkcje, takie jak: poczta elektroniczna, katalogi stron internetowych, wyszukiwarki, czat, pobieranie plików.

[8] ==Wortal internetowy== - portal wertykalny (ang. `vertical portal`), czyli wyspecjalizowany, zawierający informację z jednej dziedziny, tematycznie ze sobą powiązane.

[9] ==Serwer internetowy== - określenia tego używa się w odniesieniu do komputera podłączonego do internetu i świadczącego różne usługi w internecie oraz w odniesieniu do oprogramowania uruchamianego na tym komputerze. Przykłady: serwery FTP, DNS, HTTP.

[10] ==Statyczna strona internetowa== - strony statyczne to takie, których zawartość i wygląd nie zmieniają się przy każdym odwołaniu do nich. Aby wprowadzić zmiany na stronie, programista musi zmienić jej kod.

[11] ==Dynamiczna strona internetowa== - strony dynamiczne są generowane na bieżąco przez serwer HTTP na podstawie zmiennych i parametrów przekazanych przez przeglądarkę internetową. Takie strony zmieniają zawartość i wygląd w zależności od interakcji z użytkownikiem.
Zmiany zawartości strony mogą odbywać się w dwojaki sposób. Można wprowadzić te zmiany po stronie użytkownika, na jego komputerze (ang. `client-side`), przy użyciu języków skryptowych takich jak JavaScript, dokonujących zmian bezpośrednio na obiektach.
Drugim sposobem jest kompilacja dynamicznej zawartości na serwerze (ang. `server-side`) z wykorzystaniem języków programowania takich jak PHP, ASP, Perl, Java, Python.
# 1.2. Języki HTML, XML, XHTML
---
#### 1.2.1. HTML (ang. `HyperText Markup Language`)
---
[12] Podstawowym elementem języka HTML jest znacznik. Znaczniki są poleceniami umieszczonymi w nawiasach ostrokątnych, np. `<body>`, `<head>`. Informują one przeglądarkę o wyglądzie otwieranej strony oraz o strukturze umieszczonego na niej tekstu.

> [!NOTE] **Important**
> [13] **Nazwy poleceń mogą być napisane małymi lub wielkimi literami, nie ma to znaczenia. Wyróżnia się znaczniki otwierające, np. `<p>`, i zamykające, np. `</p>`. Znacznik zamykający zawsze rozpoczyna się znakiem `/` i ma taką samą nazwę jak znacznik otwierający.**

[14] Pomiędzy tymi znacznikami może zostać umieszczony tekst, którego znaczniki dotyczą, np. wpisanie kodu: `<p> Formatowanie tekstu </p>` spowoduje umieszczenie tekstu zapisanego między znacznikami w nowym akapicie. Prawie wszystkie znaczniki otwierające trzeba zamknąć, stosując znaczniki zamykające. Wyjątki to, np.:
- `<br>` - znacznik łamania wierszy,
- `<hr>` - znacznik linii poziomej,
- `<img>` - znacznik wstawiania obrazka.

[15] Znaczniki, które formalnie nie posiadają oddzielnego elementu domykającego, możemy zapisać w  taki sposób, aby to domknięcie się pojawiło. Wymóg taki pojawił się w języku XHTML, ale zapis taki został również dopuszczony w HTML5. Dla wskazanych powyżej wyjątków może on mieć następującą postać:
- `<br />`
- `<hr />`
- `<img />`

[16] Znaczniki mają dodatkowe elementy, zwane atrybutami, która definiują ich działanie. Jeden znacznik może posiadać wiele atrybutów. Atrybuty mogą przyjmować różne wartości, nazywane ==parametrami==. Wartości atrybutu powinna zostać zapisana w `'apostrofach'` lub `"cudzysłowie"`.
`<nazwa_znacznika atrybut="wartość"> zawartość </nazwa_znacznika>`

[17] Serwery rozróżniają wielkość liter w nazwach plików. Jeżeli wartością parametru jest nazwa pliku, to wielkość liter może mieć znaczenie przy interpretacji zapisu znacznika, np.:
`<img src="Obrazek.jpg />"` to coś zupełnie innego niż `<img src="obrazek.jpg />`.
[P-1]`<p><a href="http://www.pxp.com"></a></p>`

[18] W dokumencie tworzonym w języku HTML powinna być wstawiona deklaracja typu dokumentu (ang. `Document Type Definition - DTD`). Określa ona, która wersja języka HTML jest stosowana na stronie.
[P-2] Deklaracja w HTML5:
`<!DOCTYPE html>`
Deklaracja w HTML 4.01:
`<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">`
#### 1.2.2. XML (ang. `Extensible Markup Language`)
---
[19] XML jest metajęzykiem opartym na zwykłym tekście, przeznaczonym do definiowania języków znakowania. Jest to coś więcej niż tekstowy format do opisywania dokumentów. XML daje dostęp do wielu technologii konstruowania, przetwarzania i przeszukiwania danych. Dostarcza mechanizmów opisywania struktury dokumentu za pomocą znaczników.
[20] XML jest powszechnie używany do opisu nowych formatów dokumentów na potrzeby internetu oraz do opisu danych posiadających wyraźną lub słabą wewnętrzną strukturę (arkuszy kalkulacyjnych, protokołów sieciowych, plików konfiguracyjnych).

> [!NOTE] **Important**
> [21] **Ze względu na to, że składnia XML jest oparta na zwykłym tekście, dokumenty XML mogą być czytane i edytowane przy użyciu najprostszych edytorów tekstu.**

[22] Język XML nie ma ustalonego słownika, dlatego można tworzyć słowniki przeznaczone dla określonych aplikacji lub branż. Opracowano już słowniki XML dla różnych gałęzi przemysłu i wielu zastosowań (np. dla dokumentów internetowych opracowano standard XHTML, a dla protokołów sieciowych - standard SOAP (ang. `Simple Object Access Protocol`) - protokół wywołania zdalnego dostępu do obiektów). Aplikacje wykorzystujące formaty XML są bardziej odporne na zmiany w strukturze danych niż aplikacje oparte na innych formatach.

[23] XML nie jest związanych z żadnym językiem programowania ani z żadnym systemem operacyjnym. Dzięki temu dokumenty można tworzyć i edytować, korzystając z różnych języków programowania, a XML może współpracować z różnymi systemami operacyjnymi.

###### ==Składnia== XML 1.0
[24] Specyfikacja XML 1.0 określa tekstowy format do opisu danych przy użyciu składni podobnej do składni języka HTML.
Dokument jest zbudowany z elementów, a każdy element składa się ze znacznika otwierającego (np. `<table>`), znacznika zamykającego (np. `</table>`) oraz z informacji znajdujących się pomiędzy tymi znacznikami. Elementy mogą być opatrywane atrybutami zawierającymi metadane opisujące element i jego zawartość.