# TerminalImageViewer

Small Java program to display images in a (modern) terminal using RGB ANSI codes and unicode block graphic characters

Algorithm (for each 4x8 pixel cell mapped to a unicode block graphics character):

1. Find the color channel (R, G or B) that has the biggest range of values for the current cell
2. Split this range in the middle 
3. Average the colors above and below and create a corresponding bitmap for the cell
3. Compare the bitmap to the assumed bitmaps for various unicode block graphics characters


Usage:

```
javac TerminalImageViewer.java

java TerminalImageViewer [-w <width-in-characters>] <image-filename-or-url>

```

![Examples](http://i.imgur.com/8UyGjg8.png)

If multiple images match the filename spec, thumbnails are shown.

![Thumbnails](http://i.imgur.com/PTYgSqz.png)
