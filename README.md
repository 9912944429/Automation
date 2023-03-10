# Automation
package testcase;

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;
import org.testng.Assert;
import org.testng.annotations.Test;
import org.testng.Assert;
public class Logintest {
	WebDriver d;
  @Test
  public void login() {
	  System.setProperty("webdriver.chrome.driver", "G:\\chrome driver 110\\chromedriver.exe");
		WebDriver d=new ChromeDriver();
		d.manage().window().maximize();  
		
		d.get("https://test.vaccineledger.com/");
		
		d.findElement(By.name("email")).sendKeys("dev@statwig.com");
		
		d.findElement(By.xpath("//*[@id=\"root\"]/div/div/section[1]/div/div/article[2]/div/form/div[2]/button")).click();
		
		d.findElement(By.name("otp0")).sendKeys("1");
}
}
