# Marketing Case study (with social/economic context)

This dataset contains information about a marketing campaign of a digital service provider. The dataset includes 41188 entries with 20 input variables and one output variable. The task is to predict if the client will subscribe to the offered service based on the given informations about the last contact of the current campaign. The dataset includes variables such as the clients job, education, housing, loan, contact communication type, day of the week, duration of the last contact, and others. The dataset is a good example for a binary classification task with a social/economic context.

## dataset info

- Target variable: The binary classification task is to predict if the user will subscribe to the service or not (variable y).
- N = 41188 
- Missing attribute values:
There are missing values in the categorical attributes, all labelled as "Unbekannt".
These columns with missing values can be used to apply data cleaning and imputation techniques. 

## Input variables:
   ### Demographic data
   1.  Alter : age (numeric)
   2.  Beruf : type of job (categorical)
   3.  marital : marital status (categorical)
   4.  Bildung: education (categorical)
   5.  Kreditverpflichtung: has credit in default? (categorical)
   6.  Wohnsituation: has housing loan? (categorical)
   7.  Kredit: has personal loan? (categorical)
   ### Related with the last contact of the current campaign
   8.  Kontakt: contact communication type
   9.  Monat: last contact month of year
  10.  Wochentag: last contact day of the week (categorical)
  11.  Dauer: last contact duration, in seconds (numeric). Important note: this attribute highly affects the output target (e.g., if duration=0 then y="no"). Yet, the duration is not known before a call is performed. Also, after the end of the call y is obviously known. Thus, this input should only be included for benchmark purposes and should be discarded if the intention is to have a realistic predictive model.
  ### Other attributes
  12.  Kampagne: number of contacts performed during this campaign and for this client (numeric, includes last contact)
  13.  Kontaktversuche: number of days that passed by after the client was last contacted from a previous campaign (numeric; 999 means client was not previously contacted)
  14.  Vorherige Kontaktanzahl: number of contacts performed before this campaign and for this client (numeric)
  15.  Vorheriges Ergebnis: outcome of the previous marketing campaign (categorical)
  ### Social and economic context attributes
  16.  Arbeitslosenquote: employment variation rate - quarterly indicator (numeric)
  17.  Verbraucherpreisindex: consumer price index - monthly indicator (numeric)     
  18.  Verbraucher-Konfidenzindex: consumer confidence index - monthly indicator (numeric)     
  19.  Euribor 3M: euribor 3 month rate - daily indicator (numeric)
  20.  Arbeitnehmerquote: number of employees - quarterly indicator (numeric)
  ### Target variable
  21.  y - has the user subscribed?  (binary)

## virtual environment
create conda environment with python 3.11

install requirements.txt via
```
conda install --yes --file requirements.txt
```