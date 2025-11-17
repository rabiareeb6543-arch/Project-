<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Delish Dine Restaurant</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f9f6f2;
            margin: 0;
            padding: 0;
        }

        /* Header Section */
        .header {
            background: linear-gradient(135deg, #a9441b, #802f0f);
            color: white;
            text-align: center;
            padding: 30px 20px;
        }

        .header h1 {
            margin: 0;
            font-size: 2.5em;
            letter-spacing: 2px;
        }

        .header h3 {
            font-style: italic;
            color: #ffddb6;
            margin-top: 5px;
        }

        .intro {
            text-align: center;
            margin: 10px auto;
            width: 80%;
            font-size: 16px;
        }

        hr {
            width: 70%;
            border: 1px solid #fff;
        }

        /* Menu Section */
        .menu {
            text-align: center;
            margin-top: 20px;
        }

        table {
            width: 70%;
            margin: 0 auto;
            border-collapse: collapse;
            box-shadow: 0 4px 10px rgba(0,0,0,0.1);
        }

        th, td {
            border: 1px solid #a9441b;
            padding: 12px;
            text-align: center;
            position: relative;
        }

        th {
            background-color: #ffe5cc;
            color: #a9441b;
        }

        td {
            background-color: #fff8f2;
            transition: background-color 0.3s, transform 0.2s;
        }

        tr:hover td {
            background-color: #ffe7cc;
            transform: scale(1.02);
            cursor: pointer;
        }

        /* Tooltip */
        td[data-tooltip]:hover::after {
            content: attr(data-tooltip);
            position: absolute;
            bottom: 110%;
            left: 50%;
            transform: translateX(-50%);
            background: #a9441b;
            color: #fff;
            padding: 5px 8px;
            border-radius: 4px;
            font-size: 12px;
            white-space: nowrap;
        }

        /* Offers Section */
        .offers {
            width: 70%;
            margin: 30px auto;
            background-color: #fff3e0;
            border-left: 5px solid #a9441b;
            padding: 15px;
            box-shadow: 0 4px 10px rgba(0,0,0,0.1);
        }

        .offers h3 {
            text-align: center;
            color: #a9441b;
        }

        .offers ul {
            font-size: 15px;
            line-height: 1.8;
        }

        .offers ul li:hover {
            background: #ffe7cc;
            cursor: pointer;
            transition: 0.3s;
        }

        /* Contact Form */
        .contact {
            width: 70%;
            margin: 30px auto;
            background-color: #ffe7cc;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 4px 10px rgba(0,0,0,0.1);
        }

        .contact h3 {
            text-align: center;
            color: #a9441b;
        }

        input, textarea {
            width: 95%;
            padding: 10px;
            margin: 8px 0;
            border: 1px solid #a9441b;
            border-radius: 4px;
            transition: border-color 0.3s;
        }

        input:focus, textarea:focus {
            border-color: #802f0f;
            outline: none;
        }

        textarea {
            height: 80px;
        }

        button {
            display: block;
            width: 97%;
            padding: 12px;
            background-color: #a9441b;
            color: white;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            font-size: 16px;
            transition: background-color 0.3s, transform 0.2s;
        }

        button:hover {
            background-color: #802f0f;
            transform: scale(1.05);
        }

        /* Modal */
        .modal {
            display: none;
            position: fixed;
            z-index: 1000;
            left: 0; top: 0;
            width: 100%; height: 100%;
            background: rgba(0,0,0,0.6);
            justify-content: center;
            align-items: center;
        }

        .modal-content {
            background: #fff8f2;
            padding: 20px;
            border-radius: 8px;
            width: 50%;
            text-align: center;
            box-shadow: 0 4px 10px rgba(0,0,0,0.2);
        }

        .close {
            float: right;
            font-size: 20px;
            cursor: pointer;
            color: #a9441b;
        }

        .close:hover {
            color: #802f0f;
        }
    </style>
</head>
<body>
    <div class="header">
        <h1>Delish Dine Restaurant</h1>
        <h3>Taste that touches your heart</h3>
        <hr>
        <p class="intro">
            Welcome to <b>Delish Dine</b> - where every meal is crafted with <i>love</i>, <u>flavor</u>, and <big>freshness</big>.
        </p>
        <p>
            We serve <small>happiness</small> in every bite!
        </p>
    </div>

    <div class="menu">
        <h2><u>Our Menu</u></h2>
        <table>
            <tr>
                <th>Dish Name</th>
                <th>Type</th>
                <th>Price</th>
            </tr>
            <tr>
                <td data-tooltip="Creamy pasta with grilled chicken">Chicken Alfredo Pasta</td>
                <td>Main</td>
                <td>Rs. 850</td>
            </tr>
            <tr>
                <td data-tooltip="Fresh lettuce, croutons & parmesan">Caesar Salad</td>
                <td>Starter</td>
                <td>Rs. 450</td>
            </tr>
            <tr>
                <td data-tooltip="Perfectly grilled fish with herbs">Grilled Fish</td>
                <td>Main</td>
                <td>Rs. 950</td>
            </tr>
            <tr>
                <td data-tooltip="Warm chocolate cake with molten center">Chocolate Lava Cake</td>
                <td>Dessert</td>
                <td>Rs. 550</td>
            </tr>
            <tr>
                <td data-tooltip="Crispy golden fries">French Fries</td>
                <td>Starter</td>
                <td>Rs. 300</td>
            </tr>
        </table>
    </div>

    <div class="offers">
        <h3>Our Special Offers</h3>
        <ul>
            <li onclick="openModal('Buy One Get One Free on Weekends')">Buy One Get One Free on Weekends</li>
            <li onclick="openModal('Free Dessert with Family Combo')">Free Dessert with Family Combo</li>
            <li onclick="openModal('20% Discount for Students')">20% Discount for Students</li>
            <li onclick="openModal('Home Delivery Available')">Home Delivery Available</li>
        </ul>
    </div>

    <div class="contact">
        <h3>Contact Us</h3>
        <form onsubmit="event.preventDefault(); openModal('Thank you for contacting us! We will reply soon.')">
            <label for="name">Name:</label><br>
            <input id="name" type="text" placeholder="Enter your name" required><br>
            <label for="email">Email:</label><br>
            <input id="email" type="email" placeholder="Enter your email" required><br>
            <label for="message">Message:</label><br>
            <textarea id="message" placeholder="Your message here..." required></textarea><br>
            <button type="submit">Send Message</button>
        </form>
    </div>

    <!-- Modal -->
    <div id="modal" class="modal">
        <div class="modal-content">
            <span class="close" onclick="closeModal()">&times;</span>
            <p id="modal-text"></p>
        </div>
    </div>

    <script>
        function openModal(message) {
            document.getElementById('modal-text').innerText = message;
            document.getElementById('modal').style
