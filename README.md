<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Eid Mubarak!</title>
    
    <style>
        /* CSS styles go here */
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            margin: 0;
            background-color: #f0f8ff; /* Light blue background */
            color: #333;
            text-align: center;
            overflow: hidden; /* Prevent scrollbar if elements go off-screen during animation */
        }

        .container {
            background-color: #fff;
            padding: 40px;
            border-radius: 15px;
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
            animation: fadeIn 2s ease-in-out; /* Animation for the container */
            max-width: 90%; /* Ensure it's responsive on smaller screens */
            box-sizing: border-box; /* Include padding in the element's total width and height */
        }

        h1 {
            color: #28a745; /* Green for greeting */
            font-size: 3em;
            margin-bottom: 20px;
            transition: color 0.5s ease-in-out; /* Smooth color transition for JavaScript changes */
        }

        p {
            font-size: 1.2em;
            line-height: 1.6;
        }

        button {
            background-color: #ffc107; /* Yellow for button */
            color: #333;
            border: none;
            padding: 12px 25px;
            border-radius: 8px;
            font-size: 1em;
            cursor: pointer;
            transition: background-color 0.3s ease, transform 0.3s ease;
            margin-top: 20px;
        }

        button:hover {
            background-color: #e0a800;
            transform: translateY(-2px); /* Slight lift on hover */
        }

        /* Keyframe animation for initial fade-in */
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(-20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        /* Responsive adjustments */
        @media (max-width: 600px) {
            h1 {
                font-size: 2.2em;
            }
            p {
                font-size: 1em;
            }
            .container {
                padding: 25px;
            }
            button {
                padding: 10px 20px;
                font-size: 0.9em;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <h1 id="greeting">Eid Mubarak!</h1>
        <h2 id="greeting">تقبل الله منا ومنكم</h2>
        <h3 id="greeting">Taqabbalallahu Minna Wa Minkum.</h3>

        <p>Wishing You And Your Family A Blessed Eid!</p>
        <button id="surpriseButton">Click for a little surprise!</button>
    </div>

    <script>
        // JavaScript code goes here
        document.addEventListener('DOMContentLoaded', () => {
            // Get references to the button and the greeting text
            const surpriseButton = document.getElementById('surpriseButton');
            const greetingElement = document.getElementById('greeting');

            // Add an event listener to the button
            surpriseButton.addEventListener('click', () => {
                // Change the greeting text
                greetingElement.textContent = "Eid Mubarak! May Your Day Be Filled With Joy and Blessings!";

                // Briefly change the color of the greeting for a visual "surprise"
                greetingElement.style.color = '#dc3545'; // A red color
                
                // After a short delay, revert the color back to green
                setTimeout(() => {
                    greetingElement.style.color = '#28a745'; 
                }, 1000); // 1000 milliseconds = 1 second

                // You could also add other effects here, like playing a sound or showing an image.
                console.log("Surprise button clicked!");
            });
        });
    </script>
</body>
</html>
