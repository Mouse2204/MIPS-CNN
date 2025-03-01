# MIPS-CNN
This source code is describing about the CNN - Convolutional Neutral Network.

Convolution Algorithm Explanation

The convolution algorithm is a fundamental operation in signal processing, image processing, and deep learning. In the context of image processing, convolution is used to apply filters (also known as kernels) to images in order to extract features such as edges, corners, or textures.

Suppose you have an image matrix I and a filter (kernel) K. Both the image and the kernel are matrices. The convolution operation for a point at position (i,j) of the image is calculated by taking the element-wise product between the kernel matrix 𝐾 and the corresponding part of the image I at that position, and then summing all the resulting products.


**Convolution Formula:**

![image](https://github.com/user-attachments/assets/c6e69281-3751-4b9c-825d-8089fa42f381)

Steps in Convolution Operation:

***Step 1:**

Choose the Kernel: The kernel is a small matrix, such as 3x3, 5x5, or 7x7. The values in the kernel can be positive or negative, depending on the features you want to extract (e.g., edges, blurring, etc.).

***Step 2:**

Apply the Kernel on the Image:

Place the kernel at the top-left corner of the image.

For each position, multiply each value of the kernel with the corresponding value in the image and sum them all together.

Move the kernel to the next position in the image and repeat the above step.

***Step 3:**

Kernel Movement:

The kernel moves across the image with a step size called stride. The stride determines how much the kernel moves each time.

If the stride is 1, the kernel moves one pixel at a time. If the stride is greater than 1, the kernel skips over a number of pixels as it moves.

***Step 4:**

Padding:

To handle the edges of the image, padding is often used. Padding adds extra values (usually zeros) around the image to ensure that the kernel can be applied to the corners and edges.

Padding helps prevent the loss of information at the boundaries of the image when performing convolution.

Result: The result of the convolution operation is a new matrix, which is usually smaller than or equal to the size of the original matrix, depending on the size of the kernel and stride. The size of the output matrix can be calculated using the formula:
