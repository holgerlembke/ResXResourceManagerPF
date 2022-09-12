# WIP WIP WIP

https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax

# ResX Resource Manager Pain Free Start with Visual Studio 2022

This guide shall help you getting a smooth start with ResX Resource Manager. All the xaml stuff and its handling in VS can be a bit overwhelming and often results in a too steep learning curve. Oh this pain.

The secondary mouse button is your best friend. Clicking onto the right item helps a lot. But you know that already.

## Step 1: Get https://github.com/dotnet/ResXResourceManager via Extentions Manager

```
resxmanager
```

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

# Move Strings to Resouce

## Repeat A: In xaml select the text that needs translation. Include the quotes!

![alt text](img/resx7.png)

## Repeat B: Check the key. It must be a valid variable name!

![alt text](img/resx8.png)

# Add a translation language

## Repeat

![alt text](img/resx9.png)

Really. That is all you have to do. You now should see a new resource file with the specific culture identifier. Something like this:

![alt text](img/resx1b.png)

ResX Manager shows it in a new column. Now just translate into the new language.

# Translation in Code

Just write it the way you would normally do.
```
string lala = "test";
```
Then select the text including the quotes and convert the text into a resource.

![alt text](img/resx10.png)

Remember I: The key must be a valid variable name.

Remember II: you can shorten the namespace to your liking.

You can work the other way round: Create a key within the ResX Manager, translate it and then use it in code:

![alt text](img/resx11.png)

```
string c = localization.Resource.AddWindow;
```

# Force a specific translation at runtime

Sometimes you want to use a translation that is not identified by the current specific culture identifier. This is the way:

## identify the start window by opening app.xaml

![alt text](img/resx12a.png)

StartupUri contains the class that is created at startup. Go to that class constructor. It should look like that:

![alt text](img/resx12b.png)

## Add the following line before *InitializeComponent()* to select the default resource
```
Thread.CurrentThread.CurrentUICulture = new CultureInfo("");
```
or something like
```
Thread.CurrentThread.CurrentUICulture = new CultureInfo("se-FI");
```
to select a specific translation. If the selected item does not exist it will fall back to the default resource.


# Hints

* VS might complain that the xaml file is invalid. Try to Build/Run/F5. It will compile the new resource entries and VS should be happy again.

* Start small. Just add two or three translations in one dialog and get that done. When that works it is time to escalate.

* While working with xaml text Ctrl-Z is your best friend. Undo errors, don't try to fix them.

<sub>*Made with AWS Infinidash.*</sub>
