# Pre-work - *Memory Game*

**Memory Game** is a Light & Sound Memory game to apply for CodePath's SITE Program. 

Submitted by: Ayushmaan Gandhi

Time spent: **6.5** hours spent in total

Link to project: https://glitch.com/edit/#!/malleable-airy-handball

## Required Functionality

The following **required** functionality is complete:

* [x] Game interface has a heading (h1 tag), a line of body text (p tag), and four buttons that match the demo app
* [x] "Start" button toggles between "Start" and "Stop" when clicked. 
* [x] Game buttons each light up and play a sound when clicked. 
* [x] Computer plays back sequence of clues including sound and visual cue for each button
* [x] Play progresses to the next turn (the user gets the next step in the pattern) after a correct guess. 
* [x] User wins the game after guessing a complete pattern
* [x] User loses the game after an incorrect guess

The following **optional** features are implemented:

* [x] Any HTML page elements (including game buttons) has been styled differently than in the tutorial
* [x] Buttons use a pitch (frequency) other than the ones in the tutorial
* [x] More than 4 functional game buttons
* [x] Playback speeds up on each turn
* [x] Computer picks a different pattern each time the game is played
* [ ] Player only loses after 3 mistakes (instead of on the first mistake)
* [ ] Game button appearance change goes beyond color (e.g. add an image)
* [ ] Game button sound is more complex than a single tone (e.g. an audio file, a chord, a sequence of multiple tones)
* [ ] User has a limited amount of time to enter their guess on each turn

The following **additional** features are implemented:

- [ ] List anything else that you can get done to improve the app!

## Video Walkthrough (GIF)

If you recorded multiple GIFs for all the implemented features, you can add them here:
![](gif1-link-here)![Project gif(win)](https://user-images.githubusercontent.com/66655968/160678033-9fbdefec-428e-4727-a6e2-d011c7d58352.gif)

![](gif2-link-here)![Project gif(lose)](https://user-images.githubusercontent.com/66655968/160678124-187f8bbd-202b-43af-b0c1-af75518f4e61.gif)

![](gif3-link-here)![Project gif(diff pattern)](https://user-images.githubusercontent.com/66655968/160678227-873380de-4f03-40d2-93b7-216b16ddc29f.gif)

![](gif4-link-here)

## Reflection Questions
1. If you used any outside resources to help complete your submission (websites, books, people, etc) list them here. 
I referred to the ‘JavaScript Random’ page on W3Schools (https://www.w3schools.com/js/js_random.asp) in order to understand how to randomly pick an integer within my desired minimum and maximum value. I applied the line of code that I learned here (line 17) into my randomnumber() function, with which I was able to generate a new random pattern at the beginning of every game.

2. What was a challenge you encountered in creating this submission (be specific)? How did you overcome it? (recommended 200 - 400 words) 
I had a fair amount of trouble with the second optional task of speeding up the game. After I updated the clueHoldTime constant to a variable, I went to my playClueSequence function and coded “clueHoldTime *= .9” inside of the for loop, so that hold time would multiply itself by .9 every time, thus slightly decreasing with each turn. However, after running the code, I noticed that the hold time would still be sped up even when I would start the game over. Essentially, the hold time would not reset itself to 1000 every time I restarted the game, but rather it would pick up where the last game left off. In order to get around this issue, I tried initializing the clueHoldTime to 1000 in my playClueSequence function before the for loop started. However, this simply made it so that the hold time would decrease with every single new clue, rather than decreasing after every turn. I finally overcame this issue by coming to the conclusion that I must initialize clueHoldTime before the playClueSequence function even takes place. This way, the hold time could reset to 1000 at the start of every game, and the hold time would decrease with every turn rather than every clue. In order to make this happen, I initialized clueHoldTime in my startGame function right before I called my playClueSequence function. This worked as I expected since the hold time sped up on every turn instead of guess, and it reset to 1000 every time I started a new game.

3. What questions about web development do you have after completing your submission? (recommended 100 - 300 words) 
Are HTML, CSS, and JavaScript the industry standard for web development, or are other languages also frequently used? In a work environment, is it common for someone to specialize and focus on one of the three languages (HTML, CSS, JavaScript) for a given project, or are they expected to develop code in each of the three languages for said project? What strategies are most effective in debugging your code during web development? Most of my coding experience has been with Python, and when assigning a variable in Python, you don’t have to explicitly put the “var” keyword. The same goes for constants. How come you have to explicitly put “var” or “const” when declaring these in JavaScript? Are there any benefits to this, or is it purely just relevant to the syntax?

4. If you had a few more hours to work on this project, what would you spend them doing (for example: refactoring certain functions, adding additional features, etc). Be specific. (recommended 100 - 300 words) 
If I had a few more hours I would have chosen to create different difficulty levels to the game. The player would first be prompted with whether they want “easy”, “medium”, or “hard” mode. These prompts would be presented as buttons. The user would click the button of their choice and the corresponding game would then be displayed. In the “easy” mode, the clue playback would not speed up as the turns progress. In the “medium” mode, the clue playback would speed up. Essentially, this is the mode that I have already created for the pre-work. In the “hard” mode, the clue playback would speed up and there would be no audio when the buttons are clicked, so players will have to rely solely on their visual memory. Another implementation that I would make is allowing the player to continue the game until they make a mistake. Instead of there only being eight turns, players would have the opportunity to see how many turns they can last until they falter.



## Interview Recording URL Link

[My 5-minute Interview Recording](https://www.loom.com/share/8533703f9b954381af84247d9f974aac)


## License

    Copyright [Ayushmaan Gandhi]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
