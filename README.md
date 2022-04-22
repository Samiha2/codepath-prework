# Pre-work - *Memory Game*

**Memory Game** is a Light & Sound Memory game to apply for CodePath's SITE Program. 

Submitted by: **Samiha Sultana**

Time spent: **5** hours spent in total

Link to project: https://tabby-ablaze-airship.glitch.me/

## Required Functionality

The following **required** functionality is complete:

* [+] Game interface has a heading (h1 tag), a line of body text (p tag), and four buttons that match the demo app
* [+] "Start" button toggles between "Start" and "Stop" when clicked. 
* [+] Game buttons each light up and play a sound when clicked. 
* [+] Computer plays back sequence of clues including sound and visual cue for each button
* [+] Play progresses to the next turn (the user gets the next step in the pattern) after a correct guess. 
* [+] User wins the game after guessing a complete pattern
* [+] User loses the game after an incorrect guess

The following **optional** features are implemented:

* [+] Any HTML page elements (including game buttons) has been styled differently than in the tutorial
* [+] Buttons use a pitch (frequency) other than the ones in the tutorial
* [+] More than 4 functional game buttons
* [+] Playback speeds up on each turn
* [+] Computer picks a different pattern each time the game is played
* [+] Player only loses after 3 mistakes (instead of on the first mistake)
* [+] Game button appearance change goes beyond color (e.g. add an image)
* [ ] Game button sound is more complex than a single tone (e.g. an audio file, a chord, a sequence of multiple tones)
* [+] User has a limited amount of time to enter their guess on each turn

The following **additional** features are implemented:

* [+] List anything else that you can get done to improve the app!
* [+] After winning a pattern, user gets "Mission Complete" picture with winning sound
* [+] After losing a pattern, user gets "You died" picture with losing sound
* [+] User can change the pattern length which increases with every success.
* [+] The game keeps track of the maximum and current scores

## Video Walkthrough (GIF)

If you recorded multiple GIFs for all the implemented features, you can add them here:
![](https://recordit.co/YakoJKRNf2)

## Reflection Questions
1. If you used any outside resources to help complete your submission (websites, books, people, etc) list them here. 
StackOverflow: a lot of searches about Javascript syntax questions
w3schools: html and css questions, guided tutorials about guess users turn

3. What was a challenge you encountered in creating this submission (be specific)? How did you overcome it? (recommended 200 - 400 words) 
The biggest challenge was setting up the timer that limits the time user has to click a button. I wanted a timer that was visible to the player. The timer would end the game if it hit 0, but reset at the start of each round, and wouldn’t start counting down until the sequence was done playing so that the user would always have 10 seconds to enter their guesses (rather than having their time cut short by being forced to wait for the pattern to play).
At first, I thought through the logic of countdown and outlined it on paper. Then, I started experimenting with setInterval() and setTimeout(). It had some troubles combining the two at the same time. I would have several setIntervals run at the same time. I tried stopping them with clearInterval(), but it did not help. I figured that it is probably because of local vs. global variables. I read more questions on Stack Overflow and w3chools to see examples of implementing setInterval(). When I ensured that the logic is correct, I decided that it might be a bug. I went over the relevant code lines and added outputs to the console to identify the bug. After 15 minutes of careful debugging, I found that I was re-assigning variable intId, thus erasing its connection to the corresponding Interval, not being able to stop it later. What helped me is firstly understand how the functions work and interact. I learned setInterval through basic, minimal reproducible examples. I was building up complexity and experimenting with inputs. Once I understood how the function works, its inputs and outputs, I tried implementing it in my program. When I got stuck, I checked for inputs and outputs and then debugged using console.log and simply talking myself through the code.
While taking the class Data Structures and Algorithms, I had encountered similar roadblocks while writing code for homework assignments. While programming this submission, I found myself using the strategies that I've learned in that class to find solutions to issues that arise. I included statements that would print to the console in order to isolate where in the code problems are occuring, and I used boolean variables to force functions to stop running. Of course, I heavily utilized the classic strategy of googling the issue and clicking on the first StackOverflow link that appears.

4. What questions about web development do you have after completing your submission? (recommended 100 - 300 words) 
It was interesting to see how we can create a fun web app to play games. Earlier I created websites incorporating HTML and CSS. I am curious to learn to what extent we could go with HTML, CSS and Javascript? I also how we created the basic HTML and CSS style and emphasized on finishing the functionality with Javascript later. It felt like solving a puzzle and bringing each pieces together in the screen. I would be curious to learn more about creating stylish and user-friendly UI and UX efficiently. Furthermore, I'd like to see how I could incorporate my Adobe Illustrator skills into it. I have heard of some programs that allow you to design the website UI first and then get the HMLT/CSS code for it. I would be curious to see how the code and design interact with each other in such programs.

5. If you had a few more hours to work on this project, what would you spend them doing (for example: refactoring certain functions, adding additional features, etc). Be specific. (recommended 100 - 300 words) 
Firstly, I would want to ensure that anyone can understand and reproduce my code. For this, I would add comments and docstrings. I want my game to be friendly for all devices. Hence, I would turn away from fixed quantities like width: 50px and go to percentages to ensure that mobile users don't have to struggle with gigantic buttons. As a technical challenge, I would attempt using other sounds, such as bass guitar or drums. This would spice up the game and also train musical hearing skills. I would make adding buttons more efficient with a loop, rather than repeating my code many times and copy-pasting the same lines. I could add many other features, but the last, and essential one, is the colorblind mode. My buttons involve many colors, and having a toggle that turns them into colorblind colors would add accessibility to my users.

## Interview Recording URL Link

[My 5-minute Interview Recording](https://www.youtube.com/watch?v=IAuHq5ebz7o)


## License

    Copyright Samiha Sultana

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.