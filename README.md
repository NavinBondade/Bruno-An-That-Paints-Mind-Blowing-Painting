# Bruno An AI That Paints The Painting
<img src="https://github.com/NavinBondade/Bruno-An-AI-That-Paints-The-Painting/blob/main/Generated%20Images/display.png" width="950" height="450">
<p>Who doesn't want to be an artist and influence the world with creativity but the truth is not everybody holds that kind of skill. And that's why I have built a deep learning system that automatically paints mind-blowing paintings on your wish with the help of a technique called neural style transfer.</p>
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
<p align='center>
<img src="https://pyimagesearch.com/wp-content/uploads/2018/08/neural_style_transfer_gatys.jpg">
</p>          
<p>Much like the original author of the paper here also I have used transfer learning in the form of utilizing a pre-trained VGG19 model. Neural style transfer is an unsupervised task, and we are not interested in the output of the VGG19 model but inside the learning of internal layers. Here we will use three images the content image will be the prime theme of the generated image, the syle image which, will use to extract texture and style, and the fixed sample input image, which could either be a copy of the content image or white noise. All three images will get feed into the model to extract the feature maps and subsequently the content and style representations.</p>


