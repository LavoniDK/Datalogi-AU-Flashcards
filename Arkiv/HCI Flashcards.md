[[Human-Computer Interaction]]

___

#flashcards/HCI/35-Intro  
## Week 35: Intro (A)

- **What is HCI about and why does it matter?** :: Human-Computer Interaction (HCI) is the study and practice of designing, evaluating, and improving the interaction between humans and computers. It matters because well-designed interfaces enhance user satisfaction, efficiency, and safety, which is crucial in diverse fields from software applications to complex control systems.
<!--SR:!2025-02-09,20,264-->

- **What are the essential activities of HCI and how are they applied in practice?** :: The essential activities of HCI include understanding users, designing interfaces, prototyping, and evaluating systems. In practice, these activities are applied through iterative design processes, user-centered design methodologies, and usability testing to refine interfaces.
<!--SR:!2025-02-15,25,264-->

## Week 35: HTML and CSS (B)

- **What are HTML and CSS, and how is the latter integrated into the former?** :: HTML (HyperText Markup Language) structures content on the web, while CSS (Cascading Style Sheets) styles it. CSS is integrated into HTML using `<style>` tags, inline `style` attributes, or external stylesheets linked via `<link>` elements.
<!--SR:!2025-03-10,44,304-->

- **What are anchor tags in HTML used for?** :: Anchor tags (`<a>`) are used to create hyperlinks that link to other webpages or resources.
<!--SR:!2025-02-02,11,271-->

- **What is the difference between an inline and block tag?** :: Inline tags do not break the flow of content and only take up as much width as needed (e.g., `<span>`, `<a>`). Block tags start on a new line and take up the full width of their container (e.g., `<div>`, `<p>`).
<!--SR:!2025-02-14,27,284-->

- **What are the different types of selectors and how do they differ?**
?
Types of CSS selectors include:
  - **Universal (`*`)**: Selects all elements.
  - **Type (`div`)**: Selects elements by tag name.
  - **Class (`.className`)**: Selects elements by class.
  - **ID (`#idName`)**: Selects a single element by ID.
  - **Attribute (`[attr=value]`)**: Selects elements with specific attributes.
  They differ in specificity and use cases.
<!--SR:!2025-02-06,19,264-->

- **How do rules in CSS cascade?**
?
CSS rules cascade based on:
  1. **Importance** (`!important` overrides all).
  2. **Specificity** (ID > class > type selectors).
  3. **Source order** (later rules override earlier ones if they have the same specificity).
<!--SR:!2025-02-05,18,264-->

- **Explain the box model of CSS**
?
  The CSS box model represents elements as rectangular boxes consisting of:
  - **Content**: The actual content of the element.
  - **Padding**: Clears space around the content.
  - **Border**: Surrounds the padding.
  - **Margin**: Clears space outside the border.
<!--SR:!2025-02-09,22,264-->

- **What is specificity?**
?
Specificity in CSS determines which rules are applied when multiple rules target the same element. It is calculated based on the types of selectors used in the rule. The hierarchy is:
  1. Inline styles (`style="..."`) – highest specificity.
  2. ID selectors (`#id`).
  3. Class, attribute, and pseudo-class selectors (`.class`, `[attr=value]`, `:hover`).
  4. Type selectors (`div`, `p`) and pseudo-elements (`::before`).
If two rules have the same specificity, the one defined later in the stylesheet is applied.
<!--SR:!2025-02-13,26,284-->


____

#flashcards/HCI/36  
## Week 36: UI Devices (A)

- **What is a _transfer function_?** :: A transfer function in HCI defines the relationship between a user’s input and the resulting output on the display. It characterizes how input from a device (e.g., a mouse or joystick) is translated into changes on the screen, affecting precision and responsiveness.
<!--SR:!2025-02-14,27,286-->

- **Explain the classification of input devices**
?
  Input devices are classified based on the type of interaction they support:
  1. **Direct vs. Indirect devices**: Direct devices (e.g., touchscreens) operate directly on the display, while indirect devices (e.g., mouse, trackpad) require a mapping to the display.
  2. **Discrete vs. Continuous devices**: Discrete devices (e.g., keyboard) generate individual events, while continuous devices (e.g., joystick) provide ongoing input.
  3. **Isotonic, Isometric, Elastic devices**: Isotonic devices (e.g., mouse) allow free movement, isometric devices (e.g., force-sensitive joystick) measure force without displacement, and elastic devices provide resistance to input.
<!--SR:!2025-02-07,20,266-->

- **What is the difference between absolute and relative pointing devices?**
?
**Absolute pointing devices** are input devices that provide direct and fixed positional input relative to a reference frame, typically a display screen. Unlike **relative pointing devices** (e.g., mice or trackballs), which detect motion changes to move a cursor, absolute pointing devices map the device’s position directly to a corresponding point on the screen.
<!--SR:!2025-02-08,18,267-->

- **What is _control-display gain_? and name the most common types**
?
Control-display (C-D) gain refers to the ratio between the physical movement of the input device and the resulting movement on the display. Common types are:
  1. **Low gain**: High precision but requires large movements.
  2. **High gain**: Covers large distances quickly but may reduce precision.
  3. **Adaptive gain**: Dynamically adjusts based on speed or context.
<!--SR:!2025-02-16,25,266-->

- **What are _degrees of freedom_?** :: Degrees of freedom (DOF) refer to the number of independent movements an input device can detect. For example, a mouse has 2 DOF (x, y axes), while a 3D controller may have up to 6 DOF (x, y, z axes + pitch, yaw, roll).
<!--SR:!2025-02-03,16,246-->

- **What is _controller resistance_** :: Controller resistance describes how much force is required to operate an input device. Types of resistance include static resistance (initial force required to move) and dynamic resistance (force during movement).
<!--SR:!2025-02-06,19,268-->

- **What is _order of control_?**
?
Order of control refers to how an input affects the display over time:
  1. **Zero-order**: Position control – directly maps input position to output (e.g., mouse).
  2. **First-order**: Rate control – input changes output speed (e.g., joystick).
  3. **Second-order**: Acceleration control – input changes output acceleration.
<!--SR:!2025-02-19,25,226-->

- **What is the *design space* of input devices?** :: The design space of input devices refers to the range of possible input methods based on factors like degrees of freedom, control type, resistance, and feedback. It helps in systematically exploring device options for different tasks.
<!--SR:!2025-03-07,41,288-->

- **What different types of displays are there?** ? Types of displays include:  
  1. **Visual displays**: Standard monitors, projectors, augmented reality.  
  2. **Audio displays**: Speakers, headphones for auditory feedback.  
  3. **Haptic displays**: Devices providing tactile feedback (e.g., vibration motors).  
  4. **Emerging forms**: Mixed reality and holographic displays.

- **What is clutching in HCI?** :: The action of adjusting or repositioning a pointing device to maintain control during interaction. E.g. lifting and centering a mouse when you run out of space on the surface you are operating the mouse on.
<!--SR:!2025-01-31,11,286-->

## Week 36: JavaScript (B)

- **What are the key characteristics of JavaScript?** :: JavaScript is a high-level, dynamically typed, prototype-based language used for web development. Key characteristics include event-driven programming, first-class functions, asynchronous capabilities (via callbacks, promises, and async/await), and platform independence.
<!--SR:!2025-02-07,20,266-->

- **How does scoping work in JavaScript?**
?
JavaScript uses **lexical scoping**, meaning the scope of a variable is determined by its position in the code. There are three types of scope:
  1. **Global scope**: Variables declared outside any function are globally accessible.
  2. **Function scope**: Variables declared inside a function are accessible only within that function (`var`).
  3. **Block scope**: Variables declared with `let` and `const` are scoped to the nearest enclosing block (`{}`).
<!--SR:!2025-02-08,21,268-->

- **What is the third argument in `addEventListener`?** :: The third argument specifies whether the event should be captured during the capture phase (`true`) or the bubble phase (`false`). The default value is `false`, meaning the event listener operates in the bubble phase by default.
<!--SR:!2025-02-10,16,293-->


___

#flashcards/HCI/37  
## Week 37: GUIs (A)

- **What does _translational distance_ mean?** :: Translational distance refers to the physical or perceived distance that a user must move an input device or a cursor to perform a task on the graphical user interface.
<!--SR:!2025-02-14,26,270-->

- **What is _direct manipulation_ and what trade-offs does it have?** :: Direct manipulation refers to an interaction style where users engage with digital objects in a way that mimics interacting with physical objects. Instead of relying on abstract commands or syntax, users directly manipulate on-screen elements through actions like clicking, dragging, or resizing. This approach makes the interaction more intuitive, responsive, and user-friendly, at the cost of increased system complexity and resource consumption.
<!--SR:!2025-02-12,25,284-->

- **What are the types of direct manipulation in user interfaces?**
?
Direct manipulation refers to interacting with digital objects as if they were physical. The types include:
- **Weak Direct Manipulation**: Simple interactions with immediate feedback, such as dragging and dropping files.
- **Strong Direct Manipulation**: Advanced feedback and control, providing a higher degree of user involvement, like resizing an image with live previews.
- **Immersive Direct Manipulation**: Fully integrates the user into the environment, such as interacting with 3D objects in virtual reality (VR) systems.
<!--SR:!2025-02-19,20,251-->

- **What are _interaction tasks_?** :: Interaction tasks are fundamental operations users perform when interacting with a system, such as selecting, pointing, dragging, and typing.
<!--SR:!2025-02-10,21,264-->

- **What are _interaction techniques_?** :: Interaction techniques are methods or tools that enable users to accomplish interaction tasks, such as mouse-based point-and-click, multi-touch gestures, or voice commands.
<!--SR:!2025-02-12,25,284-->

- **How do interaction task and interaction techniques differ?** :: Interaction tasks describe *what* the user needs to do, while interaction techniques describe *how* the system supports accomplishing those tasks.
<!--SR:!2025-03-04,41,304-->

- **What’s the considerations when designing interaction techniques?** :: Key considerations include usability, learnability, efficiency, error prevention, and compatibility with the user’s physical and cognitive capabilities.
<!--SR:!2025-02-03,12,244-->

- **What’s the considerations when evaluating interaction techniques?** :: Evaluation considerations include task performance (speed and accuracy), user satisfaction, error rates, and the cognitive load imposed by the technique.
<!--SR:!2025-03-05,35,264-->

- **What is integration in UIs?** :: Combining different systems or components into a unified interface.
<!--SR:!2025-02-08,17,267-->

- **What is customization in UIs?** :: Allowing users to modify the interface to better suit their preferences or needs.
<!--SR:!2025-02-09,18,267-->

- **What is extension in UIs?** :: Adding new functionality to an existing system without altering the core components.
<!--SR:!2025-02-07,16,267-->

- **What is scalability in UIs?** ::The ability of the user interface to handle increasing amounts of work or users without performance degradation.
<!--SR:!2025-03-19,48,307-->

- **What is adaptability in UIs?** ::The capability of a user interface to adjust itself based on user behavior or environmental changes.
<!--SR:!2025-02-03,12,247-->

## Week 37: DOM and Events (B)

- **What is the DOM and how is it structured?** :: The DOM (Document Object Model) is a tree-like representation of an HTML document, where each node corresponds to an element, attribute, or piece of text. The root of the tree is the `<html>` element, with branches for child elements.
<!--SR:!2025-02-13,26,284-->

- **What is the _event flow_?**
?
Event flow describes the order in which events are processed in the DOM. It consists of three phases:
  1. **Capturing phase**: Events are captured from the root down to the target.
  2. **Target phase**: The event reaches the target element.
  3. **Bubbling phase**: The event bubbles back up to the root.
<!--SR:!2025-02-14,27,284-->

- **What is the _event object_?** :: The event object contains information about the event that occurred, such as the type of event, the target element, and any additional properties (e.g., mouse position, key pressed).
<!--SR:!2025-02-13,26,284-->

- **How can we change the event flow (preventing default behaviour and stopping propagation)?**
?
  - **Prevent default behavior**: Use `event.preventDefault()` to stop the browser's default action (e.g., preventing a form from submitting).
  - **Stop propagation**: Use `event.stopPropagation()` to prevent the event from propagating to parent elements.
<!--SR:!2025-02-08,21,264-->

- **What is event delegation and how can you implement it?** :: Event delegation is a technique where a parent element handles events for its child elements by using a single event listener. This works by exploiting event bubbling. To implement it, attach a listener to the parent and use `event.target` to determine the child element that triggered the event.
<!--SR:!2025-03-04,38,284-->

- **How do you use event listeners?** :: Event listeners are added using the `addEventListener` method, which takes the event type, a callback function, and an optional options object (e.g., `element.addEventListener('click', callback)`).
<!--SR:!2025-03-06,40,290-->

- **What types of events can you react to in the browser?**
?
You can react to various types of events, including:
  1. **Mouse events**: `click`, `dblclick`, `mousemove`, `mousedown`, `mouseup`.
  2. **Keyboard events**: `keydown`, `keypress`, `keyup`.
  3. **Form events**: `submit`, `input`, `change`, `focus`, `blur`.
  4. **Touch events**: `touchstart`, `touchmove`, `touchend`.
  5. **Window events**: `resize`, `scroll`, `load`, `unload`.
<!--SR:!2025-02-13,23,250-->


____

#flashcards/HCI/38  
## Week 38: Design Principles (A)

- **What is an _error_?** :: An error in HCI refers to any user action that does not achieve the intended goal or results in unintended consequences. Errors typically occur due to a mismatch between the user’s intentions and the system’s behavior.
<!--SR:!2025-02-24,34,279-->

- **What different types of _errors_ are there?**
?
Common types of errors include:
  1. **Slips**: When a user performs the wrong action but has the correct goal (e.g., pressing the wrong button).
  2. **Mistakes**: When a user has an incorrect goal or plan (e.g., misinterpreting how a feature works).
  3. **Lapses**: Failures due to memory errors (e.g., forgetting a step in a process).
  4. **Mode errors**: Occur when a user performs an action appropriate to one mode while in another mode.
<!--SR:!2025-02-08,20,239-->

- **What are guidelines, principles and theories in HCI, and how do they relate?**
?
  - **Guidelines**: Specific rules or recommendations for design (e.g., "use a consistent color scheme").
  - **Principles**: Broader design goals or best practices that guide decisions (e.g., "keep user control high").
  - **Theories**: Explanations or models that provide a foundation for understanding interaction (e.g., Fitts’ Law).
  Guidelines are often derived from principles, while theories provide the underlying rationale for both.
<!--SR:!2025-02-12,24,279-->

- **What are Shneiderman’s three high-level design principles?**
?
  1. **Prevent errors**: Design systems that prevent users from making errors.
  2. **Simplify recovery**: Make it easy for users to recover from errors.
  3. **Maintain consistency**: Ensure consistency across interactions to reduce cognitive load.
<!--SR:!2025-02-03,6,159-->

- **What types of theories are there?**
?
Types of theories in HCI include:
  1. **Descriptive theories**: Explain how users behave (e.g., GOMS model).
  2. **Prescriptive theories**: Provide guidance for how systems should be designed (e.g., usability heuristics).
  3. **Predictive theories**: Predict user performance based on specific parameters (e.g., Fitts’ Law).
<!--SR:!2025-02-10,20,259-->

- **What is the difference between micro- and macro theories?**
?
  - **Micro theories**: Focus on detailed aspects of user interaction, such as how users perform tasks (e.g., keystroke-level models).
  - **Macro theories**: Address broader contexts, such as how systems fit into social or organizational environments (e.g., Activity Theory).
<!--SR:!2025-03-15,45,259-->


____

#flashcards/HCI/39  
## Week 39: GUI Design (A)

- **What are mental models?** :: Mental models are internal representations users form about how a system works based on their past experiences, knowledge, and the system’s behavior. They influence how users interact with an interface.
<!--SR:!2025-03-03,40,299-->

- **What are metaphors?** :: Metaphors in GUI design are familiar concepts or images used to help users understand unfamiliar systems (e.g., the desktop metaphor for operating systems).
<!--SR:!2025-02-13,25,279-->

- **What are conceptual blends?** :: Conceptual blends combine elements from multiple mental spaces to create new meanings or experiences. In HCI, they help designers create innovative interfaces by blending existing concepts in new ways.
<!--SR:!2025-02-21,25,239-->

- **What are inspectors in web development?** :: Inspectors are developer tools in web browsers used to examine and modify the HTML, CSS, and JavaScript of a webpage in real-time.
<!--SR:!2025-02-10,16,291-->

- **What are the five visual design principles? (from NN/g)**
?
  1. **Scale**: Use size to emphasize important elements.
  2. **Visual hierarchy**: Arrange elements to show their relative importance.
  3. **Balance**: Distribute visual weight evenly across the design.
  4. **Contrast**: Make key elements stand out by using differing properties (e.g., color, size).
  5. **Alignment**: Ensure elements are visually connected through proper alignment.
<!--SR:!2025-02-20,22,199-->

## Week 39: Responsive Web (B)

- **What is responsive web design?** :: Responsive web design is an approach to web development where websites dynamically adjust their layout and content based on the screen size, resolution, and orientation of the user’s device.
<!--SR:!2025-03-13,47,299-->

- **What are the challenges involved in adapting a user-interface to different types of devices with different display sizes and input modalities?** :: Challenges include ensuring consistent usability across devices, maintaining visual appeal, optimizing performance, handling various input methods (touch, keyboard, mouse), and dealing with different network speeds.
<!--SR:!2025-02-10,21,259-->

- **How do you do media queries?**
?
Media queries are used in CSS to apply styles conditionally based on device characteristics such as width, height, and resolution. Example:
```css
  @media (max-width: 768px) {
    body {
      font-size: 14px;
    }
  }
```
<!--SR:!2025-02-27,33,279-->


- **What techniques are available in CSS to do fluid grids?**
?
- Multicol: We specify the width of each column, and the maximum number of rows, and the content will be organized according to this.
- Flexbox: For arranging items in rows or columns. Items _flex_ (expand) to fill additional space or shrink to fit into smaller spaces.
- CSS grid: Declarative way to organize content into a grid.
<!--SR:!2025-02-20,30,281-->

- **How do you implement fluid images**
?
Fluid images are implemented by setting their width to a percentage or using the `max-width` property to ensure they scale within their container:
```css
img {
  max-width: 100%;
  height: auto;
}
```
___
<!--SR:!2025-03-06,35,243-->

#flashcards/HCI/40  
## Week 40: Evaluations (A)

- **What is _key-stroke level analysis_?** :: Keystroke level analysis (KLM) is a predictive evaluation method in HCI that estimates the time it takes for a user to complete a task by modeling low-level actions such as keystrokes, mouse movements, and clicks.
<!--SR:!2025-02-16,20,240-->

- **What is a _think-aloud study_?** :: A think-aloud study involves users verbalizing their thoughts, actions, and decision-making processes as they perform tasks, helping researchers understand their cognitive processes and identify usability issues.
<!--SR:!2025-03-14,48,300-->

- **What are the levels of verbalization in think-aloud studies?**
?
The levels include:
- Concurrent verbalization: Describing thoughts in real-time while performing tasks.
- Retrospective verbalization: Reflecting on and describing thoughts after the task is complete.
- Hybrid verbalization: Combining elements of both concurrent and retrospective verbalization.
<!--SR:!2025-02-17,19,254-->

- **What is the observer effect?** :: The observer effect refers to changes in participant behavior due to being aware of being observed.
<!--SR:!2025-02-09,15,294-->

- **What is the egocentric fallacy?** :: The egocentric fallacy is the tendency to assume that others share one's own perspectives, beliefs, or experiences.
<!--SR:!2025-02-02,11,274-->


- **What is a _heuristic evaluation_?** :: A heuristic evaluation is an expert review of a system’s interface based on established usability principles or heuristics, identifying potential usability problems without involving real users.
<!--SR:!2025-02-11,24,279-->

- **What is a _cognitive walkthrough_?** :: A cognitive walkthrough is a usability evaluation method where evaluators simulate a user’s problem-solving process by stepping through tasks and questioning whether the system supports each step effectively.
<!--SR:!2025-02-17,28,280-->

- **What are evaluations in HCI and why are they done?** :: Evaluations in HCI assess the usability, functionality, and user experience of a system. They are done to ensure that the system meets user needs, reduces errors, and improves overall satisfaction and efficiency.
<!--SR:!2025-02-25,31,280-->

- **What is the difference between formative and summative evaluations?**
?
  - **Formative evaluations**: Conducted during the design process to identify and address issues early.
  - **Summative evaluations**: Conducted after development to assess the system’s overall effectiveness and performance.
<!--SR:!2025-02-03,13,240-->

- **What are the difference between quantitative and qualitative evaluations?**
?
  - **Quantitative evaluations**: Measure objective metrics (e.g., task completion time, error rates) and provide numerical data for statistical analysis.
  - **Qualitative evaluations**: Collect subjective feedback (e.g., user opinions, observations) and provide insights into user experiences and preferences.
<!--SR:!2025-02-05,18,260-->

- **What are the difference between analytical and empirical evaluations?**
?
  - **Analytical evaluations**: Performed by experts using theoretical models or heuristics without involving users (e.g., heuristic evaluations, GOMS).
  - **Empirical evaluations**: Involve real users performing tasks to collect data on usability and user experience (e.g., usability testing, field studies).
<!--SR:!2025-03-01,38,299-->

- **What is the difference between pilot studies and deployment studies?**
?
- **Pilot studies**: Small-scale tests to refine methods and tools.
- **Deployment studies**: Full-scale implementations in real-world contexts to validate findings.
<!--SR:!2025-02-02,11,274-->

- **What is the difference between confirmatory and exploratory research questions?**
?
- **Confirmatory questions**: Test specific hypotheses or predictions.
- **Exploratory questions**: Seek to uncover new patterns or insights without predefined expectations.
<!--SR:!2025-02-03,12,274-->

## Week 40: CSS Frameworks (B)

- **What are CSS frameworks and what are the pros and cons of using a CSS framework?**
?
  CSS frameworks are pre-built libraries that provide reusable classes, components, and grid systems to simplify web design.
  **Pros**:
  - Speeds up development.
  - Ensures consistency in design.
  - Provides cross-browser compatibility.
  - Includes responsive design features by default.
  **Cons**:
  - Adds extra overhead if only a few features are needed.
  - May result in less customized designs.
  - Requires learning the framework's syntax and structure.
<!--SR:!2025-02-07,19,260-->


____

#flashcards/HCI/41  
## Week 41: Evaluations 2 (A)

- **What’s an experiment in HCI and when is it used?** :: An experiment in HCI is a controlled study designed to test specific hypotheses about user interaction with a system. It is used when researchers want to establish causal relationships between variables and evaluate the effects of specific interface designs or interaction techniques.
<!--SR:!2025-02-25,28,244-->

- **Key concerns of experiments are validity and reliability. What are those and why those?**
?
  - **Validity**: Ensures that the experiment measures what it is intended to measure. High validity is essential to draw accurate conclusions.
  - **Reliability**: Refers to the consistency of results across repeated trials or different participants. Reliable experiments produce stable and reproducible outcomes.
<!--SR:!2025-02-22,32,280-->

- **What are the constituents of an experiment?**
?
The main constituents of an experiment include:
  1. **Hypothesis**: A testable prediction.
  2. **Variables**: Independent and dependent variables.
  3. **Participants**: The users involved in the experiment.
  4. **Procedure**: Detailed steps for conducting the experiment.
  5. **Metrics**: Measurements collected during the study.
<!--SR:!2025-02-06,19,262-->

- **What’s the role of the hypothesis and how is it formulated?** :: The hypothesis states the expected relationship between variables. It is formulated based on prior knowledge or theory and should be specific, measurable, and testable (e.g., "Increasing font size will reduce reading errors").
<!--SR:!2025-02-07,18,242-->

- **What’s independent and dependent variables?**
?
  - **Independent variable**: The factor manipulated by the experimenter (e.g., font size).
  - **Dependent variable**: The outcome measured to see the effect of the independent variable (e.g., error rate).
<!--SR:!2025-02-26,27,244-->

- **How are dependent variables selected?** :: Dependent variables are selected based on the goals of the experiment and the aspects of user interaction that need to be measured (e.g., task completion time, error rates, user satisfaction).
<!--SR:!2025-02-12,24,280-->

- **How are participants chosen?** :: Participants are chosen to represent the target user population. Selection methods include random sampling and stratified sampling to ensure diversity and reduce bias. 10-20 participants are usually chosen for HCI studies, although between-subject experiments require significantly more participants for getting solid results.
<!--SR:!2025-02-02,5,222-->

- **How are results from experiments analysed?** :: Results are analyzed using statistical methods to determine whether changes in the independent variable caused significant effects on the dependent variable. This includes descriptive statistics, hypothesis testing, and confidence intervals.
<!--SR:!2025-02-16,25,260-->

- **What is a field study and how is it different from an experiment?** :: A field study involves observing and collecting data in real-world settings without controlling variables, while an experiment is conducted in a controlled environment with manipulated variables to test specific hypotheses.
<!--SR:!2025-02-28,34,280-->

- **What is a within-subjects design?** :: An experimental design where the all participants are exposed to all conditions.
<!--SR:!2025-02-09,18,267-->

- **What is a between-subjects design?** :: An experimental design where different participants are assigned to different conditions.
<!--SR:!2025-02-08,17,267-->

## Week 41: JS for Desktop Apps (B)

- **How can JavaScript be used to develop desktop applications?** :: JavaScript can be used to develop desktop applications using frameworks like Electron, which allow developers to create cross-platform apps by combining web technologies (HTML, CSS, JS) in a chromium-based browser window, with Node.js for system-level functionality.
<!--SR:!2025-02-05,18,262-->

- **What is the difference between running JavaScript in the browser and with Electron?** :: In the browser, JavaScript runs in a sandboxed environment with limited access to system resources. In Electron, JavaScript runs alongside Node.js, enabling direct access to the file system, OS APIs, and other system-level features.
<!--SR:!2025-02-05,16,244-->

- **How is the interplay between Node.js and Electron in the creation of desktop apps with JavaScript?** :: Electron uses Chromium to render the front-end (HTML, CSS, JS) and Node.js to handle backend processes, enabling a seamless combination of UI and system-level functionality. The main process handles application-level operations, while renderer processes manage UI rendering and interactions.
<!--SR:!2025-02-02,15,242-->


____

#flashcards/HCI/43  
## Week 43: Understanding People (A)

- **What does it mean to be human-centered?** :: Being human-centered means designing systems and interfaces that prioritize user needs, capabilities, and limitations. It involves focusing on usability, accessibility, and user satisfaction throughout the design process.
<!--SR:!2025-02-28,34,283-->

- **What is perception and why is it relevant for HCI?** :: Perception is the process through which humans interpret sensory information. It is relevant for HCI because understanding how users perceive interfaces helps in designing intuitive and effective systems.
<!--SR:!2025-02-18,29,281-->

- **What does the human sensor system consist of?** :: The human sensor system includes vision, hearing, touch, smell, and taste. In HCI, vision, hearing, and touch are most relevant for interacting with digital interfaces.
<!--SR:!2025-03-02,39,303-->

- **How does the basics of the eye work?** :: The eye works by focusing light onto the retina, where photoreceptors (rods and cones) detect light and color. Signals are then transmitted to the brain via the optic nerve for interpretation.
<!--SR:!2025-02-01,10,241-->

- **What are the three central motor tasks?**
?
The three central motor tasks in HCI are:
  1. **Pointing**: Moving a cursor to a target.
  2. **Clicking**: Selecting an item.
  3. **Dragging**: Moving an object on the screen.
<!--SR:!2025-02-18,27,259-->

- **What is Fitts’ law and what can it be used for?** :: Fitts' law predicts the time required to move to a target based on its size and distance. It is used in HCI to design interfaces that minimize user effort by optimizing target placement and size.
<!--SR:!2025-03-09,43,301-->

- **What are the different reaction types?**
?
Reaction types include:
  1. **Simple reactions**: Responding to a single stimulus.
  2. **Choice reactions**: Choosing between multiple responses based on the stimulus.
  3. **Complex reactions**: Involving multiple stimuli and responses.
<!--SR:!2025-02-01,11,203-->

- **What does the Ratcliff model explain?** :: The Ratcliff model explains decision-making in tasks that require speed and accuracy. It models how information accumulates over time until a decision threshold is reached.
<!--SR:!2025-02-01,13,243-->

- **What does the Hick-Hyman law express?** :: The Hick-Hyman law states that the time it takes to make a decision increases logarithmically with the number of choices. It is relevant for interface design by emphasizing the need to reduce unnecessary options.
<!--SR:!2025-03-03,37,281-->

- **What are the elementary cognitive abilities?** :: Elementary cognitive abilities include perception, attention, memory, learning, and decision-making. These abilities govern how users interact with systems.
<!--SR:!2025-02-04,10,203-->

- **What is cognitive control?** :: Cognitive control refers to the ability to regulate attention, manage tasks, and inhibit distractions. It is crucial in complex or multi-step interactions.
<!--SR:!2025-02-15,19,220-->

- **How do we measure cognitive workload?** :: Cognitive workload can be measured using subjective methods (e.g., NASA-TLX), physiological measures (e.g., heart rate, eye-tracking), and performance-based metrics (e.g., error rates, task completion time).
<!--SR:!2025-02-20,23,241-->

- **What types of memory do we have and how do they differ?**
?
  1. **Sensory memory**: Short-term storage of sensory information.
  2. **Short-term memory (STM)**: Temporary storage for information in use.
  3. **Long-term memory (LTM)**: Permanent storage of knowledge and experiences.
<!--SR:!2025-02-11,24,279-->
  
- **What governs learning over time?** :: Learning is governed by repetition, feedback, and the gradual formation of mental models. Factors such as motivation and cognitive load also influence learning.
<!--SR:!2025-02-09,19,243-->

- **What’s the two systems of decision making?**
?
  1. **System 1**: Fast, automatic, and intuitive.
  2. **System 2**: Slow, deliberate, and analytical.
<!--SR:!2025-02-26,32,263-->

- **What’s a mental model?** :: A mental model is a user’s internal representation of how a system works, based on their experience and understanding.
<!--SR:!2025-02-12,25,283-->

- **How can insights about cognition be applied to HCI?** :: Insights about cognition help designers create interfaces that match users’ mental models, reduce cognitive load, and improve learnability and usability.
<!--SR:!2025-02-06,17,240-->

- **What does it means to view the human as an information processor?** :: Viewing humans as information processors means considering users as systems that receive input, process it, and produce output. This model helps in understanding user interaction and designing efficient interfaces.
<!--SR:!2025-02-15,27,283-->

- **What is the model human processor, what does it consist of and what can it be used for?**
?
The model human processor (MHP) is a framework that models human interaction as a series of perceptual, cognitive, and motor processes. It consists of three subsystems:
  1. **Perceptual system**: Processes sensory input.
  2. **Cognitive system**: Processes information and makes decisions.
  3. **Motor system**: Executes physical actions.
  MHP can be used to predict user performance and guide interface design.
<!--SR:!2025-02-11,21,241-->

- **What are the performance of our perceptual, cognitive and motor system according to MHP?**
?
  - **Perceptual system**: Processes inputs at a rate of about 100ms per cycle.
  - **Cognitive system**: Decision-making takes about 70ms per step.
  - **Motor system**: Reaction time for physical actions is approximately 70ms.
<!--SR:!2025-01-31,13,241-->

- **What is perceptual memory in MHP?** :: Perceptual memory acts as a buffer for sensor data, holding information briefly as it is processed.
<!--SR:!2025-02-03,7,274-->

- **What are the limitations of MHP?** :: MHP assumes a linear and sequential process, which may oversimplify real-world interactions. It also doesn’t account for emotional and social factors.
<!--SR:!2025-02-14,25,261-->

- **What is the recognize-act cycle in MHP?**
?
The recognize-act cycle involves:
- Recognition: A highly parallel process for interpreting stimuli.
- Act: A serial process for decision-making and response.
- **(extra): Uncertainty Principle**: Decision time increases with uncertainty about judgments, requiring more cognitive cycles. Cycle time shortens with practice or increased effort.
<!--SR:!2025-01-31,9,254-->

- **What is the motor system in MHP?** :: The motor system in MHP translates thought into physical actions, with cycle time diminishing with practice or task-specific effort.
<!--SR:!2025-02-05,11,274-->

- **How are needs and motivations relevant to HCI?** :: Needs and motivations influence user behavior, goal setting, and engagement. Designing systems that address users’ intrinsic and extrinsic motivations improves user satisfaction and long-term usage.
<!--SR:!2025-02-04,17,259-->

- **What is self-determination theory, its assumptions and basic ideas?** :: Self-determination theory (SDT) posits that humans have three basic psychological needs: autonomy, competence, and relatedness. Fulfillment of these needs leads to intrinsic motivation, which is key to sustained user engagement.
<!--SR:!2025-02-02,13,201-->

- **What is the perceptual task of detection?** :: The process of noticing the presence of a stimulus.
<!--SR:!2025-02-16,22,267-->

- **What is the perceptual task of discrimination?** :: The ability to distinguish between different stimuli.
<!--SR:!2025-01-31,10,227-->

- **What is the perceptual task of recognition?** :: Identifying a stimulus as something familiar.
<!--SR:!2025-02-03,12,247-->

- **What is the perceptual task of search?** :: The task of locating a particular stimulus among several.
<!--SR:!2025-02-08,17,267-->

- **What is the perceptual task of identification?** :: Determining the specific category or label of a stimulus.
<!--SR:!2025-02-10,16,247-->

## Additional Questions on Gestalt Principles (A)

- **What are Gestalt principles in HCI, and why are they important?** :: Gestalt principles are psychological theories explaining how humans naturally group visual elements based on patterns and relationships. They are important in HCI because they help designers create intuitive interfaces by aligning with users' natural perceptual tendencies.
<!--SR:!2025-02-06,19,261-->

- **How does the principle of proximity influence interface design?** :: The principle of proximity states that elements close to each other are perceived as related. In interface design, grouping related controls or information reduces cognitive load and improves user comprehension.
<!--SR:!2025-02-09,19,261-->

- **What is the principle of similarity, and how can it improve user experience?** :: The principle of similarity suggests that elements with similar characteristics (e.g., color, shape, size) are perceived as related. This principle helps users quickly identify and understand patterns, improving the consistency and clarity of an interface.
<!--SR:!2025-02-27,33,283-->

- **What is the principle of continuity, and how is it applied in GUIs?** :: The principle of continuity states that users prefer continuous, smooth paths and patterns. In GUIs, it can be applied by aligning elements along consistent lines or curves, guiding users' attention and making navigation easier.
<!--SR:!2025-01-31,12,241-->

- **What is the principle of figure-ground, and how can it enhance visual clarity?** :: The principle of figure-ground explains how people distinguish a foreground object from its background. Enhancing visual clarity involves ensuring sufficient contrast between key elements (figure) and the background, improving readability and focus.
<!--SR:!2025-02-15,24,259-->

- **What are common design mistakes that violate Gestalt principles?** :: Common mistakes include inconsistent grouping (violating proximity), using too many dissimilar styles (violating similarity), misaligned elements (violating continuity), poor contrast (violating figure-ground), and chaotic layouts that reduce visual clarity.
<!--SR:!2025-02-04,14,221-->

- **What role does the principle of common fate play in dynamic interfaces?** :: The principle of common fate states that elements moving together are perceived as related. In dynamic interfaces, it is used to group elements through synchronized animations, such as buttons that slide together or lists that expand uniformly.
<!--SR:!2025-03-11,45,303-->


___

#flashcards/HCI/44  
## Week 44: Activity Theory (A)

- **What is activity theory?** :: Activity theory is a conceptual framework that examines human activities as complex, socially situated processes, emphasizing the role of tools, goals, and social contexts in shaping human behavior.
<!--SR:!2025-02-25,28,239-->

- **Why was activity theory brought into HCI?** :: Activity theory was introduced into HCI to address limitations of early cognitive models by emphasizing real-world contexts, user goals, and tool-mediated interactions. It provides a holistic approach to understanding how technology fits into users' workflows and social environments
<!--SR:!2025-02-11,24,279-->

- **What does activity theory provide means to explain?** :: Activity theory provides a means to explain how tools mediate human action, how user activities evolve over time, and how social, cultural, and environmental factors influence interaction.
<!--SR:!2025-02-01,14,239-->

- **What are the fundamental principles of activity theory?**
?
  1. **Object-orientedness**: Activities are driven by goals or objects.
  2. **Mediation**: Actions are mediated by tools and artifacts.
  3. **Hierarchical structure**: Activities are organized into activities, actions, and operations.
  4. **Internalization and externalization**: Interaction involves transforming internal thought into external actions and vice versa.
  5. **Contradictions**: Development arises from resolving tensions or contradictions in activity systems.
<!--SR:!2025-02-02,5,182-->

- **How is the hierarchical structure of activity explained?**
?
Activities are structured in a hierarchy:
  1. **Activity**: A broad goal-oriented behavior (e.g., learning to use a program).
  2. **Action**: Specific, conscious steps taken to achieve the goal (e.g., opening a menu).
  3. **Operation**: Routine or automatic behaviors that support actions (e.g., clicking with a mouse).
<!--SR:!2025-02-14,27,282-->

- **What is the concept of mediation in activity theory?** :: Mediation refers to the use of tools (both physical and symbolic) in human activities. Tools shape how people interact with the world, and in turn, those interactions influence the evolution of the tools.
<!--SR:!2025-02-04,17,259-->

- **What are the principles of internalization and externalization in activity theory?**
?
  - **Internalization**: The process where external actions are transformed into internal cognitive processes (e.g., understanding how to use a tool by practicing).
  - **Externalization**: The process where internal thoughts are turned into external actions or expressions (e.g., applying learned knowledge in practice).
<!--SR:!2025-02-14,24,259-->

- **Why is development driven by contradictions according to activity theory?** :: Development is driven by contradictions—tensions or conflicts within an activity system. Resolving these contradictions leads to adaptation, learning, and the evolution of new practices or tools.
<!--SR:!2025-02-13,26,282-->

- **What is a contradiction in activity theory?** :: A contradiction is a conflict within an activity system, such as a mismatch between a user’s expectations and a system’s behavior. These conflicts prompt change and drive development by forcing users and systems to adapt.
<!--SR:!2025-02-24,28,259-->

## Additional Questions on Activity Theory (Week 44)


- **What role do tools play in activity theory?** :: In activity theory, tools mediate the relationship between the subject (user) and the object (goal). Tools can be physical (e.g., a hammer) or conceptual (e.g., language) and influence how activities are carried out. Over time, tools themselves evolve as a result of use.
<!--SR:!2025-02-07,20,259-->

- **What is the unit of analysis in activity theory?** :: The fundamental unit of analysis in activity theory is the **activity**, which includes the subject, the object, and the mediating tools. This holistic approach allows for understanding the context and purpose behind human actions.
<!--SR:!2025-03-02,39,299-->

- **How does activity theory address collaborative work?** :: Activity theory explains collaborative work by analyzing shared activities, where multiple subjects work toward a common object. The theory highlights the importance of communication, shared tools, and division of labor in achieving collective goals.
<!--SR:!2025-03-01,38,299-->

- **What is the difference between actions and operations in activity theory?**
?
  - **Actions**: Conscious, goal-directed behaviors performed to achieve a specific objective.
  - **Operations**: Routine, automatic behaviors that are performed without conscious thought, often as part of an action. Operations can become actions when users encounter new challenges requiring conscious effort.
<!--SR:!2025-02-23,33,279-->

- **What is the historical development principle in activity theory?** :: The historical development principle states that activities, tools, and social contexts evolve over time. Understanding current activities requires analyzing their historical development to see how they emerged and changed.
<!--SR:!2025-02-11,21,239-->

- **How is learning explained in activity theory?** :: Learning in activity theory is explained as a process of **internalization** and **externalization**. Individuals internalize knowledge through interaction with external tools and social practices, and they externalize their understanding by applying it in real-world tasks.
<!--SR:!2025-02-28,34,259-->

- **How does activity theory handle contradictions in design?** :: Activity theory views contradictions as drivers of development and change. In design, contradictions arise when user needs conflict with system capabilities. Identifying and resolving these contradictions helps improve the system and better align it with user goals.
<!--SR:!2025-03-12,46,299-->

- **What is the significance of community in activity theory?** :: Community refers to the group of people who share a common object and influence the subject’s activities. Community members provide social norms, expectations, and support, all of which affect how an activity is carried out.
<!--SR:!2025-03-08,39,259-->

- **What is the role of division of labor in activity theory?** :: Division of labor describes how tasks and responsibilities are distributed among participants in an activity. It highlights the interdependence of roles and the need for coordination in collaborative settings.
<!--SR:!2025-03-08,42,299-->

- **What are the key components of an activity according to Activity Theory?** :: The key components are Subject, Object, Tools, Rules, Community, and Division of Labor.
<!--SR:!2025-03-07,37,287-->

- **What is conceptualization in Activity Theory?** :: Conceptualization in Activity Theory involves understanding and framing tasks or activities in relation to their goals and the context in which they occur. It represents the mental process of defining and organizing the elements of an activity to achieve desired outcomes.
<!--SR:!2025-02-22,24,266-->

- **What is automatization in Activity Theory?** :: Automatization refers to the transition of actions from being consciously controlled to becoming automatic or habitual through practice and repetition.
<!--SR:!2025-02-22,26,286-->

- **How do we move up and down the hierarchical ladder of activities in Activity Theory?** :: Movement up the ladder involves breaking down automated actions into consciously controlled steps for reevaluation or learning. Movement down the ladder happens when conscious actions are practiced and refined into automated routines.
<!--SR:!2025-02-21,25,286-->

- **What is an instrument-producing activity?** :: An instrument-producing activity refers to creating tools or artifacts that mediate and enhance other activities.
<!--SR:!2025-02-10,16,293-->

- **What is a rule-producing activity?** :: A rule-producing activity involves the creation of norms, guidelines, or procedures that govern actions within a community or organization.
<!--SR:!2025-02-04,10,273-->

___

#flashcards/HCI/45  
## Week 45: Universal Usability (A)

- **What is universal usability?** :: Universal usability refers to the design of interfaces that can be effectively used by the widest possible range of people, regardless of their abilities, age, experience, or cultural background. The goal is to make technology accessible to everyone, including those with disabilities.
<!--SR:!2025-02-05,17,262-->

- **What broad categories of disabilities are there?**
?
Broad categories of disabilities include:
  1. **Visual impairments**: Blindness, low vision, color blindness.
  2. **Hearing impairments**: Deafness, partial hearing loss.
  3. **Motor impairments**: Reduced or limited mobility, tremors.
  4. **Cognitive impairments**: Learning disabilities, memory issues, difficulty with focus.
<!--SR:!2025-02-13,24,264-->

- **Why do we have to consider disabilities when designing user interfaces?** :: Designing for users with disabilities ensures inclusivity, improves usability for all users, and is often legally required. It helps avoid excluding a significant portion of the population and aligns with ethical principles of fairness and equal access.
<!--SR:!2025-02-13,26,282-->

- **What is internationalization and localization of software?**
?
  - **Internationalization**: The process of designing software so it can be adapted to different languages and regions without requiring changes to the codebase.
  - **Localization**: The process of adapting software for a specific language, culture, or region by translating text and adjusting formats (e.g., date, currency).
<!--SR:!2025-03-05,37,264-->

## Week 45: Usability (A)

- **How do you write accessible HTML?**
?
Writing accessible HTML involves:
  1. Using semantic elements (`<header>`, `<main>`, `<footer>`, etc.) for better structure.
  2. Providing alternative text (`alt` attributes) for images.
  3. Ensuring sufficient contrast between text and background.
  4. Using labels for form elements (`<label>` tags).
  5. Ensuring keyboard navigability by using logical tab orders and focus indicators.
<!--SR:!2025-02-07,18,244-->

- **What is WAI-ARIA and when is it used?** :: **WAI-ARIA is an accessibility standard** developed by the **W3C** to enhance web accessibility. It provides a framework for developers to ensure that web applications, especially complex and dynamic ones, are accessible to users with disabilities who rely on assistive technologies, such as screen readers.
<!--SR:!2025-02-12,23,259-->

- **How can internationalization be implemented on the Web (in broad strokes)?**
?
Internationalization on the web can be implemented by:
  1. Using Unicode for text encoding.
  2. Providing locale-specific formats for dates, numbers, and currencies.
  3. Storing content separately from its presentation to facilitate translation.
  4. Allowing users to select their preferred language and region.
  5. Designing layouts that accommodate text expansion in different languages.
<!--SR:!2025-02-26,29,244-->


___

#flashcards/HCI/46  
## Week 46: Data Visualization (A)

- **What is data visualization?** :: Data visualization is the graphical representation of information and data. It uses visual elements like charts, graphs, and maps to make complex data more accessible, understandable, and usable for analysis and decision-making.
<!--SR:!2025-03-09,43,301-->

- **What are examples of historical visualization techniques? (Minard, John Snow, Nightingale, etc.)**
?
  1. **Minard’s map**: Depicts Napoleon’s Russian campaign, showing the army’s size, direction, and temperature.
  2. **John Snow’s cholera map**: Used to identify the source of a cholera outbreak in London by plotting cases on a map.
  3. **Florence Nightingale’s diagrams**: Polar area diagrams used to show causes of mortality in the Crimean War, influencing public health reform.
<!--SR:!2025-02-14,25,261-->

- **What is the difference between illustration and photorealism in data visualization?** :: Illustration focuses on clarity and abstraction, highlighting key patterns or trends, while photorealism attempts to closely mimic real-world appearances. In data visualization, illustration is often preferred as it reduces cognitive load and emphasizes the underlying data without unnecessary details.
<!--SR:!2025-02-12,25,281-->

- **What are basic data types and corresponding visualizations (multidimensional, trees, graphs, time, etc)?**
?
  1. **Multidimensional data**: Represented using scatter plots, parallel coordinates, or heatmaps.
  2. **Hierarchical data (trees)**: Visualized using tree diagrams, dendrograms, or sunburst charts.
  3. **Relational data (graphs)**: Depicted using node-link diagrams or adjacency matrices.
  4. **Time-series data**: Represented with line charts, timelines, or area charts.
<!--SR:!2025-02-16,25,262-->

## Week 46: JavaScript Front-end Frameworks (B)

- **What is a JavaScript framework for front-end development?** :: A JavaScript framework for front-end development is a library that provides pre-built components and structures for building web applications. Examples include Vue.js, React, and Angular, which help manage user interfaces and application state efficiently.
<!--SR:!2025-02-19,30,281-->

- **Why would you use a JavaScript framework like Vue.js?** :: Vue.js simplifies front-end development by offering reactive data binding, component-based architecture, and built-in directives. It speeds up development, improves maintainability, and makes it easier to build interactive UIs.
<!--SR:!2025-03-01,31,241-->

____

#flashcards/HCI/47  
## Week 47: History of Interactive Computing (A)

- **What was the development of interactive computing motivated by?** :: The development of interactive computing was motivated by the need to make computers more accessible and useful for individuals. Early computing focused on batch processing, but users wanted real-time feedback, interactive problem-solving, and tools for creativity and collaboration.
<!--SR:!2025-02-12,25,281-->

- **How did interaction with early computers happen and how did it evolve?** :: Interaction with early computers happened through punch cards and command-line interfaces. Over time, it evolved to include graphical user interfaces (GUIs), direct manipulation (using a mouse), and touch-based interaction, making computers easier to use.
<!--SR:!2025-02-14,27,284-->

- **When were some of the ideas we now take for granted first presented (pointing, hypertext, collaborative editing, video communication)?**
?
  1. **Pointing devices**: Introduced by Douglas Engelbart in 1968 (mouse demonstration).
  2. **Hypertext**: Concept introduced by Vannevar Bush in 1945 (“Memex”), and later implemented by Ted Nelson and Engelbart.
  3. **Collaborative editing**: Demonstrated in Engelbart’s 1968 "Mother of All Demos".
  4. **Video communication**: Also part of Engelbart’s 1968 demonstration, envisioning future collaborative work environments.
<!--SR:!2025-02-18,22,244-->

- **Where was the personal computer invented, and what vision drove its development?** :: The personal computer was developed at Xerox PARC in the 1970s, driven by the vision of empowering individuals through personal, graphical, and interactive computing environments.
<!--SR:!2025-02-10,21,261-->

- **What is the WIMP paradigm and when was it introduced?** :: The WIMP paradigm (Windows, Icons, Menus, Pointer) refers to the standard graphical user interface model used in modern computing. It was introduced in the 1970s by Xerox PARC and popularized by the Apple Macintosh in 1984.
<!--SR:!2025-02-13,26,284-->

- **When was the Web invented and for what?** :: The Web was invented by Tim Berners-Lee in 1989 at CERN. It was created to facilitate information sharing among researchers via a system of interconnected hypertext documents.
<!--SR:!2025-02-06,16,224-->

- **What kind of phases can interaction with computers be characterized by?**
?
Interaction with computers can be characterized by the following phases:
  1. **Batch processing phase**: Users interacted indirectly via punched cards or printed output.
  2. **Command-line phase**: Real-time interaction through text-based commands.
  3. **Graphical user interface (GUI) phase**: Direct manipulation using windows, icons, and menus.
  4. **Web-based interaction phase**: Interaction over the internet via browsers and hyperlinked content.
  5. **Ubiquitous computing phase**: Interaction through multiple, embedded devices (smartphones, IoT).
  6. **Augmented and virtual reality phase**: Immersive interaction with virtual environments.
<!--SR:!2025-02-09,18,241-->

## Additional Questions on the History of Interactive Computing (Week 47)

- **What is Vannevar Bush’s vision in "As We May Think" and how did it influence modern computing?** :: In "As We May Think" (1945), Vannevar Bush envisioned a device called the **Memex**, which would allow users to store and retrieve information via associative links, resembling modern hypertext systems. His ideas influenced the development of interactive computing by inspiring concepts like hypertext, personal information systems, and knowledge management.
<!--SR:!2025-02-01,5,181-->

- **What were the key contributions of Alan Kay to personal computing?** :: Alan Kay played a crucial role in developing the concept of the **Dynabook**, an early vision of a personal portable computer designed for learning and creativity. He also contributed to the development of **object-oriented programming**, **graphical user interfaces**, and **Smalltalk**, a pioneering programming environment at Xerox PARC.
<!--SR:!2025-02-15,19,201-->

- **How did Myer’s article characterize the evolution of HCI technology?** :: Myer’s article outlines the evolution of HCI in stages, starting from **batch processing systems**, moving through **command-line interfaces**, and finally arriving at **graphical user interfaces (GUIs)**. He highlights key technological milestones and innovations that transformed user interaction, such as windows, icons, and pointing devices.
<!--SR:!2025-02-04,14,221-->

- **What innovations were introduced at Xerox PARC, and how did they shape modern computing?**
?
Xerox PARC introduced several groundbreaking innovations, including:
  1. The **mouse** as a pointing device.
  2. The **WIMP paradigm** (Windows, Icons, Menus, Pointer).
  3. **Ethernet** for local networking.
<!--SR:!2025-02-05,11,273-->

- **Which system is considered the earliest ancestor of modern graphical user interfaces?** :: Ivan Sutherland's Sketchpad is considered the earliest ancestor of modern graphical user interfaces.
<!--SR:!2025-01-31,3,254-->

___
<!--SR:!2025-01-20,7,241-->

#flashcards/HCI/48  
## Week 48: Canvas and WebGL (B)

- **What are the stroke, region, and pixel models for 2D graphics?**
?
  1. **Stroke model**: Represents shapes by their outlines, defined by paths and styled using stroke properties (e.g., color, width).
  2. **Region model**: Represents shapes by the areas they cover, which can be filled with colors or patterns.
  3. **Pixel model**: Represents graphics as individual pixels, where each pixel’s color is directly manipulated, commonly used for bitmap images and low-level rendering.
<!--SR:!2025-02-17,26,260-->

- **What is the canvas element and what is it used for?** :: The `<canvas>` element is an HTML element that provides a drawable region for dynamic, scriptable rendering of 2D and 3D graphics using JavaScript. It is commonly used for games, data visualizations, and custom graphic interfaces.
<!--SR:!2025-02-05,16,240-->

- **How can the canvas element be used for 3D graphics?** :: The `<canvas>` element can be used for 3D graphics by employing WebGL, a JavaScript API for rendering interactive 3D content. While `<canvas>` provides the drawable region, WebGL handles low-level 3D rendering by interfacing with the GPU to draw 3D shapes, apply textures, and handle lighting. Libraries like **Three.js** simplify WebGL usage by providing higher-level abstractions for common 3D operations.
<!--SR:!2025-02-11,21,240-->

___

#flashcards/HCI/Misc

## Additional Questions

- **What is usability, and how is it measured?**
?
Usability refers to how effectively, efficiently, and satisfactorily a user can interact with a system to achieve their goals. It is measured using:
  1. **Effectiveness**: Whether users can complete tasks correctly.
  2. **Efficiency**: How quickly users can complete tasks.
  3. **Satisfaction**: How enjoyable or comfortable the experience is for users.
  Methods like usability testing, surveys, and performance metrics are commonly used to measure these attributes.
<!--SR:!2025-02-08,17,239-->

- **What is user-centered design (UCD), and what are its key steps?**
?
UCD is an iterative design process that focuses on understanding user needs at every stage. The key steps include:
  1. **Understanding user requirements** through research.
  2. **Prototyping solutions** based on those requirements.
  3. **Evaluating prototypes** with users.
  4. **Refining the design** based on feedback.
<!--SR:!2025-02-23,27,259-->

- **How does activity theory differ from cognitive theories in HCI?** :: While cognitive theories focus on individual mental processes, activity theory emphasizes the social, cultural, and contextual factors that shape human interaction. Activity theory views actions as part of larger goal-directed activities mediated by tools, whereas cognitive theories often model isolated tasks.
<!--SR:!2025-02-06,18,259-->

- **What are pre-attentive attributes in data visualization, and why are they important?** :: Pre-attentive attributes are visual properties that the human brain processes quickly and automatically before conscious attention is required. Examples include color, shape, size, and orientation. They are important because they help users quickly identify patterns and key data points.
<!--SR:!2025-02-12,23,262-->


- **What is a mode error, and how can it be prevented in interaction design?**
?
A mode error occurs when a user performs an action appropriate to one mode while the system is in another mode (e.g., typing when Caps Lock is unintentionally on). Mode errors can be prevented by:
  1. Minimizing the number of modes.
  2. Providing clear feedback about the current mode.
  3. Allowing easy mode switching.
<!--SR:!2025-02-13,24,261-->

- **What is the role of iteration in the design process?** :: Iteration is crucial in the design process because it allows designers to continuously refine and improve a product based on user feedback and testing. This approach ensures that the final design meets user needs effectively.
<!--SR:!2025-03-02,39,302-->

- **How can the application of Gestalt principles enhance the learnability of an interface?** :: Gestalt principles help users quickly perceive relationships between elements by leveraging natural human tendencies for grouping and pattern recognition. This reduces the time required to learn and understand an interface.
<!--SR:!2025-02-15,24,259-->

- **What is the importance of accessibility in modern interface design?** :: Accessibility ensures that interfaces can be used by people with a wide range of abilities, improving inclusivity. It also enhances usability for all users and is often a legal requirement. Accessible design leads to better user experiences and broader adoption of products.
<!--SR:!2025-02-04,17,259-->

- **What are the key challenges in designing for multiple devices and platforms?** :: Key challenges include ensuring consistency across devices, optimizing for different screen sizes and input methods, maintaining performance, and providing a seamless user experience. Responsive design and progressive enhancement are common strategies for addressing these challenges.
<!--SR:!2025-03-18,47,264-->

- **Why is it important to balance usability and aesthetics in interface design?** :: While usability ensures that an interface is functional and easy to use, aesthetics contribute to user satisfaction and engagement. A well-designed interface balances both aspects, making the product not only efficient but also enjoyable to use.
<!--SR:!2025-03-03,40,301-->

