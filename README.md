# Skip All Lessons on Udemy to Get Course Certificate

This script automates the process of marking all sections and lessons complete on Udemy, enabling users to quickly obtain course certificates without going through each lesson manually.

## Usage

### Prerequisites

- A web browser with developer tools (tested on Google Chrome)
- Basic knowledge of using browser developer tools

### Instructions

1. **Access Udemy Course Page:** Log in to your Udemy account and navigate to the course you want to complete.

2. **Open Developer Console:** Right-click on the page and select "Inspect" or press `F12` (Windows) to open the Developer Tools.

3. **Navigate to Console Tab:** In the Developer Tools window, navigate to the "Console" tab.

4. **Paste Script:** Copy the provided JavaScript code below and paste it into the Console.

```javascript
const sections = document.querySelectorAll("div.accordion-panel-module--panel--Eb0it.section--section--yXfqc");
for (let section of sections) {
    if (!section.querySelector('span[data-checked="checked"]')) {
        section.querySelector('div').click();
    }
}
const checkBoxes = document.querySelectorAll('[data-purpose="progress-toggle-button"]')
for(let checkBox of checkBoxes){
    if(!checkBox.checked){
        checkBox.click();
    }
}
```

5. **Execute Script:** Press `Enter` to execute the script. The script will automatically mark all sections and lessons as complete.

6. **Verify Progress:** Once the script has finished running, verify that all sections and lessons are marked as complete.

7. **Get Certificate:** After completing all sections and lessons, you can proceed to obtain the course certificate.

## Important Notes

- **Use Responsibly:** This script is intended for educational purposes and convenience. Please use it responsibly and respect the terms of service of Udemy.

- **Check Compatibility:** The script was tested on Google Chrome. Compatibility with other browsers may vary.

- **Customization:** You may need to adjust the script if Udemy updates its website structure or layout.

- **Feedback:** If you encounter any issues or have suggestions for improvement, feel free to open an issue or submit a pull request.

## Disclaimer

This script is provided as-is, without any warranty or guarantee. The developers are not responsible for any misuse or consequences resulting from the use of this script.
