# teacamera

I was unable to get this program to compile at all, it seems to be having the same issue I was having with my own program and would launch the emulator and then error out immedietly with no reasoning or explanation as to why.

As such I did my best to look over your code and found some errors that even when fixed, didn't allow for it to run.
At the end of your code you are adding things to the windows you created, since you created tabGroup, it should be the one that is having the tabs added to it at the end with any other things being added to the windows prior. It should look something like this:
win1.add(nav);
win2.add(options);
tabGroup.add(tab1); // you connected this tab to win1
tabGroup.add(tab2); // you connected this tab to win2
tabGroup.open();

Also when listing the various tea colors you left out a ' before the final color, which would have prevented anything past that point to run as written.
how you had it before for this specific one was:
#3D2B1F'
when it should be:
'#3D2B1F'

These were the only major issues that I was able to find since it refused to compile at all for me. I hope that this can help.

and the extra utility code was that of the camera from the book.
