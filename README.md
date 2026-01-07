🗂️ Accordion V2 Learning Activity

A refined, interactive accordion component designed for structured content delivery and progressive disclosure in learning environments. This version features enhanced iconography, smoother transitions, and distinct active states.

🚀 Live Demo

Explore the Accordion V2 Component Here

✨ Project Overview

Accordion V2 provides a clean, organized way to present complex information. By grouping content into collapsible sections, it prevents cognitive overload and allows learners to focus on one topic at a time.

Key Features

Single-Open Logic: The component is designed to automatically close other sections when a new one is opened, maintaining a clean and focused viewport.

Visual Wayfinding: Each header includes a descriptive SVG icon (Target, Input, Checklist) to provide immediate context for the content within.

Dynamic Active States:

Inactive: White background with Midnight Blue text and a Slate Grey chevron.

Hover: Shifts to a Light Aqua tint to signal interactivity.

Active: Transitions to a full Teal background with white text and a rotated chevron for clear directional feedback.

Fluid Animations: Utilizes max-height and ease-out transitions to create a smooth sliding effect when expanding or collapsing sections.

🛠️ Technical Implementation

State Management: The toggleAccordion(header) function manages DOM classes. It loops through all headers and content blocks to remove active states from non-target elements before toggling the clicked item.

Responsive Architecture: The container is capped at 750px for optimal readability but scales to 100% width on mobile devices.

SVG Integration: Icons are embedded as inline SVGs to allow for CSS-based color transitions during state changes.

Tailwind CSS: Used for utility-first layout management (flexbox, spacing, shadows) alongside custom CSS for specific animation logic.

📂 Design Tokens

Midnight Blue (#1f2a52): Used for primary container borders and default text.

Teal (#00bec7): The "Active" state color for headers and primary icons.

Light Aqua (#d2f0f0): Used for hover states and content separators.

Slate Grey (#abb5bf): Used for inactive UI elements like arrows.

📖 Usage Instructions

To add more items, duplicate the accordion-item div structure. Ensure the onclick attribute is preserved on the header:

<div class="accordion-item">
    <div class="accordion-header" onclick="toggleAccordion(this)">
        <h3>
            <div class="icon-wrapper">
                <!-- Insert SVG here -->
            </div>
            Your Section Title
        </h3>
        <!-- Chevron SVG here -->
    </div>
    <div class="accordion-content">
        <div class="content-inner">
            <p>Your content goes here...</p>
        </div>
    </div>
</div>


📄 License

MIT License - Developed as part of the accounts-eles UI component library.
