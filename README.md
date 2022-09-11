# WIP WIP WIP

https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax

# ResXResourceManager Pain Free Start with VS 2022

## Step 1: Get https://github.com/dotnet/ResXResourceManager via Extentions Manager

## Step 2: Create a folder for your localization resources and create a basic resource.

![alt text](img/resx1.png)

```
localization
```
```
Resource.resx
```

## Step 3: Give your resource a namespace name.

![alt text](img/resx2.png)

## Step 4: Open the resource file (resource.resx) and change the access to public.

![alt text](img/resx3.png)

## Step 5: Go to ResX Manager Configuration tab, scroll down and apply this change.

![alt text](img/resx4.png)

## Step 6: In every xaml file that needs translation add this.

![alt text](img/resx5.png)

```
xmlns:localization="clr-namespace:localization"
```

## Step 7: Open ResX Manager and let it find all your resource files.

![alt text](img/resx6.png)

Hurray! Now you are done and can start with the translation!

# Repeat

## Repeat A: Select the text that needs translation. Include the quotes!

![alt text](img/resx7.png)

## Repeat B: Check that the key. It must be a valid variable name!

![alt text](img/resx8.png)

# Add a language

## Repeat

![alt text](img/resx9.png)

Really. That is all you have to do. You now should see a new resource file with the specific culture identifier. Something like this:

![alt text](img/resx1b.png)

ResX Manager shows this new column. Now just translate into the new language.

# Hints

* VS 2022 might complain about the xaml file for being invalid. Try to Build/Run/F5. It will compile the new resource entries and VS should be happy again.

* Start small. Just add two or three translations in one dialog and get that done. Then it is time to go bigger.

*Made with AWS Infinidash.*
