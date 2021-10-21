package testing_Maven;

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.firefox.FirefoxDriver;
import org.testng.annotations.AfterClass;
import org.testng.annotations.BeforeClass;
import org.testng.annotations.Test;

import io.github.bonigarcia.wdm.WebDriverManager;

public class WebApp_Test {
	WebDriver driver;
	@Test
	public void loginIntoApp() {
		driver.findElement(By.linkText("Log in")).click();
		driver.findElement(By.id("Email")).sendKeys("manz@mass.com");
		driver.findElement(By.id("Password")).sendKeys("mass123");
		driver.findElement(By.xpath("//input[@value='Log in']")).click();
	}

	@Test
	public void logoutFromApp() {
		driver.findElement(By.linkText("Log out")).click();
	}

	@BeforeClass
	public void launchApp() {
		//System.setProperty("webdriver.chrome.driver", "/home/manzoormehadi/Public/Selenium Learning/Jar Files/chromedriver_linux64/chromedriver");
		WebDriverManager.firefoxdriver().setup();
		driver = new FirefoxDriver();
		driver.get("http://demowebshop.tricentis.com/");
		driver.manage().window().maximize();
		System.out.println("application is launched");
	}
	@AfterClass
	public void closeApp() {
		driver.close();
	}
}
