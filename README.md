<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
    <title>Chronicle of the Rus' - 12 Pages</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: #eef2f0;
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            font-family: 'SimSun', '宋体', 'Times New Roman', serif;
            font-size: 12px;
            line-height: 1.6;
            padding: 1.5rem;
        }

        /* main card container */
        .site-container {
            max-width: 880px;
            width: 100%;
            background: #fffef7;
            border-radius: 24px;
            box-shadow: 0 20px 35px -12px rgba(0, 0, 0, 0.2);
            overflow: hidden;
            transition: all 0.2s;
        }

        /* content area */
        .page-wrapper {
            padding: 2.2rem 2.5rem;
        }

        /* title style */
        .page-title {
            font-family: 'SimSun', '宋体', serif;
            font-size: 22px;
            font-weight: 600;
            letter-spacing: 1px;
            color: #2c3e2f;
            border-left: 5px solid #b87333;
            padding-left: 18px;
            margin-bottom: 1.8rem;
            margin-top: 0;
            line-height: 1.3;
        }

        /* text content */
        .page-text {
            font-family: 'SimSun', '宋体', serif;
            font-size: 12px;
            color: #1e2a1c;
            text-align: justify;
            word-break: break-word;
            margin-bottom: 2rem;
        }

        .page-text p {
            margin-bottom: 1.1em;
        }

        .page-text blockquote {
            margin: 1em 0;
            padding-left: 1.2em;
            border-left: 3px solid #b87333;
            color: #3c4b3a;
            font-style: normal;
            background: #faf8f0;
            padding: 0.8em 1.2em;
            border-radius: 12px;
        }

        /* navigation bar */
        .nav-bar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1rem 2rem 1.8rem 2rem;
            background: #fffef7;
            border-top: 1px solid #e0dbcf;
            flex-wrap: wrap;
            gap: 12px;
        }

        .nav-buttons {
            display: flex;
            gap: 20px;
        }

        .arrow-btn {
            background: #f4f1e6;
            border: none;
            font-size: 28px;
            font-weight: normal;
            width: 56px;
            height: 56px;
            border-radius: 40px;
            cursor: pointer;
            display: inline-flex;
            align-items: center;
            justify-content: center;
            transition: all 0.2s ease;
            color: #3c5e3a;
            box-shadow: 0 2px 5px rgba(0,0,0,0.05);
            font-family: monospace;
        }

        .arrow-btn:hover:not(:disabled) {
            background: #e3daca;
            transform: scale(0.96);
            color: #1d2f1b;
        }

        .arrow-btn:disabled {
            opacity: 0.35;
            cursor: not-allowed;
            background: #eae7df;
        }

        .page-indicator {
            font-family: 'SimSun', '宋体', monospace;
            font-size: 13px;
            background: #f0ede5;
            padding: 8px 18px;
            border-radius: 40px;
            color: #3e5a39;
            letter-spacing: 0.5px;
            font-weight: 500;
        }

        /* small hint for editing */
        .edit-hint {
            font-family: 'SimSun', '宋体', monospace;
            font-size: 10px;
            text-align: center;
            padding: 12px 20px 16px;
            background: #faf9f3;
            color: #8b7a66;
            border-top: 1px solid #ede7db;
            letter-spacing: 0.3px;
        }

        .edit-hint code {
            background: #e9e5db;
            padding: 2px 8px;
            border-radius: 20px;
            font-family: monospace;
            font-size: 10px;
            color: #b1622c;
        }

        @media (max-width: 580px) {
            .page-wrapper {
                padding: 1.6rem;
            }
            .arrow-btn {
                width: 48px;
                height: 48px;
                font-size: 24px;
            }
            .page-title {
                font-size: 18px;
            }
        }
    </style>
</head>
<body>
<div class="site-container">
    <div class="page-wrapper">
        <h1 class="page-title" id="dynamicTitle">内乱</h1>
        <div class="page-text" id="dynamicText">
            <!-- content injected from js -->
        </div>
    </div>
    <div class="nav-bar">
        <div class="nav-buttons">
            <button class="arrow-btn" id="prevBtn" aria-label="Previous page">←</button>
            <button class="arrow-btn" id="nextBtn" aria-label="Next page">→</button>
        </div>
        <div class="page-indicator" id="pageIndicator">Page 1 / 12</div>
    </div>
    <div class="edit-hint">
        ⚡ EDIT PAGES: modify <code>pagesData</code> array inside script → 12 entries (title + html content)
    </div>
</div>

<script>
    // --------------------------------------------------------------
    // 12 PAGES DATA - Replace title & contentHTML for each page.
    // Page 1 is pre-filled with the required historical text.
    // Pages 2..12 are placeholders — replace with your own text.
    // --------------------------------------------------------------
    const pagesData = [
        { // page 1
            title: "内乱",
            contentHTML: `
                <p>谁做主的问题，成为东斯拉夫部落联盟内部纷争的原因。这个成为‘争端焦点’的权力，决定交给瓦良格人中的罗斯部落。据编年史记载，公元862年，发生了传奇性的‘邀请瓦良格人’事件。<br>某些斯拉夫部落之间时而相互敌对和征战。</p>
                <p>九世纪中期，将瓦良格人从西北地区驱逐出去并未给当地部落带来期盼的安宁，内部的争斗反而更加激烈。</p>
                <blockquote>“……他们中间没有公义，宗族起而对抗宗族，内讧不断，于是彼此攻战。他们对自己说：‘我们要寻找一位王公，由他来治理我们，并按公义审判我们。’于是他们渡海前往瓦良格人那里，去到罗斯人那里。</blockquote>
                <p>楚德人、斯洛文人、克里维奇人和с维斯人对罗斯人说：“我们的土地辽阔富饶，可是其中没有秩序。请你们来为王并统治我们吧。</p>
                <p>于是三位兄弟带着各自的宗族被推选出来，他们带上了全体罗斯人，便前来了。</p>
                <blockquote>——年长的留里克坐镇于诺夫哥罗德，另一位西涅乌斯坐镇于白湖，第三位特鲁沃尔坐镇于伊兹博尔斯克。”<br>——《往年纪事》，12世纪</blockquote>
                <p>没有任何一个部落拥有征服邻国的力量，但自身也不愿被征服。继续内讧直至彼此耗竭，或者彻底分道扬镳，都将面临丧失独立的危险。走出这一困境的办法是围绕“第三方力量”实现联合——这支力量既是外来的，又是他们所熟悉的，且不威胁到自由。</p>
                <p>为了寻求一个统一而强大的政权，斯拉夫人及其邻近的芬兰部落派出了使团，前往不久前被他们驱逐的瓦良格人那里，请求从他们中间推举一位王公来统治他们：“我们的土地辽阔富饶，可是其中没有秩序。请你们来为王并统治我们吧。”</p>
                <p>响应这一提议的留里克证明了自己不负所召——他不仅在罗斯稳固了统治，还开创了一个王朝，该王朝统治罗斯长达七个世纪。</p>
            `
        },
        { // page 2 — placeholder (replace)
            title: "Page 2 · Assembly of Tribes",
            contentHTML: `<p><strong>Placeholder text — replace with your own content.</strong> Here you can write any historical notes, analysis, or extended narrative. Use paragraphs, blockquotes or simple HTML.</p><p>Example: The invitation of the Varangians marked a turning point in Eastern Slavic history. You may continue the chronicle or insert new topics.</p>`
        },
        { // page 3
            title: "Page 3 · Legacy of Riurik",
            contentHTML: `<p>[Replace this text] Describe the rise of the Riurikid dynasty. Add citations, reflections or secondary sources. Keep the font family SimSun as required. This is page 3 of 12. You can edit freely.</p>`
        },
        { // page 4
            title: "Page 4 · Early Rus' society",
            contentHTML: `<p>Custom text for page four. Insert your own research, medieval trade routes, or political structures. The navigation arrows allow full browsing across all 12 pages.</p>`
        },
        { // page 5
            title: "Page 5 · Cultural influences",
            contentHTML: `<p>Page 5: Fill with relevant content — Slavic, Finnish, Varangian interactions. Use bold, italics, or blockquotes as you wish. The design is clean and classic.</p>`
        },
        { // page 6
            title: "Page 6 · Chronicles & sources",
            contentHTML: `<p>Primary Chronicle (Tale of Bygone Years) is the key source. Write down your own translation fragments or analytical comments. This is page six.</p>`
        },
        { // page 7
            title: "Page 7 · Inter-tribal diplomacy",
            contentHTML: `<p>Placeholder for page 7. Explore the role of the veche, treaties, or the consolidation around Novgorod. Replace with your narrative or references.</p>`
        },
        { // page 8
            title: "Page 8 · Shifts of power",
            contentHTML: `<p>Page 8: Discuss the expansion from Ladoga to the Dnieper, or the relationship with Khazars. Your text goes here — maintain clarity and academic tone.</p>`
        },
        { // page 9
            title: "Page 9 · Material culture",
            contentHTML: `<p>This is page nine. Insert descriptions of archaeological findings, burial mounds, or early urban centers. SimSun 12px applies to all content.</p>`
        },
        { // page 10
            title: "Page 10 · Religious transformations",
            contentHTML: `<p>Page 10 placeholder: Pre-Christian beliefs, the future adoption of Christianity. Write your own insights, quotations or hypotheses.</p>`
        },
        { // page 11
            title: "Page 11 · Dynastic continuity",
            contentHTML: `<p>Here you can continue the royal lineage after Riurik. Oleg, Igor, Olga — adapt this chapter with your preferred level of detail. Page 11 of 12.</p>`
        },
        { // page 12
            title: "Page 12 · Conclusion / Aftermath",
            contentHTML: `<p>Final page: Summarize the invitation of the Varangians and its long-term consequences. The Riurikid dynasty ruled for seven centuries — you may extend the story or add bibliography. This is the last page.</p>`
        }
    ];

    // Ensure we have exactly 12 pages (safety)
    while(pagesData.length < 12) {
        pagesData.push({ title: "Extra Page", contentHTML: "<p>Add your content here.</p>" });
    }
    if(pagesData.length > 12) pagesData.length = 12;

    // DOM elements
    const titleEl = document.getElementById('dynamicTitle');
    const textEl = document.getElementById('dynamicText');
    const prevBtn = document.getElementById('prevBtn');
    const nextBtn = document.getElementById('nextBtn');
    const indicator = document.getElementById('pageIndicator');

    let currentIdx = 0;      // 0-based index (0 = page 1)

    function renderPage() {
        const page = pagesData[currentIdx];
        if (page) {
            titleEl.textContent = page.title;
            textEl.innerHTML = page.contentHTML;
        } else {
            // fallback (should not happen)
            titleEl.textContent = "Page";
            textEl.innerHTML = "<p>Content missing. Edit pagesData array.</p>";
        }
        indicator.textContent = `Page ${currentIdx+1} / ${pagesData.length}`;

        // update disabled state for arrows
        prevBtn.disabled = (currentIdx === 0);
        nextBtn.disabled = (currentIdx === pagesData.length - 1);
    }

    // Event listeners
    function goPrev() {
        if (currentIdx > 0) {
            currentIdx--;
            renderPage();
            window.scrollTo({ top: 0, behavior: 'smooth' });
        }
    }

    function goNext() {
        if (currentIdx < pagesData.length - 1) {
            currentIdx++;
            renderPage();
            window.scrollTo({ top: 0, behavior: 'smooth' });
        }
    }

    prevBtn.addEventListener('click', goPrev);
    nextBtn.addEventListener('click', goNext);

    // optional keyboard support (left/right arrows)
    window.addEventListener('keydown', (e) => {
        if (e.key === 'ArrowLeft') {
            e.preventDefault();
            goPrev();
        } else if (e.key === 'ArrowRight') {
            e.preventDefault();
            goNext();
        }
    });

    // initial render
    renderPage();
</script>
</body>
</html>
