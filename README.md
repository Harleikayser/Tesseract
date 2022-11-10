This program will convert a Image in a string

To do that we need import tree library ( Tesseract , Pilllow and numpy )


Tesseract Documentation: 
 
https://pypi.org/project/pytesseract/


Pillow Documentation: 

https://pillow.readthedocs.io/en/stable/reference/Image.html




							Code 
____________________________________________________________________________________________

# import PILLOW module
from PIL import Image

# import TESSERACT module
import pytesseract

# import NUMPY module
import numpy as np

# for window users TESSERACT needs to be download and install the EXE, after needs to be pass the path.
pytesseract.pytesseract.tesseract_cmd = r"C:\Program Files\Tesseract-OCR\tesseract.exe"

# file name 
filename = 'Tesseract image.png'

# open the file 
img = np.array(Image.open(filename))

# convert to string
text = pytesseract.image_to_string(img)

print(len(text))
print(text)

____________________________________________________________________________________________