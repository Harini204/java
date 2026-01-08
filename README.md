package week2;


import java.util.List;

import org.openqa.selenium.By;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;




public class facebook {
	public static void main(String[] args) {
		
		
		ChromeDriver driver = new ChromeDriver();
		driver.manage().window() . maximize();
		driver.get("https : // WWW.facebook.com/");
		
		
		List<WebElement> languages = driver.findElements(
				By.xpath(" //u1 [Contains(@class, 'localeSelectorList')]//a")
		);
		
		
		for(int i=0; i<languages.size();i++) {
			System.out.println(i+" -> "+languages.get(i).getAttribute("href"));
			
		}
			
			List<WebElement> footerlinks = driver.findElements(
					By.xpath("//div[@id='pageFooter']//a")
		);
		for (int i = 0; i < footerlinks.size(); i++) {
			System.out.println(i + " -> " + footerLinks.grt(i) .getAttribute("href"));
				
		}
	
	}
}
