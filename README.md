import org.openqa.selenium.*;
import org.openqa.selenium.By.ById;
import org.openqa.selenium.firefox.FirefoxDriver;
import org.openqa.selenium.ie.InternetExplorerDriver;
public class MyWebdriver_Setting_Class {

	/**
	 * @param args
	 * @throws InterruptedException 
	 */
	public static void main(String[] args) throws InterruptedException {
		// TODO Auto-generated method stub
		WebDriver driver=new InternetExplorerDriver();
		driver.get("https://accounts.google.com");
		driver.manage().window().maximize();
		WebElement userName=driver.findElement(By.id("Email"));
		userName.clear();
		userName.sendKeys(new String[]{"himajahoney"});
		WebElement nextButton=driver.findElement(By.id("next"));
		nextButton.click();
		Thread.sleep(5);
		System.out.println("test");
		WebElement passwd=driver.findElement(By.name("Passwd"));
		passwd.clear();
		passwd.sendKeys(new String[]{"jaisreeram"});
		WebElement btnSubmit=driver.findElement(By.id("signIn"));
		btnSubmit.click();
System.out.print(driver.getTitle());
driver.close();

	}

	private static By ById(String string) {
		// TODO Auto-generated method stub
		return null;
	}

}
