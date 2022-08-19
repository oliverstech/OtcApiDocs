# Embedding Videos in WinForms with OTCAPI
**Note: this guide applies to WinForms .Net Framework.**

This page will show you how to embed videos within your Windows Form Application easily with the OTCAPI.

## Step 1: Add a web browser
First of all, you need to add a browser control to your form. To do so, simply search 'browser' in the toolbox and add it to your project. 

![image](https://user-images.githubusercontent.com/89639839/185601746-4d4d77d8-7a39-454d-8e95-8d8b3f0547e2.png)


Adjust the size to how to like it, then take note of the 'Width, Height' in the properties (listed as Size).

![image](https://user-images.githubusercontent.com/89639839/185601889-8aaba548-784f-4ebe-9e2d-838b6429287b.png)

## Step 2: Making an API link
Secondly, you need to make an API link with the [Video Embed Maker for WinForms](https://https://maker.video.otcapi.ml/).

1. Paste your video link in the 'Video URL' field.
2. Type your width and height from earlier in the appropriate fields. (Example: 800 and 450)
3. If you'd like to set a custom background for the page (which is displayed if the video doesn't load, or the size doesn't correctly match), you can do so by entering the hex in the 'Background Hex' field (please exclude the #). You can find your desired colour's hex with [this tool](https://g.co/kgs/jo82Xj).
4. Choose whether you'd like to show the video controls and whether the video should autoplay on form launch/show.
5. Press 'Generate Link'. You'll see the link appear in the field beside.
6. Click 'copy to clipboard' to copy the newly-generated link. You can now continue to the final step.

## Step 3: Using within your form
Lastly, you need to paste the newly-made API link within your Browser Control's URL property. 
### With Designer
![image](https://user-images.githubusercontent.com/89639839/185602844-aea1aac1-6c70-43bd-be48-e9a7abd5266a.png)
### With Code
Change webBrowser1/WebBrowser1 to whatever your Browser Control's name is.

C#:
```cs
webBrowser1.Url = new Uri("YourApiLinkHere");
```
VB:
```vb
WebBrowser1.Url = New Uri("YourApiLinkHere")
```

#### You're Done!
