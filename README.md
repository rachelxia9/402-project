Steps of the pipeline with corresponding code files:
1. removeline.r (change Mindware exported text files to correct format) 1.1 on task data txt 1.2 on baseline data txt
2. ledalab_export.m (use Matlab toolbox to extract tonic and phasic data, and downsample size) 2.1 on task data txt 2.2 on baseline data txt
3. analysis.r (on task data, extract epoches and assign conditions base on events)
4. baseline calculation.r (on baseline data, get summary file of averaged tonic and phasic data in baseline for each testing session)
5. full trial artifacts.r (plot all epoches for each testing sessions, corrected to baseline phasic)

6. Thresholding + Automatic Noise Removal + Filtering (each of the cleaning steps uses a variation of full trials artifacts to plot all epoches)
   6.1 full trial artifacts_thresholding.R (removes noise using set of manually rated thresholds)
   6.2 automatic_removal_with_new_criteria.R (removes noise using a set of criteria that is consistent for the entire dataset)

8. Average_all_trials_for_ICC.r (calculate percent change in SCR from baseline to task)
9. ICC-test-retest.r (calculate test-retest reliability via ICC, Pearson's R, and paired t-test)
