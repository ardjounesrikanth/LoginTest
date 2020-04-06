# LoginTest
Login Test Script for Selenium in Eclipse IDE


import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;
//import org.openqa.selenium.support.ui.ExpectedConditions;
//import org.openqa.selenium.support.ui.WebDriverWait;

public class FirstSeleniumTest {

	public static void main(String[] args) throws InterruptedException {

		System.setProperty("webdriver.chrome.driver", "C:\\Selenium\\selenium-java-3.141.59\\chromedriver_win32\\chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		String baseUrl = "https://demo.clickdoc.de/cd-de/my-profile";
		driver.manage().window().maximize();
		driver.get(baseUrl);
		Thread.sleep(9000);
		//WebDriverWait wait = new WebDriverWait(driver, 5);
		//wait.until(ExpectedConditions.visibilityOfElementLocated(By.xpath("/html/body/app-root/div/div/main/app-login/div/div[1]/div/div/div[2]/div[1]/form/mat-form-field[1]/div/div[1]/div/input")));
		//WebElement email = driver.findElement(By.xpath("/html/body/app-root/div/div/main/app-login/div/div[1]/div/div/div[2]/div[1]/form/mat-form-field[1]/div/div[1]/div/input"));
		WebElement email = driver.findElement(By.id("mat-input-0"));
		WebElement password = driver.findElement(By.id("mat-input-1"));
		
		email.click();
		email.clear();
		email.sendKeys("derek@gmail.com");
		
		password.click();
		password.clear();
		password.sendKeys("recruitingTest1!");
		WebElement login=driver.findElement(By.xpath("//button[text()='Einloggen']"));
		login.click();


	}

}

