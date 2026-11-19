# Portfolio Project Data — Calgeo - 2D Geometry Calculator

- **Category:** `desktop-mobile` (Mobile App)
- **Category Label:** `Mobile App`
- **Accent Color:** `amber`
- **Target Assets Folder:** `public/images/projects/calgeo_2d_geometry_calculator/`
- **Required Local Images:** `banner.webp`, `image01.webp`

## TypeScript Data (`ProjectCaseStudy`)

```typescript
{
  "id": "calgeo-2d-geometry-calculator",
  "code": "PRO-22 // APP-01",
  "title": "Calgeo - 2D Geometry Calculator",
  "category": "desktop-mobile",
  "categoryLabel": "Mobile App",
  "year": "2022",
  "status": "Completed",
  "accentColor": "amber",
  "repoUrl": "https://github.com/weztcy/Calgeo---2D-Geometry-Calculator",
  "license": "MIT License",
  "imageUrl": "/images/projects/calgeo_2d_geometry_calculator/banner.webp",
  "images": [
    "/images/projects/calgeo_2d_geometry_calculator/banner.webp"
  ],
  "summary": "An offline Android geometry utility for computing accurate area and perimeter metrics across eight standard 2D shapes with real-time validation.",
  "projectDescription": "Calgeo is a native Android calculation app designed to simplify 2D geometric evaluations. Built with Java and Material Design, it delivers instant mathematical precision, dynamic input generation, and strict geometric boundary validation without requiring any network connectivity or permissions.",
  "architectureSummary": "Modular client architecture decoupling Android Jetpack UI, dynamic input bindings, geometric business logic, and validation rules.",
  "techStack": [
    "Java",
    "Android SDK",
    "Android Jetpack",
    "Material Design Components",
    "ViewBinding",
    "Navigation Component",
    "ConstraintLayout",
    "RecyclerView",
    "JUnit",
    "Espresso",
    "Gradle"
  ],
  "telemetryMatrix": {
    "projectType": "Native Mobile Utility",
    "targetPlatform": "Android 8.0+ (API 26-36)",
    "primaryDomain": "Computational Geometry",
    "architecturePipeline": "Clean ViewBinding & Modular Utils",
    "testingAndAudit": "Verified",
    "projectStatus": "Completed",
    "projectYear": "2022"
  },
  "desktopMobileProjectInfo": {
    "applicationType": "Native Mobile Utility",
    "targetPlatform": "Android",
    "developmentStatus": "Completed",
    "developmentYear": "2022",
    "applicationCategory": "Educational & Scientific Utilities"
  },
  "desktopMobileBackground": "Calculating area and perimeter across irregular 2D geometric shapes often leads to manual formula errors, improper input handling, and sluggish interfaces. Calgeo was developed as a reliable offline mobile utility that streamlines mathematical operations through dynamic layout rendering and automated geometric constraint validation.",
  "desktopMobileProblemStatements": [
    {
      "title": "Manual Calculation Inaccuracies",
      "description": "Manual computation of two-dimensional geometry areas and perimeters is prone to arithmetic slips and formula misapplication across complex polygons like trapezoids and kites.",
      "issueCode": "ISSUE_01"
    },
    {
      "title": "Invalid Geometric Dimension Configurations",
      "description": "Traditional calculators permit impossible geometric inputs, such as negative dimensions or side lengths violating the triangle inequality theorem.",
      "issueCode": "ISSUE_02"
    },
    {
      "title": "Cluttered and Static User Interfaces",
      "description": "Existing scientific calculators present cumbersome static button layouts and obscure mathematical inputs instead of adaptive, shape-focused input fields.",
      "issueCode": "ISSUE_03"
    }
  ],
  "desktopMobileObjectives": [
    {
      "title": "Automate 2D Geometric Computations",
      "description": "Provide instantaneous area and perimeter calculation engines for 8 primary 2D shapes with high floating-point precision.",
      "targetTag": "TARGET_01"
    },
    {
      "title": "Enforce Rigorous Input Validation",
      "description": "Prevent invalid states through real-time numeric checks, positive-value verification, and mathematical inequality rules before executing calculations.",
      "targetTag": "TARGET_02"
    },
    {
      "title": "Dynamic Responsive Presentation",
      "description": "Dynamically generate input text containers matched to each shape's required dimensions while ensuring edge-to-edge UI compliance on all Android viewports.",
      "targetTag": "TARGET_03"
    }
  ],
  "desktopMobileFeatures": [
    {
      "title": "Comprehensive 2D Shape Suite",
      "description": "Supports 8 geometric entities: Square, Rectangle, Triangle, Circle, Parallelogram, Trapezoid, Rhombus, and Kite with specialized formulas.",
      "badge": "Geometry Engine",
      "metric": "8 Supported Shapes"
    },
    {
      "title": "Dynamic Input Form Generation",
      "description": "Automatically inflates tailored input fields per shape with dedicated hint texts and floating labels using Android ViewBinding.",
      "badge": "Dynamic UI",
      "metric": "Instant Field Binding"
    },
    {
      "title": "Strict Geometric Boundary Validation",
      "description": "Validates positive finite inputs and evaluates triangle inequality constraints to guarantee mathematical validity.",
      "badge": "Validation Core",
      "metric": "100% Geometry Guard"
    },
    {
      "title": "Edge-to-Edge System Bar Adaptation",
      "description": "Leverages WindowInsetsCompat to gracefully handle status bars, navigation gestures, and display cutouts without clipping content.",
      "badge": "Modern UI/UX",
      "metric": "Full Inset Ingress"
    }
  ],
  "desktopMobileInterfaceShowcase": [
    {
      "imageUrl": "/images/projects/calgeo_2d_geometry_calculator/image01.webp",
      "caption": "Interactive shape calculation view featuring dynamic input fields, real-time constraint validation, and formatted geometric result cards.",
      "badge": "Calculator Workspace"
    }
  ],
  "desktopMobileUserFlow": {
    "summary": "The user selects a 2D shape from the home grid, triggering the dynamic calculator screen. Upon entering dimensions, the app executes instant type-safe input checks, applies geometric inequality validations, computes real-time area and perimeter metrics, and displays clean formatted results with quick reset capabilities.",
    "steps": [
      {
        "step": "01",
        "title": "Shape Catalog Selection",
        "description": "User explores the two-column grid on HomeFragment and taps one of the eight geometric shape cards.",
        "actorOrNode": "User & RecyclerView"
      },
      {
        "step": "02",
        "title": "Dynamic Calculator Navigation",
        "description": "NavHostFragment transitions to CalculatorFragment, passing the ShapeType argument via safe bundle arguments.",
        "actorOrNode": "Navigation Component"
      },
      {
        "step": "03",
        "title": "Input Inflation & Dimension Entry",
        "description": "The screen dynamically instantiates required dimension fields from ShapeRepository, and user inputs measurement values.",
        "actorOrNode": "ViewBinding & User"
      },
      {
        "step": "04",
        "title": "Validation & Calculation",
        "description": "User taps Calculate; InputValidator confirms positive numbers and triangle constraints before GeometryCalculator computes area and perimeter.",
        "actorOrNode": "Validation & Computation Engine"
      },
      {
        "step": "05",
        "title": "Result Presentation & Reset",
        "description": "Calculated area and perimeter or circumference are formatted with unit suffixes and displayed, with one-tap reset capability.",
        "actorOrNode": "UI Presentation Layer"
      }
    ]
  },
  "desktopMobileArchitecture": {
    "summary": "Calgeo follows Android Jetpack architectural principles with single-activity navigation, ViewBinding presentation, and complete decoupling of calculation engines. GeometryCalculator and InputValidator isolate pure mathematical formulas from UI lifecycles, ensuring modularity, edge-to-edge rendering, and zero runtime dependencies.",
    "layers": [
      {
        "name": "Presentation Layer",
        "role": "Manages Fragment lifecycles, edge-to-edge system insets, and user interactions.",
        "tech": "Android Jetpack ViewBinding",
        "components": [
          "MainActivity",
          "HomeFragment",
          "CalculatorFragment",
          "AboutFragment",
          "ShapeAdapter"
        ]
      },
      {
        "name": "Navigation Layer",
        "role": "Orchestrates seamless screen transitions and safe argument passing between fragments.",
        "tech": "Navigation Component",
        "components": [
          "NavHostFragment",
          "nav_graph.xml"
        ]
      },
      {
        "name": "Domain & Calculation Layer",
        "role": "Executes pure geometric mathematical formulas and enforces geometric validity rules.",
        "tech": "Java Utilities",
        "components": [
          "GeometryCalculator",
          "InputValidator",
          "ShapeRepository",
          "CalculationResult",
          "Shape",
          "InputField"
        ]
      }
    ]
  },
  "desktopMobileDataManagement": {
    "storageType": "In-Memory Data Repository",
    "stateEngine": "Android ViewBinding State Management",
    "offlineSyncStrategy": "Fully Offline Standalone Architecture",
    "cachingMechanism": "In-Memory Shape Definition Cache"
  },
  "desktopMobilePlatformImplementation": [
    {
      "title": "Edge-to-Edge Display Cutout Inset Management",
      "description": "Implements WindowCompat and ViewCompat.setOnApplyWindowInsetsListener in MainActivity to apply dynamic padding for status bars, navigation bars, and display cutouts.",
      "badge": "System UI Integration"
    },
    {
      "title": "Single-Activity Navigation Graph Architecture",
      "description": "Utilizes Android Jetpack Navigation Component with NavHostFragment to manage smooth fragment transitions and type-safe argument passing.",
      "badge": "App Architecture"
    },
    {
      "title": "Dynamic View Inflation with Material ViewBinding",
      "description": "Dynamically inflates custom ItemInputFieldBinding components programmatically based on the active shape definition, maintaining high memory efficiency.",
      "badge": "UI Rendering"
    }
  ],
  "desktopMobileTechSpecs": {
    "programmingLanguage": "Java",
    "framework": "Android SDK",
    "localStorage": "In-Memory Data Repository"
  },
  "desktopMobilePlatformSpecs": {
    "targetPlatform": "Android 8.0 and Higher",
    "packageFormat": "Android Application Package APK",
    "targetArchitecture": "Universal Device Architecture",
    "buildFootprint": "Ultra Lightweight Client Utility"
  }
}
```
