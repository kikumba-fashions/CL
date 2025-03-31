# CL
/head>
<body>
    <!-- Navigation -->
    <nav class="navbar">
        <div class="nav-container">
            <div class="logo">CL</div>
            <div class="nav-links">
                <a href="#home">Home</a>
                <a href="#profile">Profile</a>
                <a href="#live">Live</a>
                <a href="#conference">Conference</a>
                <a href="#chat">Chat</a>
            </div>
        </div>
    </nav>

    <!-- Main Content -->
    <div class="container">
        <!-- Left Sidebar -->
        <div class="sidebar">
            <div class="sidebar-item"><i class="fas fa-user"></i> Profile</div>
            <div class="sidebar-item"><i class="fas fa-video"></i> Live Stream</div>
            <div class="sidebar-item"><i class="fas fa-users"></i> Conference</div>
            <div class="sidebar-item"><i class="fas fa-comments"></i> Messages</div>
        </div>

        <!-- Main Content Area -->
        <div class="main-content">
            <div class="video-section">
                <h2>Live Stream / Video Conference</h2>
                <div class="video-player" id="videoPlayer">
                    <!-- Video stream will be injected here -->
                </div>
                <div class="controls">
                    <button class="btn" onclick="startStream()">Start Stream</button>
                    <button class="btn" onclick="startConference()">Start Conference</button>
                    <button class="btn" onclick="startChat()">Video Chat</button>
                </div>
            </div>
        </div>

        <!-- Right Sidebar -->
        <div class="right-sidebar">
            <h3>Active Users</h3>
            <div class="user-list">
                <p>User 1 <span class="status online"></span></p>
                <p>User 2 <span class="status offline"></span></p>
            </div>
        </div>
    </div>

    <!-- Mobile Navigation -->
    <nav class="mobile-nav">
        <div class="nav-links">
            <a href="#home"><i class="fas fa-home"></i></a>
            <a href="#profile"><i class="fas fa-user"></i></a>
            <a href="#live"><i class="fas fa-video"></i></a>
            <a href="#conference"><i class="fas fa-users"></i></a>
            <a href="#chat"><i class="fas fa-comments"></i></a>
        </div>
    </nav>

    <!-- AI Chatbot -->
    <div class="chatbot" id="chatbot">
        <div class="chatbot-header">
            <h3>AI Assistant</h3>
        </div>
        <div class="chatbot-body" id="chatbotBody">
            <p>Hello! How can I assist you today?</p>
        </div>
    </div>

    <script>
        // Basic Video Functionality (Placeholder - Requires WebRTC implementation)
        async function startStream() {
            try {
                const stream = await navigator.mediaDevices.getUserMedia({ video: true, audio: true });
                const video = document.createElement('video');
                video.srcObject = stream;
                video.autoplay = true;
                document.getElementById('videoPlayer').innerHTML = '';
                document.getElementById('videoPlayer').appendChild(video);
            } catch (err) {
                console.error('Error accessing media devices:', err);
                alert('Could not start stream. Please check your camera permissions.');
            }
        }

        function startConference() {
            alert('Conference feature coming soon! Requires WebRTC peer connection.');
        }

        function startChat() {
            document.getElementById('chatbot').classList.toggle('active');
        }

        // AI Chatbot basic interaction
        const chatbotBody = document.getElementById('chatbotBody');
        function addMessage(message) {
            const p = document.createElement('p');
            p.textContent = message;
            chatbotBody.appendChild(p);
            chatbotBody.scrollTop = chatbotBody.scrollHeight;
        }

        // Simulate AI response
        document.getElementById('chatbot').addEventListener('click', () => {
            setTimeout(() => addMessage('AI: How can I help with your video needs?'), 1000);
        });
    </script>
</body>
</html>video.autoplaychatbotBody.scrollTop0.mobile-nav {
                display: block;
                position: fixed;
                bottom: 0;
                width: 100%;
                background: #fff;
                padding: 10px;
                box-shadow: 0 -2px 5px rgba(0,0,0,0.1);
            }
            .mobile-nav .nav-links {
                display: flex;
                justify-content: space-around;
            }
        }

        @media (min-width: 969px) {
            .mobile-nav {
                display
        /* Right Sidebar */
        .right-sidebar {
            background: #fff;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }2video.srcObjectp.textContent/* AI Chatbot */
        .chatbot {
            position: fixed;
            bottom: 20px;
            right: 20px;
            width: 300px;
            background: #fff;
            border-radius: 10px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.2);
            display: none;
        }

        .chatbot.active {
            display: block;
        }

        .chatbot-header {
            background: #1877f2;
            color: #fff;
            padding: 10px;
            border-radius: 10px 10px 0 0;
        }

        .chatbot-body {
            padding: 10px;
            max-height: 300px;
            overflow-y: auto;
        }/* Responsive Design */
        @media (max-width: 968px) {
            .container {
                grid-template-columns: 1fr;
            }
            .sidebar, .right-sidebar {
                display: none;
