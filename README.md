# selenium-script
package seleniumScripts;

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.firefox.FirefoxDriver;
import org.openqa.selenium.support.ui.Select;

public class Google {

	public static void main(String[] args) {
		WebDriver driver=new FirefoxDriver();
		driver.get("https://edit.europe.yahoo.com/registration?.intl=uk");
		//driver.findElement(By.id("Sign up"));//
		driver.findElement(By.xpath(".//*[@id='first-name']")).sendKeys("senthil");
driver.findElement(By.xpath(".//*[@id='last-name']")).sendKeys("kumaran");
driver.findElement(By.xpath(".//*[@id='user-name']")).sendKeys("kumarans993");
driver.findElement(By.xpath(".//*[@id='password']")).sendKeys("Kumaranjeru");
driver.findElement(By.xpath(".//*[@id='mobile']")).sendKeys("123456789");


WebElement ele1=driver.findElement(By.id("day"));
Select sel=new Select(ele1);
sel.selectByVisibleText("13");

WebElement ele2=driver.findElement(By.id("month"));
Select sel1=new Select(ele2);
sel1.selectByVisibleText("July");

WebElement ele3=driver.findElement(By.id("year"));
Select sel2=new Select(ele3);
sel2.selectByValue("1994");

driver.findElement(By.xpath(".//*[@id='male']")).click();
driver.findElement(By.xpath(".//*[@id='gender-wrapper']/fieldset/div/label[1]"));
driver.findElement(By.xpath(".//*[@id='mobile-rec']")).sendKeys("987654321");
driver.findElement(By.xpath(".//*[@id='relationship']")).sendKeys("single");
driver.findElement(By.linkText("Yahoo Terms")).click();
driver.findElement(By.linkText("Privacy")).click();
driver.findElement(By.linkText("Cookie Use")).click();
driver.findElement(By.className("Create account")).click();

	}

}
