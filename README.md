# shrii
import cv2


image = cv2.imread('kung.jpg')


height, width = image.shape[:2]


center = (width/2, height/2)


rotate_matrix = cv2.getRotationMatrix2D(center=center, angle=180, scale=1)


rotated_image = cv2.warpAffine(src=image, M=rotate_matrix, dsize=(width, height))


cv2.imshow('Original image', image)


cv2.imshow('Rotated image', rotated_image)


cv2.waitKey(0)


cv2.imwrite('rotated_image.jpg', rotated_image)


![image](https://user-images.githubusercontent.com/95746233/148203776-113399f8-b69f-4d04-95c7-e9ad2c5ec0e0.png)
