## Zapiski za pripravo na test iz Računalništva (Poklicna matura) | Computer Science Vocational Matura Exam Preparation Notes

**Datum:** 11. 3. 2025 **Številka dokumenta:** 6032-2/2025

---

### 1. Upravljanje s programirljivimi napravami (Managing Programmable Devices) 💻

**Jeziki (Languages):** C, C++, C#, Java, Python, PHP.

**Ključne vsebine (Key Concepts):**

- **Vhodi in Izhodi (Inputs and Outputs)**
    
    Python
    
    ```
    # Vhodi
    user_input = input("Vnesite število: ")  # Uporabnik vnese število
    print("Vnesli ste:", user_input)  # Izpis vnosa
    
    # Izhodi
    print("To je izhodni primer.")  # Izpis na zaslon
    ```
    
- **Spremenljivke (Variables):**
    
    - Deklaracija in inicializacija spremenljivk.
        
    - Delo z numeričnimi vrednostmi: cela števila (integers) in realna števila (floating-point numbers).
        
    
    <!-- end list -->
    
    Python
    
    ```
    # Deklaracija in inicializacija spremenljivk
    x = 10  # Celo število
    y = 3.14  # Realno število
    z = "Pozdravljen svet"  # Niz
    flag = False  # Logična vrednost
    
    # Primeri osnovnih podatkovnih tipov v Pythonu
    
    # int (celo število)
    celo_stevilo = 42
    print("Celo število:", celo_stevilo)
    
    # float (realno število)
    realno_stevilo = 3.14159
    print("Realno število:", realno_stevilo)
    
    # str (niz)
    niz = "Pozdravljen svet"
    print("Niz:", niz)
    
    # bool (logična vrednost)
    logicna_vrednost = True
    print("Logična vrednost:", logicna_vrednost)
    
    # list (seznam)
    seznam = [1, 2, 3, 4, 5]
    print("Seznam:", seznam)
    
    # tuple (nabor)
    nabor = (1, 2, 3)
    print("Nabor:", nabor)
    
    # dict (slovar)
    slovar = {"kljuc": "vrednost", "stevilo": 42}
    print("Slovar:", slovar)
    
    # set (množica)
    mnozica = {1, 2, 3}
    print("Množica:", mnozica)
    
    # NoneType (prazna vrednost)
    prazna_vrednost = None
    print("Prazna vrednost:", prazna_vrednost)
    
    # Delo z numeričnimi vrednostmi
    a = 7
    b = 2.5
    print("Seštevanje:", a + b)
    print("Množenje:", a * b)
    print("Deljenje:", a / b)
    print("Celoštevilsko deljenje:", a // b)
    
    # Primer lokalne in globalne spremenljivke
    globalna_spremenljivka = 50  # Globalna spremenljivka
    
    def uporabi_spremenljivke():
        lokalna_spremenljivka = 10  # Lokalna spremenljivka
        print("Lokalna spremenljivka:", lokalna_spremenljivka)
        print("Globalna spremenljivka znotraj funkcije:", globalna_spremenljivka)
    
    def spremeni_globalno():
        global globalna_spremenljivka  # Uporaba globalne spremenljivke
        globalna_spremenljivka += 10
        print("Spremenjena globalna spremenljivka:", globalna_spremenljivka)
    
    # Klic funkcij
    uporabi_spremenljivke()
    spremeni_globalno()
    print("Globalna spremenljivka zunaj funkcije:", globalna_spremenljivka)
    ```
    
- **Kontrolni stavki (Control Statements):**
    
    - **Pogojni stavki (Conditional Statements):** npr. `if`, `else if`, `else`, `switch`.
        
        Python
        
        ```
        # Pogojni stavki
        x = 10 # Potrebno je definirati x za primer
        if x > 5:
            print("x je večji od 5")
        else:
            print("x je manjši ali enak 5")
        ```
        
    - **Zanke (Loops):** npr. `for`, `while`, `do-while`.
        
        Python
        
        ```
        # Zanke
        # Potrebno je ponovno inicializirati x za while zanko, če je bila prej spremenjena
        x = 10
        for i in range(5):  # Zanka for
            print("Števec:", i)
        
        while x > 0:  # Zanka while
            print("x:", x)
            x -= 1
        ```
        
- **Podprogrami (Subprograms/Methods/Functions):**
    
    - **Definicija (Definition).**
        
    - **Prenos parametrov (Parameter Passing):**
        
        - Po vrednosti (by value).
            
        - Po referenci (by reference).
            
    - Prenos polja v podprogram (passing an array to a subprogram).
        
    - **Vračanje vrednosti (Returning Values).**
        
    
    <!-- end list -->
    
    Python
    
    ```
    # Podprogrami (metode, funkcije)
    # Definicija
    def pozdrav(ime):
        return f"Pozdravljen, {ime}!"
    
    # Prenos parametrov po vrednosti
    def povecaj_za_ena(stevilo):
        return stevilo + 1
    
    # Prenos parametrov po referenci (v Pythonu se objekti prenašajo s sklicem na objekt)
    # Če je objekt spremenljiv , se spremembe odrazijo izven funkcije.
    def spremeni_prvi_element(seznam_param): # Ime parametra spremenjeno, da se ne prekriva z globalnim 'seznam'
        if seznam_param: # Preverimo, če seznam ni prazen
             seznam_param[0] = 100
    
    # Prenos polja v podprogram
    def izpisi_seznam(seznam_param): # Ime parametra spremenjeno
        for element in seznam_param:
            print(element)
    
    # Vračanje vrednosti
    rezultat = povecaj_za_ena(10)
    print("Rezultat:", rezultat)
    
    # Primer klica funkcije spremeni_prvi_element
    moj_seznam_za_spreminjanje = [1, 2, 3]
    spremeni_prvi_element(moj_seznam_za_spreminjanje)
    print("Spremenjen seznam:", moj_seznam_za_spreminjanje)
    
    # Primer klica funkcije izpisi_seznam
    izpisi_seznam(moj_seznam_za_spreminjanje)
    ```
    
- **Polja (Arrays/Tables/Lists) in Nizi (Strings):**
    
    - **Polja:**
        
        - Enodimenzionalna in večdimenzionalna (one-dimensional and multi-dimensional).
            
        - Osnovne operacije nad polji: pridobivanje velikosti polja, vpis in izpis polja ali samo določenega elementa v polju, zamenjava vrednosti. <!-- end list -->
            
        
        Python
        
        ```
        # Polja (tabele, seznami)
        # Enodimenzionalna
        seznam_polje = [1, 2, 3, 4, 5] # Ime spremenljivke spremenjeno
        print("Velikost seznama:", len(seznam_polje))
        print("Prvi element:", seznam_polje[0])
        seznam_polje[0] = 10  # Zamenjava vrednosti
        print("Posodobljen seznam:", seznam_polje)
        
        # Večdimenzionalna
        matrika = [[1, 2], [3, 4]]
        print("Element matrike [1][1]:", matrika[1][1])
        ```
        
    - **Nizi:**
        
        - Osnovne operacije nad nizi: združevanje, velikost, zamenjava znaka v nizu, izpisovanje. <!-- end list -->
            
        
        Python
        
        ```
        # Nizi
        niz_primer = "Hello" # Ime spremenljivke spremenjeno
        print("Združevanje nizov:", niz_primer + " World")
        print("Velikost niza:", len(niz_primer))
        print("Zamenjava znaka:", niz_primer.replace("H", "J")) # Python nizi so nespremenljivi, replace vrne nov niz
        print("Izpisovanje niza:", niz_primer)
        ```
        

---

### 2. Načrtovanje in postavitev podatkovnih baz (Database Design and Implementation) 🗄️

Podatki so surovina, ki se pretaka skozi informacijski sistem (IS) in se v njem obdelujejo ter shranjujejo. Informacijski sistem je skupek ljudi, postopkov in naprav, zasnovan za obdelovanje podatkov oziroma informacij. Cilj IS je posredovati pravo informacijo na pravo mesto ob pravem času z minimalnimi stroški.

**Osnovni koncepti:**

- **Podatek vs. Informacija:**
    - Podatki so dejstva, predstavljena z vrednostmi (številke, znaki, simboli).
        
    - Informacija je skupek podatkov, ki tvori smiselno celoto.
        
    - Podatek ni informacija in podatki sami po sebi ne vsebujejo informacije. Šele ko podatke interpretiramo, lahko postanejo informacija.
        
    - PODATEK tvori INFORMACIJE, ki tvorijo ZNANJE.
        
- **Podatkovna baza (Database - PB):**
    - Množica urejenih podatkov, zapisana v računalniško informacijskem sistemu.
        
    - PB v širšem smislu sestavljajo: podatki, uporabniki in uporabniški programi, upravitelj podatkovne baze ter sistem za upravljanje podatkovne baze (SUPB).
        
    - **Arhitektura podatkovne baze (Database Architecture):** Trinivojska arhitektura je zasnovana z namenom ločevanja uporabniškega pogleda od fizične predstavitve podatkov.
        
        - **Zunanji nivo (External Level):** Uporabniški pogled na PB; opis dela PB, ki je pomemben za določenega uporabnika. Predstavljen je z entitetami, atributi in relacijami.
            
        - **Konceptualni nivo (Conceptual Level):** Skupen pogled na PB, ki vključuje vse entitete, relacije, atribute, omejitve, semantične informacije ter informacije o varnosti in integriteti.
            
        - **Notranji nivo (Internal Level):** Fizična predstavitev PB na računalniku; opisuje, kako so podatki shranjeni (dodelitev pomnilnika, opis zapisov, enkripcija, stiskanje).
            
    - **Podatkovna neodvisnost (Data Independence):** Spremembe na nižjem nivoju naj ne bi vplivale na višji nivo.
        
        - **Fizična podatkovna neodvisnost:** Spremembe v fizični hrambi (npr. spremenjene pristopne metode) ne vplivajo na logično predstavitev.
            
        - **Logična podatkovna neodvisnost:** Razširitev PB z novimi entitetami ne vpliva na uporabnike, ki teh sprememb vsebinsko ne potrebujejo.
            
- **Sistem za upravljanje podatkovnih baz (SUPB) (Database Management System - DBMS):**
    - Posrednik med podatkovno bazo in njenimi uporabniki.
        
    - Njegova naloga je upravljati PB v skladu s potrebami uporabnikov, omogočati dostop do podatkov ter izvajati zaščito in nadzor.
        

**Načrtovanje podatkovne baze (Database Design):**

Proces oblikovanja PB običajno poteka v treh fazah:

1. **Konceptualno oblikovanje (Conceptual Design):** Oblikuje se model, ki je neodvisen od logičnega in fizičnega oblikovanja, npr. E-R model.
    
2. **Logično oblikovanje (Logical Design):** Izbere se SUPB in preoblikuje konceptualni model v logični model (npr. relacijski, mrežni, hierarhični).
    
3. **Fizično oblikovanje (Physical Design):** Pripravi se opis implementacije PB v sekundarnem pomnilniku za izbrani SUPB.
    

**ER diagram (Entity-Relationship Diagram - ERD):**

- Uporablja se za izdelavo podatkovnega modela v fazi analize. Je semantični podatkovni model.
    
- **Prednosti:** Ni omejen z omejitvami komercialnih SUPB, ima enostavne koncepte in ga je lahko pretvoriti v relacijski ali druge klasične modele.
    
- **Slabosti:** Ni standardiziran glede pomena konceptov ali grafične predstavitve in ni uporaben v vseh fazah modeliranja.
    
- **Gradniki ER modela (ER Model Components):**
    - **Entiteta (Entity):** Nekaj, kar obstaja v realnem svetu ali v naših predstavah in je pomembno za obravnavani IS. Lahko je fizični objekt (npr. VOZILO, ŠTUDENT) ali pojem (npr. PODJETJE, SEMINAR). Imena tipov entitet so enolična in se pišejo v ednini. Tip entitete je predstavljen z imenom in seznamom atributov.
        
        - **Entitetna množica (Entity Set):** Množica vseh primerkov entitet, ki v določenem trenutku pripadajo tipu entitete. <!-- end list -->
            
        
        ```
        DRŽAVLJAN --> tip entitete
        --------------------
        ime | spol | poklic  --> atributi
        --------------------
        Janez|  m   | kuhar   |
        Andrej| m   | učitelj | } entitetna množica
        Ana  |  ž   | pravnica|
        --------------------
        (Primer po vzoru iz [cite: 24])
        ```
        
    - **Atribut (Attribute):** Lastnost entitete, ki opisuje ali določa njene značilnosti. Število atributov je poljubno.
        
        - **Vrste atributov:**
            - **Elementarni vs. Sestavljeni (Atomic vs. Composite):** Elementarni atributi niso deljivi, medtem ko so sestavljeni sestavljeni iz več manjših delov (npr. atribut `naslov` je lahko sestavljen iz `ulica`, `številka`, `pošta`, `država`).
                
            - **Enovrednostni vs. Večvrednostni (Single-valued vs. Multi-valued):** Enovrednostni atribut ima za posamezen primerek entitete eno samo vrednost (npr. `rojstni datum`). Večvrednostni atribut lahko ima več vrednosti (npr. `poklic`, če ima oseba več poklicev).
                
    - **Ključi (Keys):**
        - **Primarni ključ (Primary Key):** Atribut (ali skupina atributov), katerega vrednosti enolično identificirajo posamezne primerke entitet. Je obvezen in vedno en sam. Če ni naravnih kandidatov, se vpelje umetni atribut (kratek, numeričen). Označi se s podčrtavanjem ali znakom `#`.
            
        - **Sestavljeni (speti) ključ (Composite Key):** Primarni ključ, sestavljen iz več atributov. Npr. `priimek + ime + rojstni_datum + naslov`.
            
        - **Tuji ključ (Foreign Key):** Atribut v eni entiteti, ki predstavlja primarni ključ neke druge entitete. S tujimi ključi se realizirajo povezave med entitetami. V eni entiteti jih je lahko več.
            
    - **Povezava/Razmerje (Relationship):** Izraža pomensko povezavo med dvema (ali več) entitetama.
        
        - **Števnost/Kardinalnost (Cardinality):** Pove, koliko primerkov ene entitete nastopa v povezavi z enim primerkom druge entitete.
            
            - **1:1 (ena proti ena):** En primerek tipa entitete A sodeluje v povezavi z natanko enim primerkom tipa entitete B (npr. RAVNATELJ - VODI - ŠOLA, kjer šola ima enega ravnatelja in ravnatelj vodi eno šolo).
                
            - **1:N (ena proti mnogo):** En primerek tipa entitete A sodeluje v povezavi z enim ali več primerki tipa entitete B, vsak primerek tipa B pa je povezan z največ enim primerkom tipa A (npr. MATI - IMA - OTROK; mati ima lahko več otrok, otrok ima eno mater).
                
            - **N:M (mnogo proti mnogo):** En ali več primerkov tipa entitete A sodeluje v povezavi z enim ali več primerki tipa entitete B (npr. UČITELJ - UČI - DIJAK; učitelj uči več dijakov, dijaka uči več učiteljev).
                
        - **Obveznost (Optionality/Modality):** Določa, ali mora primerek entitete sodelovati v povezavi.
- **Grafična notacija (Graphical Notation) (primeri iz, podobno kot Crow's Foot):**
    
    - **Entiteta:** Pravokotnik.
    - **Povezava:** Črta med entitetama, včasih z rombom na sredini, ki opisuje povezavo.
    - **Števnost:**
        - `1:1`: `|---|` (črta z navpičnico na obeh koncih)
        - `1:N`: `|---<` (črta z navpičnico na "1" strani in vranjo nogo na "N" strani)
        - `N:M`: `>---<` (črta z vranjo nogo na obeh straneh)
    - **Obveznost:**
        - Obvezna: Navpična črta (`|`) na liniji povezave bližje entiteti.
        - Neobvezna (opcijska): Krogec (`o`) na liniji povezave bližje entiteti.

**SQL (Structured Query Language):** Standardni jezik za delo z relacijskimi podatkovnimi bazami.

- **Skupine SQL ukazov:**
    
    - **DDL (Data Definition Language - Jezik za definiranje podatkov):** Ukazi za ustvarjanje, spreminjanje in brisanje podatkovnih baz, tabel, pogledov, indeksov.
        
        - **`CREATE DATABASE ime_podatkovne_baze;`**: Ustvari novo podatkovno bazo.
            
            SQL
            
            ```
            CREATE DATABASE Testna_baza; /* [cite: 114] */
            ```
            
        - **`DROP DATABASE ime_podatkovne_baze;`**: Zbriše podatkovno bazo (vključno z vsemi tabelami in podatki).
            
            SQL
            
            ```
            DROP DATABASE Testna_baza; /* [cite: 115] */
            ```
            
        - **`CREATE TABLE ime_tabele (stolpec1 tip_podatkov omejitve, stolpec2 tip_podatkov omejitve, ...);`**: Ustvari novo tabelo. Vsakemu stolpcu je treba določiti podatkovni tip in morebitne omejitve.
            
            SQL
            
            ```
            CREATE TABLE R3e (
                idr3e INT(5) PRIMARY KEY,
                ime TEXT(55),
                priimek TEXT(66)
            ); /* [cite: 118] */
            
            CREATE TABLE razred (
                idrazred INT(13),
                ime VARCHAR, /* V MySQL je VARCHAR brez dolžine neveljaven, potrebna je dolžina npr. VARCHAR(255) */
                priimek VARCHAR,
                spol CHAR(1)
            ); /* [cite: 122] */
            ```
            
            - **Osnovni podatkovni tipi (primeri iz MySQL):** `VARCHAR`, `TEXT`, `CHAR`, `DATE`, `INT`, `DECIMAL`, `TIMESTAMP`.
                
        - **`CREATE TABLE novo_ime_tabele AS SELECT * FROM ime_tabele;`**: Ustvari novo tabelo in prekopira stolpce ter podatke iz obstoječe tabele (ne prekopira tujih ključev, povezav in indeksov).
            
            SQL
            
            ```
            CREATE TABLE R1ta_1 AS SELECT * FROM R1ta; /* [cite: 121] */
            ```
            
        - **`ALTER TABLE ime_tabele ...;`**: Spreminja strukturo tabele (dodajanje, brisanje, spreminjanje stolpcev ali omejitev).
            
            - **Dodajanje stolpca:** `ADD ime_stolpca tip_podatkov(dolzina) [omejitve] [FIRST | AFTER obstojeci_stolpec];`
                
                SQL
                
                ```
                ALTER TABLE avtomobilizem ADD lastnik VARCHAR(255); /* Prilagojeno iz [cite: 188] */
                ```
                
            - **Spreminjanje imena stolpca:** `CHANGE staro_ime novo_ime tip_podatkov(dolzina) [omejitve];`
                
                SQL
                
                ```
                ALTER TABLE avtomobilizem CHANGE lastnik owner VARCHAR(255); /* Prilagojeno iz [cite: 189] */
                ```
                
            - **Spreminjanje tipa podatkov stolpca:** `MODIFY ime_stolpca novi_tip_podatkov(dolzina) [omejitve];` ali `CHANGE ime_stolpca ime_stolpca novi_tip_podatkov(dolzina) [omejitve];`
                
                SQL
                
                ```
                ALTER TABLE avtomobilizem MODIFY moc VARCHAR(55); /* [cite: 191] */
                ```
                
            - **Brisanje stolpca:** `DROP ime_stolpca;`
                
                SQL
                
                ```
                ALTER TABLE avtomobilizem DROP cena; /* [cite: 190] */
                ```
                
        - **`DROP TABLE ime_tabele;`**: Zbriše tabelo.
        - **`TRUNCATE TABLE ime_tabele;`**: Zbriše vse podatke iz tabele, vendar ohrani strukturo tabele. Ponastavi števec `AUTO_INCREMENT`.
            
        - **Prikaz tabel/baz:**
            - `SHOW TABLES;`: Prikaže vse tabele v trenutno izbrani podatkovni bazi.
                
            - `SHOW DATABASES;`: Prikaže vse podatkovne baze.
                
            - `USE ime_podatkovne_baze;`: Izbere podatkovno bazo za delo.
                
    - **Omejitve (Constraints):** Pravila, ki veljajo za podatke v tabelah.
        - **Dolžina zapisa:** Določena v oklepaju za podatkovnim tipom, npr. `VARCHAR(50)`.
            
            SQL
            
            ```
            CREATE TABLE razred(idrazred INT(44), ime TEXT(55), priimek TEXT); /* [cite: 128] */
            ```
            
        - **`NOT NULL`**: Stolpec ne sme vsebovati praznih (NULL) vrednosti.
            
            SQL
            
            ```
            CREATE TABLE razred(idrazred INT(44) NOT NULL, ime TEXT(55) NOT NULL, priimek TEXT); /* [cite: 137] */
            ```
            
        - **`UNIQUE`**: Vse vrednosti v stolpcu morajo biti unikatne. Uporabno za EMŠO, davčne številke ipd..
            
            SQL
            
            ```
            CREATE TABLE razred(idrazred INT(44) UNIQUE, ime TEXT(55), priimek TEXT); /* [cite: 143] */
            ```
            
        - **`PRIMARY KEY` (Primarni ključ):** Enolično identificira vsako vrstico v tabeli. Je kombinacija `NOT NULL` in `UNIQUE`.
            
            SQL
            
            ```
            CREATE TABLE razred(idrazred INT(44) PRIMARY KEY, ime TEXT(55), priimek TEXT); /* [cite: 152] */
            ```
            
        - **`FOREIGN KEY` (Tuji ključ):** Povezuje vrstico v eni tabeli z vrstico v drugi tabeli. Nanaša se na `PRIMARY KEY` v drugi tabeli.
            
            SQL
            
            ```
            CREATE TABLE razred(
                idrazred INT(44) PRIMARY KEY,
                idsola INT,
                FOREIGN KEY (idsola) REFERENCES sola(idsola)
            ); /* [cite: 158] */
            ```
            
        - **`CHECK`**: Zagotavlja, da vrednost v stolpcu ustreza določenemu pogoju (sintaksa se lahko razlikuje med SQL sistemi, npr. MS SQL in MySQL). V MySQL `CHECK` omejitev je parsirana, a ne vedno uveljavljena pred MySQL 8.0.16.
            
            SQL
            
            ```
            /* MS SQL & MySQL (z opozorilom za starejše verzije) */
            CREATE TABLE Persons (ID INT NOT NULL, LastName VARCHAR(255) NOT NULL, Age INT CHECK (Age>=18)); /* [cite: 160, 161] */
            ```
            
        - **`DEFAULT`**: Določi privzeto vrednost za stolpec, če vrednost ni podana ob vnosu.
            
            SQL
            
            ```
            CREATE TABLE Persons (City VARCHAR(255) DEFAULT 'Ljubljana'); /* [cite: 162] */
            ```
            
        - **`AUTO_INCREMENT` (MySQL specifično):** Samodejno povečuje numerično vrednost za polje, ki je običajno primarni ključ.
            
            SQL
            
            ```
            CREATE TABLE razred(idrazred INT(44) PRIMARY KEY AUTO_INCREMENT, ime TEXT(55)); /* [cite: 148] */
            ```
            
        - **`ENUM` (MySQL specifično):** Določa, da lahko stolpec vsebuje samo eno vrednost iz seznama predhodno določenih vrednosti.
            
            SQL
            
            ```
            CREATE TABLE Razred (spol ENUM('moški','ženska')); /* [cite: 166] */
            ```
            
        - **`CHARSET` (MySQL specifično):** Določa nabor znakov za tabelo ali stolpec. `DEFAULT CHARSET` določa privzeti nabor znakov za tabelo.
            
            SQL
            
            ```
            CREATE TABLE avtomobilizem ( /* ... definicije stolpcev ... */ ) DEFAULT CHARSET='utf8'; /* [cite: 176] */
            ```
            
    - **DML (Data Manipulation Language - Jezik za manipulacijo s podatki):** Ukazi za poizvedovanje, vstavljanje, spreminjanje in brisanje podatkov v tabelah.
        
        - **`INSERT INTO ime_tabele (stolpec1, stolpec2, ...) VALUES (vrednost1, vrednost2, ...);`**: Vstavi nove vrstice (podatke) v tabelo.
            
            SQL
            
            ```
            INSERT INTO ime_tabele (stolpec1, stolpec2, stolpec3)
            VALUES ('vrednost1', 'vrednost2', 'vrednost3'),
                   ('vrednostA', 'vrednostB', 'vrednostC'); /* [cite: 195] */
            ```
            
        - **`UPDATE ime_tabele SET stolpec1 = nova_vrednost1, stolpec2 = nova_vrednost2, ... WHERE pogoj;`**: Posodobi obstoječe podatke v tabeli. Če `WHERE` pogoj ni podan, se posodobijo vse vrstice!. Za brisanje vrednosti (nastavitev na prazno) se uporabi `NULL`.
            
            SQL
            
            ```
            UPDATE razred SET ime='Janez', priimek='Novak' WHERE idrazred='4'; /* [cite: 199] */
            UPDATE razred SET ime=NULL WHERE idrazred='4'; /* [cite: 202] */
            ```
            
        - **`DELETE FROM ime_tabele WHERE pogoj;`**: Zbriše vrstice iz tabele. Če `WHERE` pogoj ni podan, se zbrišejo vse vrstice!.
            
            SQL
            
            ```
            DELETE FROM razred WHERE idrazred='4'; /* [cite: 205] */
            ```
            
        - **`SELECT stolpec1, stolpec2, ... FROM ime_tabele WHERE pogoj LIMIT stevilo_vrstic;`**: Izbere (pridobi) podatke iz ene ali več tabel.
            
            - `SELECT * FROM ime_tabele;`: Izbere vse stolpce in vse podatke iz tabele. Previdno pri velikih tabelah, uporabi `LIMIT`.
                
            - **`AS` (Alias):** Preimenuje stolpec ali tabelo samo za namen izpisa.
                
                SQL
                
                ```
                SELECT ime_stolpca AS novo_ime_stolpca FROM ime_tabele; /* [cite: 216] */
                SELECT ime_stolpca FROM ime_tabele AS novo_ime_tabele; /* [cite: 217] */
                ```
                
            - **`DISTINCT`**: Vrne samo različne (ne duplicirane) vrednosti za izbrane stolpce.
                
                SQL
                
                ```
                SELECT DISTINCT ime, priimek FROM ime_tabele; /* [cite: 220] */
                ```
                
            - **`WHERE` pogoj:** Filtrira vrstice na podlagi določenega pogoja.
                
                - **Operatorji:** `=`, `>`, `<`, `>=`, `<=`, `!=` (ali `<>`).
                - **`AND`, `OR`, `NOT`:** Logični operatorji za kombiniranje pogojev. Pri več `NOT` pogojih je vmes obvezno `AND`.
                    
                - **`IN (vrednost1, vrednost2, ...)`**: Enako kot več `OR` pogojev; preveri, ali je vrednost stolpca ena izmed navedenih vrednosti.
                    
                    SQL
                    
                    ```
                    /* Primer uporabe IN namesto več OR [cite: 234] */
                    SELECT * FROM drzava WHERE drzava IN ('slovenija', 'avstrija', 'nizozemska');
                    ```
                    
                - **`BETWEEN vrednost1 AND vrednost2`**: Izbere vrednosti znotraj danega obsega (vključno z začetno in končno vrednostjo). `NOT BETWEEN` naredi nasprotno.
                    
                    SQL
                    
                    ```
                    SELECT * FROM Produkt WHERE cena BETWEEN 10 AND 20; /* [cite: 255] */
                    ```
                    
                - **`LIKE`**: Uporablja se za iskanje določenega vzorca v stolpcu. Uporablja nadomestne znake:
                    
                    - `%`: Predstavlja nič, enega ali več znakov.
                        
                    - `_`: Predstavlja en sam znak. <!-- end list -->
                        
                    
                    SQL
                    
                    ```
                    /* Poišče imena strank, ki se končajo na 'a' */
                    SELECT * FROM Customers WHERE CustomerName LIKE '%a'; /* [cite: 262] */
                    /* Poišče imena, kjer je druga črka 'n' */
                    SELECT * FROM Customers WHERE CustomerName LIKE '_n%';
                    ```
                    
                - **`IS NULL` / `IS NOT NULL`**: Preveri, ali je vrednost stolpca `NULL` (prazna) ali ne. `NULL` je različno od nič ali presledkov.
                    
                    SQL
                    
                    ```
                    SELECT column_names FROM table_name WHERE column_name IS NULL; /* [cite: 246] */
                    ```
                    
            - **`ORDER BY stolpec1 [ASC|DESC], stolpec2 [ASC|DESC], ...`**: Razvrsti rezultat po enem ali več stolpcih naraščajoče (`ASC`, privzeto) ali padajoče (`DESC`). Razvršča po ASCII tabeli.
                
                SQL
                
                ```
                SELECT * FROM r3b ORDER BY ime DESC; /* [cite: 239] */
                /* Razvrsti po drugem stolpcu padajoče */
                SELECT * FROM r3b ORDER BY 2 DESC; /* [cite: 239] */
                ```
                
            - **`CONCAT(niz1, niz2, ...)`**: Združi več nizov (stolpcev ali konstant) v enega.
                
                SQL
                
                ```
                SELECT CONCAT(ime, ' ', priimek) AS Pisatelj FROM knjiga; /* [cite: 250, 251] */
                ```
                
            - **Agregatne funkcije:** Izvajajo izračune na skupini vrednosti in vrnejo eno samo vrednost.
                
                - **`COUNT(stolpec)`**: Vrne število vrstic (ne šteje `NULL` vrednosti, razen `COUNT(*)`).
                    
                - **`SUM(stolpec)`**: Vrne vsoto numeričnih vrednosti.
                    
                - **`AVG(stolpec)`**: Vrne povprečno vrednost numeričnih vrednosti.
                    
                - **`MIN(stolpec)`**: Vrne najmanjšo vrednost (po ASCII).
                    
                - **`MAX(stolpec)`**: Vrne največjo vrednost (po ASCII). <!-- end list -->
                    
                
                SQL
                
                ```
                SELECT COUNT(column_name) FROM table_name WHERE condition; /* [cite: 271] */
                SELECT MAX(column_name) FROM table_name WHERE condition; /* [cite: 269] */
                ```
                
            - **`GROUP BY stolpec1, stolpec2, ...`**: Združi vrstice, ki imajo enake vrednosti v določenih stolpcih, v vrstice s povzetkom. Pogosto se uporablja z agregatnimi funkcijami.
                
                SQL
                
                ```
                SELECT COUNT(CustomerID), Country FROM Customers GROUP BY Country;
                ```
                
            - **`HAVING pogoj`**: Filtrira rezultate po združevanju (uporablja se z `GROUP BY`), ker `WHERE` ni mogoče uporabiti z agregatnimi funkcijami na ta način.
                
                SQL
                
                ```
                SELECT COUNT(CustomerID), Country FROM Customers GROUP BY Country HAVING COUNT(CustomerID) > 5; /* [cite: 275] (primer pojasnjen) */
                ```
                
            - **`UNION` / `UNION ALL`**: Združi rezultate dveh ali več `SELECT` stavkov. Stolpci morajo imeti enako število, podobne tipe podatkov in biti v istem vrstnem redu. `UNION` odstrani duplikate, `UNION ALL` jih ohrani.
                
                SQL
                
                ```
                SELECT column_name(s) FROM table1
                UNION
                SELECT column_name(s) FROM table2; /* [cite: 285] */
                ```
                
            - **Povezovanje tabel (Joins):** Kombiniranje vrstic iz dveh ali več tabel na podlagi povezanih stolpcev.
                - **Implicitno povezovanje (z enačajem v `WHERE` klavzuli):** Navedemo imena tabel in pogoje povezovanja v `WHERE`.
                    
                    SQL
                    
                    ```
                    SELECT t1.stolpec1, t2.stolpec1
                    FROM tabela1 t1, tabela2 t2
                    WHERE t1.povezovalni_stolpec = t2.povezovalni_stolpec; /* [cite: 291] */
                    
                    SELECT * FROM stranke s, poste p WHERE s.postna_st=p.postna_st; /* [cite: 291] */
                    ```
                    
                - **Eksplicitno povezovanje (JOIN klavzule):** `INNER JOIN`, `LEFT OUTER JOIN`, `RIGHT OUTER JOIN` (kot je omenjeno v prvotnih zapiskih, a ni podrobno razloženo v tej PPT).
    - **DCL (Data Control Language - Jezik za nadzor podatkov):** Ukazi za upravljanje pravic dostopa do podatkov (npr. `GRANT`, `REVOKE`).
        
    - **TCL (Transaction Control Language - Jezik za nadzor transakcij):** Ukazi za upravljanje transakcij (npr. `COMMIT`, `ROLLBACK`).
        
- **Pogledi (Views):**
    
    - Navidezna tabela, ki predstavlja rezultat poizvedbe `SELECT`.
        
    - Uporabni za poenostavitev zapletenih poizvedb. Ime pogleda ne sme biti enako imenu obstoječe tabele.
        
    - **Kreiranje:** `CREATE VIEW ime_pogleda AS SELECT ...;`
        
    - **Posodabljanje:** `CREATE OR REPLACE VIEW ime_pogleda AS SELECT ...;`
        
    - **Brisanje:** `DROP VIEW ime_pogleda;`
        
    - **Prikaz podatkov iz pogleda:** `SELECT * FROM ime_pogleda;`
        
        SQL
        
        ```
        CREATE VIEW [Brazil Customers] AS
        SELECT CustomerName, ContactName, City
        FROM Customers
        WHERE Country = 'Brazil'; /* [cite: 296] */
        ```
        
- **Indeksi (Indexes):**
    
    - Posebne iskalne tabele, ki jih pogon podatkovne baze lahko uporabi za pospešitev pridobivanja podatkov. Uporabniki jih ne vidijo neposredno.
        
    - Posodabljanje tabele z indeksi traja dlje, zato se ustvarijo samo za stolpce, po katerih se pogosto išče. Indeksov se običajno ne posodablja neposredno; zbrišejo se in ustvarijo na novo, če je potrebna sprememba strukture indeksa.
        
    - **Kreiranje:** `CREATE INDEX ime_indeksa ON ime_tabele (stolpec1, stolpec2, ...);`
        
    - **Kreiranje unikatnega indeksa:** `CREATE UNIQUE INDEX ime_indeksa ON ime_tabele (stolpec1, ...);`
        
    - **Brisanje (MySQL):** `ALTER TABLE ime_tabele DROP INDEX ime_indeksa;`
        
    - **Prikaz (MySQL):** `SHOW INDEXES FROM ime_tabele;`
---

### 3. Načrtovanje in razvoj spletnih aplikacij (Web Application Design and Development) 🌐

- **HTML (HyperText Markup Language):**
    
    - **HTML sintaktična pravila (HTML Syntax Rules):** sestavljanje elementov, začetna in končna značka, pravilno gnezdenje, atributi.
    - **Osnovna zgradba dokumenta (Basic HTML Document Structure):**
        
        - `<!DOCTYPE>`: Določa verzijo (X)HTML dokumenta.
            
        - `<html>`: Korenski element HTML dokumenta. Običajno z atributom `lang` za določitev jezika vsebine (npr. `<html lang="sl">`).
            
        - `<head>`: Vsebuje meta informacije o strani (ne prikažejo se neposredno na strani).
            
            - `<title>`: Določa naslov dokumenta, ki se prikaže v naslovni vrstici brskalnika ali zavihku strani.
                
            - `<meta />`: Zagotavlja meta podatke o HTML dokumentu.
                
                - `charset`: Določa nabor znakov (npr. `<meta charset="UTF-8">`).
                - `description`: Kratek opis vsebine strani.
                - `viewport`: Nastavi vidno območje na različnih napravah (npr. `<meta name="viewport" content="width=device-width, initial-scale=1.0">`).
            - `<link />`: Povezuje zunanje vire, najpogosteje CSS datoteke (npr. `<link rel="stylesheet" href="style.css">`).
                
            - `<style>`: Uporablja se za vključitev notranjih CSS pravil.
                
            - `<script>`: Uporablja se za vključitev JavaScript kode.
                
            - `<base />`: Določa osnovni URL za vse relativne povezave na strani.
                
        - `<body>`: Vsebuje vso vidno vsebino HTML dokumenta.
            
            - **Strukturni elementi (Semantic/Structural Elements):**
                - `<header>`: Glava dokumenta ali sekcije.
                - `<footer>`: Noga dokumenta ali sekcije.
                - `<nav>`: Navigacijske povezave.
                - `<section>`: Generični odsek dokumenta.
                - `<article>`: Samostojen del vsebine (npr. novica, članek).
                - `<aside>`: Stranska vsebina (npr. stranska vrstica).
                - `<main>`: Glavna vsebina dokumenta.
                - `<figure>`: Skupina medijske vsebine, običajno s `<figcaption>`.
                - `<figcaption>`: Naslov za element `<figure>`.
                - `<div>`: Generični vsebnik (blokovni element) za združevanje elementov za stiliziranje ali skriptiranje.
                    
                - `<span>`: Generični vsebnik (vrstični element) za dele besedila ali dokumenta.
                    
            - **Naslovi (Headings):** `<h1>` do `<h6>` – označujejo naslove različnih nivojev.
                
            - **Odstavki (Paragraphs):** `<p>` – označuje odstavek besedila.
                
            - **Oblikovanje besedila (Text Markup):**
                - `<strong>`: Močan poudarek (običajno krepko).
                    
                - `<em>`: Poudarek (običajno ležeče).
                    
                - `<blockquote>`: Daljši citat (običajno z zamikom).
                    
                - `<q>`: Krajši, vrstični citat (običajno z narekovaji).
                    
                - `<abbr>`: Okrajšava.
                    
                - `<code>`: Del računalniške kode.
                    
                - `<cite>`: Navedba (npr. naslov dela).
                    
                - `<sub>`: Podpisano besedilo.
                    
                - `<sup>`: Nadpisano besedilo.
                    
                - `<pre>`: Predformatirano besedilo (ohranja presledke in prelome vrstic).
                    
                - `<br />`: Prelom vrstice.
                    
                - `<hr />`: Tematska prekinitev (običajno prikazana kot vodoravna črta).
                    
            - **Povezave (Links):**
                - `<a href="url">Besedilo povezave</a>`: Hiperpovezava na drug dokument ali vir.
                    
                - Notranje povezave: `<a href="#id_elementa">Povezava na del strani</a>`.
                    
                - Relativne povezave: Glede na trenutni dokument (npr. `stran2.html`, `/slike/logo.png`, `../index.html`).
            - **Slike (Images):**
                - `<img src="pot_do_slike.jpg" alt="opis slike" />`: Vstavi sliko. `src` določa pot do slike, `alt` pa alternativno besedilo.
                    
            - **Seznami (Lists):**
                - `<ul>`: Neurejen (bulleted) seznam.
                    
                - `<ol>`: Urejen (numbered) seznam.
                    
                - `<li>`: Element seznama (znotraj `<ul>` ali `<ol>`).
                    
                - `<dl>`: Definicijski seznam.
                    
                - `<dt>`: Izraz v definicijskem seznamu.
                    
                - `<dd>`: Opis/definicija izraza v definicijskem seznamu.
                    
            - **Tabele (Tables):**
                - `<table>`: Definira tabelo.
                    
                - `<tr>`: Definira vrstico v tabeli.
                    
                - `<td>`: Definira celico s podatki v tabeli.
                    
                - `<th>`: Definira glavno celico v tabeli (naslov stolpca ali vrstice).
                    
                - `<caption>`: Naslov tabele.
                    
                - `<thead>`: Glava tabele.
                    
                - `<tbody>`: Telo tabele.
                    
                - `<tfoot>`: Noga tabele.
                    
                - Atributa `rowspan` in `colspan` za združevanje celic.
            - **Obrazci (Forms):** Elementi za zbiranje uporabniških podatkov.
                
                - `<form action="url_skripte" method="get|post" enctype="tip_kodiranja">`: Definira obrazec.
                    
                    - `action`: URL, kamor se pošljejo podatki obrazca. Če je izpuščen, se podatki pošljejo na isti dokument.
                        
                    - `method`: HTTP metoda za pošiljanje podatkov (`get` ali `post`). Privzeto je `get`, če je atribut izpuščen.
                        
                    - `enctype="multipart/form-data"`: Uporablja se pri nalaganju datotek.
                        
                - `<input />`: Najpogosteje uporabljen element obrazca. Tip se določi z atributom `type`. Vsako polje, ki prenaša podatke, mora imeti atribut `name`.
                    
                    - `type="text"`: Enovrstično vnosno polje za besedilo.
                        
                    - `type="password"`: Enovrstično vnosno polje za geslo (znaki so maskirani).
                        
                    - `type="number"`: Za vnos številčnih vrednosti.
                    - `type="email"`: Za vnos e-poštnega naslova (z vgrajeno validacijo oblike).
                    - `type="date"`: Za izbiro datuma.
                    - `type="radio"`: Izbirni gumb (samo ena možnost iz skupine z istim `name` atributom je lahko izbrana).
                        
                    - `type="checkbox"`: Potrditveno polje (več možnosti iz skupine z istim `name` (pogosto z `[]` na koncu imena, npr. `jezik[]`) je lahko izbranih).
                        
                    - `type="submit"`: Gumb za pošiljanje obrazca.
                        
                    - `type="reset"`: Gumb za ponastavitev obrazca na privzete vrednosti.
                        
                    - `type="file"`: Za izbiro datoteke za nalaganje.
                        
                    - `type="hidden"`: Skrito vnosno polje za pošiljanje podatkov, ki jih uporabnik ne vidi ali spreminja.
                        
                - `<textarea name="ime" rows="vrstic" cols="stolpcev"></textarea>`: Večvrstično vnosno polje za besedilo.
                    
                - `<label for="id_elementa">Napis</label>`: Oznaka za element obrazca. Atribut `for` se poveže z `id` ustreznega vnosnega polja.
                    
                - `<select name="ime">`: Ustvari spustni seznam.
                    
                    - `<option value="vrednost">Besedilo možnosti</option>`: Možnost znotraj spustnega seznama. Atribut `selected` predizbere možnost.
                        
                - `<button type="submit|reset|button">Besedilo gumba</button>`: Gumb.
                    
                - `<fieldset>`: Združi povezane elemente v obrazcu.
                    
                - `<legend>`: Naslov za `<fieldset>`.
                    
                - **Ostali atributi vnosnih polj:** `required` (obvezno polje), `value` (privzeta vrednost/poslana vrednost), `min`, `max` (za številske tipe), `checked` (za radio/checkbox), `placeholder` (namig v vnosnem polju), `name` (ključno za pošiljanje podatkov na strežnik).
                    
            - **Identifikator in klasifikator:**
                - `id`: Unikatni identifikator za HTML element (samo en na stran).
                    
                - `class`: Eden ali več razredov, dodeljenih HTML elementu (za stiliziranje).
                    
            - **Komentarji:** `` – brskalnik jih ignorira.
                
            - **Kodiranje znakov (Character Entities):** Za prikaz posebnih znakov, npr. `&nbsp;` (nedeljivi presledek), `&copy;` (copyright), `&lt;` (<), `&gt;` (>), `&amp;` (&), `&quot;` (").
                
- **CSS (Cascading Style Sheets):** Stilske predloge za oblikovanje HTML elementov. Omogočajo ločevanje vsebine od oblike, kar poveča preglednost kode in olajša vzdrževanje.
    
    - **CSS sintaksa:** `selektor { lastnost: vrednost; }`. Več lastnosti se loči s podpičjem. Priporoča se pisanje vsake lastnosti v svojo vrstico za boljšo preglednost. Če je vrednost sestavljena iz več besed, se uporabijo narekovaji (npr. pri `font-family`).
        
        - Komentarji v CSS: `/* Komentar */`.
            
    - **Vključevanje CSS v HTML:**
        
        - **Zunanja slogovna predloga (External CSS):** Povezava na `.css` datoteko v `<head>`: `<link rel="stylesheet" href="style.css">`. Datoteka `.css` ne sme vsebovati HTML značk.
            
        - **Notranja slogovna predloga (Internal CSS):** Pravila znotraj značke `<style>` v `<head>`.
            
        - **Vrstični slogi (Inline Styles):** Atribut `style` neposredno v HTML znački (npr. `<p style="color: blue;">`). Ta način se odsvetuje, ker meša vsebino in obliko, razen za specifične primere.
            
    - **Kaskadno pravilo in prioriteta (Cascading Rule and Specificity):** Določa, katero pravilo obvelja, če jih je za isti element več.
        
        - Prioriteta od najnižje do najvišje:
            
            1. Privzete nastavitve brskalnika.
                
            2. Zunanja slogovna predloga.
                
            3. Notranja slogovna predloga (v `<head>`).
                
            4. Vrstični slogi (atribut `style`).
                
        - Specifičnost selektorjev (ID je bolj specifičen kot class, ta pa bolj kot tip elementa).
        - Kasnejše pravilo v kodi prepiše prejšnje, če imata enako specifičnost.
    - **Selektorji (Selectors):** Vzorci za izbiranje HTML elementov, ki jih želimo stilizirati.
        
        - **Osnovni selektorji:**
            - Univerzalni selektor: `*` (izbere vse elemente).
                
            - Selektor tipa/značke: `p`, `div` (izbere vse elemente določenega tipa).
                
            - Selektor razreda: `.ime-razreda` (izbere elemente z določenim razredom, npr. `.box`). Element lahko ima več razredov (npr. `<div class="odstavek posebnobesedilo">`).
                
            - Selektor ID-ja: `#id-elementa` (izbere element z določenim ID-jem, npr. `#box`). ID mora biti unikaten na strani.
                
        - **Kombinirani selektorji (Verige):**
            - Potomci: `div p` (izbere vse `<p>` elemente, ki so kjerkoli znotraj `<div>`).
                
            - Otroci: `div > p` (izbere vse `<p>` elemente, ki so neposredni otroci `<div>`).
                
            - Sosednji bratje: `div + p` (izbere `<p>` element, ki je takoj za `<div>` in imata istega starša).
                
            - Splošni bratje: `div ~ p` (izbere vse `<p>` elemente, ki sledijo `<div>` in imata istega starša).
        - **Grupni selektor:** `div, p` (izbere vse `<div>` IN vse `<p>` elemente).
            
        - **Atributni selektorji:**
            - `[atribut]` (npr. `a[target]`)
            - `[atribut="vrednost"]` (npr. `input[type="text"]`, `div[class="box"]` ).
                
            - `[atribut~="vrednost"]` (atribut vsebuje dano besedo)
            - `[atribut|="vrednost"]` (atribut se začne z dano vrednostjo, ločeno z vezajem)
            - `[atribut^="vrednost"]` (atribut se začne z dano vrednostjo)
            - `[atribut$="vrednost"]` (atribut se konča z dano vrednostjo)
            - `[atribut*="vrednost"]` (atribut vsebuje dano podniz)
        - **Psevdo-razredi (Pseudo-classes):** Ključne besede, dodane selektorjem, ki določajo posebno stanje izbranega elementa.
            - Povezave: `:link` (neobiskana), `:visited` (obiskana), `:hover` (kazalec miške nad elementom), `:active` (aktivna/kliknjena).
                
            - Uporabniški vmesnik: `:focus` (element ima fokus), `:checked`, `:disabled`, `:enabled`.
            - Strukturni: `:first-child` (prvi otrok svojega starša), `:last-child`, `:nth-child(n)`.
                
            - `:first-line` (prva vrstica blokovnega elementa), `:first-letter` (prva črka blokovnega elementa).
                
        - **Psevdo-elementi (Pseudo-elements):** Stilizirajo določene dele elementa (npr. `::before`, `::after`, `::first-line`, `::first-letter`). V starejših CSS verzijah se je uporabljal enojni dvopičje.
    - **Enote (Units):**
        - Absolutne: `px` (piksli), `pt` (točke, 1/72 inča), `cm` (centimetri), `mm` (milimetri), `in` (inči).
            
        - Relativne: `%` (odstotek glede na starševski element), `em` (glede na velikost pisave trenutnega elementa ali starša), `rem` (glede na velikost pisave korenskega elementa), `vw` (1% širine vidnega polja), `vh` (1% višine vidnega polja).
            
        - `0` ne potrebuje enote (npr. `margin: 0;`).
            
    - **Barve (Colors):**
        - Imena barv: `red`, `blue`, `transparent`.
            
        - Hexadecimalni zapis: `#RRGGBB` (npr. `#FF0000`) ali krajše `#RGB` (npr. `#F00`).
            
        - RGB funkcija: `rgb(r, g, b)` (vrednosti od 0-255, npr. `rgb(255, 0, 0)`).
            
        - RGBA funkcija: `rgba(r, g, b, a)` (dodaja alfa kanal za prosojnost, a od 0.0 do 1.0, npr. `rgba(255, 0, 0, 0.5)`).
            
        - HSL funkcija: `hsl(hue, saturation, lightness)` (npr. `hsl(0, 100%, 50%)` za rdečo).
            
        - HSLA funkcija: `hsla(hue, saturation, lightness, alpha)`.
            
    - **Model škatle (Box Model):** Vsak HTML element je obravnavan kot pravokotna škatla. Sestavljajo jo vsebina (content), notranji odmik (padding), obroba (border) in zunanji odmik (margin).
        
        - `width`, `height`: Določata širino in višino območja vsebine elementa.
            
        - `min-width`, `max-width`, `min-height`, `max-height`: Minimalne in maksimalne dimenzije.
            
        - `padding`: Notranji odmik med vsebino in obrobo. Lahko se določi za vsako stran posebej (`padding-top`, `padding-right`, `padding-bottom`, `padding-left`) ali s skrajšanim zapisom (`padding: 5px;` ali `padding: 10px 5px;` ali `padding: 10px 5px 15px;` ali `padding: 10px 5px 15px 20px;` - vrstni red: zgoraj, desno, spodaj, levo).
            
        - `margin`: Zunanji odmik med obrobo elementa in sosednjimi elementi. Enake možnosti za posamezne strani in skrajšane zapise kot `padding`. `margin: 0 auto;` se uporablja za horizontalno centriranje blokovnega elementa, ki ima določeno širino (`width`).
            
        - `border`: Obroba okoli notranjega odmika in vsebine.
            - `border-width`: Debelina obrobe (npr. `2px`).
                
            - `border-style`: Slog obrobe (`solid`, `dashed`, `dotted`, `double`, `groove`, `ridge`, `inset`, `outset`, `none`).
                
            - `border-color`: Barva obrobe.
                
            - Skrajšani zapis: `border: 1px solid black;`.
                
            - Možno je določiti obrobe za posamezne strani: `border-top`, `border-right-style`, `border-bottom-color`, itd.
                
            - `border-radius`: Zaokrožitev vogalov obrobe.
                
        - `box-sizing`: Določa, kako se računata skupna širina in višina elementa (`content-box` (privzeto) ali `border-box`).
    - **Ozadje (Background):**
        - `background-color`: Barva ozadja.
            
        - `background-image`: Slika za ozadje (`url('pot_do_slike.png')`).
            
        - `background-repeat`: Način ponavljanja slike ozadja (`repeat`, `repeat-x`, `repeat-y`, `no-repeat`).
            
        - `background-position`: Položaj slike ozadja.
            
        - `background-attachment`: Ali se slika ozadja premika s stranjo (`scroll`) ali je fiksna (`fixed`).
            
        - Skrajšani zapis: `background: #fff url('slika.png') no-repeat fixed center;`.
            
    - **Pisava (Font):**
        - `font-family`: Družina pisave (npr. `"Times New Roman", Times, serif` - priporočljivo je navesti več možnosti, končati s generično družino). Obstajajo "web safe fonts".
            
        - `font-size`: Velikost pisave (npr. `16px`, `1.2em`).
            
        - `font-weight`: Debelina pisave (`normal`, `bold`, `bolder`, `lighter`, številčne vrednosti 100-900).
            
        - `font-style`: Slog pisave (`normal`, `italic`, `oblique`).
            
        - `line-height`: Višina vrstice (vpliva na razmik med vrsticami besedila).
            
        - Skrajšani zapis: `font: italic bold 12px/1.5 "Arial", sans-serif;`.
            
    - **Besedilo (Text):**
        - `color`: Barva besedila.
            
        - `text-align`: Poravnava besedila (`left`, `right`, `center`, `justify`).
            
        - `text-decoration`: Okrasitev besedila (`none`, `underline`, `overline`, `line-through`).
            
        - `text-transform`: Sprememba velikosti črk (`none`, `capitalize`, `uppercase`, `lowercase`).
            
        - `text-indent`: Zamik prve vrstice besedila.
            
        - `letter-spacing`: Razmik med znaki.
            
        - `word-spacing`: Razmik med besedami.
            
    - **Prikaz (Display) in Vidnost (Visibility):**
        - `display`: Določa tip prikaza elementa.
            - `block`: Element zasede celotno širino, začne se v novi vrstici.
            - `inline`: Element zasede le potrebno širino, ne začne se v novi vrstici, `width` in `height` ne delujeta.
            - `inline-block`: Kombinacija, element je vrstični, a mu lahko določimo `width`, `height`, `margin`/`padding`.
                
            - `none`: Element se ne prikaže in ne zaseda prostora.
                
            - `flex`: Omogoča fleksibilno postavitev elementov v vsebniku (zahteva dodatne lastnosti za urejanje).
        - `visibility`: Določa vidnost elementa.
            - `visible`: Element je viden (privzeto).
                
            - `hidden`: Element je skrit, a še vedno zaseda prostor na strani.
                
    - **Pozicioniranje (Positioning):** Določa metodo pozicioniranja elementa.
        
        - `position: static | relative | absolute | fixed | sticky;`
            
            - `static`: Privzeta vrednost, element sledi normalnemu toku strani. Lastnosti `top`, `right`, `bottom`, `left`, `z-index` ne delujejo.
                
            - `relative`: Element je pozicioniran relativno na svojo normalno pozicijo. Z `top`, `right`, `bottom`, `left` ga lahko odmaknemo.
                
            - `absolute`: Element je pozicioniran relativno na najbližjega pozicioniranega prednika (ki ni `static`). Če takega ni, je relativno na `<body>`.
                
            - `fixed`: Element je pozicioniran relativno na okno brskalnika (viewport) in ostane na mestu med drsenjem.
                
            - `sticky`: Hibrid med `relative` in `fixed`. Element se drži določene pozicije znotraj svojega vsebnika med drsenjem.
                
        - `top`, `right`, `bottom`, `left`: Določajo odmik za pozicionirane elemente.
            
        - `z-index`: Določa vrstni red prekrivanja pozicioniranih elementov (višja vrednost je bolj spredaj).
            
    - **Plavanje (Float):** Omogoča, da element "plava" levo ali desno, ostala vsebina pa se ovije okoli njega.
        
        - `float: left | right | none;`
            
        - `clear: both | left | right | none;`: Prepreči, da bi se elementi ovijali okoli plavajočih elementov. Pogosto se uporabi prazen `div` s `clear: both;` ali psevdo-element `::after` na staršu plavajočih elementov.
            
    - **Seznami (Lists Styling):**
        - `list-style-type`: Tip oznake (`disc`, `circle`, `square`, `decimal`, `none`, itd.).
            
        - `list-style-image`: Uporaba slike kot oznake (`url('slika.png')`).
            
        - `list-style-position`: Položaj oznake (`inside`, `outside`).
            
        - Skrajšani zapis: `list-style: square inside;`.
    - **Tabele (Tables Styling):**
        - `border-collapse: collapse | separate;` (ali so obrobe združene ali ločene).
            
        - `border-spacing`: Razmik med celicami (če je `border-collapse: separate;`).
            
    - **Prosojnost (Opacity):**
        - `opacity: vrednost;` (od 0.0 - popolnoma prosojno, do 1.0 - popolnoma vidno).
    - **Postavitve elementov (Element Layouts):**
        - Centriranje blokovnih elementov: `margin-left: auto; margin-right: auto;` (in določena `width`).
            
        - Postavljanje blokovnih elementov drug zraven drugega: `float`, `display: inline-block`, `flexbox`, `grid`.
            
        - Navigacijska vrstica: Pogosto se ustvari s seznamom `<ul>`, kjer so `<li>` elementi stilizirani z `display: inline` ali `float: left`.
    - **Flexbox (Flexible Box Layout):** Napreden model za postavljanje elementov v eni dimenziji.
        - Za starševski element (container): `display: flex;`
        - `flex-wrap: nowrap | wrap | wrap-reverse;` (določa, ali se elementi prelomijo v novo vrstico, če ne ustrezajo v eno).
    - **Media Queries:** Omogočajo uporabo različnih stilov za različne naprave ali velikosti zaslona.
        - Sintaksa: `@media tip_medija and (pogoj) { /* CSS pravila */ }` (npr. `@media screen and (max-width: 600px) { body { background-color: lightblue; } }`).

---

### 4. Vzpostavitev in vzdrževanje omrežnih servisov

#### IP naslovi in naslavljanje (IP Addresses and Addressing)

**IP naslovi in verzije:**
- **Kaj je IP naslov?**
    - IP naslov je unikatni identifikator naprave v omrežju, ki omogoča komunikacijo med napravami. Sestavljen je iz dveh delov:
        - **Omrežni del (Network Portion):** Identificira omrežje, v katerem se naprava nahaja.
        - **Gostiteljski del (Host Portion):** Identificira specifično napravo znotraj omrežja.

- **Zakaj imamo različne verzije?**
    - **IPv4 (Internet Protocol version 4):**
        - Najpogosteje uporabljena verzija.
        - 32-bitni naslov, ki omogoča približno 4,3 milijarde unikatnih naslovov.
        - Zaradi omejenega števila naslovov je prišlo do pomanjkanja, kar je spodbudilo razvoj nove verzije.
    - **IPv6 (Internet Protocol version 6):**
        - Naslednik IPv4, zasnovan za reševanje pomanjkanja naslovov.
        - 128-bitni naslov, ki omogoča ogromno število naslovov (2^128).
        - Ponuja izboljšano varnost, avtomatsko konfiguracijo in boljšo podporo za mobilne naprave.

**Razlike med IPv4 in IPv6:**
| Lastnost         | IPv4                          | IPv6                          |
|------------------|-------------------------------|-------------------------------|
| Dolžina naslova  | 32-bitni                     | 128-bitni                    |
| Zapis naslova    | Decimalni (npr. 192.168.1.1) | Šestnajstiški (npr. 2001:db8::1) |
| Število naslovov | ~4,3 milijarde               | ~340 undecilijonov           |
| Konfiguracija    | Ročna ali DHCP               | Avtomatska ali DHCPv6         |
| Vgrajena varnost | Ni obvezna                   | IPsec je obvezen             |

---

**IP razredi (IPv4 Classes):**
- IPv4 naslovi so razdeljeni v razrede, ki določajo velikost omrežja in število gostiteljev:
    - **Razred A:** 
        - Območje: `1.0.0.0` - `126.255.255.255`
        - Maska: `255.0.0.0` (ali `/8`)
        - Namenjen velikim omrežjem (do ~16 milijonov gostiteljev).
    - **Razred B:** 
        - Območje: `128.0.0.0` - `191.255.255.255`
        - Maska: `255.255.0.0` (ali `/16`)
        - Namenjen srednje velikim omrežjem (do ~65 tisoč gostiteljev).
    - **Razred C:** 
        - Območje: `192.0.0.0` - `223.255.255.255`
        - Maska: `255.255.255.0` (ali `/24`)
        - Namenjen majhnim omrežjem (do 254 gostiteljev).
    - **Razred D:** 
        - Območje: `224.0.0.0` - `239.255.255.255`
        - Namenjen za multicast (večtočkovno oddajanje).
    - **Razred E:** 
        - Območje: `240.0.0.0` - `255.255.255.255`
        - Rezerviran za eksperimentalne namene.

---

**Rezervirani naslovi:**
- **Zasebni naslovi (Private IP Addresses):**
    - Uporabljajo se znotraj lokalnih omrežij in niso usmerljivi po internetu.
    - Območja:
        - `10.0.0.0` - `10.255.255.255` (Razred A)
        - `172.16.0.0` - `172.31.255.255` (Razred B)
        - `192.168.0.0` - `192.168.255.255` (Razred C)
- **APIPA (Automatic Private IP Addressing):**
    - `169.254.0.0` - `169.254.255.255`
    - Samodejno dodeljeni naslovi, če DHCP strežnik ni na voljo.
- **Loopback naslovi:**
    - `127.0.0.0` - `127.255.255.255`
    - Uporabljajo se za testiranje omrežnih nastavitev na lokalni napravi.

---

**Maske podomreženja (Subnet Masks):**
- **Kaj je maska podomrežja?**
    - Določa, kateri del IP naslova pripada omrežju in kateri gostitelju.
    - Primer: Maska `255.255.255.0` pomeni, da so prvi trije okteti omrežni del, zadnji oktet pa gostiteljski del.

- **Podomreženje (Subnetting):**
    - Postopek delitve večjega omrežja na manjša podomrežja.
    - Omogoča boljšo organizacijo omrežja in učinkovitejšo uporabo naslovnega prostora.
    - Primer: Omrežje `192.168.1.0/24` lahko razdelimo na dve podomrežji:
        - `192.168.1.0/25` (128 naslovov)
        - `192.168.1.128/25` (128 naslovov)

---

**VLSM (Variable Length Subnet Masking):**
- **Kaj je VLSM?**
    - Tehnika, ki omogoča uporabo različnih dolžin mask podomrežja znotraj istega omrežja.
    - Omogoča boljšo optimizacijo naslovnega prostora, saj se vsakemu podomrežju dodeli le toliko naslovov, kolikor jih potrebuje.
- **Primer:**
    - Omrežje `192.168.1.0/24`:
        - Podomrežje za 50 gostiteljev: `192.168.1.0/26` (64 naslovov)
        - Podomrežje za 20 gostiteljev: `192.168.1.64/27` (32 naslovov)
        - Podomrežje za 10 gostiteljev: `192.168.1.96/28` (16 naslovov)

VLSM omogoča bolj fleksibilno in učinkovito načrtovanje omrežij, še posebej v večjih organizacijah.

### OSI in TCP/IP referenčni modeli

#### OSI model (Open Systems Interconnection Model)
OSI model je teoretični okvir, ki opisuje, kako poteka komunikacija v omrežjih. Razdeljen je na 7 plasti, kjer vsaka plast opravlja specifične naloge in komunicira z neposredno sosednjimi plastmi.

1. **Aplikacijska plast (Application Layer)**  
    - Vmesnik med uporabniškimi aplikacijami in omrežnimi storitvami.  
    - **Protokoli:** HTTP (80), HTTPS (443), FTP (20, 21), SMTP (25), POP3 (110), IMAP (143), DNS (53).  

2. **Predstavitvena plast (Presentation Layer)**  
    - Formatiranje podatkov, kodiranje znakov, šifriranje in stiskanje.  
    - **Primeri:** SSL/TLS (šifriranje), ASCII, JPEG.  

3. **Sejna plast (Session Layer)**  
    - Upravljanje sej (vzpostavljanje, vzdrževanje in prekinjanje).  
    - **Primeri:** NetBIOS, RPC.  

4. **Transportna plast (Transport Layer)**  
    - Zanesljiv prenos podatkov, segmentacija, nadzor napak.  
    - **Protokoli:** TCP (zanesljiv, povezavno usmerjen), UDP (hiter, nepovezavno usmerjen).  
    - **Vrata:** TCP/UDP vrata (npr. 80 za HTTP, 443 za HTTPS).  

5. **Omrežna plast (Network Layer)**  
    - Logično naslavljanje in usmerjanje paketov.  
    - **Protokoli:** IP, ICMP (ping), ARP (prevajanje IP v MAC).  

6. **Povezavna plast (Data Link Layer)**  
    - Prenos podatkovnih okvirjev med napravami v istem omrežju.  
    - **Protokoli:** Ethernet, Wi-Fi (802.11).  

7. **Fizična plast (Physical Layer)**  
    - Prenos surovih bitov preko fizičnega medija.  
    - **Primeri:** UTP kabli, optični kabli, radijski valovi.  

---

#### TCP/IP model
TCP/IP model je praktični okvir, ki temelji na protokolih, uporabljenih v internetu. Ima 4 plasti (včasih 5).

1. **Aplikacijska plast (Application Layer)**  
    - Združuje funkcije OSI plasti 5, 6, 7.  
    - **Protokoli:** HTTP, HTTPS, FTP, SMTP, DNS, SNMP.  

2. **Transportna plast (Transport Layer)**  
    - Enaka kot v OSI modelu.  
    - **Protokoli:** TCP, UDP.  

3. **Internetna plast (Internet Layer)**  
    - Enaka kot omrežna plast v OSI modelu.  
    - **Protokoli:** IP, ICMP, ARP.  

4. **Plast omrežnega dostopa (Network Access Layer)**  
    - Združuje funkcije OSI plasti 1 in 2.  
    - **Protokoli:** Ethernet, Wi-Fi.  

---

#### Zakaj se uporablja OSI model?
- **Standardizacija:** Omogoča enoten način razumevanja omrežnih procesov.  
- **Diagnostika:** Pomaga pri odpravljanju težav z omrežjem.  
- **Razvoj:** Omogoča modularni razvoj omrežnih tehnologij.  

#### Zakaj se uporablja TCP/IP model?
- **Praktičnost:** Temelji na protokolih, ki se uporabljajo v internetu.  
- **Interoperabilnost:** Omogoča komunikacijo med različnimi napravami in sistemi.  
- **Razširljivost:** Podpira velike in kompleksne omrežne infrastrukture.  

---

#### Pomembni protokoli in pripadajoča vrata
| **Protokol** | **Vrata** | **Opis** |
|--------------|-----------|----------|
| HTTP         | 80        | Prenos spletnih strani. |
| HTTPS        | 443       | Varen prenos spletnih strani. |
| FTP          | 20, 21    | Prenos datotek. |
| SMTP         | 25        | Pošiljanje e-pošte. |
| POP3         | 110       | Sprejemanje e-pošte. |
| IMAP         | 143       | Sprejemanje e-pošte (naprednejše). |
| DNS          | 53        | Resolucija domenskih imen. |
| SSH          | 22        | Varen oddaljeni dostop. |
| Telnet       | 23        | Oddaljeni dostop (nezavarovan). |
| DHCP         | 67, 68    | Samodejna dodelitev IP naslovov. |
| SNMP         | 161, 162  | Upravljanje omrežja. |
| RDP          | 3389      | Oddaljeno namizje. |


- **Vzpostavitev lokalnega (Ethernet, Wi-Fi) omrežja in povezava v medmrežje (Setting up a local (Ethernet, Wi-Fi) network and connecting to the internet):**
    
    - **Fizična postavitev (Physical Layout):**
        - **Prenosni mediji (Transmission Media):**
            - **UTP kabel (Unshielded Twisted Pair cable):** Najpogosteje uporabljen v lokalnih omrežjih (LAN - Local Area Network). Sestavljen je iz paric prepletenih bakrenih žic.
                - **Kategorije (Categories):** Cat 5e (do 1 Gbps), Cat 6 (do 1 Gbps, boljša zmogljivost na daljših razdaljah, do 10 Gbps na krajših), Cat 6a (do 10 Gbps). Vsaka kategorija podpira določene frekvence in hitrosti prenosa.
                - **Lastnosti:** Relativno poceni, enostaven za namestitev, občutljiv na elektromagnetne motnje (EMI - Electromagnetic Interference).

            - **STP kabel (Shielded Twisted Pair cable):** Ima dodatno zaščito (folijo ali pletenico) okoli posameznih paric ali celotnega kabla, kar zmanjšuje elektromagnetne motnje.
                - **Prednosti:** Boljša zaščita pred EMI in presluhi (crosstalk) v primerjavi z UTP kabli.
                - **Slabosti:** Višja cena, težja in bolj zahtevna namestitev.

            - **S/FTP kabel (Shielded Foiled Twisted Pair cable):** Kombinacija zaščite, kjer je celoten kabel ovit v pletenico (S - Shielded), posamezne parice pa so ovite v folijo (FTP - Foiled Twisted Pair).
                - **Prednosti:** Najboljša zaščita pred EMI in presluhi, primeren za okolja z visoko elektromagnetno interferenco.
                - **Slabosti:** Višja cena in zahtevnejša namestitev.

            - **Primerjava:**
                - **UTP:** Najbolj ekonomičen in enostaven za uporabo, vendar manj odporen na motnje.
                - **STP:** Boljša zaščita pred motnjami, primeren za industrijska okolja ali okolja z veliko električne opreme.
                - **S/FTP:** Najboljša izbira za okolja z visoko stopnjo motenj, kjer je potrebna maksimalna zaščita.

            - **Zakaj izbrati STP ali S/FTP?**
                - Če je omrežje postavljeno v okolju z veliko elektromagnetnih motenj (npr. tovarne, bližina električnih kablov), STP ali S/FTP kabli zagotavljajo bolj stabilno povezavo in manj izgub podatkov.
                - Za visoke hitrosti prenosa in dolge razdalje, kjer je pomembna minimalna degradacija signala, so S/FTP kabli najboljša izbira.
            - **RJ45:** Standardni konektor za UTP kable pri Ethernet povezavah.
            - Optični konektorji: SC (Subscriber Connector), ST (Straight Tip), LC (Lucent Connector) – različni tipi za povezovanje optičnih kablov.
        - **MDI/MDIX (Media Dependent Interface / Media Dependent Interface Crossover):**
            - Funkcija **Auto MDI/MDIX** na sodobnih mrežnih napravah (stikala, usmerjevalniki) samodejno zazna, ali je potreben navaden (straight-through) ali križni (crossover) UTP kabel, in ustrezno prilagodi povezavo. S tem odpade potreba po skrbi za pravilen tip kabla med istovrstnimi (npr. stikalo-stikalo) ali raznovrstnimi (npr. računalnik-stikalo) napravami.
            - Navadni (Straight-through) UTP kabel: Povezuje raznovrstne naprave (npr. računalnik s stikalo/usmerjevalnikom). Žice so na obeh koncih enako razporejene (npr. po standardu T568B).
            - Križni (Crossover) UTP kabel: Povezuje istovrstne naprave (npr. računalnik-računalnik, stikalo-stikalo), če naprave nimajo Auto MDI/MDIX. Določene parice so na enem koncu zamenjane.
    - **Konfiguracija mrežnih nastavitev na računalniku oz. na končni napravi (Configuration of network settings on a computer or end device):**
        - **IP naslov (IP Address):** Unikatni logični naslov naprave v omrežju.
            - Statični (Static IP): Ročno dodeljen IP naslov, ki se ne spreminja. Uporabno za strežnike, tiskalnike.
            - Dinamični (Dynamic IP): Samodejno dodeljen s strani DHCP strežnika (Dynamic Host Configuration Protocol server) za določen čas (lease time). Najpogostejša nastavitev za odjemalce.
        - **Mrežna maska (Subnet Mask):** Določa, kateri del IP naslova pripada omrežju (network portion) in kateri del gostitelju (host portion). Npr. 255.255.255.0 pomeni, da so prvi trije okteti IP naslova omrežni del.
        - **Privzeti prehod (Default Gateway):** IP naslov usmerjevalnika (router) v lokalnem omrežju, preko katerega naprave dostopajo do drugih omrežij (npr. interneta). **Pomembno:** Gateway je lahko katerikoli veljaven IP naslov znotraj istega podomrežja kot odjemalec, ni nujno prvi ali zadnji uporabni naslov tega podomrežja.
        - **DNS strežnik (DNS Server - Domain Name System Server):** Strežnik, ki prevaja človeku prijazna domenska imena (npr. [www.google.com](https://www.google.com)) v IP naslove (npr. 172.217.16.36) in obratno. Lahko jih je več (primarni, sekundarni).
    - **Funkcije in delovanje mrežnih naprav (Functions and operation of network devices):**
        - **Stikalo (Switch):** Naprava druge plasti (Layer 2) OSI modela. Preusmerja podatkovne okvire (frames) med napravami v istem lokalnem omrežju na podlagi MAC naslovov (MAC addresses). Vodi tabelo MAC naslovov (MAC address table) in na katera vrata (port) so povezane naprave. Zmanjšuje kolizije (collisions) v primerjavi z vozliščem (hub). **Upravljiva stikala (Managed switches)** omogočajo naprednejše funkcije (VLAN, QoS, SNMP) in konfiguracijo preko IP naslova (spletni vmesnik ali ukazna vrstica - CLI).
        - **Usmerjevalnik (Router):** Naprava tretje plasti (Layer 3) OSI modela. Povezuje različna omrežja (npr. LAN z WAN - Wide Area Network) in usmerja podatkovne pakete (packets) med njimi na podlagi IP naslovov in usmerjevalnih tabel (routing tables). Vsaka vrata na usmerjevalniku predstavljajo ločeno oddajno domeno (broadcast domain).
        - **Modem (Modulator-Demodulator):** Naprava, ki pretvarja digitalne signale iz računalnika v analogne signale za prenos preko določenih medijev (npr. telefonske linije za DSL, koaksialni kabel za kabelski internet) in obratno.
        - **Dostopna točka (Access Point - AP):** Omogoča brezžičnim napravam (Wi-Fi clients) povezavo v žično omrežje ali ustvarja samostojno brezžično omrežje.
    - **Povezava v druga omrežja (Connection to other networks):** Uporabniške naprave v lokalnem omrežju se povezujejo v druga omrežja (npr. internet) preko privzetega prehoda (default gateway), ki je običajno usmerjevalnik.
- **Osnovna vzpostavitev brezžičnega domačega omrežja (Basic setup of a wireless home network):**
    
    - **Nastavitve usmerjevalnika (Router Settings):**
        - **Dostop do konfiguracije:** Običajno se na usmerjevalnik povežemo z računalnikom (žično ali brezžično) in v spletni brskalnik vpišemo njegov privzeti IP naslov (npr. `192.168.1.1`, `192.168.0.1` – naveden v navodilih usmerjevalnika ali na nalepki). Za prijavo sta potrebna uporabniško ime in geslo (privzeta sta pogosto `admin/admin`, `admin/password`, ki ju je **nujno treba spremeniti**).
        - **Osnovne brezžične nastavitve (Basic Wireless Settings):**
            - **SSID (Service Set Identifier):** Ime brezžičnega omrežja. Lahko se odločimo za skritje SSID-ja (disable SSID broadcast), kar pomeni, da omrežje ni vidno na seznamu razpoložljivih omrežij, a to ni močna varnostna mera.
            - **Brezžični kanal (Wireless Channel):** Za 2.4 GHz pas so pogosto priporočljivi kanali 1, 6 ali 11, da se zmanjšajo interference s sosednjimi omrežji. Za 5 GHz pas je izbira kanalov manj kritična zaradi večjega števila in manjše zasedenosti.
            - **Način delovanja (Wireless Mode/Standard):** Npr. 802.11a/b/g/n/ac/ax. Izbira vpliva na hitrost in doseg.
            - **Širina kanala (Channel Width):** Npr. 20 MHz, 40 MHz, 80 MHz. Širši kanali omogočajo višje hitrosti, a so bolj občutljivi na motnje in imajo lahko krajši doseg.
    - **Varovanje brezžičnega domačega omrežja (Securing a wireless home network):**
        - **Šifriranje in gesla (Encryption and Passwords):**
            - **WPA2 (Wi-Fi Protected Access II) s PSK (Pre-Shared Key) in AES šifriranjem:** Trenutno priporočen minimalni standard za domačo uporabo.
            - **WPA3 (Wi-Fi Protected Access III):** Novejši in varnejši standard, ki nudi boljšo zaščito pred napadi na gesla.
            - Izbira močnega, unikatnega gesla (passphrase) je ključna.
            - WEP (Wired Equivalent Privacy) in WPA (prva verzija) sta zastarela in nezanesljiva.
        - **MAC filtriranje (MAC Filtering):** Omejevanje dostopa do omrežja na podlagi MAC naslovov (fizičnih naslovov) mrežnih kartic. Ustvari se seznam dovoljenih (whitelist) ali prepovedanih (blacklist) MAC naslovov. To nudi dodatno plast varnosti, vendar jo je mogoče zaobiti s ponarejanjem MAC naslova (MAC spoofing).
        - **Sprememba privzetih prijavnih podatkov usmerjevalnika.**
        - **Redno posodabljanje vdelane programske opreme (firmware) usmerjevalnika.**
    - **Filtriranje prometa (Traffic Filtering) - zapiranje/odpiranje vrat (closing/opening ports) / Port Forwarding:**
        - **Požarni zid (Firewall):** Večina domačih usmerjevalnikov ima vgrajen požarni zid, ki nadzoruje dohodni in odhodni promet med lokalnim omrežjem in internetom. Lahko blokira nezaželen promet.
        - **Zapiranje/odpiranje vrat:** S pravili na požarnem zidu lahko specifično zapremo (blokiramo) ali odpremo (dovolimo) promet na določenih vratih (port numbers) za določene protokole.
            - Pogosti porti in protokoli:
                - HTTP: 80 (spletni promet)
                - HTTPS: 443 (varen spletni promet)
                - FTP: 20 (prenos podatkov), 21 (nadzor)
                - SSH: 22 (varen oddaljeni dostop)
                - SMTP: 25 (pošiljanje e-pošte)
                - POP3: 110 (sprejemanje e-pošte)
                - IMAP: 143 (sprejemanje e-pošte)
                - DNS: 53 (resolucija domenskih imen)
                - DHCP: 67, 68 (samodejno dodeljevanje IP naslovov)
        - **Prevajanje vrat (Port Forwarding):** Omogoča zunanjim napravam z interneta dostop do specifičnih storitev na napravah znotraj lokalnega omrežja. Usmerjevalnik preusmeri promet, ki pride na določena zunanja vrata, na notranji IP naslov in vrata naprave v LAN-u (npr. za domači spletni strežnik, igralni strežnik).
        - Primer težave: Če so na požarnem zidu blokirana vrata 80 (HTTP) in 443 (HTTPS), računalnik ne bo mogel dostopati do spletnih strani. Če so blokirana vrata 53 (DNS), ne bo mogel razreševati domen v IP naslove, kar bo prav tako onemogočilo brskanje po spletu z uporabo domen.
- **IP naslovi in naslavljanje (IP Addresses and Addressing):**
    
    - **Prepoznavanje ustreznih naslovov (IPv4 in IPv6):**
        - **IPv4:** 32-bitni naslov, sestavljen iz štirih oktetov (vsak 8 bitov), zapisanih decimalno in ločenih s pikami (npr., `192.168.1.10`).
            - **Zasebni IP naslovi (Private IP Addresses):** Območja, rezervirana za uporabo v lokalnih omrežjih in niso usmerljiva po internetu (RFC 1918): `10.0.0.0` - `10.255.255.255` (10.0.0.0/8), `172.16.0.0` - `172.31.255.255` (172.16.0.0/12), `192.168.0.0` - `192.168.255.255` (192.168.0.0/16).
            - **APIPA (Automatic Private IP Addressing):** Če naprava ne more pridobiti IP naslova od DHCP strežnika, si lahko sama dodeli naslov iz območja `169.254.0.0` - `169.254.255.255` (169.254.0.0/16). Naprave z APIPA naslovi lahko komunicirajo le z drugimi napravami v istem fizičnem segmentu, ki prav tako uporabljajo APIPA.
        - **IPv6:** 128-bitni naslov, zapisan kot osem skupin po štirih šestnajstiških števk, ločenih z dvopičji (npr., `2001:0db8:85a3:0000:0000:8a2e:0370:7334`).
            - **Krajšanje IPv6 naslovov:** Vodilne ničle v vsaki skupini se lahko izpustijo (npr. `0db8` -> `db8`, `0000` -> `0`). Ena zaporedna skupina samih ničel se lahko nadomesti z dvojnim dvopičjem (`::`), vendar le enkrat v naslovu.
        - **Ukaz `ipconfig` (Windows) / `ifconfig` ali `ip addr` (Linux/macOS):** Prikazuje konfiguracijo omrežnih vmesnikov. Analiza izpisa pomaga diagnosticirati težave:
            - Manjkajoč IP naslov ali maska.
            - IP naslov iz APIPA območja (kaže na težavo z DHCP).
            - Napačen privzeti prehod (onemogoča dostop do drugih omrežij).
            - Napačni DNS strežniki (onemogoča razreševanje domen).
    - **Računanje z omrežnimi naslovi (Calculating with network addresses) (za IPv4):**
        - **Naslov omrežja (Network ID):** Dobimo ga z logično operacijo AND med IP naslovom in mrežno masko. Vsi biti gostiteljskega dela so 0.
        - **Oddajni naslov (Broadcast ID):** Naslov, na katerega poslan paket prejmejo vse naprave v tem podomrežju. Vsi biti gostiteljskega dela so 1.
        - **Uporabni naslovi za gostitelje (Usable Host Addresses):** Vsi naslovi med naslovom omrežja in oddajnim naslovom. Število uporabnih naslovov = 2h−2, kjer je h število bitov za gostiteljski del.
        - **Podomreženje (Subnetting):** Postopek delitve večjega omrežja na manjša, logično ločena podomrežja. To se doseže s "sposojanjem" bitov iz gostiteljskega dela IP naslova za ustvarjanje dela za podomrežje (subnet portion) v mrežni maski.
        - **VLSM (Variable Length Subnet Masking):** Tehnika, ki omogoča uporabo različno dolgih mrežnih mask za različna podomrežja znotraj istega večjega omrežja. S tem se učinkoviteje izkoristi naslovni prostor, saj se vsakemu podomrežju dodeli le toliko naslovov, kolikor jih potrebuje.
- **NAT (Network Address Translation):**
    
    - **Namen:** Omogoča napravam v zasebnem omrežju (z zasebnimi IP naslovi) dostop do interneta preko enega ali več javnih IP naslovov. Glavni razlog za uporabo je pomanjkanje javnih IPv4 naslovov. Prav tako nudi osnovno raven varnosti, saj skriva notranjo strukturo omrežja.
    - **Delovanje:** Usmerjevalnik z NAT funkcionalnostjo spreminja izvorne IP naslove (in po potrebi vrata) odhodnih paketov iz zasebnih v javne in ciljne IP naslove (in vrata) dohodnih paketov iz javnih nazaj v zasebne.
    - **Vrste NAT:**
        - **Statični NAT (Static NAT):** Trajna ena-na-ena preslikava med zasebnim in javnim IP naslovom. Uporabno za strežnike v lokalnem omrežju, ki morajo biti dostopni z interneta preko fiksnega javnega IP naslova.
        - **Dinamični NAT (Dynamic NAT):** Preslikava zasebnih IP naslovov v enega iz nabora (pool) razpoložljivih javnih IP naslovov. Ko naprava potrebuje dostop, ji NAT dodeli prvi prosti javni IP naslov iz nabora.
        - **PAT (Port Address Translation) ali NAPT (Network Address Port Translation) ali NAT Overload:** Najpogostejša oblika. Več naprav z zasebnimi IP naslovi uporablja en sam javni IP naslov. Razlikovanje med povezavami se doseže s preslikavo kombinacije (zasebni IP : zasebna vrata) v (javni IP : unikatna javna vrata).
    
    
- **Topologija omrežij (Network Topologies):** Način, kako so naprave v omrežju fizično ali logično povezane.
    
    - **Vodilo (Bus Topology):** Vse naprave so priključene na en sam osrednji kabel (vodilo). Podatki potujejo po celem vodilu. Zastarela, težave pri odkrivanju napak, prekinitev kabla onemogoči celo omrežje.
    - **Zvezda (Star Topology):** Vse naprave so povezane z osrednjo napravo (npr. stikalo - switch, včasih vozlišče - hub). Če odpove osrednja naprava, odpove celo omrežje. Prekinitev ene povezave do naprave ne vpliva na ostale. Najpogostejša topologija v sodobnih LAN omrežjih.
    - **Obroč (Ring Topology):** Naprave so povezane v sklenjeno zanko, podatki potujejo v eni smeri. Zastarela za LAN, uporablja se v nekaterih WAN (npr. FDDI, Token Ring).
    - **Mreža (Mesh Topology):** Naprave so med seboj poljubno povezane.
        - **Polna mreža (Full Mesh):** Vsaka naprava je povezana z vsako drugo. Zagotavlja visoko redundanco in zanesljivost, a je draga in kompleksna.
        - **Delna mreža (Partial Mesh):** Nekatere naprave so povezane z več drugimi, a ne z vsemi. Kompromis med redundanco in ceno.
    - **Drevesna (Tree Topology) / Hierarhična (Hierarchical Topology):** Kombinacija zvezdaste topologije, kjer so osrednje naprave zvezd med seboj povezane.
    - **Hibridna (Hybrid Topology):** Kombinacija dveh ali več različnih osnovnih topologij.
- **Varnost pri načrtovanju omrežja (Security in Network Design):** Načela in tehnike za zaščito omrežja in podatkov.
    
    - **Požarni zid (Firewall):** Ključna komponenta. Postavlja se na robu omrežja (med lokalnim omrežjem in internetom) in lahko tudi med različnimi segmenti znotraj lokalnega omrežja (notranji požarni zid) za nadzor in filtriranje prometa na podlagi pravil (npr. IP naslovi, vrata, protokoli).
    - **DMZ (Demilitarized Zone):** Vmesno, delno zaupanja vredno omrežje med nezaupanja vrednim zunanjim omrežjem (internet) in zaupanja vrednim notranjim omrežjem. V DMZ se običajno postavljajo javno dostopni strežniki (npr. spletni, poštni, DNS strežniki), da so izolirani od notranjega omrežja.
    - **Segmentacija omrežja (Network Segmentation):** Delitev omrežja na manjše, izolirane logične enote (segmente), pogosto z uporabo **VLAN-ov (Virtual LANs)**. To omejuje obseg morebitnega napada, zmanjšuje oddajni promet in omogoča lažje upravljanje varnostnih politik za različne skupine uporabnikov ali naprav.
    - **IDS/IPS (Intrusion Detection System / Intrusion Prevention System):**
        - **IDS:** Spremlja omrežni promet in išče sumljive vzorce ali znane grožnje. Ob zaznavi sproži alarm.
        - **IPS:** Podobno kot IDS, vendar lahko aktivno blokira zaznane grožnje.
    - **VPN (Virtual Private Network):** Ustvari varen, šifriran "tunel" med dvema točkama preko javnega omrežja (npr. interneta), kar omogoča varno oddaljeno delo ali povezovanje oddaljenih lokacij.
    - **Fizična varnost (Physical Security):** Zaščita mrežne opreme (usmerjevalniki, stikala, strežniki) pred nepooblaščenim fizičnim dostopom, krajo ali poškodbami (npr. zaklepanje prostorov, nadzor dostopa).
---

### 5. Vzdrževanje informacijske strojne opreme (Maintenance of Information Hardware) 🛠️

Vzdrževanje informacijske strojne opreme je ključnega pomena za zagotavljanje zanesljivega in dolgotrajnega delovanja računalniških sistemov ter njihovih komponent. Redno in pravilno vzdrževanje lahko prepreči nepričakovane okvare, izgubo podatkov in podaljša življenjsko dobo opreme.

---

## Številski sistemi (Number Systems)

Številski sistem je sistem, v katerem so urejena števila. Za računalniško obdelavo morajo biti podatki pretvorjeni (kodirani) v obliko, primerno za računalnik. Vsako pretvorbo iz ene oblike v drugo obliko zapisa imenujemo **kodiranje**.

- **Dvojiški (Binarni) sistem (Binary System - osnova 2):** Uporablja samo števki 0 in 1. Je temelj delovanja računalnikov, saj ti interno shranjujejo in obdelujejo podatke v binarni obliki. Vsako mesto v dvojiškem številu imenujemo **bit**.
- **Desetiški (Decimalni) sistem (Decimal System - osnova 10):** Vsakdanji sistem s števkami 0-9.
- **Šestnajstiški (Heksadecimalni) sistem (Hexadecimal System - osnova 16):** Uporablja števke 0-9 in črke A-F (kjer A=10, B=11, C=12, D=13, E=14, F=15). Uporablja se za krajšo in bolj pregledno predstavitev dvojiških števil (npr. MAC naslovi, barvne kode).
- **Pretvarjanje med sistemi (Number System Conversions):**
    - **Desetiško v dvojiško:** Decimalno število se zaporedno deli z 2, dokler količnik ni 0. Ostanki deljenja, zapisani v obratnem vrstnem redu, tvorijo dvojiško število.
        - Primer: 2510​=110012​.
    - **Dvojiško v desetiško:** Vsako dvojiško mesto se pomnoži z 2 na ustrezno potenco (začne se s potenco 0 na desni) in seštevki se seštejejo.
        - Primer: 11012​=1⋅23+1⋅22+0⋅21+1⋅20=8+4+0+1=1310​.
    - **Desetiško v šestnajstiško:** Decimalno število se zaporedno deli s 16. Ostanki (kjer se 10-15 zamenja z A-F) se zapišejo v obratnem vrstnem redu.
        - Primer: 172110​=6B916​. 17510​=AF16​.
    - **Šestnajstiško v desetiško:** Vsako šestnajstiško mesto se pomnoži s 16 na ustrezno potenco in seštevki se seštejejo.
        - Primer: A316​=10⋅161+3⋅160=160+3=16310​.
    - **Dvojiško v šestnajstiško in obratno:** Dvojiško število razdelimo v skupine po 4 bite (od desne) in vsako skupino pretvorimo v eno šestnajstiško števko (ali obratno).
- **Predznačena binarna števila (Signed Binary Numbers):** Način zapisa pozitivnih in negativnih števil v dvojiškem sistemu (npr. predznak in velikost, dvojni komplement).
- **Dvojiška aritmetika (Binary Arithmetic):** Osnovne operacije, kot sta seštevanje in odštevanje, se izvajajo po pravilih dvojiškega sistema.
- **BCD kodiranje (Binary Coded Decimal):** Vsaka desetiška števka se posebej kodira s 4-bitnim dvojiškim številom.

---

## Uporaba ustreznih merskih enot (Use of appropriate units of measurement)

- **Količina podatkov:**
    - **Bit (b):** Najmanjša enota informacije, lahko ima vrednost 0 ali 1.
    - **Bajt (Byte - B):** Skupina 8 bitov (1 B = 8 b).
    - **Decimalni prefiksi (SI):** Temeljijo na potenci 10.
        - Kilobajt (KB) = 1000 B.
        - Megabajt (MB) = 1000 KB=106 B.
        - Gigabajt (GB) = 1000 MB=109 B.
        - Terabajt (TB) = 1000 GB=1012 B.
    - **Dvojiški prefiksi (IEC):** Temeljijo na potenci 2, bolj natančni pri opisu kapacitet pomnilnika.
        - Kibibajt (KiB) = 1024 B (210 B).
        - Mebibajt (MiB) = 1024 KiB (220 B).
        - Gibibajt (GiB) = 1024 MiB (230 B).
        - Tebibajt (TiB) = 1024 GiB (240 B).
        - Razlika med MB in MiB je pomembna, saj proizvajalci diskov pogosto uporabljajo decimalne, operacijski sistemi pa dvojiške vrednosti, kar vodi do navidezne razlike v kapaciteti.
- **Hitrost prenosa podatkov (Data Transfer Rate):**
    - Bitov na sekundo (bps).
    - Kilobitov na sekundo (Kbps ali kb/s).
    - Megabitov na sekundo (Mbps ali Mb/s).
    - Gigabitov na sekundo (Gbps ali Gb/s).
    - Osnovna enačba za hitrost prenosa: Hitrost prenosa=CˇasKolicˇina podatkov​. Iz tega lahko izpeljemo čas prenosa: Cˇas prenosa=Hitrost prenosa (v bitih na sekundo)Kolicˇina podatkov (v bitih)​.
    - Primer: Prenos datoteke velikosti 5 GB pri hitrosti 10 Mbps: 5 GB=5×1024 MB=5120 MB (v kontekstu datotek se pogosteje uporablja 210 za kilo, mega itd.) 5120 MB×8MBMb​=40960 Mb Cˇas=10 Mbps40960 Mb​=4096 sekund≈68.27 minut.
- **Frekvenca (Frequency):** Uporablja se za merjenje takta procesorja, pomnilnika.
    - Hertz (Hz): En cikel na sekundo.
    - Megahertz (MHz): Milijon ciklov na sekundo.
    - Gigahertz (GHz): Milijarda ciklov na sekundo.
- **Izračun velikosti datoteke (primer za nekompresiran avdio):** Velikost (v bajtih)=Trajanje (s)×Frekvenca vzorcˇenja (Hz)×Sˇt. kanalov×8Bitna globina (biti)​ ali če je bitna globina že v bajtih: Velikost (v bajtih)=Trajanje (s)×Frekvenca vzorcˇenja (Hz)×Sˇt. kanalov×Globina vzorcˇenja (bajti)

---

## Zgradba in delovanje računalnika (Computer Architecture and Operation)

Računalnik je sistem medsebojno povezanih komponent, ki skupaj obdelujejo podatke in izvajajo ukaze. Glavni namen je sprejemanje vhodnih podatkov, njihova obdelava in prikaz rezultatov na izhodnih napravah.

- **Osnovno delovanje ob zagonu (Boot Process):**
    1. **Vklop:** Napajalnik (PSU) oskrbi komponente z električno energijo.
    2. **POST (Power-On Self-Test):** BIOS/UEFI izvede samopreverjanje osnovne strojne opreme (CPU, RAM, grafična kartica, diski).
    3. **Iskanje zagonskega medija:** BIOS/UEFI poišče zagonski sektor (boot sector) na mediju, določenem v zagonskem vrstnem redu (npr. SSD, HDD, USB).
    4. **Nalaganje operacijskega sistema (OS Loading):** Zagonski nalagalnik (bootloader) naloži jedro (kernel) operacijskega sistema v RAM.
    5. **Inicializacija OS:** Operacijski sistem prevzame nadzor, naloži gonilnike in sistemske storitve. Računalnik je pripravljen za uporabo.
- **Ključne komponente računalnika:**
    - **Matična plošča (Motherboard):** Osrednja tiskana vezna plošča, ki fizično povezuje vse druge komponente (CPU, RAM, grafična kartica, razširitvene kartice) in omogoča njihovo medsebojno komunikacijo ter prenos podatkov. Na njej so različni čipi, vključno s **čipovjem (chipset)**, ki nadzira pretok podatkov.
        - **Komponente na matični plošči:**
            - **Procesorsko podnožje/vtičnica (CPU Socket):** Mesto za namestitev procesorja.
            - **Reže za pomnilnik (RAM Slots):** Za namestitev modulov RAM.
            - **Čipovje (Chipset):** Skupina integriranih vezij, ki upravlja komunikacijo med CPU, RAM, razširitvenimi karticami in perifernimi napravami. Določa združljivost komponent in nekatere funkcionalnosti matične plošče.
            - **Razširitvene reže (Expansion Slots):** Npr. PCIe (Peripheral Component Interconnect Express) reže za grafične kartice, zvočne kartice, mrežne kartice itd.
            - **Priključki za pomnilniške nosilce:** SATA (za HDD/SSD), M.2 (za SSD, podpira SATA in NVMe protokole).
            - **Priključki za napajanje:** Za povezavo z napajalnikom.
            - **BIOS/UEFI čip:** Vsebuje osnovno programsko opremo za zagon.
            - **CMOS baterija:** Napaja CMOS pomnilnik, ki hrani nastavitve BIOS/UEFI, ko je računalnik izklopljen.
            - Vgrajeni priključki za periferne naprave (USB, avdio, LAN).
        - **Formati (Form Factor):** Standardizirane velikosti in razporeditve komponent (npr. ATX, Micro-ATX, Mini-ITX), ki določajo združljivost z ohišji in število rež.
        - **BIOS (Basic Input/Output System) in UEFI (Unified Extensible Firmware Interface):**
            - **BIOS:** Starejša programska oprema, shranjena na ROM čipu, ki se zažene ob vklopu računalnika, izvede POST in naloži operacijski sistem.
            - **UEFI:** Novejši naslednik BIOS-a z naprednejšimi funkcijami: grafični vmesnik, hitrejši zagon, podpora za večje diske (nad 2TB z GPT), boljša varnost (npr. Secure Boot).
            - **Nastavitve BIOS/UEFI:** Dostopne ob zagonu (npr. s tipko Del, F2, F10). Omogočajo konfiguracijo strojne opreme: zagonski vrstni red (boot order), nastavitve CPU in RAM (frekvence, napetosti), sistemski čas in datum, omogočanje/onemogočanje vgrajenih naprav, diagnostika.
    - **Centralno procesna enota (CPU - Central Processing Unit) / Procesor:** "Možgani" računalnika, ki izvajajo programske ukaze in obdelujejo podatke. Izvaja vse računske in logične operacije.
        - **Osnovno delovanje (cikel izvajanja ukaza):**
            1. **Prevzem ukaza (Fetch):** Krmilna enota prevzame naslednji ukaz iz pomnilnika (RAM ali predpomnilnika).
            2. **Dekodiranje ukaza (Decode):** Krmilna enota razčleni ukaz, da ugotovi, katero operacijo je treba izvesti.
            3. **Izvedba ukaza (Execute):** Aritmetično-logična enota (ALE) izvede operacijo (npr. seštevanje, primerjanje).
            4. **Zapis rezultata (Write-back/Store):** Rezultat operacije se shrani nazaj v register ali pomnilnik.
        - **Deli procesorja:**
            - **Aritmetično-logična enota (ALE/ALU):** Izvaja aritmetične (seštevanje, odštevanje itd.) in logične (AND, OR, NOT itd.) operacije nad podatki.
            - **Krmilna enota (Control Unit - CU):** Upravlja in usklajuje delovanje vseh delov procesorja in ostalih komponent sistema. Skrbi za pretok podatkov in ukazov.
            - **Registri (Registers):** Majhne, zelo hitre pomnilniške celice znotraj CPU za začasno shranjevanje podatkov, ukazov ali naslovov, s katerimi procesor trenutno operira.
        - **Tehnične značilnosti procesorja:**
            - **Takt (Clock Speed/Frequency):** Hitrost, s katero procesor izvaja cikle, merjena v Hertzih (Hz), običajno Gigahercih (GHz). Višji takt običajno pomeni hitrejše delovanje.
                - Čas za en cikel (t) je obratna vrednost frekvence (f): t=f1​.
                - Primer: Če je frekvenca procesorja 3.8 GHz: t=3.8×109 Hz1​≈0.263×10−9 s=0.263 ns.
            - **Število jeder (Cores):** Jedro je samostojna procesna enota znotraj CPU. Več jeder omogoča sočasno izvajanje več opravil (multitasking) ali hitrejše izvajanje programov, ki podpirajo večnitno delovanje (multithreading).
            - **Število niti (Threads):** Nit je zaporedje ukazov, ki jih lahko obdeluje jedro. Nekateri procesorji podpirajo tehnologijo sočasnega večnitnega izvajanja (npr. Intel Hyper-Threading, AMD SMT), kjer eno fizično jedro lahko obdeluje dve niti hkrati.
            - **Predpomnilnik (Cache Memory):** Majhen, hiter SRAM pomnilnik, integriran v CPU ali zelo blizu njega, za shranjevanje pogosto uporabljenih podatkov in ukazov, kar zmanjša čas dostopa do počasnejšega RAM-a. Obstaja več nivojev: L1 (najmanjši, najhitrejši, ločen za ukaze in podatke), L2 (večji, počasnejši od L1), L3 (še večji, počasnejši od L2, pogosto deljen med jedri), L4 (redkejši).
            - **Arhitektura (Instruction Set Architecture - ISA):** Nabor ukazov, ki jih procesor razume (npr. x86, x86-64/AMD64, ARM). Število bitov (32-bitni ali 64-bitni) določa, koliko podatkov lahko procesor obdela naenkrat in maksimalno količino naslovljivega RAM-a.
            - **Podnožje (Socket):** Fizični vmesnik (tip konektorja) na matični plošči, v katerega se vgradi procesor. Procesor in matična plošča morata imeti združljivo podnožje.
        - **Proizvajalci:** Glavna proizvajalca sta Intel (serije Celeron, Pentium, Core i3/i5/i7/i9, Xeon) in AMD (serije Athlon, Ryzen, EPYC, prej Fusion, FX, Opteron).
    - **Pomnilnik (Memory):**
        - **Delovni pomnilnik (RAM - Random Access Memory):** Hiter, hlapljiv (volatile - podatki se ob izklopu izgubijo) pomnilnik, kjer računalnik začasno shranjuje podatke in programe, ki jih trenutno uporablja procesor.
            - **Vrste RAM:**
                - **DRAM (Dynamic RAM):** Najpogostejši tip glavnega pomnilnika. Potrebuje nenehno osveževanje, da ohrani podatke. Je cenejši in ima večjo gostoto kot SRAM.
                    - **DDR SDRAM (Double Data Rate Synchronous DRAM):** Različne generacije (DDR, DDR2, DDR3, DDR4, DDR5) prinašajo višje hitrosti prenosa podatkov, večje kapacitete in nižjo porabo energije.
                - **SRAM (Static RAM):** Hitrejši od DRAM, ne potrebuje osveževanja. Je dražji in se uporablja za predpomnilnike (cache) v procesorjih.
        - **Bralni pomnilnik (ROM - Read-Only Memory):** Nehlapljiv pomnilnik, katerega vsebina je običajno zapisana med proizvodnjo in je ni mogoče enostavno spreminjati (ali pa sploh ne). Vsebuje firmware, kot je BIOS/UEFI.
            - **Vrste ROM:** PROM (Programmable ROM - enkrat zapisljiv), EPROM (Erasable PROM - brisljiv z UV svetlobo), EEPROM (Electrically Erasable PROM - električno brisljiv in zapisljiv).
        - **Flash pomnilnik (Flash Memory):** Vrsta EEPROM, ki se uporablja v SSD diskih, USB ključih, pomnilniških karticah. Nehlapljiv.
        - **Pomnilniška hierarhija (Memory Hierarchy):** Sistem več nivojev pomnilnika z različnimi hitrostmi, kapacitetami in cenami, urejen tako, da CPU čim hitreje dostopa do potrebnih podatkov. Nivoji od najhitrejšega do najpočasnejšega: Registri CPU -> L1 Cache -> L2 Cache -> L3 Cache -> RAM -> SSD/HDD (navidezni pomnilnik) -> Arhivski mediji.
        - Maksimalna količina naslovljivega pomnilnika: 2sˇirina naslovnega vodila (v bitih).
    - **Pomnilniški nosilci (Storage Devices - Dolgoročni pomnilnik):** Trajno shranjevanje operacijskega sistema, programov in uporabniških podatkov.
        - **Trdi disk (HDD - Hard Disk Drive):** Elektromehanska naprava, ki shranjuje podatke na vrtečih se magnetnih ploščah z uporabo bralno-pisalnih glav.
            - **Organizacija podatkov:** Plošče (platters), sledi (tracks), sektorji (sectors), cilindri (cylinders).
            - **Tehnične lastnosti:** Kapaciteta (GB, TB), hitrost vrtenja (RPM - revolutions per minute, npr. 5400, 7200), vmesnik (SATA), predpomnilnik (cache).
            - **Prednosti:** Velika kapaciteta, nizka cena na GB.
            - **Slabosti:** Počasnejši dostopni časi in hitrosti prenosa v primerjavi s SSD, mehanski deli so občutljivi na udarce in obrabo, višja poraba energije, hrup, **fragmentacija** podatkov.
            - **Dostopni čas HDD:** Dostopni cˇas=Iskalni cˇas+Latenca vrtenja+Cˇas prenosa.
            - **Kapaciteta HDD (približno):** Sˇt. cilindrov×Sˇt. glav×Sˇt. sektorjev/sled×Velikost sektorja.
        - **SSD (Solid State Drive):** Uporablja polprevodniške flash pomnilniške čipe za shranjevanje podatkov, brez gibljivih delov.
            - **Tehnične lastnosti:** Kapaciteta, hitrost branja/pisanja (MB/s, IOPS), vmesnik (SATA, M.2, PCIe/NVMe), tip flash pomnilnika (SLC, MLC, TLC, QLC).
            - **Prednosti:** Zelo hitri dostopni časi in hitrosti prenosa, tiho delovanje, manjša poraba energije, večja odpornost na udarce, ni fragmentacije.
            - **Slabosti:** Višja cena na GB (čeprav se razlika manjša), omejeno število zapisovalnih ciklov na celico (sodobni SSD-ji imajo napredne tehnologije za podaljšanje življenjske dobe).
        - **NVMe (Non-Volatile Memory Express):** Komunikacijski vmesnik in gonilnik, zasnovan posebej za SSD-je, ki uporabljajo PCIe vodilo, kar omogoča bistveno višje hitrosti kot SATA.
        - **Zunanji diski:** HDD ali SSD v ohišju s priključkom USB ali Thunderbolt.
        - **Optični pogoni in mediji:** CD, DVD, Blu-ray (vse manj pogosti).
        - **RAID (Redundant Array of Independent Disks):** Tehnologija, ki združuje več fizičnih diskov v eno ali več logičnih enot za izboljšanje zmogljivosti (hitrosti), redundance (varnosti podatkov) ali obojega.
            - **RAID 0 (Striping - porazdeljevanje):** Podatki se delijo in zapisujejo čez vse diske v polju. Poveča hitrost branja in pisanja. Brez redundance – če en disk odpove, so vsi podatki na vseh diskih izgubljeni. Potrebujeta vsaj 2 diska.
            - **RAID 1 (Mirroring - zrcaljenje):** Podatki se hkrati zapisujejo na dva (ali več) diska, kar ustvari natančno kopijo. Zagotavlja visoko varnost podatkov; če en disk odpove, so podatki še vedno na voljo na drugem. Uporabna kapaciteta je enaka kapaciteti najmanjšega diska v polju (če sta dva). Potrebujeta vsaj 2 diska.
            - **RAID 5 (Striping with Parity - porazdeljevanje s pariteto):** Podatki in paritetne informacije (za obnovo podatkov) so porazdeljeni med tremi ali več diski. Omogoča obnovo podatkov ob odpovedi enega diska. Dobro ravnovesje med zmogljivostjo, kapaciteto in redundanco. Potrebuje vsaj 3 diske.
            - **RAID 10 (ali RAID 1+0):** Kombinacija zrcaljenja in porazdeljevanja. Podatki se najprej zrcalijo (RAID 1), nato pa se te zrcaljene skupine porazdelijo (RAID 0). Ponuja visoko hitrost in dobro redundanco. Potrebuje vsaj 4 diske.
        - **Priključki za diske:** SATA, M.2, PCIe. Starejši: IDE.
        - **Particioniranje diskov (Disk Partitioning):** Postopek razdelitve fizičnega diska na eno ali več logičnih enot, imenovanih particije. Vsaka particija se lahko formatira z drugačnim datotečnim sistemom in jo operacijski sistem vidi kot ločen disk. Uporabno za organizacijo podatkov, namestitev več operacijskih sistemov, ločevanje OS od uporabniških podatkov.
        - **MBR (Master Boot Record) vs. GPT (GUID Partition Table):** Standarda za shranjevanje informacij o particijah na disku.
            - **MBR:** Starejši standard, omejen na diske do 2TB in do 4 primarne particije (ali 3 primarne in 1 razširjeno).
            - **GPT:** Novejši standard, del UEFI. Podpira diske večje od 2TB, do 128 particij v Windows, bolj zanesljiv zaradi replikacije particijske tabele.
        - **Datotečni sistemi (File Systems):** Organizacijska struktura, ki jo operacijski sistem uporablja za shranjevanje, iskanje in upravljanje datotek na pomnilniškem nosilcu. Primeri: FAT32, exFAT, NTFS (Windows), HFS+, APFS (Apple), ext4 (Linux).
            - **Dovoljenja datotek in imenikov (File and Directory Permissions):** Nadzor dostopa do datotek in map (branje, pisanje, izvajanje) za različne uporabnike in skupine, kar vpliva na varnost podatkov.
        - **Fragmentacija diska (Disk Fragmentation):** Pojav pri HDD diskih, kjer se deli datoteke shranijo na ne-sosednjih lokacijah na disku, kar upočasni dostop, saj mora bralno-pisalna glava večkrat premikati.
        - **Defragmentacija diska (Disk Defragmentation):** Postopek prerazporejanja fragmentiranih delov datotek na HDD disku, tako da so shranjeni zaporedno, kar pospeši dostop. SSD diski defragmentacije ne potrebujejo (in jim lahko skrajša življenjsko dobo).
    - **Vhodno-izhodne enote (Input/Output - I/O Devices):** Komponente, ki omogočajo interakcijo med uporabnikom in računalnikom ter med računalnikom in drugimi napravami.
        - **Vhodne enote (Input Devices):** Pošiljajo podatke v računalnik. Primeri: tipkovnica, miška, optični bralnik (scanner), mikrofon, spletna kamera, sledilna ploščica (touchpad), zaslon na dotik.
        - **Izhodne enote (Output Devices):** Prikazujejo ali oddajajo podatke iz računalnika. Primeri: zaslon (monitor), tiskalnik, zvočniki, slušalke, projektor.
        - **Vhodno/Izhodne enote:** Nekatere naprave opravljajo obe funkciji (npr. zaslon na dotik, mrežna kartica, zunanji diski).
    - **Hlajenje (Cooling) in Napajalnik (Power Supply Unit - PSU):**
        - **Hlajenje:** Komponente med delovanjem proizvajajo toploto, ki jo je treba odvesti, da se prepreči pregrevanje in poškodbe.
            - **Pasivno hlajenje:** Hladilna telesa (heatsinks) – kovinski bloki z rebri, ki povečajo površino za oddajanje toplote.
            - **Aktivno hlajenje:** Ventilatorji (fans), ki pospešujejo pretok zraka preko hladilnih teles ali skozi ohišje. Tekočinsko hlajenje (liquid cooling) za zahtevnejše sisteme.
            - Redno čiščenje prahu iz ventilatorjev in hladilnih teles je pomembno za ohranjanje učinkovitosti hlajenja.
        - **Napajalnik (PSU):** Pretvori izmenično napetost (AC) iz električnega omrežja v stabilne enosmerne napetosti (DC), ki jih potrebujejo različne komponente računalnika (+3.3V, +5V, +12V). Pomembne lastnosti so izhodna moč (merjena v Vatih - W), učinkovitost (npr. certifikati 80 PLUS Bronze, Silver, Gold, Platinum, Titanium), število in tipi konektorjev.
    - **Grafična kartica (GPU - Graphics Processing Unit / Video Card):** Specializirana elektronska vezja za obdelavo slik in grafike ter njihov prikaz na zaslonu. Odgovorna je za renderiranje 2D in 3D grafike, video predvajanje in druge grafično intenzivne naloge.
        - **Integrirana grafika (Integrated GPU):** Vgrajena v procesor (CPU) ali na matično ploščo. Primerna za osnovna opravila, manj zahtevne igre in varčevanje z energijo.
        - **Diskretna (namenska) grafična kartica (Discrete GPU):** Ločena kartica, ki se vgradi v PCIe režo na matični plošči. Ponuja bistveno večjo zmogljivost za igre, profesionalno grafično oblikovanje, video urejanje, strojno učenje.
        - **Ključne komponente/lastnosti:**
            - **Grafični procesor (GPU chip):** Glavni del kartice, ki izvaja izračune.
            - **Video pomnilnik (VRAM):** Namenski RAM na grafični kartici (npr. GDDR6, GDDR6X) za shranjevanje tekstur, medpomnilnikov okvirjev (framebuffers) in drugih grafičnih podatkov. Kapaciteta (npr. 8GB, 12GB, 16GB) je pomembna za višje ločljivosti in kakovostnejše teksture.
            - Takt jedra (Core Clock) in pomnilnika (Memory Clock).
            - Število procesorskih enot (npr. CUDA jedra pri NVIDIA, Stream Procesorji pri AMD).
            - Priključki za zaslone (HDMI, DisplayPort).
    - **Vodila (Buses):** Komunikacijske poti (skupine žic ali optičnih vlaken) na matični plošči in znotraj komponent, ki omogočajo prenos podatkov, naslovov in krmilnih signalov med različnimi deli računalniškega sistema.
        - **Vrste vodil glede na namen:**
            - **Podatkovno vodilo (Data Bus):** Prenaša podatke med CPU, RAM-om in drugimi komponentami. Njegova širina (npr. 32-bitna, 64-bitna) določa, koliko bitov podatkov se lahko prenese hkrati, kar vpliva na hitrost prenosa.
            - **Naslovno vodilo (Address Bus):** Prenaša naslove pomnilniških lokacij ali V/I naprav, do katerih želi CPU dostopati. Njegova širina določa največjo količino pomnilnika, ki ga sistem lahko naslovi (npr. 32-bitno naslovno vodilo lahko naslovi 232 lokacij, kar je 4 GB).
            - **Krmilno vodilo (Control Bus):** Prenaša krmilne signale (npr. za branje/pisanje, zahteva za prekinitev) in signale o stanju med komponentami sistema.
        - **Primeri sistemskih in razširitvenih vodil:**
            - **FSB (Front Side Bus) - starejše:** Povezoval CPU z northbridge čipom.
            - **PCI (Peripheral Component Interconnect):** Starejše razširitveno vodilo.
            - **AGP (Accelerated Graphics Port):** Starejše vodilo, namenjeno grafičnim karticam.
            - **PCIe (Peripheral Component Interconnect Express):** Sodobno, hitro serijsko razširitveno vodilo za grafične kartice, SSD diske (NVMe), mrežne kartice itd. Obstaja v različnih različicah (npr. PCIe 3.0, 4.0, 5.0) in širinah (x1, x4, x8, x16).
            - **SATA (Serial ATA):** Vodilo za povezavo HDD in SSD diskov.
            - **USB (Universal Serial Bus):** Vodilo za priklop širokega nabora zunanjih naprav.
    - **Vmesniki (Interfaces):** Fizični priključki in protokoli, ki omogočajo povezavo med računalnikom in perifernimi napravami ali drugimi sistemi.
        - **Notranji vmesniki:** SATA, M.2, PCIe reže.
        - **Zunanji vmesniki (konektorji na ohišju):** USB (Type-A, Type-C), HDMI, DisplayPort, Ethernet (RJ-45), avdio priključki (3.5mm jack), Thunderbolt.

---

## Servis in vzdrževanje (Service and Maintenance)

- **Preventivno vzdrževanje (Preventive Maintenance):** Dejavnosti za ohranjanje delovanja in preprečevanje okvar.
    - **Redno čiščenje prahu:** Iz notranjosti ohišja, ventilatorjev, hladilnih teles in komponent (npr. s stisnjenim zrakom). Prah lahko povzroči pregrevanje in okvare.
    - **Posodabljanje programske opreme:** Redno posodabljanje operacijskega sistema, gonilnikov (drivers) za strojno opremo in firmware-a (npr. BIOS/UEFI, firmware SSD diskov) za izboljšanje stabilnosti, zmogljivosti in varnosti.
    - **Preverjanje stanja pomnilniških nosilcev:** Uporaba orodij, kot je `chkdsk` (Check Disk) v Windows, za preverjanje napak na datotečnem sistemu in fizičnih napak na HDD. S.M.A.R.T. (Self-Monitoring, Analysis, and Reporting Technology) podatki lahko napovejo bližajočo se odpoved diska.
    - **Preverjanje sistema hlajenja:** Zagotavljanje, da ventilatorji delujejo pravilno in da hladilna telesa niso zamašena s prahom. Po potrebi zamenjava termalne paste na CPU/GPU.
- **Diagnostika in odpravljanje napak (Diagnostics and Troubleshooting):**
    - **Prepoznavanje simptomov:** Nenadni ponovni zagoni, "modri zasloni smrti" (BSOD), počasno delovanje, nenavadni zvoki, napake pri zagonu.
    - **Uporaba diagnostičnih orodij:** Programska oprema za testiranje komponent (RAM, CPU, HDD/SSD, GPU), sistemski dnevniki (event logs), zvočni signali BIOS-a (beep codes) ob zagonu, ki kažejo na specifične napake.
    - **Postopno odpravljanje težav:** Preverjanje povezav, odstranjevanje nedavno dodane strojne opreme, testiranje komponent posamično.
    - **Iskanje informacij:** Uporaba priročnikov za strojno opremo, tehničnih specifikacij, spletnih forumov in baz znanja.
- **Izbira in namestitev komponent:** Pravilna izbira združljivih komponent za nadgradnjo ali zamenjavo (npr. CPU in podnožje matične plošče, tip RAM-a, moč napajalnika). Varna in pravilna namestitev.

---

## Vrednotenje zmogljivosti sistemov (System Performance Evaluation)

- **Merila zmogljivosti:** Hitrost procesorja (takt, IPC - instructions per cycle, število jeder/niti), količina in hitrost RAM-a (frekvenca, zakasnitve - timings), hitrost branja/pisanja in IOPS (Input/Output Operations Per Second) pomnilniških nosilcev, zmogljivost grafične kartice (hitrost sličic - FPS v igrah, čas renderiranja).
- **Programska oprema za testiranje (Benchmarking Software):** Orodja, ki izvajajo standardizirane teste za merjenje in primerjavo zmogljivosti komponent ali celotnega sistema (npr. Cinebench za CPU, 3DMark za GPU, CrystalDiskMark za diske).
- **Primeri specifikacij komponent in njihov pomen:**
    - **Procesor (CPU):** Npr. Intel Core i7-12700K ima 12 jeder (8 zmogljivostnih P-jeder in 4 energijsko učinkovita E-jedra) in 20 niti. Osnovna taktna frekvenca je 3.6 GHz. Več jeder in niti ter višji takt običajno pomenijo boljšo zmogljivost pri zahtevnih opravilih in večopravilnosti.
    - **Pomnilnik (RAM):** Npr. modul Corsair Vengeance LPX 16GB DDR4 ima frekvenco 3200 MHz in kapaciteto 16GB. Večja kapaciteta omogoča sočasno delo z več programi, višja frekvenca pa hitrejši prenos podatkov med RAM-om in CPU.
    - **SSD disk:** Npr. Samsung 970 EVO Plus 1TB NVMe SSD ima hitrost branja do 3500 MB/s in hitrost zapisovanja do 3300 MB/s. Te hitrosti bistveno vplivajo na odzivnost sistema, hitrost zagona OS in nalaganja programov.
    - **Grafična kartica (GPU):** Npr. NVIDIA GeForce RTX 3060 ima 12 GB GDDR6 video pomnilnika (VRAM). Količina in hitrost VRAM-a sta pomembni za igranje iger pri višjih ločljivostih in grafičnih nastavitvah, pa tudi za profesionalne aplikacije, kot sta 3D modeliranje in video urejanje.