# Image Pre-processing

- More about color spaces
- Changing color space from one to another
- Image Rotation
- Image Flip
- Image Resizing (interpolation methods: nearest-neighbor, bilinear, bicubic)
- image normalization
- histogram equalization

1. Image orientation

   ```python
   # Rotate 90 Degree Clockwise
   cv2.rotate(img, cv2.ROTATE_90_CLOCKWISE)

   # Rotate 90 Degree Counter Clockwise
   cv2.rotate(img, cv2.ROTATE_90_COUNTERCLOCKWISE)

   # Rotate 180 Degree Clockwise
   cv2.rotate(img, cv2.ROTATE_180)
   ```

2. Image flip

   ```python
   # Flip horizontally
   cv2.flip(img, 1)

   # Flip verticallly
   cv2.flip(img, 0)

   # Flip horizontally and verticallly
   cv2.flip(img, -1)
   ```

3. Image resize

   ```python
   # Make it smaller
   cv2.resize(image, (0, 0), fx = 0.5, fy = 0.5)

   # Make it bigger
   cv2.resize(image, (0,0), fx = 2, fy = 2)
   ```
