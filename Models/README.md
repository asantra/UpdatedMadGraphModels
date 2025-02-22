This is the repository of MadGraph UFO models. These models are well tested for all spin cases (0, 1/2 and 1) and all processes (photon fusion and Drell-Yan).

1. Run the part 1 of the script: ./bin/mg5_aMC Spin0ScriptDY.txt

2. A new folder named Pre5For will be generated.

3. Go to Pre5For/Sources and open genps.inc.

4. Use the absolute path of 'maxparticles.inc' on line 5.

5. Run the part 2 of the script: ./bin/mg5_aMC Spin0ScriptDY2.txt

6. If you don't change the part 1 of the script at all (you only need to change it to import different monopole models), then you just need to use steps 1-4 only once. After that, in step 5, change the mass parameter in script 2 and run for different mass points.

7. For different spin models, one just needs to import those corresponding models. 

8. IMPORTANT: Only for beta dependent models, when you run the part 2 of the script, remember to add this line in the run_card.dat after False = fixed_fac_Scale: False = fixed_couplings   .

8a. Your run_card after the above modification should have these three lines:

False = fixed_ren_scale

False = fixed_fac_scale

False = fixed_couplings

9. The naming convention: beta independent models - mono_spinzero, mono_spinhalf, mono_spinone.
                          beta dependent models - mono_spinzero_beta, mono_spinhalf_beta, mono_spinone_beta. 
