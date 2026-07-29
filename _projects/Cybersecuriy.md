---
layout: page
title: Cybersecurity
description: Cyber-security for Industry 4.0 and smart cities
img: assets/img/Cyber/Security_thumb_1x1.png
importance: 2
category: Work
---



<p>A main driver for smart city development is Industry 4.0, in which ICT helps connect physical systems to the cyber-world, thereby enabling supply chain market more efficient, agile, and customer-focused. However, cyber-security risks become a key concern due to open systems with IP addresses, creating more avenues for cyber-attacks.</p>

<p>Information and communication technology (ICT) is expected to play an increasingly pivotal role in deepening economic integration and community building across the Association of Southeast Asian Nations (ASEAN), transitioning towards a digitally-enabled economy that is <em>secure</em>, sustainable, and transformative. This project considers the development of connected smart cities for a smart ASEAN society in general and in Vietnam in particular.</p>

<p>The project aims to provide tools to enhance cyber-security in Industry 4.0, contributing to the enhancement of information reliability for smart society.</p>

<div class="avt2">

  <div class="avt2-head">
    <div class="eyebrow">Our approaches</div>
  </div>

  <!-- SOLUTION 01 -->
  <div class="sol">
    <div class="sol-copy">
      <div class="sol-index"><b>01</b> Foundation</div>
      <h3>Collaborative learning for attack detection</h3>
      <span class="en">Collaborative / Federated learning</span>
      <p>Each node in the network, such as a blockchain full node or an IoT gateway, collects data and trains a model locally. Instead of sending raw data to a server, the nodes exchange only the learned knowledge (model weights). A central server aggregates them into a global model and sends it back to every node.</p>
      <p>This way, the system leverages knowledge from the whole network without exposing private data or congesting the network with large transfers. On the task of detecting and classifying network-layer attacks, the model reaches up to 97.7% accuracy.</p>
      <div class="refs">Tran V. Khoa, Do H. Son et al., <a href="https://doi.org/10.1109/TSMC.2024.3374280">IEEE TSMC (2024)</a>; <a href="https://doi.org/10.1109/WCNC57260.2024.10571103">WCNC (2024)</a>.</div>
    </div>
    <div class="fig-card">
       <img class="figimg" src="{{ 'assets/img/Cyber/Security_2.png' | relative_url }}" alt="Distributed collaborative learning">
       <div class="fig-cap">Distributed collaborative learning, raw data stays on each node.</div>
    </div>
  </div>

  <!-- SOLUTION 02 -->
  <div class="sol flip">
    <div class="sol-copy">
      <div class="sol-index"><b>02</b> Blockchain</div>
      <h3>Detecting attacks in transactions &amp; smart contracts</h3>
      <span class="en">Attacks in transactions &amp; smart contracts</span>
      <p>Blockchain is increasingly popular, yet its transactions and smart contracts themselves become attack targets. The threats span two layers: the network layer (meaningless transaction spam, brute-force passwords) and the transaction/smart-contract layer (exploiting vulnerabilities to steal assets or break the system's integrity).</p>
      <p>Our group developed a detector based on collaborative learning, deployed directly on the mining nodes for real-time monitoring and identifying attacks on both layers, reaching up to 94% accuracy.</p>
      <div class="refs">Tran V. Khoa, Do H. Son et al., <a href="https://doi.org/10.1109/TCCN.2025.36372742">IEEE TCCN (2025)</a>.</div>
    </div>
    <div class="fig-card">
      <img class="figimg" src="{{ 'assets/img/Cyber/Security_1.png' | relative_url }}" alt="Attack detection on blockchain">
      <div class="fig-cap">Real-time attack detection on blockchain.</div>
    </div>
  </div>

  <!-- SOLUTION 03 -->
  <div class="sol">
    <div class="sol-copy">
      <div class="sol-index"><b>03</b> Computer vision</div>
      <h3>Vision-based cyberattack detection</h3>
      <span class="en">Vision-based learning · Vision Transformer</span>
      <p>A preprocessing tool based on natural language processing (NLP) converts transaction features, such as transaction value, gas used, and input length, into an image representation. This image is fed to a Vision Transformer (ViT), which is very strong at capturing complex patterns and semantic relationships.</p>
      <p>Combining NLP with vision-based learning helps detect many types of attacks, reaching 99.5% accuracy while using only about 8% of the parameters of ResNet, i.e., light enough to deploy on resource-constrained nodes.</p>
      <div class="refs">Do H. Son, Le V. Hieu et al., <a href="https://doi.org/10.1109/ISCIT67082.2025.11231741">ISCIT (2025)</a>.</div>
    </div>
    <div class="fig-card">
      <img class="figimg" src="{{ 'assets/img/Cyber/Security_5.png' | relative_url }}" alt="Vision Transformer classification">
      <div class="fig-cap">Transaction, image, Vision Transformer, classification.</div>
    </div>
  </div>

  <!-- SOLUTION 04 -->
  <div class="sol flip">
    <div class="sol-copy">
      <div class="sol-index"><b>04</b> Supply chains</div>
      <h3>Semi-supervised anomaly detection with limited labeled data</h3>
      <span class="en">Semi-supervised anomaly detection</span>
      <p>In blockchain-based supply chains, anomalous data is usually rare and expensive to label. Semi-supervised learning exploits a small amount of labeled samples together with a large pool of unlabeled data to build a decision boundary, thereby flagging out-of-distribution behavior as anomalous.</p>
      <div class="refs">Do H. Son, Bui D. Manh et al., <a href="https://doi.org/10.1109/ISCIT63075.2024.10793673">ISCIT (2024)</a>.</div>
    </div>
    <div class="fig-card">
      <img class="figimg" src="{{ 'assets/img/Cyber/Security_6.png' | relative_url }}" alt="Semi-supervised learning for supply chains">
      <div class="fig-cap">Semi-supervised learning for supply chains.</div>
    </div>
  </div>

  <!-- SOLUTION 05 -->
  <div class="sol">
    <div class="sol-copy">
      <div class="sol-index"><b>05</b> Industry 4.0</div>
      <h3>Cyber risk assessment for Industry 4.0</h3>
      <span class="en">Cyber risk assessment framework</span>
      <p>We builds a cyber-risk assessment framework for Industry 4.0 that helps identify and rank threats across connected systems, together with recommendations tailored to the Vietnamese context.</p>
      <div class="refs">Bui M. Tuan, Tran V. Khoa, Do H. Son et al., <a href="http://dx.doi.org/10.21553/rev-jec.323">REV-JEC (2023)</a>.</div>
    </div>
    <div class="fig-card">
      <img class="figimg" src="{{ 'assets/img/Cyber/Security_7.png' | relative_url }}" alt="Risk assessment for Industry 4.0">
      <div class="fig-cap">Risk assessment for Industry 4.0.</div>
    </div>
  </div>

  <div class="avt2-head">
    <div class="eyebrow">Applications</div>
    <h2>Deployed on real blockchain infrastructure</h2>
    <p class="avt2-intro">The solutions above have been deployed on real systems in our laboratory: a provenance-tracing system built on Ethereum infrastructure, a smart grid, and Industry 4.0 IoT networks.</p>
  </div>

  <figure class="fig-card apps-banner">
    <div class="wide">
        <img class="figimg" src="{{ 'assets/img/Cyber/Security_3.png' | relative_url }}" alt="Blockchain platform for smart-city applications">
    </div>
    <div class="fig-cap">A blockchain platform behind many smart-city applications.</div>
  </figure>

  <div class="avt2-head">
    <div class="eyebrow">Publications</div>
  </div>

  <div class="pub-section">
    <h3>Journals</h3>
    <ol class="pub-list">
      <li>
        Tran Viet Khoa, <strong>Do Hai Son</strong>, Chi-Hieu Nguyen, Dinh Thai Hoang, Diep N. Nguyen, Tran Thi Thuy Quynh, Trong-Minh Hoang, Nguyen Viet Ha, Eryk Dutkiewicz, Mohammad Abu Alsheikh, and Nguyen Linh Trung. <em><a class="general" href="https://doi.org/10.1109/TCCN.2025.36372742">Collaborative learning framework to detect attacks in transactions and smart contracts</a></em>. <strong>IEEE Transactions on Cognitive Communications and Networking</strong>, 12:4290 – 4306, November 2025.
      </li>
      <li>
        Tran Viet Khoa, <strong>Do Hai Son</strong>, Dinh Thai Hoang, Nguyen Linh Trung, Tran Thi Thuy Quynh, Nguyen Viet Ha, Diep N Nguyen, and Eryk Dutkiewicz. <em><a class="general" href="https://doi.org/10.1109/TSMC.2024.3374280">Collaborative learning for cyberattack detection in blockchain networks</a></em>. <strong>IEEE Transactions on Systems, Man, Cybernetics: Systems</strong>, vol. 54, no 7, pages 3920-3933, July 2024.
      </li>
      <li>
        Bui Minh Tuan, Tran Viet Khoa, <strong>Do Hai Son</strong>, Nguyen Linh Trung, Tran Thi Thuy Quynh, Nguyen Viet Ha, Nguyen Ngoc Hoa, Nguyen Dai Tho, and Le Quang Minh. <em><a class="general" href="http://dx.doi.org/10.21553/rev-jec.323">A new framework for cyber risk assessment for Industry 4.0 and recommendations for Vietnam</a></em>. <strong>REV Journal on Electronics and Communications</strong>, 13(3–4):28–44, July–December 2023.
      </li>
    </ol>

    <h3>Conferences</h3>
    <ol class="pub-list">
      <li>
        <strong>Do Hai Son</strong>, Le Vu Hieu, Tran Viet Khoa, Yibeltal F. Alem, Hoang Trong Minh, Tran Thi Thuy Quynh, Nguyen Viet Ha, and Nguyen Linh Trung. <em><a class="general" href="https://doi.org/10.1109/ISCIT67082.2025.11231741">Vision-based learning for cyberattack detection in blockchain smart contracts and transactions</a></em>. <strong>In 24th International Symposium on Communications and Information Technologies (ISCIT)</strong>, Hanoi, Vietnam, 16-18 October 2025.
      </li>
      <li>
        <strong>Do Hai Son</strong>, Bui Duc Manh, Tran Viet Khoa, Nguyen Linh Trung, Dinh Thai Hoang, Hoang Trong Minh, Yibeltal Alem, and Le Quang Minh. <em><a class="general" href="https://doi.org/10.1109/ISCIT63075.2024.10793673">Semi-supervised learning for anomaly detection in blockchain-based supply chains</a></em>. <strong>In 2024 23rd International Symposium on Communications and Information Technologies (ISCIT)</strong>, pages 140–145, 2024.
      </li>
      <li>
        Tran Viet Khoa, <strong>Do Hai Son</strong>, Dinh Thai Hoang, Nguyen Linh Trung, Tran Thi Thuy Quynh, Nguyen Viet Ha, Diep N Nguyen, and Eryk Dutkiewicz. <em><a class="general" href="https://doi.org/10.1109/WCNC57260.2024.10571103">Real-time cyberattack detection with collaborative learning for blockchain networks</a></em>. <strong>In IEEE Wireless Communications and Networking Conference (WCNC)</strong>, Dubai, United Arab Emirates, April 2024.
      </li>
      <li>
        <strong>Do Hai Son</strong>, Tran Thi Thuy Quynh, Tran Viet Khoa, Dinh Thai Hoang, Nguyen Linh Trung, Nguyen Viet Ha, Dusit Niyato, Diep N. Nguyen, and Eryk Dutkiewicz. <em><a class="general" href="https://doi.org/10.1109/ATC52653.2021.9598199">An effective framework of private Ethereum blockchain network for smart grid</a></em>. <strong>International Conference on Advanced Technologies for Communications (ATC)</strong>, Ho Chi Minh city, Vietnam, 2021. <b style="color: var(--brand);">[Best paper award]</b>
      </li>
    </ol>
  </div>

</div>