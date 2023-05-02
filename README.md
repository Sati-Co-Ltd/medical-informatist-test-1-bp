# Medical Informatician Test: Blood pressure extraction

## Prerequisite

1. Challenge (1/3)
   1. We prefer python. But if you have better approach, you can show it to us.
   2. Explain the code
2. Challenge (3/3)
   1. Use any programming language
   2. Separate github repo from other challenges

## Preface

Most hospitals store thier past medical records in image of scanned paper. That results in difficulty to query information.
Now, you are assigned to solve this problem by transform the images into digitalized records in database.

Fortunately, you don't have to extract the information from these images by yourself because our team have already done.
However, the extracted data are free text, consisting of misspelling due to dirty noise, crumple, wrinkle, scanning quality and numerous factors.

## Your challenge (1/3)

You receive the extracted text from blood pressure-recording fields from Adult out-patient department in [data/bp_text.json](./data/bp_text.json). Now, you have to:  

1. Extract the systolic and diastolic blood pressure into numeric format and save into TSV file as [table 1](#table-1).
2. Separate the abnormal values or unextractable rows into another TSV as [table 2](#table-2).
3. Put your code or your notebook and result into your github and send the **link** to email [contact@sati.co.th](mailto:contact@sati.co.th).

We ensure that [all data](./data/bp_text.json) are only the values of blood pressure, and not mixed with other fields.

### Table 1

| encounterId | rawInput     | systolicBP | diastolicBP |
| ----------- | ------------ | ---------- | ----------- |
| example1    | 12080        | 120        | 80          |
| example2    | 194/112 mmHg | 194        | 112         |
| example2    | BP = 94;62   | 94         | 62          |

### Table 2

| encounterId | rawInput | systolicBP | diastolicBP | reason                       |
| ----------- | -------- | ---------- | ----------- | ---------------------------- |
| example3    | 123      |            |             | one value of BP              |
| example3    | 90/12    | 90         | 12          | DBP: lower than normal range |
| example3    | ล้อนั่ง     |            |             | non-numeric value            |

You can design the label of reason by yourself.  

### (Fun) fact about blood pressure

Blood pressure (BP) consists of two values: systolic and diastolic blood pressure. Systolic BP (SBP) is always higher than diastolic BP (DBP). Their units are millimeter of mercury (mmHg). In general, they are recorded in slash-separated pair (SBP/DBP), e.g. 120/80 mmHg.  

The usual range of BP are 90/60 to 180/120 mmHg. But, sometimes, you can see people walking to OPD (out-patient department) with BP lower than 90/60 mmHg or greater than 180/120 mmHg. So, the possible range of BP in OPD situation is 80 - 250 mmHg for SBP and 40 - 150 mmHg for DBP.  

Healthcare staff usually measures your BP once at OPD. However, for some situation, such as abnormal value, monitoring treatment, or special examination, they will measures your BP for multiple times. **But for this test, the BP is measured once per encouter.**

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
