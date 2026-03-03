# friday18pm.github.io
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>저희 결혼합니다</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Noto+Serif+KR:wght@300;400&family=Gowun+Batang&display=swap" rel="stylesheet">
    <style>
        body { font-family: 'Gowun Batang', serif; background-color: #fcfaf7; color: #4a4a4a; }
        .fade-in { opacity: 0; transform: translateY(20px); transition: all 1s ease-out; }
        .fade-in.visible { opacity: 1; transform: translateY(0); }
        .bg-main { background: url('https://images.unsplash.com/photo-1511285560929-80b456fea0bc?q=80&w=2069&auto=format&fit=crop') center/cover; height: 80vh; }
    </style>
</head>
<body>

    <section class="relative flex flex-col items-center justify-end pb-20 bg-main text-white text-center">
        <div class="absolute inset-0 bg-black/20"></div>
        <div class="relative z-10">
            <p class="text-lg tracking-widest mb-2">MARRY ME</p>
            <h1 class="text-4xl mb-4 font-light">신랑 & 신부</h1>
            <p class="text-sm">2026. 05. 23. SAT PM 12:30</p>
        </div>
    </section>

    <section class="py-20 px-8 text-center fade-in">
        <h2 class="text-xl mb-10 text-stone-500 tracking-widest uppercase">Invitation</h2>
        <p class="leading-loose text-stone-600">
            서로가 마주 보며 다진 약속,<br>
            함께 걸어가는 첫걸음에<br>
            소중한 분들을 초대합니다.<br><br>
            저희의 시작을 따뜻한 마음으로<br>
            축복해 주시면 감사하겠습니다.
        </p>
        <div class="mt-12 border-t border-stone-200 pt-8">
            <p class="text-lg">김철수 · 박영희 <span class="text-xs text-stone-400 mx-2">의 아들</span> <b>신랑</b></p>
            <p class="text-lg mt-2">이영남 · 최순자 <span class="text-xs text-stone-400 mx-2">의 딸</span> <b>신부</b></p>
        </div>
    </section>

    <section class="bg-stone-100 py-16 px-4 fade-in">
        <h2 class="text-center text-xl mb-8 text-stone-500 tracking-widest">GALLERY</h2>
        <div class="grid grid-cols-2 gap-2">
            <div class="bg-white h-40 overflow-hidden"><img src="https://images.unsplash.com/photo-1519741497674-611481863552?w=500&auto=format" class="w-full h-full object-cover"></div>
            <div class="bg-white h-40 overflow-hidden"><img src="https://images.unsplash.com/photo-1583939003579-730e3918a45a?w=500&auto=format" class="w-full h-full object-cover"></div>
            <div class="bg-white h-40 overflow-hidden col-span-2"><img src="https://images.unsplash.com/photo-1515934751635-c81c6bc9a2d8?w=800&auto=format" class="w-full h-full object-cover"></div>
        </div>
    </section>

    <section class="py-20 px-8 text-center fade-in">
        <h2 class="text-xl mb-6 text-stone-500 tracking-widest">LOCATION</h2>
        <p class="text-lg font-bold">서울 웨딩 컨벤션 1층 그랜드홀</p>
        <p class="text-sm text-stone-500 mt-2">서울 강남구 테헤란로 123</p>
        <div class="mt-8 flex justify-center gap-4">
            <a href="#" class="px-6 py-2 border border-stone-300 text-sm rounded-full">네이버 지도</a>
            <a href="#" class="px-6 py-2 border border-stone-300 text-sm rounded-full">카카오 내비</a>
        </div>
    </section>

    <section class="py-16 bg-stone-50 px-8 fade-in">
        <h2 class="text-center text-lg mb-8 text-stone-500">마음 전하실 곳</h2>
        <div class="space-y-4">
            <div class="bg-white p-5 rounded-lg shadow-sm flex justify-between items-center">
                <div>
                    <p class="text-xs text-stone-400">신랑측 계좌</p>
                    <p class="text-sm">국민은행 123-4567-890</p>
                </div>
                <button onclick="copyToClipboard('123-4567-890')" class="text-xs bg-stone-200 px-3 py-1 rounded">복사</button>
            </div>
            <div class="bg-white p-5 rounded-lg shadow-sm flex justify-between items-center">
                <div>
                    <p class="text-xs text-stone-400">신부측 계좌</p>
                    <p class="text-sm">신한은행 098-765-4321</p>
                </div>
                <button onclick="copyToClipboard('098-765-4321')" class="text-xs bg-stone-200 px-3 py-1 rounded">복사</button>
            </div>
        </div>
    </section>

    <footer class="py-10 text-center text-xs text-stone-400">
        Copyright © 2026. 신랑 & 신부 All rights reserved.
    </footer>

    <script>
        // 스크롤 애니메이션
        const observerOptions = { threshold: 0.1 };
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) entry.target.classList.add('visible');
            });
        }, observerOptions);

        document.querySelectorAll('.fade-in').forEach(el => observer.observe(el));

        // 복사 기능
        function copyToClipboard(text) {
            navigator.clipboard.writeText(text).then(() => {
                alert('계좌번호가 복사되었습니다.');
            });
        }
    </script>
</body>
</html>
