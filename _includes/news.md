<h2 id="news">News</h2>

<style>
  #scrollableDiv {
    min-height: 100px;
    height: 100px;
    overflow-y: hidden;
    opacity: 1;
    transition: height 0.5s ease-in-out, opacity 0.5s ease-in-out;
  }

  #scrollableDiv li {
    font-size: 16px;
    margin-bottom: 8px;
    line-height: 1.4;
  }

  #scrollableDiv a {
    color: #1a73e8;
    text-decoration: none;
  }

  #scrollableDiv a:hover {
    text-decoration: underline;
  }
</style>

<ul id="scrollableDiv" onmouseover="showScrollbar()" onmouseout="hideScrollbar()">
  <li><strong style="color: #c13c33;">[Pinned to top] I am actively seeking a PhD position and a research internship in 2026. I am always happy to discuss potential opportunities!</strong></li>

  <li><b>[2026.05]</b>  At <a href="https://hunyuan.tencent.com/">Tencent Hunyuan</a>, I am driving <b>omni-video understanding</b> — unifying video, audio, and language for reasoning over dynamic scenes, e.g. <a href="https://arxiv.org/pdf/2604.11244">Script-a-Video</a> (deep structured audio-visual captioning). </li>

  <li><b>[2026.05]</b>  <a href="https://01yzzyu.github.io/UFO/">UFO</a> was accepted to ICML 2026 🎉. The <a href="https://huggingface.co/datasets/yzzyu/UFO">dataset</a> and <a href="https://github.com/01yzzyu/UFO">code</a> are now open-sourced. </li>

  <li><b>[2026.02]</b>  EmoRes was accepted to ACL 2026 🎉. </li>
    
  <li><b>[2026.02]</b>  <a href="https://01yzzyu.github.io/svagent.github.io/">SVAgent</a> and MeteoNet were accepted to CVPR 2026 🎉. </li>
  
  <li><b>[2026.01]</b>  <a href="https://01yzzyu.github.io/xr.github.io/">XR</a> was accepted to WWW 2026 🎉. </li>
  
  <li><b>[2025.11]</b>  <a href="https://01yzzyu.github.io/inex.github.io/">InEx</a> was accepted to AAAI 2026 🎉. </li>
  
  <li><b>[2025.10]</b>  <a href="https://01yzzyu.github.io/script.github.io/">Script</a> was accepted to TMLR 2025 🎉. </li>
  
  <li><b>[2025.08]</b>  <a href="https://01yzzyu.github.io/rechar.github.io/">ReChar</a> was accepted to SIGGRAPH Asia 2025 🎉. </li>
  
  <li><b>[2025.08]</b>  <a href="https://01yzzyu.github.io/mermaid.github.io/">MERMAID</a> was accepted to EMNLP 2025 (Main) 🎉. </li>
  
  <li><b>[2025.06]</b> <a href="https://wikiautogen.github.io">WikiAutoGen</a> was accepted to ICCV 2025 🎉. </li>

  <li><b>[2025.03]</b> We present <a href="https://wikiautogen.github.io">WikiAutoGen</a> for automated multimodal Wikipedia-style article generation. Featured in <a href="https://x.com/_akhaliq/status/1904900714519761315?s=46" style="color:#FF0000;">Hugging Face Daily Papers</a> and reposted by <a href="https://x.com/_akhaliq?t=Xbpfc0mTpJQfRsiC_ugQrw&s=09">AK</a>.</li>

  <li><b>[2024.12]</b> Started Remote Research Internship with <a href="https://junchen14.github.io/">Jun Chen</a> and <a href="https://www.mohamed-elhoseiny.com/">Mohamed Elhoseiny</a> (KAUST), focusing on web-scale RAG systems for vision.</li>
  
  <li><b>[2024.11]</b> Released <a href="https://01yzzyu.github.io/rechar.github.io/">ReChar</a>: structure-preserving and user-aesthetic-enhanced character generation.</li>

  <li><b>[2024.05]</b> Our paper <a href="https://doi.org/10.1016/j.frl.2024.105669">Green Effect of Energy Transition Policy</a> was accepted to Finance Research Letters (SSCI Q1 Top journal) 🎉. </li>

  <li><b>[2024.04]</b> National Innovation Project funded: <a href="http://gjcxcy.bjtu.edu.cn/NewLXItemListForStudentDetail.aspx?ItemNo=1186318&IsLXItem=1">FPGA-Based AI Doctor</a>, advised by Prof. Xinhua Wang.</li>

  <li><b>[2024.04]</b> Joined CUHKSZ as Research Assistant with <a href="http://www.zhangruimao.site/">Ruimao Zhang</a>, focusing on AI4Science and CV.</li>

  <li><b>[2024.03]</b> Began Remote Research Internship with <a href="https://yuanjames.github.io/">Yingfang Yuan</a> at Heriot-Watt University on AIGC.</li>

  <li><b>[2024.01]</b> Project <i>UNet-Centric MambaMorph</i> selected as <a href="https://xxb.lzu.edu.cn/xingzhenggongwen/xzgwpdf/2024/0621/271594.html">Outstanding Undergraduate Project</a> (TOP 0.1%) under Barley Plan, advised by Prof. <a href="http://mathteacher.lzu.edu.cn/system/TeacherProfileqt/content.jsp?id=45">Wenting Zhang</a>.</li>

  <li><b>[2023.05]</b> Paper <a href="https://doi.org/10.1016/j.renene.2023.05.044">Environmental Quality in OECD Countries</a> was accepted to Renewable Energy (SCI Q1 Top journal) 🎉. </li>

  <li><b>[2023.03]</b> As sophomore, led innovation project on <a href="http://gjcxcy.bjtu.edu.cn/NewLXItemListForStudentDetail.aspx?ItemNo=1100306">Tropical Linear Representation</a> of Chinese Monoids, advised by Prof. Wenting Zhang. <a href="https://docs.google.com/viewer?url=https://raw.githubusercontent.com/01yzzyu/yzzyu.github.io/master/assets/Tropical_Representation.pdf">[Tech Report] can be finding. </a></li>
</ul>

<script>
  function showScrollbar() {
    var div = document.getElementById('scrollableDiv');
    div.style.height = div.scrollHeight + 'px';
    div.style.opacity = 1;
  }
  function hideScrollbar() {
    var div = document.getElementById('scrollableDiv');
    div.style.height = '100px';
    div.style.opacity = 1;
  }
</script>
