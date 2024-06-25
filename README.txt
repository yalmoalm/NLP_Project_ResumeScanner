# Resume Matching with Job Description

## Description

This Python script is designed to calculate the similarity between a job description and resumes based on the cosine similarity metric. It utilizes the `scikit-learn` library for text processing and similarity calculations.

## Prerequisites

Before running the script, ensure that you have the following Python libraries installed:

- scikit-learn
- docx2txt

You can install them using pip:

pip install scikit-learn docx2txt

## Usage

1. Prepare your job description and resume files in the `.docx` format.
2. Update the file paths in the script to match the locations of your job description and resume files.
3. Run the script.
4. The script will output the similarity scores between the job description and each resume.

## Code Explanation

1. The script installs the required libraries (`scikit-learn` and `docx2txt`) if they are not already installed.
2. The `docx2txt` library is imported to read the content from the `.docx` files.
3. The `job_descrption`, `resume_1`, and `resume_2` variables are assigned the text content extracted from the respective `.docx` files using `docx2txt.process()`.
4. The job description and resumes are combined into separate lists (`content_1` and `content_2`) for processing.
5. The `CountVectorizer` from `scikit-learn` is used to convert the text data into numerical feature vectors.
6. The `cosine_similarity` function from `scikit-learn` is used to calculate the similarity scores between the job description and each resume.
7. The similarity scores are printed to the console.

## Example Output

[[1.         0.99854213]
[0.99854213 1.        ]] [[1.         0.86523478]
[0.86523478 1.        ]]
Resume matches by 99.85421302445605%
Resume matches by 86.52347826086951%


In this example, the first resume (`Resume 1 (Closer Match).docx`) has a similarity score of 99.85% with the job description, while the second resume (`Resume 2 (Less Matching).docx`) has a similarity score of 86.52%.

## Note

- The script assumes that the `.docx` files are located in the specified file paths. Ensure that the file paths are correct before running the script.
- The script does not perform any preprocessing or normalization of the text data. For more advanced text processing, you may need to add additional steps.
- The similarity scores are calculated based on the bag-of-words model, which considers only the presence and frequency of words, not their order or context.

