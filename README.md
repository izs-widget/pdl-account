# IZS 'PDL Account' Embedded Widget

The `IZS embedded widget` is a versatile tool designed and developed for seamless integration into your website. This README provides a brief guide on how to use the widget.

## Table of Contents

- [Usage](#usage)
- [Customization](#customization)
- [Support](#support)

## Usage

To get started with the `IZS 'PDL Account' embedded widget`, you need to include the widget's script and styles on your website.

### Step 1: Include the Widget Styles and Script

Add the following link tag to the `<head>` section 

```html
<link rel="stylesheet" href="https://widget-izs.s3.eu-north-1.amazonaws.com/izs-style.css">
```

and following script tag to the `<body>` section of your HTML file:

```html
<link rel="stylesheet" href="https://widget-izs.s3.eu-north-1.amazonaws.com/izs-style.css">
```

Example:

```html
<head>
    ...
    <link rel="stylesheet" href="https://widget-izs.s3.eu-north-1.amazonaws.com/izs-style.css">
    ...
</head>
<body>
    ...
    <script src="https://widget-izs.s3.eu-north-1.amazonaws.com/izs-widget.umd.js"></script>
</body>
```

### Step 2: Initialize the Widget

In the <body> section of your HTML file where you want the widget to appear, add the following html element with defined id attribute 

```html
<div id="izsWidget"></div>
```

and initialize the widget with the folowing code, where you call the widget function with the selector of the widget container and the configuration object with required api key (provided by the ISZ support) and other optional properties.

```html
IzsWidget.init('#izsWidget', {
  apiKey: 'sfe6efef87876efeeefe',
  pdlId: 'q937A00000oln1vQA'
});
```

### Basic Example

Here is a basic example of how to use the widget:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link rel="stylesheet" href="https://widget-izs.s3.eu-north-1.amazonaws.com/izs-style.css">
  <title>IZS Embedded Widget Example</title>
</head>
<body>
  <div id="izsWidget"></div>
  
  <script src="https://widget-izs.s3.eu-north-1.amazonaws.com/izs-widget.umd.js"></script>
  <script>
    document.addEventListener('DOMContentLoaded', () => {
      IzsWidget.init('#izsWidget', {
        apiKey: 'sfe6efef87876efeeefe',
        pdlId: 'q937A00000oln1vQA'
      });
    });
  </script>
</body>
</html>
```

## Customization

Comming soon... In the next versions of the widget you will be able to customize the IZS embedded widget by passing different options to the init method.

## Support

If you encounter any issues or have any questions, please reach out to our support team at info@izs-institut.de
