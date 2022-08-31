# Chem 274A - Lab 1

In this lab, you will be using the molecular simulation code we wrote in Chem 280 - Foundations of Molecular Modelling and Software Engineering.

## Exercises

### Section 1 - Makefile (Spend 30 minutes max on this)
1. Use the `makefile` to create an environment for this lab.
    ```
    cd mcsim_python
    make environment
    ```
2. Activate the environment created by the `makefile`
    ```
    conda activate chem274A_lab1
    ```
3. Use the `makefile` to install `mcsim`
    ```
    make install
    ```

4. Review the Makefile in `mcsim_python`. Write a comment above each target explaining what the target does.
Answer: all the comments are in the Makerfile.

### Section 2 - Runnning Simulations
1. Use the notebook `run_mcsim.ipynb` to run Monte Carlo simulations. Follow the instructions in the notebook.
Q3: the newly generated rdf looks messy, no curly shape as the 1st simulation with extensive equilibration. Also particle distribution for the 1st simulation is more uniform than the 2nd simulation.
The non-zero values close to zero distance is un-physical, indicating the particles are physically overlapped and it can't happen.

Q4: from the rdf curves, low density makes the system more gaseous than liquidic. Hence the g(r) quickly equilibrates and converges to 1 after seeing the 1st layer of particles surrounding it.

Q5: high temperature condition lowers down the 1st layer of particle density, likely because of more vibrant environment.

Q6: cubic lattice doesn't change the rdf, but impacts the equilibration energy curve. Still after production cycles the system equilibrates.