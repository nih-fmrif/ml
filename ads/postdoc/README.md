# HIRING: Post-Doctoral Fellow

## Who we are:

Drs. [Daniel Pine](https://www.nimh.nih.gov/research/research-conducted-at-nimh/research-areas/clinics-and-labs/edb/sdan/index.shtml) and [David Jangraw](https://davidjangraw.wordpress.com) are seeking applicants for a Post-Doctoral Fellowship position that would develop new machine learning-based approaches for the diagnosis and treatment of mental illnesses. Our aims are to better understand the causes and mechanisms of certain psychiatric disorders, improve their definition and classification, and ensure the best treatment can be offered to psychiatric patients. We do this by identifying neuroscience-based phenotypes that map onto clinical phenotypes, and which can be targeted with novel treatments. The position is co-advised by the [NIMH Machine Learning Team](https://cmn.nimh.nih.gov/mlt), led by Dr. Francisco Pereira, whose mission is to solve the scientific problems of NIMH researchers by developing new machine learning methods, or developing new analysis approaches relying on existing methods.

## What you will do:

One line of research will focus on refining and testing latent constructs derived from multiple brain imaging and behavioral markers of inhibitory control. Inhibitory control deficits are common to many psychiatric disorders, and if the latent construct shows good reliability, it may serve as a target for novel treatments. Another line of research will hinge on extracting characteristics of psychotherapy session data, such as therapist speech and facial expressions, that can predict patient clinical outcomes. While the work will concentrate on anxiety and mood disorders in young people, the approaches will be applicable to any mental disorder. 

The fellow will work with multi-modal imaging datasets that include MRI (functional, structural), EEG, MEG, and associated behavioral and clinical data, all of which may be used as input to machine learning methods. Data sets are already available, and the fellow will devote most of their time to analyzing these data or developing new methods. The fellow will also have access to excellent computational resources within NIH (e.g., top-100 supercomputer with hundreds of thousands of CPUs and hundreds of GPUs).

## Who you are:

Candidates with a strong computational background (e.g., PhD in Engineering, Physics, Computer Science, Mathematics, Statistics, Computational Neuroscience, and related areas) who are interested in brain development and psychopathology are particularly encouraged to apply. Requirements for this position include:
- Programming experience in data-intensive computation tasks, in Python (preferably) or in R/Matlab
- Practical machine learning experience (e.g., training of classification/regression models, statistical testing of results, interpretation and visualization of models), especially using open source machine learning platforms such as scikit-learn
- Excellent interpersonal and written (English) communication skills

Experience in psychiatry or knowledge of software for processing neuroimaging data are not required. However, the candidate will be expected to learn some of these topics as part of their role in our research group.

## How to apply:

The successful candidate will work jointly with Drs. Daniel Pine, David Jangraw, and Francisco Pereira. Please write to them (pined@mail.nih.gov, david.jangraw@nih.gov, francisco.pereira@nih.gov) with your CV, using the email as the cover letter. Other enquiries are also very welcome. The National Institutes of Health is an equal opportunity employer.


I've sent the ad to a few more venues where machine learning people with an interest in health applications might see it. I'm about to leave to travel, and I may not be able to  accesss the internet while  I'm away (til Dec 1), so I'm afraid I won't be able to add any more names to the spreadsheet.


25 + 15

The first dataset is in our server

/data/MLcore/PhysiologicalPrediction

It contains three subject folders: sub-001, sub-002, and sub-003.

Each subject folder, e.g. sub-001, contains 10 session folders, e.g.

ses-01	ses-02	ses-03	ses-04	ses-05	ses-06	ses-07	ses-08	ses-09	ses-10

Each session folder, e.g. ses-01, contains separate folders for anatomical (anat) and functional (func) data.

Inside the func folder, there is data for multiple scanning runs. For each run,  these files are relevant

sub-001_ses-01_task-checkerboard_run-001_bold.nii.gz
(the 4D fMRI dataset, containing T consecutive XxYxZ volumes)
sub-001_ses-01_task-checkerboard_run-001_respiratory_targetsPerSlice.txt
(a T x Z binary matrix, where row t indicates whether each of the Z slices had a respiratory peak in it)

There may be some instances of runs where the target file does not exist, but they will be rare.

Only the task-checkerboard runs have physiological data, so we'll focus on those.
