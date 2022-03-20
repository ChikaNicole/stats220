# Hello!
*This is Nicole's website!*


## Some information about me:
I am an university student and my major is **statistics**. I am an native speaker of Chinese and I can also speak English and Japanese also with some German and Korean because I am an amateur of languages~ I like music especially J-POP and also coding!

## This is `the first time that I use code to make a meme!`
*Below is a meme I made using the R package [{magick}](https://cran.r-project.org/web/packages/magick/vignettes/intro.html) of saga(who is a character in Arknights).

![my_meme](https://user-images.githubusercontent.com/100815234/157364901-0cd1a4f4-7738-4d11-9266-0f3524b31efc.jpeg)

## My motivation of making this meme
1. Saga is a very popular character in Arknights.
2. I got the idea that she likes eating natto rice and she always want to eat which is very funny from the story line so I screenshotted her and make this meme.


## How my meme is new/original 
I use my screenshot to make the first picture of my meme and I use another screenshot of a video from a website called bilibili and then put the two pictures together with what I think she's going to say on the right-hand side to make this meme so that it is a new/original meme.

## The r code that I used to make the meme
‘’‘
library(magick)

#picture one
hungry_saga <- image_read("https://www.meme-arsenal.com/memes/f518b1afdbdfa0c7993e3fc27eb1ebdc.jpg") %>%
  image_scale(500)

#picture two
full_saga <- image_read("https://www.meme-arsenal.com/memes/4fc680be8c8554160c6694860b50f4be.jpg") %>%
  image_scale(500)

#text_square one
saga_text1 <- image_blank(width = 500, height = 500, color = "#e6f7ff") %>%
  image_annotate(text = " I want to eat Natto rice!", color = "#000000", size = 40, font = "Gill Sans", gravity = "center")

#text_square one
saga_text2 <- image_blank(width = 500, height = 500, color = "#e6f7ff") %>%
  image_annotate(text = "That's exactly what I want!", color = "#000000", size = 40, font = "Gill Sans", gravity = "center")

first_row <- c(hungry_saga, saga_text1) %>%
  image_append()

second_row <- c(full_saga, saga_text2) %>%
  image_append()

saga <- c(first_row, second_row) %>%
  image_append(stack = TRUE)

print(saga)

image_write(saga, "my_meme.png")
’‘’
