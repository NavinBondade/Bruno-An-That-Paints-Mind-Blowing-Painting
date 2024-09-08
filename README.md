# Producing Mind Blowing Painting With Deep Learning
<p align="center">
<a href="https://nbviewer.jupyter.org/github/NavinBondade/Bruno-An-That-Paints-Mind-Blowing-Painting/blob/main/Notebook/AI_That_Paints_Paintings.ipynb" target="_blank">
  <img align="center"  src="https://github.com/NavinBondade/Distinguishing-Fake-And-Real-News-With-Deep-Learning/blob/main/Graphs/button_if-github-fails-to-load-the-notebook-click-here%20(4).png?raw=true"/>
</a>
</p>
<img src="https://github.com/NavinBondade/Bruno-An-AI-That-Paints-The-Painting/blob/main/Generated%20Images/display.png" width="950" height="450">
<p>The aspiration to create meaningful art and leave a lasting creative legacy is a shared human experience. Yet, for many, the lack of formal artistic training or innate skills can present a significant barrier to realizing their artistic vision. In response to this challenge, I have developed an advanced deep learning system designed to democratize the art creation process, enabling individuals of all skill levels to produce visually striking, high-quality paintings with ease.

This system is built on the innovative concept of neural style transfer, a technique that blends the content of one image with the stylistic elements of another, producing a unique and visually captivating artwork. By analyzing the intricate patterns of both the content and style images, the system seamlessly merges them, preserving the essence of the content while applying the artistic qualities of the chosen style. This technology transforms the creative process, empowering users to generate personalized, professional-grade artworks effortlessly, and allowing anyone—regardless of artistic background—to create distinctive and inspiring pieces that reflect their vision.</p>
<h2>Libraries Used</h2>
<ul>
  <li>Pytorch</li>
  <li>Matplotlib</li>
  <li>PIL</li>
  <li>OS</li>
  <li>OpenCV</li>
</ul>
<h2>Data Visualization</h2>
<img src="https://github.com/NavinBondade/Bruno-An-AI-That-Paints-The-Painting/blob/main/Dataset/Content%20Images/all%20content%20images.png" width="950" height="600">
<br>
<img src="https://github.com/NavinBondade/Bruno-An-AI-That-Paints-The-Painting/blob/main/Dataset/Style%20Images/all%20style%20images.png" width="950" height="600">
<h2>Implementation Details</h2>
<p align="center">
 <img src="https://pyimagesearch.com/wp-content/uploads/2018/08/neural_style_transfer_gatys.jpg">
</p>          
<p>In alignment with methodologies developed by pioneering researchers, I have utilized a sophisticated approach called transfer learning, employing the pre-trained VGG19 model, a widely recognized deep neural network developed for image classification tasks. In the specialized application of neural style transfer, this model serves a unique role that deviates from its original classification purpose. Here, the primary interest lies not in the model's final output, but rather in extracting deep insights from the intermediate layers of the VGG19 network.

Neural style transfer is an unsupervised learning task that involves the manipulation of three key images within this framework: the content image, the style image, and a sample input image, which serves as the initial canvas. The content image defines the primary subject and structure of the output, while the style image contributes textures and artistic elements derived from another artwork. The initial sample input can be either a duplicate of the content image or a randomly generated pattern, such as white noise.

These images are processed through the VGG19 model, allowing for the extraction of intricate feature maps at various layers. These feature maps are critical in capturing the distinct content details and stylistic attributes of the input images. By strategically comparing and minimizing the differences between the feature representations of the style and content images, the system can blend these elements effectively. The resulting image emerges as a new creation that retains the essence and thematic depth of the original content while dynamically incorporating the aesthetic characteristics of the chosen style. This innovative blending of content and style through deep learning offers a powerful tool for artists and creators, enabling the generation of unique, stylistically enriched artworks.</p>
<h2>Loss Function</h2>
<h3>Content Loss</h3>
<p>To preserve the structure and details of the original content image, both the content image and the input base image are passed through a pre-trained VGG19 model. We focus on the outputs from specific intermediate layers—namely ‘conv1_1’, ‘conv2_1’, ‘conv3_1’, ‘conv4_1’, and ‘conv5_1’. The content loss is then computed by calculating the Euclidean distance (also known as the L2 norm) between the intermediate feature representations of the content image and the input base image. This metric measures how closely the base image retains the original content's features, ensuring that the key elements of the content image are preserved in the final output.</p>
<h3>Style Loss</h3>
<p>To capture the artistic style, the VGG19 network is utilized to analyze all layers of the Convolutional Neural Network (CNN). The style information is extracted by measuring the correlations between feature maps within a given layer, represented by the Gram matrices of these feature maps. The style loss is defined as the difference in these correlations between the feature maps of the generated image and those of the style image. By minimizing this loss, the system ensures that the stylistic patterns, textures, and colors of the style image are accurately applied to the generated image.</p>
<h3>Total Loss</h3>
<p>The total loss function is a weighted combination of the content loss and style loss, controlled by two hyperparameters, alpha (α) and beta (β). These parameters allow for the adjustment of the balance between content fidelity and style transfer. The total loss function thus encapsulates the objective of the neural style transfer process: to generate an image that maintains the content of the original content image while adopting the artistic style of the style image. By tweaking the values of alpha and beta, one can fine-tune the influence of content and style on the final output, achieving the desired artistic effect.
</p>
<h2>Breathtaking Results</h2>
<p align="center">
 <img src="https://github.com/NavinBondade/Bruno-An-AI-That-Paints-Mind-Blowing-Painting/blob/main/Generated%20Images/all%20paintings.png">
</p> 




