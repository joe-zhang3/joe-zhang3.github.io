# Activity module 

__Change log__



__Notes__

1. Relationships
    - 1:* means 1:many
    - 1:1: means 1:1
2. The activity does have a `login-location` relationship which is deprecated already. 

## Activity

__Relationships__

  name | relationship | map in CCM | comments
  -|-|-|-|
  type|1:1| |activity type
  season|1:1| | season of the activity
  category|1:1||
  sub-category|1:1|||
  tax-location|1:1|||
  inventory-location|1:1|||
  ar-accounts|1:1|||
  group|1:1||group of the activity belongs to
  waiver|1:1||waivers of the activity, including online waiver and in-house waiver
  grade|1:1||grade required by the activity, includes min grade and max grade
  gender|1:1|| 
  membership-discount-group|1:1|| **TODO**
  required-vendors|1:*||**TODO**
  scholarship-group|1:1||**TODO**
  prerequisites|1:*||
  pass-skills|1:*||
  general-fees|1:*|| fees setup of the activity
  account|1:1||**TODO** 
  custom-earned-dates|1:*|| setup earned dates for this activity, which is manily used for payment schedule
  staff|1:*||
  payment-schedules|1:*||
  custom-field-group|1:1||setup custom questions etc
  registration-alert|1:1||
  documents|1:*||
  domains|1:*||
  init-payment-type|1:1||**TODO**
  payment-method|1:1||**TODO**
  status|1:1||status of the activity
  condiational-reg-dates|1:*||conditional reg dates, like who has a membership can register earlier etc
  label-group|1:1||**TODO**
  vendor-season-assns|1:*||**TODO**


__Attributes__

  name | map in CCM | comments
  -|-|-|
  name| | 
  code| | activity code (**TODO**)
  start-date| |
  end-date| |
  start-time| |
  end-time| |
  weekdays| | 
  sessions| | **TODO**
  description| | 
  in-house-reg-start-datetime| |
  in-house-reg-end-datetime| |
  online-reg-start-datetime| |
  online-reg-end-datetime| |
  online-display-start-datetime| |
  online-display-end-datetime| |
  online-reg-limit||
  enroll-min|| **TODO**
  enroll-max|| **TODO**
  age-min-year||
  age-min-month||
  age-min-as-of|| datetime
  age-max-year||
  age-max-month||
  age-max-as-of||datetime
  age-required||boolean. If this true, all 6 above properties will be valid
  grade-required||boolean
  gender-required||boolean
  scholarship-percent|| **TODO**
  scholarship-amount|| **TODO**
  deferred-rev-opt|| enum **TODO**
  confirmation-notes||
  receipt-notes||
  init-payment-amount||
  use-waitlist||boolean, indicate if waitlist can be used for this activity
  prerequisites-required||boolean, if true, prerequisites will be valid

## Registration

__Relationships__

name | relationship | map in CCM | comments
-|-|-|-|
individual|1:1|| individual of this registration
account|1:1||
activity|1:1||
origianl-registration|1:1||the original registration of the current registration which might be modified/transfered etc.
custom-values|1:*|| answers for those custom field questions if have

__Attributes__

name | map in CCM | comments
-|-|-|
status|| enum. status of the registration, active, waitlist, tentatinve, deleted
pass-status|| boolean
in-house-flag|| boolean. indicates if the registration is made in-house
notes||
waiver-date||
registration-date||
waitlist-date||
created-date||
modified-date||
created-by||
modified-by||


## Purchase

