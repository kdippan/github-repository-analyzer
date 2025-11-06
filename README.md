# 🔍 GitHub Repository Analyzer

A beautiful, modern web application to extract and visualize GitHub repository details with comprehensive analytics. Features include repository health scoring, commit analysis, contributor statistics, language distribution charts, and real-time data from GitHub API with glassmorphism UI design.

[![Live Demo](https://img.shields.io/badge/demo-live-success?style=for-the-badge)](https://github-repository-analyzer.netlify.app)
[![GitHub](https://img.shields.io/badge/GitHub-Repository-blue?style=for-the-badge&logo=github)](https://github.com/KDippan/github-repository-analyzer)
[![License](https://img.shields.io/badge/license-MIT-green?style=for-the-badge)](LICENSE)

![GitHub Repository Analyzer](https://img.shields.io/badge/Status-Active-brightgreen?style=flat-square)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)

---

## ✨ Features

### 📊 **Comprehensive Analytics**
- **Repository Metadata Extraction**: Name, description, owner, creation date, last updated, visibility, license, topics, stars, forks, watchers
- **Language Distribution**: Visual pie chart showing programming language breakdown
- **Commit Analysis**: Timeline visualization with commit activity tracking
- **Contributor Statistics**: Bar charts and rankings of top contributors
- **Issues & Pull Requests**: Complete tracking of open/closed issues and PRs
- **File System Browser**: Navigate repository structure with file listings
- **Repository Health Score**: Algorithm-based scoring for repository quality

### 🎨 **Modern Design**
- **Glassmorphism UI**: Beautiful glass morphism effects with backdrop blur
- **Responsive Layout**: Works seamlessly on desktop, tablet, and mobile
- **Dark Theme**: Eye-friendly dark color scheme with vibrant accents
- **Smooth Animations**: AOS (Animate On Scroll) library integration
- **Interactive Charts**: Chart.js powered visualizations
- **Material Icons**: Google Material Icons throughout

### 🚀 **Advanced Functionality**
- **GitHub API Integration**: Real-time data fetching from GitHub REST API
- **Authentication Support**: Optional token support for increased rate limits (60 → 5000 requests/hour)
- **Rate Limit Tracking**: Live display of remaining API requests
- **Error Handling**: Graceful error messages and validation
- **Loading States**: Skeleton loaders and progress indicators
- **Example Repositories**: Quick access to popular repos (React, VS Code, Next.js, TensorFlow)

---

## 🎯 Use Cases

- **Developers**: Quickly analyze repositories before contributing or forking
- **Project Managers**: Monitor team activity and repository health
- **Recruiters**: Evaluate candidate contributions and project engagement
- **Researchers**: Study open-source project patterns and trends
- **Students**: Learn from popular repositories and understand project structures

---

## 🖼️ Screenshots

### Dashboard Overview
![Dashboard](https://via.placeholder.com/800x450/0f172a/6366f1?text=Dashboard+Overview)

### Commit Analysis
![Commits](https://via.placeholder.com/800x450/0f172a/8b5cf6?text=Commit+Timeline)

### Contributors Ranking
![Contributors](https://via.placeholder.com/800x450/0f172a/ec4899?text=Top+Contributors)

---

## 🛠️ Technologies Used

| Technology | Purpose |
|------------|---------|
| **HTML5** | Semantic markup and structure |
| **CSS3** | Modern styling with Flexbox/Grid, animations, glassmorphism |
| **JavaScript (ES6+)** | Async/await, Fetch API, DOM manipulation |
| **Chart.js** | Interactive data visualizations |
| **AOS** | Animate On Scroll library |
| **GitHub REST API** | Real-time repository data |
| **Google Fonts** | Inter, Poppins, Fira Code typography |
| **Material Icons** | Comprehensive icon library |

---

## 🚀 Getting Started

### Prerequisites
- Modern web browser (Chrome, Firefox, Safari, Edge)
- Internet connection for API requests
- (Optional) GitHub Personal Access Token for increased rate limits

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/KDippan/github-repository-analyzer.git
   cd github-repository-analyzer
   ```

2. **Open locally**
   ```bash
   # Simply open index.html in your browser
   open index.html
   
   # Or use a local server (recommended)
   python -m http.server 8000
   # Visit http://localhost:8000
   ```

3. **Deploy to Netlify** (Recommended)
   - Drag and drop the folder to [Netlify Drop](https://app.netlify.com/drop)
   - Or connect your GitHub repository for automatic deployments

### Usage

1. **Enter Repository URL**
   - Paste any GitHub repository URL (e.g., `https://github.com/facebook/react`)
   - Click "Analyze" button

2. **Add GitHub Token** (Optional)
   - Click "Add Token" button in header
   - Generate a token at [GitHub Settings > Developer Settings > Personal Access Tokens](https://github.com/settings/tokens)
   - Required scopes: `public_repo` (for public repos)
   - Increases rate limit from 60 to 5000 requests/hour

3. **Explore Tabs**
   - **Overview**: Repository stats, language distribution
   - **Commits**: Commit timeline and history
   - **Contributors**: Top contributors and their stats
   - **Issues & PRs**: Open/closed issues and pull requests
   - **Files**: Repository file structure
   - **Analytics**: Health score and engagement metrics

---

## 📊 Data Extracted

### Repository Information
- ✅ Name, description, owner
- ✅ Creation & last update dates
- ✅ Stars, forks, watchers count
- ✅ Open issues count
- ✅ License type
- ✅ Topics/tags
- ✅ Default branch
- ✅ Repository size
- ✅ Programming languages

### Commit Data
- ✅ Commit history (last 100)
- ✅ Commit messages
- ✅ Author information
- ✅ Commit dates
- ✅ Activity timeline

### Contributors
- ✅ Top 30 contributors
- ✅ Contribution counts
- ✅ Contributor profiles

### Issues & Pull Requests
- ✅ Open/closed issues
- ✅ Pull request status
- ✅ Issue titles and authors
- ✅ Creation dates

### Files & Contents
- ✅ Root directory structure
- ✅ File/folder names
- ✅ File sizes
- ✅ Content types

---

## ⚠️ Limitations

| Limitation | Details |
|------------|---------|
| **API Rate Limits** | 60 requests/hour (unauthenticated), 5000/hour (with token) |
| **Directory Listings** | Limited to 1,000 files via API |
| **Private Repositories** | Requires authentication token with appropriate scopes |
| **Large Repositories** | May require pagination for complete data (handled automatically) |
| **Repository Size** | Recommended under 5GB for optimal performance |

---

## 📈 Repository Health Scoring

The app calculates a health score (0-100) based on:

- **Recent Activity** (30 points): Commits in last 30 days
- **Community Engagement** (45 points): Stars and forks (logarithmic scale)
- **Documentation** (10 points): Has wiki, description
- **Issue Management** (15 points): Ratio of closed to total issues

**Score Interpretation:**
- 🟢 **80-100**: Excellent - Very healthy repository
- 🟡 **60-79**: Good - Active and maintained
- 🟠 **40-59**: Fair - Moderate activity
- 🔴 **0-39**: Poor - Low activity or maintenance

---

## 🎨 Design System

### Color Palette
```css
Primary: #6366f1 (Indigo)
Secondary: #8b5cf6 (Purple)
Accent: #ec4899 (Pink)
Background: #0f172a (Dark Blue)
Surface: #1e293b (Slate)
Text: #f8fafc (Off White)
```

### Typography
- **Primary Font**: Inter (UI elements)
- **Secondary Font**: Poppins (Headings)
- **Monospace Font**: Fira Code (Code blocks)

### Effects
- Glassmorphism with backdrop blur
- Smooth transitions and animations
- Gradient backgrounds
- Shadow elevations
- Hover state transformations

---

## 🔒 Privacy & Security

- **No Data Collection**: All analysis happens client-side
- **Local Storage**: Optional GitHub token stored locally in browser
- **No Server**: Direct API calls to GitHub (no intermediary)
- **Open Source**: Complete transparency of code

---

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. **Fork the repository**
2. **Create a feature branch** (`git checkout -b feature/AmazingFeature`)
3. **Commit your changes** (`git commit -m 'Add some AmazingFeature'`)
4. **Push to the branch** (`git push origin feature/AmazingFeature`)
5. **Open a Pull Request**

### Ideas for Contributions
- Add more visualizations (heatmaps, network graphs)
- Implement repository comparison feature
- Add export to PDF functionality
- Create browser extension version
- Add dark/light theme toggle
- Implement search history
- Add bookmark feature
- Improve mobile responsiveness

---

## 📝 Roadmap

- [ ] Compare multiple repositories side-by-side
- [ ] Dependency tree visualization
- [ ] Security vulnerabilities check integration
- [ ] Code frequency analysis
- [ ] Commit heatmap calendar
- [ ] Repository recommendations based on analysis
- [ ] Export reports as PDF
- [ ] Browser extension version
- [ ] Light theme support
- [ ] Keyboard shortcuts
- [ ] Advanced search filters
- [ ] Bookmark and save favorite repos
- [ ] Historical data tracking

---

## 🐛 Known Issues

- Rate limit may be reached quickly without authentication token
- Very large repositories (>10,000 files) may have incomplete file listings
- Some private repositories may not be accessible even with tokens

---

## 📚 Resources

- [GitHub REST API Documentation](https://docs.github.com/en/rest)
- [Chart.js Documentation](https://www.chartjs.org/docs/latest/)
- [AOS Animation Library](https://michalsnik.github.io/aos/)
- [Material Icons Guide](https://fonts.google.com/icons)
- [Glassmorphism Design Trend](https://uxdesign.cc/glassmorphism-in-user-interfaces-1f39bb1308c9)

---

## 📄 License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

```
MIT License

Copyright (c) 2025 KDippan

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

## 👤 Author

**KDippan**

- GitHub: [@KDippan](https://github.com/KDippan)
- Project Link: [github-repository-analyzer](https://github.com/KDippan/github-repository-analyzer)
- Live Demo: [github-repository-analyzer.netlify.app](https://github-repository-analyzer.netlify.app)

---

## 🌟 Acknowledgments

- GitHub for providing the comprehensive REST API
- Chart.js team for excellent visualization library
- AOS library for smooth scroll animations
- Material Design team for beautiful icons
- Open source community for inspiration

---

## 💖 Support

If you find this project useful, please consider:

- ⭐ Starring the repository
- 🐛 Reporting bugs and issues
- 💡 Suggesting new features
- 🔀 Contributing code
- 📢 Sharing with others

---

<div align="center">

**Built with ❤️ by developers, for developers**

[🌐 Live Demo](https://github-repository-analyzer.netlify.app) • [📖 Documentation](https://github.com/KDippan/github-repository-analyzer/wiki) • [🐛 Report Bug](https://github.com/KDippan/github-repository-analyzer/issues) • [✨ Request Feature](https://github.com/KDippan/github-repository-analyzer/issues)

---

Made with 💻 and ☕ | Powered by GitHub API | © 2025 KDippan

</div>