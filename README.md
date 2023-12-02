# ImplementationPartOne

These steps will help you successfully set up and run the project in Eclipse.
1. Start by downloading the project from the GitHub repository at 
Add the url here
2. Follow these steps to set up a JavaFX non-modular project using your preferred IDE. If you don't have the project, you can find a similar one for download.
3. Download the appropriate JavaFX SDK for your operating system and extract it to a chosen location, like /Users/your-user/Downloads/javafx-sdk-21.0.1.
4. In Eclipse, navigate to File -> Import -> General -> Import existing project -> Browse to the downloaded project -> Click Next.
5. Include the JavaFX 21.0.1 library in the classpath. Add the JavaFX library created in the previous step.
6. Note: Running the project at this point will result in an error - "JavaFX runtime components are missing." To resolve this, follow these steps:
   a. Click on Run -> Run Configurations... -> Java Application.
   b. Create a new launch configuration for your project (e.g., hellofx) and add the following VM arguments:
      Linux/Mac: `--module-path /path/to/javafx-sdk-21.0.1/lib --add-modules javafx.controls,javafx.fxml`
      Windows: `--module-path \path\to\javafx-sdk-21.0.1\lib --add-modules javafx.controls,javafx.fxml`
      Ensure the checkbox "Use the -XstartOnFirstThread argument when launching with SWT" is unchecked.
   c. Click Apply and close the dialog.
7. Run the project by selecting Run -> Run As -> Java Application -> Main - hellofx.
8. Optionally, you can create a new User Library in Eclipse under Window -> Preferences -> Java -> Build Path -> User Libraries -> New. Name it JavaFX21 and include the JAR files from the lib folder in JavaFX 21.
9. Add the JavaFX JARs to the library.
