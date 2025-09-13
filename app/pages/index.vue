<template>
  <div class="min-h-screen relative overflow-hidden" style="background: linear-gradient(135deg, #1A1A1A 0%, #2C2C2C 50%, #222222 100%);">
    <!-- LOADING STATE -->
    <div v-if="loading" class="fixed inset-0 bg-black/50 backdrop-blur-sm z-50 flex items-center justify-center">
      <div class="text-center">
        <div class="animate-spin rounded-full h-12 w-12 border-b-2 border-white mx-auto mb-4"></div>
        <p class="text-white text-lg">홈페이지 로딩 중...</p>
      </div>
    </div>
    <!-- Animated Background Elements -->
    <div class="absolute inset-0 overflow-hidden">
      <!-- Floating orbs -->
      <div class="absolute top-1/4 left-1/4 w-64 h-64 rounded-full blur-3xl animate-pulse opacity-30" style="background: radial-gradient(circle, rgba(245,245,245,0.1) 0%, transparent 70%);"></div>
      <div class="absolute top-3/4 right-1/4 w-96 h-96 rounded-full blur-3xl animate-pulse delay-1000 opacity-20" style="background: radial-gradient(circle, rgba(240,242,245,0.08) 0%, transparent 70%);"></div>
      <div class="absolute top-1/2 left-1/2 w-72 h-72 rounded-full blur-3xl animate-pulse delay-500 opacity-25" style="background: radial-gradient(circle, rgba(237,237,237,0.06) 0%, transparent 70%);"></div>

      <!-- Geometric patterns -->
      <div class="absolute top-10 left-10 w-32 h-32 rotate-45 animate-spin-slow opacity-20" style="border: 1px solid rgba(245,245,245,0.1);"></div>
      <div class="absolute bottom-20 right-20 w-24 h-24 rotate-12 animate-spin-reverse opacity-15" style="border: 1px solid rgba(240,242,245,0.08);"></div>
      <div class="absolute top-1/3 right-10 w-20 h-20 rotate-45 animate-pulse opacity-10" style="background: linear-gradient(135deg, rgba(245,245,245,0.05) 0%, transparent 100%);"></div>

      <!-- Subtle grid overlay -->
      <div class="absolute inset-0 opacity-3">
        <div class="absolute inset-0" style="background-image: radial-gradient(circle at 1px 1px, rgba(245,245,245,0.08) 1px, transparent 0); background-size: 50px 50px;"></div>
      </div>
    </div>
    <!-- header -->
    <header class="relative overflow-hidden z-10">
      <div class="absolute inset-0" style="background: rgba(12,12,12,0.15); backdrop-filter: blur(4px);"></div>
      <div class="relative max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-24">
        <div class="text-center">
          <h1 class="text-5xl md:text-7xl font-bold mb-6" style="color: #F5F5F5;">
            박현준
            <span class="block text-2xl md:text-3xl font-light mt-2" style="color: #F0F2F5;">
              HYUNJUN PARK
            </span>
          </h1>
          <p class="text-xl md:text-2xl mb-8 max-w-3xl mx-auto" style="color: #EDEDED;">
            IT 스타트업 학생 창업자 & 풀스택 개발자
          </p>
          <p class="text-lg max-w-2xl mx-auto" style="color: #FAF9F6;">
            디지털 인프라와 클라우드 기술을 통해 비즈니스의 가능성을 확장하는 학생 개발자입니다.
          </p>
        </div>
      </div>
    </header>

    <!-- introduction -->
    <section class="py-20 relative z-10" style="background: rgba(26,26,26,0.05); backdrop-filter: blur(16px);">
      <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
        <h2 class="text-3xl md:text-4xl font-bold text-center mb-16" style="color: #F5F5F5;">About Me</h2>

        <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center mb-16">
          <!-- profile area -->
          <div class="text-center lg:text-left">
            <div class="relative inline-block mb-8">
              <div class="w-32 h-32 md:w-40 md:h-40 mx-auto lg:mx-0 rounded-full bg-gradient-to-br from-purple-600 to-cyan-600 p-1">
                <div class="w-full h-full rounded-full bg-gradient-to-br from-slate-900 to-gray-800 flex items-center justify-center text-6xl">
                  👨‍💻
                </div>
              </div>
              <div class="absolute -bottom-2 -right-2 w-8 h-8 bg-green-500 rounded-full border-4 border-gray-900 animate-pulse"></div>
            </div>

            <h3 class="text-2xl md:text-3xl font-bold mb-4" style="color: #F5F5F5;">박현준 (HYUNJUN PARK)</h3>
            <p class="text-lg mb-6" style="color: #F0F2F5;">IT 스타트업 창업자 & 풀스택 개발자</p>

            <!-- main statistics -->
            <div class="grid grid-cols-3 gap-4 mb-8">
              <div class="text-center p-4 rounded-lg" style="background: rgba(44,44,44,0.2); border: 1px solid rgba(245,245,245,0.1);">
                <div class="text-2xl font-bold" style="color: #F5F5F5;">3+</div>
                <div class="text-sm" style="color: #EDEDED;">년 경험</div>
              </div>
              <div class="text-center p-4 rounded-lg" style="background: rgba(44,44,44,0.2); border: 1px solid rgba(245,245,245,0.1);">
                <div class="text-2xl font-bold" style="color: #F5F5F5;">5+</div>
                <div class="text-sm" style="color: #EDEDED;">프로젝트</div>
              </div>
              <div class="text-center p-4 rounded-lg" style="background: rgba(44,44,44,0.2); border: 1px solid rgba(245,245,245,0.1);">
                <div class="text-2xl font-bold" style="color: #F5F5F5;">10k+</div>
                <div class="text-sm" style="color: #EDEDED;">코드 라인</div>
              </div>
            </div>
          </div>

          <!-- self introduction -->
          <div class="space-y-6">
            <div class="rounded-2xl p-6" style="background: rgba(44,44,44,0.15); backdrop-filter: blur(20px); border: 1px solid rgba(245,245,245,0.1);">
              <h4 class="text-xl font-semibold mb-4" style="color: #F5F5F5;">🚀 현재 활동</h4>
              <p class="text-base leading-relaxed" style="color: #EDEDED;">
                학생 개발자이자 IT 스타트업 창업자로서, 세계에 이로운 영향을 미치기 위해
                디지털 인프라와 클라우드 기술 분야에서 혁신적인 솔루션을 개발하고 있습니다.
              </p>
            </div>

            <div class="rounded-2xl p-6" style="background: rgba(44,44,44,0.15); backdrop-filter: blur(20px); border: 1px solid rgba(245,245,245,0.1);">
              <h4 class="text-xl font-semibold mb-4" style="color: #F5F5F5;">💡 전문 분야</h4>
              <p class="text-base leading-relaxed" style="color: #EDEDED;">
                디스코드 봇 개발부터 시작하여 DDoS 방어, 도메인 등록, 클라우드 인프라 구축까지
                다양한 분야에서 혁신적인 솔루션을 만들어왔습니다.
              </p>
            </div>

            <div class="rounded-2xl p-6" style="background: rgba(44,44,44,0.15); backdrop-filter: blur(20px); border: 1px solid rgba(245,245,245,0.1);">
              <h4 class="text-xl font-semibold mb-4" style="color: #F5F5F5;">🎯 핵심 가치</h4>
              <p class="text-base leading-relaxed" style="color: #EDEDED;">
                대규모 코드 리팩토링과 성능 최적화에 강점을 가지고 있으며,
                지속적인 학습과 혁신을 통해 더 나은 기술 생태계를 만들어가고 있습니다.
              </p>
            </div>
          </div>
        </div>

        <!-- 관심사 아이콘들 -->
        <div class="text-center">
          <h3 class="text-2xl font-bold mb-8" style="color: #F5F5F5;">🎯 주요 관심사</h3>
          <div class="grid grid-cols-2 md:grid-cols-4 lg:grid-cols-6 gap-6">
            <div class="group text-center p-4 rounded-xl transition-all duration-300 hover:scale-110" style="background: rgba(44,44,44,0.1); border: 1px solid rgba(245,245,245,0.05);">
              <div class="text-4xl mb-3">🛡️</div>
              <h4 class="font-semibold" style="color: #F5F5F5;">보안</h4>
              <p class="text-sm mt-1" style="color: #EDEDED;">DDoS 방어</p>
            </div>
            <div class="group text-center p-4 rounded-xl transition-all duration-300 hover:scale-110" style="background: rgba(44,44,44,0.1); border: 1px solid rgba(245,245,245,0.05);">
              <div class="text-4xl mb-3">☁️</div>
              <h4 class="font-semibold" style="color: #F5F5F5;">클라우드</h4>
              <p class="text-sm mt-1" style="color: #EDEDED;">인프라 구축</p>
            </div>
            <div class="group text-center p-4 rounded-xl transition-all duration-300 hover:scale-110" style="background: rgba(44,44,44,0.1); border: 1px solid rgba(245,245,245,0.05);">
              <div class="text-4xl mb-3">⚡</div>
              <h4 class="font-semibold" style="color: #F5F5F5;">성능</h4>
              <p class="text-sm mt-1" style="color: #EDEDED;">최적화</p>
            </div>
            <div class="group text-center p-4 rounded-xl transition-all duration-300 hover:scale-110" style="background: rgba(44,44,44,0.1); border: 1px solid rgba(245,245,245,0.05);">
              <div class="text-4xl mb-3">🔧</div>
              <h4 class="font-semibold" style="color: #F5F5F5;">DevOps</h4>
              <p class="text-sm mt-1" style="color: #EDEDED;">자동화</p>
            </div>
            <div class="group text-center p-4 rounded-xl transition-all duration-300 hover:scale-110" style="background: rgba(44,44,44,0.1); border: 1px solid rgba(245,245,245,0.05);">
              <div class="text-4xl mb-3">🌐</div>
              <h4 class="font-semibold" style="color: #F5F5F5;">네트워크</h4>
              <p class="text-sm mt-1" style="color: #EDEDED;">인프라</p>
            </div>
            <div class="group text-center p-4 rounded-xl transition-all duration-300 hover:scale-110" style="background: rgba(44,44,44,0.1); border: 1px solid rgba(245,245,245,0.05);">
              <div class="text-4xl mb-3">📊</div>
              <h4 class="font-semibold" style="color: #F5F5F5;">데이터</h4>
              <p class="text-sm mt-1" style="color: #EDEDED;">분석</p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- coding analytics section -->
    <section class="py-20 relative z-10" style="background: rgba(26,26,26,0.03); backdrop-filter: blur(16px);">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <h2 class="text-3xl md:text-4xl font-bold text-center mb-16" style="color: #F5F5F5;">💻 Coding Stats</h2>

        <!-- main statistics -->
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8 mb-16">
          <div class="text-center p-8 rounded-2xl" style="background: rgba(44,44,44,0.15); backdrop-filter: blur(20px); border: 1px solid rgba(245,245,245,0.1);">
            <div class="text-5xl mb-4">⏱️</div>
            <div class="text-3xl font-bold mb-2" style="color: #F5F5F5;">{{ codingStats.totalHours }}</div>
            <div class="text-lg" style="color: #EDEDED;">총 코딩 시간</div>
            <div class="text-sm mt-2" style="color: #FAF9F6;">1년간 누적</div>
          </div>

          <div class="text-center p-8 rounded-2xl" style="background: rgba(44,44,44,0.15); backdrop-filter: blur(20px); border: 1px solid rgba(245,245,245,0.1);">
            <div class="text-5xl mb-4">📅</div>
            <div class="text-3xl font-bold mb-2" style="color: #F5F5F5;">{{ codingStats.dailyAverage }}</div>
            <div class="text-lg" style="color: #EDEDED;">일일 평균</div>
            <div class="text-sm mt-2" style="color: #FAF9F6;">꾸준한 개발 습관</div>
          </div>

          <div class="text-center p-8 rounded-2xl" style="background: rgba(44,44,44,0.15); backdrop-filter: blur(20px); border: 1px solid rgba(245,245,245,0.1);">
            <div class="text-5xl mb-4">🏆</div>
            <div class="text-3xl font-bold mb-2" style="color: #F5F5F5;">{{ codingStats.bestDay }}</div>
            <div class="text-lg" style="color: #EDEDED;">최고 기록</div>
            <div class="text-sm mt-2" style="color: #FAF9F6;">{{ codingStats.bestDayDate }}</div>
          </div>
        </div>

        <!-- language usage chart -->
        <div class="grid grid-cols-1 lg:grid-cols-2 gap-12">
          <!-- language usage chart -->
          <div class="rounded-2xl p-8" style="background: rgba(44,44,44,0.15); backdrop-filter: blur(20px); border: 1px solid rgba(245,245,245,0.1);">
            <h3 class="text-2xl font-bold mb-8 text-center" style="color: #F5F5F5;">🌐 언어 사용 비율</h3>

            <div class="space-y-4">
              <div v-for="(language, index) in codingStats.languages" :key="index" class="flex items-center space-x-4">
                <div class="w-20 text-sm font-medium" style="color: #EDEDED;">{{ language.name }}</div>
                <div class="flex-1 bg-gray-700 rounded-full h-4">
                  <div class="h-4 rounded-full transition-all duration-1000" :style="{ width: language.percent + '%', backgroundColor: language.color }"></div>
                </div>
                <div class="w-12 text-sm text-right" style="color: #FAF9F6;">{{ language.percent }}%</div>
              </div>
            </div>
          </div>

          <!-- coding habits -->
          <div class="rounded-2xl p-8" style="background: rgba(44,44,44,0.15); backdrop-filter: blur(20px); border: 1px solid rgba(245,245,245,0.1);">
            <h3 class="text-2xl font-bold mb-8 text-center" style="color: #F5F5F5;">📈 코딩 습관</h3>

            <div class="space-y-6">
              <div class="text-center p-6 rounded-xl" style="background: rgba(26,26,26,0.1); border: 1px solid rgba(245,245,245,0.05);">
                <div class="text-3xl mb-3">🎯</div>
                <h4 class="text-lg font-semibold mb-2" style="color: #F5F5F5;">꾸준한 개발</h4>
                <p class="text-sm" style="color: #EDEDED;">3년간 매일 코딩하며 꾸준한 습관을 유지하고 있습니다.</p>
              </div>

              <div class="text-center p-6 rounded-xl" style="background: rgba(26,26,26,0.1); border: 1px solid rgba(245,245,245,0.05);">
                <div class="text-3xl mb-3">🚀</div>
                <h4 class="text-lg font-semibold mb-2" style="color: #F5F5F5;">풀스택 전문성</h4>
                <p class="text-sm" style="color: #EDEDED;">Frontend와 Backend 모두에서 풍부한 경험을 가지고 있습니다.</p>
              </div>

              <div class="text-center p-6 rounded-xl" style="background: rgba(26,26,26,0.1); border: 1px solid rgba(245,245,245,0.05);">
                <div class="text-3xl mb-3">⚡</div>
                <h4 class="text-lg font-semibold mb-2" style="color: #F5F5F5;">고효율 코딩</h4>
                <p class="text-sm" style="color: #EDEDED;">생산성을 높이는 도구와 방법을 적극적으로 활용합니다.</p>
              </div>

              <div class="text-center p-6 rounded-xl" style="background: rgba(26,26,26,0.1); border: 1px solid rgba(245,245,245,0.05);">
                <div class="text-3xl mb-3">🔄</div>
                <h4 class="text-lg font-semibold mb-2" style="color: #F5F5F5;">지속적 성장</h4>
                <p class="text-sm" style="color: #EDEDED;">새로운 기술을 배우고 적용하며 끊임없이 발전하고 있습니다.</p>
              </div>
            </div>
          </div>
        </div>

        <div class="text-center mt-12 space-y-3">
          <p class="text-lg" style="color: #FAF9F6;">
            📊 <span style="color: #F0F2F5; font-weight: bold;">
              {{ formatDateRange(codingStats.dataRange.start, codingStats.dataRange.end) }}
            </span> 코딩 활동 데이터
          </p>
          <p class="text-sm" style="color: #EDEDED; opacity: 0.8;">
            ※ 데이터는 IDE 플러그인 설치 상태 및 인터넷 연결에 따라 일부 오차가 있을 수 있습니다
          </p>
        </div>
      </div>
    </section>

    <!-- projects section -->
    <section class="py-20 relative z-10">
      <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
        <h2 class="text-3xl md:text-4xl font-bold text-center mb-16" style="color: #F5F5F5;">Projects & Experience</h2>

        <div class="space-y-12">
          <!-- Guilds Protect -->
          <div class="rounded-2xl p-8 transition-all duration-500 hover:scale-[1.02]" style="background: rgba(44,44,44,0.12); backdrop-filter: blur(20px); border: 1px solid rgba(245,245,245,0.08); box-shadow: 0 20px 40px -12px rgba(0,0,0,0.3);">
            <div class="flex flex-col md:flex-row md:items-center md:justify-between mb-6">
              <div>
                <h3 class="text-2xl font-bold mb-2" style="color: #F5F5F5;">Guilds Protect</h3>
                <p class="font-medium" style="color: #F0F2F5;">2022</p>
              </div>
              <a href="https://gprotect.xyz" target="_blank"
                 class="mt-4 md:mt-0 px-6 py-2 rounded-lg transition-all duration-300 hover:scale-105" style="background: linear-gradient(135deg, #2C2C2C 0%, #1A1A1A 100%); color: #F5F5F5; border: 1px solid rgba(245,245,245,0.1);">
                Visit Website →
              </a>
            </div>
            <p class="text-lg mb-4" style="color: #EDEDED;">
              Discord 서버 테러 방지를 위한 보안 봇입니다. 서버 관리자와 사용자들을
              악의적인 공격으로부터 보호하는 역할을 수행합니다.
            </p>
            <div class="flex flex-wrap gap-2">
              <span class="px-3 py-1 rounded-full text-sm" style="background: rgba(240,242,245,0.1); color: #F0F2F5; border: 1px solid rgba(240,242,245,0.2);">Discord API</span>
              <span class="px-3 py-1 rounded-full text-sm" style="background: rgba(245,245,245,0.08); color: #EDEDED; border: 1px solid rgba(245,245,245,0.15);">Node.js</span>
              <span class="px-3 py-1 rounded-full text-sm" style="background: rgba(250,249,246,0.1); color: #FAF9F6; border: 1px solid rgba(250,249,246,0.2);">Security</span>
            </div>
          </div>

          <!-- Feather IT -->
          <div class="rounded-2xl p-8 transition-all duration-500 hover:scale-[1.02]" style="background: rgba(34,34,34,0.15); backdrop-filter: blur(20px); border: 1px solid rgba(245,245,245,0.1); box-shadow: 0 20px 40px -12px rgba(0,0,0,0.3);">
            <div class="flex flex-col md:flex-row md:items-center md:justify-between mb-6">
              <div>
                <h3 class="text-2xl font-bold mb-2" style="color: #F5F5F5;">Feather IT (페더아이티)</h3>
                <p class="font-medium" style="color: #F0F2F5;">2023 ~ Present</p>
              </div>
              <a href="https://feather-it.com" target="_blank"
                 class="mt-4 md:mt-0 px-6 py-2 rounded-lg transition-all duration-300 hover:scale-105" style="background: linear-gradient(135deg, #222222 0%, #0C0C0C 100%); color: #F5F5F5; border: 1px solid rgba(245,245,245,0.1);">
                Visit Website →
              </a>
            </div>
            <p class="text-lg mb-6" style="color: #EDEDED;">
              DDoS 방어 인프라와 도메인 관련 IT 스타트업입니다.
              클라우드 컴퓨팅과 디지털 인프라 분야에서 혁신적인 솔루션을 제공합니다.
            </p>

            <!-- internal projects -->
            <div class="space-y-6">
              <div class="pl-6" style="border-left: 4px solid #F0F2F5;">
                <h4 class="text-xl font-semibold mb-2" style="color: #F5F5F5;">FEATHER IT CLOUD</h4>
                <p class="text-sm mb-3" style="color: #F0F2F5;">2023 - 2024</p>
                <p class="mb-3" style="color: #EDEDED;">
                  Microsoft Hyper-V, XCP-ng, Proxmox VE 하이퍼바이저를 활용한 저가형 클라우드 브랜드입니다.
                  가상화 기술과 클라우드 비즈니스의 기초를 다졌습니다.
                </p>
                <div class="flex flex-wrap gap-2">
                  <span class="px-3 py-1 rounded-full text-sm" style="background: rgba(240,242,245,0.08); color: #F0F2F5; border: 1px solid rgba(240,242,245,0.15);">Hyper-V</span>
                  <span class="px-3 py-1 rounded-full text-sm" style="background: rgba(245,245,245,0.06); color: #EDEDED; border: 1px solid rgba(245,245,245,0.12);">XCP-ng</span>
                  <span class="px-3 py-1 rounded-full text-sm" style="background: rgba(237,237,237,0.08); color: #FAF9F6; border: 1px solid rgba(237,237,237,0.15);">Proxmox VE</span>
                  <span class="px-3 py-1 rounded-full text-sm" style="background: rgba(250,249,246,0.07); color: #F5F5F5; border: 1px solid rgba(250,249,246,0.14);">Virtualization</span>
                </div>
              </div>

              <div class="pl-6" style="border-left: 4px solid #F0F2F5;">
                <h4 class="text-xl font-semibold mb-2" style="color: #F5F5F5;">TEAM ARI (팀 아리)</h4>
                <p class="text-sm mb-3" style="color: #F0F2F5;">2025 ~ Present</p>
                <p class="mb-3" style="color: #EDEDED;">
                  팀 아리의 아리 봇을 개발 담당하고 있습니다. 3만줄 이상의 코드를 리팩토링하여
                  약 30% 이상의 성능 개선 및 비즈니스 로직 개선을 달성했습니다.
                </p>
                <div class="flex flex-wrap gap-2">
                  <span class="px-3 py-1 rounded-full text-sm" style="background: rgba(245,245,245,0.06); color: #EDEDED; border: 1px solid rgba(245,245,245,0.12);">Node.js</span>
                  <span class="px-3 py-1 rounded-full text-sm" style="background: rgba(240,242,245,0.08); color: #F0F2F5; border: 1px solid rgba(240,242,245,0.15);">Performance</span>
                  <span class="px-3 py-1 rounded-full text-sm" style="background: rgba(237,237,237,0.07); color: #FAF9F6; border: 1px solid rgba(237,237,237,0.14);">Refactoring</span>
                </div>
              </div>

              <div class="pl-6" style="border-left: 4px solid #F0F2F5;">
                <h4 class="text-xl font-semibold mb-2" style="color: #F5F5F5;">PIORA (피오라)</h4>
                <p class="text-sm mb-3" style="color: #F0F2F5;">2025 ~ Present</p>
                <p class="mb-3" style="color: #EDEDED;">
                  국내 여러 도메인 등록기관과 협업하여 만들어진 최저가 도메인 등록기관입니다.
                  자사의 이익을 최소화하여 도메인 등록 단가를 낮추는 것을 목표로 합니다.
                </p>
                <div class="flex flex-wrap gap-2">
                  <span class="px-3 py-1 rounded-full text-sm" style="background: rgba(245,245,245,0.06); color: #EDEDED; border: 1px solid rgba(245,245,245,0.12);">Nuxt.js</span>
                  <span class="px-3 py-1 rounded-full text-sm" style="background: rgba(240,242,245,0.08); color: #F0F2F5; border: 1px solid rgba(240,242,245,0.15);">Nest.js</span>
                  <span class="px-3 py-1 rounded-full text-sm" style="background: rgba(237,237,237,0.07); color: #FAF9F6; border: 1px solid rgba(237,237,237,0.14);">MySQL</span>
                  <span class="px-3 py-1 rounded-full text-sm" style="background: rgba(250,249,246,0.08); color: #F5F5F5; border: 1px solid rgba(250,249,246,0.15);">Go</span>
                </div>
              </div>

              <div class="pl-6" style="border-left: 4px solid #F0F2F5;">
                <h4 class="text-xl font-semibold mb-2" style="color: #F5F5F5;">ARLINA</h4>
                <p class="text-sm mb-3" style="color: #F0F2F5;">2026 ~</p>
                <p class="mb-3" style="color: #EDEDED;">
                  페더아이티의 미래 사업인 클라우드 사업입니다. 일본과 뉴욕과 같은 주요 지역에
                  서버를 위치하여 프리미엄 클라우드 서비스를 제공할 예정입니다.
                </p>
                <div class="flex flex-wrap gap-2">
                  <span class="px-3 py-1 rounded-full text-sm" style="background: rgba(245,245,245,0.06); color: #EDEDED; border: 1px solid rgba(245,245,245,0.12);">Cloud</span>
                  <span class="px-3 py-1 rounded-full text-sm" style="background: rgba(240,242,245,0.08); color: #F0F2F5; border: 1px solid rgba(240,242,245,0.15);">Infrastructure</span>
                  <span class="px-3 py-1 rounded-full text-sm" style="background: rgba(237,237,237,0.07); color: #FAF9F6; border: 1px solid rgba(237,237,237,0.14);">Premium</span>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- tech stacks -->
    <section class="py-20 bg-white/5 backdrop-blur-xl relative z-10">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <h2 class="text-3xl md:text-4xl font-bold text-center mb-16" style="color: #F5F5F5;">Tech Stack</h2>

        <!-- Programming -->
        <div class="mb-12">
          <h3 class="text-xl font-semibold mb-6 text-center" style="color: #F0F2F5;">Programming Languages</h3>
          <div class="flex flex-wrap justify-center gap-4">
            <img src="https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=java&logoColor=white" alt="Java" class="hover:scale-110 transition-transform duration-300" />
            <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JavaScript" class="hover:scale-110 transition-transform duration-300" />
            <img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript" class="hover:scale-110 transition-transform duration-300" />
            <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python" class="hover:scale-110 transition-transform duration-300" />
            <img src="https://img.shields.io/badge/C-00599C?style=for-the-badge&logo=c&logoColor=white" alt="C" class="hover:scale-110 transition-transform duration-300" />
            <img src="https://img.shields.io/badge/Go-00ADD8?style=for-the-badge&logo=go&logoColor=white" alt="Go" class="hover:scale-110 transition-transform duration-300" />
            <img src="https://img.shields.io/badge/Minecraft-ED1C24?style=for-the-badge&logo=minecraft&logoColor=white" alt="Minecraft Plugin" class="hover:scale-110 transition-transform duration-300" />
          </div>
        </div>

        <!-- Web Frameworks & Libs -->
        <div class="mb-12">
          <h3 class="text-xl font-semibold mb-6 text-center" style="color: #F0F2F5;">Web Frameworks & Libraries</h3>
          <div class="flex flex-wrap justify-center gap-4">
            <img src="https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=next.js&logoColor=white" alt="Next.js" class="hover:scale-110 transition-transform duration-300" />
            <img src="https://img.shields.io/badge/Nest.js-E0234E?style=for-the-badge&logo=nestjs&logoColor=white" alt="Nest.js" class="hover:scale-110 transition-transform duration-300" />
            <img src="https://img.shields.io/badge/Nuxt.js-00C58E?style=for-the-badge&logo=nuxtdotjs&logoColor=white" alt="Nuxt.js" class="hover:scale-110 transition-transform duration-300" />
            <img src="https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white" alt="Flask" class="hover:scale-110 transition-transform duration-300" />
            <img src="https://img.shields.io/badge/Sonic-1ABC9C?style=for-the-badge&logo=&logoColor=white" alt="Sonic" class="hover:scale-110 transition-transform duration-300" />
            <img src="https://img.shields.io/badge/Quart-3498DB?style=for-the-badge&logo=&logoColor=white" alt="Quart" class="hover:scale-110 transition-transform duration-300" />
            <img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white" alt="FastAPI" class="hover:scale-110 transition-transform duration-300" />
            <img src="https://img.shields.io/badge/XDP-FF8C00?style=for-the-badge&logo=&logoColor=white" alt="XDP" class="hover:scale-110 transition-transform duration-300" />
          </div>
        </div>

        <!-- Databases -->
        <div class="mb-12">
          <h3 class="text-xl font-semibold mb-6 text-center" style="color: #F0F2F5;">Databases</h3>
          <div class="flex flex-wrap justify-center gap-4">
            <img src="https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white" alt="MySQL" class="hover:scale-110 transition-transform duration-300" />
            <img src="https://img.shields.io/badge/MariaDB-003545?style=for-the-badge&logo=mariadb&logoColor=white" alt="MariaDB" class="hover:scale-110 transition-transform duration-300" />
            <img src="https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb&logoColor=white" alt="MongoDB" class="hover:scale-110 transition-transform duration-300" />
          </div>
        </div>

        <!-- Specialties -->
        <div class="mb-12">
          <h3 class="text-xl font-semibold mb-6 text-center" style="color: #F0F2F5;">Specialties</h3>
          <div class="flex flex-wrap justify-center gap-4">
            <img src="https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black" alt="Linux" class="hover:scale-110 transition-transform duration-300" />
          </div>
        </div>
      </div>
    </section>

    <!-- cta -->
    <section class="py-20 relative z-10">
      <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
        <h2 class="text-3xl md:text-4xl font-bold mb-12" style="color: #F5F5F5;">Get In Touch</h2>
        <p class="text-xl mb-8" style="color: #EDEDED;">
          함께 일할 기회를 찾고 계신가요? 언제든 연락 주세요!
        </p>
        <div class="flex flex-col sm:flex-row gap-4 justify-center">
          <a href="mailto:park@hyunjun.me"
             class="px-8 py-4 rounded-lg transition-all duration-300 hover:scale-105 font-medium" style="background: linear-gradient(135deg, #2C2C2C 0%, #1A1A1A 100%); color: #F5F5F5; border: 1px solid rgba(245,245,245,0.1);">
            📧 이메일 보내기
          </a>
          <a href="https://feather-it.com"
             target="_blank"
             class="px-8 py-4 rounded-lg transition-all duration-300 hover:scale-105 font-medium" style="background: rgba(44,44,44,0.1); color: #EDEDED; border: 1px solid rgba(245,245,245,0.1); backdrop-filter: blur(10px);">
            🌐 웹사이트 방문
          </a>
        </div>
      </div>
    </section>

    <!-- footer -->
    <footer class="py-8 border-t border-white/20 backdrop-blur-xl bg-white/5 relative z-10">
      <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
        <p style="color: #FAF9F6;">
          © 2024 박현준 (HYUNJUN PARK). All rights reserved.
        </p>
      </div>
    </footer>
  </div>
</template>

<script setup lang="ts">
import { ref, onMounted } from 'vue'

const loading = ref(true)
const codingStats = ref({
  totalHours: '0시간',
  dailyAverage: '0시간 0분',
  bestDay: '0시간 0분',
  bestDayDate: '',
  dataRange: {
    start: '',
    end: '',
    range: ''
  },
  languages: [] as { name: string; percent: number; color: string }[]
})

// wakatime api calls
const fetchCodingActivity = async () => {
  try {
    const response = await fetch('https://wakatime.com/share/@98c555b6-db34-402d-8a89-c902873475b8/d780b601-245f-4261-9ba4-44a5a66e5c73.json')
    const data = await response.json()

    if (data.data) {
      const grandTotal = data.data.grand_total
      const bestDay = data.data.best_day
      const range = data.data.range
      const totalHours = Math.floor(grandTotal.total_seconds / 3600)
      const dailyAvg = grandTotal.human_readable_daily_average
      
      codingStats.value.totalHours = `${totalHours}시간`
      codingStats.value.dailyAverage = dailyAvg
      codingStats.value.bestDay = bestDay.text
      codingStats.value.bestDayDate = bestDay.date

      if (range) {
        codingStats.value.dataRange = {
          start: range.start,
          end: range.end,
          range: range.range
        }
      }
    }
  } catch (error) {
    console.error('Coding activity API 호출 실패:', error)
  }
}

const fetchLanguages = async () => {
  try {
    const response = await fetch('https://wakatime.com/share/@98c555b6-db34-402d-8a89-c902873475b8/26281119-f7d3-4841-95a0-c17596e49ca9.json')
    const data = await response.json()

    if (data.data && Array.isArray(data.data)) {
      // top 6 languages
      codingStats.value.languages = data.data.slice(0, 6).map((lang: any) => ({
        name: lang.name,
        percent: lang.percent,
        color: lang.color
      }))

      // other languages are summed up as "etc"
      const otherLanguages = data.data.slice(6)
      const otherPercent = otherLanguages.reduce((sum: number, lang: any) => sum + lang.percent, 0)

      if (otherPercent > 0) {
        codingStats.value.languages.push({
          name: '기타',
          percent: Math.round(otherPercent * 100) / 100,
          color: '#9467bd'
        })
      }
    }
  } catch (error) {
    console.error('Languages API call failed:', error)
  }
}

// component mount api calls
onMounted(async () => {
  loading.value = true

  try {
    await Promise.all([
      fetchCodingActivity(),
      fetchLanguages()
    ])
  } catch (error) {
    console.error('API 호출 중 오류 발생:', error)
  } finally {
    loading.value = false
  }
})

// format date range
const formatDateRange = (startDate: string, endDate: string) => {
  if (!startDate || !endDate) {
    return '2022년 9월 ~ 현재'
  }

  try {
    const start = new Date(startDate)
    const end = new Date(endDate)

    const startYear = start.getFullYear()
    const startMonth = start.getMonth() + 1
    const endYear = end.getFullYear()
    const endMonth = end.getMonth() + 1

    if (startYear === endYear) {
      return `${startYear}년 ${startMonth}월 ~ ${endMonth}월`
    } else {
      return `${startYear}년 ${startMonth}월 ~ ${endYear}년 ${endMonth}월`
    }
  } catch (error) {
    return '2022년 9월 ~ 현재'
  }
}

// convert language color to css class name
const getLanguageColorClass = (color: string) => {
  // WakaTime color code to Tailwind class name
  const colorMap: { [key: string]: string } = {
    '#3178c6': 'bg-blue-600',
    '#16ce40': 'bg-green-500',
    '#f1e05a': 'bg-yellow-500',
    '#3572A5': 'bg-blue-700',
    '#dc9658': 'bg-orange-600',
    '#9467bd': 'bg-purple-600'
  }
  return colorMap[color] || 'bg-gray-600'
}
</script>