# Automation
package testcase;

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;
import org.testng.annotations.Test;

public class Logintest {
	WebDriver d;
  @Test
  public void login() {
	  System.setProperty("webdriver.chrome.driver", "G:\\chrome driver 111\\chromedriver.exe");
		ChromeOptions options = new ChromeOptions();
		options.addArguments("--remote-allow-origins=*");
		WebDriver d= new ChromeDriver(options);
		d.manage().window().maximize();  
		
		d.get("https://test.vaccineledger.com/");
		
		d.findElement(By.name("email")).sendKeys("dev@statwig.com");
		
		d.findElement(By.xpath("//*[@id=\"root\"]/div/div/section[1]/div/div/article[2]/div/form/div[2]/button")).click();
		
		
		Thread.sleep(2000);
		d.findElement(By.id("otp0")).sendKeys("1");
		d.findElement(By.id("otp1")).sendKeys("2");
		d.findElement(By.id("otp2")).sendKeys("3");
		d.findElement(By.id("otp3")).sendKeys("4");
		
		d.findElement(By.xpath("//*[@id=\"root\"]/div/div/section/div/div[2]/div[2]/div/section/div/form/section[2]/button")).click();
}
}
# Automation for signup
package testcase;

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;
import org.testng.annotations.Test;

public class Signup {
  WebDriver d;
  @Test
  public void signup() {
	  System.setProperty("webdriver.chrome.driver", "G:\\chrome driver 111\\chromedriver.exe");
		ChromeOptions options = new ChromeOptions();
		options.addArguments("--remote-allow-origins=*");
		WebDriver d= new ChromeDriver(options);
		d.manage().window().maximize();  
		
		d.get("https://test.vaccineledger.com/");
		
		d.findElement(By.xpath("//*[@id=\"root\"]/div/div/header/div/nav/ul/li[6]/button")).click();
		
		d.findElement(By.id("mui-2")).sendKeys("Harish");
		
		d.findElement(By.id("mui-3")).sendKeys("Sarnala");
		
		d.findElement(By.id("mui-4")).sendKeys("sarnalaharish@gmail.com");
		
		d.findElement(By.name("phone")).sendKeys("9912944429");
		
		d.findElement(By.name("organizationExists")).click();
		
		d.findElement(By.tagName("input")).sendKeys("PHARMACY");
		
		d.findElement(By.xpath("//*[@id=\"root\"]/div/div/section/div/div[2]/div[2]/div/section/div/form/section[3]/button")).click();
			
  }
}
