# Athena Batch Tank Calculator - for Athena Pro-Line nutrients

**🚀 [Use the Live Calculator](https://athena.legacy.ag)**
This app is basically a calculator on your phone for the feed charts. https://support.athenaag.com/hc/en-us/articles/17190427112859-Pro-Line-Feed-Schedules

<img width="369" alt="image" src="https://github.com/user-attachments/assets/b35acb87-3020-489b-ab33-cdad3d9d84aa" />

At its core, this is a precise dosage calculator for mixing Athena Pro Line nutrients. It's designed for growers who need to prepare nutrient solutions in a batch tank of any size.

The main advantage of this tool over standard feed charts is its ability to scale recipes automatically. Instead of being limited to fixed per-gallon or per-liter ratios, you can input your exact reservoir volume—whether it's 17 gallons or 250 liters—and get a precise, scaled recipe. This eliminates manual calculations, reduces the risk of mixing errors, and provides the flexibility to use custom concentrate strengths, saving time and ensuring consistency.

**Disclaimer:** This is an independent tool and is not affiliated with, endorsed, or sponsored by Athena. All calculations should be verified. Use at your own risk.

## Features

- **Metric and Imperial Units:** Seamlessly toggle between liters/gallons and grams/pounds for all inputs and calculations. The interface and underlying dosage tables adapt instantly.

- **Persistent Calculation History:** Automatically saves every calculation to your browser's local storage. Each log entry retains all input parameters, including the unit system used, for future reference.

- **Data Export:** Export your entire calculation history to a CSV file for record-keeping or analysis..

- **Default Configuration:** Save your most-used inputs—such as tank size and mix ratios—as the default settings for faster subsequent use.

- **Balance Rate Utility:** Includes a tool to calculate the precise Balance dosage rate (e.g., ml/10L or ml/gal) based on the total volume used to dial in a tank.

- **Flexible Additive Dosages:** Supports calculations for both standard Cleanse and Anolyte.

- **Growth Stage Presets:** Automatically suggests a starting pH and EC when a growth stage is selected, streamlining the workflow.

- **Organized Interface:** A clean, tabbed layout separates the main calculator from the calculation history, preventing clutter.

- **Standalone Operation:** Runs entirely in the browser. No internet connection is required after the initial load. No backend and no user accounts.

- **Responsive Design:** The layout is fully optimized for a seamless experience on both desktop and mobile devices.

## Installation

No installation is required. This is a single, self-contained HTML file.

1. Download the `index.html` file from the `/www/` directory in this repository.
2. Open the file directly in any modern web browser on your computer or mobile device.

## How to Use

The calculator is designed to be intuitive and follows a logical workflow.

1. **Select Unit System:** At the top of the calculator, choose between Metric (liters, grams) and Imperial (gallons, pounds). All fields and calculations will adjust accordingly.

2. **Fill Out Inputs:** On the Calculator tab, work your way down the form:
   - **Growth Stage:** Selecting a stage (e.g., Veg, Flower) will pre-populate recommended pH and EC values.
   - **pH and EC:** Adjust the desired pH and target EC as needed.
     - *Note: The Target EC value directly changes the calculated nutrient dosages. The Desired pH setting does not affect the calculation; it is saved in the log for your records.*
   - **Batch Tank Size:** Enter the volume of your tank.
   - **Balance and Cleanse:** Select the dosage rates for your additives. To determine your Balance rate, you can use the built-in utility by entering the total amount of Balance you used to adjust a tank and clicking "Calc Rate."
   - **Mix Ratios:** Select the concentration of your stock solutions for Core/Fade and Grow/Bloom.

3. **Calculate:** Click the Calculate Dosage button. The results will appear below, showing the precise volume of each nutrient solution to add to your batch tank.

4. **Review History:**
   - Click the History tab to see a list of all past calculations.
   - Each log entry displays the inputs and results and provides options to view the result in a fullscreen, share-friendly format or to delete the entry.

5. **Manage Data:**
   - **Save Defaults:** After filling out the form with your preferred settings, click Save Defaults to store them for your next session.
   - **Export Logs:** From the History tab, click Export to download a CSV file of all your saved calculations.
   - **Clear Logs:** To erase all saved history, click the Clear button in the History tab. You will be asked to confirm this action.

## Understanding Mix Ratios

The calculator allows you to select different mix ratios (e.g., 226 g/L, 240 g/L) for your Core/Fade and Grow/Bloom concentrates. The primary purpose of this feature is to accurately dose from stock solutions that have been mixed at different concentrations based on the packaging the salts came in.

For example:
- The bottles included in the Pro Line Starter Kit are designed to be mixed into 1 gallon of water, resulting in a 226 g/L (or 2 lbs/gallon) concentrate.
- Other packaging, such as the 25 lb bulk bags or smaller sachets, may instruct you to mix with different water volumes, resulting in concentrations like 240 g/L or others.

It is common for a grower to have concentrates of different strengths. You might start with a 226 g/L Core concentrate from a starter kit, and later purchase a bulk bag of Bloom that you mix to 240 g/L.

This calculator's ability to handle these mismatched concentrations is crucial for accuracy. By selecting the correct mix ratio for each part, you ensure that the final dosage calculation is correct, regardless of how your stock solutions were prepared.

## Contributing

Bug reports and pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## License

This project is licensed under the MIT License.
