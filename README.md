# Medical Informatician Test: Blood pressure extraction

## Preface

Most hospitals store thier past medical records in image of scanned paper. That results in difficulty to query information.
Now, you are assigned to solve this problem by transform the images into digitalized records in database.

Fortunately, you don't have to extract the information from these images by yourself because our team have already done.
However, the extracted data are free text, consisting of misspelling due to dirty noise, crumple, wrinkle, scanning quality and numerous factors.

## Your challenge (1/3)

You receive the extracted text from blood pressure-recording fields in [data/bp.json](data/bp.json). Now, you have to:  

1. Extract the systolic and diastolic blood pressure into numeric format and save into TSV file as table 1
2. Separate the abnormal values or unextractable rows into another TSV as table 2
3. Put your code and result into your github and send the link to email [contact@sati.co.th](mailto:contact@sati.co.th)

## Your challenge (2/3)

Your team love your approach to solve the problem. they want to embed your solution into their pipeline.

1. Explain the way to integrate your solution into the pipeline. Discuss pros, cons and when to choose each choice
2. Write in readme file of the Challenge 1 repo

## Your chalenge (3/3)

Finally, we choose to deploy your algorithm by API.

1. Create another github repo for this task.
2. Deploy your algorithm in API
3. Write document to run and to use the API in readme file
4. For extra score
   1. Build your API container image. And write script to start it.
   2. Some framework also automatically generate documentation. Please write document in it.
5. Do not forget to send the link of github to [contact@sati.co.th](mailto:contact@sati.co.th)
