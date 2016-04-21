# Bayes Hack 2016
### Department of Health and Human Services prompt #2

_How can data get help to sufferers of opioid addication?_

##Prompt

In 2013, 71% of prescription drug overdose deaths involved opioid painkillers. That same year, nearly two million Americans aged 12 or older either abused or were dependent on opioid painkillers. In recent years, even as the epidemic of prescription opioid abuse has eased somewhat, there has been a dramatic increase in overdose deaths related to heroin: death counts increased sixfold between 2001 and 2014.
How can we leverage technology to detect abuse in early stages—perhaps by examining individual prescription use patterns—and to administer interventions, such as naloxone, in innovative and effective treatment plans?

## In this Repo

* `data/CDC` - Opioid overdose death in United States from 1999 to 2014. This dataset was retrieved from [here](http://wonder.cdc.gov). For more information about the query criteria, please refer to `analysis/Opioid Overdose Deaths.ipynb`.
    * `oos_by_cause_of_death_state_level.txt`: grouped by State, Year, Underlying Cause of death, Multiple Cause of death
    * `oos_by_cause_of_death_demographics_nationwide.txt`: grouped by Year, Multiple Cause of death, Ten-Year Age Groups, Gender, Race.
    * `oos_by_demographics_state_level.txt`: grouped by State, Year, Ten-Year Age Groups, Gender, Race

* `analysis/` - iPyton notebook files (which you can view right here on GitHub) loading the data and exploring a few things. Good to understand the datasets and get ideas for your project. _If_ you want to run this notebook, run `pip install -r requirements.txt` inside a virtualenv first.


##Other Resources
* The Substance Abuse and Mental Health Services Administration (SAMHSA) compiles an [Opioid Overdose Prevention Toolkit](http://store.samhsa.gov/shin/content//SMA16-4742/SMA16-4742.pdf) as a primer for caregivers and first-responders on the signs and treatments of various complications of opioid abuse.
* The CDC [aggregates data](http://www.cdc.gov/drugoverdose/data/overdose.html) on prescription opioid overdoses.
* The Centers for Medicare & Medicaid Services anonymize and collect [geographic opioid prescription claim data](https://www.cms.gov/Research-Statistics-Data-and-Systems/Statistics-Trends-and-Reports/Medicare-Provider-Charge-Data/OpioidMap.html) down to a ZIP code level.
* SAMHSA reports [a wide variety](http://www.samhsa.gov/data/) of aggregate datasets related to substance abuse. Consider checking for data that's related to a particular project direction with this prompt.

##Data Quirks

###Important things to know or notice
* In using CDC data, please not that drug overdose deaths were classified using the International Classification of Disease, Tenth Revision (ICD-10), based on the ICD-10 underlying cause-of-death codes:
    * X40–44 (unintentional)
    * X60–64 (suicide)
    * X85 (homicide)
    * Y10–Y14 (undetermined intent)

    Among the deaths with drug overdose as the underlying cause, the type of opioid involved is indicated by the following ICD-10 multiple cause-of-death codes:

    * opioids (T40.0, T40.1, T40.2, T40.3, T40.4, or T40.6)
    * natural and semisynthetic opioids (T40.2)
    * methadone (T40.3)
    * synthetic opioids other than methadone (T40.4); and heroin (T40.1)

