import os
#import numpy
import PIL
from PIL import Image

rootDir = 'E:\Saad Picture'
resizeDir = 'E:\Saad resizedimages'

for dirName, subdirList, fileList in os.walk(rootDir):
    print('Found directory: %s' % dirName)
    
    for fname in fileList:
        print('\t%s' % dirName+'\\' + fname)
        img = Image.open(dirName+'\\' + fname)
        img = img.resize((200, 200), PIL.Image.ANTIALIAS)
        img.save(resizeDir + '\\'+ fname) 
