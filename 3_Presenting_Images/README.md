# Presenting Images

For ease of use, instead presenting images directly in active windows like before using cv2.imshow(). We use matplotlib for presenting our image, as it easier to understand when we tried to compaer mulitple imgaes

```python
plt.figure(figsize=(9, 9))
plt.suptitle("Presenting Image Rotations")

plt.subplot(2, 2, 1)
plt.title('Original Image')
plt.imshow(img)

plt.subplot(2, 2, 2)
plt.title('Rotate 90 Clockwise')
plt.imshow(imgRotate90Clockwise)

plt.subplot(2, 2, 3)
plt.title('Rotate 90 Counter Clockwise')
plt.imshow(imgRotate90CounterClockwise)

plt.subplot(2, 2, 4)
plt.title('Rotate 180')
plt.imshow(imgRotate180)

plt.tight_layout()
plt.show()
```
