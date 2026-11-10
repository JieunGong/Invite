<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>🎉 연말 홈파티 초대장 & 날짜 투표</title>
  <!-- Tailwind CSS CDN -->
  <script src="https://cdn.tailwindcss.com"></script>

  <style>
    /* Font Family Setup: Clear & Crisp Malgun Gothic Bold */
    body, input, textarea, button {
      font-family: '맑은 고딕', 'Malgun Gothic', 'Apple SD Gothic Neo', sans-serif !important;
      letter-spacing: -0.02em;
    }
    .font-headline {
      font-family: '맑은 고딕', 'Malgun Gothic', 'Apple SD Gothic Neo', sans-serif !important;
      font-weight: 800;
    }
    .font-body {
      font-family: '맑은 고딕', 'Malgun Gothic', 'Apple SD Gothic Neo', sans-serif !important;
      font-weight: 700;
    }

    /* Custom Animation & Shadows */
    @keyframes bounce-gentle {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-8px); }
    }
    .animate-bounce-gentle {
      animation: bounce-gentle 2s infinite ease-in-out;
    }

    .card-shadow {
      box-shadow: 0 10px 25px -5px rgba(239, 68, 68, 0.15), 0 8px 10px -6px rgba(0, 0, 0, 0.1);
    }
  </style>
</head>
<body class="bg-gradient-to-br from-pink-200 via-amber-100 to-pink-100 min-h-screen font-body text-gray-900 flex flex-col justify-between p-4 sm:p-6">

  <!-- Header Container -->
  <header class="w-full max-w-lg mx-auto text-center pt-4 pb-2">
    <div class="inline-block bg-red-500 text-white font-headline text-xs sm:text-sm px-4 py-1.5 rounded-full shadow-md mb-2 animate-bounce-gentle">
      💌 HOME PARTY INVITATION
    </div>
    <h1 class="font-headline text-3xl sm:text-4xl text-red-600 drop-shadow-sm tracking-wide font-extrabold">
      🎉 연말 홈파티 초대장
    </h1>
    <p class="text-xs sm:text-sm text-gray-800 mt-1 font-bold">우리만의 신나는 홈파티! 편한 날짜를 알려주세요 🍕🥂</p>
  </header>

  <!-- Main Content Card Dynamic Views -->
  <main class="w-full max-w-md mx-auto my-auto bg-white/95 backdrop-blur-sm rounded-3xl p-6 sm:p-8 card-shadow border-4 border-pink-300 transition-all duration-300">

    <!-- STEP 1: Name Input -->
    <section id="step-1" class="space-y-6">
      <div class="text-center space-y-2">
        <span class="text-5xl">👋</span>
        <h2 class="font-headline text-2xl text-gray-900 font-extrabold">반가워요! 이름이 어떻게 되나요?</h2>
        <p class="text-sm text-gray-700 font-bold">설문조사를 시작하기 위해 이름을 입력해주세요.</p>
      </div>

      <div class="space-y-4">
        <div>
          <label for="guest-name" class="block font-headline text-sm text-red-600 mb-1">참석자 이름</label>
          <input type="text" id="guest-name" placeholder="예: 홍길동" class="w-full px-4 py-3 rounded-2xl border-2 border-pink-300 focus:border-red-500 focus:outline-none focus:ring-2 focus:ring-red-200 text-gray-900 font-bold placeholder-gray-400 text-base transition-colors">
        </div>
        <button id="btn-to-step-2" class="w-full bg-red-500 hover:bg-red-600 active:scale-95 text-white font-headline text-lg py-3.5 px-6 rounded-2xl shadow-lg hover:shadow-xl transition-all duration-200 flex items-center justify-center gap-2">
          다음으로 ➔
        </button>
      </div>
      
      <div class="text-center pt-2">
        <button id="btn-open-admin-modal" class="text-xs text-gray-600 hover:text-red-600 underline underline-offset-4 font-bold">
          🔒 주최자 전용 (결과 보기)
        </button>
      </div>
    </section>

    <!-- STEP 2: Date Vote & Extra Comments -->
    <section id="step-2" class="hidden space-y-6">
      <div class="flex items-center justify-between border-b-2 border-pink-100 pb-3">
        <span class="font-headline text-sm text-red-600 font-extrabold" id="display-guest-name"></span>
        <button id="btn-back-to-step-1" class="text-xs text-gray-600 hover:text-gray-900 underline font-bold">이름 수정</button>
      </div>

      <div class="space-y-2">
        <h2 class="font-headline text-xl sm:text-2xl text-gray-900 font-extrabold">📅 가능한 날짜를 선택해주세요</h2>
        <p class="text-xs sm:text-sm text-gray-700 font-bold">중복 선택이 가능해요! 많이 찍어줄수록 좋아요 👍</p>
      </div>

      <!-- Checkboxes -->
      <div class="space-y-3">
        <label class="flex items-center p-3.5 rounded-2xl border-2 border-pink-200 hover:border-red-400 bg-pink-50/60 cursor-pointer transition-all">
          <input type="checkbox" value="12월 13일" class="date-checkbox w-5 h-5 text-red-500 accent-red-500 rounded focus:ring-red-400">
          <span class="ml-3 font-headline text-gray-900 text-base sm:text-lg font-bold">12월 13일 (금)</span>
        </label>

        <label class="flex items-center p-3.5 rounded-2xl border-2 border-pink-200 hover:border-red-400 bg-pink-50/60 cursor-pointer transition-all">
          <input type="checkbox" value="12월 19일" class="date-checkbox w-5 h-5 text-red-500 accent-red-500 rounded focus:ring-red-400">
          <span class="ml-3 font-headline text-gray-900 text-base sm:text-lg font-bold">12월 19일 (금)</span>
        </label>

        <label class="flex items-center p-3.5 rounded-2xl border-2 border-pink-200 hover:border-red-400 bg-pink-50/60 cursor-pointer transition-all">
          <input type="checkbox" value="12월 20일" class="date-checkbox w-5 h-5 text-red-500 accent-red-500 rounded focus:ring-red-400">
          <span class="ml-3 font-headline text-gray-900 text-base sm:text-lg font-bold">12월 20일 (토)</span>
        </label>
      </div>

      <!-- Special Request Textarea -->
      <div class="space-y-1.5">
        <label for="user-request" class="block font-headline text-sm text-red-600">✍️ 요청사항 & 하고 싶은 말</label>
        <textarea id="user-request" rows="3" placeholder="먹고 싶은 음식, 알레르기, 놀이 제안 등 자유롭게 적어주세요!" class="w-full p-3 rounded-2xl border-2 border-pink-300 focus:border-red-500 focus:outline-none focus:ring-2 focus:ring-red-200 text-sm text-gray-900 font-bold placeholder-gray-400 resize-none"></textarea>
      </div>

      <button id="btn-submit-survey" class="w-full bg-red-500 hover:bg-red-600 active:scale-95 text-white font-headline text-lg py-3.5 px-6 rounded-2xl shadow-lg hover:shadow-xl transition-all duration-200">
        제출하기 💌
      </button>
    </section>

    <!-- STEP 3: Complete & Password View Access -->
    <section id="step-3" class="hidden space-y-6 text-center py-2">
      <div class="space-y-2">
        <span class="text-6xl">💖</span>
        <h2 class="font-headline text-2xl text-red-600 font-extrabold">제출이 완료되었습니다!</h2>
        <p class="text-sm text-gray-800 font-bold">소중한 의견 감사합니다.<br>곧 홈파티에서 만나요!</p>
      </div>

      <div class="bg-amber-50 p-4 rounded-2xl border border-amber-200 text-xs text-gray-700 text-left space-y-1 font-bold">
        <p class="font-extrabold text-gray-900 font-headline">💡 참고 사항</p>
        <p>• 투표 수정이 필요하면 새로 제출하시면 됩니다.</p>
        <p>• 전체 결과 조회는 주최자 비밀번호가 필요합니다.</p>
      </div>

      <div class="pt-2 space-y-3">
        <button id="btn-open-results-modal" class="w-full bg-amber-400 hover:bg-amber-500 text-gray-900 font-headline text-base py-3 px-6 rounded-2xl shadow transition-all">
          📊 전체 결과 확인하기
        </button>
        <button id="btn-restart" class="w-full bg-gray-100 hover:bg-gray-200 text-gray-800 font-bold text-sm py-2.5 px-4 rounded-2xl transition-all">
          첫 화면으로 돌아가기
        </button>
      </div>
    </section>

    <!-- STEP 4: Results Dashboard (Protected) -->
    <section id="step-results" class="hidden space-y-6">
      <div class="flex justify-between items-center border-b-2 border-pink-200 pb-3">
        <h2 class="font-headline text-xl text-red-600 font-extrabold">📊 투표 결과 총집합</h2>
        <button id="btn-close-results" class="text-xs bg-gray-200 hover:bg-gray-300 text-gray-800 px-3 py-1 rounded-full font-bold">닫기</button>
      </div>

      <!-- Summary Cards -->
      <div class="grid grid-cols-3 gap-2 text-center">
        <div class="bg-pink-50 p-2.5 rounded-xl border border-pink-200">
          <p class="text-xs font-headline text-gray-700">12/13 (금)</p>
          <p id="count-13" class="font-headline text-lg text-red-600 font-extrabold">0명</p>
        </div>
        <div class="bg-pink-50 p-2.5 rounded-xl border border-pink-200">
          <p class="text-xs font-headline text-gray-700">12/19 (금)</p>
          <p id="count-19" class="font-headline text-lg text-red-600 font-extrabold">0명</p>
        </div>
        <div class="bg-pink-50 p-2.5 rounded-xl border border-pink-200">
          <p class="text-xs font-headline text-gray-700">12/20 (토)</p>
          <p id="count-20" class="font-headline text-lg text-red-600 font-extrabold">0명</p>
        </div>
      </div>

      <!-- Detailed Table -->
      <div class="space-y-2">
        <h3 class="font-headline text-sm text-gray-900 font-extrabold">참석자별 응답 목록 (<span id="total-responses-count">0</span>명)</h3>
        <div class="max-h-60 overflow-y-auto space-y-2 pr-1" id="results-container">
          <!-- Dynamically inserted result cards -->
        </div>
      </div>

      <!-- Admin Actions -->
      <div class="pt-2 border-t border-gray-100 flex justify-between items-center">
        <button id="btn-clear-data" class="text-xs text-red-500 hover:text-red-700 underline font-bold">
          🗑️ 모든 응답 초기화
        </button>
        <button id="btn-back-home" class="bg-red-500 text-white text-xs font-headline px-4 py-2 rounded-xl">
          처음으로
        </button>
      </div>
    </section>

  </main>

  <!-- Password Modal -->
  <div id="password-modal" class="fixed inset-0 bg-black/50 backdrop-blur-sm hidden flex items-center justify-center p-4 z-50">
    <div class="bg-white rounded-3xl p-6 w-full max-w-xs shadow-2xl border-4 border-pink-300 space-y-4 text-center">
      <div class="space-y-1">
        <span class="text-3xl">🔒</span>
        <h3 class="font-headline text-lg text-gray-900 font-extrabold">비밀번호 입력</h3>
        <p class="text-xs text-gray-600 font-bold">결과를 확인하려면 패스워드를 입력하세요.</p>
      </div>
      
      <div>
        <input type="password" id="admin-password" placeholder="패스워드" class="w-full text-center tracking-widest text-lg font-bold px-4 py-2.5 rounded-xl border-2 border-pink-300 focus:border-red-500 focus:outline-none text-gray-900">
        <p id="password-error" class="text-xs text-red-500 font-bold mt-1 hidden">비밀번호가 올바르지 않습니다.</p>
      </div>

      <div class="flex gap-2">
        <button id="btn-cancel-password" class="w-1/2 bg-gray-100 hover:bg-gray-200 text-gray-800 font-headline py-2.5 rounded-xl text-sm">취소</button>
        <button id="btn-confirm-password" class="w-1/2 bg-red-500 hover:bg-red-600 text-white font-headline py-2.5 rounded-xl text-sm">확인</button>
      </div>
    </div>
  </div>

  <!-- Custom Alert Notification Box -->
  <div id="toast-msg" class="fixed bottom-5 left-1/2 -translate-x-1/2 bg-gray-900/95 text-white font-bold text-xs sm:text-sm px-5 py-2.5 rounded-full shadow-lg opacity-0 transition-opacity duration-300 pointer-events-none z-50">
    알림 메시지
  </div>

  <!-- Footer -->
  <footer class="w-full text-center py-4 text-xs text-gray-700 font-bold">
    ✨ Warm & Cozy Home Party 2026 ✨
  </footer>

  <script>
    // State management & LocalStorage Key
    const STORAGE_KEY = 'homeparty_survey_responses_v1';
    let currentGuestName = '';

    // DOM Elements
    const step1 = document.getElementById('step-1');
    const step2 = document.getElementById('step-2');
    const step3 = document.getElementById('step-3');
    const stepResults = document.getElementById('step-results');

    const guestNameInput = document.getElementById('guest-name');
    const displayGuestName = document.getElementById('display-guest-name');
    const userRequestInput = document.getElementById('user-request');

    const passwordModal = document.getElementById('password-modal');
    const adminPasswordInput = document.getElementById('admin-password');
    const passwordError = document.getElementById('password-error');

    // Utility: Show Toast Notification
    function showToast(msg) {
      const toast = document.getElementById('toast-msg');
      toast.textContent = msg;
      toast.classList.remove('opacity-0');
      toast.classList.add('opacity-100');
      setTimeout(() => {
        toast.classList.remove('opacity-100');
        toast.classList.add('opacity-0');
      }, 2500);
    }

    // Utility: Navigation Helper
    function showStep(targetStep) {
      [step1, step2, step3, stepResults].forEach(s => s.classList.add('hidden'));
      targetStep.classList.remove('hidden');
    }

    // Get Data from LocalStorage
    function getStoredResponses() {
      const data = localStorage.getItem(STORAGE_KEY);
      return data ? JSON.parse(data) : [];
    }

    // Save Response to LocalStorage
    function saveResponse(name, dates, request) {
      const responses = getStoredResponses();
      // Overwrite if same name exists or push new
      const existingIndex = responses.findIndex(r => r.name === name);
      const newEntry = {
        name: name,
        dates: dates,
        request: request,
        timestamp: new Date().toLocaleString('ko-KR')
      };

      if (existingIndex >= 0) {
        responses[existingIndex] = newEntry;
      } else {
        responses.push(newEntry);
      }

      localStorage.setItem(STORAGE_KEY, JSON.stringify(responses));
    }

    // Step 1 -> Step 2
    document.getElementById('btn-to-step-2').addEventListener('click', () => {
      const name = guestNameInput.value.trim();
      if (!name) {
        showToast('이름을 입력해주세요!');
        guestNameInput.focus();
        return;
      }
      currentGuestName = name;
      displayGuestName.textContent = `👤 ${name} 님의 투표`;
      showStep(step2);
    });

    // Step 2 -> Back to Step 1
    document.getElementById('btn-back-to-step-1').addEventListener('click', () => {
      showStep(step1);
    });

    // Step 2 -> Submit
    document.getElementById('btn-submit-survey').addEventListener('click', () => {
      const checkedBoxes = document.querySelectorAll('.date-checkbox:checked');
      const selectedDates = Array.from(checkedBoxes).map(cb => cb.value);
      const requestText = userRequestInput.value.trim();

      if (selectedDates.length === 0) {
        showToast('최소 하나의 날짜를 선택해주세요!');
        return;
      }

      saveResponse(currentGuestName, selectedDates, requestText);
      showStep(step3);
    });

    // Step 3 -> Restart
    document.getElementById('btn-restart').addEventListener('click', () => {
      guestNameInput.value = '';
      userRequestInput.value = '';
      document.querySelectorAll('.date-checkbox').forEach(cb => cb.checked = false);
      showStep(step1);
    });

    // Password Modal Logic
    function openPasswordModal() {
      adminPasswordInput.value = '';
      passwordError.classList.add('hidden');
      passwordModal.classList.remove('hidden');
      adminPasswordInput.focus();
    }

    function closePasswordModal() {
      passwordModal.classList.add('hidden');
    }

    document.getElementById('btn-open-admin-modal').addEventListener('click', openPasswordModal);
    document.getElementById('btn-open-results-modal').addEventListener('click', openPasswordModal);
    document.getElementById('btn-cancel-password').addEventListener('click', closePasswordModal);

    // Confirm Password
    document.getElementById('btn-confirm-password').addEventListener('click', verifyPassword);
    adminPasswordInput.addEventListener('keypress', (e) => {
      if (e.key === 'Enter') verifyPassword();
    });

    function verifyPassword() {
      const pwd = adminPasswordInput.value.trim();
      if (pwd === '961216') {
        closePasswordModal();
        renderResults();
        showStep(stepResults);
      } else {
        passwordError.classList.remove('hidden');
      }
    }

    // Render Results Dashboard
    function renderResults() {
      const responses = getStoredResponses();
      const resultsContainer = document.getElementById('results-container');
      const totalCountSpan = document.getElementById('total-responses-count');
      
      totalCountSpan.textContent = responses.length;

      // Count dates
      let c13 = 0, c19 = 0, c20 = 0;
      responses.forEach(r => {
        if (r.dates.includes('12월 13일')) c13++;
        if (r.dates.includes('12월 19일')) c19++;
        if (r.dates.includes('12월 20일')) c20++;
      });

      document.getElementById('count-13').textContent = `${c13}명`;
      document.getElementById('count-19').textContent = `${c19}명`;
      document.getElementById('count-20').textContent = `${c20}명`;

      // Render Cards
      resultsContainer.innerHTML = '';
      if (responses.length === 0) {
        resultsContainer.innerHTML = '<p class="text-center text-xs text-gray-400 py-6">아직 제출된 응답이 없습니다.</p>';
        return;
      }

      responses.forEach(item => {
        const card = document.createElement('div');
        card.className = 'bg-pink-50/70 p-3 rounded-2xl border border-pink-200 text-xs space-y-1.5';

        const datesBadge = item.dates.map(d => 
          `<span class="inline-block bg-red-100 text-red-600 font-headline px-2 py-0.5 rounded-md mr-1">${d}</span>`
        ).join('');

        card.innerHTML = `
          <div class="flex justify-between items-center">
            <span class="font-headline text-sm text-gray-900">${escapeHtml(item.name)}</span>
            <span class="text-[10px] text-gray-400">${item.timestamp || ''}</span>
          </div>
          <div>${datesBadge}</div>
          ${item.request ? `<div class="bg-white/80 p-2 rounded-xl text-gray-700 italic border border-pink-100 mt-1 font-body">💬 "${escapeHtml(item.request)}"</div>` : ''}
        `;
        resultsContainer.appendChild(card);
      });
    }

    // Clear Data Option
    document.getElementById('btn-clear-data').addEventListener('click', () => {
      if (confirm('정말로 모든 응답 데이터를 삭제하시겠습니까?')) {
        localStorage.removeItem(STORAGE_KEY);
        renderResults();
        showToast('모든 응답 데이터가 삭제되었습니다.');
      }
    });

    document.getElementById('btn-close-results').addEventListener('click', () => {
      showStep(step1);
    });

    document.getElementById('btn-back-home').addEventListener('click', () => {
      showStep(step1);
    });

    // Helper: Prevent XSS in rendered content
    function escapeHtml(str) {
      if (!str) return '';
      return str.replace(/&/g, "&amp;")
                .replace(/</g, "&lt;")
                .replace(/>/g, "&gt;")
                .replace(/"/g, "&quot;")
                .replace(/'/g, "&#039;");
    }
  </script>
</body>
</html>
