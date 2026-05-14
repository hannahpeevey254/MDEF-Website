## ★  Cognitive Orgies II
</div>
<h2 style="margin-top:0; text-align:center;"> MOCHI.</h2>


</div>
<p style="font-size:14px; line-height:1.5; text-align:center; max-width:700px; margin: 0 auto 40px auto;">
  Mochi is a self-contained cyberdeck companion — no cloud, no app store, no extraction. 
  
  You feed it data through physical buttons: sleep, water, food. 
  
  It responds with its body. Tend to it and it grows. Neglect it and it shrinks. Abandon it and it dies. It is not a wellness tracker. It is not a fitness app. It is a mirror with a body
  
   a physical object that makes the invisible exchange between you and your data visible, chosen, and consequential.

</p>
 </div>

<div style="display:flex; align-items:flex-start; justify-content:space-between; gap:20px; margin-top:30px;">

  <!-- LEFT SIDE TEXT -->
  <div style="width:55%; font-size:12px; line-height:1.5;">

 <h4 style="margin-bottom:10px;">Process</h4>

 <p>
      Built entirely through iterative vibe coding — no prior hardware experience, no existing template, no blueprint to follow. Starting from a concept and a components list, I programmed the full firmware from scratch: the sensor logic, the button inputs, the mood states, the shrink and grow animations, and the death mechanic. Every behaviour Mochi has was written, tested, broken, and rewritten. The stack was assembled deliberately.
  </p>

  <p>
       ESP32 as the brain — cheap, powerful, offline by design. Physical buttons as the only interface — no touchscreen, no scroll, no infinite feed. Just three inputs: sleep, water, food. The companion Expo app exists as an optional mirror, not a requirement. Mochi works without your phone. That was a non-negotiable design decision. The entire codebase is open source on GitHub — the schematic, the firmware, the death logic, all of it. Making it open wasn't an afterthought. It is part of the argument.
    </p>

 <h4 style="margin-top:20px; margin-bottom:10px;">Outcome</h4>

 <p>
      Mochi is the first act of a trilogy about what happens to your data self. Here, you choose to tend it. In Data Body, it gets extracted and traded. In Safe Hands, it outlives you. Together they trace the full arc of personal data — from body, to commodity, to ghost. 
    </p>

 <p>
      Mochi asks the earliest question: what if the act of logging yourself was a practice of care, not a product to be sold?
    </p>

  </div>

  <!-- RIGHT SIDE IMAGE -->
  <div style="width:30%;">
  <img src="../images/mochi 1.jpeg" style="width:80%; height:auto; border-radius:6px;">
</div>

</div>

----
<!-- MOCHI PET — SELF-CONTAINED SYSTEM DIAGRAM -->
<div style="width:100%;margin:40px 0;font-family:'Courier New',monospace;">

  <!-- Title -->
  <div style="text-align:center;margin-bottom:32px;">
    <div style="font-size:9px;letter-spacing:.3em;text-transform:uppercase;color:#888;margin-bottom:6px;">System Architecture · Signal Flow</div>
    <div style="width:40px;height:1px;background:#e05a2b;margin:0 auto;"></div>
  </div>

  <!-- CONTAINER -->
  <div style="max-width:560px;margin:0 auto;position:relative;padding:0 20px;">

  <!-- Vertical spine -->
  <div style="position:absolute;left:50%;top:0;bottom:0;width:1px;background:linear-gradient(to bottom,transparent,#333 60px,#333 calc(100% - 60px),transparent);transform:translateX(-50%);z-index:0;"></div>

  <!-- ── 01 HARDWARE ── -->
  <div style="display:flex;align-items:center;gap:0;margin-bottom:8px;position:relative;z-index:1;">
    <div style="flex:1;height:1px;background:#444;"></div>
    <div style="padding:3px 12px;border:1px solid #444;font-size:8px;letter-spacing:.25em;text-transform:uppercase;color:#888;white-space:nowrap;background:#fff;">
      01 · Hardware
    </div>
    <div style="flex:1;height:1px;background:#444;"></div>
  </div>

  <!-- ESP32-S3 node -->
  <div style="display:flex;justify-content:center;margin:16px 0;position:relative;z-index:1;">
    <div style="width:90px;height:90px;border-radius:50%;border:2px solid #1a1a1a;background:#1a1a1a;display:flex;flex-direction:column;align-items:center;justify-content:center;text-align:center;">
      <span style="font-size:9px;font-weight:700;color:#fff;line-height:1.3;">ESP32-S3<br>WROOM-1</span>
      <span style="font-size:7px;color:#888;margin-top:3px;letter-spacing:.1em;">MICROCONTROLLER</span>
    </div>
  </div>

  <!-- Hardware branches -->
  <div style="display:flex;justify-content:space-between;margin:0 0 24px 0;position:relative;z-index:1;">
    <!-- Left -->
    <div style="width:45%;display:flex;flex-direction:column;gap:6px;align-items:flex-end;">
      <div style="display:flex;align-items:center;gap:6px;">
        <span style="font-size:8px;color:#555;text-align:right;">Feed btn GPIO 15</span>
        <div style="width:20px;height:1px;background:#555;"></div>
        <div style="width:5px;height:5px;border-radius:50%;background:#555;"></div>
      </div>
      <div style="display:flex;align-items:center;gap:6px;">
        <span style="font-size:8px;color:#555;text-align:right;">Water btn GPIO 17</span>
        <div style="width:20px;height:1px;background:#555;"></div>
        <div style="width:5px;height:5px;border-radius:50%;background:#555;"></div>
      </div>
      <div style="display:flex;align-items:center;gap:6px;">
        <span style="font-size:8px;color:#555;text-align:right;">Sleep btn GPIO 16</span>
        <div style="width:20px;height:1px;background:#555;"></div>
        <div style="width:5px;height:5px;border-radius:50%;background:#555;"></div>
      </div>
    </div>
    <!-- Right -->
    <div style="width:45%;display:flex;flex-direction:column;gap:6px;align-items:flex-start;">
      <div style="display:flex;align-items:center;gap:6px;">
        <div style="width:5px;height:5px;border-radius:50%;background:#555;"></div>
        <div style="width:20px;height:1px;background:#555;"></div>
        <span style="font-size:8px;color:#555;">Grove OLED 128×128</span>
      </div>
      <div style="display:flex;align-items:center;gap:6px;">
        <div style="width:5px;height:5px;border-radius:50%;background:#555;"></div>
        <div style="width:20px;height:1px;background:#555;"></div>
        <span style="font-size:8px;color:#555;">I²C 0x3C · SH1107</span>
      </div>
      <div style="display:flex;align-items:center;gap:6px;">
        <div style="width:5px;height:5px;border-radius:50%;background:#555;"></div>
        <div style="width:20px;height:1px;background:#555;"></div>
        <span style="font-size:8px;color:#555;">NVS (Preferences)</span>
      </div>
    </div>
  </div>

  <!-- ── 02 FIRMWARE ── -->
  <div style="display:flex;align-items:center;gap:0;margin-bottom:8px;position:relative;z-index:1;">
    <div style="flex:1;height:1px;background:#444;"></div>
    <div style="padding:3px 12px;border:1px solid #444;font-size:8px;letter-spacing:.25em;text-transform:uppercase;color:#888;white-space:nowrap;background:#fff;">
      02 · Firmware
    </div>
    <div style="flex:1;height:1px;background:#444;"></div>
  </div>

  <!-- Flow tag -->
  <div style="text-align:center;margin:12px 0 8px;position:relative;z-index:1;">
    <span style="font-size:7.5px;letter-spacing:.2em;color:#aaa;">/ boot /</span>
  </div>

  <!-- Loading screen node -->
  <div style="display:flex;justify-content:center;margin:0 0 4px;position:relative;z-index:1;">
    <div style="width:80px;height:80px;border-radius:50%;border:1.5px solid #1a1a1a;background:#fff;display:flex;flex-direction:column;align-items:center;justify-content:center;text-align:center;">
      <span style="font-size:9px;font-weight:700;color:#1a1a1a;line-height:1.3;">Loading<br>Screen</span>
      <span style="font-size:7px;color:#888;margin-top:2px;letter-spacing:.1em;">HEART RINGS</span>
    </div>
  </div>

  <!-- Loading screen branches -->
  <div style="display:flex;justify-content:space-between;margin:6px 0 12px;position:relative;z-index:1;">
    <div style="width:45%;display:flex;align-items:center;justify-content:flex-end;gap:6px;">
      <span style="font-size:8px;color:#555;">Concentric hearts</span>
      <div style="width:20px;height:1px;background:#555;"></div>
      <div style="width:5px;height:5px;border-radius:50%;background:#555;"></div>
    </div>
    <div style="width:45%;display:flex;align-items:center;gap:6px;">
      <div style="width:5px;height:5px;border-radius:50%;background:#555;"></div>
      <div style="width:20px;height:1px;background:#555;"></div>
      <span style="font-size:8px;color:#555;">"hi im mochi"</span>
    </div>
  </div>

  <!-- Flow tag -->
  <div style="text-align:center;margin:4px 0 8px;position:relative;z-index:1;">
    <span style="font-size:7.5px;letter-spacing:.2em;color:#aaa;">/ main loop ~60fps /</span>
  </div>

  <!-- Stat engine node -->
  <div style="display:flex;justify-content:center;margin:0 0 4px;position:relative;z-index:1;">
    <div style="width:90px;height:90px;border-radius:50%;border:1.5px solid #1a1a1a;background:#fff;display:flex;flex-direction:column;align-items:center;justify-content:center;text-align:center;">
      <span style="font-size:9px;font-weight:700;color:#1a1a1a;line-height:1.3;">Stat<br>Engine</span>
      <span style="font-size:7px;color:#888;margin-top:2px;letter-spacing:.1em;">LOOP ~60FPS</span>
    </div>
  </div>

  <!-- Stat engine branches -->
  <div style="display:flex;justify-content:space-between;margin:6px 0 16px;position:relative;z-index:1;">
    <div style="width:45%;display:flex;flex-direction:column;gap:6px;align-items:flex-end;">
      <div style="display:flex;align-items:center;gap:6px;">
        <span style="font-size:8px;color:#555;">Decay (10s interval)</span>
        <div style="width:20px;height:1px;background:#555;"></div>
        <div style="width:5px;height:5px;border-radius:50%;background:#555;"></div>
      </div>
      <div style="display:flex;align-items:center;gap:6px;">
        <span style="font-size:8px;color:#555;">Food / Water / Sleep</span>
        <div style="width:20px;height:1px;background:#555;"></div>
        <div style="width:5px;height:5px;border-radius:50%;background:#555;"></div>
      </div>
    </div>
    <div style="width:45%;display:flex;flex-direction:column;gap:6px;align-items:flex-start;">
      <div style="display:flex;align-items:center;gap:6px;">
        <div style="width:5px;height:5px;border-radius:50%;background:#555;"></div>
        <div style="width:20px;height:1px;background:#555;"></div>
        <span style="font-size:8px;color:#555;">Weighted avg score</span>
      </div>
      <div style="display:flex;align-items:center;gap:6px;">
        <div style="width:5px;height:5px;border-radius:50%;background:#555;"></div>
        <div style="width:20px;height:1px;background:#555;"></div>
        <span style="font-size:8px;color:#555;">Death if any stat = 0</span>
      </div>
    </div>
  </div>

  <!-- ── 03 SPRITES ── -->
  <div style="display:flex;align-items:center;gap:0;margin-bottom:8px;position:relative;z-index:1;">
    <div style="flex:1;height:1px;background:#444;"></div>
    <div style="padding:3px 12px;border:1px solid #444;font-size:8px;letter-spacing:.25em;text-transform:uppercase;color:#888;white-space:nowrap;background:#fff;">
      03 · Sprites
    </div>
    <div style="flex:1;height:1px;background:#444;"></div>
  </div>

  <!-- Flow tag -->
  <div style="text-align:center;margin:12px 0 8px;position:relative;z-index:1;">
    <span style="font-size:7.5px;letter-spacing:.2em;color:#aaa;">/ sprites.h · PROGMEM /</span>
  </div>

  <!-- Renderer node -->
  <div style="display:flex;justify-content:center;margin:0 0 4px;position:relative;z-index:1;">
    <div style="width:90px;height:90px;border-radius:50%;border:1.5px solid #e05a2b;background:#fff;display:flex;flex-direction:column;align-items:center;justify-content:center;text-align:center;">
      <span style="font-size:8px;font-weight:700;color:#e05a2b;line-height:1.3;">Pixel Art<br>Renderer</span>
      <span style="font-size:7px;color:#888;margin-top:2px;letter-spacing:.1em;">U8G2 · MSB-FIRST</span>
    </div>
  </div>

  <!-- Sprite branches -->
  <div style="display:flex;justify-content:space-between;margin:6px 0 16px;position:relative;z-index:1;">
    <div style="width:45%;display:flex;flex-direction:column;gap:6px;align-items:flex-end;">
      <div style="display:flex;align-items:center;gap:6px;">
        <span style="font-size:8px;color:#555;">Size 4 · 28×34px · thriving</span>
        <div style="width:20px;height:1px;background:#555;"></div>
        <div style="width:5px;height:5px;border-radius:50%;background:#555;"></div>
      </div>
      <div style="display:flex;align-items:center;gap:6px;">
        <span style="font-size:8px;color:#555;">Size 3 · 21×26px · okay</span>
        <div style="width:20px;height:1px;background:#555;"></div>
        <div style="width:5px;height:5px;border-radius:50%;background:#555;"></div>
      </div>
      <div style="display:flex;align-items:center;gap:6px;">
        <span style="font-size:8px;color:#555;">Size 2 · 14×17px · neglected</span>
        <div style="width:20px;height:1px;background:#555;"></div>
        <div style="width:5px;height:5px;border-radius:50%;background:#555;"></div>
      </div>
    </div>
    <div style="width:45%;display:flex;flex-direction:column;gap:6px;align-items:flex-start;">
      <div style="display:flex;align-items:center;gap:6px;">
        <div style="width:5px;height:5px;border-radius:50%;background:#555;"></div>
        <div style="width:20px;height:1px;background:#555;"></div>
        <span style="font-size:8px;color:#555;">Size 1 · 7×9px · critical</span>
      </div>
      <div style="display:flex;align-items:center;gap:6px;">
        <div style="width:5px;height:5px;border-radius:50%;background:#555;"></div>
        <div style="width:20px;height:1px;background:#555;"></div>
        <span style="font-size:8px;color:#555;">Grave · 21×25px · dead</span>
      </div>
      <div style="display:flex;align-items:center;gap:6px;">
        <div style="width:5px;height:5px;border-radius:50%;background:#555;"></div>
        <div style="width:20px;height:1px;background:#555;"></div>
        <span style="font-size:8px;color:#555;">Sine bounce animation</span>
      </div>
    </div>
  </div>

  <!-- ── 04 OUTPUT ── -->
  <div style="display:flex;align-items:center;gap:0;margin-bottom:16px;position:relative;z-index:1;">
    <div style="flex:1;height:1px;background:#444;"></div>
    <div style="padding:3px 12px;border:1px solid #444;font-size:8px;letter-spacing:.25em;text-transform:uppercase;color:#888;white-space:nowrap;background:#fff;">
      04 · Output
    </div>
    <div style="flex:1;height:1px;background:#444;"></div>
  </div>

  <!-- Funnel ovals -->
  <div style="display:flex;flex-direction:column;align-items:center;gap:8px;margin-bottom:24px;position:relative;z-index:1;">
    <div style="width:260px;padding:7px 0;border:1.5px solid #1a1a1a;border-radius:40px;text-align:center;font-size:8px;color:#1a1a1a;letter-spacing:.05em;">OLED display · 128×128px</div>
    <div style="width:220px;padding:7px 0;border:1.5px dashed #888;border-radius:40px;text-align:center;font-size:8px;color:#666;letter-spacing:.05em;">Corner stat overlay (F / S / W)</div>
    <div style="width:180px;padding:7px 0;border:1.5px dashed #888;border-radius:40px;text-align:center;font-size:8px;color:#666;letter-spacing:.05em;">Death screen · gravestone</div>
    <div style="width:140px;padding:7px 0;border:1.5px dashed #888;border-radius:40px;text-align:center;font-size:8px;color:#666;letter-spacing:.05em;">NVS autosave · 60s</div>
  </div>

  <!-- Footer tagline -->
  <div style="text-align:center;position:relative;z-index:1;">
    <div style="font-size:7.5px;letter-spacing:.3em;text-transform:uppercase;color:#e05a2b;">/ take care of me /</div>
  </div>

  </div>
</div>
<!-- END DIAGRAM -->
---

<!-- IMAGE STRIP -->
<div style="margin: 20px 0 8px 0;">
  <div style="font-size:9px; letter-spacing:.25em; text-transform:uppercase; color:#888; margin-bottom:12px;">Mochi Screen Display</div>
  <div style="display:flex; flex-direction:row; gap:4px; overflow-x:auto; overflow-y:hidden; width:100vw; position:relative; left:50%; transform:translateX(-50%);">
    <div style="flex:0 0 auto;"><img src="../images/mochi_01_boot_heart.jpg" alt="mochi" style="height:240px; width:auto; display:block;"></div>
    <div style="flex:0 0 auto;"><img src="../images/mochi_02_hi_im_mochi.jpg" alt="mochi" style="height:240px; width:auto; display:block;"></div>
    <div style="flex:0 0 auto;"><img src="../images/mochi_04_size3_okay.jpg" alt="mochi" style="height:240px; width:auto; display:block;"></div>
    <div style="flex:0 0 auto;"><img src="../images/mochi_05_size2_neglected.jpg" alt="mochi" style="height:240px; width:auto; display:block;"></div>
    <div style="flex:0 0 auto;"><img src="../images/mochi_06_size1_critical.jpg" alt="mochi" style="height:240px; width:auto; display:block;"></div>
    <div style="flex:0 0 auto;"><img src="../images/mochi_07_death.jpg" alt="mochi" style="height:240px; width:auto; display:block;"></div>
  </div>
  <div style="font-size:11px; color:#aaa; margin-top:8px; font-style:italic;">Scroll to see more →</div>
</div>


<!-- DEVICE DOCUMENTATION GRID -->
<div class="section-label">Documentation</div>
<div style="display:grid; grid-template-rows:auto auto; gap:8px; margin-bottom:56px;">
  

  <!-- Bottom row — three equal photos -->
  <div style="display:grid; grid-template-columns:1fr 1fr 1fr; gap:8px;">
    <div style="aspect-ratio:1/1; overflow:hidden; border:1px solid #d0cdc8;">
      <img src="../images/mochi 2.jpeg" alt="Echo of Mind" style="width:100%;height:100%;object-fit:cover;">
    </div>
    <div style="aspect-ratio:1/1; overflow:hidden; border:1px solid #d0cdc8;">
      <img src="../images/mochi 3.jpeg" alt="Echo of Mind" style="width:100%;height:100%;object-fit:cover;">
    </div>
    <div style="aspect-ratio:1/1; overflow:hidden; border:1px solid #d0cdc8;">
      <img src="../images/mochi 5.jpeg" alt="Echo of Mind" style="width:100%;height:100%;object-fit:cover;">
    </div>
  </div>

</div>

---

</div>
<h3 style="margin-top:0; text-align:center;"> Personal Reflection of Week 1.</h3>
</div>

</div>
<h3 style="margin-top:0; text-align:left;"> Cognitive Traces.</h3>
<p style="font-size:15px; line-height:1.5; text-align:center; max-width:700px; margin: 0 auto 40px auto;">
   Originally we tried using an open source Tamagotchi I found online, but after our previous experience in cognitive orgies struggling with a similar approach, I made the decision to build from scratch instead. That experience taught me something important: using open source code is genuinely difficult to modify and adapt to your needs. It is almost always more effective to use an existing project as inspiration and reference, but to build your own implementation from the ground up.
</p>
 </div>

---

</div>
<h3 style="margin-top:0; text-align:left;"> Moral Traces.</h3>
<p style="font-size:15px; line-height:1.5; text-align:center; max-width:700px; margin: 0 auto 40px auto;">
   The group had a really healthy dynamic where everyone worked in areas they genuinely wanted to grow in, while still contributing to a shared project. I focused on building Mochi from scratch and designing it as open source so the other group members could make their own versions and adapt it to whatever screen size they needed. We supported each other in moments of needing help or making stylistic choices, but maintained a real respect for each person to develop their own work independently. It was a very positive group dynamic overall.
</p>
 </div>

---

</div>
<h3 style="margin-top:0; text-align:left;"> Technical Process Traces.</h3>
<p style="font-size:15px; line-height:1.5; text-align:center; max-width:700px; margin: 0 auto 40px auto;">
  One of the more difficult design challenges was figuring out how to physically fit the Arduino, buttons, and power source into a device we wanted to keep small and compact. To solve this, I designed a star shaped enclosure that functions as a carabiner and acts as an open container to hold all the components together. In the end it turned out considerably larger than intended, but it was a deliberate design decision. Looking back, in future prototyping rounds I would revisit that solution and find a more compact alternative.
</p>
 </div>

---


 <div>
 <p style="text-align:center; font-size:20px; font-weight:500; margin:10px 0 10px 0;">
  Build your own MOCHI
</p>

<!-- White box with black border BLINKING, text stays solid -->
<div class="blink-box" style="
  background-color:white;
  width:100%;
  padding:18px;
  text-align:center;
  margin-top:10px;
  border:2px solid black;
">

<a href="https://github.com/hannahpeevey254/MOCHI-PET"
   style="color:#0066ff; font-size:20px; text-decoration:none; font-weight:600;">
   https://github.com/hannahpeevey254/MOCHI-PET
</a>

</div>
</div>