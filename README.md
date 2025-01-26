
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <title>ÔN LUYỆN TOÁN THCS - TRUNG TÂM ÁNH DƯƠNG</title>
     <!-- Thêm MathJax -->
    <script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
    <script>
        window.MathJax = {
            tex: {
                inlineMath: [['$', '$'], ['\\(', '\\)']]
            },
            svg: {
                fontCache: 'global'
            }
        };
    </script>
    <script id="MathJax-script" async
        src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js">
    </script>
<link rel="stylesheet" href="styles.css"> <!-- Kết nối CSS -->
</head>
<body>
    <h1>ÔN LYỆN TOÁN LỚP 6  - THẦY GIÁO TÔN THANH CHƯƠNG</h1>    
    <div id="loginContainer">
        <input type="text" id="studentId" placeholder="Nhập mã học sinh">
        <button id="loginBtn">Đăng nhập</button>
    </div>
   <div id="mainContent" style="display: none;">
    <!-- Hàng trên cùng: Khung nhập số và các nút liên quan -->
    <div id="topControls">
        <input type="number" id="problemIndexInput" placeholder="Nhập số thứ tự (1, 2, ...)" />
        <button id="selectProblemBtn">Hiển thị bài tập</button>
        <button id="randomProblemBtn">Lấy bài tập ngẫu nhiên</button>
	<div id="progressContainer" style="display: none;">
    <p>
        Số bài: <span id="completedExercises">0</span> | 
        Điểm TB: <span id="averageScore">0</span>
    </p>
</div>
    </div>
    <!-- Hàng thứ hai: Đề bài -->
    <div id="problemContainer">
        <label for="problemText">Đề bài:</label>
        <div id="problemText"></div>
	</div>

    <!-- Hàng thứ ba: Các nút chức năng -->
    <div id="bottomControls">
        <button id="submitBtn">Chấm Bài</button>
        <button id="hintBtn">Gợi ý</button>
	<button id="deleteAllBtn">Xóa tất cả</button>
    </div>
  <div id="result"></div>
         
        <label for="studentImage">Ảnh bài làm của học sinh:</label>
        <input type="file" id="studentImage" accept="image/*">
	<label for="cameraStream">Hoặc chụp ảnh từ camera:</label>
<div id="cameraAndImageContainer">
    <!-- Video container -->
    <div id="videoContainer">
        <video id="cameraStream" autoplay playsinline></video>
        <button id="captureButton" style="margin-top: 10px;">Chụp ảnh</button>
    </div>

    <!-- Image container -->
    <div id="imageContainer">
        <canvas id="photoCanvas" style="display: none;"></canvas>
        <img id="capturedImage" alt="Ảnh đã chụp" style="max-width: 100%; display: none;">
    </div>
</div>        
    </div>
   
</body>
</html>
