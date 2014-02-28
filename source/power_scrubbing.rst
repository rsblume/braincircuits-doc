The scrubbing method
===========================================

A paper by `Power et al., 2011 in Neuroimage <http://www.ncbi.nlm.nih.gov/pubmed/22019881>`_ introduces a procedure they call *"scrubbing"* which removes spurious correlated signal due to motion.

Their procedure is the same as the Fox method for pre-processing and for extracting the timeseries but diverges after that.


**Pre-processing:**
--------------------

These steps included: 

* removal of a central spike caused by MR signal offset

* correction of odd versus even slice intensity differences attributable to interleaved acquisition without gaps

* correction for head movement within and across runs

* within run intensity normalization to a whole brain mode value of 1000. 



**Atlas Registration:**
-----------------------

* Atlas transformation of the functional data was computed for each individual using the MP-RAGE scan. 

* Each run was then resampled in atlas space on an isotropic 3 mm grid combining movement correction and atlas transformation in a single interpolation.


**Timeseries Correlation:**
------------------------------

These steps included: 

* a temporal band-pass filter (0.009 Hz < f < 0.08 Hz) 

* spatial smoothing (6 mm full width at half maximum)

* regression of six parameters obtained by rigid body head motion correction

* regression of the whole brain signal averaged across the whole brain

* regression of ventricular signal averaged from ventricular regions of interest (ROIs)

* regression of white matter signal averaged from white matter ROIs. The first derivatives of these regressors were also regressed



**Scrubbing**
---------------

1) Framewise data quality / displacement:
"""""""""""""""""""""""""""""""""""""""""""""

calculated as the sum of the absolute values of the derivatives of the six realignment parameters.
	
* how much movement change from one frame to the next


2) DVARS: frame by frame image intensity change:
""""""""""""""""""""""""""""""""""""""""""""""""""""""""
	
calculated in each volume as the RMS of the derivatives of the timecourses of all within-brain voxels.

* DVARS thus measures how much image intensity has changed from one frame to the next.


You then determine a criterion or cutoff by which to remove volumes

Power et al chose:

	* 0.5 for framewise displacement
	
	* and 0.5% ΔBOLD for DVARS were chosen
	
	* when a volume exceeds both of these criteria, then it is masked out

	* a minumum requirement is that at least 5 minutes of resting data is left
	
