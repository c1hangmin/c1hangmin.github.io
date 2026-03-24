<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Infra Tech Log | Study Notes</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Noto+Sans+KR:wght@300;400;500;700&display=swap');
        body {
            font-family: 'Noto Sans KR', sans-serif;
            background-color: #0f172a; /* Tailwind slate-900 */
            color: #f8fafc; /* Tailwind slate-50 */
        }
        .post-card:hover h3 {
            color: #3b82f6; /* text-blue-500 */
        }
    </style>
</head>
<body class="antialiased selection:bg-blue-500 selection:text-white">

    <!-- Header / Hero Section -->
    <header class="bg-slate-900 border-b border-slate-800 pt-20 pb-16 px-6">
        <div class="max-w-5xl mx-auto">
            <h1 class="text-4xl md:text-6xl font-bold mb-4 tracking-tight">
                <i class="fas fa-terminal text-blue-500 mr-3"></i>Infra Tech Log
            </h1>
            <p class="text-lg md:text-xl text-slate-400 max-w-2xl leading-relaxed">
                네트워크 인프라 구축, 트러블슈팅, 보안 솔루션 운영 과정에서 <br class="hidden md:block">
                새롭게 배우고 고민한 기술 요소들을 기록하는 공간입니다.
            </p>
            
            <!-- Search Bar (UI Only) -->
            <div class="mt-8 relative max-w-md">
                <input type="text" placeholder="검색어 입력 (예: OSPF, 방화벽, Linux)" class="w-full bg-slate-800 text-slate-200 border border-slate-700 rounded-lg py-3 pl-10 pr-4 focus:outline-none focus:border-blue-500 focus:ring-1 focus:ring-blue-500 transition-colors">
                <i class="fas fa-search absolute left-4 top-3.5 text-slate-500"></i>
            </div>
        </div>
    </header>

    <!-- Main Content -->
    <main class="max-w-5xl mx-auto px-6 py-12 flex flex-col md:flex-row gap-12">

        <!-- Left Column: Posts List -->
        <div class="md:w-2/3 space-y-8">
            <h2 class="text-2xl font-bold border-b border-slate-700 pb-3 mb-6 flex items-center gap-2 text-slate-100">
                <i class="fas fa-book-open text-blue-400"></i> 최근 학습 노트
            </h2>

            <!-- Mock Post 1 -->
            <article class="post-card bg-slate-800 p-6 rounded-xl border border-slate-700 hover:border-slate-500 transition-all cursor-pointer">
                <div class="flex items-center gap-3 mb-3">
                    <span class="bg-blue-900/50 text-blue-400 text-xs font-semibold px-2.5 py-1 rounded">Network</span>
                    <span class="text-slate-500 text-sm"><i class="far fa-calendar-alt mr-1"></i> 2026.03.20</span>
                </div>
                <h3 class="text-xl font-bold text-white mb-2 transition-colors">OSPF Multi-Area 구성 및 경로 최적화 실습</h3>
                <p class="text-slate-400 text-sm leading-relaxed mb-4 line-clamp-2">
                    단일 에어리어에서 발생하는 LSA Flooding 부하를 줄이기 위해 Multi-Area OSPF를 구성해보았습니다. ABR 라우터에서의 축약 설정과 Stub 에어리어 지정에 따른 라우팅 테이블 변화를 분석합니다.
                </p>
                <div class="flex gap-2 text-xs text-slate-500">
                    <span>#Cisco</span>
                    <span>#Routing</span>
                    <span>#OSPF</span>
                </div>
            </article>

            <!-- Mock Post 2 -->
            <article class="post-card bg-slate-800 p-6 rounded-xl border border-slate-700 hover:border-slate-500 transition-all cursor-pointer">
                <div class="flex items-center gap-3 mb-3">
                    <span class="bg-red-900/50 text-red-400 text-xs font-semibold px-2.5 py-1 rounded">Security</span>
                    <span class="text-slate-500 text-sm"><i class="far fa-calendar-alt mr-1"></i> 2026.03.15</span>
                </div>
                <h3 class="text-xl font-bold text-white mb-2 transition-colors">엔드포인트 보안 강화를 위한 NAC 차단 정책 구성</h3>
                <p class="text-slate-400 text-sm leading-relaxed mb-4 line-clamp-2">
                    IPScanNAC 환경에서 비인가 단말의 네트워크 접근을 차단하고, 필수 보안 소프트웨어 미설치 PC를 격리망으로 이동시키는 정책 수립 과정을 정리했습니다.
                </p>
                <div class="flex gap-2 text-xs text-slate-500">
                    <span>#NAC</span>
                    <span>#Endpoint_Security</span>
                </div>
            </article>

            <!-- Mock Post 3 -->
            <article class="post-card bg-slate-800 p-6 rounded-xl border border-slate-700 hover:border-slate-500 transition-all cursor-pointer">
                <div class="flex items-center gap-3 mb-3">
                    <span class="bg-green-900/50 text-green-400 text-xs font-semibold px-2.5 py-1 rounded">System</span>
                    <span class="text-slate-500 text-sm"><i class="far fa-calendar-alt mr-1"></i> 2026.03.10</span>
                </div>
                <h3 class="text-xl font-bold text-white mb-2 transition-colors">Linux 네트워크 인터페이스 본딩(Bonding) 설정</h3>
                <p class="text-slate-400 text-sm leading-relaxed mb-4 line-clamp-2">
                    서버의 네트워크 가용성을 높이기 위해 CentOS 환경에서 NIC 2개를 Active-Standby (Mode 1) 방식으로 묶는 과정을 스크립트와 함께 기록합니다.
                </p>
                <div class="flex gap-2 text-xs text-slate-500">
                    <span>#Linux</span>
                    <span>#Bonding</span>
                    <span>#고가용성</span>
                </div>
            </article>

            <!-- Mock Post 4 -->
            <article class="post-card bg-slate-800 p-6 rounded-xl border border-slate-700 hover:border-slate-500 transition-all cursor-pointer">
                <div class="flex items-center gap-3 mb-3">
                    <span class="bg-yellow-900/50 text-yellow-400 text-xs font-semibold px-2.5 py-1 rounded">Troubleshooting</span>
                    <span class="text-slate-500 text-sm"><i class="far fa-calendar-alt mr-1"></i> 2026.03.01</span>
                </div>
                <h3 class="text-xl font-bold text-white mb-2 transition-colors">L2 스위치 루핑(Looping) 장애 발생 및 조치 내역</h3>
                <p class="text-slate-400 text-sm leading-relaxed mb-4 line-clamp-2">
                    필드 환경에서 발생한 브로드캐스트 스톰으로 인한 통신 마비 상황. STP(Spanning Tree Protocol) 설정 누락을 확인하고 BPDU Guard를 적용하여 해결한 사례입니다.
                </p>
                <div class="flex gap-2 text-xs text-slate-500">
                    <span>#Switching</span>
                    <span>#STP</span>
                    <span>#장애조치</span>
                </div>
            </article>
            
            <button class="w-full py-3 mt-4 border border-slate-700 text-slate-400 rounded-lg hover:bg-slate-800 hover:text-white transition-colors">
                더 많은 글 보기
            </button>
        </div>

        <!-- Right Column: Sidebar (Categories & Tags) -->
        <aside class="md:w-1/3 space-y-8">
            
            <!-- Categories -->
            <div class="bg-slate-800 rounded-xl border border-slate-700 p-6">
                <h3 class="text-lg font-bold text-white mb-4 border-b border-slate-700 pb-2">
                    <i class="fas fa-folder-open mr-2 text-slate-400"></i> Categories
                </h3>
                <ul class="space-y-3">
                    <li>
                        <a href="#" class="flex justify-between items-center text-slate-300 hover:text-blue-400 transition-colors">
                            <span><i class="fas fa-network-wired w-6 text-center"></i> Network (L2/L3)</span>
                            <span class="bg-slate-900 text-xs py-1 px-2 rounded">12</span>
                        </a>
                    </li>
                    <li>
                        <a href="#" class="flex justify-between items-center text-slate-300 hover:text-blue-400 transition-colors">
                            <span><i class="fas fa-shield-alt w-6 text-center"></i> Security & NAC</span>
                            <span class="bg-slate-900 text-xs py-1 px-2 rounded">8</span>
                        </a>
                    </li>
                    <li>
                        <a href="#" class="flex justify-between items-center text-slate-300 hover:text-blue-400 transition-colors">
                            <span><i class="fab fa-linux w-6 text-center"></i> System & Linux</span>
                            <span class="bg-slate-900 text-xs py-1 px-2 rounded">5</span>
                        </a>
                    </li>
                    <li>
                        <a href="#" class="flex justify-between items-center text-slate-300 hover:text-blue-400 transition-colors">
                            <span><i class="fas fa-tools w-6 text-center"></i> Troubleshooting</span>
                            <span class="bg-slate-900 text-xs py-1 px-2 rounded">15</span>
                        </a>
                    </li>
                </ul>
            </div>

            <!-- Popular Tags -->
            <div class="bg-slate-800 rounded-xl border border-slate-700 p-6">
                <h3 class="text-lg font-bold text-white mb-4 border-b border-slate-700 pb-2">
                    <i class="fas fa-hashtag mr-2 text-slate-400"></i> Tags
                </h3>
                <div class="flex flex-wrap gap-2">
                    <span class="px-3 py-1 bg-slate-900 text-slate-300 text-sm rounded-full border border-slate-700 cursor-pointer hover:border-blue-500 hover:text-blue-400 transition-colors">Cisco</span>
                    <span class="px-3 py-1 bg-slate-900 text-slate-300 text-sm rounded-full border border-slate-700 cursor-pointer hover:border-blue-500 hover:text-blue-400 transition-colors">Alcatel</span>
                    <span class="px-3 py-1 bg-slate-900 text-slate-300 text-sm rounded-full border border-slate-700 cursor-pointer hover:border-blue-500 hover:text-blue-400 transition-colors">Firewall</span>
                    <span class="px-3 py-1 bg-slate-900 text-slate-300 text-sm rounded-full border border-slate-700 cursor-pointer hover:border-blue-500 hover:text-blue-400 transition-colors">VLAN</span>
                    <span class="px-3 py-1 bg-slate-900 text-slate-300 text-sm rounded-full border border-slate-700 cursor-pointer hover:border-blue-500 hover:text-blue-400 transition-colors">OSPF</span>
                    <span class="px-3 py-1 bg-slate-900 text-slate-300 text-sm rounded-full border border-slate-700 cursor-pointer hover:border-blue-500 hover:text-blue-400 transition-colors">IPScan</span>
                    <span class="px-3 py-1 bg-slate-900 text-slate-300 text-sm rounded-full border border-slate-700 cursor-pointer hover:border-blue-500 hover:text-blue-400 transition-colors">CentOS</span>
                </div>
            </div>

            <!-- GitHub Link Button -->
            <a href="https://github.com" target="_blank" class="block w-full text-center bg-slate-800 hover:bg-slate-700 text-white font-medium py-3 rounded-xl border border-slate-700 transition-colors">
                <i class="fab fa-github mr-2"></i> GitHub 저장소 가기
            </a>
            
        </aside>

    </main>

    <!-- Footer -->
    <footer class="bg-slate-900 py-8 text-center text-slate-500 border-t border-slate-800 mt-12">
        <p>© 2026 Infra Tech Log. All rights reserved.</p>
        <p class="text-sm mt-2">Powered by GitHub Pages</p>
    </footer>

</body>
</html>
