The HTML File (index.html)
HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Card Designs & Display Properties</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <header class="page-header">
        <h1>Pricing Cards & Display Showcase</h1>
        <p>Explore distinct card designs and practical examples of CSS display properties.</p>
    </header>

    <main class="container">
        
        <!-- STEP 5: Display Demonstration Section -->
        <section class="display-section">
            <h2>Understanding CSS Display Properties</h2>
            <p>
                This text contains an <span class="demo-inline">inline span element</span> that flows within the text line. 
                Next, we have a <span class="demo-inline-block">inline-block badge</span> which respects padding and width while staying in line.
            </p>
            <div class="demo-block">This is a block-level div element that takes up the full width by default.</div>
        </section>

        <!-- STEPS 1, 2, 3, 4, & 6: Three Card Designs -->
        <section class="cards-container">
            
            <!-- Basic Card -->
            <div class="card card-basic">
                <h3>Basic Plan</h3>
                <p class="price">$9 / mo</p>
                <p class="description">Essential features for individuals starting out with basic needs.</p>
                <button class="btn">Choose Basic</button>
            </div>

            <!-- Standard Card -->
            <div class="card card-standard">
                <h3>Standard Plan</h3>
                <p class="price">$29 / mo</p>
                <p class="description">Great for growing projects requiring advanced tools and support.</p>
                <button class="btn">Choose Standard</button>
            </div>

            <!-- Premium Card -->
            <div class="card card-premium">
                <h3>Premium Plan</h3>
                <p class="price">$59 / mo</p>
                <p class="description">Full-featured tier with top-tier priority support and unlimited access.</p>
                <button class="btn">Choose Premium</button>
            </div>

        </section>

    </main>

</body>
</html>
2. The CSS File (style.css)
CSS
/* Global Page Settings */
body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    background-color: #f1f5f9;
    color: #334155;
    margin: 0;
    padding: 30px;
    line-height: 1.6;
}

.page-header {
    text-align: center;
    margin-bottom: 40px;
}

.page-header h1 {
    color: #1e293b;
    margin-bottom: 8px;
}

.container {
    max-width: 1000px;
    margin: 0 auto;
}

/* STEP 5: Display Demonstration Styles */
.display-section {
    background-color: #ffffff;
    padding: 20px;
    border-radius: 8px;
    border: 1px solid #cbd5e1;
    margin-bottom: 40px;
}

.display-section h2 {
    margin-top: 0;
    font-size: 1.25rem;
    color: #0f172a;
}

/* display: inline */
.demo-inline {
    display: inline;
    background-color: #fde047;
    padding: 2px 4px; /* Note: vertical padding doesn't affect line height for inline elements */
    font-weight: bold;
}

/* display: inline-block */
.demo-inline-block {
    display: inline-block;
    background-color: #38bdf8;
    color: white;
    padding: 6px 12px;
    border-radius: 4px;
    margin: 0 5px;
    font-weight: 600;
}

/* display: block */
.demo-block {
    display: block;
    background-color: #e2e8f0;
    padding: 12px;
    margin-top: 15px;
    border-left: 4px solid #64748b;
}

/* STEPS 1, 2, 3, 4, & 6: Cards Layout */
.cards-container {
    display: flex;
    gap: 20px;
    flex-wrap: wrap;
    justify-content: center;
}

/* Base Card Styling */
.card {
    width: 100%;            /* Step 6 */
    max-width: 300px;       /* Step 6: max-width constraint */
    min-height: 320px;      /* Step 6: height specification */
    padding: 25px;
    border-radius: 12px;    /* Step 4: rounded corners */
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.05);
    transition: transform 0.2s ease;
}

.card:hover {
    transform: translateY(-4px);
}

.card h3 {
    margin-top: 0;
    font-size: 1.4rem;
}

.card .price {
    font-size: 1.75rem;
    font-weight: bold;
    margin: 10px 0;
}

.card .description {
    font-size: 0.95rem;
    flex-grow: 1;
}

/* Buttons inside cards */
.btn {
    background-color: #334155;
    color: white;
    border: none;
    padding: 10px 16px;
    border-radius: 6px;
    font-weight: 600;
    cursor: pointer;
    text-align: center;
    transition: background-color 0.2s;
}

.btn:hover {
    background-color: #0f172a;
}

/* STEP 3: Distinct Background Colors and Borders */

/* Basic Card */
.card-basic {
    background-color: #ffffff;
    border: 2px solid #cbd5e1;
}

.card-basic .price {
    color: #475569;
}

/* Standard Card */
.card-standard {
    background-color: #f0fdf4;
    border: 2px solid #22c55e;
}

.card-standard .price {
    color: #16a34a;
}

.card-standard .btn {
    background-color: #16a34a;
}
.card-standard .btn:hover {
    background-color: #15803d;
}

/* Premium Card */
.card-premium {
    background-color: #fef2f2;
    border: 2px dashed #ef4444; /* Dashed border for visual distinction */
}

.card-premium .price {
    color: #dc2626;
}

.card-premium .btn {
    background-color: #dc2626;
}
.card-premium .btn:hover {
    background-color: #b91c1c;
}