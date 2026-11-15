# NocturnalPulse.com
A regular news site
<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>NocturnalPulse_4</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&family=JetBrains+Mono:wght@400;500;600&display=swap" rel="stylesheet" />

  <style>
    :root {
      --accent-color: #00f0ff;
      --accent-rgb: 0, 240, 255;
      --btn-radius: 10px;
      --btn-border-width: 1px;
      --bg-overlay-opacity: 0.72;
      --bg-blur: 4px;
    }
    * { box-sizing: border-box; scrollbar-width: thin; scrollbar-color: rgba(var(--accent-rgb), 0.35) rgba(15, 23, 42, 0.5); }
    body { font-family: 'Inter', sans-serif; background-color: #060913; color: #e2e8f0; margin: 0; min-height: 100vh; overflow-x: hidden; }
    .font-mono-tech { font-family: 'JetBrains Mono', monospace; }

    #wallpaper-layer { position: fixed; inset: 0; z-index: -2; background: radial-gradient(circle at 80% 20%, rgba(var(--accent-rgb), 0.12), transparent 50%), #060913; filter: blur(var(--bg-blur)); transform: scale(1.03); }
    #wallpaper-overlay { position: fixed; inset: 0; z-index: -1; background: rgba(6, 9, 19, var(--bg-overlay-opacity)); }

    .glass-panel { background: rgba(13, 19, 34, 0.74); backdrop-filter: blur(14px); -webkit-backdrop-filter: blur(14px); border: 1px solid rgba(148, 163, 184, 0.14); box-shadow: 0 12px 36px -10px rgba(0, 0, 0, 0.65); }

    .np-btn { border-radius: var(--btn-radius); transition: all 0.22s cubic-bezier(0.22, 1, 0.36, 1); position: relative; overflow: hidden; cursor: pointer; }
    .np-btn-primary { background-color: var(--accent-color); color: #040711; font

https://github.com/user-attachments/assets/da8fcaf6-3e16-43a8-ac0b-bbb16e6c8648

-weight: 600; border: var(--btn-border-width) solid var(--accent-color); box-shadow: 0 0 18px rgba(var(--accent-rgb), 0.3); }
    .np-btn-primary:hover { filter: brightness(1.1); box-shadow: 0 0 26px rgba(var(--accent-rgb), 0.5); transform: translateY(-1px); }
    .np-btn-outline { background: rgba(15, 23, 42, 0.65); color: #f1f5f9; border: var(--btn-border-width) solid rgba(var(--accent-rgb), 0.45); }
    .np-btn-outline:hover { background: rgba(var(--accent-rgb), 0.14); border-color: var(--accent-color); box-shadow: 0 0 16px rgba(var(--accent-rgb), 0.22); }
    .np-btn-outline.active-depth { background: rgba(var(--accent-rgb), 0.2); border-color: var(--accent-color); color: var(--accent-color); }

    body.btn-style-neon .np-btn-primary { background: rgba(var(--accent-rgb), 0.14); color: var(--accent-color); border: 1.5px solid var(--accent-color); box-shadow: inset 0 0 12px rgba(var(--accent-rgb), 0.25), 0 0 16px rgba(var(--accent-rgb), 0.3); }
    body.btn-style-neon .np-btn-primary:hover { background: rgba(var(--accent-rgb), 0.24); }

    .role-card { border-radius: var(--btn-radius); border: 1px solid rgba(148, 163, 184, 0.16); background: rgba(15, 23, 42, 0.62); transition: all 0.25s ease; cursor: pointer; }
    .role-card:hover { border-color: rgba(var(--accent-rgb), 0.55); transform: translateY(-2px); background: rgba(20, 30, 52, 0.82); }
    .role-card.active { border-color: var(--accent-color); background: linear-gradient(145deg, rgba(var(--accent-rgb), 0.18), rgba(13, 19, 34, 0.9)); box-shadow: 0 0 24px rgba(var(--accent-rgb), 0.22); }

    @keyframes corePulse { 0%, 100% { opacity: 1; transform: scale(1); box-shadow: 0 0 10px var(--accent-color); } 50% { opacity: 0.55; transform: scale(0.85); box-shadow: 0 0 4px var(--accent-color); } }
    .pulse-dot { background-color: var(--accent-color); animation: corePulse 2.2s infinite ease-in-out; }

    .prose-output h3 { color: var(--accent-color); font-weight: 600; font-size: 1.05rem; margin-top: 1rem; margin-bottom: 0.45rem; }
    .prose-output p { margin-bottom: 0.65rem; line-height: 1.65; color: #cbd5e1; }
    .prose-output ul { margin-left: 1.25rem; margin-bottom: 0.75rem; color: #cbd5e1; list-style: disc; }
    .prose-output li { margin-bottom: 0.3rem; }
    .prose-output table { width: 100%; border-collapse: collapse; margin: 0.85rem 0; font-size: 0.875rem; }
    .prose-output th { background: rgba(var(--accent-rgb), 0.15); color: var(--accent-color); text-align: left; padding: 0.55rem 0.75rem; border: 1px solid rgba(148, 163, 184, 0.25); }
    .prose-output td { padding: 0.5rem 0.75rem; border: 1px solid rgba(148, 163, 184, 0.18); color: #e2e8f0; }
  </style>
</head>
<body class="antialiased selection:bg-cyan-500/30 selection:text-white">

  <div id="wallpaper-layer"></div>
  <div id="wallpaper-overlay"></div>

  <header class="sticky top-0 z-30 glass-panel border-b border-slate-800/80">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 h-16 flex items-center justify-between gap-3">
      <div class="flex items-center gap-3">
        <div class="w-10 h-10 rounded-lg flex items-center justify-center border bg-slate-900/90" style="border-color: rgba(var(--accent-rgb), 0.45);">
          <svg class="w-6 h-6" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" style="color: var(--accent-color);">
            <path d="M2 12h4l3-7 4 14 3-7h6" stroke-linecap="round" stroke-linejoin="round"/>
            <circle cx="12" cy="12" r="9.5" stroke-opacity="0.28"/>
          </svg>
        </div>
        <div>
          <div class="flex items-center gap-2">
            <h1 class="text-lg sm:text-xl font-bold tracking-tight text-white font-mono-tech">NocturnalPulse_4</h1>
            <span class="w-2 h-2 rounded-full pulse-dot"></span>
          </div>
          <p class="text-[11px] text-slate-400 hidden sm:block">Мультипрофильная аналитическая и инженерная среда</p>
        </div>
      </div>
      <div class="flex items-center gap-2 sm:gap-3">
        <button id="btn-open-add-btn" class="np-btn np-btn-outline px-3 py-2 text-xs sm:text-sm font-medium">+ Добавить кнопку</button>
        <button id="btn-open-customizer" class="np-btn np-btn-primary px-3.5 py-2 text-xs sm:text-sm">Настройка интерфейса</button>
      </div>
    </div>
  </header>

  <main class="max-w-7xl mx-auto px-4 sm:px-6 py-6 space-y-6">

    <section>
      <div class="flex flex-wrap items-center justify-between gap-2 mb-3">
        <h2 class="text-sm font-semibold uppercase tracking-wider text-slate-300">Выбор специализации и профиля</h2>
        <span id="active-role-badge" class="text-xs font-mono-tech px-2.5 py-1 rounded border" style="color: var(--accent-color); border-color: rgba(var(--accent-rgb), 0.4); background: rgba(var(--accent-rgb), 0.1);">Модуль: Аналитик</span>
      </div>
      <div id="roles-grid" class="grid grid-cols-2 sm:grid-cols-3 xl:grid-cols-6 gap-3"></div>
      <div id="role-subpanel" class="hidden mt-3 glass-panel p-4 rounded-xl"></div>
    </section>

    <section class="glass-panel p-4 rounded-xl">
      <div class="flex flex-wrap items-center justify-between gap-2 mb-3">
        <h2 class="text-xs font-semibold uppercase tracking-wider text-slate-300">Панель быстрых команд</h2>
        <span class="text-[11px] text-slate-400">Нажмите для вставки в поле задачи, × для удаления</span>
      </div>
      <div id="custom-buttons-container" class="flex flex-wrap gap-2.5"></div>
    </section>

    <section class="grid grid-cols-1 lg:grid-cols-12 gap-5">
      <div class="lg:col-span-5 space-y-4">
        <div class="glass-panel p-5 rounded-xl space-y-4">
          <div class="flex items-center justify-between">
            <h3 class="text-sm font-semibold text-white">Терминал постановки задачи</h3>
            <span id="role-mode-label" class="text-[11px] font-mono-tech text-slate-400">РЕЖИМ: СВОДКА И ПАТТЕРНЫ</span>
          </div>
          <div>
            <label for="task-input" class="block text-xs text-slate-400 mb-1.5">Опишите задачу, данные, код, улики или тему для разбора:</label>
            <textarea id="task-input" rows="6" class="w-full rounded-lg bg-slate-950/80 border border-slate-700/80 p-3 text-sm text-slate-100 placeholder-slate-500 focus:outline-none" placeholder="Введите запрос для выбранного специалиста..."></textarea>
          </div>
          <div class="grid grid-cols-3 gap-2">
            <button type="button" data-depth="express" class="depth-btn np-btn np-btn-outline py-2 px-2 text-xs font-medium active-depth">Краткий отчет</button>
            <button type="button" data-depth="deep" class="depth-btn np-btn np-btn-outline py-2 px-2 text-xs font-medium">Глубокий анализ</button>
            <button type="button" data-depth="structured" class="depth-btn np-btn np-btn-outline py-2 px-2 text-xs font-medium">Таблицы и схемы</button>
          </div>
          <div class="flex items-center gap-2.5 pt-1">
            <button id="btn-execute-task" class="np-btn np-btn-primary flex-1 py-2.5 px-4 text-sm">Запустить обработку</button>
            <button id="btn-clear-workspace" title="Очистить поле" class="np-btn np-btn-outline px-3 py-2.5 text-sm text-slate-300">Очистить</button>
          </div>
        </div>

        <div class="glass-panel p-5 rounded-xl space-y-3">
          <div class="flex items-center justify-between">
            <h3 class="text-sm font-semibold text-white">Блокнот артефактов и гипотез</h3>
            <span class="text-[11px] text-slate-400">Не сохраняется после перезагрузки</span>
          </div>
          <textarea id="scratchpad-notes" rows="4" class="w-full rounded-lg bg-slate-950/75 border border-slate-700/70 p-3 text-xs font-mono-tech text-slate-300 placeholder-slate-500 focus:outline-none" placeholder="Фиксируйте здесь улики, формулы, конспекты или параметры баланса..."></textarea>
        </div>
      </div>

      <div class="lg:col-span-7">
        <div class="glass-panel p-5 rounded-xl min-h-[480px] flex flex-col justify-between">
          <div>
            <div class="flex flex-wrap items-center justify-between gap-2 pb-3 mb-4 border-b border-slate-800">
              <div class="flex items-center gap-2.5">
                <span class="w-2.5 h-2.5 rounded-full" style="background-color: var(--accent-color);"></span>
                <h3 class="text-sm font-semibold text-white">Вывод модуля NocturnalPulse_4</h3>
              </div>
              <div class="flex items-center gap-2">
                <span id="status-indicator" class="text-xs font-mono-tech text-slate-400">ГОТОВ К РАБОТЕ</span>
                <button id="btn-copy-result" class="np-btn np-btn-outline px-2.5 py-1 text-xs">Копировать</button>
              </div>
            </div>
            <div id="output-container" class="prose-output text-sm space-y-3">
              <div class="p-4 rounded-lg bg-slate-900/75 border border-slate-800 space-y-2">
                <div class="text-xs font-mono-tech uppercase tracking-wider" style="color: var(--accent-color);">Системная инициализация завершена</div>
                <p class="text-slate-300 text-sm">Платформа <strong>NocturnalPulse_4</strong> загружена. Выберите специализацию, введите задачу и запустите обработку.</p>
              </div>
            </div>
          </div>
          <div class="mt-6 pt-3 border-t border-slate-800/80 flex flex-wrap items-center justify-between gap-2 text-[11px] font-mono-tech text-slate-400">
            <span id="footer-role-info">ПРОФИЛЬ: АНАЛИТИК ДАННЫХ</span>
            <span>ЯДРО: NOCTURNALPULSE_4 ENGINE</span>
          </div>
        </div>
      </div>
    </section>
  </main>

  <!-- Модальное окно добавления кнопки -->
  <div id="add-modal" class="fixed inset-0 z-50 hidden items-center justify-center p-4">
    <div id="add-backdrop" class="absolute inset-0 bg-black/70"></div>
    <div class="relative glass-panel rounded-xl p-5 w-full max-w-md space-y-3">
      <h2 class="text-base font-bold text-white">Новая быстрая команда</h2>
      <input id="new-btn-label" type="text" maxlength="30" placeholder="Название кнопки" class="w-full rounded-lg bg-slate-950/80 border border-slate-700/80 p-2.5 text-sm text-slate-100 focus:outline-none" />
      <textarea id="new-btn-text" rows="4" placeholder="Текст, который будет вставлен в поле задачи" class="w-full rounded-lg bg-slate-950/80 border border-slate-700/80 p-2.5 text-sm text-slate-100 focus:outline-none"></textarea>
      <div class="flex justify-end gap-2">
        <button id="btn-cancel-add" class="np-btn np-btn-outline px-3 py-2 text-sm">Отмена</button>
        <button id="btn-confirm-add" class="np-btn np-btn-primary px-3 py-2 text-sm">Добавить</button>
      </div>
    </div>
  </div>

  <!-- Панель настроек интерфейса -->
  <div id="customizer-drawer" class="fixed inset-0 z-50 hidden">
    <div id="customizer-backdrop" class="absolute inset-0 bg-black/70"></div>
    <aside class="absolute right-0 top-0 bottom-0 w-full max-w-md glass-panel border-l border-slate-700/80 p-6 overflow-y-auto space-y-6">
      <div class="flex items-center justify-between pb-3 border-b border-slate-800">
        <h2 class="text-base font-bold text-white">Конструктор интерфейса</h2>
        <button id="btn-close-customizer" class="p-1.5 rounded-lg text-slate-400 hover:text-white hover:bg-slate-800">✕</button>
      </div>

      <div class="space-y-3">
        <label class="block text-xs font-semibold text-slate-300 uppercase tracking-wider">Цветовая палитра акцента</label>
        <div class="grid grid-cols-5 gap-2" id="preset-colors"></div>
      </div>

      <div class="space-y-3">
        <label class="block text-xs font-semibold text-slate-300 uppercase tracking-wider">Стиль кнопок</label>
        <div class="grid grid-cols-2 gap-2">
          <button type="button" data-style="solid" class="style-btn np-btn np-btn-outline py-2 text-xs">Сплошной</button>
          <button type="button" data-style="neon" class="style-btn np-btn np-btn-outline py-2 text-xs">Неоновый контур</button>
        </div>
      </div>

      <div class="space-y-3">
        <label class="block text-xs font-semibold text-slate-300 uppercase tracking-wider">Затемнение фона: <span id="overlay-val" class="font-mono-tech text-slate-400"></span></label>
        <input id="overlay-range" type="range" min="0.3" max="0.95" step="0.01" class="w-full" />
      </div>

      <div class="space-y-3">
        <label class="block text-xs font-semibold text-slate-300 uppercase tracking-wider">Размытие фона: <span id="blur-val" class="font-mono-tech text-slate-400"></span>px</label>
        <input id="blur-range" type="range" min="0" max="12" step="1" class="w-full" />
      </div>

      <button id="btn-reset-ui" class="np-btn np-btn-outline w-full py-2 text-sm">Сбросить настройки</button>
    </aside>
  </div>

<script>
  const PALETTE = [
    { name: 'Циан', hex: '#00f0ff' },
    { name: 'Фиолетовый', hex: '#a78bfa' },
    { name: 'Изумрудный', hex: '#34d399' },
    { name: 'Розовый', hex: '#f472b6' },
    { name: 'Янтарный', hex: '#fbbf24' }
  ];

  const ROLES = [
    { id: 'analyst', name: 'Аналитик', footer: 'АНАЛИТИК ДАННЫХ', hint: 'Сводка, паттерны, выводы по данным' },
    { id: 'detective', name: 'Детектив', footer: 'ДЕТЕКТИВ', hint: 'Улики, версии, проверка гипотез' },
    { id: 'engineer', name: 'Инженер', footer: 'ИНЖЕНЕР', hint: 'Архитектура, код, расчёты' },
    { id: 'teacher', name: 'Учитель', footer: 'УЧИТЕЛЬ', hint: 'Объяснение темы с учётом уровня' },
    { id: 'expert', name: 'Эксперт', footer: 'ЭКСПЕРТ', hint: 'Оценка решения и рекомендации' },
    { id: 'custom', name: 'Своя роль', footer: 'СВОЯ РОЛЬ', hint: 'Задайте роль сами' }
  ];

  const DEPTH_LABELS = {
    express: 'РЕЖИМ: СВОДКА И ПАТТЕРНЫ',
    deep: 'РЕЖИМ: ГЛУБОКИЙ АНАЛИЗ',
    structured: 'РЕЖИМ: ТАБЛИЦЫ И СХЕМЫ'
  };

  const state = {
    role: 'analyst',
    depth: 'express',
    teacherLevel: 'школа',
    customRoleName: '',
    buttons: [
      { id: 1, label: 'Резюме', text: 'Сделай краткое резюме следующего материала:\n' },
      { id: 2, label: 'Гипотезы', text: 'Предложи возможные версии и способы их проверки для:\n' },
      { id: 3, label: 'Риски', text: 'Составь таблицу рисков и мер снижения для:\n' }
    ],
    nextBtnId: 4
  };

  const $ = (id) => document.getElementById(id);
  const esc = (s) => String(s).replace(/[&<>"']/g, c => ({ '&': '&amp;', '<': '&lt;', '>': '&gt;', '"': '&quot;', "'": '&#39;' }[c]));

  function hexToRgb(hex) {
    const n = parseInt(hex.slice(1), 16);
    return `${(n >> 16) & 255}, ${(n >> 8) & 255}, ${n & 255}`;
  }

  function applyAccent(hex) {
    document.documentElement.style.setProperty('--accent-color', hex);
    document.documentElement.style.setProperty('--accent-rgb', hexToRgb(hex));
    document.querySelectorAll('.preset-btn').forEach(b => {
      b.style.outline = b.dataset.color === hex ? `2px solid ${hex}` : 'none';
    });
  }

  function renderPalette() {
    $('preset-colors').innerHTML = PALETTE.map(p =>
      `<button type="button" class="preset-btn h-10 rounded-lg border border-slate-700" title="${p.name}" data-color="${p.hex}" style="background:${p.hex}"></button>`
    ).join('');
    document.querySelectorAll('.preset-btn').forEach(b =>
      b.addEventListener('click', () => { applyAccent(b.dataset.color); saveNothing(); })
    );
  }

  function renderRoles() {
    $('roles-grid').innerHTML = ROLES.map(r => `
      <button type="button" data-role="${r.id}" class="role-card p-3 text-left ${state.role === r.id ? 'active' : ''}">
        <div class="text-sm font-semibold text-white">${esc(r.id === 'custom' && state.customRoleName ? state.customRoleName : r.name)}</div>
        <div class="text-[11px] text-slate-400 mt-1">${esc(r.hint)}</div>
      </button>`).join('');
    document.querySelectorAll('.role-card').forEach(c =>
      c.addEventListener('click', () => selectRole(c.dataset.role))
    );
    renderSubpanel();
  }

  function selectRole(id) {
    state.role = id;
    const role = ROLES.find(r => r.id === id);
    $('active-role-badge').textContent = 'Модуль: ' + (id === 'custom' && state.customRoleName ? state.customRoleName : role.name);
    $('footer-role-info').textContent = 'ПРОФИЛЬ: ' + role.footer;
    renderRoles();
  }

  function renderSubpanel() {
    const panel = $('role-subpanel');
    if (state.role === 'teacher') {
      panel.classList.remove('hidden');
      panel.innerHTML = `
        <label class="block text-xs text-slate-400 mb-2">Уровень объяснения:</label>
        <select id="teacher-level" class="w-full rounded-lg bg-slate-950/80 border border-slate-700/80 p-2.5 text-sm text-slate-100">
          ${['школа', 'студент', 'профессионал'].map(l => `<option ${l === state.teacherLevel ? 'selected' : ''}>${l}</option>`).join('')}
        </select>`;
      $('teacher-level').addEventListener('change', e => state.teacherLevel = e.target.value);
    } else if (state.role === 'custom') {
      panel.classList.remove('hidden');
      panel.innerHTML = `
        <label class="block text-xs text-slate-400 mb-2">Название вашей роли:</label>
        <input id="custom-role-name" type="text" maxlength="30" value="${esc(state.customRoleName)}" placeholder="Например: Редактор" class="w-full rounded-lg bg-slate-950/80 border border-slate-700/80 p-2.5 text-sm text-slate-100 focus:outline-none" />`;
      $('custom-role-name').addEventListener('input', e => {
        state.customRoleName = e.target.value.trim();
        $('active-role-badge').textContent = 'Модуль: ' + (state.customRoleName || 'Своя роль');
        $('footer-role-info').textContent = 'ПРОФИЛЬ: ' + (state.customRoleName.toUpperCase() || 'СВОЯ РОЛЬ');
      });
    } else {
      panel.classList.add('hidden');
      panel.innerHTML = '';
    }
  }

  function renderButtons() {
    $('custom-buttons-container').innerHTML = state.buttons.map(b => `
      <span class="inline-flex items-center rounded-lg border border-slate-700/80 bg-slate-900/70 text-sm">
        <button type="button" data-insert="${b.id}" class="px-3 py-1.5 text-slate-100 hover:text-white">${esc(b.label)}</button>
        <but
