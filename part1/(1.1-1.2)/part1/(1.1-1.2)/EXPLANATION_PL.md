# Wyjaśnienie kodu w folderze `(1.1-1.2)`

Poniżej znajduje się szczegółowy, linijka po linijce opis działania plików znajdujących się w `src/` projektu.

## `src/App.jsx`

1. `const Header = ({ course }) => <h1>{course}</h1>`  
   - Definiuje komponent funkcyjny `Header`, który odbiera z propsów obiekt zawierający klucz `course`, a następnie renderuje go w nagłówku `<h1>`.
2. Pusta linia – dla czytelności.
3. `const Part = ({ part, exercises }) => (`  
   - Deklaruje komponent `Part`, który przyjmuje propsy `part` (nazwa części kursu) i `exercises` (liczba zadań).  
   - Otwiera nawias dla wieloliniowego JSX.
4. `  <p>` – otwiera paragraf HTML, do którego trafi treść w kolejnej linii.
5. `    {part} {exercises}` – wstawia nazwę części oraz liczbę zadań obok siebie dzięki interpolacji w JSX.
6. `  </p>` – zamyka paragraf.
7. `)` – kończy definicję JSX komponentu `Part`.
8. Pusta linia – dla czytelności.
9. `const Content = ({ part1, exercises1, part2, exercises2, part3, exercises3 }) => (`  
   - Tworzy komponent `Content`, który dostaje sześć propsów: nazwy trzech części kursu oraz odpowiadające im liczby zadań.  
   - Rozpoczyna blok JSX z nawiasem otwierającym.
10. `  <div>` – opakowanie na zawartość komponentu.
11. `    <Part part={part1} exercises={exercises1} />` – renderuje `Part` dla pierwszej części, przekazując odpowiednie propsy.
12. `    <Part part={part2} exercises={exercises2} />` – renderuje `Part` dla drugiej części.
13. `    <Part part={part3} exercises={exercises3} />` – renderuje `Part` dla trzeciej części.
14. `  </div>` – zamyka kontener `div`.
15. `)` – kończy deklarację komponentu `Content`.
16. Pusta linia – dla czytelności.
17. `const Total = ({ exercises1, exercises2, exercises3 }) => (`  
    - Definiuje komponent `Total`, który przyjmuje trzy liczby zadań i pokaże ich sumę.  
    - Otwiera blok JSX.
18. `  <p>Number of exercises {exercises1 + exercises2 + exercises3}</p>` – wyświetla paragraf z tekstem „Number of exercises” oraz sumą trzech wartości przekazanych w propsach.
19. `)` – kończy komponent `Total`.
20. Pusta linia – dla czytelności.
21. `const App = () => {` – główny komponent aplikacji, zainicjowany jako funkcja strzałkowa.
22. `  const course = 'Half stack application development'` – stała przechowująca nazwę kursu.
23. `  const part1 = 'Fundamentals of React'` – tytuł pierwszej części.
24. `  const exercises1 = 10` – liczba zadań w części pierwszej.
25. `  const part2 = 'Using props to pass data'` – tytuł drugiej części.
26. `  const exercises2 = 7` – liczba zadań w części drugiej.
27. `  const part3 = 'State of a component'` – tytuł trzeciej części.
28. `  const exercises3 = 14` – liczba zadań w części trzeciej.
29. Pusta linia – oddzielenie danych wejściowych od renderowania.
30. `  return (` – początek zwracanego JSX komponentu `App`.
31. `    <div>` – główny kontener dla całej strony.
32. `      <Header course={course} />` – renderuje nagłówek, przekazując nazwę kursu.
33. `      <Content` – rozpoczyna wywołanie komponentu `Content` (przechodzi w kolejne linie dla lepszej czytelności).
34. `        part1={part1}` – przekazuje nazwę pierwszej części.
35. `        exercises1={exercises1}` – przekazuje liczbę zadań dla pierwszej części.
36. `        part2={part2}` – przekazuje nazwę drugiej części.
37. `        exercises2={exercises2}` – przekazuje liczbę zadań dla drugiej części.
38. `        part3={part3}` – przekazuje nazwę trzeciej części.
39. `        exercises3={exercises3}` – przekazuje liczbę zadań dla trzeciej części.
40. `      />` – zamyka wywołanie komponentu `Content` (składnia self-closing w JSX).
41. `      <Total exercises1={exercises1} exercises2={exercises2} exercises3={exercises3} />` – renderuje komponent `Total`, aby pokazać łączną liczbę zadań.
42. `    </div>` – zamyka główny kontener.
43. `  )` – domyka wyrażenie `return`.
44. `}` – koniec definicji funkcji `App`.
45. Pusta linia – dla czytelności.
46. `export default App` – eksport domyślny, aby `App` można było importować w innych plikach.

## `src/main.jsx`

1. `import ReactDOM from 'react-dom/client'` – importuje funkcje ReactDOM do renderowania aplikacji w drzewie DOM.
2. `import App from './App'` – pobiera główny komponent `App` z bieżącego katalogu.
3. `import './index.css'` – dołącza globalne style CSS z pliku `index.css`.
4. Pusta linia – dla czytelności.
5. `ReactDOM.createRoot(document.getElementById('root')).render(` – tworzy korzeń React przypięty do elementu o id `root` w HTML i rozpoczyna renderowanie.
6. `  <App />` – renderuje komponent `App` jako zawartość węzła korzenia.
7. `)` – domyka metodę `render` i kończy wywołanie.

## `src/index.css`

1. `:root {` – selektor pseudo-elementu `:root` (globalny poziom dokumentu) otwiera blok stylów dla korzenia.
2. `  font-family: 'Inter', system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;` – ustawia stos czcionek domyślnych dla całej strony.
3. `  line-height: 1.5;` – ustawia wysokość linii na 1.5 dla lepszej czytelności tekstu.
4. `  font-weight: 400;` – definiuje standardową grubość czcionki.
5. `  color: #0f172a;` – ustawia domyślny kolor tekstu na ciemny granat.
6. `  background-color: #f8fafc;` – nadaje jasne tło całej stronie.
7. `}` – kończy blok stylów `:root`.
8. Pusta linia – dla czytelności.
9. `body {` – rozpoczyna regułę CSS dla elementu `<body>`.
10. `  margin: 0;` – usuwa domyślne marginesy przeglądarki.
11. `  min-height: 100vh;` – wymusza, by body miało co najmniej pełną wysokość okna.
12. `}` – zamyka regułę dla `body`.
13. Pusta linia – dla czytelności.
14. `div {` – otwiera regułę dla wszystkich elementów `<div>`.
15. `  padding: 1.5rem;` – dodaje wewnętrzny odstęp 1.5 rem do każdego `div`.
16. `}` – zamyka regułę `div`.
17. Pusta linia – dla czytelności.
18. `h1 {` – otwiera regułę dla nagłówków `<h1>`.
19. `  margin-top: 0;` – usuwa górny margines, by nagłówek był bliżej górnej krawędzi kontenera.
20. `}` – zamyka regułę `h1`.
