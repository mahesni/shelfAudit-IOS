**********************
shelf audit automation
**********************

params.setPlatformName(System.getProperty("platformName", "Android"));
//params.setUDID(System.getProperty("udid", "DRGID18110202650"));
//params.setDeviceName(System.getProperty("deviceName", "Nokia 6.1 Plus"));
params.setUDID(System.getProperty("udid", "0J739301222179AE"));
params.setDeviceName(System.getProperty("deviceName", "real me narzo N53"));

case "Android":
params.setSystemPort(System.getProperty("systemPort", "10000"));
params.setChromeDriverPort(System.getProperty("chromeDriverPort", "11000"));
break

caps.setCapability("automationName", props.getProperty("androidAutomationName"));
caps.setCapability("appPackage", props.getProperty("androidAppPackage"));
caps.setCapability("appActivity", props.getProperty("androidAppActivity"));
caps.setCapability("systemPort", params.getSystemPort());
caps.setCapability("chromeDriverPort", params.getChromeDriverPort());
caps.setCapability("chromedriverUseSystemExecutable", true);
caps.setCapability("platformVersion", "13.0");
//caps.setCapability("browserName", "Chrome");
caps.setCapability("newCommandTimeout",240000);
//caps.setCapability("autoWebview",true);
//caps.setCapability("webviewConnectTimeout",90000);
caps.setCapability("enableWebviewDetailsCollection",true);
//caps.setCapability("autoGrantPermissions",true);
//caps.setCapability("chromeOptions:{args: ['--windowTypes=webview']});
//String androidAppUrl = getClass().getResource(props.getProperty("androidAppLocation")).getFile();
String androidAppUrl = System.getProperty("user.dir") + File.separator + "src" + File.separator + "test"+File.separator +"resources" + File.separator +"application" + File.separator +"Android" + File.separator + "CoinOut_v2.1.96-uat-release.apk";
System.out.println(androidAppUrl);
utils.log().info("appUrl is" + androidAppUrl);
caps.setCapability("app", androidAppUrl);
caps.setCapability("appWaitActivity", "*");

caps.setCapability("noReset", true);
caps.setCapability("fullReset", false);
caps.setCapability("platformName", params.getPlatformName());
caps.setCapability("udid", params.getUDID());
caps.setCapability("deviceName", params.getDeviceName());

appiumURL=http://127.0.0.1:4753
androidAutomationName=UiAutomator2
