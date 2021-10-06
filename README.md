import org.openqa.selenium.By;

import org.openqa.selenium.Keys;

import org.openqa.selenium.WebDriver;

import org.openqa.selenium.chrome.ChromeDriver;



public class FisrtTest

{

    public static void main(String[] args) throws InterruptedException {

        System.setProperty("webdriver.chrome.driver", "C:\\Users\\Barte\\Downloads\\selenium-java-3.141.59\\chromedriver.exe");

        WebDriver driver = new ChromeDriver();

        driver.manage().window().maximize();

        driver.get("https://10minutemail.net/?lang=pl");

        driver.findElement(By.id("copy-button")).click();

        driver.get("http://automationpractice.com/index.php?controller=authentication");

        driver.findElement(By.id("email_create")).sendKeys(Keys.CONTROL + "v");

        driver.findElement(By.id("SubmitCreate")).click();

        Thread.sleep(10000);

        driver.findElement(By.id("id_gender1")).click();

        driver.findElement(By.id("customer_firstname")).sendKeys("John");

        driver.findElement(By.id("customer_lastname")).sendKeys("Wick");

        driver.findElement(By.id("passwd")).sendKeys("password");

        driver.findElement(By.id("days")).sendKeys("10");

        driver.findElement(By.id("months")).sendKeys("June");

        driver.findElement(By.id("years")).sendKeys("1976");

        driver.findElement(By.id("newsletter")).click();

        driver.findElement(By.id("optin")).click();

        driver.findElement(By.id("firstname")).clear();

        driver.findElement(By.id("firstname")).sendKeys("John");

        driver.findElement(By.id("lastname")).clear();

        driver.findElement(By.id("lastname")).sendKeys("Wick");

        driver.findElement(By.id("address1")).sendKeys("Browning Lane 292");

        driver.findElement(By.id("city")).sendKeys("Johnson City");

        driver.findElement(By.id("id_state")).sendKeys("Tennessee");

        driver.findElement(By.id("postcode")).sendKeys("37752");

        driver.findElement(By.id("id_country")).sendKeys("Unites States");

        driver.findElement(By.id("phone_mobile")).sendKeys("12345678");

        driver.findElement(By.id("alias")).clear();

        driver.findElement(By.id("alias")).sendKeys("My address");

        driver.findElement(By.id("submitAccount")).click();

        driver.quit();


    }

}
