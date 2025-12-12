src/App.jsx
const Header = ({ course }) => <h1>{course.name}</h1> – deklaruje komponent funkcyjny Header, który odbiera prop course i zwraca nagłówek <h1> z nazwą kursu. 

Pusta linia dla czytelności. 
3–7. Definicja komponentu Part: przyjmuje prop part, a JSX w wierszach 4–6 tworzy akapit z nazwą oraz liczbą ćwiczeń z obiektu part; linia 7 zamyka wyrażenie funkcyjne. 

Pusta linia dla oddzielenia komponentów. 
9–15. Komponent Content: w linii 9 definiuje funkcję przyjmującą parts; linie 10–14 renderują kontener <div> z listą komponentów Part, tworzonych poprzez iterację map po tablicy parts; linia 15 kończy definicję. 

Pusta linia. 
17–19. Komponent Total: w wierszu 17 rozpoczyna funkcję przyjmującą parts; linia 18 renderuje akapit z sumą ćwiczeń obliczoną metodą reduce; linia 19 zamyka funkcję. 

Pusta linia. 

Rozpoczęcie głównego komponentu App. 
22–38. Definicja obiektu course: linia 22 inicjuje stałą; 23 ustawia nazwę kursu; 24 zaczyna tablicę parts; linie 25–37 definiują trzy obiekty części (nazwa i liczba ćwiczeń); 38 zamyka obiekt. 

Pusta linia. 
40–46. Blok return: linia 40 otwiera wyrażenie JSX, 41 tworzy kontener <div>, 42–44 renderują komponenty Header, Content i Total z odpowiednimi propami, 45 zamyka <div>, 46 kończy return. 

Zamyka funkcję App. 

Pusta linia. 

Eksport domyślny komponentu App, aby mógł być użyty w innych plikach. 

src/main.jsx
Importuje moduł react-dom/client, który dostarcza API do tworzenia korzenia renderowania w React 18. 

Importuje komponent App z pliku App.jsx. 

Importuje globalne style z index.css. 

Pusta linia dla czytelności. 
5–7. Tworzy korzeń React powiązany z elementem o id="root" w dokumencie i renderuje w nim komponent App; linia 7 zamyka wywołanie render. 

src/index.css
1–7. Definiuje style dla elementu :root: ustawienia rodziny czcionek, interlinii, grubości fontu, koloru tekstu i tła oraz zamknięcie deklaracji. 
8. Pusta linia. 
9–12. Style dla body: reset marginesu do 0 i minimalna wysokość 100% widoku; linia 12 zamyka blok. 
13. Pusta linia. 
14–16. Style dla wszystkich div: padding 1.5 rem; linia 16 zamyka blok. 
17. Pusta linia. 
18–20. Style dla nagłówków h1: usuwa górny margines (ustawia na 0); linia 20 zamyka blok. 

index.html
Deklaracja typu dokumentu HTML5. 

Otwiera element <html> z językiem angielskim. 
3–7. Sekcja <head>: linia 3 otwarcie; 4 ustawia kodowanie UTF-8; 5 metadane viewport; 6 tytuł strony; 7 zamknięcie nagłówka. 
8–12. Sekcja <body>: 8 otwarcie; 9 kontener <div id="root"> dla aplikacji React; 10 skrypt typu module ładujący src/main.jsx; 11 zamknięcie body; 12 zamknięcie html. 

package.json
Otwiera obiekt JSON opisujący projekt. 
2–6. Podstawowe metadane: nazwa pakietu, wersja, flaga prywatności (zapobiega publikacji), typ modułu ES. 
7–11. Skrypty npm: dev uruchamia Vite w trybie deweloperskim, build tworzy produkcyjny build, preview serwuje zbudowany projekt. 
12–15. Sekcja dependencies: wersje React i ReactDOM wymagane w runtime. 
16–18. devDependencies: narzędzia deweloperskie (wtyczka React dla Vite i sam Vite) wraz z wersjami semantycznymi. 

Zamyka obiekt JSON. 

vite.config.js
Importuje funkcję defineConfig z Vite, która ułatwia typowanie konfiguracji. 

Importuje wtyczkę React dla Vite. 

Pusta linia dla czytelności. 
4–6. Eksport domyślny konfiguracji Vite: linia 4 otwiera defineConfig, 5 przekazuje tablicę wtyczek zawierającą react(), 6 zamyka obiekt konfiguracji i moduł. 
