# LoadJs 
This is a simple javascript function for lazy-loading images 

#### Functionality 
This is a simple javascript plugin that performs a lazy loading on html elements with ```data-src``` attribute using javascript intersection observer. This attribute is expected to be supplied an image path value. The path supplied will either be added as src attribute of an image ```img``` element or as a background image of a div element depending on the html element upon which it is used. 

#### Usage Sample

```html 

<div data-src="some-image-1.jpg" style="width:400px; height: 400px;"></div>

<img data-src="some-image-2.jpg" style="width:400px; height: 400px;" />

<script src="loadImages.js"/>
<script>
     
    LoadImages();

</script>
```

#### Onclick Events 
This function can be used with onclick events. However, when called, all images within the page will be loaded. A sample of this is shown below.

```html 

<div data-src="some-image-1.jpg" style="width:400px; height: 400px;"></div>

<button onclick="LoadImage()" />

<script src="loadImages.js"/>
<script>
     
    LoadImages({
        threshold: 1,
        rootMargin: "300px"
    });

</script>
```

> All images in the sample above will be loaded into the respective tags once the button is clicked

#### Notice 
This plugin does not perform any form of validation on the image or image path supplied.