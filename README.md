# LastFM Signature

![alt text](https://lfm-sig.herokuapp.com/sig.php "Live preview")

Simple class for those who want to make their signature cool. 
Features:

1. Custom font, font size, color, offset 
2. Custom image, local file or URL 
3. Varity. You can make many cases of images with custom settings and return them randomly

### How to
1. Include class to new `.php` script or append code to this class. 
2. Build image case using `buildPicture()`.
3. Then just run script via `run()` with your username.

For example
```PHP
$creator = new LFMNowPlaying();
//For local image with standart offsets
$creator->buildPicture("DancingScript", 16, "#FF0000", "rin.png"); 
//For hosted image with custom offset
$creator->buildPicture("Permanent Marker", 16, "008cf0", "http://i.imgur.com/VRUiYl7.png", 8, 130); 

$creator->run("mr7kill");
```
Make sure that `fonts` dir contains used fonts and pictures located in `pics` directory. Or you can use `setFontsPath()` and `setPicsPath()` to set your default directories. 
```PHP
$creator = new LFMNowPlaying();
$creator->setPicsPath("MyPictures/");
$creator->buildPicture("DancingScript", 16, "#FF0000", "rin.jpeg");
$creator->run("mr7kill", "Currently playing: ", "Was playing: ", " / ");
```
You can read script documentation for additional information. 


### [Live Demo](http://sig-lfmgen.rhcloud.com/json.php)
