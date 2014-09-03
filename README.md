Guide on how to set the pagetype for Google Tag Manager
=================================

Implementation guide for proper Google Tag Manager pagetype code. In advance of implementing the Google Tag Manager pagetype code you should check if 1. the [Google Tag Manager container code](https://github.com/orangevalley/GTM_standard) is working properly and 2. you have received an instruction document from you Orangevalley point of contact regarding the preferred parameter values. When referred to Google Tag Manager pagetype code you should use the script within GTM_pagetypeScript.js.

## Background
Google Tag Manager is a free tool that eliminates tedious code-editing tasks for your website. For tracking pagetypes the Google Tag Manager additional information about the page. This is done by using the Data Layer.

The pagetype value can be used for multiple purposes. For instance it can be set for Content Grouping within Google Analytics, for setting up affiliates, and setting up rules to fire on within the Google Tag Manager interface.

This value needs to be available on all pages of the website and is always placed above the Google Tag Manager container code. The basic syntax for setting an event, then, is as follows:

```html
<script>
 dataLayer = [{'pagetype': 'pagetype_name'}];
</script>
```

##### Explanatory notes
| Property       | Example   | Description                                                     | Required |
| -------------- | --------- |---------------------------------------------------------------- | -------- |
| pagetype          | pagetype     | Fixed value                                                     | Yes      |
| pagetype_name     | home    | Value should follow the specification received per e-mail | Yes      |


#### Example
```html
<!-- Google Tag Manager container -->
<script>
 dataLayer = [{'pagetype': 'home'}];
</script>
<noscript><iframe src="//www.googletagmanager.com/ns.html?id=GTM-XXXXX"
height="0" width="0" style="display:none;visibility:hidden"></iframe></noscript>
<script>(function(w,d,s,l,i){w[l]=w[l]||[];w[l].push({'gtm.start':
new Date().getTime(),event:'gtm.js'});var f=d.getElementsByTagName(s)[0],
j=d.createElement(s),dl=l!='dataLayer'?'&l='+l:'';j.async=true;j.src=
'//www.googletagmanager.com/gtm.js?id='+i+dl;f.parentNode.insertBefore(j,f);
})(window,document,'script','dataLayer','GTM-XXXXX');</script>
<!-- End Google Tag Manager -->

## Change History

* 1 (September 3 - 2014): Initial release of standardised Google Tag Manager pagetype code
