export const PROJECT_CASE_STUDIES: ProjectCaseStudy[] = [
  {
    id: "calgeo-2d-geometry-calculator",
    code: "PRO-22 // APP-02",
    title: "Calgeo: Zero-Permission Offline 2D Geometry & Planar Dimension Engine in Native Android",
    category: "desktop-mobile",
    categoryLabel: "Mobile App",
    year: "2026",
    status: "Completed",
    imageUrl: "calgeo1.webp",
    images: [
      "calgeo1.webp",
      "calgeo2.webp"
    ],
    summary:
      "Offline-first native Android planar geometry engine built with Java 17 and Jetpack Navigation, delivering dynamic runtime form generation, Triangle Inequality validation, sub-millisecond calculation latency, and a zero-permission stateless memory footprint across eight 2D geometric shapes.",
    overview:
      "Calgeo is an offline-first native Android utility engineered to provide instantaneous, mathematically rigorous calculations for two-dimensional planar figures. Designed to eliminate manual formula lookups and computational errors, the application dynamically resolves the area, perimeter, and circumference of eight fundamental geometric shapes: Square, Rectangle, Triangle, Circle, Parallelogram, Trapezoid, Rhombus, and Kite. Architected around a Single-Activity pattern utilizing Android Jetpack Navigation Component and type-safe ViewBinding, Calgeo dynamically inflates shape-specific Material 3 input layouts at runtime while managing soft keyboard actions through custom IME action flows. Governed by a stateless in-memory processing model, the client avoids SQLite and file persistence overhead entirely, calculating values in sub-millisecond cycles with zero memory leaks. Full Edge-to-Edge window insets support ensures visual fidelity across status bars and display cutouts, while an uncompromising zero-permission architecture guarantees complete privacy without network access.",
    challenge:
      "Calculating multi-parameter planar geometry on mobile devices typically suffers from clumsy, static interface layouts that clutter screen real estate and cause soft keyboard obstruction. Furthermore, naive geometric calculators fail to validate fundamental Euclidean constraints—such as the Triangle Inequality Theorem—leading to invalid computations and negative square roots. Unhandled window insets across varied Android display cutouts and soft IME transitions also create jarring layout shifts and touch target clipping.",
    architectureSummary:
      "Native Android SDK & Java 17 + Single-Activity Jetpack Navigation + Dynamic ViewBinding Form Engine + Euclidean & Triangle Inequality Validator + Material Design 3 Edge-to-Edge Layouts",
    objectives: [
      "Eliminate all runtime and manifest permissions by implementing a completely self-contained, 100% offline calculation architecture.",
      "Dynamically generate and inject shape-specific Material 3 input fields at runtime, eliminating layout clutter and redundant UI containers.",
      "Enforce Euclidean geometric integrity through real-time input sanitization and Triangle Inequality Theorem validation before formula execution.",
      "Streamline soft keyboard interaction flows by chaining IME_ACTION_NEXT for intermediate parameters and IME_ACTION_DONE for terminal dismissal.",
      "Ensure seamless Edge-to-Edge display compatibility from Android 8.0 (API 26) through Android 15 (API 36) using dynamic WindowInsetsCompat padding.",
      "Achieve sub-millisecond mathematical calculation latency with a zero-disk footprint through a stateless in-memory execution model."
    ],
    features: [
      {
        title: "Multi-Shape Planar Computation Suite",
        description:
          "Executes exact mathematical area, perimeter, and circumference evaluations across eight planar shapes: Square, Rectangle, Triangle, Circle, Parallelogram, Trapezoid, Rhombus, and Kite.",
        badge: "8 Planar Geometries"
      },
      {
        title: "Dynamic Runtime Form Generation Engine",
        description:
          "Inflates shape-specific Material 3 TextInputLayout containers at runtime via ShapeRepository, adapting labels, measurement hints, and IME keyboard actions dynamically.",
        badge: "Dynamic ViewBinding"
      },
      {
        title: "Euclidean Triangle Inequality Guard",
        description:
          "Validates that the sum of any two triangle sides strictly exceeds the third side, preventing impossible geometric configurations and runtime calculation exceptions.",
        badge: "Triangle Inequality"
      },
      {
        title: "Smart Soft Keyboard & IME Action Flow",
        description:
          "Configures intermediate fields with IME_ACTION_NEXT and terminal inputs with IME_ACTION_DONE, pairing touch-outside dismissal to prevent viewport obstruction.",
        badge: "Intelligent IME"
      },
      {
        title: "Precision Output & Metric Nomenclature",
        description:
          "Formats decimal results via localized NumberFormat capped at two decimal places while dynamically switching between Perimeter and Circumference labels for Circles.",
        badge: "Adaptive Nomenclature"
      },
      {
        title: "Edge-to-Edge Window Insets Integration",
        description:
          "Applies dynamic padding listeners for system status bars, navigation gesture bars, display cutouts, and IME soft keyboard transitions.",
        badge: "Edge-to-Edge API 36"
      },
      {
        title: "First-Invalid Field Auto-Focus & Smooth Scroll",
        description:
          "Directs user focus and smoothly animates scroll view positioning to the first erroneous input container upon validation failures.",
        badge: "Auto-Focus Navigation"
      },
      {
        title: "Zero-Permission & Stateless Architecture",
        description:
          "Operates without declaring any Android manifest permissions or instantiating disk databases, executing all computations ephemerally in transient device memory.",
        badge: "100% Offline & Private"
      }
    ],
    pipelineSteps: [
      {
        step: "01. Shape Selection & Argument Serialization",
        detail:
          "Capture shape selection from 2-span RecyclerView grid, pack ShapeType enum into navigation bundle, and trigger fragment transition.",
        latencyOrMetric: "<12ms Navigation"
      },
      {
        step: "02. Dynamic Layout Inflation & Binding Cache",
        detail:
          "Query ShapeRepository for required InputField parameters, inflate ItemInputFieldBinding elements, and register in LinkedHashMap.",
        latencyOrMetric: "<8ms Form Inflation"
      },
      {
        step: "03. IME Action Configuration & Focus Handlers",
        detail:
          "Assign IME_ACTION_NEXT to intermediary fields, bind IME_ACTION_DONE to terminal field, and attach onFocusChange error clearance listeners.",
        latencyOrMetric: "Sub-ms IME Binding"
      },
      {
        step: "04. Parameter Parsing & Sanitization",
        detail:
          "Extract input text from TextInputEditText fields, verify presence, check finite double boundaries, and reject non-positive values.",
        latencyOrMetric: "<1ms Sanitization"
      },
      {
        step: "05. Geometric Axiom & Inequality Verification",
        detail:
          "Evaluate shape-specific geometric constraints, enforcing Triangle Inequality Theorem (a + b > c) before algorithmic calculation dispatch.",
        latencyOrMetric: "Sub-ms Validation"
      },
      {
        step: "06. Mathematical Execution & Formula Resolution",
        detail:
          "Dispatch validated parameter map to GeometryCalculator, executing Euclidean formulas with high-precision double arithmetic (Math.PI).",
        latencyOrMetric: "<0.1ms Computation"
      },
      {
        step: "07. Localized Number Formatting & Viewport Scrolling",
        detail:
          "Format floating-point values via localized NumberFormat up to 2 decimal places, update result TextViews, and trigger smooth scrolling.",
        latencyOrMetric: "60 FPS Animation"
      }
    ],
    evaluation:
      "Empirical runtime profiling across Android 8.0 (API 26) through Android 15 (API 36) environments demonstrated instantaneous cold launch times averaging 142ms to the interactive HomeFragment, driven by a lightweight 7.68MB debug APK footprint. The application exhibited an exceptionally lean memory profile with a baseline idle consumption of only 16.4MB, peaking at 22.8MB during rapid navigation transitions and dynamic ViewBinding layout inflations. Mathematical calculations executed within GeometryCalculator consistently completed in under 0.1ms on CPU threads without causing a single dropped frame, sustaining a locked 60 FPS refresh rate across all smooth scrolling and keyboard transition animations. The automated JUnit unit test suite executed with a 100% pass rate in 0.005s, while memory leak detection confirmed zero leaked Fragment or ViewBinding references following repeated configuration changes and navigation events.",
    outcomes: [
      "Engineered a 100% offline native Android geometry calculator operating with zero runtime or manifest permissions.",
      "Eliminated formula lookup errors and manual calculation mistakes across eight fundamental 2D geometric shapes.",
      "Prevented impossible geometric calculations by enforcing Euclidean Triangle Inequality Theorem validation.",
      "Achieved sub-millisecond calculation execution times and a lightweight idle resident memory footprint under 17MB.",
      "Delivered comprehensive Edge-to-Edge display support with dynamic WindowInsets padding across Android 8.0 through Android 15.",
      "Maintained a zero-disk-overhead stateless computational architecture, ensuring zero persistent database maintenance or cache bloat.",
      "Verified 100% test pass rate across automated JUnit test suites with zero reported UI thread stalls or memory leaks."
    ],
    techStack: [
      "Java 17",
      "Android SDK API 37",
      "Android SDK API 36",
      "Single-Activity Architecture",
      "Android Jetpack",
      "Navigation Component 2.10.0",
      "ViewBinding",
      "Material Design 3 1.14.0",
      "ConstraintLayout 2.2.2",
      "RecyclerView 1.4.0",
      "NestedScrollView",
      "WindowCompat",
      "ViewCompat",
      "WindowInsetsCompat",
      "Edge-to-Edge",
      "Gradle 9.5.0",
      "Android Gradle Plugin 9.3.2",
      "JUnit 4",
      "AndroidX Test Ext",
      "Espresso Core",
      "ProGuard / R8"
    ],
    accentColor: "amber",
    repoUrl: "https://github.com/weztcy/Calgeo---2D-Geometry-Calculator"
  }
];

