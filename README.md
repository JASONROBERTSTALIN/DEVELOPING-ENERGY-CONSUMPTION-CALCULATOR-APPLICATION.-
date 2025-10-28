# DEVELOPING-ENERGY-CONSUMPTION-CALCULATOR-APPLICATION.-

## AIM:
To develop an android application to perform energy calculation.

## APPARATUS REQUIRED:
ØComputer
ØAndroid studio software


## THEORY:
The Energy Calculator App allows the user to calculate the energy consumption of electrical appliances based on power usage (in watts) and time (in hours). The app takes these two inputs, calculates the energy consumed in kilowatt-hours (kWh), and displays the result. This experiment involves basic arithmetic calculations and user input handling in Android. It uses EditText for input, Button for user interaction, and TextView to display the result. The app demonstrates how to handle user input for numerical values and perform unit conversions. It is a useful application for understanding how to develop apps that perform mathematical calculations based on user input.

## PROCEDURE:
1. Open Android Studio and then click on File -> New -> New project. 24. Then type the application name as “ex.no.3″ and click Next.
2. Then select the Minimum SDK as shown below and click next. 26. Then select the Empty Activity and click next.
3. Finally click Finish.
4. Click on app -> java -> com.example -> MainActivity.java
5. Now click on Text and type the program, so now the programming part of the main activity is completed.
6. Click on app -> res -> layout -> activity_main.xml.
7. Now click on Text and type the program, so now the designing part of Activity main is also completed.
8. Select the suitable available device to display the output. 33. Now run the application to see the output. 

## PROGRAM:
```
package com.example.energycalculator;

import android.os.Bundle;
import android.widget.Button;
import android.widget.EditText;
import android.widget.TextView;
import android.widget.Toast;
import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {

    private EditText wattsInput, hoursInput;
    private Button calculateButton;
    private TextView resultView;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        wattsInput = findViewById(R.id.watts);
        hoursInput = findViewById(R.id.hours);
        calculateButton = findViewById(R.id.calc);
        resultView = findViewById(R.id.result);

        calculateButton.setOnClickListener(v -> calculateEnergy());
    }

    private void calculateEnergy() {
        String wattsText = wattsInput.getText().toString().trim();
        String hoursText = hoursInput.getText().toString().trim();

        if (wattsText.isEmpty() || hoursText.isEmpty()) {
            Toast.makeText(this, "Please enter both values", Toast.LENGTH_SHORT).show();
            return;
        }

        double watts = Double.parseDouble(wattsText);
        double hours = Double.parseDouble(hoursText);

        double energyUsed = (watts * hours) / 1000.0;
        resultView.setText("Energy Used: " + energyUsed + " kWh");
    }
}
```

## OUTPUT:
<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/1d2e5c5e-2002-4f08-ae95-f6bf2d6065d6" />




## RESULT:
Thus, the energy consumption calculator app is developed and the output is verified. 

