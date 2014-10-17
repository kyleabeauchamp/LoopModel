Get License Here:
https://www.rosettacommons.org/

See: 
https://www.rosettacommons.org/docs/latest/loopmodel.html
https://www.rosettacommons.org/docs/latest/Application-Documentation.html
https://www.rosettacommons.org/manuals/archive/rosetta3.5_user_guide/d8/df1/loopmodel.html

export MINIROSETTA_DATABASE=/home/kyleb/src/Software/rosetta_2014.35.57232_bundle/main/database/
export PATH=$PATH:/home/kyleb/src/Software/rosetta_2014.35.57232_bundle/main/source/bin/

loopmodel.linuxgccrelease -database $MINIROSETTA_DATABASE -loops:input_pdb bad.pdb -loops:loop_file bad.loop -loops:remodel perturb_kic -loops:refine refine_kic -ex1 -ex2 -nstruct 1 -loops:max_kic_build_attempts 100 -in:file:fullatom
loopmodel.linuxgccrelease -database $MINIROSETTA_DATABASE -in::file::s bad.pdb -loops:loop_file bad.loop -loops:remodel perturb_kic -loops:refine refine_kic -ex1 -ex2 -nstruct 1 -loops:max_kic_build_attempts 100 -in:file:fullatom


loopmodel.linuxgccrelease -database /pathtoyourdb/ -loops:input_pdb 1TR2_manually_added_dummy_residues_renumbered.pdb -loops:loop_file 1TR2.loop -loops:remodel perturb_kic -loops:refine refine_kic -ex1 -ex2 -nstruct 1 -loops:max_kic_build_attempts 100 -in:file:fullatom
