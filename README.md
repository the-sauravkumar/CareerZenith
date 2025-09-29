# CareerZenith: AI-Powered Job Recommendation System

CareerZenith is an innovative platform that leverages artificial intelligence to provide personalized job recommendations, skill gap analysis, and career development tools. This dynamic system helps job seekers find relevant opportunities while providing helpful insights to improve their employability.

## ✨ Key Features

### 🤖 AI-Powered Job Matching
- Intelligent algorithm that analyzes user profiles to recommend relevant job opportunities
- Real-time job market trend analysis to highlight in-demand positions
- Personalized relevance scoring based on skills, experience, and preferences

### 📊 Interactive Skill Gap Analysis
- Visual representation of user skills compared to market demands
- Color-coded skill categorization (Tech, Sales, Marketing, etc.)
- Animated progress bars showing proficiency levels for different skills

### 🔄 Dynamic Resume Builder
- Interactive resume creation with real-time preview
- AI-generated professional summaries based on user-provided bullet points
- Multiple animated templates with customizable themes and layouts

### 📰 Employment News Feed
- Curated industry news with visual cards and hover animations
- Real-time updates on job market trends and opportunities
- Interactive news filtering and categorization

## 🚀 API Endpoints

### Authentication Service
```javascript
// POST /api/auth/login
{
  "email": "user@example.com",
  "password": "securePassword123"
}

// POST /api/auth/register
{
  "name": "John Doe",
  "email": "john@example.com",
  "password": "securePassword123"
}

// GET /api/auth/profile
// Returns user profile information
```

### Job Recommendation Service
```javascript
// GET /api/recommend_jobs/:userId
// Returns personalized job recommendations

// GET /api/trending_skills
// Returns current trending skills in the job market

// GET /api/skill_gap_analysis/:userId
// Returns detailed skill gap analysis
```

### Resume Service
```javascript
// POST /generate-pdf/
{
  "name": "John Doe",
  "email": "john@example.com",
  "phone": "123-456-7890",
  "summary": "Experienced software developer...",
  "skills": ["JavaScript", "React", "Node.js"],
  "projects": [
    {
      "name": "E-commerce Platform",
      "description": "Built a full-stack e-commerce solution"
    }
  ],
  "template": "modern"
}

// POST /summarize/
{
  "bullets": [
    "5 years of experience in web development",
    "Led a team of 7 developers",
    "Increased site performance by 40%"
  ]
}
```

### News Service
```javascript
// GET /news
// Returns latest employment and industry news
```

## 💻 Technical Architecture

### Frontend
- React.js with animated UI components and transitions
- Redux for state management
- Responsive design with interactive elements
- Dynamic theme switching with smooth transitions

### Backend
- Microservices architecture for scalability
- RESTful API design with comprehensive documentation
- Firebase Authentication and Firestore database
- AI integration for intelligent job matching and skill analysis

## 🌈 User Interface Features

### Animated Components
- Hover effects on job cards that elevate and highlight on interaction
- Smooth transitions between form steps in the resume builder
- Animated progress indicators for skill proficiency levels
- Loading animations during data fetching operations

### Interactive Dashboard
- Real-time data visualization with animated charts
- Skill gap representation with dynamic color-coded categories
- Animated notifications for new job matches and recommendations
- Interactive job filtering with smooth transition effects

## 📱 User Flow

1. **Registration & Onboarding**
   - Create account with email/password or social login
   - Complete interactive profile setup with skill selection
   - Set job preferences and career goals

2. **AI Assessment**
   - Analyze user profile and experience
   - Generate visual skill gap analysis
   - Provide animated charts showing market positioning

3. **Job Discovery**
   - Browse personalized job recommendations with interactive cards
   - Filter opportunities with animated transitions
   - Save favorite positions with visual feedback

4. **Resume Enhancement**
   - Create professional resume with interactive builder
   - Generate AI-powered summaries from simple bullet points
   - Preview and download with animated transitions

5. **Skill Development**
   - Access personalized course recommendations
   - Track progress with animated indicators
   - Receive visual feedback on skill improvements

## 🔧 Implementation Details

### Job Recommendation Algorithm
```javascript
const calculateRelevanceScore = (job, user) => {
  let score = 0;
  
  // Exact skill matches (weighted heavily)
  user.skills.forEach(skill => {
    if (job.requiredSkills.includes(skill)) {
      score += 25;
    }
  });
  
  // Location preference match
  if (job.location === user.preferredLocation || 
      (user.remotePreference && job.remote)) {
    score += 15;
  }
  
  // Experience level match
  if (Math.abs(job.experienceYears - user.experienceYears)  {
  const [width, setWidth] = useState(0);
  
  useEffect(() => {
    // Animate progress bar on mount
    setTimeout(() => {
      setWidth(level * 20); // Convert level (1-5) to percentage
    }, 300);
  }, []);
  
  return (
    
      {skill}
      
        
      
      {level}/5
    
  );
};
```

## 🚀 Future Enhancements

- AI-powered interview preparation with simulated conversations
- Animated career path visualization showing potential growth trajectories
- Real-time collaboration tools for resume review and feedback
- Gamified skill development with interactive challenges and rewards

## 🛠️ Installation

```bash
# Clone the repository
git clone https://github.com/the-sauravkumar/CareerZenith.git

# Navigate to project directory
cd CareerZenith

# Install dependencies
npm install

# Set up environment variables
cp .env.example .env
# Edit .env with your configuration

# Start the development server
npm run dev

```

- For more detailed guide check `Instructions_For_Setup.txt` file

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](https://github.com/AvishekDas5/CareerZenith/blob/main/LICENSE) file for details.
