## Inleiding
<<<<<<< HEAD
Welkom bij de derde huiswerkopdracht die jullie gaan maken voor de Backend leerlijn. 
Je hebt als het goed is hoofdstuk 2.7 t/m hoofdstuk 2.9 gelezen op Edhub en je hebt de derde les van de java 
cursus gevolgd. In deze opdracht ga je oefenen met arrays, collecties en loops.
Deze week gaan we een nummer-vertaler maken.
=======
Welkom bij de derde huiswerkopdracht die jullie gaan maken voor de Backend leerlijn! Je hebt als het goed is hoofdstuk 2.7 t/m hoofdstuk 2.9 gelezen op EdHub en je hebt de derde les van de cursus Java gevolgd. In deze opdracht ga je oefenen met arrays, collecties en loops. Dit ga je doen door het maken van een nummer-vertaler.
>>>>>>> e6a9cf0837655585ab5bfd75f6bf661901b8e5b6

## Opzetten van een nieuw Java project

1. Open IntelliJ op je computer.

2. Kies rechts bovenin voor _New project_.

3. Op het volgende scherm zie je linksboven dat _Java_ blauw geselecteerd is. Daar klik je op _Next_.

4. Op het volgende scherm hoef je niks te selecteren en kun je gewoon op _Next_ klikken.

<<<<<<< HEAD
5. Op het volgende scherm kunnen we een naam meegeven aan het project. 
Kies altijd een beschrijvende naam die iets zegt over je project zodat je ook weet wat erin staat. 
Bijvoorbeeld "javaOpdracht1".
=======
5. Op het volgende scherm kun je een naam meegeven aan het project. Kies altijd een beschrijvende naam die iets zegt over je project zodat je ook weet wat erin staat. Bijvoorbeeld "javaOpdracht1".
>>>>>>> e6a9cf0837655585ab5bfd75f6bf661901b8e5b6

6. Klik daarna op 'Finish'. 


## Opdrachtbeschrijving

<<<<<<< HEAD
We gaan een applicatie bouwen die getallen vertaalt van numeriek (1, 2, 3, etc) naar alphabetisch (een, twee, drie, etc).
We gaan het vertalen door gebruik te maken van een HashMap. 
We zetten de numerieke getallen als key/sleutel en de alphabetische getallen als value/waarde in de HashMap.
Vervolgens vragen we de gebruiker om een input tussen 0 en 9 (inclusief) 
en gaan we dat "vertalen" door simpelweg de waarde uit de HashMap te vragen met de bijbehorende key 
=======
Je gaat een applicatie bouwen die getallen vertaalt van numeriek (1, 2, 3, etc.) naar alfabetisch (een, twee, drie, etc.).
Je gaat die getallen vertalen door gebruik te maken van een HashMap.
Je zet de numerieke getallen als sleutel (key) en de alfabetische getallen als waarde (value) in de HashMap.
Vervolgens vraag je de gebruiker om een input van 0 t/m 9 te geven en ga je dat "vertalen" door simpelweg de waarde uit de HashMap te vragen met de bijbehorende sleutel
>>>>>>> e6a9cf0837655585ab5bfd75f6bf661901b8e5b6
en dat terug te geven aan de gebruiker.


## Randvoorwaarden
<<<<<<< HEAD
- In je main methode staan twee arrays (1 numeriek en 1 alphabetisch), een boolean variabele, een Translator object 
en een Scanner object.
- Je maakt een Translator Class met daarin een HashMap variabele, een translate functie en 
een constructor met 2 arrays als parameter waarin je de HashMap variabele gaat programmatisch vullen.
- De logica van de applicatie wordt gedraaid in een while(boolean)-loop. Je toont de gebruikers eerst de keuze 
 `"Type 'x' om te stoppen \nType 'v' om te vertalen"`. 
  - Kiest de gebruiker verlaten, dan stop je de while-loop.
  - Kiest de gebruiker vertalen, dan vraag je de gebruiker om een nummer tussen 0 en 9 (inclusief)
  (controleer dit ook met een if-statement) in te typen. Vervolgens ga je dat vertalen en print je het uit.

## Stappenplan

1. Je maakt een Integer array genaamd `numeric` die je vult met de nummers 1,2,3,4,5,6,7,8,9,0. 
2. Je maakt een String array genaamd `alphabetic` die je vult met de de String varianten van de nummers uit stap 1, 
dus: "een", "twee", ... etc ..., "negen", "nul".
3. Maak een nieuwe `Class` aan en noem deze `Translator`.
4. Maak in de Translator Class een `Hashmap<Integer,String>` variable met de naam `numericAlpha`.
5. Maak in de Translator Class een Constructor die als parameters krijgt: `(String[] alphabetic, Integer[] numeric)`.
6. In de constructor ga je nu een for-loop schrijven die begint bij 0 en door gaat tot de lengte van de 
numeric/alphabetic array (maakt niet uit welke, ze zijn even lang).
7. In de body van de for-loop voeg je nu een nieuwe entry toe aan de hashmap met de correcte waardes uit `numeric` 
en `alphabetic`. Gebruik de `i` variable uit je for-loop om de correcte waardes uit de arrays te halen.
8. De constructor is klaar. Nu ga je deze aanroepen met de juiste argumenten in de main method van de Main class, 
oftewel, maak in main een nieuw object aan van het type Translator.
9. In de Translator class maak je nu een nieuwe methode genaamd `translate(Integer number)` die een String returned.
10. In de body van de translate method return je de waarde/value uit de numericAlpha hashmap die hoort bij de 
sleutel/key van `number`
11. In de main method van de Main class maken we nu een boolean variabele genaamd `play` met de waarde `true` 
en een nieuw Scanner object.
12. Vervolgens maken wij een while-loop die door gaat zolang `play` true is.
13. In de while-loop printen we `"Type 'x' om te stoppen \nType 'v' om te vertalen"` en maken we een String variable 
genaamd `input` waarin we de scanner.nextline() opslaan.
14. In de body van de while-loop maken we een if/else if/else statement. 
    1. __if__: Als de `input` "x" is, dan zet je `play` naar false. 
    2. __else if__: Als de `input` "v" is, dan print je als eerst "Type een cijfer in van 0 t/m 9", 
    vervolgens sla je het resultaat van scanner.nextint() op in een variabele `Integer number`, 
    3. schrijf een extra `scanner.nextLine()` (dat doet scanner.nextInt() namelijk niet) 
    en als laatste check je met een if-statement of 
       1. __if__: `number` kleiner is dan 10, dan sla je de waarde van `translator.translate(number)` op in 
       `String result` en print je `"De vertaling van " + number + " is " + result`.
       2. __else__: anders dan print je "ongeldige invoer"
    4. __else__: Als de `input` iets anders dan "x" of "v" is, dan print je "ongeldige invoer"
<!--- stap 2: eventuele uitbreiding?: sla de vertaal historie op in een arraylist. 
Als Bonus kun je ze laten bedenken hoe je dubbele resultaten in de historie voorkomt -->
=======
De opdracht moet voldoen aan de volgende voorwaarden:
- In je main methode staan twee arrays (1 numeriek en 1 alfabetisch), een boolean variabele, een Translator object en een Scanner object;
- Je project bevat 1 Translator class met daarin een HashMap variabele, een constructor met 2 arrays als parameter en een translate functie;
- De logica van de applicatie wordt gedraaid in een while(boolean)-loop in je main methode.

## Stappenplan
Let op: het is uitdagender om jouw eigen stappenplan te maken. Als je niet zo goed weet waar je moet beginnen, kun je onderstaand stappenplan gebruiken:
1. Maak in je `src`-map een Main class aan. Definieer in deze Main class een `public static void main (String[] args)` methode.
2. Maak in je main methode een Integer array genaamd `numeric` die je vult met de nummers 1,2,3,4,5,6,7,8,9,0.
3. Maak in je main methode een String array genaamd `alphabetic` die je vult met de String varianten van de nummers uit stap 1, dus: "een", "twee", ... etc ..., "negen", "nul".
4. Maak een nieuwe class aan en noem deze `Translator`.
5. Maak in de Translator class een `Hashmap<Integer,String>` variabele met de naam `numericAlpha`.
6. Maak in de Translator class een constructor die de volgende parameters krijgt: `(String[] alphabetic, Integer[] numeric)`.
7. Schrijf in de constructor een for-loop die begint bij 0 en doorgaat tot de lengte van de numeric/alphabetic array (maakt niet uit welke, ze zijn even lang).
8. Voeg in de body van de for-loop een nieuwe entry toe aan de HashMap met de correcte waardes uit `numeric` en `alphabetic`. Gebruik de `i` variabele uit je for-loop om de correcte waardes uit de arrays te halen.
9. De constructor is klaar. Nu ga je deze aanroepen met de juiste argumenten in de main methode van de Main class, oftewel: maak in main een nieuw object aan van het type Translator.
10. Maak in de Translator class een nieuwe methode genaamd `translate(Integer number)` die een String returnt.
11. In de body van de translate methode return je de waarde (value) uit de numericAlpha HashMap die hoort bij de sleutel (key) van `number`
12. Maak in de main methode van de Main class een boolean variabele genaamd `play` met de waarde `true`. Maak een String variabele genaamd `ongeldig` waarin je de String "ongeldige invoer" zet. Als laatst maak je nog een nieuw Scanner object aan met `Scanner scanner = new Scanner(System.in)`.
13. Vervolgens maak je een while-loop die doorgaat zolang `play` true is.
14. Print in de while-loop `"Type 'x' om te stoppen \nType 'v' om te vertalen"` en maak een String variabele genaamd `input` waarin je de waarde van `scanner.nextLine()` opslaat.
15. Maak in de body van de while-loop een if/else if/else statement.
    1. __if__: Als de `input` "x" is, dan zet je `play` naar false.
    2. __else if__: Als de `input` "v" is, dan print je eerst "Type een cijfer in van 0 t/m 9",
       vervolgens sla je het resultaat van `scanner.nextInt()` op in een variabele `int number`, voeg nog een `scanner.nextLine();` toe op de volgende regel (scanner.nextInt doet dit namelijk niet van zichzelf)
       en als laatste check je met een if-statement of
        1. __if__: `number` kleiner is dan 10, dan sla je de waarde van `translator.translate(number)` op in `String result` en print je
           `"De vertaling van " + number + " is " + result`.
        2. __else__: anders dan print je `ongeldig`
    3. __else__: Als de `input` dus iets anders dan "x" of "v" is, dan print je `ongeldig` 
 