# RGB image quantifier

## Macro for cell count estimation in confocal images  

**Usage:**  

1. Install ImageJ (https://imagej.nih.gov/ij/).  
2. Download the script from this repository.  
3. Install the macro.  
4. Import RGB images as sequence. Save the RGB stack.   
5. Run the macro on the stack (set the desired size and circularity).  
6. Save the stack with the overlay and the count summary.  
7. Validate the count and settings by inspecting the stack with the overlay.  

**Principle:**  
1. Each image in the image sequence is split into its three channels (RGB: red, green, blue).   
2. The channel for the counterstain and one additional specific stain are kept and the third channel image discarded.   
3. The two remaining images are then multiplied in order to enhance the overlap between the nucleic acid marker and the specific marker.   
4. The product image is then converted to binary followed by watershedding to enhance separation.   
5. Remaining and separate structures are counted based on user defined cell size and circularity measures.   
6. The cell count is exported as a comma separated value file and the overlay is added onto the original image sequence for verification purposes.  

*Lab: Svensson Brundin*
