
# FOBOS Design Documents

## Current Strawman design

The baseline design for FOBOS is as follows:

 - Keck 10m primary mirror
 - ~15 arcmin diameter FOV (patrol)
 - Multiplex of 400 with 7x0.57 arcsec mini-IFUs per target (~1.7 arcsec
   overall on-sky aperture for each target)
 - Wavelength: 350-1000nm
 - Spectral Resolution: R~2500-4500 (from blue-red)
 - Nominal seeing: 0.6" (median 0.4" with GLAO upgrade) 

## Science Drivers

Document started 17 Apr 2018.  Linked to an Overleaf repo.

| Directory             | Overleaf |
| --------------------- | ------------- |
| science_drivers | https://www.overleaf.com/15611483cdhzxxhmcbps#/59306618/ |

### Add new science cases:

 - Create a tex file in `science_drivers/src` called, e.g.,
   `kinematic_weak_lensing.tex`
 - The first line should be `\subsection{My Science Case Title}`
 - Write the science case
 - Include any bibtex references in `science_drivers/master.bib`
 - Include the tex file in `science_drivers/ms.tex` using the input
   command within the Science Cases section.  E.g.,
   `\input{kinematic_weak_lensing}`.

