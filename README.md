# SSSC LSST Cadence Optimization Orbit Test Populations
Test Orbital Populations for LSST Cadence Operation SImulation Comparisons 

* `mbc.txt` (Kelley, Hsieh, Snodgrass): Asteroids with orbits similar to main-belt comets (MBC), based on the analysis of Kim et al. (2018, AJ 155, 142).  2000 orbits were picked randomly from the Minor Planet Center based on the following criteria:
  * 3.0 < a < 3.278 - Outer main-belt asteroids, avoiding the 2:1 mean-motion resonnance with Jupiter.
  * e > 0.15 - Eccentric orbits that have perihelion distances which favor water sublimation.
  * i < 22 - Avoid contamination from Jupiter-family comets.
  * observation arc length > 100 days - Avoid low-quality orbits.
  * H > 15 mag - Cometary activity only seen in smaller objects (with Ceres as an exception).
* `Kreutz.txt` (Ye): 2000 synthetic Kreutz sungrazing comets generated using the statistical orbit model in [Ye et al. (2014, AJ, 796, 83)](http://iopscience.iop.org/article/10.1088/0004-637X/796/2/83/meta). Note that the model does not include size information and all $H$ are set to 26.
* `2-1-leading-small.txt` (Volk et al., 2016; https://ui.adsabs.harvard.edu/?#abs/2016AJ....152...23V): Simplified model of objects in the leading libration island of Neptune's 2:1 resonance. Evenly samples the eccentricity and libration amplitudes possible in that island
* `2-1-trailing-small.txt` (Volk et al., 2016; https://ui.adsabs.harvard.edu/?#abs/2016AJ....152...23V): Simplified model of objects in the trailing libration island of Neptune's 2:1 resonance. Evenly samples the eccentricity and libration amplitudes possible in that island.
* `5-1-leading-input.txt`: Simplified model of objects in the leading libration island of Neptune's 5:1 resonance, scaled from the 2:1 leading island model in Volk et al., 2016.
* `5-1-trailing-input.txt`: Simplified model of objects in the trailing libration island of Neptune's 5:1 resonance, scaled from the 2:1 leading island model in Volk et al., 2016.
* `5-1-symmetric-input.txt`: Simplified model of objects in the symetric libration island of Neptune's 5:1 resonance, scaled from the 2:1 symmetric island model in Volk et al., 2016.
