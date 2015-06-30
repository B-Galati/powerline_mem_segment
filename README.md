# Powerline Memory Segment
Segment for [Powerline](https://github.com/powerline/powerline) showing the current memory usage in percent or absolute values.
![](images/img1.png?raw=true)
![](images/img2.png?raw=true)

## Installation
    pip install .

## Usage
To apply the segment, add the following to the Powerline configuration file:

    {
        "function": "powerlinemem.mem_usage.mem_usage"
    }

For a percentage status, use the ```mem_usage_percent``` callable:

    {
        "function": "powerlinemem.mem_usage.mem_usage_percent"
    }

The format can be configured using the ```format``` argument:

    {
        "function": "powerlinemem.mem_usage.mem_usage_percent",
        "priority": 50,
		"args": {
		    "format": "Mem: %d%%"
		}
    }

One or two highlight groups named ```mem_usage``` and ```mem_usage_gradient``` have to be defined in the colorscheme json file. For example:

    "mem_usage":                 { "fg": "gray8", "bg": "gray0", "attr": [] },
	"mem_usage_gradient":        { "fg": "green_yellow_orange_red", "bg": "gray0", "attr": [] }

## Dependencies
The only dependency is [psutil](https://github.com/giampaolo/psutil).
