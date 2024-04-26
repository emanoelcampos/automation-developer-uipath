# Introduction to Output Methods

Output actions are used to extract data, generally in the form of text, from UI elements. Output methods are how output actions extract data from UI elements.

Modern UI automation design typically employs three main output methods, which include:

1. Full Text
- The FullText method is the default method and good enough in most cases. 
- It is the fastest, it can extract hidden text, it has 100% accuracy, and can work in the background.
2. Native Text
- The Native method is compatible with applications that use Graphics Design Interface (GDI), the Microsoft API used for representing graphical objects. 
- It doesn’t extract hidden text and it cannot work in the background; and just like FullText, it doesn’t support virtual environments.
3. Optical character recognition (OCR)
- OCR (or Optical Character Recognition) is the only output method that works with virtual environments and with “reading” text from images. 
- Its technology relies on recognizing each character and its position. On the other hand, it cannot work in the background, it cannot extract hidden text, and its speed is by far the lowest.

Now, let's take a closer look at the differences between these output methods.

| Output Method                        | FULL TEXT                                                                                            | NATIVE                                                                                                                                                                         | OCR                                                                                                                                                                                                                                                                                               |
| ------------------------------------ | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Default method and Compatibility** | It is the **Default method** and good enough in most cases.                                          | Compatible with applications that use **Graphics Design Interface (GDI)**, the **Microsoft API is** used for representing graphical objects.                                   | OCR (or Optical Character Recognition) is the only output method that works with **virtual environments** and with **“reading” text from images**.  <br>  <br>Its technology relies on recognizing each character and its position.                                                               |
| **Automation Speed**                 | **Fastest** compared to the other two methods.                                                       | Somewhat **s****lower than FullText.**                                                                                                                                         | By far the **slowest.**                                                                                                                                                                                                                                                                           |
| **Accuracy**                         | **100%** accuracy.                                                                                   | **100%** accuracy on the **applications that support GDI.**                                                                                                                    | Accuracy varies from **one text to** another, by **changing the settings** we can improve the results.                                                                                                                                                                                            |
| **Running in Background**            | **Works** in the background.                                                                         | **Cannot** work in the background.                                                                                                                                             | **Cannot** work in the background.                                                                                                                                                                                                                                                                |
| **Hidden Text**                      | **Can** extract hidden text (for example, the options in a drop-down list).                          | **Cannot** extract hidden text.                                                                                                                                                | **Cannot** extract hidden text.                                                                                                                                                                                                                                                                   |
| **Virtual Environment**              | **Doesn’t** support virtual environments.                                                            | **Doesn’t** support virtual environments.                                                                                                                                      | **Works** with virtual environments and with **“reading” text from images**.                                                                                                                                                                                                                      |
| **Text position and Formatting**     | **Doesn’t capture** text position and formatting.                                                    | **Can** extract the text position and formatting (including text color)                                                                                                        | Like the **Native** method, it also captures the text position.                                                                                                                                                                                                                                   |
| **Other**                            | The method offers the **option** **to ignore the hidden message** and capture only the visible text. | By default, it can process all known **characters as separators** (**comma, space, and so on**), but when only certain separators are specified, it can ignore all the others. | The OCR method has **two default engines** that can be used alternatively:<br><br>- **Google Tesseract,** <br>- **Microsoft MODI.**<br><br>There are additional OCR engines that can be installed free of charge (such as Omnipage and Abbyy Embedded) or paid (IntelligentOCR offered by Abbyy). |
