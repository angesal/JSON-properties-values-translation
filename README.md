# JSON-properties-values-translation
Translate the propertie values of a given JSON up to 4 indentation level

Given a JSON object and a transalation object with a list of translation terms and their translation, the code loops through the JSON checking if the terms are in the list and translating those terms that match.
The code checks if there are objects inside the JSON covering up to 4 indentation level.

Example of initial JSON object:

```

var myObj =
{
"ACCOUNT": {
    "DETAILS": {
      "IBAN_REQUEST": "IBAN request",
      "IBAN_REQUEST_SUBTITLE": "is waiting for IBAN approval",
      "IBAN_FIELD": "IBAN",
      "BIC_FIELD": "BIC",
      "CURRENCY_FIELD": "Currency",
      "ADDITIONAL_ACCOUNT_NUMBER_FIELD": "Additional account number",
      "APPROVE_DECLINE_IBAN_REQUEST": "Approve or decline IBAN request",
      "SUMMARY": {
        "REQUESTER": "Applicant",
        "REGISTRATION_NUMBER": "Company registration number",
        "DATE": "Date"
      }
    }
  }
};

```

Example of translation object:

```
var myTrans =
{
"USERNAME":"Nombre de usuario","CURRENCY_FIELD":"Divisa", "REQUESTER":"Solicitante", "Date":"Fecha"
}

```

The resulting object will change these property values in the original object.

In the future this should be encapsulated in a function, but for the moment you can just copy and paste the code in https://jsfiddle.net or in your javascript console and run it.

We've added the code to download the resulting JSON (see https://jsfiddle.net/cowboy/hHZa9/)
You'll need to add jQuery extension in order to run it.

