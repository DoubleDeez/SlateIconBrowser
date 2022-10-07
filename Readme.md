# Editor Icon Browser

This small tool lets you browse Unreal Engine's Editor icons/brushes easily, search for specific ones and copy slate code for the selected icon.

![Screenshot of the window](Documentation/WindowScreenshot.png)

## Invocation

When the plugin is activated, there's only one window which you can open via `Tools -> Editor Icon Browser`.

## Features

### Searching

Using the search bar it's possible to filter the icons based on their names.

### Select a Style Set

Using a dropdown menu you can select another style set besides the default Editor style.

### Non-Image Brushes

Non-image brushes (like solid colors) will be displayed with a default size as a simple square.

### Copying Slate Code

Currently this tool only supports `FSlateIcon` code, which will be copied by double-clicking a list entry.

    FSlateIcon(FEditorStyle::GetStyleSetName(), "Icon")
    FSlateIcon(FName("SomeStyle"), "Icon")

A few default styles will be replaced by the generic class call (like `FEditorStyle::GetStyleSetName()`) while others will be copied as a FName reference instead (using `FName("SomeStyleSet")`).

As with everything source-code related you are supposed to read it before you include it and adjust it to make it work in your environment.