Lecture 6:  ASTROPY
===================

## Homework updates

Your **homework/Homework-01.ipynb** file needs to be copied to your ursa home directory. You can either use **cp** if you
are on the lab machines, or **scp** (alternatively **rsync**) on your remote laptop.
```
	ursa%    cp Homework-01.ipynb $HOME
	
	laptop%  scp Homework-01.ipynb $USER@ursa.astro.umd.edu:

	laptop%  rsync Homework-01.ipynb $USER@ursa.astro.umd.edu:
```
where *$USER* is your username on ursa.  As you can see, there 

## Updating your *astr288p* repo 

As always, update your git repo. If you modified your notebooks, you will notice some conflicts.

Is there perhaps a better solution to this...
```
   cd ~/ASTR288P/astr288p      # make sure you are in one of the 'astr288p' directories
   git status                  # notice something was modified?
   git pull                    # warnings are possible here if there are conflicts
   git stash                   # those modified files are "stashed"
   git pull                    # now get the updates
```

One possible option is to always work on your notebooks in a backup:
```
   git pull
   cp -a notebooks notebooks-trials    # copy to a trials tree
   jupiter notebook                    # work in the notebooks-trials
```   

Another option is to work in a git branch:
```
   git branch trials                   # create a new branch
   git branch                          # see which branches you have
   git branch -r                       # or which branches are on the remote
   git checkout trials                 # go to the new branch
   jupiter notebooks                   # work in the current notebooks (branch)

   
   git checkout master                 # go back to the master version
   git pull                            # get the official updates
```

## testing your modules in python

A new pure-python script was added to the ```notebooks``` directory to identify potential problems
before you start a notebook (although some of them are on purpose):

```
cd astr288p/notebooks
./testing.py
```

## ASTROPY

A community Python Library... 

### Official references

* Home page:   http://www.astropy.org/
* Affiliated packages:  http://www.astropy.org/affiliated/
* Developers (git) : http://docs.astropy.org/en/stable/development/workflow/development_workflow.html



### Astronomical Data


* Images:  FITS files.  (a new file **ngc6503.cube.fits** was added to your astr288p/data directory)
  * **ds9**: http://ds9.si.edu/site/Download.html
    Supports 3D cubes: a 3D slicer comes up autmatically. To bring up a spectrum, select Edit->Region, double click the region (or Region->Get Information)
    and set Analysis->Plot3D (save in Preferences -> Region -> Auto Plot 3D to make it persistent)
  * **ginga**: https://ginga.readthedocs.io/en/latest/
    Supports 3D cubes, but perhaps not as intuitive as ds9
  
* Tables  (astropy http://docs.astropy.org/en/stable/io/unified.html)
  * ascii tables
  * FITS tables
  * VO tables
* 


### Reminder on installing software in python:

Various ways, in increasing complexity and varying degrees of success:

* conda
```
	conda install ginga
```
* pip
```
	pip install ginga
```
* source
```
	git clone https://github.com/ejeschke/ginga.git
	cd ginga
	python setup.py install
```
Now you should test (perhaps after a **rehash** command if you use the **csh** shell) where ginga lives:
```
	which ginga
```

## Today's notebooks:

* **05-images** :  images in numpy (left over from last week)
* **n6503-case1** : analyzing the new ngc6503.cube.fits using astropy
* **n6503-case2** : analyzing the new ngc6503.cube.fits using radio-astro-tools (experimental)
* **n6503-orbits** : theoretical models what to expect of a galactic velocity field

## Other Interesting Notebooks:

*  GW150914 merging black hole : https://losc.ligo.org/s/events/GW150914/GW150914_tutorial.html

