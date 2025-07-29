# Newton Second-Law Playground

A web-based interactive simulation playground built with HTML, CSS, and JavaScript, demonstrating Newton's Second Law ($F=ma$) through two classic physics scenarios: an Inclined Table with a hanging mass, and an Atwood Machine. The simulation allows users to adjust various parameters and visualize the resulting motion through animated graphics and real-time data plots.

https://atreyuartax.github.io/N2L-Pulley-Simulation/N2L_Table.html

## Features

* **Two Simulation Modes:**
    * **Inclined Table:** Simulate a cart on an inclined plane connected to a hanging mass via a pulley. Adjust table height, cart mass, hanging mass, friction, and table angle.
    * **Atwood Machine:** Simulate two masses connected by a string over a pulley. Adjust pulley height and the individual masses.
* **Customizable Gravity:** Choose from preset gravitational accelerations (Earth, Moon, Mars, Jupiter) or input a custom value.
* **Physics Modes:**
    * **Perfect Mode:** Ideal simulation without any random variations.
    * **Real Mode:** Introduces slight random variations to acceleration, mimicking real-world experimental inconsistencies.
* **Real-time Data Visualization:**
    * Interactive charts for Position vs. Time, Velocity vs. Time, and Acceleration vs. Time using Chart.js.
    * Live display of average acceleration, final velocity, net force, and simulation status.
* **Dynamic Canvas Resizing:** The simulation canvas adjusts its height based on the chosen parameters to ensure all elements are visible.
* **Responsive Design:** The layout adapts to different screen sizes for optimal viewing on various devices.

## How to Use

1.  **Open `N2L_Table.html` in your web browser.**
2.  **Select Simulation Type:** Choose between "Inclined Table" and "Atwood Machine" using the "Simulation" dropdown.
3.  **Adjust Parameters:** Use the sliders or number inputs in the "Controls" section to change values like masses, heights, friction, and angle (depending on the simulation type).
4.  **Set Gravity:** Select a preset gravity value or enter a custom one.
5.  **Choose Mode:** Toggle between "Perfect" and "Real" modes using the "Mode" button.
6.  **Start Simulation:** Click the "Start" button to begin the animation and data collection.
7.  **Stop/Reset Simulation:**
    * While running, click "Stop/Reset" to pause the simulation. The button text will change to "Reset".
    * When stopped, click "Reset" to clear the graphs and return the simulation to its initial state.
8.  **Analyze Graphs:** Observe the position, velocity, and acceleration plots as the simulation runs. Hover over the charts to see specific data points.
9.  **Monitor Status:** The "Simulation Status" card provides real-time updates on key physics values.

## Technical Details

The project is a single HTML file containing all the necessary CSS and JavaScript.

* **HTML5:** Structures the content and user interface.
* **CSS3:** Styles the layout and components, providing a clean and responsive design.
* **JavaScript (ES6+):** Powers the simulation logic, physics calculations, canvas drawing, and DOM manipulation.
* **Chart.js:** A powerful JavaScript library used for generating the interactive line graphs for position, velocity, and acceleration.

### Physics Equations Used (Implicitly in Code)

The core of the simulation relies on Newton's Second Law: $F_{\text{net}} = ma$. The `acc` variable is calculated based on the net force and total mass for each scenario:

* **Inclined Table:**
    * Net Force ($F_{\text{net}}$): Influenced by hanging mass gravity, cart's gravitational component along the incline, and friction.
        $F_{\text{net}} = m_{\text{hanging}}g + m_{\text{cart}}g\sin(\theta) - \mu m_{\text{cart}}g\cos(\theta)$
    * Acceleration ($a$): $a = F_{\text{net}} / (m_{\text{cart}} + m_{\text{hanging}})$
* **Atwood Machine:**
    * Net Force ($F_{\text{net}}$): The difference in gravitational forces of the two masses.
        $F_{\text{net}} = |m_2 - m_1|g$
    * Acceleration ($a$): $a = \frac{m_2 - m_1}{m_1 + m_2}g$

Kinematic equations are then used to update position and velocity:
* $v = v_0 + at$
* $x = x_0 + v_0t + \frac{1}{2}at^2$

## Development

To run and modify the code:

1.  Clone this repository or download the `N2L_Table.html` file.
2.  Open the `N2L_Table.html` file in any modern web browser (e.g., Chrome, Firefox, Edge).
3.  Edit the HTML, CSS, or JavaScript directly in your preferred code editor.

## License

This project is open-source and available under the [MIT License](LICENSE).