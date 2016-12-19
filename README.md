# patronage_2017_QA

Odpowiedzi do zadania 1:
1.	Testy funkcjonalne od niefunkcjonalnych przede wszystkim różnią się tym że:
	a.	Testy funkcjonalne obejmują testowanie funkcjonalności w systemie lub działaniem użytkownika:
		i.	„funkcja mnożenia dwóch liczb – zwraca złe wartości”
		ii.	„Klikam przycisk ‘zapisz’ i program przestaje działać
	b.	Testy niefunkcjonalne obejmują wszystko co nie jest działaniem użytkownika lub funkcjonalnością, np.: 
		i.	Bezpieczeństwo
		ii.	Ergonomię
		iii.	Konwersję danych
		iv.	Testowanie instalacji
2.	
	a.	„Smoke testy” używane są jako typowe pierwsze testy, czy aplikacja zadziała. Czy do każdej funkcji – program ma dostęp. Jednakże ten test nie ma za zadania sprawdzić czy poszczególne funkcjonalności działają poprawnie – ma tylko sprawdzić czy coś się uruchomi. Czy program się zainstaluje itp.
		i.	Tak jak napisane wyżej, przed oddaniem kodu do testów, lub już po stronie testera jako pierwszy test.
	b.	„Test regresji” to testy, które mają za zadanie sprawdzić, czy kawałek naprawionego kodu nie wywołał błędu w innym miejscu, lub też wykrycia błędów, nie zostały odkryte podczas „naprawy”.
		i.	Ten rodzaj testów powstaje na przetestowanym już raz kodzie, by móc znaleźć problemy, które mogą wyniknąć podczas „naprawy”.
3.	Celem testowania jest poprawa jakości kodu. Zminimalizowanie lub całkowite wyeliminowanie błędów (a przynajmniej dążenie do tego – w praktyce całkowite uchronienie się od błędów jest niemożliwe) w programie. Testowanie jest niezbędne by wyeliminować niepożądane skutki zachowania użytkownika, jak również uchronić się przed ewentualnymi konsekwencjami błędów ludzkich.
4.	Wykonując Re-testy, czyli testy regresji. Oczywiście by był pewny – test musi przejść pozytywnie :)
5.	Jako wartości przychodzące z czujnika – podałbym własne argumenty „wchodzące” do funkcji. Sprawdziłbym wartości brzegowe, jak również wartości bliskie temu. Dla tego przykładu sprawdziłbym wartości:
	a.	-49
	b.	-50
	c.	-51
	d.	199
	e.	200
	f.	201
6.	Aby pokryć wszystkie możliwości potrzeba 9 testów:
	a.	a > 0, b = 3
	b.	a = 0, b = 3
	c.	a < 0, b = 3
	d.	a > 0, b < 3
	e.	a = 0, b < 3
	f.	a < 0, b < 3
	g.	a > 0, b > 3
	h.	a = 0, b > 3
	i.	a <0, b > 3
7.	17, 18, 60, 61
8.	 
	a.	Czy pole z hasłem ma być „gwiazdkowane” (<input type=password>) ?
	b.	Czy pole z loginem może zawierać cyfry, znaki specjalne, spację ?
	c.	Przykładowy login i hasło pozwalające na dostanie się do bazy
	d.	Czy Hasło ma specjalne „wymagania”, tj.: Duże/małe litery, cyfry, znaki specjalne
	e.	Na wszelki wypadek – czy posiadają kopię bazy
	f.	Czy Baza danych jest ‘online’ to znaczy działanie na żywym organizmie – aplikacji która aktywnie korzysta z tej bazy
9.	 
	a.	GET:
		i.	metoda pozwalająca  na przesyłanie wartości parametrów w sposób widoczny dla użytkownika. 
		ii.	Posiada ograniczoną długość wartości parametrów
		iii.	Może być trzymana w pamięci 
		iv.	Można odwołać się poprzez historię przeglądarki
		v.	Nie powinna być nigdy używana do przesyłania danych z formularza, jak również każdych innych danych, które muszę spełniać zakładane wymogi bezpieczeństwa
	b.	POST:
		i.	Nie jest trzymana w pamięci
		ii.	Nie jest trzymana w historii przeglądarki
		iii.	Nie posiada ograniczenia co do długości danych
		iv.	Dane idą „pod spodem” przez co nie można jawnie powiedzieć co zostało przesłane, bez odpowiednich metod (np.: echo ‘$value1’; w php) przez co jest trochę bardziej bezpieczna.
10.	Nie, jest protokołem bezstanowym, gdzie każde zapytanie to osobna transakcja nie mająca żadnych powiązań do poprzedniej.
11.	W SQL różnica jest następująca:
	a.	LEFT JOIN - Klucze A można powiązać (czyli dołączyć) z kluczami B, ale tylko z tymi, które posiada ją wspólne klucze z A, to znaczy:
		i.	A: klucze(1,2,3,4,5), B:klucze(3,4,5,6,7,8) => left join połączy je w sposób następujący: AB:klucze(1,2,3,4,5)
	b.	INNER JOIN – Zostaną wybrane tylko te klucze które występują w tabeli A i B:
		i.	A: klucze(1,2,3,4,5), B:klucze(3,4,5,6,7,8) => inner left join połączy je w sposób następujący: AB:klucze(3,4,5)
12.	/etc
13.	 
	a.	Kopiowanie elementu (zwykłe tak obok siebie kopia leży)
	b.	Kopiowanie elementu wraz z usuwaniem bazowego pliku (lub bezpieczniej – przeniesienie go do innego folderu)
	c.	Kopiowanie folderu i sprawdzenie, czy zawartość pozostała taka sama w obu folderach
	d.	Kopiowanie folderu wraz z usuwaniem bazowego folderu
	e.	Kopiowanie elementu połączonego dowiązaniem symbolicznym z innym plikiem
	f.	Kopiowanie elementu połączonego dowiązaniem symbolicznym z innym plikiem wraz z usunięciem bliku bazowego lub pliku z dowiązaniem
	g.	Kopiowanie pliku z dowiązaniem stałym
h.	Kopiowanie pliku z dowiązaniem stałym oraz usunięcie pliku bazowego