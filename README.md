# Meta-optimization of GA for image reconstruction

This is a computational intelligence course project programmed in Python using Pillow (PIL) (<https://pillow.readthedocs.io/en/stable/>) and scikit-image (<https://scikit-image.org/>) libraries for drawing and image processing.  

### Genetic algorithm for image reconstruction  

Algorithm tries to reconstruct an image with an array of figures with the same given type. <b>Fitness</b> is calculated as structural similarity (SSIM) between the original image and the reconstruction. Reconstruction is generated by drawing figures from the array that represents the chromosome.  

Figures are either squares, circles or triangles.  

<b>Mutation</b> is defined as a slight change in color, size and figure position. Each gene (figure) mutates with the given mutation probability.  

Two <b>selection</b> methods are implemented. GA uses either tournament selection or roulette selection.  

<b>Crossover</b> is either uniform, k-position or mix crossover. Mix crossover creates two children by copying allels from parents up to a randomly chosen position <i><b>p</b></i> in the chromosome. Both children have the same mixed parent allels for each position after <i><b>p</b></i>.

### Meta-optimization of image reconstruction GA  

Genetic algorithm was used for meta-optimization. One chromosome represents the image reconstruction GA parameters.  

<b>Mutation</b> is defined as a slight change in value for each gene, and specificaly for selection and crossover types, it is defined by randomly choosing a different method. Each gene (meta-parameter) mutates with the given mutation probability.  

<b>Selection</b> is tournament and meta-opt. GA uses uniform <b>crossover</b>.
