# IZS 'PDL Account' Embedded Widget

The `IZS embedded widget` is a versatile tool designed and developed for seamless integration into your website. This README provides a brief guide on how to use the widget.

## Table of Contents

- [Usage](#usage)
- [Demo](#demo)
- [Customization](#customization)
- [Info](#info)
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
<script src="https://widget-izs.s3.eu-north-1.amazonaws.com/izs-widget.js"></script>
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
    <script src="https://widget-izs.s3.eu-north-1.amazonaws.com/izs-widget.js"></script>
</body>
```

### Step 2: Initialize the Widget

In the <body> section of your HTML file where you want the widget to appear, add the following html element with defined id attribute 

```html
<div id="izsWidget"></div>
```

and initialize the widget with the folowing code, where you call the widget function with the selector of the widget container and the configuration object with required api key (provided by the ISZ support) and other optional properties.

```javascript
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
  
  <script src="https://widget-izs.s3.eu-north-1.amazonaws.com/izs-widget.js"></script>
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

## Demo

You can visit a [demo page](https://pdl-account-widget.netlify.app/) with integrated IZS 'PDL Account' Embedded Widget to see how it works.

## Customization

You are able to customize the IZS embedded widget by passing different options to the init method. For that aim there is additional object 'styles' where you can pass key-value pairs provided below to style different parts of the widget.
All available options for styling with default values are provided below in the code example.

```javascript
IzsWidget.init('#izsWidget', {
  apiKey: 'sfe6efef87876efeeefe', //required
  pdlId: 'q937A00000oln1vQA', // required
  styles: {
    containerMaxWidth: '1366px', // max width of the main widget container, minimum value to set 860px
    tabViewHeight: '600px', // height of the tab section, minimum value to set 400px

    primaryColor: '#373737',
    secondaryColor: '#202020',
    backgroundColor: '#ffffff',
    linkColor: '#ee7a0a',
    selectedColor: '#f89809',
    ratingGreen: '#36C689',
    ratingYellow: '#f7de00',
    ratingRed: '#fe5858',
    ratingGrey: '#dadada',

    titleFontSize: '26px',
    titleColor: '#202020',
    subtitleFontSize: '14px',
    subtitleColor: '#202020',

    standardTextSize: '16px',
    headingTextSize: '16px',
    testimonialTextSize: '19px',
    testimonialProviderTextSize: '12px',
    tableHeaderTextSize: '12px',
    documentsTableHeaderTextSize1: '16px',
    documentsTableHeaderTextSize2: '13px',
    tableTextSize: '15px',
    tableSubTextSize: '12px',

    izsButtonTextColor: '#ee7a0a',
    izsButtonBackgroundColor: '#fff',
    izsButtonFontSize: '16px',
    izsButtonBorderColor: '#ee7a0a',
    izsButtonBorderRadius: '10px',

    reportButtonTextColor: '#fff',
    reportButtonBackgroundColor: '#ee7a0a',
    reportButtonFontSize: '16px',
    reportButtonBorderColor: '#fff',
    reportButtonBorderRadius: '10px'
  }
});
```

## Info

There is no mobile optimized view for the widget. The notification about that will be shown on mobile devices instead of the widget content. You can hide the section with the widget if the device screen width or height is less than 680 pixels (below this value the notification is displayed).

## Support

If you encounter any issues or have any questions, please reach out to our support team at info@izs-institut.de
