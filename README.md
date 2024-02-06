# ACTAM-Project


<p align="center">
    <img src="Deliveries/Images/Logo.png" alt="alt text">
</p>

<p align="center">
    At this link you can try the app:
  <a href="https://annafusari.github.io/itsNotGarageBand/">click and try (DA METTERCI IL LINK GIUSTO!)</a>
</p>


## Group:

- ####  Francesca Benesso &nbsp;([@fr-bn](https://github.com/fr-bn))<br> 10700542 &nbsp;&nbsp; francesca1.benesso@mail.polimi.it

- ####  Filippo Marri &nbsp;([@filippomarri](https://github.com/filippomarri))<br> 11010508&nbsp;&nbsp; filippo.marri@mail.polimi.it

<br>

<p align="center">
  <a href="https://youtu.be/9ChYAzdux1c">
    <img src="https://github.com/ChiaraAuriemma/ACTM-Project/blob/main/deliveries/images/Screen3.png" alt="Watch the video" width="800" style="border-radius: 8px;">
  </a>
</p>

<br>

### About the project
The aim of the project is to create an application able to simulate the effect that a person who has chromaesthesia experiments when is watching at an image. Actually, the proper chromaesthesia follows the inverse path: sounds are associated to colours and not vice-versa, but we tried to see what happens by reversing the pathway. The project is based upon the studies made by Aleksandr Nikolaevič Skrjabin and Vasilij Vasil'evič Kandinskij, two artists both with synaesthesia who have examined this idiosyncrasy from different points of view. The former focused his attention on pitch trying to create a formal relation between the circle of fiths and the main colours of the raimbow, while the latter devoted his studies on the relation between colours and intruments's timbre. Drewing ispiration from their results, we tried to merge the two theories with an algorithm that associates a speficic pitch (according to Skrjabin) and a peculiar timbre (according to Kandinskj) to the colours of an image.

<br>

### How does the algorithm work
The image is divided into blocks and the "averaged colour" of each block is stored inside a matrix. The averaged colour of one block is evaluated by averagin the values of the RGB components of each pixel contained in the block. So each element of the matrix will contain three pieces of data: red, green and blue. By pushing the button play, the columns of the matrix are read in sequence while all the rows of a same column are played togther. The sound are produced by activating oscillators in different configurations.
<br>
<div  align="center">
<img width="80%" src="Deliveries/Images/Screen1.png" align="center" />
</div>
<br><br>
<div  align="center">
<img width="80%" src=" " align="center" />
</div>
<br>

### How to use the app
- **Introduction:** press everywhere on the screen to skip the first three introduction pages.
- **Upload an image:** press on the upload button and choose the image you want to hear.
- **Play:** choose the speed by using the slider and press play.

### Technologies and libraries
- Per il giro di pagina le prime due
- Funzione importata per i timbri degli strumenti (sono gli strumenti).

### Project-related challenges
The biggest difficulty of the project was its heterogeneity. A DAW allows you to carry out various operations, and we chose the ones that seemed most significant to us. The project contained many elements, but we tried to have an as modular approach as possible. Instead of writing dedicated code for each instrument, we created classes and shared as much code as possible for each one. Regarding recording, we adopted a different approach for instruments compared to voice because it seemed more useful to save information related to notes rather than a much bulkier audio file in terms of memory.The difficulty with MIDI was establishing the correspondence between sounds and keys, but once resolved, we were able to limit the code by reusing functions like noteon and noteoff, which were already used elsewhere to play the sounds. In particular we observe that differt parts of the MIDI keyboard sometimes are mapped in different ways depending on the device. The main problem was with the pads, so we decided to let the pads play every time we don't have to play the keyboard.
