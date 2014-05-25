## README

### Overview

### Variable Selection

The project instructions for selecting a subset of features from the full dataset reads:

    Extracts only the measurements on the mean and standard deviation for each measurement.

This is somewhat ambiguous so after consulting the description of the features given in the original
dataset and the discussion forums, I think the most reasonable thing to do is select based on these
criteria:

* Extract features for which 'mean()' or 'std()' appears in the names given by the original documentation
* Don't include 'meanFreq()' features and,
* Don't include '*Mean' features such as 'tBodyAccJerkMean' because these aren't what we are looking for

### Style

I follow the [Google Style
Guide](https://google-styleguide.googlecode.com/svn/trunk/Rguide.xml#identifiers) when it comes to
variable naming.

    Don't use underscores ( _ ) or hyphens ( - ) in identifiers. 
    Identifiers should be named according to the following conventions. 
    The preferred form for variable names is all lower case letters and words separated with dots (variable.name), 
    but variableName is also accepted; function names have initial capital letters and no dots (FunctionName); 
    constants are named like functions but with an initial k. 

This is somewhat at odds with the style laid out by Prof. Leek, but as many others have pointed out, other naming
conventions are more widely preferred in by the community.

So I have chosen to name variables using all lower case letters with words separated by dots.
For example, freq.body.gyro.mean.z.averaged
