# Bankmarket_pyspark
## Data Understanding
- The data is related with direct marketing campaigns of a Portuguese banking institution. The marketing campaigns were based on phone calls. Often, more than one contact to the same client was required, in order to access if the product (bank term deposit) would be ('yes') or not ('no') subscribed.
- The classification goal is to predict if the client will subscribe (yes/no) a term deposit (variable y).

- Data Dictionary:
    - Input variables:
    ### bank client data:
    - 1 - age (numeric)
    - 2 - job : type of job (categorical: 'admin.','blue collar','entrepreneur','housemaid','management','retired','self-employed','services','student','technician','unemployed','unknown')
    - 3 - marital : marital status (categorical: 'divorced','married','single','unknown'; note: 'divorced' means divorced or widowed)
    - 4 - education (categorical: 'basic.4y','basic.6y','basic.9y','high.school','illiterate','professional.course','university.degree','unknown')
    - 5 - default: has credit in default? (categorical: 'no','yes','unknown')
    - 6 - balance
    - 7 - housing: has housing loan? (categorical: 'no','yes','unknown')
    - 8 - loan: has personal loan? (categorical: 'no','yes','unknown')
    ### related with the last contact of the current campaign:
    - 9 - contact: contact communication type (categorical: 'cellular','telephone')
    - 10 - day: last contact day of the week (int: 1-7)
    - 11 - month: last contact month of year (categorical: 'jan', 'feb', 'mar', ..., 'nov', 'dec')
    - 12 - duration: last contact duration, in seconds (numeric). Important note: this attribute highly affects the output target (e.g., if duration=0 then y='no'). Yet, the duration is not known before a call is performed. Also, after the end of the call y is obviously known. Thus, this input should only be included for benchmark purposes and should be discarded if the intention is to have a realistic predictive model.
    ### other attributes:
    - 13 - campaign: number of contacts performed during this campaign and for this client (numeric, includes last contact)
    - 14 - pdays: number of days that passed by after the client was last contacted from a previous campaign (numeric; 999 means client was not previously contacted)
    - 15 - previous: number of contacts performed before this campaign and for this client (numeric)
    - 16 - poutcome: outcome of the previous marketing campaign (categorical: 'failure','nonexistent','success')

    ### Output variable (desired target):
    - 17 - y - has the client subscribed a term deposit? (binary: 'yes','no')
