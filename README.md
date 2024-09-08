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
<p>To maintain the structural integrity and detailed features of the original content image, both the content image and the base input image are processed through a pre-trained VGG19 model. In this process, the outputs from specific intermediate layers—‘conv1_1’, ‘conv2_1’, ‘conv3_1’, ‘conv4_1’, and ‘conv5_1’—are extracted, as these layers capture progressively deeper representations of the image. The content loss is computed by determining the Euclidean distance (L2 norm) between the feature representations of the content image and the base input image at these layers. This measurement ensures that the base input image retains key features, structures, and details from the content image in the final output, thus preserving the core thematic elements of the original content throughout the transformation process.</p>
<h3>Style Loss</h3>
<p>The capture of the artistic style is achieved through an analysis of the feature maps at multiple layers of the VGG19 model. The style of an image is reflected in the patterns of spatial relationships between feature maps within each layer, which are represented through Gram matrices—a mathematical tool that captures the correlation between activations of different features at a given layer. Style loss is computed by measuring the difference between the Gram matrices of the generated image and those of the style image. By minimizing this difference, the model ensures that the textures, colors, and broader stylistic patterns of the style image are accurately applied to the generated output. This meticulous process allows the system to capture and replicate the nuances of artistic elements in the style image.</p>
<h3>Total Loss</h3>
<p>The final objective in the neural style transfer process is encapsulated in the total loss, a weighted combination of the content loss and style loss. This is regulated by two hyperparameters: alpha (α), which controls the weight of the content loss, and beta (β), which governs the influence of the style loss. These parameters allow fine-tuning of the balance between content fidelity and style transfer. The total loss function, therefore, enables the model to generate an image that strikes the desired equilibrium between preserving the core content and adopting the artistic features of the style image. By adjusting the values of α and β, users can manipulate the output to prioritize either content or style, achieving a wide range of artistic effects tailored to their preferences. This flexibility ensures that the final image not only maintains the essence of the original content but also incorporates the aesthetic character of the chosen style in a controlled and intentional manner.
</p>
<h2>Breathtaking Results</h2>
<p align="center">
 <img src="https://github.com/NavinBondade/Bruno-An-AI-That-Paints-Mind-Blowing-Painting/blob/main/Generated%20Images/all%20paintings.png">
</p> 
<h2>Conclusion</h2>
<p>In conclusion, this project leverages advanced neural networks and transfer learning to democratize the art creation process, empowering individuals to generate professional-grade paintings with ease. By blending content and style through a sophisticated deep learning framework, it offers a powerful tool for creating unique, visually striking artworks. This system not only bridges the gap between creativity and technical skill but also opens new possibilities for artistic expression.</p>



