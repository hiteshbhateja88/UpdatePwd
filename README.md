# UpdatePwd
from concurrent.futures import thread
import time
import login as login
from selenium import webdriver
from selenium.webdriver.remote.webelement import WebElement
from selenium.webdriver.support.ui import WebDriverWait


driver = webdriver.Chrome(executable_path="C:/Users/Bhateja's/PycharmProjects/untitled/chromedriver.exe")
wait = WebDriverWait(driver, 20)
url = "https://www.facebook.com/"
driver.get(url)
driver.maximize_window();
b="HelloWorld123"
a="YkhBVEVKQUAxMjM"
driver.find_element_by_id('email').send_keys("happy.hitu@gmail.com");
driver.find_element_by_id('pass').send_keys(a);
driver.find_element_by_id('loginbutton').click();
time.sleep(3);
driver.find_element_by_xpath("//div[@aria-label='Account']").click();
#driver.find_element_by_xpath("//div[@role='button']").click();
time.sleep(3);
#//span[contains(text(),’Settings & privacy’)]
driver.find_element_by_xpath("//div[@aria-label='Account']//div//span[contains(text(),'Settings & privacy')]").click();
time.sleep(3);
driver.find_element_by_xpath("(//div[@aria-label='Account']//div//span[contains(text(),'Settings')])[2]").click();
time.sleep(15);
driver.find_element_by_xpath("//ul[@id='u_0_0']//li//a[@title='Security and login']").click();
time.sleep(3);
driver.find_element_by_xpath("//span[contains(text(),’Change Password’)]").click();
time.sleep(3);
driver.find_element_by_xpath("//input[@name='password_old']").send_keys(a);
time.sleep(3);
driver.find_element_by_xpath("//input[@name='password_new']").send_keys(b);
time.sleep(3);
driver.find_element_by_xpath("//input[@name='password_new']").send_keys(b);
time.sleep(3);
driver.find_element_by_xpath("//input[@id='u_e_1']").click();
