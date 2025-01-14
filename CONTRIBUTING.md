# Lawnicons contributing guide
Welcome to the Lawnicons contributing guide! This file will tell you  what you need to know to contribute to Lawnicons.

## Icon guidelines
See the below image for a summary of the icon guidelines. If you don't follow them, a team member will likely request changing the icons.

![](./contributing-image-1.png)

Each icon must fit the 160x160px or 144x144px (depending on the shape) content area size. It must not be smaller nor bigger than the specified sizes.

The stroke should be kept at 12px for most lines. If 12px is too thick, a stroke of 8px can be used.

In addition to the above, the icons must have an outlined (not filled) style. If the original icon has a filled style, you should change the icon to adhere to the guidelines as seen below.

![](./contributing-image-2.png)

## Adding an icon to Lawnicons
Here’s how to add an icon to&nbsp;Lawnicons:

1. Prepare your icon in the SVG format, adhering to the [above guidelines](#icon-guidelines). Use snake case for the filename (e.g.&nbsp;`files_by_google.svg`).

1. Add the ready SVG to the `svgs`&nbsp;directory.

1. Using Android Studio, convert the SVG to an XML drawable, and add the XML drawable to the `app/src/main/res/drawable` directory. Use snake case for the drawable name (e.g. `files_by_google`). You can keep all settings at their&nbsp;defaults.

    ![](./contributing-image-3.png) ![](./contributing-image-4.png)

1. Add a new line to `app/src/main/res/xml/grayscale_icon_map.xml` (sorted alphabetically by drawable name), and map the new icon to a package name and app name. For&nbsp;example:

    ```xml
    <icon drawable="@drawable/files_by_google" package="com.google.android.apps.nbu.files" name="Files by Google" />
    ```

    A general template is as&nbsp;follows:

    ```xml
    <icon drawable="@drawable/[DRAWABLE NAME]" package="[PACKAGE NAME]" name="[APP NAME]" />
    ```

1. Done! You’re ready to open a pull request. Please set `develop` as the base&nbsp;branch.
