Amazon Automation Testing Project
 This is a Selenium + TestNG based automation testing project for Amazon India. It
 automates the following features:- Search for existing and non-existing products- Add product to cart- Change product quantity in cart- Remove product from cart
 Project Structure:
 AmazonAutomation/
 ├── pom.xml
 ├── testng.xml
 ├── README.md
 ├── /drivers/
 │   └── chromedriver.exe
 ├── /src/
 │   └── /test/
 │       └── /java/
 │           ├── base/
 │           │   └── BaseTest.java
 │           └── base/
 │               └── AmazonTest.java
Tools & Technologies:- Java- Maven- Selenium WebDriver- TestNG- Eclipse IDE / IntelliJ IDEA- Chrome Browser
 How to Run the Tests
 1. Clone the Repository
 git clone https://github.com/yourusername/amazon-automation.git
 cd amazon-automation
 2. Setup Chromedriver
 Make sure chromedriver.exe is present in the drivers/ folder
 Use correct version matching your Chrome browser
 Update path in BaseTest.java if needed
 System.setProperty("webdriver.chrome.driver", "drivers/chromedriver.exe");
 3. Run via TestNG
 Option A: From Eclipse
- Right-click on testng.xml -> Run As -> TestNG Suite
 Option B: From Maven CLI
 mvn test
 testng.xml Configuration:
 <suite name="Amazon Suite">
    <test name="Amazon Test">
        <classes>
            <class name="base.AmazonTest"/>
        </classes>
    </test>
 </suite>
 Test Scenarios:
 Test Name                        Description-------------------------------- ---------------------------------------------
testNonExistingProductSearch()  Verify no results for gibberish query
 testExistingProductSearch()     Verify products are shown for "Laptop"
 testAddToCart()                 Add product to cart and verify
 testChangeQty()                 Change quantity to 2 in cart
 testRemoveFromCart()           Remove product and verify empty cart
 Prerequisites:
- Java 11 or higher- Maven installed- Chrome browser- Internet connection
 License:
 This project is open-source under the MIT License
