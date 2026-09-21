# Quiz Application

A Java desktop quiz game with a Swing GUI. Has a login screen, a rules page, the quiz itself with a countdown timer per question, and a score screen at the end.

## What it does

User enters their name on the login screen, reads the rules, then goes through 10 multiple choice questions. Each question has a 20-second timer. There is a lifeline option to skip a question. At the end, the score screen shows how many you got right.

## Stack

Swing (javax.swing) - the entire UI across four screens: Login, Rules, Quiz and Score. Each screen is its own JFrame. JRadioButton grouped with ButtonGroup handles the multiple choice options so only one can be selected at a time.

AWT (java.awt) - layout, fonts, colors and background images. The quiz screen loads a full-width banner image as a JLabel background.

Timer (java.util.Timer with javax.swing.Timer) - counts down 20 seconds per question. The timer updates a label on screen each second and auto-submits if the user doesn't answer in time.

ActionListener - handles all button clicks: next question, submit answer, lifeline. The quiz logic (checking the selected answer against the correct one, updating the score) all runs inside actionPerformed.

ImageIcon - loads the login background, quiz banner and score screen image from the icons folder.