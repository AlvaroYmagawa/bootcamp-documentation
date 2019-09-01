# Date-fns
A package for data-type variable manipulat.

## Installation
```bash
# Install date-fns in your last version
yarn add data-fns@next
```

## Time manipulation

### Check for past dates
Here we have a past dates validation, if a date in the body request is older than the current date throws an error.
* Example: https://github.com/AlvaroYmagawa/GoStack08/blob/master/Node.js/Date-fns/PastDates.txt

### Check date availability

Here we have a date availibility validation, if the user try to create a new appointment in the same date of another one throws a error.
* Example: https://github.com/AlvaroYmagawa/GoStack08/blob/master/Node.js/Date-fns/dateAvailibility.txt

### Get values between a range
* First you need to import this methods
```bash
import { startOfDay, endOfDay, parseISO } from 'date-fns';
import { Op } from 'sequelize';
```

* Example: https://github.com/AlvaroYmagawa/GoStack08/blob/master/Node.js/Date-fns/dateBetween.txt


### Formating text 
* Example: https://github.com/AlvaroYmagawa/GoStack08/blob/master/Node.js/Date-fns/formatingText.txt



