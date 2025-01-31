# African Seeds Art
African Seeds Art  is committed to amplifying Indigenous African seeds through the medium of mixed media artworks. Dawa seeds which was used for this model is an African millet seed. Dawa seeds were used to create concepts in arts, and this is a source of inspiration to train the model to learn about the dawa concept to create AI artworks.

## Motivation
African seeds art 2021  is an artificial intelligence (AI) procreated creation with mixed media artworks made with African seeds. Dawa seeds which was used to create the mixed media artworks is a class of the African millet seed. Nefertiti Emezue used the Dawa seeds to create mixed media artworks and together with [Chris Emezue](https://github.com/chrisemezue), they trained the model to assimilate and interpret the artwork to create an AI artwork. For this project, we used [Deep Daze model](https://github.com/lucidrains/DALLE-pytorch), a text to image generation model that uses [OpenAI's CLIP](https://arxiv.org/abs/2103.00020) and [Siren (Implicit neural representation network)](https://vsitzmann.github.io/siren/). By configuring the model on a joint optimization task of both the image and the text (interpretation of the dawa image), the model learns to create abstract interpretations of the text while trying represent an art close to the dawa art as possible.

## Our Work
In this project, we work with three unique artworks of Nefertiti Emezue which were created with African seeds.
#### African Seeds artworks and their interpretation
Picture of artwork | Title of artwork | Full Interpretation (for Setup A) | One-sentence interpretation (for Setup B) 
------------- | ------------- | ------------- | -------------
![alt text](./artworks/Art2.jpg)  | Education Connecting the World Dawa art | This artwork represents the connections of  education and the globe. This artwork represents the idea that education serves as a unifying factor between countries of the World. | Global education connects the world.
![alt text](./artworks/Art1.jpg)   | African Bride Seed Art | This artwork captures the state of an excited Nigerian bride who comes out during the traditional wedding ceremony to find her husband.| A Gleeful Nigerian bride on her traditional attire on her wedding day.
![alt text](./artworks/Art3.jpg)  | Peace Seed Art |This artwork shows a bird hovering over a Battlefield Cross. A battlefield cross signifies a dead soldier and it is a symbolic replacement of a cross, or marker appropriate to an individual service-member.  It is made up of the soldier's rifle stuck into the ground or into the soldier's boots, with helmet on top.  The bird symbolizes Peace whilst the battlefield cross  symbolizes the casualties of war. “Peace” expresses the hope that despite the aridity that has crept over most African countries like Nigeria as a result of violence, there is hope for peace. | The tranquility of a fallen hero.

#### Idea
1. We give the model _our artwork_ as the image and a text. For the text, we explore two scenarios:
    1. We give the full interpretation as the text. We call this ***Setup A***.
    2. We give a one-sentence summary of the artwork. We refer to this as ***Setup B***.
2. The model learns from both the text and _our artwork_ through a joint optimization task.
3. While learning, the model outputs an abstract art (or series of abstract pictures during its learning process which we compile into a video) which is the model’s interpretation of _our artwork_ and the text.


#### Model Parameters
After testing different hyperparameters, we settled with the following for the rest of our experiments.
```python
NUM_LAYERS = 32
SAVE_EVERY =  20
IMAGE_WIDTH = 512
LEARNING_RATE = 1e-5
EPOCHS=20
ITERATIONS = 1050
```
## Results
1. The Setup A gave a better imagination. We compile our results into the video below:

https://user-images.githubusercontent.com/36100251/134716851-095a575f-f33f-4c81-af95-99f92d5e4547.mp4

## Future Work
There is room to explore in:
1. leveraging the GAN or Transformer-based networks for art imagination.
2. Training the model with more African-inspired artworks in order to improve the model's imagination of African concepts.
3. [Differential Rastirizer](https://people.csail.mit.edu/tzumao/diffvg/) thanks to Peter Schaldenbrand.
