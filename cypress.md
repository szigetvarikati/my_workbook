# Cypress questions

#### 1. What is Cypress, and how does it differ from other testing frameworks?
Cypress is a modern JavaScript end-to-end testing framework for web applications. Unlike traditional testing frameworks, Cypress operates directly within the browser and offers real-time feedback, automatic waiting, and easy debugging capabilities.
   
(A Cypress egy modern JavaScript alapú end-to-end tesztelő keretrendszer webalkalmazásokhoz. A hagyományos tesztelő keretrendszerekkel ellentétben a Cypress közvetlenül a böngészőben működik, valós idejű visszajelzést, automatikus várakozást és könnyű hibakeresési képességeket kínál.)


#### 2. What are some key features of Cypress?
Some key features of Cypress include automatic waiting, real-time reloading, and native access to every DOM element.

(A Cypress kulcsfontosságú jellemzői közé tartozik az automatikus várakozás, az azonnali újratöltés és a natív hozzáférés minden DOM elemhez.)


#### 3. How do you install Cypress and set up a new test project?
You can install Cypress via npm by running the command `npm install cypress`. After installation, you can set up a new test project by navigating to your project directory and running `npx cypress open` to initialize the Cypress directory structure.
   
(A Cypress telepítés: `npm install cypress`. A telepítés után új teszt projektet hozhatsz létre úgy, hogy a projekt mappájába navigálsz, majd futtatod a `npx cypress open` parancsot a Cypress könyvtár struktúrájának inicializálásához.)


#### 4. How do you locate elements on a webpage in Cypress tests?
Elements on a webpage in Cypress tests can be located using various methods, such as CSS selectors, custom data attributes, or Cypress-specific commands like `cy.get()` and `cy.contains()`.
   
(Az elemeket a Cypress tesztekben különböző módszerekkel lehet megtalálni, például CSS szelektorok, egyedi adat attribútumok vagy a Cypress specifikus parancsok, mint például a `cy.get()` és `cy.contains()` segítségével.)


#### 5. How does Cypress handle asynchronous operations in tests?
Cypress handles asynchronous operations using commands like `then()` or by using `await` for asynchronous functions.

(A Cypress az aszinkron műveleteket olyan parancsokkal kezeli, mint a `then()` vagy az `await` az aszinkron függvényekhez.)


#### 6. Can you explain the difference between "describe" and "it" in Cypress tests?
In Cypress tests, `describe` is used to group together related test cases, providing a way to organize and structure your tests. `it`, on the other hand, is used to define individual test cases within those groups.
   
(A Cypress tesztekben a `describe` az összefüggő tesztesetek csoportosítására szolgál, lehetővé téve a tesztek szervezését és strukturálását. `it` viszont az egyéni tesztesetek meghatározására szolgál ezekben a csoportokban.)


#### 7. What are aliases in Cypress, and why are they useful?
Aliases in Cypress are variables that hold references to DOM elements, routes, or responses. They are useful for storing and reusing commonly accessed elements or data in tests.
   
(Az aliasok a Cypress-ben változók, amelyek hivatkozásokat tartalmaznak a DOM elemekre, útvonalakra vagy válaszokra. Hasznosak a gyakran hozzáférhető elemek vagy adatok tárolásához és újrafelhasználásához a tesztekben.)


#### 8. Can you discuss the difference between "cy.get()" and "cy.contains()" in Cypress?
`cy.get()` is used to select elements based on CSS selectors or attributes, while `cy.contains()` is used to select elements based on their text content.
   
(A `cy.get()` az elemek kiválasztására szolgál CSS szelektorok vagy attribútumok alapján, míg a `cy.contains()` az elemek kiválasztására szolgál a szöveges tartalmuk alapján.)


#### 9. How do you simulate user interactions like clicks and keyboard inputs in Cypress tests?
User interactions like clicks and keyboard inputs can be simulated in Cypress tests using commands like `cy.click()` and `cy.type()`.

(A felhasználói interakciók, mint például a kattintások és a billentyűzetbevitel szimulálása a Cypress tesztekben a `cy.click()` és `cy.type()` parancsok segítségével történik.)


#### 10. What built-in assertion options are available in Cypress?
Cypress provides built-in assertion options such as the `should()` function, which allows formulating and verifying assertions.


#### 11. How can you confirm that an element is visible on the page in Cypress?
Using the 'should' command, for example: cy.get(selector).should('be.visible')


#### 12. What are the differences between cy.click() and cy.check() commands?
cy.check()
   - specifically designed for selecting or checking checkboxes.
   - used to set the state of a checkbox, and it automatically waits for the checkbox to appear and become checked.
   - reflects real user interaction when a user selects or checks a checkbox in the application.

cy.click()
   - more general and can be applied to any DOM element, not just checkboxes.
   - While the `click()` can be used on checkboxes, it may not necessarily reflect real user interaction since selecting a checkbox involves more factors (e.g., the current state of the checkbox).
   - does not wait for the post-click state to settle, so additional waiting steps need to be added to tests to ensure state changes.

Overall, the `check()` is a better choice for checkbox selection in Cypress tests as it is more precise and purpose-built for handling checkboxes. The `click()` is more general and versatile but less suited for specific tasks like selecting checkboxes.


#### 13. What is the purpose of the `cypress.config.js` file?
The `cypress.config.js` file is the Cypress configuration file, which allows customization of Cypress settings and configurations.

In a `cypress.config.js` file, you can define the following:

Environment configuration: You can configure settings related to different environments, such as development, testing, or production environments.
Browser configuration: You can specify which browser to use for running tests or configure multiple browsers.
Execution settings: You can set various parameters required for running tests, such as timeout values, wait times, etc.
Test data: You can define test data, such as fixtures or different configuration settings.
Configuration of plugins and extensions: Settings for Cypress plugins and extensions can also be placed in this file.

Overall, the `cypress.config.js` file allows customization of the Cypress test environment and easy management of various settings. This provides greater flexibility and easier maintenance during the testing process.


#### 14. How does the outcome of the `npx cypress run` command differ from the outcome of the `npx cypress open` command?
The `npx cypress run` command runs Cypress tests in the terminal without opening the Cypress Test Runner GUI. It executes tests headlessly in a background browser, logs the progress and results to the terminal, and exits with an appropriate status code. In contrast, the `npx cypress open` command launches the Cypress Test Runner GUI, allowing interactive test execution, selection of tests, and real-time feedback.

(A `npx cypress run` - terminalban futtat, egy háttérben lévő böngésző, naplózza a haladást és az eredményeket a terminálba, majd megfelelő státuszkóddal kilép, Ha failure-t talál screenshotot készít, illetve videót rögzít a tesztelésről.. Ezzel szemben a `npx cypress open` parancs elindítja a Cypress Test Runner GUI-t, lehetővé téve az interaktív tesztfuttatást, a tesztek kiválasztását és a valós idejű visszajelzést.)


#### 15. What is Cypress Studio for?
Cypress Studio is a feature of Cypress that facilitates the creation of Cypress tests through a visual, interactive interface. It allows testers and developers to record interactions with their web application and generate corresponding Cypress test code automatically.

With Cypress Studio:
Interactive Test Creation: Users can interact with their web application as they normally would, and Cypress Studio records these interactions, such as clicks, form submissions, or keyboard inputs.
Automatic Test Code Generation: As interactions are recorded, Cypress Studio generates Cypress test code in the background, representing the actions performed during the recording session.
Test Script Customization: Users have the flexibility to customize and edit the generated test code within Cypress Studio. This enables fine-tuning of tests and adding assertions or additional commands as needed.
Visual Feedback: Cypress Studio provides visual feedback during test creation, highlighting the elements being interacted with and allowing users to easily identify the steps recorded.

Overall, Cypress Studio streamlines the process of creating Cypress tests, particularly for users who prefer a more visual approach or who are new to writing test code. It promotes faster test creation and easier test maintenance by automating much of the test code generation process.

(Lehetővé teszi a Cypress tesztek létrehozását egy vizuális, interaktív felületen keresztül. Segítségével a tesztelők és fejlesztők rögzíthetik az interakcióikat a webalkalmazásukkal, és automatikusan generálhatják a megfelelő Cypress teszkódot.
Interaktív tesztkészítés: A felhasználók kölcsönhatásba léphetnek a webalkalmazásukkal, ahogyan általában tennék, és a Cypress Studio rögzíti ezeket az interakciókat, például kattintásokat, űrlapok beküldéseit vagy billentyűleütéseket.
Automatikus teszkódgenerálás: Ahogyan rögzítik az interakciókat, a Cypress Studio automatikusan generálja a Cypress teszkódot a háttérben, amely tükrözi a felvett műveleteket.
Tesztkód testreszabása: A felhasználóknak lehetőségük van testre szabni és szerkeszteni a generált teszkódot a Cypress Studio-ban. Ez lehetővé teszi a tesztek finomhangolását, és hozzáadhatnak állításokat vagy további parancsokat szükség szerint.
Vizuális visszajelzés: A Cypress Studio vizuális visszajelzést nyújt a tesztkészítés során, kiemelve az interakciók során érintett elemeket, így könnyen azonosíthatók a felvett lépések.)

#### 16. How does chaining in Cypress contribute to the readability and maintainability of test code compared to non-chained approaches?
Chaining in Cypress offers several advantages:
Expressive Test Code: Chaining allows for writing clear and expressive test code. Operations can be sequenced together, resulting in code that is easy to follow and understand.
Simplicity: Chaining makes it easy to list different operations in sequence, reducing redundancy and making the test code more readable.
Continuous Execution: Cypress commands run asynchronously, and chaining enables the automatic continuation of the next command once the previous one completes. This facilitates seamless execution in tests.
Additional Checks and Operations: Chaining enables checking the results of individual operations and appending further checks or operations to the chaining sequence. This helps in making tests more detailed and robust.
Consistency and Continuity: Through chaining, test code can consistently and continuously follow the process or interface being tested, contributing to the stability and reliability of tests.

In summary, chaining in Cypress allows for more efficient and expressive test code, making tests easier to maintain and scale.

(A láncolás (chaining) használata a Cypress-ben számos előnnyel jár:
Kifejező tesztkód: A láncolás lehetővé teszi a tiszta és kifejező tesztkód írását, mivel az egyes műveleteket egymásra fűzve lehet leírni, ami könnyen követhető és érthető kódot eredményez.
Egyszerű kezelés: A láncolásnak köszönhetően a különböző műveletek egyszerűen sorolhatók fel, és a tesztkód kevésbé lesz redundáns és átláthatóbb.
Folyamatos végrehajtás: A Cypress parancsok aszinkron módon futnak, és a láncolás lehetővé teszi, hogy az egyik parancs végrehajtását követően automatikusan folytassuk a következő parancsot, amint az előző befejeződött. Ez lehetővé teszi a folyamatos működést a tesztekben.
További ellenőrzések és műveletek: A láncolás lehetővé teszi az egyes műveletek eredményének ellenőrzését, és az ellenőrzések vagy további műveletek hozzáfűzését a láncolási sorozathoz. Ez segít abban, hogy a tesztek részletesebbek legyenek és jobban ellenőrizhetők legyenek.
Folyamatosság és konzisztencia: A láncolás révén a tesztkód folytonosan és konzisztensen követheti a tesztelendő folyamatot vagy felületet, ami segít a tesztek stabilitásának és megbízhatóságának növelésében.

Összességében a láncolás (chaining) lehetővé teszi a hatékonyabb és kifejezőbb tesztkód írását a Cypress-ben, ami segít abban, hogy a tesztek könnyebben karbantarthatók és skálázhatók legyenek.)

#### 17. What is the Cypress Dashboard, and why is it useful for teams?
The Cypress Dashboard is a cloud-based service provided by Cypress.io that offers various features for managing and analyzing test runs. It provides a centralized platform for teams to view test results, analyze test performance, track historical trends, and collaborate on testing efforts. The Dashboard allows teams to gain insights into test execution across different environments and configurations, facilitating faster debugging and improving overall test efficiency.

(A Cypress Dashboard egy a Cypress.io által nyújtott felhőalapú szolgáltatás, amely különböző funkciókat kínál a tesztfutások kezeléséhez és elemzéséhez. Központi platformot biztosít a csapatoknak a teszteredmények megtekintéséhez, a teszt teljesítményének elemzéséhez, a történelmi trendek nyomon követéséhez és a tesztelési erőfeszítések együttműködéséhez. A Dashboard lehetővé teszi a csapatok számára, hogy betekintést nyerjenek a tesztek végrehajtásába különböző környezetekben és konfigurációkban, segítve ezzel a gyors hibakeresést és az általános teszt hatékonyságának javítását.)

#### 18. Can you explain the concept of "time travel" in Cypress, and how does it enhance testing capabilities?
"Time travel" in Cypress refers to the ability to control and manipulate time within tests. Cypress allows testers to freeze, advance, or control the system clock during test execution, enabling scenarios such as testing time-sensitive features, handling animations, or simulating delays in asynchronous operations. This feature enhances testing capabilities by providing more control over timing-related scenarios, ensuring accurate and reliable testing results.

(A "time travel" a Cypress-ben a tesztek során az idő vezérlésének és manipulálásának képességét jelenti. A Cypress lehetővé teszi a tesztelők számára, hogy befagyasszák, előre vagy irányítsák a rendszerórát a tesztfuttatás során, lehetővé téve olyan forgatókönyveket, mint például időérzékeny funkciók tesztelése, animációk kezelése vagy késleltetések szimulálása aszinkron műveletek során. Ez a funkció javítja a tesztelési képességeket azzal, hogy nagyobb kontrollt biztosít az idővel kapcsolatos forgatókönyvek felett, pontos és megbízható teszteredményeket biztosítva.)

#### 19. How does Cypress handle cross-browser testing, and what are its limitations in this regard?
Cypress primarily focuses on testing within a single browser environment, typically Chrome. While it offers limited support for running tests in other browsers via third-party plugins or Docker containers, Cypress is optimized for Chrome and may not fully replicate the behavior of tests in other browsers. Therefore, its cross-browser testing capabilities are more limited compared to other frameworks like Selenium WebDriver, which natively supports testing across multiple browsers.

(A Cypress főként egyetlen böngészőkörnyezetre, általában a Chrome-ra koncentrál. Bár korlátozott támogatást nyújt a tesztek futtatásához más böngészőkben harmadik féltől származó pluginek vagy Docker konténerek segítségével, a Cypress a Chrome-ra van optimalizálva, és esetleg nem teljesen replikálja a tesztek viselkedését más böngészőkben. Ezért a böngészők közti tesztelési képességei korlátozottabbak a Cypress esetében más keretrendszerekhez képest, mint például a Selenium WebDriver, amely natívan támogatja a tesztelést több böngészőben.)

#### 20. What are custom commands in Cypress, and how can they improve test code readability and maintainability?
Custom commands in Cypress are user-defined functions that encapsulate sequences of Cypress commands for reusability and abstraction. They allow testers to create domain-specific abstractions, reduce code duplication, and improve test code readability by expressing test actions in a more concise and descriptive manner. Additionally, custom commands promote maintainability by centralizing common functionalities, making it easier to update and refactor tests as needed.

(A szokásos parancsok a Cypress-ben olyan felhasználó által definiált funkciók, amelyek összefoglalják a Cypress parancsok sorozatát újrafelhasználhatóság és absztrakció céljából. Lehetővé teszik a tesztelők számára, hogy létrehozzanak domain-specifikus absztrakciókat, csökkentsék a kódkettőzést és javítsák a tesztkód olvashatóságát, kifejezve a tesztműveleteket egy áttekinthetőbb és leíróbb módon. Ezenkívül a szokásos parancsok segítik a karbantarthatóságot azáltal, hogy központosítják a közös funkcionalitásokat, ami megkönnyíti a tesztek frissítését és refaktorálását szükség esetén.)

#### 21. Describe the role of plugins in Cypress, and provide examples of popular Cypress plugins and their functionalities.
Plugins in Cypress extend its functionality by integrating additional features, custom commands, or third-party tools into the testing workflow. They can enhance test capabilities, improve reporting, or integrate with other services for better test management. Examples of popular Cypress plugins include Cypress Testing Library for enhanced DOM querying, Cypress Axe for accessibility testing, and Cypress File Upload for handling file uploads in tests.

(A pluginek a Cypress funkcióinak kiterjesztését szolgálják, további funkciók, szokásos parancsok vagy harmadik féltől származó eszközök integrálásával a tesztelési folyamatba. Növelhetik a tesztek képességeit, javíthatják a jelentést, vagy integrálhatnak más szolgáltatásokkal a jobb tesztkezelés érdekében. Néhány példa népszerű Cypress pluginekre a Cypress Testing Library, ami lehetővé teszi az átfogóbb DOM lekérdezéseket, a Cypress Axe, ami az akadálymentesség tesztelését segíti, és a Cypress File Upload, ami a fájlok feltöltésének kezelését teszi lehetővé a tesztekben.)

#### 22. What is the Cypress Test Runner, and how does it assist in the test development process?
The Cypress Test Runner is a graphical user interface provided by Cypress for writing, running, and debugging tests. It offers features such as real-time test execution, interactive debugging tools, automatic reloading of tests, and detailed test output with screenshots and videos. The Test Runner assists in the test development process by providing a user-friendly interface for authoring tests, executing them in different environments, and debugging failures efficiently.

(A Cypress Test Runner a Cypress által nyújtott grafikus felhasználói felület a tesztek írásához, futtatásához és hibakereséséhez. Olyan funkciókat kínál, mint például a valós idejű tesztfuttatás, az interaktív hibakereső eszközök, a tesztek automatikus újratöltése és a részletes tesztkimenetek képernyőképekkel és videókkal. A Test Runner segíti a tesztek fejlesztési folyamatát azzal, hogy felhasználóbarát felületet biztosít a tesztek írásához, különböző környezetekben való futtatásukhoz és a hibák hatékony hibakereséséhez.)

#### 23. How does Cypress support test parallelization, and what are the benefits of parallel test execution?
Cypress supports test parallelization by allowing tests to run concurrently across multiple instances or containers. Test parallelization improves testing efficiency by reducing overall test execution time, enabling faster feedback loops, and maximizing resource utilization. It helps teams achieve faster test runs, scalable testing infrastructure, and improved test coverage, especially in continuous integration and delivery pipelines.

(A Cypress támogatja a tesztpárhuzamosítást azzal, hogy lehetővé teszi a tesztek egyidejű futtatását több példányban vagy konténerben. A tesztpárhuzamosítás javítja a tesztelés hatékonyságát azzal, hogy csökkenti az összes tesztfuttatási időt, lehetővé teszi a gyorsabb visszajelzést és maximalizálja az erőforrások kihasználtságát. Segít a csapatoknak gyorsabb tesztfuttatásokat elérni, skálázható tesztinfrastruktúrát és jobb tesztlefedettséget, különösen a folyamatos integráció és szállítás (CI/CD) csövekre.)

#### 24. Discuss the concept of "cy.route()" in Cypress and its significance in mocking network requests during tests.
"cy.route()" in Cypress is a command used to intercept and stub network requests made by the application under test. It allows testers to mock server responses, simulate network conditions, and control the behavior of external dependencies during tests. By intercepting network traffic, "cy.route()" enables precise control over API responses, facilitates testing of error handling scenarios, and reduces reliance on external services, leading to more deterministic and reliable tests.

(A "cy.route()" a Cypress-ben egy parancs, amelyet a teszt alatt álló alkalmazás által készített hálózati kérések elfogására és helyettesítésére használnak. Lehetővé teszi a tesztelők számára, hogy hamisítják a szerver válaszokat, szimulálják a hálózati feltételeket, és irányítsák a külső függőségek viselkedését a tesztek során. A hálózati forgalom elfogásával a "cy.route()" precíz irányítást biztosít az API válaszok felett, megkönnyíti a hibakezelési forgatókönyvek tesztelését, és csökkenti az külső szolgáltatások iránti függőséget, ami megbízhatóbb és megbízhatóbb teszteredményekhez vezet.)

#### 25. Explain the purpose of the "before", "beforeEach", "after", and "afterEach" hooks in Cypress, and when would you use them?
These hooks are used for setting up and tearing down test fixtures and environment state before and after test suites and individual tests. "before" and "after" hooks are executed once before and after the entire test suite, respectively, while "beforeEach" and "afterEach" hooks run before and after each test case within the suite. They are commonly used for tasks such as initializing test data, starting and stopping servers, or cleaning up resources to ensure a consistent test environment.

(Ezeket a hookokat a tesztesetek és a tesztfuttatók előtti és utáni tesztelési eszközök és környezeti állapot felállítására és lerombolására használják. A "before" és "after" hookok egyszer futnak le a teljes tesztelési sorozat előtt és után, míg a "beforeEach" és "afterEach" hookok a teljes tesztkészleten belül minden egyes teszteset előtt és után futnak. Gyakran használják olyan feladatokhoz, mint a tesztadatok inicializálása, szerverek indítása és leállítása, vagy erőforrások tisztítása annak érdekében, hogy egy következetes tesztelési környezetet biztosítsanak.)

#### 26. Compare Cypress and Selenium in terms of speed, ease of use, and test reliability, highlighting the advantages and disadvantages of each testing framework.
Cypress is known for its speed, as it operates directly within the browser and executes tests asynchronously, resulting in fast and reliable test runs. Its simple and intuitive API makes it easy to write and maintain tests, while features like automatic waiting and real-time reload provide instant feedback during test development. However, Cypress is limited to testing web applications and primarily supports Chrome, with limited cross-browser testing capabilities.Selenium, on the other hand, is a more versatile testing framework that supports multiple programming languages and browsers, making it suitable for testing a wide range of web and mobile applications. It offers extensive cross-browser testing capabilities and integrates with various testing frameworks and tools. However, Selenium tests can be slower due to the use of WebDriver protocols, and setting up Selenium environments and handling asynchronous operations may require more effort compared to Cypress. Additionally, Selenium tests may be more prone to flakiness and maintenance issues due to its reliance on external factors and the complexities of interacting with the browser.

(A Cypress gyorsaságáról ismert, mivel közvetlenül a böngészőben működik, és aszinkron módon futtatja a teszteket, gyors és megbízható tesztfuttatásokat eredményezve. Egyszerű és intuitív API-jának köszönhetően könnyű írni és karbantartani a teszteket, míg az automatikus várakozás és a valós idejű újratöltés funkciók gyors visszajelzést biztosítanak a tesztfejlesztés során. Azonban a Cypress csak webalkalmazások tesztelésére korlátozódik, és elsősorban a Chrome-ot támogatja, korlátozott böngészők közti tesztelési képességekkel.A Selenium viszont sokoldalúbb tesztelési keretrendszer, amely több programozási nyelvet és böngészőt támogat. Ez lehetővé teszi a többplatformos tesztelést, a mobilalkalmazások tesztelését és a felhasználói felületek integrált tesztelését. Bár a Selenium erősebb a böngészők közti tesztelés terén, az aszinkron műveletek kezelése és a várakozási mechanizmusok kezelése nehezebb lehet a fejlesztők számára. Emellett a Selenium tesztek lassabbak lehetnek a Cypress tesztekhez képest, mivel a WebDriver távoli vezérlést használ, és a tesztek instabilabbak lehetnek a különböző böngészők és környezetek közötti összehasonlítás miatt.)

#### 27. What are the bacis commands in Cypress?
- cy.visit(): This command loads a URL in the browser to start the test on a specific website.
- cy.get(): Helps select elements in the DOM based on unique identifiers, classes, or other selectors.
- cy.contains(): Selects elements based on whether they contain a specific text.
- cy.click(): Simulates a click on a specific element in the browser.
- cy.type(): Simulates keyboard input into a specific input field or text box.
- cy.url(): Returns the currently loaded URL in the browser.
- cy.wait(): Aids in waiting for a specific event or condition to occur during the test process.
- cy.should(): Allows you to assert various conditions, such as whether a specific element is visible or contains the expected text.
- cy.intercept(): Enables you to intercept and manipulate network requests during tests.

(
- cy.visit(): Ezzel a parancsalapú paranccsal betölthetsz egy URL-t a böngészőben, hogy elindítsd a tesztet az adott webhelyen.
- cy.get(): Ez a parancs segít az elemek kiválasztásában a DOM-ban, például az egyedi azonosítók, osztályok vagy egyéb szelektorok alapján.
- cy.contains(): Segít az elemek kiválasztásában az alapján, hogy tartalmazzák-e egy adott szövegrészt.
- cy.click(): Ez a parancs szimulálja a kattintást egy adott elemre a böngészőben.
- cy.type(): Használd ezt a parancsot a billentyűleütések szimulálásához egy adott inputmezőbe vagy szövegdobozba.
- cy.url(): Visszaadja a böngészőben jelenleg betöltött URL-t.
- cy.wait(): Segít várakozni egy adott eseményre vagy feltétel teljesülésére a tesztfolyamat során.
- cy.should(): A should parancs segítségével különböző feltételeket ellenőrizhetsz, például hogy egy adott elem látható-e, vagy megfelelő szöveget tartalmaz-e.
- cy.intercept(): Ezzel a paranccsal lehetőséged van a hálózati kérések elfogására és manipulálására a tesztek során.)

