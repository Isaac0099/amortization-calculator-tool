# Amortization Calculator

A JavaScript class for calculating loan amortization schedules and analyzing loan costs. This calculator provides precise calculations for loan payments while handling rounding appropriately.

## Features

- Calculate monthly loan payments
- Generate detailed amortization schedules
- Calculate total loan costs including interest
- Precise calculations with appropriate rounding for display

## Installation

```javascript
import AmortizationCalculator from './AmortizationCalculator';
```

## Usage

### Basic Example

```javascript
const calculator = new AmortizationCalculator();

// Calculate for a $200,000 loan at 5.5% for 30 years
const principal = 200000;
const annualInterestRate = 5.5;
const loanTermYears = 30;

// Get monthly payment
const monthlyPayment = calculator.calculateMonthlyPayment(
    principal,
    annualInterestRate,
    loanTermYears
);

// Get complete payment schedule
const schedule = calculator.generateAmortizationSchedule(
    principal,
    annualInterestRate,
    loanTermYears
);

// Get total cost breakdown
const costs = calculator.calculateLoanCosts(
    principal,
    annualInterestRate,
    loanTermYears
);
```

## Error Handling

The calculator includes input validation and will throw errors for:
- Non-numeric inputs
- Zero or negative values
- Invalid values for calculations

## Precision

- All values are rounded to 2 decimal places for display
- Final payment is adjusted to ensure the loan is fully paid off
