# Luhn’s Algorithm

This repository is a template project for performing the stage 2 interview with back-end candidates.

## Implement

The following is an error check algorithm used for testing if a card numberis valid. Given a card number:

1. From the last digit moving backwards, double every second digit
2. If the doubled number is greater than 9, add it’s two digits together
3. Sum all card digits together (taking the value of step 2 for every second digit)
4. If the summed total’s end digit is a zero, it is a valid card number

## Test cases

There is a ```CardNumberValidationServiceTest``` class, it has the following two example card numbers declared as statics. Implement tests using these example numbers to assert your algorithm is working correctly:

<div style="text-align: center;">
    <table>
        <tr>
            <td>4242424242426742</td>
            <td>Valid</td>
        </tr>
        <tr>
            <td>1111111111111111</td>
            <td>Invalid</td>
        </tr>
    </table>
</div>

## Reason

1. Explain how your implementation works
2. If you were given more time, how might you change your implementation to be better?

## REST Endpoint

There is a ```CardNumberValidationController``` class in the project, leveraging Spring:

1. Register ```CardNumberValidationService``` as a service so it can be autowired
2. Register ```CardNumberValidationController``` as a REST controller so it is detected by the ApplicationContext
3. Add an endpoint to the controller that allows card numbers to be RESTfully validated via the ```CardNumberValidationService``` algorithm implemented earlier