# SHA-256 vs MD5 Collision & Performance Demo

A web-based educational tool demonstrating the critical differences between MD5 and SHA-256 hashing algorithms, with interactive performance testing and comprehensive justification for using SHA-256 over MD5 in security applications.

## 🎯 Project Overview

This project provides a hands-on demonstration of cryptographic hash functions, specifically comparing the deprecated MD5 algorithm with the industry-standard SHA-256. Users can:

- Generate and compare hash outputs for custom input
- Run performance benchmarks comparing both algorithms
- View detailed justification reports on why SHA-256 is superior
- Visualize performance differences through interactive charts

## 🚀 Features

### 1. Interactive Hash Generator
- Real-time hash generation for user input
- Side-by-side comparison of MD5 and SHA-256 outputs
- Clean, professional interface

### 2. Performance Benchmarking
- Client-side performance testing with large string inputs
- Statistical results displayed in tabular format
- Visual comparison through dynamic bar charts

### 3. Justification Report
- Detailed comparison of security features
- Real-world attack examples and vulnerabilities
- Industry recommendations and standards compliance
- Appears dynamically after running performance tests

### 4. Modern UI/UX
- Responsive design for desktop and mobile
- Clean, professional styling without gradients
- Smooth animations and transitions
- Accessible color scheme with good contrast

## 📋 Technical Stack

- **HTML5** - Structure and semantic markup
- **CSS3** - Modern styling with animations
- **JavaScript (ES6+)** - Hash generation and chart rendering
- **Chart.js** - Performance visualization
- **Web Crypto API** - Native SHA-256 implementation
- **Custom MD5 Implementation** - Educational JavaScript implementation

## 🛠️ Installation & Setup

### Prerequisites
- A modern web browser (Chrome, Firefox, Edge, Safari)
- Python 3.x (for local server) or any other HTTP server

### Running Locally

1. **Clone the repository**
   ```bash
   git clone https://github.com/ChilliRoger/cyber-assignment.git
   cd cyber-assignment
   ```

2. **Start a local HTTP server**
   
   Using Python:
   ```bash
   python -m http.server 8000
   ```
   
   Or using Node.js (http-server):
   ```bash
   npx http-server -p 8000
   ```

3. **Open in browser**
   ```
   http://localhost:8000/index.html
   ```

### Alternative: Direct File Access
Simply open `index.html` directly in your browser. However, some features may require a local server due to CORS policies.

## 📖 Usage Guide

### Generating Hashes
1. Navigate to the "Hash Generator" section
2. Enter any text in the input field
3. Click "Generate Hashes"
4. View the MD5 and SHA-256 outputs side-by-side

### Running Performance Tests
1. Navigate to the "Performance Test" section
2. Click "Run Speed Test"
3. Wait for the test to complete (~2-5 seconds)
4. View results in:
   - Performance table (numerical values)
   - Bar chart (visual comparison)
   - Justification report (detailed analysis)

## 🔐 Security Considerations

### MD5 Vulnerabilities
- **Collision Attacks**: Multiple practical collision attacks demonstrated since 2004
- **Cryptographic Weakness**: Hash output is only 128 bits (insufficient for modern security)
- **Deprecated Status**: No longer approved by NIST or recommended by security organizations
- **Real-World Exploits**: Used in Flame malware (2012) and rogue certificate generation

### SHA-256 Strengths
- **No Known Collisions**: Remains cryptographically secure since 2001
- **256-bit Output**: Provides sufficient security margin
- **Industry Standard**: Used in Bitcoin, SSL/TLS, code signing
- **FIPS Approved**: Meets government security standards (FIPS 180-4)

### Recommendation
**Never use MD5 for security-critical applications.** Always use SHA-256 or stronger algorithms (SHA-3, BLAKE2, etc.) for:
- Password hashing (preferably with bcrypt/Argon2)
- Digital signatures
- Certificate generation
- Authentication tokens
- Data integrity verification

## 📊 Performance Comparison

Typical results on modern hardware:
- **MD5**: ~100-150ms for 2MB string
- **SHA-256**: ~130-200ms for 2MB string

**Note**: While MD5 is ~30% faster, this negligible performance difference (milliseconds) is far outweighed by its severe security vulnerabilities.

## 🎓 Educational Value

This project is designed for:
- **Cybersecurity Students**: Understanding cryptographic hash functions
- **Developers**: Learning why algorithm choice matters
- **Security Professionals**: Demonstrating vulnerabilities to stakeholders
- **General Audience**: Accessible explanation of complex security concepts

## 📁 Project Structure

```
cyber-assignment/
├── index.html          # Main application file
├── README.md          # Project documentation
└── .git/              # Git repository
```

## 🔧 Technical Implementation

### MD5 Implementation
Custom JavaScript implementation based on the blueimp-md5 library, demonstrating:
- 4 rounds of processing (F, G, H, I functions)
- 128-bit hash output
- Bitwise operations and modular arithmetic

### SHA-256 Implementation
Uses the native Web Crypto API (`crypto.subtle.digest`):
- Hardware-accelerated performance
- Standards-compliant implementation
- Asynchronous processing

### Chart.js Integration
- Dynamic bar chart generation
- Color-coded visualization (red for MD5, green for SHA-256)
- Responsive canvas scaling
- Interactive tooltips

## 🌐 Browser Compatibility

- **Chrome/Edge**: Full support
- **Firefox**: Full support
- **Safari**: Full support (requires HTTPS for crypto.subtle)
- **Mobile Browsers**: Responsive design supported

**Note**: HTTPS is required for the Web Crypto API in production environments.

## 🤝 Contributing

Contributions are welcome! To contribute:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/improvement`)
3. Commit your changes (`git commit -am 'Add new feature'`)
4. Push to the branch (`git push origin feature/improvement`)
5. Open a Pull Request

## 📝 License

This project is open-source and available for educational purposes.

## 👤 Author

**ChilliRoger**
- GitHub: [@ChilliRoger](https://github.com/ChilliRoger)
- Repository: [cyber-assignment](https://github.com/ChilliRoger/cyber-assignment)

## 🙏 Acknowledgments

- MD5 algorithm by Ronald Rivest (1992)
- SHA-256 specification by NIST (FIPS 180-4)
- Chart.js for visualization library
- blueimp-md5 for MD5 implementation reference

## 📚 References

- [NIST FIPS 180-4](https://nvlpubs.nist.gov/nistpubs/FIPS/NIST.FIPS.180-4.pdf) - SHA-256 Specification
- [RFC 6151](https://tools.ietf.org/html/rfc6151) - MD5 Security Considerations
- [OWASP Cryptographic Storage Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Cryptographic_Storage_Cheat_Sheet.html)
- [Web Crypto API Documentation](https://developer.mozilla.org/en-US/docs/Web/API/Web_Crypto_API)

## ⚠️ Disclaimer

This tool is for **educational purposes only**. The MD5 implementation is provided to demonstrate its operation and vulnerabilities, not for production use. Always use established, audited cryptographic libraries for security-critical applications.

---

**Last Updated**: November 2025  
**Version**: 1.0.0
