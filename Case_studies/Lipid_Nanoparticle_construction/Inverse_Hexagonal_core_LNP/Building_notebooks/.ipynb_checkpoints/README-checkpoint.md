# Steps for contructing a LNP with inverse hexagonal core. The cargo is 21nt siRNA (poly A/U)

Step 1 ) Make make 4 channels and relax for 10 ns  (Step1_construct_core.ipynb)

Step 2 ) Make channels whole using the notebook and mdvwhole.  (Step2_channel_extraction.ipynb)

The notebook outputs cluster.npy, which you can then use with mdvwhole:
mdvwhole -f r_whole.gro -x r_whole.gro -clus clusters.npy -wa True -o whole.pdb

Step 3 ) Repeat the 4 channels to generate a hexagon core using the notebook (Step3_hexagon_channels.ipynb)

Step 4 ) Write toplogy for hexagon core  (Step4_create_top_hexagon.ipynb)

Step 4.5 ) generate tpr file for hexagon core and perform gmx trjconv -pbc whole 

gmx trjconv -f whole_hexagon.pdb -s hexagon_fake.tpr -pbc whole -o hexagon_fake_whole.pdb -conect

#### Change the box to cubic:
gmx editconf -f hexagon_fake_whole.pdb -bt cubic -c -o hexagon_fake_whole_cubic.pdb

Step4.6 ) Make trangulatd mesh of hexagon using blender.
First load in the hexagon in VMD, then make quicksurfe with 4 in radius, gridsize 4 and max resolution, render surface as stl file. Remember to remove axis, so you wont render those in as well. 
Alternatively, we have provided a tcl script for doing so called render_stl.tcl. 

      ## For maunal way ##
      Load in the stl file in Blender (DO NOT TURN IT AROUND) 
      Trangylate the surface with Blender, optimize the mesh
      make squares into triangles by ctr+shift+T
      Reorientate normals
      Use script to write out the tsi file. The script can be found here: 
      https://github.com/marrink-lab/TS2CG1.1/blob/master/Tutorials/files/blender_mesh2tsi.py 
      #####################
      
      ## Simple one step script ##
      run blender script (rename input and output file name in script)
      blender --background remesh.py --python 
      ############################

This is the most vital step, the key is to get a good surface for TS2CG to place the lipids onto. 

Step 5 ) Make the coating with TS2CG - the steps are in the notebook - and combine using the notebook(Step5_combine_coating.ipynb)

Step 6 ): write the topology for the hexagon with coating using the notebook (Step6_create_top_hexagon.ipynb)

Step 6.5 ): minimize in vacume the complex:

gmx editconf -f coated_test.pdb -d 7 -c -o coated_test.gro
gmx grompp -f MDPs/min_vac.mdp -c coated_test.gro -p hexagon_coat.top -o hexagon_coat_m.tpr


Step 7 + 7.5): Solvate and neutralize using the notebooks Step7_Solvate.ipynb and Step7.5_create_top_hexagon.ipynb 


NB : for these notebook you will need the legacy version of MDVcontainment 
