# Sensitivity analysis
### Process
To test how much changing the Pc value effected the results of the RDMSim we first opted to cast a wide net, testing every value between 0 and 1 with 0.05 intervals. Based on the results of this first analysis a more thorough analysis was performed.

### analysis
What was found is changing the Pc value would have an increasingly large impact the closer it got to 0. What this looks like is in earlier values, particularly close to 0 had little to no effect. This would remain the case for most of the run, Pc values between 0 and 0.6 would not differ much, behaviour in topology selection only shifting by a small amount.

This behaviour changes for values larger than 0.8 leading us to perform further analysis, checking each pc value between 0.8 and 1 in intervals of 0.1. What was found confirmed what we thought, the smaller differences  did in fact cause larger changes and were far more sensitive for larger Pc values.

What this means is that one should take care when choosing an appropriate Pc value due to the sensitivity, it is unlikely that someone would need a Pc value close to 1 but this effect should still be taken into consideration when choosing an appropriate value.
