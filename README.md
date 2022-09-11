# ResXResourceManager Pain Free Start with VS 2022

Step 1: Get https://github.com/dotnet/ResXResourceManager via Extentions Manager

Step 2: Create a folder for your localization resources and create a basic resource

![alt text](img/resx1.png)

Step 3: Give your resource a namespace name

![alt text](img/resx2.png)

Step 4: Open the resource file (resource.resx) and change the access to public. Remember this step for every new resource.

![alt text](img/resx3.png)

Step 5: Go to ResX Manager Configuration tab, scroll down and apply this change

![alt text](img/resx4.png)

Step 6: In every xaml file that needs translation add this

![alt text](img/resx5.png)

Step 7: Open ResX Manager and let it find all your resource files

![alt text](img/resx6.png)

Hurray! Now you are done and can start with the translation!

Repeat A: Select the text that needs translation. Include the quotes!

![alt text](img/resx7.png)

Repeat B: Check that the key. It must be a valid variable name!

![alt text](img/resx8.png)
