# Airbnb-price-category-prediction

One of the biggest problems when people prepare to post a new listing on airbnb is, how much should one ask for? Of course the most intuitive way is to check how other similar postings price their apartment/house. 
So in this project, we are going to predict the listing price based on the listing characteristics 🔥🔥, in this way to optimize user experience and lower the bar to be a new host😍 !

Predicting the actual price could be simple (well you can just go search online 👍), so we cut the pricing into three different bins for classification 😂. For each listing, we recommend a pricing range to the new host rather than a fix price (how nice is that!). So we define three categories: beginner, plus, premium based on the created listing. Respectively we use 0, 1, 2 to denote these three categories.

The dataset contains listings of different areas in Montreal during 2019. It comes with rich information for each listing, including a link to the thumbnails etc. 

Note: We will follow a multi-objective (multi-task) multi-modality solution.

_________________________________________________________________________________

The notebook consists of:

1) General Questions & their answers to enhance understanding the problem domain.
2) Problem Questions & their answers to enhance understanding the problem solutions.
3) Import important libraries.
4) Import data.
   - You will find the data link in ("Link of competition on Kaggle") file attached above.
5) Data Exploration.
6) Working on data "Data Translation".

   - After displaying the dataset we found that, it contains two languages (English and French). So we should translate it to one of two languages so we should unify the language to English language by using the translator.
   
7) Trial 1
   - We will use tokenization only on text as it contains some text preprocessing and one convolutional layer with some small number of filters on images with max pooling layer after that

8) Trial 2
   - We will apply english translation over our data to unify our language to english and use the rest operations as the previous trial

9) Trial 3
   - We will use the same as the previous trial but with adding the LSTM layer in text part with some adjustments that they are:

       1) give the two targets(price & type) equal loss_weights(.5) instead of (1&0 for type)
       2) add dropout to both text & image parts so we can overcome overfitting
       3) use different optimizer(sgd)

10) Trial 4
    - We will use the same as previous trail except replacing lstm layer with bi-directional lasm layer.

11) Trial 5
    - We will do the same as the previous trial but with replacing bi directional lstm layer with GRU layer.

12) Trial 6
    - In this trial we will use different preprocessing on the text with applying the translation, also we will replce the previous added layers with averaged layer again.

13) Bonus trial
    - We will use transfer learning model with our problem(VGG 19).

Note: Each trial came with its plan, observations and its explanation in details.

Competition link on Kaggle: https://www.kaggle.com/competitions/cisc-873-dm-f22-a4
