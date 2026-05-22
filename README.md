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
{ // ----------------- PAGE 2 (Rurik biography, as you provided) -----------------
            title: "留里克（862–879年在位的罗斯王公）",
            contentHTML: `
                <p>9世纪后半叶初期 ，一位维京首领成为了伊利门斯洛文人部落联盟的领袖，编年史中称其为留里克。留里克的出身至今仍笼罩在谜团之中。一部分当代研究者将他与著名的丹麦国王——日德兰的罗里克（Rørik of Jutland）视为同一人。但也有一种说法认为，这位罗斯人的首领出身于西斯拉夫中的波拉布斯拉夫人。</p>
                <p>关于传奇人物留里克，流传至今的记载并不多。然而，他被公认为是罗斯第一个统治王朝的始祖，这个王朝在罗斯的历史与文化中发挥了关键作用。留里克的身世之谜留里克的出身一直是个谜。根据《往年纪事》的说法，瓦良格人留里克在862年接到罗斯西北部各部落的邀请，带着兄弟西涅乌斯和特鲁沃尔“从海外”前来做他们的王公。</p>
                <p>传说中，他和当地一些斯拉夫族的长老还有亲戚关系。“瓦良格人”这个词在当时用来称呼那些当雇佣兵的人，所以光凭这个称号，很难判断留里克到底是哪个民族的人。</p>
                <p>有人觉得留里克是斯堪的纳维亚的维京人，也有人认为他是来自波罗的海南岸、属于西斯拉夫王公家族的后代。 编年史把他归为“瓦良格-罗斯人”，并且提到在瓦良格人当中，除了罗斯人，还有挪威人、瑞典人、哥特兰岛人、英国人等。</p>
                <p>写这部编年史的作者生活在这些事件发生两百五十年之后，但他很肯定地认为，是留里克带来了“所有罗斯人”。</p>
                <p>留里克有个儿子叫伊戈尔，也就是后来的罗斯王公，他是在留里克去世前不久出生的。关于孩子的母亲，历史上没有留下任何记载。</p>
            `
        },
{ // PAGE 3 · Igor (912–945)
    title: "912–945年在位的罗斯王公",
    contentHTML: `
        <p>伊戈尔王公在历史上留下的名声并不好。他远征拜占庭时，对当地希腊平民犯下了血腥的暴行。他贪得无厌，不断对臣服于他的斯拉夫人施加暴力和压迫。</p>
        <p>留里克的儿子伊戈尔在父亲去世时还是个孩子。《往年纪事》提到，伊戈尔在婴儿时期就已经在基辅即位，不过编年史并没有记载他确切的出生年份。</p>
        <blockquote>“你们不是王公，也不是王公家族的人，而我才是王公家族的。这个孩子是留里克的儿子。”<br>——《往年纪事》中奥列格王公对基辅人所说的话</blockquote>
        <p>据编年史记载，留里克去世时，他的儿子伊戈尔还“非常年幼”，因此王公的权力转交给了留里克的亲属奥列格，由奥列格担任伊戈尔的抚养人。即便伊戈尔成年之后，也仍然事事听从自己的监护人，直到奥列格去世，他才真正掌握了实权。</p>
        <p>伊戈尔王公曾镇压过德列夫利安人，也跟佩切涅格人打过仗并议和。941年，他大举进攻君士坦丁堡，但以失败告终。《往年纪事》中记载了俄军将士归来后的话：</p>
        <blockquote>“希腊人手里仿佛有一种天上的闪电，他们放出这种闪电，烧毁了我们；所以我们没能战胜他们。”</blockquote>
        <p>在君士坦丁堡遭受巨大损失之后，伊戈尔被迫撤退。拜占庭人趁机停止支付贡款。但到了944年，这位罗斯王公与佩切涅格人结盟，再次组织了对君士坦丁堡的远征。</p>
        <p>拜占庭皇帝罗曼一世没有等到罗斯军队入侵，就主动与罗斯签订了和约，同意增加缴纳的贡款。伊戈尔王公的亲兵们劝他，用向自己属民加征税赋的方式来弥补没能在战争中抢到的战利品。</p>
        <p>在索贡巡行（王公每年到各地征收贡赋的行程）期间，伊戈尔从德列夫利安人那里多征收了一倍的贡品，之后还不罢休，继续强征暴敛。愤怒的德列夫利安人起义反抗，杀死了伊戈尔。</p>
    `
}
{ // PAGE 4 · Oleg (879–912)
    title: "先知奥列格（879–912年在位的罗斯王公）",
    contentHTML: `
        <p>大公奥列格无疑是古罗斯历史上最引人入胜的英雄人物之一。编年史把他描写成一个极其敏锐、狡猾的人——正是凭借这些本事，他攻占了基辅，成功远征君士坦丁堡，并与拜占庭人缔结了有利的和约。</p>
        <p>奥列格这个名字因为俄罗斯文学而为我们所熟知。他在留里克去世后成为罗斯的统治者。据编年史记载，奥列格是年幼的伊戈尔的监护人，但他行事完全像一位拥有全权的王公，而不仅仅是当个摄政。</p>
        <p>即使在留里克的儿子长大成人之后，奥列格依然是罗斯的统治者。奥列格掌权后不久便攻占了基辅，并将自己的驻地迁到了那里。他率领瓦良格人、楚德人、斯洛文人、维斯人、梅里亚人和克里维奇人前来基辅。随后，他又征服了周围的谢韦里安人和拉迪米奇人——这些部落此前一直向哈扎尔汗国缴纳贡赋。</p>
        <p>编年史在907年的条目下记载了奥列格王公远征君士坦丁堡的辉煌胜利，这次征战以他将盾牌插在“皇城（君士坦丁堡）的大门上”而告终。</p>
        <p>这个传奇故事令不少历史学家为之惊叹——奥列格组织远征时，调动了所有斯拉夫部落、瓦良格人，甚至还包括楚德人和梅里亚人，规模之大非同寻常。不过，也有学者怀疑这样的事是否真有可能发生。</p>
        <p>但无论如何，正是奥列格王公把不同族群统一到自己的统治之下，为后来《往年纪事》中所称的“罗斯民族”这一社会政治共同体奠定了基础。</p>
    `
}
     { // PAGE 5 · Olga (945–962)
    title: "奥丽加女大公（945–962年在位；969年去世）",
    contentHTML: `
        <p>奥丽加女大公最初是以铁腕镇压德列夫利安人的形象走入罗斯历史的。然而，正是这位曾经一心复仇的异教女子，却注定成为留里克家族中第一个接受基督教洗礼的人，并最终赢得了真正虔诚的基督徒的声誉。</p>
        <p>奥丽加是在丈夫伊戈尔死后开始统治罗斯的。945年，伊戈尔被德列夫利安人杀害。当时她的儿子斯维亚托斯拉夫尚且年幼，而奥丽加本人则展现出一位果断而有远见的统治者的才干，无论在国内还是国外都赢得了尊敬。</p>
        <p>关于奥丽加的身世，流传下来的说法充满传奇色彩，而且彼此矛盾。 有的说她出身于显赫的斯拉夫家族，有的说她是先知奥列格的女儿，还有的说她只是一个贫穷的瓦良格家庭的姑娘。</p>
        <p>奥列格大公把她嫁给了伊戈尔。伊戈尔非常珍视和敬重她，因为奥丽加为人明理、聪慧。</p>
        <blockquote>“奥丽加俯身朝向坑中，问他们：‘这份荣耀你们满意吗？’ 他们回答说：‘伊戈尔的死还不如此。’ 奥丽加便下令把他们活活埋掉。于是人们把他们填埋了……”<br>——《往年纪事》</blockquote>
        <p>奥丽加为夫报仇，对德列夫利安人施以了残酷的报复。她下令将在基辅的德列夫利安使节全部杀死，随后率军征讨德列夫利安人，并将他们击败。德列夫利安人的首府伊斯科罗斯滕被焚毁，幸存的居民被迫缴纳沉重的贡赋。</p>
    `
}
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
