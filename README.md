# AI for Software Engineers: Neural Networks Challenges

## Summary

The purpose of these challenges is to gain an under-the-hood understanding of how neural networks work. Each challenge correlates to a section of the [AI for Software Engineers](https://frontendmasters.com/workshops/engineering-and-ai/) by Will Sentance for [Frontend Masters](https://frontendmasters.com/).

Throughout these challenges, we will cover topics such as traditional machine-learning approaches, data representation, parameters, generalization, overfitting, and validation.

## Getting Started

Make a copy of [this spreadsheet](https://docs.google.com/spreadsheets/d/1J_CkPBp2RTHsdt6qe_rYheSzk2DRyuuZINlWvIyHVrc/edit?usp=sharing).
You are welcome to work in Google Sheets or Microsoft Excel.

_Note: formula hints will be provided for Google Sheets and may not directly translate to Microsoft Excel formulas._

## Part 1: Traditional Machine Learning Approaches
We have been tasked with building a model for a food delivery app that predicts whether or not refund requests are valid.

Our sample set of training data (spanning cells `B6`-`F11`) has pulled four refund requests from our greater population. In this challenge, you will "train" your model to predict whether or not refunds will be accepted based on the historical data provided in our sample by identifying boundaries and producing the "best fit" for our sample.

Our models have different values associated with them (boundaries, weights, intercepts, etc.) that we call **parameters**. Based on these parameters, we hope to create a model with the highest instance of correct conversions.

Review the values in the training data.

1. Based on the valid and invalid refund requests in our sample set, we need to identify a set of parameters - in this case, boundaries - to create and train our model.

   - What set of boundaries (spanning cells `H16`-`J20`) will recreate the same refund outcomes (rows `11` & `21`, columns `C`-`F`) for the given dataset?
     - Keep in mind that this is open-ended! In other words, there are multiple boundary conditions that _could_ work.

   - How many parameters must be met (i.e. TRUE) for a refund to be considered warranted? (This is also open-ended!)

   - Once you've built out your boundaries, enter a boolean prediction based on whether or not the individual piece of data would pass or fail based on the established boundary.

2. Determine whether or not your model returns good predictions.

   - How can you confirm that you've trained the model on your sample dataset? What would make a prediction "good"?
	 
   - Adjust your boundaries until all of the prediction data (spanning cells `L16`-`P22`) is confirmed as a good prediction.

3. Validate your model by applying your boundaries to the validation data (spanning cells `B27`-`D32`).

   - How well did your boundaries work on the validation data? Are there enough parameters being met to grant refunds to Will and Hannah?

### How do I know whether or not my model "works"?

Apply the same boundaries to your validation data. How accurate (or not) were your model's predictions?

**Does your model generalize?** Our training data is only a small subset of our population data. Generalization is the opposite of overfitting. It ensures that our model can make predictions about the broader data set instead of simply memorizing the data in the sample set.

**What is [overfitting](https://developers.google.com/machine-learning/crash-course/overfitting/overfitting)?** Overfitting refers to when a model matches (memorizes) the training set so closely that the model actually fails when it comes to making correct predictions when it comes to new data. An overfit model is analogous to an invention that performs well in the lab but is worthless in the real world.

## Traditional Approach Extension(s)

### Low-code solutions with Google Sheets

*Coming Soon*

## Part 2: Introducing Neural Networks

Our sample data set contains two images of a face pulled from a population of all 4,096 possible combinations of grey and white cells in a 3x4 grid. Each image is a 3 x 4 cell representation of a face, where each cell would represent a single pixel with grey squares representing the eyes and mouth. In this ssample set we have an example of a collection of pixels that represents a smile and a collection of pixels that represents a frown -- or more simply a smile and not a smile.
In this challenge, our goal is to build and train our model using a single layer of weights (represented by a matrix of boolean values) to recognize whether or not similar groupings of grey and white pixels (cells) are also smiles.

**Navigate to the sheet labeled 'Single Layer NN' in the spreadsheet linked above. In this sheet, we have a set of 5 images: two images in our sample set and three images in our validation set.**

1. Compare the grey and white pixels in the smile (reference cell) and frown (reference cell) representations. Which pixel(s) indicate the difference between whether or not the shaded pixels represent a smile?

	- For the smile image in the sample data set, which cell(s) indicate that the image is a smile?

	- For the frown image in the sample data set, which cell(s) indicate the image is not a smile?

2. Adjust your weights in the relevant cells to establish a good fit for our model.

3. Based on your weights, does our model match the target?

	- If not, how can we adjust our weights to ensure that our model is a good fit for our sample set?

