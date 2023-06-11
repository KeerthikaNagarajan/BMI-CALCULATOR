# EX-08: 
## CREATE A BMI CALCULATOR
### AIM:
The aim of this code is to create a BMI (Body Mass Index) calculator using React. The calculator takes inputs for weight and height and calculates the BMI value based on the provided values. It then displays the calculated BMI value to the user.
### ALGORITHM:
1. Create a functional component called "BMICalculator".
2. Use the useState hook to define state variables for weight, height, and bmi.
3. Implement a function called "calculateBMI" that calculates the BMI value using the weight and height inputs.
4. Update the BMI state variable with the calculated BMI value.
5. Export the BMICalculator component as the default export.
### PROGRAM:
```javascript
import React, { useState } from 'react';

function BMICalculator() {
  const [weight, setWeight] = useState('');
  const [height, setHeight] = useState('');
  const [bmi, setBMI] = useState(null);

  const calculateBMI = () => {
    const heightInMeters = height / 100;    
    const bmiValue = weight / (heightInMeters * heightInMeters);
    setBMI(bmiValue.toFixed(2));
  };

  return (
    <div>
      <h2>BMI Calculator</h2>
      <div>
        <label htmlFor="weight">Weight (kg):</label>
        <input
          type="text"
          id="weight"
          value={weight}
          onChange={(e) => setWeight(e.target.value)}
        />
      </div>
      <div>
        <label htmlFor="height">Height (cm):</label>
        <input
          type="text"
          id="height"
          value={height}
          onChange={(e) => setHeight(e.target.value)}
        />
      </div>
      <button onClick={calculateBMI}>Calculate BMI</button>
      {bmi && <p>Your BMI is: {bmi}</p>}
    </div>
  );
}

export default BMICalculator;

```
### OUTPUT:

<img width="364" alt="1" src="https://github.com/KeerthikaNagarajan/BMI-CALCULATOR/assets/93427089/0a9a5477-f91c-4465-b24b-88754fc77076">

<img width="345" alt="2" src="https://github.com/KeerthikaNagarajan/BMI-CALCULATOR/assets/93427089/16dd2140-2cd4-4e1b-9b03-d711010090ff">

### RESULT:
The code will generate a BMI calculator with input fields for weight and height. 
