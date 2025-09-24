# M 5.2 Lab Caleb Pollock

## Usage

Because this project is using javascript, packages should be installed before running:

```
npm install 
```

You can either view the website through the vscode live preview plugin or by using
a web browser and opening the index.html file.

## Accessibility Lab Answers

### Color

Using the WebAIM constrast checker I tested the text color against the current background. It failed
this test for all variations and had a contrast ration of 2.79:1. So not very high. Results are linked below:
```
https://webaim.org/resources/contrastchecker/?fcolor=2A2A2A&bcolor=008000
```
I adjusted the text to be darker and the green to be lighter until the contrast check passed. I then
added these values to the css of the webpage.    
    
I had the same issue with the background and header text. I did the same test:
```
https://webaim.org/resources/contrastchecker/?fcolor=DDDDEE&bcolor=FFFFFF
```
And changed the colors to something that passed the contrast level required.

### Semantic HTML

The tab order is able to move to most of the links and references, but not through any of the text. This
results in a weird sort of jumping around that results in a bad experience on the web site. I also noticed
that the tab selection misses the comment box, which is not very accessible as a result.    
    
Looking at the html, I saw that the website format was constructed using line breaks and font tags
for headers, which is bad practice html that results in a single block of text in the DOM. This can
be fixed by using p and header tags, which should also help with accessablitity given that those
tags have more built in browser accessablity support.   
   
After updating these tags in the html, the website looks a little better and is also hopefully much
more accessible for users.

### The Images

The images provided lack any alt text. I added this to both images.

### The Audio Player

The audio uses the builtin browser audio player to work. If the browser does not support this,
an additional paragraph tag can be added in the audio tag that can link to the audio file. I added
this to the given audio segment to accomate users in this situation.    
    
For hearing impaired people a transcript to the audo should be provided. Because the audio is rather
short, I added the transcript directly below the audio playback.

### The Forms

I added label elements linked to the input fields of the search form. I then updated the css to hide
the labels. This has the effect of making it eaiser for screen reader users to fill out the form, as 
the label will be read to them associated with the input. It also does not distract the users who are
not using a screen reader.    
     
I additionally associated the labels for the comment form by wrapping them in
label attributes and setting their for tags to the names of the input fields. This
should have the effect of linking the labels to the inputs.

### The Show/Hide Comment Control

I was able to fix the issue of the button not focusing by replacing the div tags with button ones.
This also had the effect of the button activating when the enter key was pressed.

### The Table

The data table provided was minimally constructed. I added th tags for the header elements and
defined the header scope used in the table. I also added a caption tag explaining what the table
was showing. I also added a css element that hid the caption, as it would likely not be important
to users who can already see the table.

### Other Considerations?

One thing that bothers me about this site is how small the text is. I was kind of having
a hard time with it if I didn't focus, so I increased the size a good amount until it
was eaiser to read. I also set the font to bold, which seemed to help with reading it as well.    
     
I also feel like the heading font is probably not the most accessible choice. It looks nice,
but some of the characters are kind of hard to tell apart or distinguish. I set this to the
default font and felt it made things much eaiser to read.    
    
I changed the styling of the comments header in the comments dropdown. This is because changing the
background would have messed up either the visibility of the black or white text. It was eaiser
just to set the white header to black then to cheage the background and a set of text elements.    
    
One thing that would make the website more accessible but I did not impliement would be to
impliment the audio player in javascript instead. This would allow you to provide more 
accessability hooks and have more control over the experience for disabled users.
