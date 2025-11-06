/* Basic Reset & Body Styling */
body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    margin: 0;
    background-color: #f0f2f5; /* Light grey background */
    color: #333;
    line-height: 1.6;
}

header {
    background-color: #333;
    color: white;
    padding: 20px 0;
    text-align: center;
    box-shadow: 0 2px 5px rgba(0,0,0,0.2);
}

h1 {
    margin: 0;
    font-size: 2.5em;
}

/* Gallery Container - The heart of the Grid Layout */
.gallery-container {
    display: grid; /* Turns the container into a CSS Grid */
    
    /* Defines responsive columns: at least 280px wide, and as many as fit */
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); 
    
    gap: 20px; /* Space between grid items */
    padding: 20px;
    max-width: 1200px; /* Max width for the entire gallery */
    margin: 20px auto; /* Center the gallery on the page */
}

/* Styling for each individual gallery item */
.gallery-item {
    background-color: white;
    border-radius: 8px;
    overflow: hidden; 
    box-shadow: 0 4px 8px rgba(0,0,0,0.1);
    /* Transition for smooth hover effects */
    transition: transform 0.3s ease-in-out, box-shadow 0.3s ease-in-out;
}

.gallery-item:hover {
    transform: translateY(-5px) scale(1.02); /* Slight lift and scale on hover */
    box-shadow: 0 8px 16px rgba(0,0,0,0.2);
}

.gallery-item img {
    width: 100%; 
    height: 200px; /* Fixed height for uniformity */
    object-fit: cover; /* Ensures images cover the area without distortion */
    display: block; 
}

.caption {
    padding: 15px;
    font-size: 1.1em;
    font-weight: bold;
    color: #555;
    text-align: center;
}

/* Responsive Adjustments */
@media (max-width: 600px) {
    .gallery-container {
        grid-template-columns: 1fr; /* On very small screens, stack items in a single column */
        padding: 10px;
        gap: 15px;
    }
}
