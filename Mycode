<!DOCTYPE html>
<html>
<head>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f2f2f2;
        }

        .container {
            margin: 50px auto;
            width: 400px;
            background-color: #fff;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.3);
        }

        h1 {
            text-align: center;
            padding: 20px;
            color: #3498db;
        }

        #qr-code {
            text-align: center;
            padding: 20px;
        }

        #input {
            text-align: center;
            padding: 20px;
        }

        #qr-text {
            width: 100%;
            font-size: 16px;
            padding: 10px;
            border: 1px solid #e0e0e0;
            border-radius: 5px;
        }

        #generate-button {
            background-color: #27ae60;
            color: #fff;
            border: none;
            border-radius: 5px;
            padding: 10px 20px;
            cursor: pointer;
            margin-top: 10px;
        }

        #share-button {
            background-color: #3498db;
            color: #fff;
            border: none;
            border-radius: 5px;
            padding: 10px 20px;
            cursor: pointer;
            margin-top: 10px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>QR Code Generator</h1>
        <div id="qr-code">
            <img id="qr-image" src="" alt="QR Code">
        </div>
        <div id="input">
            <input type="text" id="qr-text" placeholder="Enter text or URL">
            <button id="generate-button">Generate QR Code</button>
            <button id="share-button">Share QR Code</button>
        </div>
    </div>

    <script>
        const qrText = document.getElementById("qr-text");
        const qrImage = document.getElementById("qr-image");
        const generateButton = document.getElementById("generate-button");
        const shareButton = document.getElementById("share-button");

        generateButton.addEventListener("click", () => {
            generateQRCode();
        });

        shareButton.addEventListener("click", () => {
            if (qrImage.src) {
                // Generate a shareable link or use your preferred method
                alert("Share this QR code: " + qrImage.src);
            }
        });

        function generateQRCode() {
            const text = qrText.value.trim();
            if (text) {
                const qrCodeURL = `https://api.qrserver.com/v1/create-qr-code/?size=150x150&data=${encodeURIComponent(text)}`;
                qrImage.src = qrCodeURL;
            }
        }
    </script>
</body>
</html>
