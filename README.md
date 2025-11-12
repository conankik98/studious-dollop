<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>TalentHub - Nền tảng tuyển dụng thông minh</title>
    <style>
        :root {
            --primary: #2563eb;
            --secondary: #64748b;
            --success: #10b981;
            --warning: #f59e0b;
            --error: #ef4444;
            --background: #f8fafc;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background-color: var(--background);
            color: #334155;
        }

        /* Header */
        .navbar {
            background: white;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            padding: 1rem 5%;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
        }

        .nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1400px;
            margin: 0 auto;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: bold;
            color: var(--primary);
        }

        .nav-links {
            display: flex;
            gap: 2rem;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--secondary);
            font-weight: 500;
            transition: color 0.3s;
        }

        .nav-links a:hover {
            color: var(--primary);
        }

        .auth-buttons {
            display: flex;
            gap: 1rem;
        }

        .btn {
            padding: 0.5rem 1.5rem;
            border-radius: 6px;
            border: none;
            font-weight: 500;
            cursor: pointer;
            transition: all 0.3s;
        }

        .btn-primary {
            background: var(--primary);
            color: white;
        }

        .btn-outline {
            background: transparent;
            border: 1px solid var(--primary);
            color: var(--primary);
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(135deg, #2563eb 0%, #1e40af 100%);
            color: white;
            padding: 120px 5% 80px;
            text-align: center;
        }

        .hero h1 {
            font-size: 3rem;
            margin-bottom: 1rem;
        }

        .hero p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
            opacity: 0.9;
        }

        /* Features Section */
        .features {
            padding: 80px 5%;
            max-width: 1200px;
            margin: 0 auto;
        }

        .section-title {
            text-align: center;
            margin-bottom: 3rem;
        }

        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .feature-card {
            background: white;
            padding: 2rem;
            border-radius: 10px;
            box-shadow: 0 4px 6px rgba(0,0,0,0.05);
            transition: transform 0.3s;
        }

        .feature-card:hover {
            transform: translateY(-5px);
        }

        .feature-icon {
            background: var(--primary);
            color: white;
            width: 50px;
            height: 50px;
            border-radius: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-bottom: 1rem;
        }

        /* Dashboard Demo */
        .dashboard {
            background: white;
            margin: 40px 5%;
            border-radius: 10px;
            box-shadow: 0 4px 6px rgba(0,0,0,0.05);
            overflow: hidden;
        }

        .dashboard-tabs {
            display: flex;
            background: #f1f5f9;
            border-bottom: 1px solid #e2e8f0;
        }

        .tab {
            padding: 1rem 2rem;
            cursor: pointer;
            border-bottom: 3px solid transparent;
        }

        .tab.active {
            border-bottom-color: var(--primary);
            color: var(--primary);
            font-weight: 500;
        }

        .tab-content {
            padding: 2rem;
            display: none;
        }

        .tab-content.active {
            display: block;
        }

        .job-list {
            display: grid;
            gap: 1rem;
        }

        .job-item {
            padding: 1.5rem;
            border: 1px solid #e2e8f0;
            border-radius: 8px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .candidate-item {
            display: flex;
            align-items: center;
            gap: 1rem;
            padding: 1rem;
            border: 1px solid #e2e8f0;
            border-radius: 8px;
            margin-bottom: 1rem;
        }

        .match-score {
            background: var(--success);
            color: white;
            padding: 0.25rem 0.5rem;
            border-radius: 20px;
            font-size: 0.8rem;
        }

        /* AI Features */
        .ai-section {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 80px 5%;
            text-align: center;
        }

        .ai-features {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .ai-card {
            background: rgba(255,255,255,0.1);
            padding: 2rem;
            border-radius: 10px;
            backdrop-filter: blur(10px);
        }

        /* Responsive */
        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }
            
            .hero h1 {
                font-size: 2rem;
            }
            
            .features-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <!-- Navigation -->
    <nav class="navbar">
        <div class="nav-container">
            <div class="logo">TalentHub</div>
            <div class="nav-links">
                <a href="#features">Tính năng</a>
                <a href="#pricing">Bảng giá</a>
                <a href="#about">Về chúng tôi</a>
                <a href="#blog">Blog</a>
            </div>
            <div class="auth-buttons">
                <button class="btn btn-outline">Đăng nhập</button>
                <button class="btn btn-primary">Đăng ký Nhà tuyển dụng</button>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section class="hero">
        <h1>Tuyển Dụng Thông Minh, Kết Nối Tin Cậy</h1>
        <p>Nền tảng tuyển dụng thế hệ mới với AI - Tìm ứng viên chất lượng cao, nhanh chóng và hiệu quả</p>
        <button class="btn btn-primary" style="background: white; color: var(--primary); margin-right: 1rem;">
            Bắt đầu miễn phí
        </button>
        <button class="btn btn-outline" style="border-color: white; color: white;">
            Xem demo
        </button>
    </section>

    <!-- Features Section -->
    <section class="features" id="features">
        <div class="section-title">
            <h2>Tính Năng Đột Phá Dành Cho Nhà Tuyển Dụng</h2>
        </div>
        <div class="features-grid">
            <div class="feature-card">
                <div class="feature-icon">🤖</div>
                <h3>AI Sourcing Thông minh</h3>
                <p>Tự động tìm kiếm và đề xuất ứng viên phù hợp nhất dựa trên mô tả công việc của bạn</p>
            </div>
            <div class="feature-card">
                <div class="feature-icon">📊</div>
                <h3>Phân tích HR Analytics</h3>
                <p>Theo dõi ROI, phân tích hiệu quả tuyển dụng với báo cáo chi tiết theo thời gian thực</p>
            </div>
            <div class="feature-card">
                <div class="feature-icon">🔍</div>
                <h3>Hồ sơ Ứng viên Đa chiều</h3>
                <p>Xác thực kỹ năng, đánh giá từ đồng nghiệp cũ, video giới thiệu bản thân</p>
            </div>
            <div class="feature-card">
                <div class="feature-icon">👥</div>
                <h3>Công cụ Hợp tác Nhóm</h3>
                <p>Quản lý tuyển dụng theo nhóm, đánh giá ứng viên tập trung, lịch phỏng vấn thông minh</p>
            </div>
            <div class="feature-card">
                <div class="feature-icon">💬</div>
                <h3>Phỏng vấn Tích hợp</h3>
                <p>Công cụ phỏng vấn video tích hợp, ghi hình tự động, chấm điểm ứng viên</p>
            </div>
            <div class="feature-card">
                <div class="feature-icon">🎯</div>
                <h3>Cộng đồng Chuyên gia</h3>
                <p>Kết nối với cộng đồng ứng viên thụ động chất lượng cao theo ngành nghề</p>
            </div>
        </div>
    </section>

    <!-- Dashboard Demo -->
    <section class="features">
        <div class="section-title">
            <h2>Trải nghiệm Bảng Điều Khiển Thông Minh</h2>
            <p>Quản lý toàn bộ quy trình tuyển dụng trong một giao diện duy nhất</p>
        </div>
        
        <div class="dashboard">
            <div class="dashboard-tabs">
                <div class="tab active" onclick="switchTab('jobs')">Tin tuyển dụng</div>
                <div class="tab" onclick="switchTab('candidates')">Ứng viên</div>
                <div class="tab" onclick="switchTab('analytics')">Phân tích</div>
                <div class="tab" onclick="switchTab('ai')">AI Sourcing</div>
            </div>
            
            <div id="jobs" class="tab-content active">
                <h3>Quản lý Tin Tuyển Dụng</h3>
                <div class="job-list">
                    <div class="job-item">
                        <div>
                            <h4>Senior Frontend Developer</h4>
                            <p>Đã nhận: 24 hồ sơ • Ứng viên phù hợp: 8</p>
                        </div>
                        <div>
                            <span class="match-score">5 ứng viên 80%+</span>
                        </div>
                    </div>
                    <div class="job-item">
                        <div>
                            <h4>Product Manager</h4>
                            <p>Đã nhận: 15 hồ sơ • Ứng viên phù hợp: 4</p>
                        </div>
                        <div>
                            <span class="match-score">2 ứng viên 85%+</span>
                        </div>
                    </div>
                </div>
            </div>
            
            <div id="candidates" class="tab-content">
                <h3>Quản lý Ứng viên</h3>
                <div class="candidate-item">
                    <div style="width: 40px; height: 40px; background: var(--primary); border-radius: 50%; display: flex; align-items: center; justify-content: center; color: white;">
                        NN
                    </div>
                    <div style="flex: 1;">
                        <h4>Nguyễn Văn A</h4>
                        <p>Senior Frontend Developer • 5 năm kinh nghiệm</p>
                    </div>
                    <div class="match-score">92% phù hợp</div>
                </div>
                <div class="candidate-item">
                    <div style="width: 40px; height: 40px; background: var(--success); border-radius: 50%; display: flex; align-items: center; justify-content: center; color: white;">
                        TB
                    </div>
                    <div style="flex: 1;">
                        <h4>Trần Thị B</h4>
                        <p>Product Manager • 4 năm kinh nghiệm</p>
                    </div>
                    <div class="match-score">88% phù hợp</div>
                </div>
            </div>
            
            <div id="analytics" class="tab-content">
                <h3>Phân tích Tuyển Dụng</h3>
                <p>📈 Thời gian tuyển dụng trung bình: <strong>18 ngày</strong></p>
                <p>💰 Chi phí mỗi lần tuyển: <strong>12.5 triệu VND</strong></p>
                <p>🎯 Nguồn ứng viên chất lượng nhất: <strong>AI Sourcing (45%)</strong></p>
            </div>
            
            <div id="ai" class="tab-content">
                <h3>AI Sourcing - Ứng viên Đề xuất</h3>
                <p>AI đã tìm thấy <strong>12 ứng viên tiềm năng</strong> phù hợp với yêu cầu của bạn</p>
                <div style="background: #f0f9ff; padding: 1rem; border-radius: 8px; margin-top: 1rem;">
                    <h4>🎯 Nguyễn Văn C - Fullstack Developer</h4>
                    <p>• 4 năm kinh nghiệm React & Node.js</p>
                    <p>• Đang làm tại Công ty Tech hàng đầu</p>
                    <p>• Phù hợp 94% với vị trí Senior Developer</p>
                    <button class="btn btn-primary" style="margin-top: 0.5rem;">Liên hệ ngay</button>
                </div>
            </div>
        </div>
    </section>

    <!-- AI Features Section -->
    <section class="ai-section">
        <h2>Công nghệ AI - Thay đổi cách bạn Tuyển dụng</h2>
        <p>Ứng dụng trí tuệ nhân tạo tiên tiến để tự động hóa và tối ưu hóa toàn bộ quy trình</p>
        
        <div class="ai-features">
            <div class="ai-card">
                <h3>AI JD Writer</h3>
                <p>Tự động viết mô tả công việc hấp dẫn, tối ưu từ khóa</p>
            </div>
            <div class="ai-card">
                <h3>Phân tích Phù hợp</h3>
                <p>Đánh giá và xếp hạng ứng viên tự động với độ chính xác cao</p>
            </div>
            <div class="ai-card">
                <h3>Dự đoán Thành công</h3>
                <p>Dự đoán khả năng thành công của ứng viên trong công ty</p>
            </div>
        </div>
    </section>

    <!-- Pricing Section -->
    <section class="features" id="pricing">
        <div class="section-title">
            <h2>Linh hoạt với Mọi Ngân sách</h2>
        </div>
        <div class="features-grid">
            <div class="feature-card">
                <h3>🎗️ Miễn phí</h3>
                <p><strong>0 VND/tháng</strong></p>
                <ul style="list-style: none; margin-top: 1rem;">
                    <li>✓ 1 tin tuyển dụng</li>
                    <li>✓ Quản lý cơ bản</li>
                    <li>✓ Truy cập cộng đồng</li>
                </ul>
                <button class="btn btn-outline" style="width: 100%; margin-top: 1rem;">Bắt đầu ngay</button>
            </div>
            <div class="feature-card" style="border: 2px solid var(--primary);">
                <h3>🚀 Pro</h3>
                <p><strong>1.200.000 VND/tháng</strong></p>
                <ul style="list-style: none; margin-top: 1rem;">
                    <li>✓ 5 tin tuyển dụng</li>
                    <li>✓ AI Sourcing cơ bản</li>
                    <li>✓ Phân tích cơ bản</li>
                    <li>✓ Hỗ trợ 24/7</li>
                </ul>
                <button class="btn btn-primary" style="width: 100%; margin-top: 1rem;">Dùng thử 7 ngày</button>
            </div>
            <div class="feature-card">
                <h3>🏢 Enterprise</h3>
                <p><strong>Liên hệ</strong></p>
                <ul style="list-style: none; margin-top: 1rem;">
                    <li>✓ Tin tuyển dụng không giới hạn</li>
                    <li>✓ AI Sourcing nâng cao</li>
                    <li>✓ HR Analytics đầy đủ</li>
                    <li>✓ Tích hợp hệ thống</li>
                    <li>✓ Hỗ trợ chuyên dụng</li>
                </ul>
                <button class="btn btn-outline" style="width: 100%; margin-top: 1rem;">Liên hệ tư vấn</button>
            </div>
        </div>
    </section>

    <script>
        function switchTab(tabName) {
            // Ẩn tất cả tab content
            document.querySelectorAll('.tab-content').forEach(tab => {
                tab.classList.remove('active');
            });
            
            // Bỏ active tất cả tabs
            document.querySelectorAll('.tab').forEach(tab => {
                tab.classList.remove('active');
            });
            
            // Hiển thị tab được chọn
            document.getElementById(tabName).classList.add('active');
            
            // Active tab button
            event.currentTarget.classList.add('active');
        }

        // Demo tính năng AI JD Writer
        function generateJD() {
            const position = document.getElementById('positionInput').value;
            if (position) {
                document.getElementById('jdResult').innerHTML = `
                    <div style="background: #f0f9ff; padding: 1rem; border-radius: 8px; margin-top: 1rem;">
                        <h4>📝 Mô tả công việc được AI gợi ý cho: ${position}</h4>
                        <p><strong>Vị trí:</strong> ${position}</p>
                        <p><strong>Mô tả:</strong> Chúng tôi đang tìm kiếm một ${position} xuất sắc với kinh nghiệm chuyên sâu... 
                        Ứng viên lý tưởng sẽ có kỹ năng... và khả năng...</p>
                        <p><strong>Yêu cầu:</strong></p>
                        <ul>
                            <li>3+ năm kinh nghiệm liên quan</li>
                            <li>Thành thạo các công nghệ hiện đại</li>
                            <li>Kỹ năng giao tiếp và làm việc nhóm</li>
                        </ul>
                        <button class="btn btn-primary" onclick="useThisJD()">Sử dụng JD này</button>
                    </div>
                `;
            }
        }

        function useThisJD() {
            alert('Mô tả công việc đã được áp dụng! Bạn có thể chỉnh sửa chi tiết.');
        }
    </script>
</body>
</html>
