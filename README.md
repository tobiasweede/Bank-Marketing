# Case study

# Marketing Case study (with social/economic context)

## dataset info

- Target variable: The binary classification task is to predict if the user will subscribe to the service or not (variable y).
- N = 41188 
- Missing attribute values:
There are missing values in the categorical attributes, all labelled as "unknown".
These columns with missing values can be used to apply data cleaning and imputation techniques. 
- Input variables:
   ### demographic data
   1.  age (numeric)
   2.  job : type of job (categorical: "admin.","blue-collar","entrepreneur","housemaid","management","retired","self-employed","services","student","technician","unemployed","unknown")
   3.  marital : marital status (categorical: "divorced","married","single","unknown"; note: "divorced" means divorced or widowed)
   4.  education (categorical: "basic.4y","basic.6y","basic.9y","high.school","illiterate","professional.course","university.degree","unknown")
   5.  default: has credit in default? (categorical: "no","yes","unknown")
   6.  housing: has housing loan? (categorical: "no","yes","unknown")
   7.  loan: has personal loan? (categorical: "no","yes","unknown")
   /./related with the last contact of the current campaign:
   8.  contact: contact communication type (categorical: "cellular","telephone") 
   9.  month: last contact month of year (categorical: "jan", "feb", "mar", ..., "nov", "dec")
  10.  day_of_week: last contact day of the week (categorical: "mon","tue","wed","thu","fri")
  11.  duration: last contact duration, in seconds (numeric). Important note:  this attribute highly affects the output target (e.g., if duration=0 then y="no"). Yet, the duration is not known before a call is performed. Also, after the end of the call y is obviously known. Thus, this input should only be included for benchmark purposes and should be discarded if the intention is to have a realistic predictive model.
  ### Other attributes
  12.  campaign: number of contacts performed during this campaign and for this client (numeric, includes last contact)
  13.  pdays: number of days that passed by after the client was last contacted from a previous campaign (numeric; 999 means client was not previously contacted)
  14.  previous: number of contacts performed before this campaign and for this client (numeric)
  15.  poutcome: outcome of the previous marketing campaign (categorical: "failure","nonexistent","success")
  // Social and economic context attributes
  16.  emp.var.rate: employment variation rate - quarterly indicator (numeric)
  17.  cons.price.idx: consumer price index - monthly indicator (numeric)     
  18.  cons.conf.idx: consumer confidence index - monthly indicator (numeric)     
  19.  euribor3m: euribor 3 month rate - daily indicator (numeric)
  20.  nr.employed: number of employees - quarterly indicator (numeric)

  ### Target variable
  21.  y - has the user subscribed?  (binary: "yes","no")


## virtual environment
create conda environment with python 3.11

install requirements.txt via
```
conda install --yes --file requirements.txt
```