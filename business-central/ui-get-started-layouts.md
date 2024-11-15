---
title: Get Started Creating Layouts
description: Learn how to create layouts to personalize the appearance of a report when viewed, printed, or saved.
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: customized report, document layout, logo, personalize
ms.search.form: 9650, 9652, 9660_Primary
ms.date: 11/05/2024
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.reviewer: jswymer
---
# Get started creating report layouts

Business Central comes with many built-in layouts that you can use on your reports. Other layouts may have been added as part of other extensions. But it's also possible to create your own reports either from scratch or based on an existing layout.

> [!IMPORTANT]
> You can also use report layouts to add content to email messages. For example, report layouts can save time and help ensure consistency by reusing the same content when you communicate with your customers. To use custom report layouts with email, the file type for the layout must be Word. You cannot use the RDLC file type. Learn more in [Set Up Reusable Email Texts and Layouts](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts). 

## Overview

When working with report layouts, it helps to think of the layout as a file that's imported and assigned to a report. Regardless of the layout type, how you manage layouts in Business Central is basically the same. Usually, you work from the **Report Layouts** page. The main difference is how you design the layout, which is done by using the application software that the layout's built on, like Word, Excel, or SQL Server Report Builder.

With this concept in mind, there are basically three or four tasks involved in setting up a layout on a report:

1. Decide on the layout type.
2. Export a copy of an existing layout to use as a starting point.
3. Make changes to the layout file in the appropriate application.
4. Add the new layout file to the report.

> [!IMPORTANT]
> You can't modify or replace an extension layout, which is a layout that originates from an extension. You can only modify or replace user-defined layouts. On the **Report Layouts** page, you can tell whether the layout is an extension layout or user-defined layout by looking at **Extension** column. An extension layout will show information about the source extension in the column. The **Extension** column will be empty for a user-defined layout.
>
> Learn more about the difference between extension layouts and user-defined layouts in [Layout source](ui-manage-report-layouts.md#layout-sources).

## Get started

Depending on what your situation is, the actual tasks vary. Use the following table to help you get started.

|What do you want to do?|Learn more|
|-----------------------|------|
|Figure out what's the best layout type to use for my situation|[Decide what type of layout you want](#decide)|
|Create a new layout for a report that's based on a copy an existing layout or create one from scratch|[Create a new layout](#create)|
|Make changes to an existing layout that's used on a report|[Modify a layout](#modify)|
|I have a new version of a layout file for a report. I want to replace the existing layout file.|[Replace a layout](#replace)|
|Switch the current layout used by a report to another layout|[Setting the Layout Used by a Report](ui-set-report-layout.md)|
|Change the name and description of a layout|[Rename a layout](#rename)|

## <a name="decide"></a>Decide what type of layout you want

The first thing when creating a layout is to decide which [layout type](ui-manage-report-layouts.md#layout-types) you want. You can choose either Word, Excel, or RDLC. The layout type depends on how you want the generated report to look. Plus, it depends on your knowledge of application software for creating the layouts, like Word, Excel, and SQL Server Report Builder.

* Excel layouts are generally the easiest to create and modify because the features for summarizing data, adding graphics, and styling, are common Excel features.

* Not all reports and documents have a dataset that is optimized for use with an Excel layout. For example, aggregations and complex calculations work best with RDLC or Word layouts. The same is true for documents.

* If you're only making style changes like font type, size and colors, a Word layout is also a good choice.

* Adding data fields or rearranging data fields in Word or RDLC is more advanced than with Excel.

* Word and RDLC layouts are good to use for reports that will eventually be printed.  

* The general design concepts for Word and RDLC layouts are similar. However, each type has certain design features that affect how the generated report appears in [!INCLUDE[prod_short](includes/prod_short.md)]. The same report might look different when using the Word layout compared to the RDLC layout.

## <a name="create"></a>Create a new layout

There are different ways to create a new layout. The easiest ways involve using a copy of an existing layout, which you can do by either saving an existing layout directly as a copy or exporting it and then importing it to a new layout. Another, more advanced way, is to create a layout from scratch using a blank.

### [Save existing as copy](#tab/copy)

Copying is a quick way to create a new layout that's the same as an existing layout. Once you have the copy, you can make modifications by exporting the layout. 

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Select the layout that you want a copy of for your new layout, then choose the **Edit Info** action.

    If you select an extension layout, you're prompted whether you want to edit a copy. To continue, select **Yes**.

    > [!TIP]
    > To help you find the layout, use the **Search** box, **Filter** pane, and columns sorting.
3. Change the **Layout Name**.
4. Turn the **Save Changes to Copy** switch to **On**, then select **OK**.

   The new layout shows in the **Report Layouts** page.
5. If you want to make changes to the new layout, refer to [Modify an existing layout](#modify).

### [Export existing as copy and import as new](#tab/export)

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Select the layout that you want a copy of for your new layout, then choose the **Export Layout** action.

   The layout file is downloaded to your device. 

    > [!TIP]
    > To help you find the layout, use the **Search** box, **Filter** pane, and columns sorting.

3. Open the layout file in the appropriate application, like Word (for a .docx file) or Excel (for an .xlsx file).

   Learn more in:

   * [Work with Word Layouts](ui-how-add-fields-word-report-layout.md)
   * [Work with Excel Layouts](ui-excel-report-layouts.md)
   * [Work with RDLC Layouts](ui-rdlc-report-layouts.md)

   Make changes to the file and save it.

4. Back on the **Report Layouts** page, select **New**.
5. In **Add New Layout for a Report** page, fill in the following fields:

   |Field|Description|Mandatory|
   |-----|-----------|---------|
   |Report ID|Set to the ID assigned to the report|yes|
   |Layout Name| Type a brief description name for the layout to help you easily identify it.|yes|
   |Description| Type more detailed information about the layout. |no|
   |Format Options|Set this field to match the type of layout, like Word, Excel, or RDLC.|yes|

6. Select **OK**, then do one of the following steps to upload the layout file for the report:

   [!INCLUDE[file-upload](includes/file-upload.md)]

   The selected file is uploaded to the layout, and you return to the **Report Layouts** page.

If you want to see how the report looks with the new layout, select the layout in the list, then select **Run Report**.

### [Create from blank](#tab/blank)

When you create a layout from a blank, you need to design it entirely. The layout file provides all the report fields that you can add and arrange as needed.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
1. Select any layout in the list that is for the same report that you want use for the new layout.
1. Select **New**.
1. In **Add New Layout for a Report** page, fill in the following fields:

   |Field|Description|Mandatory|
   |-----|-----------|---------|
   |Report ID|Set to the ID assigned to the report|yes|
   |Layout Name| Type a brief description name for the layout to help you easily identify it.|yes|
   |Description| Type more detailed information the layout. |no|
   |Format Options|Set this field to match the type of the layout, like Word, Excel, or RDLC.|yes|
1. Turn on the **Create a blank layout from the report object** switch.
1. Select **OK** when finished.

   The new layout appears in the list. The layout is blank, but all the reports fields and captions are available for you to start adding them to the layout.

1. Now, you're ready to start designing the layout. Learn more in [Modify an existing layout](#modify).

---

## <a name="modify"></a>Modify a layout

Follow these steps to modify an existing user-defined layout.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Select the layout that you want to modify, then choose the **Export Layout** action.

   The layout file is downloaded to your device. 

   > [!TIP]
   > To help you find the layout, use the **Search** box, **Filter** pane, and columns sorting.

3. Open the layout file in the appropriate application, like Word (for a .docx file) or Excel (for an .xlsx file).

   Learn more in:

   * [Work with Word Layouts](ui-how-add-fields-word-report-layout.md)
   * [Work with Excel Layouts](ui-excel-report-layouts.md)
   * [Work with RDLC Layouts](ui-rdlc-report-layouts.md)

   Make changes to the file and save it.

4. Back on the **Report Layouts** page, select the existing layout, then select the **Replace Layout** action.
5. Select **OK** > **Choose** to open file explorer on your device.
6. Find and select the Excel file, then select **Open**.

   The selected file is uploaded to the layout, and you return to the **Report Layouts** page.
7. If you want to see how the report looks with the new layout, select the layout in the list, then select **Run Report**.

## <a name="replace"></a>Replace a layout

Follow these steps to replace the existing user-defined layout file with a new file.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Select the existing layout, then select the **Replace Layout** action.
3. Select **OK** > **Choose** to open file explorer on your device.
4. Find and select the Excel file, then select **Open**.

   The selected file is uploaded to the layout, and you return to the **Report Layouts** page.
5. If you want to see how the report looks with the new layout, select the layout in the list, then select **Run Report**.

## <a name="rename"></a>Rename a layout

Follow these steps if you want to change the name and description of a user-defined layout.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Select the layout that you want to rename, then choose the **Edit Info** action.

    > [!TIP]
    > To help you find the layout, use the **Search** box, **Filter** pane, and columns sorting.
3. Change the **Layout Name**, then select **OK**.

## Related information

[Managing Report Layouts](ui-manage-report-layouts.md)  
[Working with Word Layouts](ui-how-add-fields-word-report-layout.md)  
[Working with Excel Layouts](ui-excel-report-layouts.md)  
[Working with Reports, Batch Jobs, and XMLports](ui-work-report.md)  
[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
