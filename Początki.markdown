# Początki
2019-12-09

Zim
---
Po kilku latach przerwy wróciła do mnie myśl o dokumentowaniu życia w formie użytecznej dla postronnego czytelnika. Postanowiłem na początek napisać o rzeczach, które inaczej łatwo byłoby mi zapomnieć. I, oczywiście, musiałem zacząć od przygotowania sobie środowiska pracy. Przez jakiś czas marzyłem o systemie, w którym mógłbym bezpośrednio publikować swoje notatki. Napisać, wcisnąć guzik i w ten sposób coś opublikować albo poprawić. Używałem wielu różnych aplikacji do prowadzenia notatek, jedną z najlepszych był zawsze skromny, darmowy Zim. Odpowiednio skonfigurowany edytor nie przeszkadza w pisaniu, dzięki pluginom mogę np. zamienić go w minimalistyczny edytor ułatwiający skupienie, a przy zastosowaniu dowolnego narzędzia do synchronizacji danych mogę swobodnie przesiadać się między różnymi systemami bez ryzyka, że coś się wykrzaczy albo rozsypie. 

Przez lata mój windowsowy komputer obrósł masą niepotrzebnych danych, więc zacząłem od wybrania nowego systemu i nowego środowiska. Żadnych ikon na pulpicie, żadnego zbędnego oprogramowania, nic, co by mnie rozpraszało. Z założenia miał to być lekki system na pendrajwie, coś, co postawię raz i później przez parę lat będę mógł swobodnie korzystać, a w razie portzeby nie będzie problemu z rekonstrukcją. Jeden pendrajw miał działać na obu domowych kompach. Sprawdziłem wszystkie dystrybucje linuksowe pojawiające się w zestawieniach "top X Linux live" i bezproblemowy okazał się tylko Slax. Puppy Linux wyglądał obiecująco, ale miał problemy z obsłużeniem laptopowego wifi. Do obu tych dystrybucji z różnych powodów co jakiś czas wracam, w tym wypadku Slax zwyczajnie okazał się skuteczniejszy w wykrywaniu karty wifi w laptopie.

Linux
-----
Slax to bardzo mała dystrybucja, więc użytkowanie zacząłem od przygotowania sobie paczek z oprogramowaniem. Użyłem do tego skryptu apt2sb, który wygrzebałem na forum. Przygotowałem co następuje:

* Zim razem z rekomendowanym modułem do sprawdzania pisowni i polskim słownikiem aspell. Myślałem też o Publii i może spróbuję po przejściu na 64-bitową wersję systemu.
* MOC z rekomendowanymi bibliotekami ffmpeg, ponieważ w systemie nie znalazłem odtwarzacza muzyki.
* edytor tekstu geany, dość rozbudowany jak na podstawowe narzędzie, ale paczka wyszła całkiem niewielka
* ncftp
* przeglądarki Lynx (Dillo nie działa za dobrze, Chromium i Firefox w podczas używania szybko puchną, ale zainstalowałem również Firefoxa)
* alpine, klienta poczty działającego z wiersza poleceń
* rodzinę fontów Lato

Oraz, korzystając z instrukcji podanych na stronie slax.org:

* zmodyfikowane szablony do Zima
* tapetę - jedno z ulubionych zdjęć z Flickra.


Konfiguracja
------------
Następnie wyłączyłem komputer i usnąłem z pendrajwa plik changes.dat, kasując zapisane przez system dane, zostawiając tylko wytworzone przez siebie moduły z oprogramowaniem. Pierwszą rzeczą, którą zrobiłem po starcie od zera było ustawienie układu klawiatury na polski. I już mogłem zaczynać pisać. Wklepałem hasło do wifi, ustawiłem strefę czasową (``timedatectl set-timezone Europe/Warsaw``), włączyłem sprawdzanie pisowni w Zimie (ustawiłem też język na "``pl``") i skonfigurowałem tam co się dało. Jeszcze taki bajer: ``echo 'Mod4 e :Exec pcmanfm' >> ~/.fluxbox/keys`` żeby wygodnie porobić coś z plikami i dopisanie Hidden=true na końcu irytujących wpisów w /usr/share/applications. Skonfigurowałem klienta poczty alpine i przeglądarkę, zainstalowałem kilka dodatków. Zapisałem te zmiany jako moduł (poleceniem ``savechanges``).
 Jeżeli w międzyczasie nic się nie posypało, to chyba można pracować?

Domena i hosting
----------------
Przyszła pora na postawienie na nogi tzw. "mojej stronki".
Wybrałem hosting, na początek zdecydowałem się na InfinityFree, mogę tam bezproblemowo i za darmo publikować. Myślałem też o Git Pages i ostatecznie chyba tam się przesiądę. Hosting nie dodaje reklam na stronach, można korzystać z bezpłatnej domeny... Naprawdę niewiele potrzebowałem: żadnego PHP, żadnego Wordpressa, po prostu miejsce na notatki, na refleksje, spostrzeżenia i rozwiązania problemów. Jest to też miejsce, w którym bez problemu można własną stronę hostować na darmowej domenie.

Transfer plików
---------------
Wysyłam strony przy pomocy polecenia ``ncftpput -u UŻYTKOWNIK -p HASŁO -R ADRES.EFTEPA /htdocs /ścieżka/do/notesu/*``
Zastanawiam się nad użyciem w przyszłości narzędzia rsync (miałbym dzięki temu jedną paczkę mniej w systemie), ale posiadanie osobnego hasła do FTP wydaje mi się wystarczające, a obawiam się, że straciłbym dzień albo dwa na rozgryzaniu podstaw korzystania z ssh, jeżeli darmowy hosting w ogóle daje taką możliwość.






