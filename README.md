# SSSC LSST Cadence Optimization Orbit Test Populations
Test Orbital Populations for LSST Cadence Operation SImulation Comparisons 

* `mbc.txt` (Kelley, Hsieh, Snodgrass): Asteroids with orbits similar to main-belt comets (MBC), based on the analysis of Kim et al. (2018, AJ 155, 142).  2000 orbits were picked randomly from the Minor Planet Center based on the following criteria:
  * 3.0 < a < 3.278 - Outer main-belt asteroids, avoiding the 2:1 mean-motion resonnance with Jupiter.
  * e > 0.15 - Eccentric orbits that have perihelion distances which favor water sublimation.
  * i < 22 - Avoid contamination from Jupiter-family comets.
  * observation arc length > 100 days - Avoid low-quality orbits.
  * H > 15 mag - Cometary activity only seen in smaller objects (with Ceres as an exception).
* `Kreutz.txt` (Ye): 2000 synthetic Kreutz sungrazing comets generated using the statistical orbit model in [Ye et al. (2014, AJ, 796, 83)](http://iopscience.iop.org/article/10.1088/0004-637X/796/2/83/meta). Note that the model does not include size information and all $H$ are set to 26.
* `2-1-leading-small.txt` (Volk et al., 2016; https://ui.adsabs.harvard.edu/?#abs/2016AJ....152...23V): Simplified model of objects in the leading libration island of Neptune's 2:1 resonance. Evenly samples the eccentricity and libration amplitudes possible in that island.
* `2-1-trailing-small.txt` (Volk et al., 2016; https://ui.adsabs.harvard.edu/?#abs/2016AJ....152...23V): Simplified model of objects in the trailing libration island of Neptune's 2:1 resonance. Evenly samples the eccentricity and libration amplitudes possible in that island.
* `5-1-leading-input.txt`: Simplified model of objects in the leading libration island of Neptune's 5:1 resonance, scaled from the 2:1 leading island model in Volk et al., 2016.
* `5-1-trailing-input.txt`: Simplified model of objects in the trailing libration island of Neptune's 5:1 resonance, scaled from the 2:1 leading island model in Volk et al., 2016.
* `5-1-symmetric-input.txt`: Simplified model of objects in the symetric libration island of Neptune's 5:1 resonance, scaled from the 2:1 symmetric island model in Volk et al., 2016.
* `ekbo-uniform-input-small.txt`: Simplified model of non-clustered extreme Kuiper belt objects. They are uniformly distrivuted from a=150-160 au and from perihelion distance q=40-60 au. All orbital angles are uniformly distributed.
* `occ-vokrouhlicky19-case1_ver10-rmax5-5k.txt` (Kelley, Nesvorny, Vokroulicky): Case 1 version 1 (C1V1) of Vokrouhlicky et al. (2019, AJ 157, 181; https://iopscience.iop.org/article/10.3847/1538-3881/ab13aa).  Orbits were generated with the following method:
  * Barycentric q, e, and i are randomly picked from the model simulation.
  * Each orbit is assigned a random argument of perihelion (0 to 2π rad), longitude of the ascending node (0 to 2π rad), and mean anomaly (-1 to 1 rad).
  * If the barycentric distance is within 5 au, then the state vector computed, otherwise the orbit is rejected.
  * The state vector is given a random epoch between 2021-01-01 and 2036-01-01, and heliocentric osculating orbital elements are generated (via NAIF SPICE).
* `occ-vokrouhlicky19-case1_ver10-rmax20-5k.txt`: Same as `occ-vokrouhlicky19-case1_ver10-rmax5-5k.txt` but picked with a maximum heliocentric distance of 20 au.
