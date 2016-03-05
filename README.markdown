******************************************************************************************
Hoa Karlotcha

Mondriaan’s Victory Boogie-like Generator 

2013-03-05
******************************************************************************************



******************************************************************************************
HOW TO USE IT? 
******************************************************************************************
I only used web technologies: open "open_me.html" in your favorite web browser (it 
is much better on GOOGLE CHROME though) to see it! 

It is a generator of random images: to generate a new one, press any key of your
keyboard.

I added some animations for the first 5 seconds. After it you can watch the new
image. 

You can also see it on my blog: 
http://karlotcha.herokuapp.com/blog/2013/02/12/mondrian-returns/

******************************************************************************************
HOW DOES IT WORK ? 
******************************************************************************************
I did it in Javascript and used two libraries: jQuery (a common library to write nice 
Javascript) and D3.js to manage the display.

My script is "script.js". 

I used a square of 600px I divided in smaller squares (I called them "Cells") of 6px.
All these cells are regrouped in a "MATRIX".

The main idea is to go through this matrix (lines 128 - 129 - 130) to apply successively 
3 functions: horiz_propa, verti_propa and normal_propa ("propa" for "propagation").

These first two functions "agglutinate" cells to create some horizontal and vertical patterns.
After that, normal_propa agglutinates cells staying inside the previous patterns (cells have a 
attribute "used" to know if they can be agglutinate by normal_propa). 

These functions use extensively a random number generator to agglutinate the cells. By comparing 
a random number to a fix number (used as a "probability" - I only used integers so it is not 
real probabilities), the functions decide to continue to "propagate" or not. 
These 3 functions use a lot of different parameters to adjust the patterns to be comparable to 
Mondriaan’s Victory Boogie. 

'draw' is a function to draw the different rectangles (and is called by propagations functions). 
I used again some random number generation to decide which color to pick in a set a few colors 
I get from the picture of Mondriaan’s Victory Boogie. 'draw' is also managing the animation for 
the first 5 seconds. 

Finally, I hide each angle of the whole creation with 4 triangles (I called this step "finish move"). 

******************************************************************************************
THANK YOU
******************************************************************************************
My participation is really modest but I had a lot of fun doing it! Thank you!
