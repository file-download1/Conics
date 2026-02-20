<!DOCTYPE html>
<html lang="bn">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>কনিক ডিজিটাল নোট</title>
    <!-- ফন্ট: হিন্দ সিলিগুড়ি -->
    <link href="https://fonts.googleapis.com/css2?family=Hind+Siliguri:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    
    <!-- ম্যাথ সিম্বল (শুধু ইংরেজি চলকের জন্য) -->
    <script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
    <script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>

    <style>
        :root {
            --blue-border: #0984e3;
            --text-main: #2d3436;
            --text-red: #d63031;
            --grid-color: #e3e3e3;
        }

        body {
            background-color: white; /* ব্যাকগ্রাউন্ড সাদা */
            margin: 0;
            padding: 0;
            font-family: 'Hind Siliguri', sans-serif;
            color: var(--text-main);
        }

        /* A4 সাইজ পেজ সেটআপ */
        .page {
            width: 210mm;
            min-height: 297mm;
            margin: 0 auto;
            padding: 40px 50px;
            box-sizing: border-box;
            position: relative;
            /* ডট গ্রিড */
            background-image: radial-gradient(var(--grid-color) 1.5px, transparent 1.5px);
            background-size: 25px 25px;
            page-break-after: always;
            display: flex;
            flex-direction: column;
        }

        /* 3D শিরোনাম বক্স */
        .title-box {
            text-align: center;
            font-size: 22px;
            font-weight: 700;
            color: var(--text-main);
            border: 2px solid var(--blue-border);
            padding: 10px 25px;
            width: fit-content;
            margin: 0 auto 30px auto;
            border-radius: 8px;
            background: white;
            box-shadow: 4px 4px 0px rgba(9, 132, 227, 0.2); /* 3D Shadow */
        }

        h3 {
            color: #0044cc;
            border-bottom: 2px dashed #b2bec3;
            padding-bottom: 5px;
            margin-top: 25px;
            font-size: 18px;
            margin-bottom: 10px;
        }

        ul { margin: 5px 0; padding-left: 20px; }
        li { margin-bottom: 5px; font-weight: 500; }

        /* বাংলা ভগ্নাংশ ফিক্স (Custom Math Look) */
        .math-expr {
            display: inline-flex;
            align-items: center;
            font-family: 'Hind Siliguri', sans-serif;
            font-size: 18px;
            margin: 10px 0;
            background: #fdfdfd;
            padding: 5px 10px;
            border-radius: 5px;
            border: 1px solid #eee;
        }
        
        .fraction {
            display: inline-flex;
            flex-direction: column;
            align-items: center;
            vertical-align: middle;
            margin: 0 5px;
        }
        
        .fraction .top {
            border-bottom: 2px solid black;
            padding-bottom: 2px;
            text-align: center;
        }
        
        .fraction .bottom {
            padding-top: 2px;
            text-align: center;
        }

        .abs-bar {
            font-size: 30px;
            font-weight: 300;
            margin: 0 5px;
            color: #444;
        }

        .highlight-red { color: var(--text-red); font-weight: bold; font-size: 0.9em; }
        .box-note {
            border: 1px solid #0044cc;
            background-color: rgba(0, 68, 204, 0.05);
            padding: 8px;
            border-radius: 5px;
            text-align: center;
            margin: 10px 0;
            width: fit-content;
        }

        /* তুলনা ছক */
        .comp-table {
            width: 100%;
            border-collapse: collapse;
            border: 2px solid var(--text-main);
            margin-top: 10px;
        }
        .comp-table td {
            width: 50%;
            border: 1px solid var(--text-main); /* মাঝখানের দাগ */
            padding: 15px;
            vertical-align: top;
        }
        .header-cell {
            text-align: center;
            background-color: #f0f0f0;
            font-weight: bold;
            border-bottom: 2px solid var(--text-main);
            padding: 8px;
        }

        /* ফুটার ডিজাইন */
        .footer-spacer {
            flex-grow: 1; /* এটি কন্টেন্ট এবং ফুটারের মাঝে জায়গা নিবে */
        }
        .footer-box {
            text-align: right;
            font-size: 13px;
            color: #555;
            border-top: 2px solid var(--blue-border);
            padding-top: 10px;
            margin-top: 30px;
            background: rgba(255,255,255,0.9);
        }
        .footer-box strong { color: var(--blue-border); }

        /* প্রিন্ট ফিক্স */
        @media print {
            body { background: white; }
            .page { margin: 0; box-shadow: none; border: none; height: 100vh; }
        }
    </style>
</head>
<body>

    <!-- ================= পৃষ্ঠা ১: পরাবৃত্ত ================= -->
    <div class="page">
        <div class="title-box">[ কেন্দ্রবিহীন কনিক &#8594; পরাবৃত্ত ]</div>

        <h3>i) পরাবৃত্তের শীর্ষবিন্দুর স্থানাঙ্ক নির্ণয় :- \([y^2=4x+8y]\)</h3>
        <ul>
            <li>* বিন্দু দ্বারা সিদ্ধ হবে।</li>
            <li>* দ্বিঘাতের অন্তরীকরণ = 0; প্রাপ্ত মান সমীকরণে বসিয়ে অপর স্থানাঙ্ক নির্ণয় করা যাবে।</li>
            <li>* \(y^2=4ax\) বা \(x^2=4ay\) আকারে সাজানো।</li>
        </ul>

        <h3>ii) উপকেন্দ্রিক লম্বের দৈর্ঘ্য নির্ণয় :-</h3>
        <div class="math-expr">
            দৈর্ঘ্য = <span class="abs-bar">|</span> 
            <div class="fraction">
                <span class="top">একঘাতের সহগ</span>
                <span class="bottom">দ্বিঘাতের সহগ</span>
            </div>
            <span class="abs-bar">|</span>
            &nbsp; ; &nbsp; <span class="highlight-red">সর্বদা ধনাত্মক</span>
        </div>
        <p style="background: #fffbe7; padding: 5px; border-radius: 4px; display: inline-block;">
            [ \(x\) দ্বিঘাত হলে, \(y\) হতে একঘাত। \(y\) দ্বিঘাত হলে \(x\) হতে একঘাত ]
        </p>

        <h3>iii) উপকেন্দ্রিক লম্ব ও নিয়ামকের মধ্যবর্তী দূরত্ব নির্ণয় :-</h3>
        <div class="math-expr">
            দূরত্ব = <span class="abs-bar">|</span> 
            <div class="fraction">
                <span class="top">উপকেন্দ্রিক লম্বের দৈর্ঘ্য</span>
                <span class="bottom">২</span>
            </div>
            <span class="abs-bar">|</span>
            = <span class="abs-bar">|</span>
            <div class="fraction">
                <span class="top">একঘাতের সহগ</span>
                <span class="bottom">২ &times; দ্বিঘাতের সহগ</span>
            </div>
            <span class="abs-bar">|</span>
        </div>

        <h3>iv) দ্বিকাক্ষ বা নিয়ামক রেখা এবং উপকেন্দ্রিক লম্বের সমীকরণ :-</h3>
        <p>\(y^2=4ax\) বা \(x^2=4ay\) সমীকরণের জন্য,</p>
        <ul>
            <li>দ্বিকাক্ষ বা নিয়ামক রেখা &#8658; একঘাত = \(-a\)</li>
            <li>উপকেন্দ্রিক লম্বের সমীকরণ &#8658; একঘাত = \(+a\)</li>
        </ul>

        <h3>v) অক্ষের সমীকরণ নির্ণয় :-</h3>
        <div class="box-note" style="margin: 0 auto;">
            [ দ্বিঘাতের সাপেক্ষে অন্তরীকরণ = 0 ]
        </div>
        <p><strong>Ex:</strong> \(y^2-6x+4y+11=0\) পরাবৃত্তের অক্ষরেখা হবে,</p>
        <p style="margin-left: 30px;">\(2y+4=0 \Rightarrow \boxed{y+2=0}\) Ans.</p>

        <h3>vi) উপকেন্দ্রিক দূরত্ব নির্ণয় :-</h3>
        <div class="math-expr">
            দূরত্ব = <span class="abs-bar">|</span> a + একঘাত <span class="abs-bar">|</span>
        </div>

        <h3>vii) a এর মান নির্ণয় :-</h3>
        <div class="math-expr">
            a = 
            <div class="fraction">
                <span class="top">একঘাতের সহগ</span>
                <span class="bottom">৪ &times; দ্বিঘাতের সহগ</span>
            </div>
        </div>

        <h3>viii) উপকেন্দ্র নির্ণয় :- [শীর্ষ যখন (0,0)]</h3>
        <p>সমীকরণকে আদর্শ আকারে নিতে হবে। যে পাশে একঘাত থাকবে, সে পাশে \(a\) হবে।</p>
        <ul>
            <li>\(y^2=4ax\) এর উপকেন্দ্র \((a,0)\)</li>
            <li>\(x^2=4ay\) এর উপকেন্দ্র \((0,a)\)</li>
        </ul>

        <!-- ফুটার -->
        <div class="footer-spacer"></div>
        <div class="footer-box">
            <strong>GST Zero to 100 Batch</strong><br>
            Session: 2025-26<br>
            Instructor: <strong>Md Sumon Hossen</strong><br>
            Note Made By: <strong>Pranto Kumar Mohanta</strong>
        </div>
    </div>


    <!-- ================= পৃষ্ঠা ২: উপবৃত্ত ও অধিবৃত্ত ================= -->
    <div class="page">
        <div class="title-box">[ উপবৃত্ত এবং অধিবৃত্ত ]</div>

        <h3>i) কেন্দ্রের স্থানাঙ্ক নির্ণয় :-</h3>
        <p>\(x\) এর সাপেক্ষে অন্তরীকরণ = 0 &#8658; \(x\) এর মান <br> \(y\) এর সাপেক্ষে অন্তরীকরণ = 0 &#8658; \(y\) এর মান</p>

        <!-- তুলনা ছক -->
        <table class="comp-table">
            <tr>
                <td class="header-cell">উপবৃত্ত (Ellipse)</td>
                <td class="header-cell">অধিবৃত্ত (Hyperbola)</td>
            </tr>
            <tr>
                <td>
                    <strong>ii) শীর্ষবিন্দু:</strong><br>
                    \(\frac{x^2}{a^2}+\frac{y^2}{b^2}=1\) হলে,<br>
                    \(a>b\) হলে \((\pm a, 0)\)<br>
                    \(b>a\) হলে \((0, \pm b)\)<br><br>

                    <strong>iii) উপকেন্দ্র:</strong><br>
                    \(a>b\) হলে \((\pm \sqrt{a^2-b^2}, 0)\)<br>
                    \(b>a\) হলে \((0, \pm \sqrt{b^2-a^2})\)<br><br>

                    <strong>iv) উৎকেন্দ্রিকতা (e):</strong><br>
                    \(e = \sqrt{\frac{\text{বড়}^2-\text{ছোট}^2}{\text{বড়}^2}}\)<br><br>

                    <strong>v) নাভিলম্বের দৈর্ঘ্য:</strong><br>
                    \(a>b\) হলে \(\frac{2b^2}{a}\) , \(b>a\) হলে \(\frac{2a^2}{b}\)<br><br>

                    <strong>vii) নিয়ামক ও উপকেন্দ্রিক লম্ব:</strong><br>
                    <span style="border-bottom: 1px solid black;">\(a>b\) হলে:</span><br>
                    নিয়ামক: \(x = \pm \frac{a}{e}\)<br>
                    উপ. লম্ব: \(x = \pm ae\)<br><br>
                    
                    <span style="border-bottom: 1px solid black;">\(b>a\) হলে:</span><br>
                    নিয়ামক: \(y = \pm \frac{b}{e}\)<br>
                    উপ. লম্ব: \(y = \pm be\)
                </td>
                
                <!-- অধিবৃত্ত -->
                <td>
                    <strong>ii) শীর্ষবিন্দু:</strong><br>
                    \(\frac{x^2}{a^2}-\frac{y^2}{b^2}=1\) হলে,<br>
                    (-ve) এর আগেরটা বড়।<br>
                    শীর্ষ \((\pm a, 0)\) | \(b>a\) হলে \((0, \pm b)\)<br><br>

                    <strong>iii) উপকেন্দ্র:</strong><br>
                    \(a>b\) হলে \((\pm \sqrt{a^2+b^2}, 0)\)<br>
                    \(b>a\) হলে \((0, \pm \sqrt{a^2+b^2})\)<br><br>

                    <strong>iv) উৎকেন্দ্রিকতা (e):</strong><br>
                    \(e = \sqrt{\frac{\text{বড়}^2+\text{ছোট}^2}{\text{বড়}^2}}\)<br><br>

                    <strong>v) নাভিলম্বের দৈর্ঘ্য:</strong><br>
                    (উপবৃত্তের মতই)<br><br>

                    <strong>vii) নিয়ামক ও উপকেন্দ্রিক লম্ব:</strong><br>
                    <span style="border-bottom: 1px solid black;">\(a>b\) হলে:</span><br>
                    নিয়ামক: \(x = \pm \frac{a}{e}\)<br>
                    উপ. লম্ব: \(x = \pm ae\)<br><br>
                    
                    <span style="border-bottom: 1px solid black;">\(b>a\) হলে:</span><br>
                    নিয়ামক: \(y = \pm \frac{b}{e}\)<br>
                    উপ. লম্ব: \(y = \pm be\)<br>
                    <span class="highlight-red">(পার্থক্য শুধু সূত্রে \(+\) আর \(-\) এ)</span>
                </td>
            </tr>
        </table>

        <br>
        <div style="border: 1px solid var(--blue-border); padding: 10px; border-radius: 5px;">
            <div style="display: flex; justify-content: space-between;">
                <div style="width: 48%;">
                    <strong>viii) উপকেন্দ্রদ্বয়ের মধ্যবর্তী দূরত্ব:</strong><br>
                    \(a>b\) হলে \(2ae\), \(b>a\) হলে \(2be\)
                </div>
                <div style="width: 48%;">
                    <strong>ix) নিয়ামকদ্বয়ের মধ্যবর্তী দূরত্ব:</strong><br>
                    \(a>b\) হলে \(\frac{2a}{e}\), \(b>a\) হলে \(\frac{2b}{e}\)
                </div>
            </div>
        </div>

        <!-- ফুটার -->
        <div class="footer-spacer"></div>
        <div class="footer-box">
            <strong>GST Zero to 100 Batch</strong><br>
            Session: 2025-26<br>
            Instructor: <strong>Md Sumon Hossen</strong><br>
            Note Made By: <strong>Pranto Kumar Mohanta</strong>
        </div>
    </div>

</body>
</html>
