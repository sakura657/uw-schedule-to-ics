# UW-Madison Course Schedule → ICS Export Tool

🔗 Try it live → [https://sakura657.github.io/uw-schedule-to-ics](https://sakura657.github.io/uw-schedule-to-ics)

[简体中文](README_CN.md) | English

A web-based tool to export your UW-Madison course schedule to iCalendar (.ics) format for easy import into calendar applications like Google Calendar, Apple Calendar, Outlook, and more.

## 🎯 Features

- **Easy Export**: Convert your UW course schedule to standard iCalendar format
- **Timezone Accurate**: Properly handles Central Time (America/Chicago) with DST support
- **Customizable Alerts**: Set default reminders for all classes
- **Location Support**: Includes classroom locations in calendar events
- **Responsive Design**: Works on desktop and mobile devices
- **UW-Madison Branding**: Official university colors and styling

## 🚀 Quick Start

1. **Get Your Schedule HTML**:
   - Log in to [MyUW Home](https://my.wisc.edu)
   - Open "Course Schedule"
   - Select your term and click "Update"
   - Right-click → "View Page Source"
   - Select all (Ctrl/Cmd+A) and copy (Ctrl/Cmd+C)

2. **Use the Tool**:
   - Open `index.html` in your web browser
   - Paste the HTML source code
   - Set term start and end dates
   - Choose alert preferences
   - Click "Generate ICS File"

3. **Import to Calendar**:
   - Download the generated `.ics` file
   - Import into your preferred calendar app

## 📋 Requirements

- Modern web browser (Chrome, Firefox, Safari, Edge)
- Access to UW-Madison MyUW portal
- Internet connection (for Tailwind CSS and fonts)

## 🛠️ Technical Details

### Supported Event Types
- ✅ Lecture (LEC)
- ✅ Laboratory (LAB) 
- ✅ Seminar (SEM)
- ✅ Discussion (DIS)
- ⚠️ Online courses (skipped if no specific meeting times)

### Timezone Handling
- All events exported with `TZID=America/Chicago`
- Automatic Daylight Saving Time (DST) transitions
- Proper weekday calculation for Central Time

### Data Processing
- Parses course schedule HTML from MyUW
- Extracts meeting times, locations, and course information
- Generates RFC-compliant iCalendar format
- Handles recurring weekly events with term end dates

## 🎨 UI Features

- **Modern Design**: Clean, professional interface with Tailwind CSS
- **UW Branding**: Official university red (#c5050c) color scheme
- **Responsive Layout**: Optimized for all screen sizes
- **Step-by-step Guide**: Clear instructions with numbered steps
- **Form Validation**: Helpful error messages and input validation

## 🔧 Troubleshooting

### Common Issues

**"Cannot find const data = { ... }; block"**
- Ensure you copied the complete HTML source
- Make sure your browser language is set to English
- Try refreshing the MyUW page and copying again

**"No events found inside data block"**
- Verify you selected the correct term
- Check that you have enrolled courses for the selected term

**Events appear on wrong days**
- This has been fixed in the latest version
- The tool now properly handles timezone conversion for weekdays

### Browser Compatibility
- ✅ Chrome 90+
- ✅ Firefox 88+
- ✅ Safari 14+
- ✅ Edge 90+

## 📁 File Structure

```
Export-ICS-UW-Madison/
├── index.html    # Main application file
├── README.md              # English documentation
├── README_CN.md           # Chinese documentation
└── images/                # (Optional) Favicon and assets
```

## 🤝 Contributing

Contributions are welcome! Please feel free to submit issues or pull requests.

### Development Setup
1. Clone the repository
2. Open `index.html` in your browser
3. Make changes and test with sample UW schedule data

## 📄 License

This project is open source and available under the MIT License.

## 🙏 Acknowledgments

- University of Wisconsin-Madison for the course schedule system
- Tailwind CSS for the styling framework
- FullCalendar for calendar inspiration

## 📞 Support

If you encounter issues:
1. Check the troubleshooting section above
2. Ensure you're using a supported browser
3. Verify your UW schedule HTML is complete
4. Open an issue on GitHub with details

---

**Note**: This tool is not officially affiliated with UW-Madison. It's a community-created utility to help students manage their schedules.
