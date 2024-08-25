# Producing Mind Blowing Painting With Deep Learning
<p align="center">
<a href="https://nbviewer.jupyter.org/github/NavinBondade/Bruno-An-That-Paints-Mind-Blowing-Painting/blob/main/Notebook/AI_That_Paints_Paintings.ipynb" target="_blank">
  <img align="center"  src="https://github.com/NavinBondade/Distinguishing-Fake-And-Real-News-With-Deep-Learning/blob/main/Graphs/button_if-github-fails-to-load-the-notebook-click-here%20(4).png?raw=true"/>
</a>
</p>
<img src="https://github.com/NavinBondade/Bruno-An-AI-That-Paints-The-Painting/blob/main/Generated%20Images/display.png" width="950" height="450">
<p>The desire to create art and leave a lasting impact on the world through creativity is a universal aspiration. However, the reality is that not everyone possesses the innate artistic skills required to achieve this. To bridge this gap, I have developed a deep learning system that empowers individuals to create stunning, high-quality paintings effortlessly. This system leverages a sophisticated technique known as neural style transfer, enabling users to generate visually captivating artworks based on their preferences. By combining the essence of a chosen content image with the stylistic elements of another, this technology transforms the creative process, allowing anyone to produce unique and inspiring pieces of art.</p>
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
<p>In line with the approach taken by the original author, I have employed transfer learning by utilizing a pre-trained VGG19 model. In the context of neural style transfer, which is an unsupervised learning task, the focus is not on the final output of the VGG19 model but rather on the insights gained from its internal layers. The process involves three key images: the content image, which dictates the primary theme of the generated image; the style image, used to extract textures and artistic elements; and a fixed sample input image, which can either be a duplicate of the content image or a random initialization such as white noise. These images are processed through the VGG19 model to obtain feature maps, from which the content and style representations are derived. This technique allows for the blending of the content and style elements to create a new, stylized image that retains the essence of the original content while incorporating the desired stylistic features.</p>
<h2>Loss Function</h2>
<h3>Content Loss</h3>
<p>The content image and the input base image are passed to our model and the intermediate layers' outputs that is from layer ‘conv1_1’, ‘conv2_1’, ‘conv3_1’, ‘conv4_1’ and ‘conv5_1’ are extracted. Then we calculate the euclidean distance between the intermediate representation of the content image and the input base image.</p>
<h3>Style Loss</h3>
<p>As I already mentioned, that to extract the style information from the VGG network, we use all the layers of the CNN. The style information is measured as the amount of correlation present between features maps in a given layer. Here the loss is defined as the difference of correlation present between the feature maps computed by the generated image and the style image. We describe the style loss of the base input image, x, and the style image, a, as the distance between the style representation thats the gram matrices of these images.</p>
<h3>Total Loss</h3>
<p>The alpha and beta are the two hyperparameter which act as the weights for content and style. They can be tweaked to alter our final result. So our total loss function basically represents our problem we need the content of the final image to be similar to the content of the content image and the style of the final image should be similar to the style of the style image.</p>
<h2>Breathtaking Results</h2>
<p align="center">
 <img src="https://github.com/NavinBondade/Bruno-An-AI-That-Paints-Mind-Blowing-Painting/blob/main/Generated%20Images/all%20paintings.png">
</p> 




