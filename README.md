# Prior-Experience-Based-Dual-Encoder-Approach-for-Efficient-Image-Text-Retrieval
The aim of remote sensing (RS) image
text retrieval (RSITR) is to extract pertinent texts 
(RS images) from a given RS image (text) by using 
its content. Enhancing a vision- language model 
based on prior experience for distant sensing image
text retrieval is a challenge for the current approach. 
The current method uses different encoders for text
to-image and image-to-text conversion. Swin 
transformer is utilized as the visual encoder, while 
BERT is employed as the text encoder. Our 
objective is to simplify the model’s architecture and 
increase efficiency by combining these features into 
a single encoder that can handle both image-to-text 
and text-to-image conversions. For image-text and 
text-image retrieval tasks, we use a single CLIP 
(Contrastive Language-Image Pre training) model 
and processor in the project. CLIP maps text and 
images into a common multi-modal feature space 
by using a single shared encoder for processing both. 
This method simplifies the model design by doing 
away with the necessity for distinct encoders for 
image-text 
and text-image activities. Pre
processing inputs, such as transforming text and 
images into a format, the model can comprehend, is 
the responsibility of the CLIP Processor. The model 
creates a feature vector (embedding) after 
processing the image through its visual encoder for 
image-text retrieval. The text queries are tokenized 
and sent through the text encoder at the same time, 
producing a matching text embedding. Cosine 
similarity is used to calculate the similarity between 
each text embedding and the image embedding, 
making it possible to retrieve the most pertinent text 
for a particular image. The roles are reversed for 
text-to-image 
retrieval: 
the 
visual 
encoder 
processes the image, while the text encoder 
processes the text query. The model is able to get 
the image that is most pertinent to the text query by 
calculating the cosine similarity between the text 
and image embeddings. CLIP is incredibly efficient 
and able to handle both retrieval tasks at once since 
it 
uses a single encoder for both modalities, 
effectively mapping words and images into a shared 
embedding space where their similarities can be 
immediately computed. Significant benefits in 
terms of computing performance and model 
simplicity are provided by this cohesive approach
