# cherry-picker

Event log filter that allows milti-range filtering of variants and activities.

## Structure

This repository contains 2 jupyter notebooks, **cherrypicker** and **cherrypicker_filter_only**. The **cherrypicker_filter_only** saves the filtered log to a .xes file for further processing is some other process mining tool, whereas the **cherrypicker** shows how the log can be used for process mining directly in PM4Py.

## Usage

Regardless of the notebook chosen, the only user input that is required are the name of the input log as *input_file* and the variables *custom_path_range* and *custom_activity_range* in the second cell. 

Each of the range variables must be an array of tuples in form *\[(lower, higher),(lower,higher),...\]* where *lower* and *higher* are the percentage boundaries for the filter as numbers between 0 and 1, e.g. `custom_path_range = [(0,0.2),(0.8,1)]` would mean to choose 20% least frequent **and** 20% most frequent paths.

After providing this input, the user has to **run all cells**.

The **cherrypicker_filter_only** saves the generated log as *exportedLog.xes* in the same directory as the notebook.
