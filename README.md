# import and plot Gromacs xvg files
These two Matlab functions imports and plots the type of .xvg files that the MD package Gromacs uses for some of its text-based data output. The functions tries to read the names/labels of the plotted data columns, as well as the axis-labels. Examples on how-to import and plot can be found in the functions. Note that Data is the default name for the output data for both functions. The import_xvg function imports the Data, and is itself called by the plot_xvg function. Note that with this function you can also set the x/y-ranges of the plot.

Examples on how to import Data (and plot it) 

Data = import_xvg('filename.xvg') 

Data = import_xvg('filename.xvg','plot')

Examples on how to plot (and import Data) 

plot_xvg('energy.xvg') 

Data = plot_xvg('energy.xvg',[1 5 3]) % Will plot the 5th and 3rd column vs. the 1st one

Data = plot_xvg('energy.xvg',[1 5 3],[0 200]) % Will also set the X-axis to be between 0 and 200 

Data = plot_xvg('energy.xvg',[1 5 3],[0 200],[0 1.5]) % Will also set the Y-axis to be between 0 and 1.5

