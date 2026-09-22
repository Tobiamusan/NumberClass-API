# Number Classification API

A REST API that classifies numbers and returns mathematical properties.

## Endpoint

GET `/api/classify-number?number=371`

## Response

```json
{
"number": 371,
"is_prime": false,
"is_perfect": false,
"properties": ["armstrong", "odd"],
"digit_sum": 11,
"fun_fact": "371 is an Armstrong number."
}

## API Behavior

### Valid Request

Example:

GET `/api/classify-number?number=371`

Returns HTTP `200` with the number's classification details.

### Invalid Request

Example:

GET `/api/classify-number?number=alphabet`

Returns HTTP `400`:

```json
{
"number": "alphabet",
"error": true
}