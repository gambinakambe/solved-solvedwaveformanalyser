Download Link: https://assignmentchef.com/product/solved-solvedwaveformanalyser
<br>
The assignment focuses on using ArrayLists to store collections of values. Mostly, the programs read data from a file and construct an ArrayList of the data. They then do things to each element of the list, or manipulate the list in more complicated ways.

The assignment is a bit shorter than usual because of the terms test. WaveformAnalyser is like PowerAnalyser from assignment 4, but reads numbers from a file into an ArrayList and analyses the signal. It also displays the waveform, displays the amplitude, shows the distortion, highlights the peaks, draws the upper and lower envelopes (the lines linking the peaks), and lets the user edit out parts of the waveform.

To Submit:

Submit your best version of WaveformAnalyser.java by the due date. Remember to include files for all of the classes you modified, and don’t forget to click the button for the final step of the submission process after you have uploaded the files (which does some automated checking for you).

You may work in pairs for the Core and Completion parts, but if you do, youmust include a comment at the top of your program saying who you worked with. You must do the Challenge parts on your own. Remember to submit your Reflection.txt file.

Preparation

Download the zip file and extract it to your home folder. It should contain templates for the Java program you are to complete, along with data. Read through the whole assignment to see what you need to do. You can run the demo programs on the ECS lab computers. Look again at your answer and/or the model answer to the PowerAnalyser program from assignment 4 and go over the code examples in slides from the lectures on ArrayLists. Waveform Analyser Many music players will allow you to display the sound being played. One of the displays is typically the waveform.

For this program you will write a very simple waveform display. There are several things about a waveform that one may be interested in:The highest and lowest (most negative) points on the waveform are significant.The distortion level: if the signal is too large (positive or negative), the sound might get distorted. Reporting on the points gone over the distortion level becomes then useful.The peaks of the waveform which are all the points that are greater than both their neighbouring points.The upper envelope which is the graph that links all the peaks of the signal.The lower envelope which is the graph that links all the “negative” peaks (the peaks below the zero line).Editing the waveform, eg by scaling it down so it is all below the distortion level, or removing some segments of the waveform.WaveformAnalyser is an extension of the PowerAnalyser program from assignment 4 which displays a waveform and performs some analysis and editing. However, instead of reading data directly from the user,WaveformAnalyser reads the data from the file (eg waveform1.txt andwaveform2.txt) into an ArrayList stored in the waveform field, which means that it can analyse the data more easily and in more different ways. It can also cope with much larger sets of numbers. Another difference with the PowerAnalyser program is that the values can benegative and the signal swings above and below zero. The code that sets up and responds to the buttons is provided for you – the parts of the program you have to complete are the ones involving the ArrayList The constructor sets up an interface with ten buttons, and responds to the mouse:Read Data: [core] reads data from a waveform file into an ArrayList field.Display Waveform: [core] displays the waveform as a line graph.Report Distortion: [core] prints out the fraction of time the signal is distorted.

Spread: [completion] displays the maximum and minimum values with two horizontal lines (on top of the waveform).Display Distortion: [completion] displays a waveform that highlights in red the distorted values.Peaks: [completion] plots the peaks with small green circles.

Normalise: [challenge] normalises all the values by scaling them down so there is no distortion and redisplays the waveform.Envelope: [challenge] displays the upper and lower “envelope” of the displayed waveform by connecting all the peaks.Save: [challenge] saves the current waveform values into a file.The mouse will allow the user to select a region of the waveform to delete it.Core For the core, you should complete the following methods:doRead(): creates an ArrayList stored in a field, asks user for a waveform file and reads data from the file into the ArrayList.

doDisplay(): Displays the waveform as a line graph, as in the demo. The horizontal line representing the value zero should also been drawn. If the lines go off the window, that is OK.

doReportDistortion(): Computes and prints the faction of time the signal is distorted. This fraction of time is defined as the number of distorted values, divided by the number of values. A distorted value is defined as one that is either greater than the positive value of the threshold or less than the negative value of the threshold. Note that the threshold value is stored in the constant field THRESHOLD.Completion For the completion, you should complete the following methods:doSpread(): Displays two horizontal lines on the waveform, one green line for the maximum value and one red line for the minimum (most negative) value, as in the demo.

doDisplayDistortion(): Shows in red the distorted part of the signal. This methods draws in red every line that has either end point beyond the distortion threshold.

doHighlightPeaks(): plots the waveform and the places small green circles on all the peaks. A peak is defined as a point that is greater or equal to bothneighbouring points. Note the size of the circle is stored in the constant fieldSIZE_CIRCLEChallenge: For the challenge, you should complete four of the five following methods:doNormalise(): Finds the largest value (positive or negative) in the waveform, and scale all the values down so that the largest value is now equal to the distortion threshold. Then redraws the waveform.

upperEnvelope(): displays the upper envelope with green lines connecting all the peaks, as in the demo.

lowerEnvelope(): displays the lower envelope with red lines connecting all the “negative” peaks, as in the demo.

doSave(): asks the user for a filename and saves the current waveform to that file.

doMouse: Lets user select a region of the waveform with the mouse, deletes that section of the waveform, and redisplays the waveform.