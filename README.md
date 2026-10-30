# BrainBook
A simple and smart note book for everyone
index.html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>BrainBook</title>

    <style>
        body {
            font-family: Arial, sans-serif;
            background: #f4f6f9;
            margin: 0;
            padding: 20px;
        }

        .container {
            max-width: 600px;
            margin: auto;
            background: white;
            padding: 20px;
            border-radius: 12px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }

        h1 {
            text-align: center;
            color: #304ffe;
        }

        textarea {
            width: 100%;
            height: 120px;
            padding: 10px;
            box-sizing: border-box;
            border: 1px solid #ccc;
            border-radius: 8px;
            font-size: 16px;
        }

        button {
            width: 100%;
            padding: 12px;
            margin-top: 10px;
            background: #304ffe;
            color: white;
            border: none;
            border-radius: 8px;
            font-size: 16px;
            cursor: pointer;
        }

        button:hover {
            background: #1a36c9;
        }

        .note {
            background: #eef1ff;
            padding: 12px;
            margin-top: 12px;
            border-radius: 8px;
            overflow-wrap: anywhere;
        }
    </style>
</head>

<body>

    <div class="container">
        <h1>BrainBook</h1>

        <p>Write down your thoughts and ideas.</p>

        <textarea id="noteInput" placeholder="Write your note here..."></textarea>

        <button onclick="saveNote()">Save Note</button>

        <h2>My Notes</h2>

        <div id="notesList"></div>
    </div>

    <script>
        function saveNote() {
            const input = document.getElementById("noteInput");
            const notesList = document.getElementById("notesList");

            const noteText = input.value.trim();

            if (noteText === "") {
                alert("Please write something first!");
                return;
            }

            const note = document.createElement("div");
            note.className = "note";
            note.textContent = noteText;

            notesList.appendChild(note);

            input.value = "";
        }
    </script>

</body>
</html>
+
