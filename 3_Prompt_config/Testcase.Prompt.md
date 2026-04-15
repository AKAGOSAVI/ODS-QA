
This file contains prompts for generating Java Selenium automation scripts

Framework Analysis:
⦁	Base Test Class: BasePage.java (driver management, configuration)
⦁	Page Objects: LoginPage, ZEDPage
⦁	Utilities: Base
⦁	Listeners: ExtentReportListener, ScreenshotListener
⦁	Test Data: JSON/Excel support via ExcelReader
⦁	Reporting: ExtentReports with enhanced logging

TEST_SCRIPT_GENERATION_PROMPTS
Generate SQL query for
based on test cases TC001-TC005 from Base_Repo Path : C:\Users\ODS-QA\Documents\ZED\https---github.com-Akash_gosavi\ZED_Scripts\src\OptimusCore\1_Base_Repo\Template\Template.md
FRAMEWORK COMPONENTS TO REUSE:
⦁	Base Class: extends BasePage.java for driver and config management
⦁	Page Object: LoginPage.java with methods:
⦁	clickOnbtnLogin()
⦁	loginZEDApplication()
⦁	update_Quote_ErrorMessage();
⦁	updateQuote_NewBusiness();
⦁	selectOneEFilecheckBox();
⦁	clickOnbtnDraft();
⦁	clickDraftPopUpAndClickOnContinue();
⦁	validateTo();
⦁	clickBackToTransactionScreen();
⦁	includeBCCEmailRecipientsCheckBox();
⦁	clickOnContinue();
⦁	clickOnSendEmail();
⦁	Utilities:
⦁	ConfigReader.getProperty("app.url")
⦁	TestDataReader.getTestData("login_credentials.json")
⦁	TestLogger.logInfo(), TestLogger.logPass(), TestLogger.logFail()
⦁	Test Data: Use TestDataReader for credentials from JSON/Excel
REQUIREMENTS:
⦁	Use @Test annotations with priority and description
⦁	Implement data-driven testing with TestDataReader
⦁	Use ExtentReports logging for each step
⦁	Include proper assertions with meaningful messages
⦁	Handle waits using WaitUtils class
⦁	Capture screenshots on failures using ScreenshotUtils
⦁	Follow Page Object Model pattern strictly
SAMPLE TEST METHOD STRUCTURE:
@Beforeclass
@Test
public void verify_Binder_Efile_Retrive_Upload_Documnet() {
try {
// clicking on Login Button
Zed.clickOnbtnLogin();
// clicking on ZED application Login
Zed.loginZEDApplication();
Zed.update_BinderUWD();
Zed.uwuaPhoneNumberVerification();
Zed.clickingOncheckBoxes_Random();
Zed.ClickOnTabUploadDocument();







FOR ODS - Prompts
Prompt for test cases genartion
Generate teste cases from user story -
"User story path"
Generate test cases for fields -
"Mention fields which required to test as part of ETL testing"
 
Generate test cases based on requirement -
"Give specifiec requirement for field"
Generate test cases for source to target validation -
"Source and target information"
generate test cases for Policy center based on transaction and scenario -
"Give transaction details of policies and scenario for testing"
generate test cases for Claim center based on transaction and scenario -
"Give transaction details of claims and scenario for testing"
Generate test cases for commercial auto policies -
"Give product type, Province, Risk typ and scenario specifiec"
Zed.clickOnbtnupload();
String[] sPath = map.get("Filenames").split(";");
for (int i = 0; i < sPath.length; i++) {
Zed.uploadfile(sPath[i]);
}
System.out.println(sPath.length + "- files are uploaded");
Zed.clickOnbtnClose();
Zed.fillZDWDocumentType(sPath.length);
Zed.clickOnbtnDraft();
Zed.clickDraftPopUpAndClickOnContinue();
Zed.validateTo();
Zed.clickOnSendEmail();
Zed.hardWait();
Zed.verifypopEmail();
} catch (Exception e) {
System.out.println(e.getMessage());
}
}
@Afterclass

Based on the above prompt, the generated test class should include all necessary imports, class definition, and methods for each test case. Each method should follow the structure provided in the sample test method structure, ensuring proper logging, assertions, and error handling.
Generate the complete Java test class for the Authentication module using the provided prompt and requirements.
Generate the test script in C:\Users\SRIRAM.MAHESWARA\Documents\ZED\https---github.com-Sriram-Maheswara-zed_project\ZED_Scripts\src\test\java\com\zed\zed_tickets\SampleOptimusTest.java
