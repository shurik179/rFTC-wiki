# /r/FTC Wiki
This readme will act as a guide for how to edit the wiki according to guidelines. __If guidelines are not met, your pull request will NOT be fulfilled__.

***Remember, if you want to contribute, make a fork and then submit a pull request to master.***

## Guidelines
 - All files must be written in Reddit-compatible Markdown syntax in Markdown (\*.md) files.
 - The text must adhere to a reasonable definition of *Gracious Professionalism*.
 - It is recommended to write in 3rd person as much as possible. *i.e. Instead of "Our team, XXXXX, tried...", use "Team XXXXX tried using..."*
 - You must adhere to the following file layout unless a compelling reason is provided; major changes to the file layout are discouraged. New files, however, can be added easily given a good reason.
```
rFTC Wiki (From the point of view of the front page)
"Appearance" is to clarify how pages will look to the
user.
(MAIN) /r/FTC Wiki
|-(FOLDER) building
| |-(FOLDER) building-systems
| | |-(FILE) building-systems
| | |-(FILE) matrix-robotics
| | |-(FILE) tetrix
| | |-(FILE) gobilda
| | |-(FILE) actobotics
| | |-(FILE) vex-edr
| | |-(FILE) vex-pro
| | |-(FILE) andymark
| | |-(FILE) rev-robotics
| | |-(FILE) t-slot-extrusions
| | |-(NOTE) It is discouraged to add 
| | | pages for individual building 
| | | components of little importance, 
| | | however, if an important part 
| | | like a ServoBlock is given an 
| | | article, it can be placed into a 
| | | folder with the same name of the 
| | | building system and placed in 
| | | this directory.
| |-(FOLDER) common-designs
| | |-(FILE) common-designs
|-(FOLDER) programming
| |-(FOLDER) ftc-app
| | |-(FILE) wifi-direct
| | |-(FILE) ftc-app
| |-(FOLDER) java-resources
| | |-(FILE) java-resources
| |-(FOLDER) specific-parts
| | |-(FILE) specific-parts
| | |-(FILE) cr-servos
|-(FOLDER) electronics
| |-(FILE) electronics
|-(FOLDER) actuators
| |-(FILE) actuators
| |-(FOLDER) motors
| | |-(FILE) motors
| |-(FOLDER) servos
| | |-(FILE) servos
|-(FILE) frequently-asked-questions
|-(LINK) FIRST Tech Challenge
|-(LINK) /r/FTC
|-(LINK) FTC Forums
|-(LINK) Chief Delphi
```
## Guidelines (continued)
 - Git pulls must have all changes documented; excessive commits are discouraged.
 - All files must start with the latest header format specified in header.md.
 - All files must end with the latest footer format specified in footer.md.
 - All hyperlinks that reference other /r/FTC wiki pages must reference them relative to the subreddit.
 For example:
 ```Markdown
 More information is at [Java Programming](/r/FTC/wiki/programming/java-programming).
 ```
