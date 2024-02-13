# inpainting-of-satellite-images
Machine Learning course project for the academic year 2023/2024 at UNIBO.  

The project is about image inpainting, that consists in filling deteriorated, or missing parts of a picture to reconstruct a complete image.

The dataset taken into consideration is the tensorflow EuroSAT dataset based on Sentinel-2 satellite images, in the the rgb version. This consists of 27000 images, at resolution 64x64.

A portion of the image is randomly masked according to the procedure described by the "generator" function. The goal is to reconstruct the full image.

---
The project has been very interesting and, above all, challenging, particularly from the perspective of researching and constructing the best model to effectively perform the assigned task. Initially I believed that a model only focused on image reconstruction wouldn't be sufficient. As a matter of facts, I attempted to implement not only a generator structured as a UNet but also a discriminator to provide feedback to the UNet, enabling continuous improvement to better fool the discriminator. Essentially, the first model I tried to build was a simplified version of a GAN. However, I didn't achieved the desired results, mainly because I couldn't halt the discriminator from continually improving itself beyond a certain threshold, making it effectively unreachable by the UNet. Therefore, after briefly testing this model, I transitioned to a model consisting only in a UNet network, experimenting with various configurations, which I will provide a more detailed explanation of later.

In the notebook, I didn't include the code for the discriminator, but I did include the UNet configurations.
