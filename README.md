<!DOCTYPE html><html lang="vi"><head><meta http-equiv="Content-Security-Policy" content="default-src 'self' 'unsafe-inline' 'unsafe-eval' data: blob: https://cdnjs.cloudflare.com https://cdn.jsdelivr.net https://code.jquery.com https://unpkg.com https://d3js.org https://threejs.org https://cdn.plot.ly https://stackpath.bootstrapcdn.com https://maps.googleapis.com https://cdn.tailwindcss.com https://ajax.googleapis.com https://kit.fontawesome.com https://cdn.datatables.net https://maxcdn.bootstrapcdn.com https://code.highcharts.com https://tako-static-assets-production.s3.amazonaws.com https://www.youtube.com https://fonts.googleapis.com https://fonts.gstatic.com https://pfst.cf2.poecdn.net https://puc.poecdn.net https://i.imgur.com https://wikimedia.org https://*.icons8.com https://*.giphy.com https://picsum.photos https://images.unsplash.com; frame-src 'self' https://www.youtube.com https://trytako.com; child-src 'self'; manifest-src 'self'; worker-src 'self'; upgrade-insecure-requests; block-all-mixed-content;">
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Khung Đo Lường ASO</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            darkMode: 'class',
            theme: {
                extend: {
                    colors: {
                        primary: '#5D5CDE',
                        primaryLight: '#7A79E8',
                        primaryDark: '#4A49B8',
                    }
                }
            }
        }

        // Check for dark mode preference
        if (window.matchMedia && window.matchMedia('(prefers-color-scheme: dark)').matches) {
            document.documentElement.classList.add('dark');
        }
        window.matchMedia('(prefers-color-scheme: dark)').addEventListener('change', event => {
            if (event.matches) {
                document.documentElement.classList.add('dark');
            } else {
                document.documentElement.classList.remove('dark');
            }
        });
    </script>
</head>
<body class="bg-white dark:bg-gray-900 text-gray-800 dark:text-gray-200 min-h-screen">
    <div class="container mx-auto px-4 py-8 max-w-5xl">
        <!-- Header -->
        <header class="mb-8 text-center">
            <h1 class="text-3xl md:text-4xl font-bold text-primary dark:text-primaryLight mb-2">Khung Đo Lường ASO</h1>
            <p class="text-gray-600 dark:text-gray-400">Quy trình tối ưu hóa và đo lường hiệu quả cho App Store Optimization</p>
        </header>

        <!-- Navigation -->
        <div class="mb-8 overflow-x-auto">
            <nav class="flex space-x-1 md:space-x-2 min-w-max">
                <button onclick="showStage('problem')" id="nav-problem" class="nav-btn bg-primary text-white px-3 py-2 rounded-lg text-sm md:text-base">
                    1. Phát hiện vấn đề
                </button>
                <button onclick="showStage('hypothesis')" id="nav-hypothesis" class="nav-btn bg-white dark:bg-gray-800 hover:bg-gray-100 dark:hover:bg-gray-700 px-3 py-2 rounded-lg text-sm md:text-base">
                    2. Đặt giả thiết
                </button>
                <button onclick="showStage('execution')" id="nav-execution" class="nav-btn bg-white dark:bg-gray-800 hover:bg-gray-100 dark:hover:bg-gray-700 px-3 py-2 rounded-lg text-sm md:text-base">
                    3. Thực thi
                </button>
                <button onclick="showStage('measurement')" id="nav-measurement" class="nav-btn bg-white dark:bg-gray-800 hover:bg-gray-100 dark:hover:bg-gray-700 px-3 py-2 rounded-lg text-sm md:text-base">
                    4. Đo lường
                </button>
                <button onclick="showStage('evaluation')" id="nav-evaluation" class="nav-btn bg-white dark:bg-gray-800 hover:bg-gray-100 dark:hover:bg-gray-700 px-3 py-2 rounded-lg text-sm md:text-base">
                    5. Đánh giá
                </button>
            </nav>
        </div>

        <!-- Content sections -->
        <div id="content-container" class="bg-white dark:bg-gray-800 rounded-lg shadow-md p-6">
            <!-- Problem identification section -->
            <div id="problem-section" class="stage-section">
                <h2 class="text-2xl font-bold mb-4 text-primary dark:text-primaryLight">1. Phát Hiện Vấn Đề</h2>
                <p class="mb-4">Giai đoạn này tập trung vào việc xác định các vấn đề hiện tại trong hiệu suất ASO của ứng dụng.</p>
                
                <div class="mb-6">
                    <h3 class="text-xl font-semibold mb-2">Các chỉ số cần phân tích:</h3>
                    <ul class="list-disc pl-5 space-y-1">
                        <li>Lượt hiển thị (Impressions)</li>
                        <li>Lượt tải ứng dụng (Downloads/Conversions)</li>
                        <li>Tỷ lệ chuyển đổi (Conversion Rate)</li>
                        <li>Từ khóa xếp hạng (Keyword Rankings)</li>
                        <li>Đánh giá và xếp hạng sao (Ratings &amp; Reviews)</li>
                        <li>Tỷ lệ rời bỏ (Uninstall Rate)</li>
                    </ul>
                </div>

                <div class="bg-gray-100 dark:bg-gray-700 p-4 rounded-lg mb-6">
                    <h3 class="text-xl font-semibold mb-2">Công cụ thu thập dữ liệu:</h3>
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                        <div>
                            <h4 class="font-medium mb-1">Dữ liệu Console:</h4>
                            <ul class="list-disc pl-5 space-y-1">
                                <li>Google Play Console</li>
                                <li>App Store Connect</li>
                                <li>Firebase Analytics</li>
                            </ul>
                        </div>
                        <div>
                            <h4 class="font-medium mb-1">Công cụ phân tích ASO:</h4>
                            <ul class="list-disc pl-5 space-y-1">
                                <li>App Annie</li>
                                <li>Sensor Tower</li>
                                <li>AppTweak</li>
                                <li>MobileAction</li>
                            </ul>
                        </div>
                    </div>
                </div>

                <form id="problem-form" class="space-y-4 border dark:border-gray-600 rounded-lg p-4">
                    <h3 class="text-xl font-semibold">Ghi nhận vấn đề:</h3>
                    
                    <div>
                        <label class="block text-sm font-medium mb-1">Vấn đề chính được phát hiện:</label>
                        <textarea class="w-full rounded-lg border border-gray-300 dark:border-gray-600 dark:bg-gray-700 p-2 text-base" rows="3" placeholder="Mô tả vấn đề chính..."></textarea>
                    </div>
                    
                    <div>
                        <label class="block text-sm font-medium mb-1">Dữ liệu hỗ trợ:</label>
                        <textarea class="w-full rounded-lg border border-gray-300 dark:border-gray-600 dark:bg-gray-700 p-2 text-base" rows="3" placeholder="Liệt kê dữ liệu chứng minh vấn đề..."></textarea>
                    </div>
                    
                    <div>
                        <label class="block text-sm font-medium mb-1">Mức độ ưu tiên (1-5):</label>
                        <select class="w-full rounded-lg border border-gray-300 dark:border-gray-600 dark:bg-gray-700 p-2 text-base">
                            <option value="1">1 - Thấp</option>
                            <option value="2">2</option>
                            <option value="3">3 - Trung bình</option>
                            <option value="4">4</option>
                            <option value="5">5 - Cao</option>
                        </select>
                    </div>
                    
                    <button type="button" class="bg-primary hover:bg-primaryLight text-white font-medium py-2 px-4 rounded-lg transition duration-300 ease-in-out">
                        Lưu thông tin
                    </button>
                </form>
            </div>

            <!-- Hypothesis section -->
            <div id="hypothesis-section" class="stage-section hidden">
                <h2 class="text-2xl font-bold mb-4 text-primary dark:text-primaryLight">2. Đặt Giả Thiết</h2>
                <p class="mb-4">Dựa trên vấn đề đã xác định, đề xuất các giả thiết về nguyên nhân và giải pháp tiềm năng.</p>
                
                <div class="mb-6">
                    <h3 class="text-xl font-semibold mb-2">Quy trình đặt giả thiết:</h3>
                    <ol class="list-decimal pl-5 space-y-1">
                        <li>Phân tích nguyên nhân gốc rễ</li>
                        <li>Dựa trên dữ liệu để đề xuất các yếu tố ảnh hưởng</li>
                        <li>Xác định các biến có thể thay đổi</li>
                        <li>Dự đoán kết quả khi thay đổi các biến</li>
                        <li>Ưu tiên hóa các giả thiết dựa trên khả năng tác động</li>
                    </ol>
                </div>

                <div class="bg-gray-100 dark:bg-gray-700 p-4 rounded-lg mb-6">
                    <h3 class="text-xl font-semibold mb-2">Các lĩnh vực cần xem xét:</h3>
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                        <div>
                            <h4 class="font-medium mb-1">Tối ưu hóa trang sản phẩm:</h4>
                            <ul class="list-disc pl-5 space-y-1">
                                <li>Tiêu đề ứng dụng</li>
                                <li>Mô tả ngắn và dài</li>
                                <li>Từ khóa và metadata</li>
                                <li>Icon và hình ảnh minh họa</li>
                                <li>Video giới thiệu</li>
                            </ul>
                        </div>
                        <div>
                            <h4 class="font-medium mb-1">Yếu tố hiệu suất:</h4>
                            <ul class="list-disc pl-5 space-y-1">
                                <li>Tổng thể UX/UI của ứng dụng</li>
                                <li>Đánh giá và phản hồi</li>
                                <li>Cập nhật và phát hành</li>
                                <li>Thời điểm quảng cáo</li>
                                <li>Định vị thị trường</li>
                            </ul>
                        </div>
                    </div>
                </div>

                <form id="hypothesis-form" class="space-y-4 border dark:border-gray-600 rounded-lg p-4">
                    <h3 class="text-xl font-semibold">Thiết lập giả thiết:</h3>
                    
                    <div>
                        <label class="block text-sm font-medium mb-1">Giả thiết:</label>
                        <textarea class="w-full rounded-lg border border-gray-300 dark:border-gray-600 dark:bg-gray-700 p-2 text-base" rows="3" placeholder="Nếu [thay đổi X], thì [kết quả Y] sẽ xảy ra vì [lý do Z]..."></textarea>
                    </div>
                    
                    <div>
                        <label class="block text-sm font-medium mb-1">Yếu tố thay đổi:</label>
                        <select class="w-full rounded-lg border border-gray-300 dark:border-gray-600 dark:bg-gray-700 p-2 text-base">
                            <option value="">Chọn yếu tố</option>
                            <option value="title">Tiêu đề ứng dụng</option>
                            <option value="description">Mô tả ứng dụng</option>
                            <option value="keywords">Từ khóa</option>
                            <option value="icon">Icon</option>
                            <option value="screenshots">Hình ảnh minh họa</option>
                            <option value="video">Video giới thiệu</option>
                            <option value="ratings">Đánh giá và phản hồi</option>
                            <option value="other">Khác</option>
                        </select>
                    </div>
                    
                    <div>
                        <label class="block text-sm font-medium mb-1">Kết quả dự kiến:</label>
                        <textarea class="w-full rounded-lg border border-gray-300 dark:border-gray-600 dark:bg-gray-700 p-2 text-base" rows="2" placeholder="Mô tả kết quả mong đợi..."></textarea>
                    </div>
                    
                    <div>
                        <label class="block text-sm font-medium mb-1">Phương pháp kiểm chứng:</label>
                        <textarea class="w-full rounded-lg border border-gray-300 dark:border-gray-600 dark:bg-gray-700 p-2 text-base" rows="2" placeholder="Mô tả cách kiểm chứng giả thiết..."></textarea>
                    </div>
                    
                    <button type="button" class="bg-primary hover:bg-primaryLight text-white font-medium py-2 px-4 rounded-lg transition duration-300 ease-in-out">
                        Lưu giả thiết
                    </button>
                </form>
            </div>

            <!-- Execution section -->
            <div id="execution-section" class="stage-section hidden">
                <h2 class="text-2xl font-bold mb-4 text-primary dark:text-primaryLight">3. Thực Thi</h2>
                <p class="mb-4">Triển khai các thay đổi dựa trên giả thiết đã đặt ra và chuẩn bị cho quá trình đo lường.</p>
                
                <div class="mb-6">
                    <h3 class="text-xl font-semibold mb-2">Các bước thực hiện:</h3>
                    <ol class="list-decimal pl-5 space-y-1">
                        <li>Lập kế hoạch thực hiện chi tiết</li>
                        <li>Chuẩn bị tài nguyên (nội dung, hình ảnh, video...)</li>
                        <li>Triển khai A/B Testing nếu có thể</li>
                        <li>Đảm bảo theo dõi đúng các chỉ số liên quan</li>
                        <li>Ghi chép các thay đổi đã thực hiện</li>
                    </ol>
                </div>

                <div class="bg-gray-100 dark:bg-gray-700 p-4 rounded-lg mb-6">
                    <h3 class="text-xl font-semibold mb-2">Phương pháp triển khai:</h3>
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                        <div>
                            <h4 class="font-medium mb-1">Thay đổi trực tiếp:</h4>
                            <ul class="list-disc pl-5 space-y-1">
                                <li>Cập nhật metadata trên store console</li>
                                <li>Điều chỉnh tài nguyên hình ảnh</li>
                                <li>Phát hành phiên bản cập nhật</li>
                                <li>Triển khai chiến dịch đánh giá</li>
                            </ul>
                        </div>
                        <div>
                            <h4 class="font-medium mb-1">A/B Testing:</h4>
                            <ul class="list-disc pl-5 space-y-1">
                                <li>Google Play Experiments</li>
                                <li>Phân phối theo khu vực/quốc gia</li>
                                <li>Testing theo phân đoạn người dùng</li>
                                <li>Đo lường hiệu suất song song</li>
                            </ul>
                        </div>
                    </div>
                </div>

                <form id="execution-form" class="space-y-4 border dark:border-gray-600 rounded-lg p-4">
                    <h3 class="text-xl font-semibold">Kế hoạch thực thi:</h3>
                    
                    <div>
                        <label class="block text-sm font-medium mb-1">Mô tả thay đổi:</label>
                        <textarea class="w-full rounded-lg border border-gray-300 dark:border-gray-600 dark:bg-gray-700 p-2 text-base" rows="3" placeholder="Mô tả chi tiết thay đổi sẽ thực hiện..."></textarea>
                    </div>
                    
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                        <div>
                            <label class="block text-sm font-medium mb-1">Ngày bắt đầu:</label>
                            <input type="date" class="w-full rounded-lg border border-gray-300 dark:border-gray-600 dark:bg-gray-700 p-2 text-base">
                        </div>
                        <div>
                            <label class="block text-sm font-medium mb-1">Ngày kết thúc dự kiến:</label>
                            <input type="date" class="w-full rounded-lg border border-gray-300 dark:border-gray-600 dark:bg-gray-700 p-2 text-base">
                        </div>
                    </div>
                    
                    <div>
                        <label class="block text-sm font-medium mb-1">Phương pháp triển khai:</label>
                        <select class="w-full rounded-lg border border-gray-300 dark:border-gray-600 dark:bg-gray-700 p-2 text-base">
                            <option value="direct">Thay đổi trực tiếp</option>
                            <option value="ab_testing">A/B Testing</option>
                            <option value="phased">Triển khai theo giai đoạn</option>
                            <option value="regional">Triển khai theo khu vực</option>
                        </select>
                    </div>
                    
                    <div>
                        <label class="block text-sm font-medium mb-1">Người phụ trách:</label>
                        <input type="text" class="w-full rounded-lg border border-gray-300 dark:border-gray-600 dark:bg-gray-700 p-2 text-base" placeholder="Tên người phụ trách">
                    </div>
                    
                    <div>
                        <label class="block text-sm font-medium mb-1">Ghi chú bổ sung:</label>
                        <textarea class="w-full rounded-lg border border-gray-300 dark:border-gray-600 dark:bg-gray-700 p-2 text-base" rows="2" placeholder="Ghi chú bổ sung..."></textarea>
                    </div>
                    
                    <button type="button" class="bg-primary hover:bg-primaryLight text-white font-medium py-2 px-4 rounded-lg transition duration-300 ease-in-out">
                        Lưu kế hoạch
                    </button>
                </form>
            </div>

            <!-- Measurement section -->
            <div id="measurement-section" class="stage-section hidden">
                <h2 class="text-2xl font-bold mb-4 text-primary dark:text-primaryLight">4. Đo Lường</h2>
                <p class="mb-4">Theo dõi và thu thập dữ liệu sau khi thực hiện các thay đổi để đánh giá hiệu quả.</p>
                
                <div class="mb-6">
                    <h3 class="text-xl font-semibold mb-2">Các chỉ số đo lường chính:</h3>
                    <ul class="list-disc pl-5 space-y-1">
                        <li><strong>Hiển thị (Impressions):</strong> Số lần ứng dụng xuất hiện trong kết quả tìm kiếm/danh mục</li>
                        <li><strong>Lượt tải (Downloads):</strong> Số lần ứng dụng được tải xuống</li>
                        <li><strong>Tỷ lệ chuyển đổi (CVR):</strong> Tỷ lệ người dùng tải ứng dụng sau khi xem trang</li>
                        <li><strong>Thứ hạng từ khóa:</strong> Vị trí xếp hạng cho các từ khóa mục tiêu</li>
                        <li><strong>Ratings &amp; Reviews:</strong> Số lượng và chất lượng đánh giá</li>
                    </ul>
                </div>

                <div class="bg-gray-100 dark:bg-gray-700 p-4 rounded-lg mb-6">
                    <h3 class="text-xl font-semibold mb-2">Phương pháp đo lường:</h3>
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                        <div>
                            <h4 class="font-medium mb-1">Đo lường trước-sau:</h4>
                            <ul class="list-disc pl-5 space-y-1">
                                <li>Thiết lập baseline dữ liệu</li>
                                <li>Thu thập dữ liệu sau thay đổi</li>
                                <li>So sánh sự khác biệt</li>
                                <li>Phân tích xu hướng dài hạn</li>
                            </ul>
                        </div>
                        <div>
                            <h4 class="font-medium mb-1">Đo lường A/B Testing:</h4>
                            <ul class="list-disc pl-5 space-y-1">
                                <li>Theo dõi biến thể A vs B</li>
                                <li>Đánh giá sự khác biệt thống kê</li>
                                <li>Ưu tiên các chỉ số quan trọng</li>
                                <li>Phát hiện biến số can thiệp</li>
                            </ul>
                        </div>
                    </div>
                </div>

                <form id="measurement-form" class="space-y-4 border dark:border-gray-600 rounded-lg p-4">
                    <h3 class="text-xl font-semibold">Theo dõi chỉ số:</h3>
                    
                    <div class="grid grid-cols-2 gap-4">
                        <div>
                            <label class="block text-sm font-medium mb-1">Khoảng thời gian:</label>
                            <select class="w-full rounded-lg border border-gray-300 dark:border-gray-600 dark:bg-gray-700 p-2 text-base">
                                <option value="7days">7 ngày</option>
                                <option value="14days">14 ngày</option>
                                <option value="30days">30 ngày</option>
                                <option value="custom">Tùy chỉnh</option>
                            </select>
                        </div>
                        <div>
                            <label class="block text-sm font-medium mb-1">So sánh với:</label>
                            <select class="w-full rounded-lg border border-gray-300 dark:border-gray-600 dark:bg-gray-700 p-2 text-base">
                                <option value="previous">Kỳ trước</option>
                                <option value="baseline">Dữ liệu cơ sở</option>
                                <option value="yoy">Cùng kỳ năm trước</option>
                                <option value="variant">Biến thể khác</option>
                            </select>
                        </div>
                    </div>
                    
                    <div class="overflow-x-auto">
                        <table class="min-w-full border-collapse">
                            <thead>
                                <tr class="bg-gray-50 dark:bg-gray-700">
                                    <th class="px-4 py-2 text-left border dark:border-gray-600">Chỉ số</th>
                                    <th class="px-4 py-2 text-left border dark:border-gray-600">Trước</th>
                                    <th class="px-4 py-2 text-left border dark:border-gray-600">Sau</th>
                                    <th class="px-4 py-2 text-left border dark:border-gray-600">% Thay đổi</th>
                                </tr>
                            </thead>
                            <tbody>
                                <tr>
                                    <td class="px-4 py-2 border dark:border-gray-600">Impressions</td>
                                    <td class="px-4 py-2 border dark:border-gray-600">
                                        <input type="number" class="w-full p-1 rounded border-gray-300 dark:border-gray-600 dark:bg-gray-700 text-base">
                                    </td>
                                    <td class="px-4 py-2 border dark:border-gray-600">
                                        <input type="number" class="w-full p-1 rounded border-gray-300 dark:border-gray-600 dark:bg-gray-700 text-base">
                                    </td>
                                    <td class="px-4 py-2 border dark:border-gray-600" id="impressions-change">-</td>
                                </tr>
                                <tr>
                                    <td class="px-4 py-2 border dark:border-gray-600">Downloads</td>
                                    <td class="px-4 py-2 border dark:border-gray-600">
                                        <input type="number" class="w-full p-1 rounded border-gray-300 dark:border-gray-600 dark:bg-gray-700 text-base">
                                    </td>
                                    <td class="px-4 py-2 border dark:border-gray-600">
                                        <input type="number" class="w-full p-1 rounded border-gray-300 dark:border-gray-600 dark:bg-gray-700 text-base">
                                    </td>
                                    <td class="px-4 py-2 border dark:border-gray-600" id="downloads-change">-</td>
                                </tr>
                                <tr>
                                    <td class="px-4 py-2 border dark:border-gray-600">Conversion Rate (%)</td>
                                    <td class="px-4 py-2 border dark:border-gray-600">
                                        <input type="number" step="0.01" class="w-full p-1 rounded border-gray-300 dark:border-gray-600 dark:bg-gray-700 text-base">
                                    </td>
                                    <td class="px-4 py-2 border dark:border-gray-600">
                                        <input type="number" step="0.01" class="w-full p-1 rounded border-gray-300 dark:border-gray-600 dark:bg-gray-700 text-base">
                                    </td>
                                    <td class="px-4 py-2 border dark:border-gray-600" id="cvr-change">-</td>
                                </tr>
                                <tr>
                                    <td class="px-4 py-2 border dark:border-gray-600">
                                        <input type="text" placeholder="Chỉ số khác..." class="w-full p-1 rounded border-gray-300 dark:border-gray-600 dark:bg-gray-700 text-base">
                                    </td>
                                    <td class="px-4 py-2 border dark:border-gray-600">
                                        <input type="number" class="w-full p-1 rounded border-gray-300 dark:border-gray-600 dark:bg-gray-700 text-base">
                                    </td>
                                    <td class="px-4 py-2 border dark:border-gray-600">
                                        <input type="number" class="w-full p-1 rounded border-gray-300 dark:border-gray-600 dark:bg-gray-700 text-base">
                                    </td>
                                    <td class="px-4 py-2 border dark:border-gray-600">-</td>
                                </tr>
                            </tbody>
                        </table>
                    </div>
                    
                    <div>
                        <label class="block text-sm font-medium mb-1">Ghi chú về các nhân tố bên ngoài:</label>
                        <textarea class="w-full rounded-lg border border-gray-300 dark:border-gray-600 dark:bg-gray-700 p-2 text-base" rows="2" placeholder="Các yếu tố bên ngoài có thể ảnh hưởng đến kết quả..."></textarea>
                    </div>
                    
                    <button type="button" class="bg-primary hover:bg-primaryLight text-white font-medium py-2 px-4 rounded-lg transition duration-300 ease-in-out">
                        Tính toán &amp; Lưu
                    </button>
                </form>
            </div>

            <!-- Evaluation section -->
            <div id="evaluation-section" class="stage-section hidden">
                <h2 class="text-2xl font-bold mb-4 text-primary dark:text-primaryLight">5. Đánh Giá</h2>
                <p class="mb-4">Phân tích kết quả đo lường, đánh giá hiệu quả của các thay đổi đã thực hiện và lập kế hoạch tiếp theo.</p>
                
                <div class="mb-6">
                    <h3 class="text-xl font-semibold mb-2">Quy trình đánh giá:</h3>
                    <ol class="list-decimal pl-5 space-y-1">
                        <li>Đánh giá mức độ thay đổi của các chỉ số</li>
                        <li>Xác định mối tương quan giữa các thay đổi và kết quả</li>
                        <li>Xác nhận hoặc bác bỏ giả thiết ban đầu</li>
                        <li>Đánh giá ý nghĩa thống kê và thực tiễn</li>
                        <li>Đề xuất hành động tiếp theo</li>
                    </ol>
                </div>

                <div class="bg-gray-100 dark:bg-gray-700 p-4 rounded-lg mb-6">
                    <h3 class="text-xl font-semibold mb-2">Phương pháp đánh giá:</h3>
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                        <div>
                            <h4 class="font-medium mb-1">Định lượng:</h4>
                            <ul class="list-disc pl-5 space-y-1">
                                <li>Phân tích thống kê</li>
                                <li>So sánh ROI</li>
                                <li>Đánh giá chi phí-lợi ích</li>
                                <li>Dự báo dài hạn</li>
                            </ul>
                        </div>
                        <div>
                            <h4 class="font-medium mb-1">Định tính:</h4>
                            <ul class="list-disc pl-5 space-y-1">
                                <li>Phân tích phản hồi người dùng</li>
                                <li>Đánh giá tác động thương hiệu</li>
                                <li>So sánh với đối thủ</li>
                                <li>Tính khả thi của triển khai rộng rãi</li>
                            </ul>
                        </div>
                    </div>
                </div>

                <form id="evaluation-form" class="space-y-4 border dark:border-gray-600 rounded-lg p-4">
                    <h3 class="text-xl font-semibold">Đánh giá kết quả:</h3>
                    
                    <div>
                        <label class="block text-sm font-medium mb-1">Kết quả tổng thể:</label>
                        <select class="w-full rounded-lg border border-gray-300 dark:border-gray-600 dark:bg-gray-700 p-2 text-base">
                            <option value="very_positive">Rất tích cực</option>
                            <option value="positive">Tích cực</option>
                            <option value="neutral">Trung tính</option>
                            <option value="negative">Tiêu cực</option>
                            <option value="very_negative">Rất tiêu cực</option>
                        </select>
                    </div>
                    
                    <div>
                        <label class="block text-sm font-medium mb-1">Đánh giá chi tiết:</label>
                        <textarea class="w-full rounded-lg border border-gray-300 dark:border-gray-600 dark:bg-gray-700 p-2 text-base" rows="3" placeholder="Đánh giá chi tiết về kết quả..."></textarea>
                    </div>
                    
                    <div>
                        <label class="block text-sm font-medium mb-1">Kết luận về giả thiết:</label>
                        <select class="w-full rounded-lg border border-gray-300 dark:border-gray-600 dark:bg-gray-700 p-2 text-base">
                            <option value="confirmed">Xác nhận giả thiết</option>
                            <option value="partially_confirmed">Xác nhận một phần</option>
                            <option value="inconclusive">Chưa có kết luận rõ ràng</option>
                            <option value="rejected">Bác bỏ giả thiết</option>
                        </select>
                    </div>
                    
                    <div>
                        <label class="block text-sm font-medium mb-1">Bài học kinh nghiệm:</label>
                        <textarea class="w-full rounded-lg border border-gray-300 dark:border-gray-600 dark:bg-gray-700 p-2 text-base" rows="2" placeholder="Những bài học rút ra từ quá trình này..."></textarea>
                    </div>
                    
                    <div>
                        <label class="block text-sm font-medium mb-1">Hành động tiếp theo:</label>
                        <textarea class="w-full rounded-lg border border-gray-300 dark:border-gray-600 dark:bg-gray-700 p-2 text-base" rows="3" placeholder="Kế hoạch hành động tiếp theo..."></textarea>
                    </div>
                    
                    <button type="button" class="bg-primary hover:bg-primaryLight text-white font-medium py-2 px-4 rounded-lg transition duration-300 ease-in-out">
                        Hoàn tất đánh giá
                    </button>
                </form>
            </div>
        </div>
        
        <!-- Navigation buttons -->
        <div class="mt-6 flex justify-between">
            <button id="prev-btn" class="bg-gray-200 dark:bg-gray-700 hover:bg-gray-300 dark:hover:bg-gray-600 text-gray-800 dark:text-gray-200 font-medium py-2 px-4 rounded-lg transition duration-300 ease-in-out" onclick="navigatePrev()">
                <span>← Trước</span>
            </button>
            <button id="next-btn" class="bg-primary hover:bg-primaryLight text-white font-medium py-2 px-4 rounded-lg transition duration-300 ease-in-out" onclick="navigateNext()">
                <span>Tiếp theo →</span>
            </button>
        </div>
    </div>

    <script>
        // State management
        let currentStage = 'problem';
        const stages = ['problem', 'hypothesis', 'execution', 'measurement', 'evaluation'];
        
        // Show selected stage
        function showStage(stage) {
            // Hide all sections
            document.querySelectorAll('.stage-section').forEach(section => {
                section.classList.add('hidden');
            });
            
            // Show selected section
            document.getElementById(`${stage}-section`).classList.remove('hidden');
            
            // Update navigation buttons
            document.querySelectorAll('.nav-btn').forEach(btn => {
                btn.classList.remove('bg-primary', 'text-white');
                btn.classList.add('bg-white', 'dark:bg-gray-800', 'hover:bg-gray-100', 'dark:hover:bg-gray-700');
            });
            
            document.getElementById(`nav-${stage}`).classList.remove('bg-white', 'dark:bg-gray-800', 'hover:bg-gray-100', 'dark:hover:bg-gray-700');
            document.getElementById(`nav-${stage}`).classList.add('bg-primary', 'text-white');
            
            // Update current stage
            currentStage = stage;
            
            // Update prev/next buttons
            updateNavButtons();
        }
        
        // Navigate to previous stage
        function navigatePrev() {
            const currentIndex = stages.indexOf(currentStage);
            if (currentIndex > 0) {
                showStage(stages[currentIndex - 1]);
            }
        }
        
        // Navigate to next stage
        function navigateNext() {
            const currentIndex = stages.indexOf(currentStage);
            if (currentIndex < stages.length - 1) {
                showStage(stages[currentIndex + 1]);
            }
        }
        
        // Update navigation buttons state
        function updateNavButtons() {
            const currentIndex = stages.indexOf(currentStage);
            const prevBtn = document.getElementById('prev-btn');
            const nextBtn = document.getElementById('next-btn');
            
            // Disable/enable previous button
            if (currentIndex === 0) {
                prevBtn.disabled = true;
                prevBtn.classList.add('opacity-50', 'cursor-not-allowed');
            } else {
                prevBtn.disabled = false;
                prevBtn.classList.remove('opacity-50', 'cursor-not-allowed');
            }
            
            // Update next button text for last stage
            if (currentIndex === stages.length - 1) {
                nextBtn.querySelector('span').textContent = 'Hoàn tất';
            } else {
                nextBtn.querySelector('span').textContent = 'Tiếp theo →';
            }
        }
        
        // Set up change calculations for measurement form
        document.querySelectorAll('#measurement-form input[type="number"]').forEach(input => {
            input.addEventListener('input', calculateChanges);
        });
        
        function calculateChanges() {
            const rows = document.querySelectorAll('#measurement-form tbody tr');
            
            rows.forEach(row => {
                const before = parseFloat(row.querySelector('td:nth-child(2) input').value);
                const after = parseFloat(row.querySelector('td:nth-child(3) input').value);
                const changeCell = row.querySelector('td:nth-child(4)');
                
                if (!isNaN(before) && !isNaN(after) && before !== 0) {
                    const changePercent = ((after - before) / before * 100).toFixed(2);
                    const isPositive = changePercent > 0;
                    
                    changeCell.textContent = `${changePercent}%`;
                    changeCell.classList.remove('text-green-600', 'text-red-600');
                    changeCell.classList.add(isPositive ? 'text-green-600' : 'text-red-600');
                } else {
                    changeCell.textContent = '-';
                    changeCell.classList.remove('text-green-600', 'text-red-600');
                }
            });
        }
        
        // Initialize
        showStage('problem');
    </script>


</body></html>
