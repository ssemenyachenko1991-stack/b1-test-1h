# Блок «Быстрая заявка» для основного сайта Б1

## Что заменить на основном сайте

Внизу сайта, в разделе **«НА СВЯЗИ СЕРГЕЙ · Б1 / Ваш потолок. Начнём с разговора.»** (`section#contact`), есть кнопка:

```html
<button class="text-link request-link" data-open>Подготовить заявку на замер ↗</button>
```

Замени **только эту кнопку** на код ниже целиком, от строки `БЛОК «БЫСТРАЯ ЗАЯВКА» — НАЧАЛО` до строки `КОНЕЦ`. Остальной сайт не трогай. Стили и скрипт уже внутри блока и на другие части сайта не влияют.

## Что написать в чат ChatGPT, где делался сайт

> На сайте в разделе #contact замени кнопку «Подготовить заявку на замер ↗» (button.request-link) на этот HTML-блок без изменений. Остальной сайт не меняй.

Дальше вставь весь код ниже.

## Что внутри блока

- Поля: «Как к вам обращаться», «Где находится объект», «Когда планируете», «Пожелания», галочка «Приложить расчёт из калькулятора», кнопка «Подготовить сообщение».
- После нажатия появляется готовый текст и кнопки: «Отправить заявку в WhatsApp», «Скопировать сообщение», «Написать в MAX», «Посмотреть работы в Telegram», «Позвонить +7 977 652-75-51».
- Подсказка: «Сайт ничего не отправляет сам. Вы получите готовый текст и отправите его в мессенджере».
- Запасная ссылка «Написать Сергею в WhatsApp напрямую».
- MAX: https://max.ru/u/f9LHodD0cOKmITu1JuSYRtmkaH4LT0gV350fSKxzlEHObgk7OSmHMTjANTQ

## Код блока

```html
<!-- ===== Б1: БЛОК «БЫСТРАЯ ЗАЯВКА» — НАЧАЛО ===== -->
<div class="b1q" id="b1q">
<style>
.b1q{--b1q-acc:#c9a46a;max-width:560px;margin:28px 0;padding:24px;border:1px solid rgba(255,255,255,.18);border-radius:14px;background:rgba(255,255,255,.04);color:inherit;font:inherit;text-align:left}
.b1q *{box-sizing:border-box}
.b1q-eyebrow{display:block;font-size:12px;letter-spacing:.12em;opacity:.7;margin-bottom:6px}
.b1q h3{margin:0 0 6px;font-size:22px;line-height:1.2}
.b1q-hint{font-size:14px;opacity:.75;margin:0 0 16px}
.b1q label{display:block;font-size:14px;margin:12px 0 6px}
.b1q input[type=text],.b1q textarea{width:100%;padding:12px 14px;font:inherit;font-size:16px;color:inherit;background:rgba(0,0,0,.25);border:1px solid rgba(255,255,255,.25);border-radius:10px}
.b1q textarea{min-height:90px;resize:vertical}
.b1q-check{display:flex!important;gap:10px;align-items:center}
.b1q-check input{width:20px;height:20px;margin:0}
.b1q-btn{display:block;width:100%;margin:10px 0 0;padding:14px 16px;font:inherit;font-size:16px;font-weight:600;text-align:center;text-decoration:none;border-radius:10px;cursor:pointer;border:1px solid var(--b1q-acc);background:transparent;color:#f3efe8}
.b1q-main{background:var(--b1q-acc);color:#111;border-color:var(--b1q-acc)}
.b1q-wa{background:#25d366;color:#08240f;border-color:#25d366}
.b1q-link{background:none;border:0;padding:10px 0;color:inherit;opacity:.8;text-decoration:underline;width:auto}
.b1q-status{font-size:14px;min-height:1.2em;margin:10px 0 0;opacity:.85}
.b1q-fallback{font-size:14px;margin:16px 0 0;opacity:.85}
.b1q-fallback a{color:inherit}
</style>
<span class="b1q-eyebrow">БЫСТРАЯ ЗАЯВКА</span>
<h3>Подготовьте сообщение Сергею</h3>
<p class="b1q-hint">Сайт ничего не отправляет сам. Вы получите готовый текст и отправите его в мессенджере.</p>
<form id="b1q-form" novalidate>
<label for="b1q-name">Как к вам обращаться</label>
<input type="text" id="b1q-name" name="name" autocomplete="name" placeholder="Например, Анна">
<label for="b1q-place">Где находится объект</label>
<input type="text" id="b1q-place" name="place" placeholder="Город, район или ЖК; квартира или дом">
<label for="b1q-when">Когда планируете</label>
<input type="text" id="b1q-when" name="when" placeholder="Например, в течение месяца">
<label for="b1q-details">Пожелания</label>
<textarea id="b1q-details" name="details" placeholder="Комнаты, свет, карнизы — всё, что важно"></textarea>
<label class="b1q-check"><input type="checkbox" id="b1q-calc"> Приложить расчёт из калькулятора</label>
<button type="submit" class="b1q-btn b1q-main">Подготовить сообщение</button>
</form>
<div id="b1q-ready" hidden>
<label for="b1q-msg">Ваше сообщение Сергею</label>
<textarea id="b1q-msg" readonly></textarea>
<a id="b1q-wa" class="b1q-btn b1q-wa" href="https://wa.me/79776527551" target="_blank" rel="noopener">Отправить заявку в WhatsApp ↗</a>
<button type="button" id="b1q-copy" class="b1q-btn">Скопировать сообщение</button>
<a class="b1q-btn" href="https://max.ru/u/f9LHodD0cOKmITu1JuSYRtmkaH4LT0gV350fSKxzlEHObgk7OSmHMTjANTQ" target="_blank" rel="noopener">Написать в MAX ↗</a>
<a class="b1q-btn" href="https://t.me/Potolkl_B1" target="_blank" rel="noopener">Посмотреть работы в Telegram ↗</a>
<a class="b1q-btn" href="tel:+79776527551">Позвонить +7 977 652-75-51</a>
<p class="b1q-status" id="b1q-status">Нажмите «Отправить заявку в WhatsApp» — текст уже готов. Для MAX скопируйте сообщение и вставьте в переписку.</p>
<button type="button" id="b1q-edit" class="b1q-btn b1q-link">← Изменить данные</button>
</div>
<p class="b1q-fallback">Не срабатывает кнопка? <a href="https://wa.me/79776527551?text=%D0%97%D0%B4%D1%80%D0%B0%D0%B2%D1%81%D1%82%D0%B2%D1%83%D0%B9%D1%82%D0%B5%2C%20%D0%A1%D0%B5%D1%80%D0%B3%D0%B5%D0%B9!%20%D0%A5%D0%BE%D1%87%D1%83%20%D0%BE%D0%B1%D1%81%D1%83%D0%B4%D0%B8%D1%82%D1%8C%20%D0%BD%D0%B0%D1%82%D1%8F%D0%B6%D0%BD%D1%8B%D0%B5%20%D0%BF%D0%BE%D1%82%D0%BE%D0%BB%D0%BA%D0%B8%20%D0%911." target="_blank" rel="noopener">Написать Сергею в WhatsApp напрямую ↗</a></p>
<script>
(function(){
var $=function(id){return document.getElementById(id)};
var form=$('b1q-form'),ready=$('b1q-ready'),msg=$('b1q-msg'),st=$('b1q-status');
var HINT='Нажмите «Отправить заявку в WhatsApp» — текст уже готов. Для MAX скопируйте сообщение и вставьте в переписку.';
function v(id){var x=$(id).value.trim();return x||'—'}
function calcText(){
 try{if(typeof estimateText!=='undefined'&&estimateText)return estimateText}catch(e){}
 var r=document.getElementById('result'),b=document.getElementById('breakdown');
 var t=((r&&r.innerText)||'')+'\n'+((b&&b.innerText)||'');t=t.trim();
 return t?('Предварительный расчёт Б1\n'+t):'';
}
form.addEventListener('submit',function(e){
 e.preventDefault();
 var text='Здравствуйте, Сергей! Хочу обсудить натяжные потолки Б1.\nИмя: '+v('b1q-name')+'\nОбъект: '+v('b1q-place')+'\nСроки: '+v('b1q-when')+'\nПожелания: '+v('b1q-details');
 if($('b1q-calc').checked){var c=calcText();if(c)text+='\n\n'+c;}
 text+='\n\nДавайте согласуем замер.';
 msg.value=text;
 $('b1q-wa').href='https://wa.me/79776527551?text='+encodeURIComponent(text);
 st.textContent=HINT;form.hidden=true;ready.hidden=false;
 ready.scrollIntoView({behavior:'smooth',block:'start'});
});
$('b1q-copy').addEventListener('click',function(){
 var t=msg.value;
 function ok(){st.textContent='Скопировано. Вставьте в переписку с Сергеем.'}
 function old(){msg.focus();msg.select();try{document.execCommand('copy');ok()}catch(e){st.textContent='Выделите текст выше и скопируйте вручную.'}}
 if(navigator.clipboard&&window.isSecureContext){navigator.clipboard.writeText(t).then(ok,old)}else{old()}
});
$('b1q-edit').addEventListener('click',function(){ready.hidden=true;form.hidden=false;form.scrollIntoView({behavior:'smooth',block:'start'})});
})();
</script>
</div>
<!-- ===== Б1: БЛОК «БЫСТРАЯ ЗАЯВКА» — КОНЕЦ ===== -->
```
