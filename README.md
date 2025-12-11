## Topic 2: Effect of Stride & Padding on CNN Feature Extraction

**Dataset:** MNIST  
**Goal:** Analyse how stride and padding affect feature extraction, spatial resolution, and accuracy in CNNs.

###  Configurations Tested
Four CNN models were trained with identical architecture but different stride and padding settings:

- **Model A:** Stride = 1, Padding = "same"  
- **Model B:** Stride = 2, Padding = "same"  
- **Model C:** Stride = 1, Padding = "valid"  
- **Model D:** Stride = 2, Padding = "valid"  

This allowed isolation of the effect of spatial movement (stride) and border handling (padding).



###  Key Findings

- **Stride = 1 + SAME padding** produced *the highest accuracy* and *best feature clarity*.  
- **VALID padding** removed border pixels, causing the model to lose important edge details.  
- **Stride = 2** significantly reduced feature map size, leading to loss of fine features and lower performance.  
- SAME padding preserved spatial alignment across convolution layers, allowing the CNN to capture digit curves and edges more effectively.




###  Summary

This topic demonstrates that **stride and padding significantly influence how CNNs perceive images**.  
Using stride=1 and SAME padding preserves maximum detail and yields the best recognition performance, especially on small, detail-rich images such as MNIST digits.
