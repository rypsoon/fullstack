# Wyjaśnienie plików projektu (1.3–1.5)

Poniżej znajduje się do skopiowania opis działania każdego pliku i każdej linii kodu w katalogu `(1.3-1.5)`.

## `src/App.jsx`
- **1**: Komponent funkcyjny `Header` zwraca nagłówek `<h1>` z nazwą kursu pobraną z prop `course`.
- **2**: Pusta linia dla czytelności.
- **3–7**: Komponent `Part` przyjmuje pojedynczy obiekt `part` i renderuje akapit z jego nazwą oraz liczbą ćwiczeń; linia 7 zamyka wyrażenie funkcyjne.
- **8**: Pusta linia oddzielająca definicje komponentów.
- **9–15**: Komponent `Content` odbiera tablicę `parts` i mapuje ją na listę komponentów `Part` wewnątrz kontenera `<div>`.
- **16**: Pusta linia.
- **17–19**: Komponent `Total` liczy łączną liczbę ćwiczeń metodą `reduce` i pokazuje wynik w akapicie.
- **20**: Pusta linia.
- **21–38**: Funkcja `App` definiuje obiekt `course` zawierający nazwę kursu oraz tablicę trzech części, z których każda ma nazwę i liczbę ćwiczeń.
- **39**: Pusta linia przed blokiem JSX.
- **40–46**: Zwracany JSX: kontener `<div>` renderuje `Header` (nazwa kursu), `Content` (lista części) oraz `Total` (suma ćwiczeń), po czym zamyka `return`.
- **47**: Zamyka definicję funkcji `App`.
- **48**: Pusta linia kończąca plik.
- **49**: Eksport domyślny udostępnia komponent `App` innym modułom.

## `src/main.jsx`
- **1**: Import `react-dom/client` dostarcza API do utworzenia korzenia renderowania w React 18.
- **2**: Importuje główny komponent `App` z lokalnego pliku.
- **3**: Importuje globalne style z `index.css`.
- **4**: Pusta linia dla czytelności.
- **5–7**: Tworzy korzeń React powiązany z elementem `#root` w HTML i renderuje w nim komponent `App`.

## `src/index.css`
- **1–7**: Ustawia styl bazowy `:root` – rodzinę czcionek, wysokość linii, grubość fontu, kolor tekstu i tła.
- **8**: Pusta linia.
- **9–12**: Styluje `body`, zerując margines i wymuszając minimalną wysokość 100% okna.
- **13**: Pusta linia.
- **14–16**: Dodaje padding 1.5 rem do wszystkich elementów `div`.
- **17**: Pusta linia.
- **18–20**: Usuwa górny margines nagłówków `h1`.

## `index.html`
- **1**: Deklaracja dokumentu HTML5.
- **2**: Otwiera element `<html>` z językiem angielskim.
- **3–7**: Sekcja `<head>`: kodowanie UTF-8, ustawienia viewportu i tytuł strony.
- **8–12**: Sekcja `<body>`: kontener `<div id="root">` dla aplikacji React oraz skrypt modułowy ładujący `src/main.jsx`.

## `package.json`
- **1**: Otwarcie obiektu JSON opisującego projekt.
- **2–5**: Metadane pakietu: nazwa, wersja, flaga `private` oraz typ modułu ES.
- **6–10**: Sekcja `scripts` definiuje polecenia `dev`, `build` i `preview` Vite.
- **11–14**: `dependencies` określa wymagane wersje `react` i `react-dom` w czasie działania.
- **15–18**: `devDependencies` zawierają narzędzia deweloperskie Vite i wtyczkę React.
- **19**: Zamyka obiekt JSON.

## `vite.config.js`
- **1**: Importuje funkcję `defineConfig` z Vite dla typowanej konfiguracji.
- **2**: Importuje wtyczkę React dla Vite.
- **3**: Pusta linia dla przejrzystości.
- **4–6**: Eksport domyślnej konfiguracji: Vite wczytuje wtyczkę `react()` zdefiniowaną w tablicy `plugins`.
