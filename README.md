# Shrapnel Engagement Details UI Tool (Unreal Engine 5)

I created the Engagements Details UI tool so that game testers on Shrapnel could get actual information about the real behaviors of weapons, to check against expected behavior in a quantifiable way.
Mainly:
1. There were about 90 character progression perks that needed to be tested, almost all of which had some minor effect on gunplay that the tool could validate quickly.
2. Design wanted to get more information about TTK and accuracy for tuning different weapons.
3. There were some pernicious issues with hit registration that I wanted to get better real-time-footage of.

<img width="1067" height="593" alt="image" src="https://github.com/user-attachments/assets/ddd88049-ca8b-4033-9ae7-b5060392ee82" />

It tracks: Time to kill from engagement start, overall accuracy over the course of an engagement, and the specific damage events (including the cause and damage value of each of them).

## Usage Directions

1. Recognize that this is a tool built for a specific game, and suffers from some tight coupling. You will not be able to use it out-of-the-box (and doing so would also infringe on NeonMachine's copyright). Feel free to take a look around however to consider how you might approach this problem in your own projects. You will likely have to debug a bit.
2. There is a cheat manager included. That is what allows players to summon the widget during gameplay. This only tool only works on Unreal Engine Test or Dev builds. You'll have to replace the cheat manager of the player with the provided one.
3. to activate the tool, use the following commands:
'''enablecheats'''
'''SummonDUITool'''
4. Once activated, shoot at an enemy (you'll have to redefine how it detects what is an enemy in the blueprint, because it looks for Shrapnel's specific class) to start the engagement.
5. The engagement will continue until the enemy dies (again, a lot of this behavior is specific to Shrapnel).
6. You can use a screen capture tool to review engagements, and see how TTK, accuracy, and damage instances changed over the course of the engagement.



---
DUI Tool - created for Neonmachine. Displayed with permission.
