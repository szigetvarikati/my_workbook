#### 1. What is TypeScript, and how does it relate to JavaScript?
TypeScript is a superset of JavaScript that adds optional static typing and other features to the language. It compiles down to plain JavaScript, making it compatible with existing JavaScript codebases.

(A TypeScript egy JavaScript fölérendeltje, amely opcionális statikus típusozást és más funkciókat ad a nyelvhez. Egyszerű JavaScriptre fordítódik, így kompatibilis a meglévő JavaScript kódbázisokkal.)

#### 2. What are the main benefits of using TypeScript over plain JavaScript?
Some main benefits of using TypeScript include better developer tooling, improved code maintainability, and catching errors at compile-time rather than runtime.

(A TypeScript használatának néhány fő előnye közé tartozik a jobb fejlesztői eszköztár, az javított kód karbantarthatóság és a hibák már fordítási időben történő felfedezése, nem pedig futási időben.)

#### 3. Explain the concept of static typing in TypeScript.
Static typing in TypeScript refers to the ability to explicitly declare variable types at compile-time, which helps catch type-related errors early in the development process.

(A TypeScript statikus típusozása arra utal, hogy a változók típusait nyilvánvalóan deklarálják a fordítás idején, amely segít a típushoz kapcsolódó hibák korai felfedezésében a fejlesztési folyamatban.)

#### 4. How do you declare variables with different types in TypeScript?
You can declare variables with different types in TypeScript using type annotations or type inference.Example with type annotations:
- Declaring a variable with a specific type: <br>
`let myNumber: number = 10;` <br>
`let myString: string = "Hello";` <br>
`let myBoolean: boolean = true;`

- Example with type inference: <br>
`let myNumber = 10;`       -> TypeScript infers myNumber to be of type number <br>
`let myString = "Hello";`  -> TypeScript infers myString to be of type string <br>
`let myBoolean = true;`    -> TypeScript infers myBoolean to be of type boolean <br>

TypeScript infers the type based on the value assigned

(A TypeScriptben különböző típusú változókat típus-annotációk vagy típusinferencia segítségével lehet deklarálni.)

#### 5. What are interfaces in TypeScript, and how are they used?
Interfaces in TypeScript define the shape of objects, specifying the properties and methods they should have. They are often used to enforce a contract between different parts of the codebase.

(Az interfészek a TypeScriptben meghatározzák az objektumok alakját, megadva a tulajdonságokat és a metódusokat, amelyekkel rendelkezniük kell. Gyakran használják arra, hogy egy szerződést érvényesítsenek a kód különböző részei között.)

#### 6. What is the difference between "null" and "undefined" in TypeScript?
In TypeScript, null represents the intentional absence of any object value, while undefined is used when a variable has been declared but not assigned a value. They are both types and can be assigned to variables explicitly.

(A TypeScriptben a null az objektum értékének szándékos hiányát jelenti, míg az undefined akkor használatos, amikor egy változó deklarált, de nem kapott értéket. Mindkettő típus és explicit módon hozzárendelhető változókhoz.)

#### 7. How does TypeScript support object-oriented programming (OOP) principles?
TypeScript supports OOP principles such as classes, interfaces, inheritance, encapsulation, and polymorphism. It allows developers to create structured and reusable code by organizing data and behavior into classes and interfaces.

(A TypeScript támogatja az objektumorientált programozási (OOP) elveket, mint például az osztályok, interfészek, öröklődés, inkapszuláció és polimorfizmus. Lehetővé teszi a fejlesztők számára a strukturált és újrafelhasználható kód létrehozását az adatok és viselkedések osztályokba és interfészekbe szervezésével.)

#### 8. What is the purpose of type annotations in TypeScript?
Type annotations in TypeScript are used to explicitly specify the type of a variable, function parameter, or function return value. They help catch type-related errors early in the development process and improve code readability and maintainability.

(A TypeScript típus-annotációit arra használják, hogy nyilvánvalóan meghatározzák egy változó, függvény paraméterének vagy függvény visszatérési értékének típusát. Segítenek a típushoz kapcsolódó hibák korai felfedezésében a fejlesztési folyamatban, és javítják a kód olvashatóságát és karbantarthatóságát.)

#### 9. How do you define arrays and tuples in TypeScript?
Arrays in TypeScript can be defined using square brackets notation, while tuples are arrays with a fixed number of elements where each element may have a different type.

(A TypeScript tömböket szögletes zárójellel definiálhatók, míg a tuple-k olyan tömbök, amelyeknek fix számú elemük van, ahol minden elem más típusú lehet.)

#### 10. Explain the difference between "interface" and "type" declarations in TypeScript.
In TypeScript, interfaces are mainly used for defining object shapes and contracts, while type declarations (often referred to as type aliases) can represent various data types, including primitive types, unions, and intersections.

(A TypeScriptben az interfészeket főként objektumalakzatok és szerződések meghatározására használják, míg a típusdeklarációk (gyakran típus-aliasokként hivatkoznak rájuk) különböző adattípusokat képviselhetnek, beleértve a primitív típusokat, uniókat és metszeteket.)

#### 11. What are generics in TypeScript, and why are they useful?
Generics in TypeScript allow you to create reusable components that can work with a variety of data types. They provide type safety while maintaining flexibility, enabling the creation of more versatile and robust code.

(A generikumok a TypeScriptben lehetővé teszik újrafelhasználható komponensek létrehozását, amelyek működhetnek különböző adattípusokkal. Biztosítják a típusbiztonságot, miközben megőrzik a rugalmasságot, lehetővé téve a sokoldalúbb és robosztusabb kód készítését.)

#### 12. How do you handle errors in TypeScript applications?
Errors in TypeScript applications can be handled using try-catch blocks, throwing custom errors, or utilizing TypeScript's built-in error handling mechanisms such as the throw keyword and Error class.

(A hibákat a TypeScript alkalmazásokban try-catch blokkokkal, egyedi hibák dobásával, vagy a TypeScript beépített hibakezelési mechanizmusainak, például a throw kulcsszó és az Error osztály használatával lehet kezelni.)

#### 13. Discuss the concept of type inference in TypeScript.
Type inference in TypeScript refers to the compiler's ability to automatically determine the data type of a variable based on its initialization value. This feature helps reduce the need for explicit type annotations and makes code more concise.

(A típusinferencia a TypeScriptben a fordító képességét jelenti arra, hogy automatikusan meghatározza egy változó adattípusát annak inicializációs értéke alapján. Ez a funkció csökkenti a szükségességet a nyilvánvaló típus-annotációkra, és a kódot tömörebbé teszi.)

#### 14. How do you compile TypeScript code into JavaScript?
TypeScript code can be compiled into JavaScript using the TypeScript compiler (tsc). You can run the compiler from the command line or integrate it into build tools like webpack or gulp. <br>
When you issue the `tsc` command (or `tsc filename.ts` command to compile a specific file), the TypeScript compiler begins to interpret and compile the specified TypeScript source files into JavaScript code. The process consists of the following steps:

- Parsing Files: The TypeScript compiler examines the provided source files and performs type checking to determine the types of variables, functions, classes, and other elements.
- Type Checking: The compiler verifies all parts of the code for type safety. This includes checking the compliance of data types and detecting type errors.
- Compilation: After successful type checking, the TypeScript source code is converted into JavaScript code. The conversion typically involves removing TypeScript-specific syntax elements, restructuring, and replacing them with JavaScript-specific language elements.
- Generating Output Files: The compiler writes the JavaScript code into one or more JavaScript files based on the resulting JavaScript code. By default, the output files are created in the same location as the source code, but this can be configured using the --outDir switch.
- Outputting Compilation Result: Finally, the compiler outputs the result of the process, including any errors or warnings encountered during compilation, to the console.

When using the `tsc --watch` command, the compiler watches the source files and recompiles them immediately whenever there is a modification. This allows developers to continuously track code changes and see their impact on the compiled JavaScript code instantly.

(A TypeScript kódot JavaScriptté lehet fordítani a TypeScript fordítóval (tsc). A fordítót futtathatod parancssorban, vagy integrálhatod build eszközökbe, mint például a webpack vagy gulp. <br>
Amikor kiadod a `tsc` parancsot (vagy `tsc filename.ts` parancsot egy konkrét fájl fordításához), a TypeScript fordító elkezdi értelmezni és fordítani a megadott TypeScript forrásfájlokat JavaScript kóddá. A folyamat a következő lépésekből áll:

- Fájl értelmezése: A TypeScript fordító megvizsgálja a megadott forrásfájlokat, és típusellenőrzést végez, hogy meghatározza a változók, függvények, osztályok és egyéb elemek típusait.
- Típusellenőrzés: A fordító ellenőrzi a kód összes részét a típusbiztonság érdekében. Ez magában foglalja az adattípusok megfelelőségének ellenőrzését és a típushibák felderítését.
- Fordítás: Miután sikeresen lefutott a típusellenőrzés, a TypeScript forráskód át lesz alakítva JavaScript kóddá. A kód konverziója általában a nyelvi szintaxis elemek eltávolítására, átstrukturálására és JavaScript-specifikus nyelvi elemekkel való helyettesítésére irányul.
- Kimeneti fájlok létrehozása: A fordító a JavaScript kódot egy vagy több JavaScript fájlba írja, amelyeket az eredményként kapott JavaScript kód alapján létrehoz. Az alapértelmezett beállítások szerint a kimeneti fájlok ugyanazon a helyen lesznek létrehozva, mint a forráskód, de ez konfigurálható a --outDir kapcsolóval.
- Fordítás eredményének kiírása: Végül a fordító a folyamat eredményét, beleértve a fordítás során fellépett hibákat vagy figyelmeztetéseket, kiírja a konzolra.
  
A `tsc --watch` parancs használata esetén a fordító figyeli a forrásfájlokat, és azonnal újrafordítja őket, amint módosítás történik bennük. Ez lehetővé teszi a fejlesztők számára, hogy folyamatosan nyomon kövessék a kódváltozásokat és azonnal lássák azok hatását a fordított JavaScript kódon.)

#### 15. What are some of the advanced features introduced in recent versions of TypeScript?
Recent versions of TypeScript have introduced several new and useful features that can assist developers in writing and maintaining code more effectively. These include:
- Optional Chaining (?.): Allows safe access to deeply nested object properties or methods, even if none of them are defined.
- Nullish Coalescing (??): Enables the explicit specification of a default value to be used only if the variable's value is null or undefined.
- Template Literal Types: Allow the definition of types based on template literal values, which can be useful for describing data types that must have specific, predetermined values.
- Assertion Functions: Functions that guarantee that the type of value they return matches what is specified in the type declaration. This can help in stronger type checking during coding.
- Improved Support for Decorators: Enhancements related to decorators, making it easier to use and manage decorators in code.
These new features enhance working with TypeScript code, improving codebase readability, maintainability, and performance, as well as enabling developers to work more efficiently during application development.

(- Opcionális láncolás (?.): Lehetővé teszi a biztonságos hozzáférést a mélyen beágyazott objektum tulajdonságaihoz vagy módszereihez, még akkor is, ha azok közül egyik sem definiált.
- Nullish coalescing (??): Segítségével egyértelműen megadható egy alapértelmezett érték, amely csak akkor kerül használatra, ha a változó értéke null vagy undefined.
- Sablon literál típusok: Lehetővé teszik a típusok definiálását sablon literál értékek alapján, ami hasznos lehet olyan adattípusok leírásához, amelyeknek konkrét, meghatározott értékekkel kell rendelkezniük.
- Állító függvények: Olyan függvények, amelyek garantálják, hogy az általuk visszaadott érték típusa egyezik azzal, amit a típusdeklarációban megadnak. Ez segíthet az erősebb típusellenőrzésben a kódolás során.
- Javított támogatás a dekorátorokhoz: A dekorátorokhoz kapcsolódó fejlesztések, amelyekkel könnyebbé válik a dekorátorok használata és kezelése a kódolás során.
Ezek az új funkciók javítják a TypeScript kóddal való munkát, növelik a kódbázis olvashatóságát, karbantarthatóságát és teljesítményét, valamint lehetővé teszik a fejlesztők számára, hogy hatékonyabban dolgozzanak az alkalmazások fejlesztése során.)
