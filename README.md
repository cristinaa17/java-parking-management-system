# Java Parking Management System 

Aplicație web pentru gestionarea unei parcări, dezvoltată în Java folosind tehnologii din ecosistemul Jakarta EE.

Proiectul permite administrarea mașinilor și a utilizatorilor, asocierea fotografiilor cu vehiculele și controlarea accesului la funcționalități în funcție de rolurile utilizatorilor.

## Funcționalități

- **Gestionarea mașinilor** – adăugarea, editarea, afișarea și ștergerea înregistrărilor despre vehicule.
- **Gestionarea utilizatorilor** – administrarea conturilor și a informațiilor asociate.
- **Autentificare** – formular de conectare și deconectare.
- **Autorizare pe roluri** – restricționarea accesului la operații în funcție de permisiuni.
- **Fotografii pentru vehicule** – încărcarea și gestionarea imaginilor asociate mașinilor.
- **Persistența datelor** – utilizarea JPA pentru maparea entităților și interacțiunea cu baza de date.
- **Interfață web** – pagini JSP și componente Bootstrap.

## Tehnologii utilizate

- Java
- Jakarta EE
- Servlets și JSP
- Jakarta Persistence API (JPA)
- Gradle
- GlassFish
- HTML și Bootstrap

## Structura proiectului

```text
parking-lot/
├── gradle/                         # Fișierele Gradle Wrapper
├── src/
│   └── main/
│       ├── java/
│       │   ├── org/common/         # Obiecte DTO
│       │   ├── org/ejb/            # Componente pentru logica aplicației
│       │   ├── org/example/        # Entități persistente
│       │   └── org/parking/        # Servlete web
│       ├── resources/
│       │   └── META-INF/           # Configurația JPA și CDI
│       └── webapp/
│           └── WEB-INF/            # Configurația web și paginile JSP
├── build.gradle
├── settings.gradle
├── gradlew
├── gradlew.bat
└── README.md
```

## Configurare și rulare

### Cerințe preliminare

- JDK compatibil cu versiunea Java configurată în proiect.
- Gradle Wrapper, inclus în repository.
- Un server de aplicații compatibil cu versiunea Jakarta EE utilizată, de exemplu GlassFish.
- O bază de date și o sursă de date JTA configurată pentru aplicație.

### 1. Clonarea repository-ului

```bash
git clone https://github.com/cristinaa17/java-parking-management-system.git
cd java-parking-management-system
```

### 2. Construirea proiectului

Pe macOS sau Linux:

```bash
./gradlew build
```

Pe Windows:

```bash
gradlew.bat build
```

### 3. Configurarea serverului

Înainte de rulare, configurează în GlassFish sursa de date `jdbc/ParkingLotResource`, realm-ul de autentificare `jdbcRealmParkingLot` și rolurile necesare aplicației.

### 4. Publicarea aplicației

Construiește arhiva WAR folosind Gradle și public-o pe serverul de aplicații compatibil. Consultă configurația Gradle pentru numele exact al arhivei generate.

> **Notă:** pașii de configurare a bazei de date, a utilizatorilor și a rolurilor depind de mediul local. Proiectul nu include automat toate aceste configurări.

## Obiective de învățare

- Dezvoltarea aplicațiilor web folosind Java și Jakarta EE.
- Separarea logicii aplicației de interfața web.
- Utilizarea servletelor și a paginilor JSP.
- Persistența datelor prin JPA.
- Implementarea autentificării și autorizării pe roluri.
- Organizarea și construirea unui proiect Java cu Gradle.

## Stadiul proiectului

Proiect universitar pentru exersarea dezvoltării aplicațiilor web Java și a tehnologiilor enterprise.

