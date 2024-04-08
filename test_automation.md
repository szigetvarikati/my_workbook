# Test Automation Workbook

## Testing Basics

#### 1. Why is quality assurance important?
Quality assurance is vital as it ensures the delivery of a high-quality product, meeting or exceeding customer expectations. By systematically monitoring and evaluating the development process, quality assurance helps in identifying and rectifying defects early on, reducing the need for extensive rework and preventing costly issues in later stages of development. Moreover, it plays a significant role in maintaining the reputation of the company by delivering reliable products consistently, thus fostering customer trust and loyalty.

#### 2. What is the purpose of testing? What is not?
The purpose of testing is multifaceted. It aims to provide information about the product's status, functionality, and compliance with requirements. Testing helps in identifying defects, weaknesses, and discrepancies between the expected and actual behavior of the product. It serves as a mechanism to assess the quality of the product and its readiness for release, acting as a critical feedback loop for developers and stakeholders.

However, it's important to understand what testing is not. Testing cannot guarantee the absence of all bugs or defects, as it's practically impossible to test every conceivable scenario comprehensively. Rather, testing provides a snapshot of the product's state at a given point in time, highlighting areas that need improvement or further investigation. Testers don't make the final decision on whether a product can be released; instead, they provide insights and recommendations based on their findings.

Testing also shouldn't be seen as a standalone activity but rather integrated throughout the software development lifecycle. It's not merely a box-ticking exercise but a continuous process aimed at ensuring the product meets quality standards and user expectations. Ultimately, testing serves as a crucial tool in mitigating risks, enhancing product quality, and fostering confidence in the software being developed.

(Információt szerezzünk a szoftver aktuális állapotának minőségéről.
Nem célja, hogy az összes hibát megtalálja, ez nem is lehetséges. Olyan a tesztelés, mint egy jelzőlámpa, információt ad neked a projekt állapotáról, minőségéről és ezáltal egy magabiztosságot tudsz szerezni. Ennek alapján azt tudod mondani, hogy ez jó minőségű, vagy rossz minőségű. Ha rossz minőségű, még akkor is release-elhetsz, de legalább tudod, hogy mire számíts. Ez az információ a legnagyobb érték.
Specifikációhoz viszonyítás: a tesztben azt ellenőrizzük le, hogy az ügyfél valóban azt kapja-e, amit kért.)

#### 3. What is verification and why is it important?
Verification is the process of ensuring that the software product or system meets specified requirements and standards. It involves reviewing documents, design, code, and other artifacts to check whether they adhere to the established criteria and whether they accurately represent the intended functionality. Verification focuses on confirming that the software is being built correctly according to the requirements and design specifications.

Verification is crucial in the software development process for several reasons:
1. **Early Detection of Issues**: By verifying requirements and designs early in the development cycle, potential issues can be identified and addressed before significant resources are invested in implementation.
2. **Cost-Effectiveness**: Detecting and fixing defects during the early stages of development is typically less costly than addressing them later in the process or after deployment.
3. **Risk Mitigation**: Verifying that the software conforms to requirements helps mitigate the risk of delivering a product that does not meet user expectations or regulatory standards.
4. **Quality Assurance**: Verification contributes to the overall quality assurance process by ensuring that each stage of development meets predetermined standards and specifications.
5. **Customer Satisfaction**: Delivering a product that has been thoroughly verified increases customer satisfaction by providing a reliable and functional solution that meets their needs.

In summary, verification is essential for ensuring that software products are developed correctly, according to specified requirements and standards, ultimately leading to higher quality, reduced costs, and increased customer satisfaction.

(Termékelemzésről, tervezésről és egyéb dokumentumokról van szó, amelyek célja, hogy ellenőrizzék, hogy azok megfelelnek-e a meghatározott követelményeknek és szabványoknak. A verifikáció arra összpontosít, hogy megerősítse, a szoftver megfelelően van-e felépítve a követelményeknek és a tervezési specifikációknak megfelelően.

A verifikáció számos okból fontos a szoftverfejlesztési folyamatban:
1. **Korai problémák észlelése**: A követelmények és tervek korai ellenőrzése lehetővé teszi a potenciális problémák azonosítását és kezelését még az implementáció jelentős erőforrásainak befektetése előtt.
2. **Költséghatékonyság**: A hibák azonosítása és javítása a fejlesztés korai szakaszaiban általában kevesebb költséggel jár, mint azoknak a későbbi szakaszokban vagy a telepítés után történő kezelése.
3. **Kockázatcsökkentés**: A szoftver megfelelőségének ellenőrzése a követelményekhez segít csökkenteni annak a kockázatát, hogy olyan terméket szállítsanak, amely nem felel meg a felhasználói elvárásoknak vagy a szabályozási szabványoknak.
4. **Minőségellenőrzés**: A verifikáció hozzájárul az általános minőségellenőrzési folyamathoz azzal, hogy biztosítja, hogy minden fejlesztési szakasz megfelel a meghatározott szabványoknak és követelményeknek.
5. **Ügyfél elégedettsége**: Az alaposan ellenőrzött termék szállítása növeli az ügyfél elégedettségét, mivel megbízható és funkcionális megoldást nyújt, amely megfelel az igényeiknek.

Összefoglalva, a verifikáció fontos azért, hogy biztosítsa, hogy a szoftvertermékek megfelelően legyenek kifejlesztve a meghatározott követelményeknek és szabványoknak megfelelően, ami végül magasabb minőséget, alacsonyabb költségeket és növekvő ügyfélelégedettséget eredményez.)

#### 4. What is validation and why is it important?
Validation involves checking whether the software meets real-world conditions and requirements. It goes beyond verifying that the software has been developed correctly according to specified requirements (which is part of verification) and ensures that it meets user needs and expectations in actual usage scenarios.

Validation is important in the software development process for several reasons:
1. **User Satisfaction**: Validation helps ensure that the final software product truly meets the needs and expectations of users. This increases customer satisfaction and loyalty.
2. **Security and Reliability**: Validation verifies whether the software operates safely and reliably in real-world conditions and complies with regulatory requirements and laws.
3. **Requirement Fulfillment**: Validation confirms that the software indeed meets the original business requirements and objectives and performs adequately in real-world usage.
4. **Product Quality**: Validation contributes to enhancing product quality and identifying any deficiencies or issues early on, before the software is fully deployed.
5. **Business Success**: Successful validation increases the likelihood of the developed software performing well in the market, thereby increasing business success and competitiveness.

Overall, validation is an essential step in the software development process to ensure that the final software product truly meets the real needs and expectations of users, contributing to customer satisfaction and product success.

(Validáció során azt vizsgáljuk, hogy a szoftver megfelel-e a valós világban használatos körülményeknek és elvárásoknak. Ez azt jelenti, hogy nemcsak az ellenőrizzük, hogy a szoftver helyesen lett-e kifejlesztve a megadott követelmények szerint (ami a verifikáció része), hanem azt is, hogy valós környezetben is megfelel-e a felhasználói igényeknek és elvárásoknak.

A validáció fontos a szoftverfejlesztési folyamatban több okból is:
1. **Felhasználói elégedettség**: A validáció segít biztosítani, hogy a kész szoftver valóban megfeleljen a felhasználók igényeinek és elvárásainak. Ezáltal növeli az ügyfél elégedettségét és hűségét.
2. **Biztonság és megbízhatóság**: A validáció során ellenőrizhető, hogy a szoftver biztonságosan és megbízhatóan működik-e valós körülmények között, és megfelel-e az esetleges szabályozási előírásoknak és jogszabályoknak.
3. **Követelmények teljesülése**: A validáció segít megerősíteni, hogy a szoftver valóban megfelel-e az eredeti üzleti követelményeknek és céloknak, és hogy valós használatban is megfelelően teljesít.
4. **Termékminőség**: A validáció hozzájárul a termék minőségének növeléséhez és az esetleges hiányosságok vagy problémák korai azonosításához, mielőtt a szoftvert teljes körűen üzembe helyeznék.
5. **Üzleti siker**: A sikeres validáció eredményeként a fejlesztett szoftver valószínűleg jobban teljesíti a piacon, növelve az üzleti siker esélyeit és a versenyképességet.

Összességében a validáció elengedhetetlen lépés a szoftverfejlesztési folyamatban annak biztosítására, hogy a kész szoftver valóban megfeleljen a felhasználók valós igényeinek és elvárásainak, ami hozzájárul az ügyfélelégedettséghez és a termék sikeréhez.)

#### 5. How can tests be categorized? Explain classifications and the categories within them.
Tests can be categorized in several ways based on various criteria. Here are some common classifications:

1. **Based on Testing Objective:**
   - **Functional Testing:** This type of testing focuses on verifying that the software functions correctly according to specified requirements. It involves testing the behavior of individual functions or features of the software.
   - **Non-Functional Testing:** Non-functional testing evaluates aspects such as performance, usability, reliability, and security of the software rather than its specific features or functionality.

2. **Based on Testing Scope:**
   - **Unit Testing:** Unit tests verify the functionality of individual components or units of code in isolation from the rest of the system.
   - **Integration Testing:** Integration tests verify the interaction and compatibility between different components or modules of the software to ensure they work together as expected.
   - **System Testing:** System tests evaluate the entire software system as a whole to verify that it meets specified requirements and functions correctly in its intended environment.

3. **Based on Testing Methodology:**
   - **Manual Testing:** Manual testing involves executing test cases and evaluating the software's behavior manually without the use of automated tools.
   - **Automated Testing:** Automated testing involves using software tools to execute test cases and compare actual outcomes with expected outcomes automatically. This includes various types of automated testing such as unit testing, regression testing, and performance testing.

4. **Based on Test Design Techniques:**
   - **Black Box Testing:** Black box testing focuses on testing the software's functionality without knowledge of its internal implementation. Testers only interact with the software through its user interface or APIs.
   - **White Box Testing:** White box testing involves testing the internal logic, structure, and code of the software. Testers have access to the source code and design specifications to create test cases based on the software's internal workings.
   - **Grey Box Testing:** Grey box testing combines elements of both black box and white box testing. Testers have partial knowledge of the internal workings of the software, allowing them to design more comprehensive test cases.

These categories provide a framework for organizing and understanding different types of tests and their purposes within the software development lifecycle. Depending on the project requirements and objectives, testers may use one or more of these categories to ensure thorough testing coverage and quality assurance.

(A teszteket több szempont alapján is kategorizálhatjuk. Íme néhány gyakori besorolás:

1. **Tesztelési cél alapján:**
   - **Funkcionális tesztelés:** Ez a tesztelési típus arra összpontosít, hogy ellenőrizze, hogy a szoftver megfelelően működik-e a meghatározott követelmények szerint. Az egyes funkciók vagy szoftveregységek viselkedését vizsgálja.
   - **Nem-funkcionális tesztelés:** A nem-funkcionális tesztelés olyan szempontokat értékel, mint a teljesítmény, a felhasználói barátságosság, az elérhetőség és a biztonság, nem pedig a konkrét funkciók vagy működési jellemzők ellenőrzésére összpontosít.

2. **Tesztelési kiterjedés alapján:**
   - **Egységtesztelés:** Az egységtesztek az egyes kódmodulok vagy komponensek működését ellenőrzik elkülönülten a rendszer többi részétől.
   - **Integrációs tesztelés:** Az integrációs tesztek az egyes szoftverkomponensek vagy modulok közötti interakciót és kompatibilitást vizsgálják, hogy meggyőződjenek arról, hogy azok együtt megfelelően működnek-e.
   - **Rendszertesztelés:** A rendszertesztek a teljes szoftverrendszert egészében vizsgálják annak érdekében, hogy megállapítsák, hogy az megfelel-e a meghatározott követelményeknek és helyesen működik-e a szándékozott környezetben.

3. **Tesztelési módszertan alapján:**
   - **Manuális tesztelés:** A manuális tesztelés során a tesztkészleteket manuálisan hajtják végre, és értékelik a szoftver viselkedését automatizált eszközök használata nélkül.
   - **Automatizált tesztelés:** Az automatizált tesztelés során szoftvereszközöket használnak a tesztesetek végrehajtásához, és az aktuális eredményeket automatikusan összehasonlítják az elvárt eredményekkel.

4. **Tesztkonstrukciós technikák alapján:**
   - **Fekete dobozos tesztelés:** A fekete dobozos tesztelés a szoftver funkcionalitását vizsgálja anélkül, hogy ismernénk annak belső működését vagy implementációját.
   - **Fejlett tesztelés:** A fejlett tesztelés a szoftver belső logikáját, szerkezetét és kódját vizsgálja. A tesztelőknek hozzáférésük van a forráskódhoz és a tervezési specifikációkhoz.
   - **Szürke dobozos tesztelés:** A szürke dobozos tesztelés elemeket kombinál a fekete dobozos és a fehér dobozos tesztelésből. A tesztelők részleges ismerettel rendelkeznek a szoftver belső működéséről.

Ezek a kategóriák keretet nyújtanak a különböző teszttípusok szervezéséhez és megértéséhez, valamint azok céljainak a szoftverfejlesztési életciklusban betöltött szerepének megértéséhez. A projekt követelményeitől és célkitűzéseitől függően a tesztelők az egyes kategóriákat használhatják vagy kombinálhatják annak érdekében, hogy alapos tesztelési lefedettséget és minőségbiztosítást érjenek el.)

#### 6. What is unit testing? Who is responsible to write unit tests?
Unit testing is a fundamental testing methodology in software development, where developers test their code in isolation. Its purpose is to verify the correct operation of individual code units, such as functions or methods. Unit tests run automatically and are often integrated into the developer workflow. Unit testing aids in the early detection and resolution of defects, improves code quality and maintainability, and enhances team and developer confidence in the software's quality.

(A fejlesztő feladata a unit test, ez egy exit criteria, hogy jól végezte-e el a feladatát, tudja-e az adott unit, amit elvárnak tőle. Ő ismeri a legjobban a saját kódját és ezért időhatékonyabb, ha ő teszteli a saját kódját. Mondhatni ez early testing, mert már azelőtt teszteléssel foglalkozik a fejlesztő, mielőtt a tesztelőkhöz eljut. Onnantól kezdve ezek a unit testek megmaradnak örökre, minden futtatási flowban érdemes őket lefuttatni. Csak akkor lehet nekiállni refaktorálni, ha unit testekkel le van fedve a kód, hogy biztosítsuk, hogy nem törik el sehol a kód. A fejlesztők nem nagyon tanulnak tesztelni, így nem feltétlenül tökéletes minőségűek a unit tesztek. Megkérhetnek minket, h írjunk unit testeket, de ez nem jó ár-érték arányú dolog, mert meg kell ismernünk előbb a kódot és jobban megéri, ha mindenki a saját maga által írt kódot teszteli.)

#### 7. What is the difference between white box, grey boy and black box testing?
**White-box**: unit testing responsible for the developers; know the codebase
**Black-box**: have specificaiton, check the working of the code (without knowing the codebase), simulate the user flows
**Grey-box**: mixture of white box and black box testing, you can have a look on the codebase, but you hanlde the testing like a blackbox testing, you can see the weaknesses int the codebase, so you can test easier and effectivelier the product

#### 8. Compare the Waterfall and Agile project management models from testing perspective!
Waterfall: lineáris, egymásra épülnek a lépések, az nem jó benne, hogy a tesztelés a fejlesztést követően 8 hónap-2 éven belül kaphatja meg az első dolgot, amit tesztelni tud
V-modell: ugyanúgy lineáris, eltart sokáig, míg a tervezéstől a megvalósításig eljutnak, de minden egyes fázishoz tartozik egy tesztelési szint is (főleg autóiparban csinálják még így, ahol az Agile nem annyira jött be pl. az ISO szabványok miatt muszáj minden lépést layerenként letesztelni)
Agile: van Kanban és SCRUM
Kanban: balról jönnek be a feladatok, nagyjából prioritási sorrendben és a csapatból az első ember, aki felszabadul, leveszi az oszlop tetején lévő dolgot és elkezdi csinálni
az in progressre van egy limitáció, mondjuk max. 7 lehet benne és ha ezt elérte a csapat, akkor odamennek segíteni egymásnak a csapattagok, addig nem mennek tovább, amíg az kész nincs
SCRUM: iterációkra bontott, csomó procedúrával járó módszertan, ez most a legelterjedtebb (SCRUM Master, PO stb.)
cross-functional team - van, h a fejlesztő egyben tesztelő is
a végén mindig van egy potentially shippable product
gyorsan lehet szállítani a terméket
a megrendelő bármikor elzárhatja a pénzcsapot és azt mondhatja, hogy vége - és neki ekkor is lesz egy használható terméke
2-4 hetes sprintek vannak, amik elvileg érinthetetlenek, ekkor kap egy visszajelzést a fejlesztői csapat és itt elképzelhető, hogy lesz egy kardinális változás, amit kér az ügyfél és ezt le kell kezelni
ezért sokkal flexibilisebb a SCRUM

#### 9.  Communication skills are important for a test engineer. Why is that? Give an example for a possible scenario where a tester needs to use their communication skills.

## Testing Methods

#### 10. What is exploratory testing and what is its role in the testing process?

#### 11. What is risk-based testing, and why is it useful?

#### 12. What is POM and why is it useful?
POM: pagenként csoportosítja a classokat és 1-1 page-hez kapcsolódóan elég egyértelműen megtalálod az elemeket, ez egy design pattern - elválasztjuk a Selenium és a Java kódot, h mindkettő cserélhető legyen

#### 13. What is keyword-driven testing and why is it useful?
Keyword Driven Testing: arra törekszel, h LEGO kockákat építesz és azokat a legértelmesebb logika szerint rakd össze kisebb elemekből, aztán még nagyobb elemekből álljon - ez egy olvashatóbb végeredményt ad, olyan is tud vele dolgozni, aki nem feltétlenül tud kódolni

#### 14. What is TDD and why is it useful?
TDD (Test Driven Development): a unit testeket megírják előre a fejlesztők és addig fejlesztenek, amíg át nem megy az összes teszt

#### 15. What is BDD and why is it useful?
BDD (Behavior Driven Development): nagyon népszerű, Cucumber, Gherkin, Given, When, Then - az ügyfél és a fejlesztő közötti félreértések el legyenek kerülve és ebből szülessen meg a kód és a teszt (feature file-t egy bondinggal össze kell kötni a step file-al)

#### 16. What is data driven testing and why is it useful?
Amikor ugyanaz a teszt, de eltérőek az adatok.
Excelből, CSV-ből behúzza az adatokat - érdemes egy hozzáértő szakembernek odaadni, aki nagyon jól ismeri a terméket és ő sokkal jobb teszt adatokat fog összeírni egy excelben.

#### 17. Describe the test data lifecycle!

#### 18. Imagine you are responsible for quality assurance in a project. The release date is tomorrow but running all the tests takes 3 days. What do you do or suggest?

#### 19. Imagine you are in charge of testing a REST API with 5-10 different entities. How would you go about it? Plan and reason your tests.

#### 20. Imagine you are in charge of testing a small application. How would you go about it? Plan and reason your tests.
  Examples: webshop, banking app, online education app, social media, etc.

## Reporting, Bugs

#### 21. What steps would you follow if you found a defect?
Megpróbáljuk reprodukálni a hibát, bug reportot készítünk. 
Jelezzük a fejlesztőknek és ha javították, akkor újra teszteljük.

#### 22. Talk about common test reports, and about their details.
- Test Execution Report (by tester, by project, by test cycle, by folder etc.)
- Defect/Bug Report
- Test Coverage Report
- Test Analysis Report
- Test Summary Report

#### 23. What does a bug report contain?
Reprodukálási lépéseket feljegyezzük a bug reportban.
Ha egyik userrel működött, másikkal nem, érdemes összegyűjteni és egy sejtést leírni, h valószínűleg ez miért történhetett. Minél több infot összeszedünk a bug kapcsán, annál jobb és annál többet segítünk a fejlesztőknek.
Összefoglalás, részletes leírás - Expected - actual resultot beleírjuk és szerintem ennek kéne történnie.
Környezet - milyen browserben, op rendszeren történt a hiba.
Print screen Chrome konzolból, hibaüzenet, milyen URL-re mutatott.
Linket beilleszteni, h kattintson arra és lássa a fejlesztő, hogy neki is rossz lesz.
Severity/Priority

#### 24. How would you prioritize a bug? (Trick question)
hasonlóan, mint a risk-based testingnél érdemes az előfordulási valószínűség és okozott kár alapján rangsorolni
ISTQB-nek vannak erre ötletei, de minden cégnél ez meg van szabva általában

## Test Automation, Selenium, JUnit

#### 25. How would you decide if a test case should be automated or not?
Azért automatizálunk, hogy gyorsan jó dolgokat tudjunk fejleszteni. És ha automatizálunk, akkor gyorsan kapunk visszacsatolást róla, hogy milyen minőségű a szoftver.
Azokat a teszteket automatizáljuk, amit megéri: sokszor fogjuk használni, amit kézzel könnyű elrontani, nagyon fontos feature-t tesztel
az automata tesztek megtérülése 10-en pár használat után következik be
Captchat például nem lehet automatizálni, mert nem lehet helyettesíteni az emberi faktort

#### 26. Test cases should not depend on each other. What does this mean and why is it important?

#### 27. What is Selenium, Selenium IDE, and Selenium WebDriver?
**Selenium**: böngésző automatizáló tool
**Selenium IDE**: böngésző bővítmény, gyorsan, egyszerűen tudsz vele eldobható teszteseteket készíteni capture&replay módban, amiket vissza tudsz játszani. Ma még működni fognak, de holnap már nem biztos.
**Selenium WebDriver**: letölthető library-je, amit a robosztus teszt frameworkbe beleépítünk, amivel programozással automata teszteket készítünk, többféle nyelvhez lehet integrálni a Seleniumot és ez egy extension a programozói készlettárunkban. A Selenium a legelterjedtebb és a legtöbb tool erre épül(pl. a Katalon Studio is).

#### 28. How can web elements be identified? How do you choose which way to do it?
- xpath
- css
- id 
- linkText
- partialText

#### 29. What are the syntactic elements of an xpath?
#### 30. How can you make your Selenium bot wait for elements, what can go wrong? Collect possible errors and root causes.
**Implicit Wait**:
Usage: Set a global wait time that applies to all elements. Selenium waits for the specified time for an element to appear before throwing an exception.

**Explicit Wait**:
Usage: Use WebDriverWait to wait for a specific condition to be met before interacting with an element.

**Fluent Wait**:
Usage: Wait for an element with more flexibility. You can specify polling intervals and ignore specific exceptions.

Possible Errors and Root Causes:

**ElementNotVisibleException**:
Root Cause: The element is present but not visible (e.g., hidden by CSS).
Solution: Ensure the element is visible before interacting with it or use ExpectedConditions.visibility_of_element_located.

**NoSuchElementException**:
Root Cause: The element cannot be found on the page.
Solution: Double-check the locator strategy (e.g., ID, XPath) and make sure the element is present.

**TimeoutException**:
Root Cause: The element did not appear within the specified timeout.
Solution: Increase the timeout, verify that the element is on the page, or consider using a different locator strategy.

**StaleElementReferenceException**:
Root Cause: The element was located, but the DOM has changed, making the element stale.
Solution: Re-locate the element or refresh the page if necessary.

**ElementNotInteractableException**:
Root Cause: The element is on the page but not interactable (e.g., covered by other elements).
Solution: Ensure the element is not obscured by other elements or make it interactable before performing actions.

**ElementClickInterceptedException**:
Root Cause: Something intercepts the click action, such as a modal or overlay.
Solution: Handle the intercepting element or wait for it to disappear before interacting with the target element.

#### 31. What are the challenges and best practices with dynamically loading web elements?
#### 32. What are the most important annotations in JUnit and what are they used for?
#### 33. How can you provide parameters to your parameterized tests in JUnit? Which way is your favorite and why?
#### 34. How would you set up a Selenium testing project from scratch? What steps are important?
#### 35. What coding principles do you find important in test automation and why?
#### 36. What are some alternatives for Selenium? Which programming language do they rely on?
#### 37. What is Katalon Studio? In what situation is it a good tool to use?

## Devops

#### 38. What is CI/CD? What are some popular CI systems?
#### 39. What is Docker and why is it useful?
#### 40. What is Kubernetes and why is it useful?

## Personal Questions

#### 41. Why did you choose to learn test automation?
#### 42. What do you like about test automation?
#### 43. Tell me about a test automation project you worked on.
#### 44. Can you recall an interesting technical challenge you encountered while studying test automation? How did you manage it?
