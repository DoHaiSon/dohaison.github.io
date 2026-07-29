---
layout: page
title: Wireless Communications
description: Advanced research, algorithms, and 5G/6G wireless communications
img: assets/img/Wireless/NearField_6G.png
importance: 3
category: Work
---



<p>Wireless communication systems are undergoing a paradigm shift towards 5G-Advanced and 6G networks, driven by Extremely Large-Scale Antenna Arrays (ELAA), near-field propagation, high-frequency spectrums, and artificial intelligence. My research focuses on developing innovative channel estimation algorithms, informed system identification frameworks, and deep learning models for next-generation physical layers.</p>

<p>Our solutions span theoretical performance limits (Cramér-Rao Bounds), robust channel identification (InSI framework, semi-blind equalizers), and deep learning-based channel estimators (RACNN, ISDNN).</p>

<div class="avt2">

  <div class="avt2-head">
    <div class="eyebrow">Our Research Approaches</div>
  </div>

  <!-- SOLUTION 01 -->
  <div class="sol">
    <div class="sol-copy">
      <div class="sol-index"><b>01</b> System Identification</div>
      <h3>Informed System Identification (InSI) Toolbox</h3>
      <span class="en">Semi-blind Equalization · Induced Properties · Prior Knowledge</span>
      <p>Conventional blind channel estimation suffers from high sample requirements and phase ambiguities. InSI is our developed MATLAB framework that incorporates high-level prior information, induced signal properties, and semi-blind processing to overcome these limitations.</p>
      <p>InSI evaluates Cramér-Rao Bounds (CRB) across FIR, specular, and structured channel models, providing optimal estimation accuracy for complex MIMO-OFDM communication systems.</p>
      <div class="refs">Son, <a href="{{ 'assets/pdf/2023_Thesis.pdf' | relative_url }}">MSc Thesis (2023)</a>; Son et al., <a href="https://doi.org/10.1109/APSIPAASC58517.2023.10317233">APSIPA ASC (2023)</a>; Repository: <a href="https://github.com/DoHaiSon/InSI">InSI</a>.</div>
    </div>
    <div class="fig-card">
       <img class="figimg" src="{{ 'assets/img/Wireless/InSI_Solution.png' | relative_url }}" alt="Informed System Identification Framework">
       <div class="fig-cap">Informed System Identification framework &amp; Cramér-Rao bound analysis.</div>
    </div>
  </div>

  <!-- SOLUTION 02 -->
  <div class="sol flip">
    <div class="sol-copy">
      <div class="sol-index"><b>02</b> 6G Near-Field</div>
      <h3>Near-Field Communication &amp; Ray-Tracing Channel Models</h3>
      <span class="en">Extremely Large Antenna Arrays (ELAA) · RACNN Deep Learning</span>
      <p>In 6G networks, Extremely Large-Scale Antenna Arrays (ELAA) expand the near-field region where spherical wavefronts dominate. We develop ray-tracing propagation models and deep learning architectures to tackle near-field channel estimation.</p>
      <p>Our proposed Residual Attention Convolutional Neural Network (RACNN) captures spatial spherical correlations, achieving superior channel estimation accuracy with significantly reduced training complexity.</p>
      <div class="refs">Khang, Son et al., <a href="https://doi.org/10.25073/2588-1086/vnucsce.7077">VNU JCSCE (2026)</a>; Lam, Son et al., <a href="https://link.springer.com/chapter/10.1007/978-3-032-00972-2_29">CITA (2025)</a>; Repository: <a href="https://github.com/DoHaiSon/RACNN">RACNN</a>.</div>
    </div>
    <div class="fig-card">
      <img class="figimg" src="{{ 'assets/img/Wireless/NearField_6G.png' | relative_url }}" alt="6G Near-Field Ray Tracing & RACNN">
      <div class="fig-cap">Spherical wavefront ray-tracing &amp; RACNN deep learning for 6G near-field.</div>
    </div>
  </div>

  <!-- SOLUTION 03 -->
  <div class="sol">
    <div class="sol-copy">
      <div class="sol-index"><b>03</b> Massive MIMO</div>
      <h3>Deep Neural Networks &amp; 3D Antenna Array Geometry</h3>
      <span class="en">ISDNN Deep Learning · Array Geometry (ULA, UCyA) Analysis</span>
      <p>Massive MIMO systems require accurate estimation of high-dimensional channel matrices under varying SNR levels. We design ISDNN, a customized deep neural network architecture for fast and robust Massive MIMO channel estimation.</p>
      <p>Additionally, we perform comprehensive Cramér-Rao Bound (CRB) impact analyses on 3D antenna array geometries (Uniform Linear, Uniform Cylindrical Arrays), establishing physical array design guidelines.</p>
      <div class="refs">Son, Lam et al., <a href="https://doi.org/10.57001/huih5804.2024.366">HaUI JST (2024)</a>; Son et al., <a href="https://doi.org/10.1109/SSP53291.2023.10208041">IEEE SSP (2023)</a>.</div>
    </div>
    <div class="fig-card">
      <img class="figimg" src="{{ 'assets/img/Wireless/Massive_MIMO.png' | relative_url }}" alt="Massive MIMO DNN & Antenna Geometry">
      <div class="fig-cap">ISDNN neural network architecture &amp; 3D antenna array geometry performance.</div>
    </div>
  </div>

  <div class="avt2-head">
    <div class="eyebrow">Publications</div>
  </div>

  <div class="pub-section">
    <h3>Journals</h3>
    <ol class="pub-list">
      <li>
        Nguyen The Khang, <strong>Do Hai Son</strong>, Tran Trong Duy, Le Thanh Trung, Tran Thi Thuy Quynh, Karim Abed-Meraim, Merouane Debbah, and Nguyen Linh Trung. <em><a class="general" href="https://doi.org/10.25073/2588-1086/vnucsce.7077">Ray-Tracing Channel Models for Near-Field Communication</a></em>. <strong>VNU Journal of Science: Computer Science and Communication Engineering</strong>, 42(3):1-24, June 2026.
      </li>
      <li>
        <strong>Do Hai Son</strong>, Vu Tung Lam, and Tran Thi Thuy Quynh. <em><a class="general" href="https://doi.org/10.57001/huih5804.2024.366">ISDNN: A Deep Neural Network for Channel Estimation in Massive MIMO systems</a></em>. <strong>Hanoi University of Industry Journal of Science and Technology</strong>, 60(11):48-54, November 2024.
      </li>
    </ol>

    <h3>Conferences &amp; Workshops</h3>
    <ol class="pub-list">
      <li>
        Vu Tung Lam, <strong>Do Hai Son</strong>, Tran Thi Thuy Quynh, and Le Trung Thanh. <em><a class="general" href="https://link.springer.com/chapter/10.1007/978-3-032-00972-2_29">RACNN: Residual Attention Convolutional Neural Network for Near-Field Channel Estimation in 6G Wireless Communications</a></em>. <strong>In Conference on Information Technology and its Applications (CITA)</strong>, Phnom Penh, Cambodia, July 2025.
      </li>
      <li>
        Hai Pham Anh, Tran Trong Duy, <strong>Do Hai Son</strong>, Karim Abed-Meraim, and Nguyen Linh Trung. <em><a class="general" href="https://ieeexplore.ieee.org/document/11249365">FlowEKF: Flow-based Extended Kalman filter</a></em>. <strong>In Asia Pacific Signal and Information Processing Association Annual Summit and Conference (APSIPA ASC)</strong>, Singapore, October 2025.
      </li>
      <li>
        <strong>Do Hai Son</strong>, Karim Abed-Meraim, Tran Trong Duy, Nguyen Linh Trung, and Tran Thi Thuy Quynh. <em><a class="general" href="https://doi.org/10.1109/APSIPAASC58517.2023.10317233">On the Semi-Blind Mutually Referenced Equalizers for MIMO Systems</a></em>. <strong>In Asia Pacific Signal and Information Processing Association Annual Summit and Conference (APSIPA ASC)</strong>, Taipei, Taiwan, November 2023.
      </li>
      <li>
        <strong>Do Hai Son</strong> and Tran Thi Thuy Quynh. <em><a class="general" href="https://doi.org/10.1109/SSP53291.2023.10208041">Impact Analysis of Antenna Array Geometry on Performance of Semi-blind Structured Channel Estimation for massive MIMO-OFDM systems</a></em>. <strong>In IEEE Statistical Signal Processing Workshop (SSP)</strong>, Hanoi, Vietnam, July 2023.
      </li>
    </ol>

    <h3>Books &amp; Theses</h3>
    <ol class="pub-list">
      <li>
        <strong>Do Hai Son</strong>. <em><a class="general" href="{{ 'assets/pdf/2023_Thesis.pdf' | relative_url }}">Nghiên cứu nhận dạng hệ thống với tri thức mới cho hệ thống truyền thông MIMO kích thước lớn</a></em>. <strong>Luận văn Thạc sĩ</strong>, Trường Đại học Công nghệ, Đại học Quốc gia Hà Nội, Tháng 6/2023.
      </li>
    </ol>
  </div>

</div>