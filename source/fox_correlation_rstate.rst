Fox 2005 resting state method
==============================

**Pre-Processing:**

* compensation of systematic, slice-dependent time shifts; 

* elimination of systematic odd-even slice intensity differences caused by interleaved acquisition

* rigid body correction for interframe head motion within and across runs--> provides a record of head position within and across all fMRI runs. 

* Each fMRI run was intensity scaled (one multiplicative constant over all voxels and frames) to yield a whole brain mode value of 1,000 (not counting the first four frames).


**Atlas Registration:**

* Atlas registration was achieved by computing affine transforms connecting the fMRI run first frame (averaged over all runs after cross-run realignment) with the T2-weighted and average T1-weighted structural images (23). 

* Our atlas representative template includes magnetization-prepared rapid gradient-echo data from 12 normal individuals and was made to conform to the 1988 Talairach atlas.

* To prepare the BOLD data for the present main analyses, each fMRI run was transformed to atlas space and resampled to 3-mm cubic voxels



** Time-series Correlation: **

* temporally band-pass filtered(0.009 < f < 0.08)

* spatially smoothed (6-mm full width at half maximum Gaussian blur).

* Several sources of spurious variance along with their temporal derivatives were then removed from the data through linear regression:

	* six parameters obtained by rigid body correction of head motion
	
	* the whole-brain signal averaged over a fixed region in atlas space
	
	* signal from a ventricular region of interest
	
	* signal from a region centered in the white matter

* Correlation maps were produced by extracting the BOLD time course from a seed region then computing the correlation coefficient between that time course and the time course from all other brain voxels


* To combine results across subjects and compute statistical significance, correlation coefficients were converted to a normal distribution by Fischer’s z transform.

	* correlations  were converted to z scores (i.e., zero mean, unit variance, Gaussian distributions) by dividing by the square root of the variance:
	
	.. math::
		
		1/(\sqrt(n-3) 
		
		
	* where n is the df measurement
	
	.. note:: 
	
				Because individual time points in the BOLD signal are not statistically independent, the degrees of freedom must be corrected according to Bartlett’s theory.
				The correction factor for independent frames was calculated to be 2.34, resulting in 318/2.34 = 135.9 df. 


* Z-score maps were combined across subjects by using a fixed-effects analysis. 

* Finally, population-based z-score maps were corrected for multiple comparisons.

