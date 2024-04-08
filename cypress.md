# Cypress questions

#### 1. What is Cypress, and how does it differ from other testing frameworks?
Cypress is a modern JavaScript end-to-end testing framework for web applications. Unlike traditional testing frameworks, Cypress operates directly within the browser and offers real-time feedback, automatic waiting, and easy debugging capabilities.
   
(A Cypress egy modern JavaScript alapú end-to-end tesztelő keretrendszer webalkalmazásokhoz. A hagyományos tesztelő keretrendszerekkel ellentétben a Cypress közvetlenül a böngészőben működik, valós idejű visszajelzést, automatikus várakozást és könnyű hibakeresési képességeket kínál.)


#### 2. What are some key features of Cypress?
Some key features of Cypress include automatic waiting, real-time reloading, and native access to every DOM element.

A Cypress kulcsfontosságú jellemzői közé tartozik az automatikus várakozás, az azonnali újratöltés és a natív hozzáférés minden DOM elemhez.


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






