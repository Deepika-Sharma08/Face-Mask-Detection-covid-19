# Face-Mask-Detection-covid-19
Face Mask Detection In Python Using OpenCV

Psedo code: ONLY USING CPU!

1. Face landmark detection. - Using Pre trained model 
2. Tilt identification, if face is tilted.
3. Skin color extraction : by taking various patches from face where mask can not exist.
4. Using 64 face landmarks, samples from cheeks(majorly) and nose to detect if skin color matches.
If face landmarks are appropriate for lips and nose and colors of samples are consistent, No MASK!


5. If two colors do not match, extract section of the face between (X) coordinates of left ear to right ear, nose to chin (Y) coordinates .
6. Lip coordiates removal (in case if a face has make up but no mask)
7. Samples from extracted section to test consistency in color and pattern (unless an image has really strage mask on!)
8. Similarity match, if yes, Mask detected.


Caveates:

a. If image is blurred or dark, where human face and mask are not identified distinctly.

b. Image clicked with low resolution and Face landmarks are not detected or Face landmarks are detected incorrectly.

c. Not all faces are detected in an image. 
