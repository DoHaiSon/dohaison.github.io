---
layout: page
title: Software-Defined Radio (SDR)
description: Real-time physical-layer testbeds, GNU Radio OOT modules, beamforming, and network coding
img: assets/img/GNU_Radio/SDR_Testbed.png
importance: 1
category: Fun
---



<p>Software-Defined Radio (SDR) bridges signal processing theory and real-world hardware implementation. By replacing dedicated hardware components with software modules in C++ and Python, SDR platforms enable flexible, reconfigurable, and rapid prototyping of physical-layer communication protocols.</p>

<p>My work in SDR focuses on custom GNU Radio Out-Of-Tree (OOT) modules, multi-antenna clock/phase synchronization, Direction of Arrival (DoA) estimation using the MUSIC algorithm, OFDM testbeds, and physical-layer network coding on BladeRF and USRP platforms.</p>

<div class="avt2">

  <div class="avt2-head">
    <div class="eyebrow">GNU Radio &amp; SDR Projects</div>
  </div>

  <!-- SOLUTION 01 -->
  <div class="sol">
    <div class="sol-copy">
      <div class="sol-index"><b>01</b> OFDM Testbed</div>
      <h3>gr-ofdm_testbed: GNU Radio OOT Module</h3>
      <span class="en">OFDM Transceiver · C++ OOT Module · BladeRF</span>
      <p>A custom GNU Radio Out-Of-Tree (OOT) module designed for real-time OFDM physical-layer prototyping. Implements frame preamble synchronization, channel estimation, equalization, and payload streaming directly on RF hardware.</p>
      <p>Serves as a flexible base for testing advanced wireless algorithms (such as near-field channel estimators and relay protocols) under over-the-air channel conditions.</p>
      <div class="refs">Repository: <a href="https://github.com/DoHaiSon/gr-ofdm_testbed">gr-ofdm_testbed</a>.</div>
    </div>
    <div class="fig-card">
       <img class="figimg" src="{{ 'assets/img/GNU_Radio/SDR_Testbed.png' | relative_url }}" alt="gr-ofdm_testbed OFDM Transceiver Module">
       <div class="fig-cap">GNU Radio companion flowgraph &amp; OFDM spectrum constellation analyzer.</div>
    </div>
  </div>

  <!-- SOLUTION 02 -->
  <div class="sol flip">
    <div class="sol-copy">
      <div class="sol-index"><b>02</b> Direction Finding</div>
      <h3>gr-DoA_BladeRF: Multi-SDR Synchronization &amp; MUSIC DoA</h3>
      <span class="en">BladeRF Array Sync · MUSIC Algorithm · Direction of Arrival</span>
      <p>A multi-SDR array processing system developed for real-time Direction of Arrival (DoA) estimation using the MUSIC algorithm. Overcomes phase and clock jitter across independent BladeRF units through hardware clock sharing and phase calibration.</p>
      <p>Enables accurate spatial beam tracking, direction finding, and array signal processing on low-cost SDR hardware platforms.</p>
      <div class="refs">Son &amp; Quynh, <a href="{{ 'assets/pdf/2021_REV-ECIT.pdf' | relative_url }}">REV-ECIT (2021)</a>; Repository: <a href="https://github.com/DoHaiSon/gr-DoA_BladeRF">gr-DoA_BladeRF</a>.</div>
    </div>
    <div class="fig-card">
      <img class="figimg" src="{{ 'assets/img/GNU_Radio/GNU_Radio_Cover.png' | relative_url }}" alt="gr-DoA_BladeRF Beamforming & DoA">
      <div class="fig-cap">Multi-antenna clock synchronization &amp; MUSIC DoA polar beam estimation.</div>
    </div>
  </div>

  <!-- SOLUTION 03 -->
  <div class="sol">
    <div class="sol-copy">
      <div class="sol-index"><b>03</b> Network Coding</div>
      <h3>SDR_NC: Network Coding &amp; Cognitive Wireless Networks</h3>
      <span class="en">Physical-Layer Network Coding · Multi-Robot · Multimedia</span>
      <p>Real-time physical-layer network coding testbed designed for cognitive wireless networking and multi-robot communication systems. Implements agile multimedia packet transmission and cooperative relaying.</p>
      <p>Demonstrates significant throughput gains and energy efficiency in spectrum-constrained multi-hop wireless networks.</p>
      <div class="refs">Son et al., <a href="{{ 'assets/pdf/2019_REV-ECIT.pdf' | relative_url }}">REV-ECIT (2019)</a>, <a href="{{ 'assets/pdf/2023_REV-ECIT.pdf' | relative_url }}">REV-ECIT (2023)</a>; Repository: <a href="https://github.com/DoHaiSon/SDR_NC">SDR_NC</a>.</div>
    </div>
    <div class="fig-card">
      <img class="figimg" src="{{ 'assets/img/GNU_Radio/SDR_NC.png' | relative_url }}" alt="SDR Network Coding & Multi-Robot Communication">
      <div class="fig-cap">Physical-layer network coding &amp; multi-robot cognitive relaying on SDR.</div>
    </div>
  </div>

  <div class="avt2-head">
    <div class="eyebrow">Publications</div>
  </div>

  <div class="pub-section">
    <ol class="pub-list">
      <li>
        <strong>Do Hai Son</strong>, Tran Thi Thuy Quynh, Ngo K. Hoang, Nguyen Van Ly, and Nguyen Linh Trung. <em>Thiết lập nền tảng SDR cho hệ thống OFDM</em>. Chương 9 trong sách <strong>Truyền thông chuyển tiếp hai chiều: Lý thuyết và Thực nghiệm</strong>, Nhà xuất bản Đại học Quốc gia Hà Nội, tr. 151-235, Tháng 6/2025.
      </li>
      <li>
        <strong>Do Hai Son</strong>, Nguyen Huu Hung, Pham Duy Hung, and Tran Thi Thuy Quynh. <em><a class="general" href="{{ 'assets/pdf/2023_REV-ECIT.pdf' | relative_url }}">Ước lượng kênh truyền trong hệ thống đa robot sử dụng SDR</a></em>. <strong>In Hội nghị Quốc gia lần thứ XXVI về Điện tử, Truyền thông và Công nghệ Thông tin (REV-ECIT)</strong>, Hanoi, Vietnam, December 2023.
      </li>
      <li>
        <strong>Do Hai Son</strong> and Tran Thi Thuy Quynh. <em><a class="general" href="{{ 'assets/pdf/2021_REV-ECIT.pdf' | relative_url }}">Đồng bộ nhiều SDR trong thực thi thuật toán ước lượng hướng sóng đến MUSIC</a></em>. <strong>In Hội nghị Quốc gia lần thứ XXIV về Điện tử, Truyền thông và Công nghệ Thông tin (REV-ECIT)</strong>, Hanoi, Vietnam, December 2021.
      </li>
      <li>
        <strong>Do Hai Son</strong>, Tran Duc Manh, and Tran Thi Thuy Quynh. <em><a class="general" href="{{ 'assets/pdf/2019_REV-ECIT.pdf' | relative_url }}">Định vị Robot di động trong nhà dựa trên tín hiệu WiFi</a></em>. <strong>In Hội nghị Quốc gia lần thứ XXII về Điện tử, Truyền thông và Công nghệ Thông tin (REV-ECIT)</strong>, Hanoi, Vietnam, December 2019.
      </li>
      <li>
        <strong>Do Hai Son</strong>. <em><a class="general" href="{{ 'assets/pdf/2020_Thesis.pdf' | relative_url }}">Xây dựng hệ thống xác định hướng sóng đến sử dụng thuật toán MUSIC trên thiết bị SDR</a></em>. <strong>Khóa luận Cử nhân</strong>, Trường Đại học Công nghệ, Đại học Quốc gia Hà Nội, Tháng 7/2020.
      </li>
    </ol>
  </div>

  <div class="avt2-head">
    <div class="eyebrow">Repositories</div>
  </div>
  <div class="pub-section">
    <ol class="pub-list">
      <li>
        <strong>gr-ofdm_testbed</strong>: <a class="general" href="https://github.com/DoHaiSon/gr-ofdm_testbed">https://github.com/DoHaiSon/gr-ofdm_testbed</a> — OFDM Transceiver Testbed OOT Module for GNU Radio.
      </li>
      <li>
        <strong>gr-DoA_BladeRF</strong>: <a class="general" href="https://github.com/DoHaiSon/gr-DoA_BladeRF">https://github.com/DoHaiSon/gr-DoA_BladeRF</a> — Multi-SDR Synchronization and MUSIC Direction of Arrival module.
      </li>
      <li>
        <strong>SDR_NC</strong>: <a class="general" href="https://github.com/DoHaiSon/SDR_NC">https://github.com/DoHaiSon/SDR_NC</a> — Network Coding with Multimedia Transmission for Cognitive Networking on SDR.
      </li>
    </ol>
  </div>

</div>