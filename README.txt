INFO 6044 Game Engine Frameworks (Final Exam)
Evan Sinasac - 1081418

CONTROLS:
WASD		- Free fly camera
QE		- Raise and lower camera
Mouse		- Aim camera
Left Arrow Key	- Move your ship left
Right Arrow Key	- Move your ship right
Enter		- Start the game (can't move ship until you do)
Esc		- Close the game
Space		- Fire missile

Built and compiled in Debug and Release in x64 in Visual Studios 2019 Community.  Very, very slow in Debug.  Unless actually debugging, best to run in Release mode.

The bombs that the Space Invaders drop still need some work, I was trying to seed them by time but as it turns out, when everything is running on the same timer, the seed is going to be almost the same every time.  You can see that it is actually somewhat random, as I saw there were times when almost every alien dropped a bomb except for like 5 of them.  I also could not simulate the "wave" motion from the old game.  I don't remember how I learned this, but I do know the original effect and speed up was from resources being cleared as you destroyed the Invaders, which allowed the game to process fewer things faster.  I think the idea to simulate it for this was to use something like the animation controller we started working on in class and will be needed for the final project and have the Invaders move sequentially.  Between how slow I usually work and the kerfuffle I emailed you about, I did not go back to try and add it in.
Also, I was getting read access violations when I was trying to delete the bombs from the aliens, so they are just hiding once they reach the bottom.  There's a small chance that the longer the game is going, the laggier it'll get depending on the bombs, but I'm pretty sure I have it set up to not draw anything that's "not visible", so it should be fine.

Otherwise, I think I covered everything other than the bonuses.  Oh!  Also, when starting the game, please try to move the mouse and aim the camera around a bit before moving it with WASD.  This has been a little feature ever since implementing this fly camera, but it doesn't apply the * deltaTime to the cameraMoveSpeed until after the aim has been updated once.  Still can't figure that one out.  And nothing in the game will move until you press Enter, for the static screen, but you can move the camera around to inspect the models, if you so choose.

Thank you.  This semester has really taught me a lot and has re-invigorated my passion for programming.  I can't wait to actually see you in person next semester!  Happy Holidays!  :)