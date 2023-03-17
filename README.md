# Registration Form Input and Validation

You worked on a project for registration input and validation at the end of Sections 7 and 8. The student entered any data, and the validation screen at the end displayed all the input, asking if it was good. In this project, you will do some minimal validation on each form, not allowing forward movement with the "Next" button until the screen is valid. 

Begin by making a COPY of the previous project.

On each screen, remove the heading about using a reducer. On the first screen, change the heading to "Account Registration", and change it to one button that says "Begin", which takes the user to the Names screen. On the phone screen, the placeholder needs to change to show an example of valid input. On the email screen, change the keyboard type to "email-address", so the "@" symbol is on that keyboard.  Here are screenshots showing the changes on the home and phone screens:

![F](https://github.com/bell-kevin/inputValidationRegistrationForm/blob/main/readMeExamplePictures/FormInput-1.PNG)    ![p](https://github.com/bell-kevin/inputValidationRegistrationForm/blob/main/readMeExamplePictures/formInput-4.PNG)   

 

Add a text component below the Next button on the 3 input screens, which will appear when the screen does not validate. When that text is present, the Next button will not work. Here are examples. The image on the left shows the screen when it first appears -- since both fields are empty, there are errors. The image on the right shows the screen when there is an error -- here, the last name is still empty.

![p](https://github.com/bell-kevin/inputValidationRegistrationForm/blob/main/readMeExamplePictures/formInput-2.PNG)     ![p](https://github.com/bell-kevin/inputValidationRegistrationForm/blob/main/readMeExamplePictures/formInput-3.PNG)

In the next image on the left, the phone number is incorrect because it is missing content -- it is not long enough. The example in the placeholder shows the pattern expected (see above). In the image on the right, the email address is incorrect because there is no "@" symbol. Note that the keyboard has an "@" symbol because the keyboard type is specific to email addresses.

![p](https://github.com/bell-kevin/inputValidationRegistrationForm/blob/main/readMeExamplePictures/formInput-5.PNG)     ![p](https://github.com/bell-kevin/inputValidationRegistrationForm/blob/main/readMeExamplePictures/formInput-6.PNG)

 

### Validations

The Name screen has two fields on it, and each one must have a length that is greater than 0. You saw this in the Udemy course -- trim the string, then check if the length is more than 0.

The Phone number screen has 10 numbers plus 2 hyphens. You could use a Regular Expression from JavaScript to check for a variety of acceptable phone number formats, but here, simply check that the string in the input field has a length of 12.

The Email screen has an email address, and those must have an "@" symbol in the strong. Check that the string contains the "@" and has a length greater than 1.

Where does the validation live? Where is the state of each variable described and changed? In the file for the context. Since you need to know if it is true or false that each field is valid -- that indicates the need for variables that hold the boolean that describes if the variable is valid or not. This is not an elegant solution, but it's sufficient to practice validation in this project. In the context file, add 4 variables for validity, like firstNameValid, lastNameValid, and so on. Set each to false. In the reducer that changes the state of the variables, check if the new data in the variable passes the validation tests. For example, when changing the firstName variable, check if the trimmed data has a length of more than zero, and if it does, set the firstNameValid variable to true, else set that variable to false. Then return the state with the spread operator, the data from the payload, and the firstNameValid boolean. You should already have this logic in place for returning all of the state with the new firstName variable overwriting the previous one -- add the "valid" variable and overwrite it as well.

In the screens, look at the code for the button to move to the next screen. You need to check that the "valid" variable is true, then navigate to the next screen. If it is not true, display the Text component that says to fix errors. Note in the screenshots above that this text is red, bold, and centered.

Take 5 screenshots: the first screen (black one above), the Names screen with errors, the Phone screen with errors, the Email screen with errors, and the final validation page that displays all the data. You had to fix those errors to move to the next screen, you don't have to take screenshots of the valid screens.

Submission: Zip together the root folder and the 5 screenshots, and submit the single zipped folder.

## How to:

Create one app. for both Android and iOS (Apple) using one computer alorithm for both apps. You'll need Visual Studio Code and Android Studio to get started:

https://code.visualstudio.com/download

https://developer.android.com/studio

If you want to see how your app. will look on iOS (Apple) devices, you'll need Xcode from the Apple app. store:

https://developer.apple.com/xcode/

To run the Xcode app, you'll need a fairly new Apple computer.

https://reactnative.dev/docs/environment-setup

https://reactnative.dev/docs/components-and-apis

https://reactnative.dev/docs/intro-react

Check out App.js here in the code files for the computer algorithm code.

## Storing Projects

When you complete a React Native project, you should keep it on your storage device for a little while. There are multiple instances where one project will be the basis of another project. The Udemy course keeps building on the projects, so you definitely need to keep those around until you are done with that project in the course.

BUT -- React Native projects are huge. There is a folder, node_modules, that takes up most of the space. If you keep every project you create in this course, you would need at least 20GB of space, probably more. How can you manage this terrible drain on your storage?

That node_modules folder is automatically added when you create a new project. Once you are done with the project, you can delete that folder, node_modules, and the size of your project will shrink dramatically.

This does not destroy the project. If you find you need to run an old project again, which no longer has its node_modules folder, open it in Visual Studio Code, open a terminal, and type "npm install". This will load the node_modules folder again, and the project is whole and ready to run.

Note that when you delete that folder, it takes a noticeable amount of time, far more than it takes to reload it.

A good practice for course maintenance is to keep the project in its full state until you are sure you won't be using it in the next few days, then delete the node_modules folder.

== We're Using GitHub Under Protest ==

This project is currently hosted on GitHub.  This is not ideal; GitHub is a
proprietary, trade-secret system that is not Free and Open Souce Software
(FOSS).  We are deeply concerned about using a proprietary system like GitHub
to develop our FOSS project. I have a [website](https://bellKevin.me) where the
project contributors are actively discussing how we can move away from GitHub
in the long term.  We urge you to read about the [Give up GitHub](https://GiveUpGitHub.org) campaign 
from [the Software Freedom Conservancy](https://sfconservancy.org) to understand some of the reasons why GitHub is not 
a good place to host FOSS projects.

If you are a contributor who personally has already quit using GitHub, please
email me at **bellKevin@pm.me** for how to send us contributions without
using GitHub directly.

Any use of this project's code by GitHub Copilot, past or present, is done
without our permission.  We do not consent to GitHub's use of this project's
code in Copilot.

![Logo of the GiveUpGitHub campaign](https://sfconservancy.org/img/GiveUpGitHub.png)
