# Student Attendance Viewer

A modern, interactive React application for tracking and visualizing student attendance data with real-time analytics, filtering, and detailed reporting capabilities.

## Features

✨ **Core Features**
- 📊 **Interactive Dashboard** - Real-time attendance statistics and overview
- 📈 **Data Visualization** - Multiple chart types (Pie, Bar, Line charts) using Recharts
- 🔍 **Advanced Search** - Search students by name with real-time filtering
- 🎯 **Smart Filtering** - Filter by attendance status (Present, Absent, Leave)
- 📋 **Detailed Student View** - Click on any student to see detailed attendance history
- 📱 **Responsive Design** - Works seamlessly on desktop, tablet, and mobile devices
- 🌙 **Dark Mode** - Toggle between light and dark themes
- ⚠️ **Low Attendance Alert** - Highlight students with attendance below threshold
- 📊 **Top Performers** - View top students by attendance percentage

## Tech Stack

- **Frontend Framework**: React 18.2
- **Build Tool**: Vite 5
- **Styling**: Tailwind CSS 3.3
- **Charts**: Recharts 3.8
- **Styling Utilities**: PostCSS + Autoprefixer

## Project Structure

```
student-attendance-viewer/
├── src/
│   ├── components/
│   │   ├── Charts.jsx              # Chart components (Pie, Bar, Line)
│   │   ├── Filters.jsx             # Filter and search components
│   │   ├── Header.jsx              # Header and stats dashboard
│   │   ├── StudentTable.jsx        # Student list table
│   │   ├── StudentDetails.jsx      # Detailed student view
│   │   └── StateComponents.jsx     # Loading, error, and empty states
│   ├── styles/
│   │   ├── animations.css          # Custom animations
│   │   ├── base.css                # Base styles
│   │   └── components.css          # Component-specific styles
│   ├── utils/
│   │   ├── calculations.js         # Data processing functions
│   │   └── dataGeneration.js       # Mock data generation
│   ├── App.jsx                     # Main application component
│   ├── constants.js                # Application constants
│   ├── index.css                   # Global styles
│   └── main.jsx                    # React entry point
├── public/
│   └── vite.svg                    # Vite logo
├── index.html                      # HTML entry point
├── package.json                    # Dependencies and scripts
├── vite.config.js                  # Vite configuration
├── tailwind.config.js              # Tailwind CSS configuration
├── postcss.config.js               # PostCSS configuration
└── README.md                       # This file
```

## Installation

### Prerequisites
- Node.js 18.x or higher
- npm 9.x or higher

### Setup Instructions

1. **Clone the repository**
   ```bash
   git clone https://github.com/smrutisanamsahoo26-glitch/attendance-viewer.git
   cd student-attendance-viewer
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Start the development server**
   ```bash
   npm run dev
   ```
   The application will be available at `http://localhost:5173`

## Available Scripts

### Development
```bash
npm run dev
```
Starts the Vite development server with hot module replacement (HMR).

### Production Build
```bash
npm run build
```
Creates an optimized production build in the `dist/` directory.

### Preview Build
```bash
npm run preview
```
Serves the production build locally for testing.

## Usage

### Main Features

**1. Dashboard Overview**
- View overall attendance statistics at a glance
- See attendance distribution across all students
- Check low attendance alerts for at-risk students

**2. Search Students**
- Use the search bar to find students by name
- Results update in real-time as you type

**3. Filter by Status**
- **All** - View all students
- **Present** - Students present today
- **Absent** - Students marked absent
- **Leave** - Students on approved leave

**4. View Student Details**
- Click any student row to see detailed attendance history
- View attendance percentage and status trends
- See individual attendance records

**5. Visualizations**
- **Pie Chart** - Attendance status distribution
- **Bar Chart** - Top 10 students by attendance percentage
- **Line Chart** - Attendance trends over time

**6. Dark Mode**
- Toggle dark mode using the theme button in the header
- Preference is remembered during your session

## Components

### Header Component
- Displays application title and stats summary
- Contains dark mode toggle
- Shows key attendance metrics

### Dashboard
- Overall attendance statistics
- Quick stats for present, absent, and leave counts
- Average attendance percentage

### Charts Section
- Pie chart: Attendance status breakdown
- Bar chart: Top performing students
- Line chart: Daily attendance trends

### Filter Bar
- Status filtering (All, Present, Absent, Leave)
- Low attendance alert toggle

### Search Bar
- Real-time student search by name

### Student Table
- Sortable student list
- Click row to view details
- Shows student ID, name, status, and percentage

### Student Details Modal
- Detailed view for individual student
- Full attendance history
- Attendance percentage

## Data Structure

### Student Object
```javascript
{
  id: number,
  name: string,
  attendance: number[],        // Daily attendance (0=absent, 1=present, 2=leave)
  percentage: number,          // Attendance percentage
  status: 'Present' | 'Absent' | 'Leave'
}
```

### Filter States
- `All` - Show all students
- `Present` - Students with present status
- `Absent` - Students with absent status
- `Leave` - Students on leave

## Customization

### Change Attendance Threshold
Edit `src/constants.js` to adjust the low attendance warning threshold:
```javascript
export const LOW_ATTENDANCE_THRESHOLD = 75; // Change this value
```

### Modify Data Generation
Update `src/utils/dataGeneration.js` to:
- Change number of students
- Adjust attendance patterns
- Modify date ranges

### Styling
- Edit Tailwind classes in components for design changes
- Modify CSS in `src/styles/` for custom animations and effects
- Update `tailwind.config.js` for theme customization

## Performance Features

- **Memoization**: Uses `useMemo` to optimize chart rendering
- **Efficient Filtering**: Calculates stats only when data changes
- **Lazy Rendering**: Components render only when needed
- **Optimized Charts**: Recharts handles large datasets efficiently

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## Known Limitations

- Mock data is generated client-side (no backend integration yet)
- Data is not persisted between sessions
- Limited to 50 students in current implementation

## Future Enhancements

- 🔌 Backend integration with real database
- 📱 Mobile app version
- 📧 Automated email notifications
- 📑 PDF report export
- 📅 Calendar view for attendance
- 👥 Teacher/Admin dashboard
- 📊 Advanced analytics and predictions
- 🔐 User authentication and role-based access

## Troubleshooting

### Dev server won't start
```bash
# Clear node_modules and reinstall
rm -rf node_modules package-lock.json
npm install
npm run dev
```

### Build fails
```bash
# Clear Vite cache
rm -rf .vite
npm run build
```

### Charts not displaying
- Check browser console for errors
- Verify data is loading correctly
- Clear browser cache and hard refresh

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is open source and available under the MIT License.

## Support

For support, email smrutisanamsahoo26@gmail.com or open an issue on GitHub.

---

**Repository**: https://github.com/smrutisanamsahoo26-glitch/attendance-viewer

**Last Updated**: April 2026
