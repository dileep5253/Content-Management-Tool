# Content-Management-Tool
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Blog Content Management Tool</title>
    <style>
        /* Add your CSS styles for the content management tool here */
    </style>
</head>
<body>
    <h1>Welcome to the Blog Content Management Tool</h1>

    <div id="content-container">
        <div id="text-editor" class="editor">
            <h2>Text Editor</h2>
            <textarea placeholder="Write your text here"></textarea>
        </div>

        <div id="image-editor" class="editor">
            <h2>Image Editor</h2>
            <input type="file" accept="image/*" id="image-upload">
            <img id="uploaded-image" alt="Uploaded Image">
        </div>

        <div id="video-editor" class="editor">
            <h2>Video Editor</h2>
            <input type="file" accept="video/*" id="video-upload">
            <video id="uploaded-video" controls>
                Your browser does not support the video tag.
            </video>
        </div>

        <!-- Add more editor sections for other elements as needed -->

    </div>

    <script>
        // Add your JavaScript code for drag-and-drop functionality here
        const imageUpload = document.getElementById("image-upload");
        const uploadedImage = document.getElementById("uploaded-image");

        const videoUpload = document.getElementById("video-upload");
        const uploadedVideo = document.getElementById("uploaded-video");

        imageUpload.addEventListener("change", (e) => {
            const file = e.target.files[0];
            if (file) {
                const imageURL = URL.createObjectURL(file);
                uploadedImage.src = imageURL;
            }
        });

        videoUpload.addEventListener("change", (e) => {
            const file = e.target.files[0];
            if (file) {
                const videoURL = URL.createObjectURL(file);
                uploadedVideo.src = videoURL;
            }
        });
    </script>
</body>
</html>
