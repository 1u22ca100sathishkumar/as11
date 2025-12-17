# as11
1. Selenium Architecture

Selenium follows a client–server architecture and consists of several key components that work together to automate web browsers.

Main Components of Selenium Architecture
1. Selenium Client Libraries

These are language-specific libraries (Java, Python, C#, Ruby, etc.).

They allow users to write test scripts in their preferred programming language.

Example: Selenium Java Client, Selenium Python Client.

2. WebDriver API

Acts as an interface between test scripts and browser drivers.

Converts test commands into browser-specific instructions.

Provides methods like get(), findElement(), click(), etc.

3. Browser Drivers

These drivers act as a bridge between Selenium WebDriver and the actual browser.

Each browser has its own driver:

Chrome → ChromeDriver

Firefox → GeckoDriver

Edge → EdgeDriver

Browser drivers understand browser-specific commands.

4. Real Browser

The actual browser (Chrome, Firefox, Edge, etc.) where automation is performed.

Executes the actions received from the browser driver.

Working Flow of Selenium Architecture

Test script is written using Selenium Client Library.

WebDriver receives commands from the test script.

WebDriver sends commands to the respective browser driver.

Browser driver communicates with the real browser.

Browser performs the action and sends response back.

📌 Diagram Flow (Textual Representation):

Test Script → WebDriver → Browser Driver → Browser

2. Selenium Program to Open Website and Close Browser
Java Program using Selenium WebDriver
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;

public class OpenWebsite {

    public static void main(String[] args) {

        // Set path of ChromeDriver
        System.setProperty("webdriver.chrome.driver", "path/to/chromedriver");

        // Launch Chrome browser
        WebDriver driver = new ChromeDriver();

        // Open the website
        driver.get("https://www.saucedemo.com/");

        // Print success message
        System.out.println("Site navigation success");

        // Close the browser
        driver.quit();
    }
}

Explanation of the Program

System.setProperty() → Sets the path of ChromeDriver

ChromeDriver() → Launches Chrome browser

driver.get() → Opens the given URL

System.out.println() → Prints success message

driver.quit() → Closes the browser

✔ Output:
Site navigation success
