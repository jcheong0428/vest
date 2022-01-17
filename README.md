# VEST: Video Event Segmentation Tool

The Video Event Segmentation Tool (VEST) is an open-source software for annotating temporal events in video clips.

You can annotate event "segments" with start & end times or event "points" that indicate only the start time of an event.

# Basic instructions
### 1. Installation  
Easiest way to use VEST is through the online app at [https://jinhyuncheong.com/vest/vest.html](https://jinhyuncheong.com/vest/vest.html). Alternatively, you can clone this repo and launch `index.html` in your browser. 

### 2. How to use
- Load your video file using the [Choose file] button
- Define the name of the event segments and points using the [Add segment buttons] and [Add point buttons]. This will create buttons with your event names on them.
- Click your label buttons to annotate segments or events as you watch your video.
- When you are finished, save your annotations by using the [Download results] button.

# Analyzing VEST outputs
VEST saves the segmentations into a json file that can be loaded in most coding languages (e.g. Python, R). Here is a sample code to load the outputs in Python [[Gist](https://gist.github.com/jcheong0428/785394bd3710e309790c1a99170d7da5)]. 

"""Python
import pandas as pd

def parse_vest_json(f):
  """Parse json output from VEST

  Args:
    f: path to VEST json output
  
  Returns:
    segmentations dataframe
    points dataframe
  """
  seg_df, pts_df = pd.DataFrame(), pd.DataFrame()

  df = pd.read_json(f, lines=True)
  seg_cols = [col for col in df.columns if 'segment' in col]
  _seg_df = df[seg_cols].dropna().T
  for rowix, row in _seg_df.iterrows():
      seg_df = pd.concat([seg_df, pd.DataFrame(row.values[0],index=[row.name])])

  pts_cols = [col for col in df.columns if 'point' in col]
  _pts_df = df[pts_cols].dropna().T
  for rowix, row in _pts_df.iterrows():
      pts_df = pd.concat([pts_df, pd.DataFrame(row.values[0], index=[row.name])])
  return seg_df, pts_df


path_to_file = "/content/segmentation_results.json"
seg_df, pts_df = parse_vest_json(f=path_to_file)
display(seg_df, pts_df)
"""


# Screenshot
![Screenshot of VEST in action](paper/Figure1.png?raw=true "Screenshot of VEST in action.")

# License
VEST uses [peaks.js](https://github.com/bbc/peaks.js/) and abides by its [license](https://github.com/bbc/peaks.js/blob/master/COPYING).
