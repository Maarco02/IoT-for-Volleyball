**1. Treshold based**
   Identify three tresholds that helps to detect the three phases of a jump:
   1- Jump's load: acceleration decrease when the subject flexes the knees
   2- Flight: values close to zero, needs to declare a minimum time to consider it as a jump and cut off errors and other movements
   3- Landing: if the acceleration is >g means that the jump's ended

   the accelerometers gives the three axis values, so to make analysis, the absolute acceleration has to be calculated as **A_tot = sqrt(ax^2 + ay^2 + az^2)**
   (check if the data gives the normalized value with respect to g or the nominal value of the acceleration in m^2/s)
