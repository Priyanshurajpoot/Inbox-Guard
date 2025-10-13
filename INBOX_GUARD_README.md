# 🛡️ Inbox Guard - Advanced Gmail Security & Intelligence

![Inbox Guard Logo](icon128.png)

**Inbox Guard** is a powerful Chrome extension that provides advanced email analysis and security scanning for Gmail. It uses Gmail API with OAuth authentication to intelligently analyze your latest unread emails, detect threats, and provide actionable insights.

[![Chrome Extension](https://img.shields.io/badge/Chrome-Extension-yellow.svg)](https://github.com/Priyanshurajpoot/Inbox-Guard/releases)
[![Version](https://img.shields.io/badge/version-2.0.0-blue.svg)](https://github.com/Priyanshurajpoot/Inbox-Guard/releases)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)
[![GitHub Issues](https://img.shields.io/github/issues/Priyanshurajpoot/Inbox-Guard)](https://github.com/Priyanshurajpoot/Inbox-Guard/issues)

---

## 👨‍💻 About the Developer

**Priyanshu Rajpoot**  
*MCA Post Graduate | Python Developer | Prompt Engineer | AI Enthusiast*

- 🔗 **LinkedIn**: [priyanshux5](https://linkedin.com/in/priyanshux5)
- 💻 **GitHub**: [Priyanshurajpoot](https://github.com/Priyanshurajpoot)
- 📧 **Email**: priyanshux5xraj@gmail.com

**Core Interests**: Prompt Engineering, Artificial Intelligence, Machine Learning, NLP, Generative AI  
**Primary Skills**: Python, PyQt5, PyTorch, Transformers, OpenCV, Chrome Extension API, OAuth 2.0, Data Analysis, GUI Development

---

## ✨ Features

### 🔍 Intelligent Email Analysis
- **Email Summary** - Concise 1-3 line summary of email content
- **Category Detection** - Automatic classification of email types
- **Sentiment Analysis** - Advanced sentiment detection toward the recipient
- **Threat Detection** - Phishing and spam identification

### 🛡️ Security Features
- **Phishing Detection** - Identifies suspicious patterns and phishing attempts
- **Spam Classification** - Detects promotional and spam content
- **Risk Assessment** - Provides security risk levels for emails
- **OAuth Security** - Secure Gmail API integration with proper authentication

### 📊 Analysis Categories
- **Phishing** - Suspicious account verification requests
- **Spam** - Lottery, prize, and promotional content
- **Finance** - Banking, transactions, and payment-related
- **Work** - Professional and business communications
- **Social** - Social media notifications and updates
- **Promo** - Marketing and promotional offers
- **Personal** - Friendly and personal communications
- **Unknown** - Unclassified or neutral content

### 🎭 Sentiment Analysis
- **Positive** - Friendly and appreciative tone
- **Negative** - Disappointed or concerned tone
- **Angry** - Hostile or demanding language
- **Frustrated** - Confused or struggling tone
- **Appreciative** - Grateful and thankful tone
- **Neutral** - Professional and balanced tone

---

## 🚀 Installation

### Option 1: Chrome Web Store (Coming Soon)
1. Visit Chrome Web Store
2. Search for "Inbox Guard"
3. Click "Add to Chrome"

### Option 2: Manual Installation
1. **Download the latest release** from [Releases](https://github.com/Priyanshurajpoot/Inbox-Guard/releases)
2. **Extract the ZIP file** to a folder
3. **Open Chrome** and go to `chrome://extensions/`
4. **Enable Developer mode** (toggle in top-right)
5. **Click "Load unpacked"** and select the extracted folder
6. **Pin the extension** for easy access

---

## 🎯 How to Use

### Initial Setup
1. **Click the Inbox Guard icon** in Chrome toolbar
2. **Grant Gmail permissions** when prompted (OAuth2)
3. **Accept the scopes** for Gmail API access

### Scanning Emails
1. **Navigate to Gmail** in your browser
2. **Click the Inbox Guard icon**
3. **Click "Scan Latest Email"**
4. **View the analysis results** including:
   - Sender information and email
   - Email subject and summary
   - Category classification
   - Sentiment analysis
   - Security assessment

### Understanding Results

#### Categories:
- 🔴 **Phishing** - Immediate attention required
- 🟡 **Spam** - Consider marking as spam
- 🔵 **Finance** - Financial communications
- 🟢 **Work** - Professional emails
- 🟣 **Social** - Social media notifications
- 🟠 **Promo** - Marketing content
- ⚪ **Personal** - Personal communications

#### Sentiment:
- 😊 **Positive** - Friendly and constructive
- 😟 **Negative** - Concerns or issues
- 😠 **Angry** - Hostile or demanding
- 😤 **Frustrated** - Confused or struggling
- 🙏 **Appreciative** - Grateful and thankful
- 😐 **Neutral** - Balanced and professional

---

## 🏗️ Architecture

### Project Structure
```
Inbox-Guard/
│
├── manifest.json          # Extension configuration
├── popup.html            # Main popup interface
├── popup.css             # Popup styling
├── popup.js              # Main application logic
├── content.js            # Gmail DOM interaction
├── sentiment.js          # Sentiment analysis engine
├── background.js         # Background service worker
├── icons/                # Extension icons
│   ├── icon16.png
│   ├── icon48.png
│   └── icon128.png
└── README.md             # Documentation
```

### Core Components

#### 1. **Popup Interface** (`popup.html`, `popup.css`, `popup.js`)
- Main user interface for the extension
- OAuth authentication handling
- Email analysis display
- Real-time status updates

#### 2. **Content Script** (`content.js`)
- Gmail DOM interaction and scraping
- Fallback email data extraction
- Navigation detection
- Real-time Gmail monitoring

#### 3. **Sentiment Analysis** (`sentiment.js`)
- Advanced sentiment detection algorithms
- Contextual understanding
- Emotional tone classification
- Pattern recognition

#### 4. **Gmail API Integration**
- OAuth 2.0 authentication
- Secure API communication
- Email content fetching
- Real-time scanning

---

## 🔧 Technical Details

### Gmail API Integration
```javascript
// OAuth2 Authentication
chrome.identity.getAuthToken({ interactive: true }, (token) => {
  // API requests with bearer token
  fetch('https://www.googleapis.com/gmail/v1/users/me/messages', {
    headers: { 'Authorization': `Bearer ${token}` }
  });
});
```

### Sentiment Analysis Engine
The sentiment analyzer uses:
- **Word pattern matching** for emotional indicators
- **Contextual analysis** for nuanced understanding
- **Phrase recognition** for complex sentiments
- **Negation handling** for accurate classification

### Security Features
- **OAuth 2.0** secure authentication
- **Minimal permissions** principle
- **Local processing** for privacy
- **No data storage** on external servers

---

## 🛠️ Development

### Prerequisites
- Chrome Browser (version 88+)
- Basic knowledge of Chrome Extensions
- Gmail account for testing

### Building from Source

1. **Clone the repository**:
```bash
git clone https://github.com/Priyanshurajpoot/Inbox-Guard.git
cd Inbox-Guard
```

2. **Load in Chrome**:
   - Open `chrome://extensions/`
   - Enable "Developer mode"
   - Click "Load unpacked"
   - Select the project folder

3. **Make changes** and reload the extension

### File Structure Details

#### `manifest.json`
- Extension metadata and permissions
- OAuth2 configuration
- Content script definitions
- Icon specifications

#### `popup.js`
- Main application logic
- Gmail API communication
- Analysis orchestration
- UI state management

#### `sentiment.js`
- Sentiment word dictionaries
- Analysis algorithms
- Score calculation
- Result formatting

---

## 📊 Analysis Algorithms

### Category Detection
```javascript
detectCategory(subject, body) {
  const text = `${subject} ${body}`.toLowerCase();
  
  // Phishing patterns (highest priority)
  const phishingPatterns = [
    /verify.*account/i, /account.*suspended/i,
    /urgent.*action.*required/i, /confirm.*identity/i
  ];
  
  if (phishingPatterns.some(pattern => pattern.test(text))) {
    return 'phishing';
  }
  // ... more category logic
}
```

### Sentiment Analysis
```javascript
analyze(text) {
  // Count sentiment words with weights
  let positiveScore = this.countWords(text, this.positiveWords);
  let negativeScore = this.countWords(text, this.negativeWords);
  let angryScore = this.countWords(text, this.angryWords) * 2;
  
  // Calculate ratios and determine sentiment
  const totalScore = positiveScore + negativeScore + angryScore;
  const posRatio = positiveScore / totalScore;
  
  return this.determineSentiment(posRatio, angryScore);
}
```

---

## 🔒 Privacy & Security

### Data Handling
- **Local Processing**: All analysis happens locally in your browser
- **No Data Storage**: Email content is not stored or transmitted
- **Minimal Permissions**: Only required Gmail API scopes
- **OAuth Security**: Secure token-based authentication

### Permissions Justification
- `activeTab`: To interact with Gmail interface
- `storage`: For extension settings and cache
- `identity`: For OAuth2 Gmail API authentication
- `https://mail.google.com/*`: To access Gmail
- `https://www.googleapis.com/*`: For Gmail API calls

---

## 🐛 Troubleshooting

### Common Issues

**"Authentication Failed"**
- Ensure you're logged into Gmail in Chrome
- Check internet connection
- Verify OAuth client configuration

**"No Unread Emails Found"**
- Check if you have unread emails in Gmail
- Refresh Gmail page
- Ensure you're in the primary inbox

**"Analysis Not Working"**
- Reload the extension
- Check Chrome console for errors
- Verify Gmail API quotas

### Debug Mode
Enable debug logging in the extension for detailed troubleshooting:

1. Open Chrome Developer Tools
2. Go to Console tab
3. Look for "Inbox Guard" logs

---

## 🤝 Contributing

We welcome contributions! Here's how you can help:

1. **Report Bugs**: [Open an issue](https://github.com/Priyanshurajpoot/Inbox-Guard/issues) with detailed description
2. **Suggest Features**: Share your ideas for improvements
3. **Code Contributions**: Fork the repo and submit pull requests
4. **Improve Documentation**: Help make Inbox Guard more accessible

### Development Setup
```bash
# Clone the repository
git clone https://github.com/Priyanshurajpoot/Inbox-Guard.git
cd Inbox-Guard

# Load in Chrome extensions developer mode
# Make your changes and test
```

### Code Style
- Use consistent JavaScript ES6+ syntax
- Follow Chrome Extension best practices
- Maintain clean and documented code
- Test across different Gmail interfaces

---

## 📝 Roadmap

### Planned Features
- [ ] **Batch Scanning** - Analyze multiple emails at once
- [ ] **Custom Rules** - User-defined classification rules
- [ ] **Advanced ML** - Machine learning-based analysis
- [ ] **Export Reports** - Save analysis results
- [ ] **Email Templates** - Quick response suggestions
- [ ] **Multi-language** - Support for non-English emails
- [ ] **Real-time Monitoring** - Automatic email analysis
- [ ] **Integration** - Connect with other security tools

### Under Development
- [ ] **Enhanced Phishing Detection** - Improved pattern recognition
- [ ] **Sentiment History** - Track sender sentiment over time
- [ ] **Priority Inbox** - Smart email prioritization

---

## 📄 License

This project is licensed under the MIT License:

```text
MIT License

Copyright (c) 2024 Inbox Guard

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## 📞 Support & Contact

- **🐛 Report Issues**: [GitHub Issues](https://github.com/Priyanshurajpoot/Inbox-Guard/issues)
- **🚀 Downloads**: [GitHub Releases](https://github.com/Priyanshurajpoot/Inbox-Guard/releases)
- **💬 Discussions**: [GitHub Discussions](https://github.com/Priyanshurajpoot/Inbox-Guard/discussions)
- **📧 Email**: priyanshux5xraj@gmail.com
- **👨‍💻 Developer**: [Priyanshu Rajpoot](https://linkedin.com/in/priyanshux5)

---

## 🙏 Acknowledgments

Built with:
- **Chrome Extension API** - Extension framework
- **Gmail API** - Email access and authentication
- **OAuth 2.0** - Secure authentication protocol
- **Modern JavaScript** - ES6+ features and async/await

Special thanks to:
- The Chrome Extensions community
- Beta testers and early users
- Open source contributors

---

## 🔗 Quick Links

- **📂 Repository**: [Inbox Guard on GitHub](https://github.com/Priyanshurajpoot/Inbox-Guard.git)
- **🚀 Releases**: [Latest Releases](https://github.com/Priyanshurajpoot/Inbox-Guard/releases)
- **🐛 Issues**: [Report Issues](https://github.com/Priyanshurajpoot/Inbox-Guard/issues)
- **👨‍💻 Developer**: [Priyanshu Rajpoot](https://linkedin.com/in/priyanshux5)

---

**Python Developer | Prompt Engineer | AI Enthusiast**  
*Building intelligent security solutions for modern communication*

---

## AUTHOR
**Priyanshu Rajpoot**  
*MCA Post Graduate | Chrome Extension Developer | AI Enthusiast*