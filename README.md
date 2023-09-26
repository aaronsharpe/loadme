# LoadMe
This is a helper to load data generated by [MeasureMe](https://github.com/spxtr/measureme)

# Installation
Modified from MeasureMe.

Installing python projects can be a real pain. Here is how I personally set up lab computers to use measureme, but other ways can work fine. I do not like to use tools such as Conda or pipenv, because I find them to be a real headache.

    1. On Windows computers I typically use GitHub Desktop for git.
    2. I install the latest Python 3 from python.org, system wide. I make sure that I can run Python from the command line. On Windows this sometimes means running py or py3 or python3. I feel like it changes every time I do it, so just try them all and see what sticks. Later versions of Windows will annoyingly pop up some app store if you don't use the right incantation. Ignore that nonsense.
    3. Next, make sure pip exists with python -m ensurepip. Again, pip might have some odd path like pip3.
    4. pip install jupyterlab.
    5. Download and install loadme. Git clone, then pip install -e.
    6. Test measureme by following the basic usage section below!

# Basic usage
TODO: fill this out