## ★  Cognitive Orgies II
</div>
<h2 style="margin-top:0; text-align:center;"> Echo of Mind.</h2>


</div>
<p style="font-size:14px; line-height:1.5; text-align:center; max-width:700px; margin: 0 auto 40px auto;">
  Echo of Mind began with a question about radical vulnerability.
  
  What happens when we make our most private mental states publicly visible? 
  
  Dreams occupy a unique position: they are deeply intimate, impossible to fake, and entirely beyond our conscious control.

    The project explores whether technology can act as a bridge between a ubconcious state and collective understanding — not through language, but through abstract visual form.

</p>
 </div>

<div style="display:flex; align-items:flex-start; justify-content:space-between; gap:20px; margin-top:30px;">

  <!-- LEFT SIDE TEXT -->
  <div style="width:55%; font-size:12px; line-height:1.5;">

 <h4 style="margin-bottom:10px;">Process</h4>

 <p>
      A person presses the blue button and speaks their dream into a microphone. 
      OpenAI Whisper transcribes the voice recording into text, which is passed to a custom 
      DreamWeaver GPT Agent. The agent interprets the dream across three psychoanalytic 
      dimensions — figurative, environmental, and emotional — and outputs a structured 
      Dream Signature as JSON.
  </p>

  <p>
      This signature becomes a visual prompt sent to FLUX.1-schnell via Hugging Face, 
      generating a unique painterly image. The image is post-processed at 800×480 with 
      grain and vignette, displayed on the Pi screen, and simultaneously pushed to a 
      public GitHub archive.
    </p>

 <h4 style="margin-top:20px; margin-bottom:10px;">Outcome</h4>

 <p>
      The Collective Archive — a live website hosted on GitHub Pages — fills up over time 
      as more people use the device. Each grid square represents one person's subconscious 
      state. The archive persists and grows, connecting strangers through their interior 
      lives in a way that language cannot.
    </p>

 <p>
      The system runs entirely on a Raspberry Pi 5 inside Docker, exposed publicly via a 
      Cloudflare Tunnel. The website polls GitHub every 10 seconds and automatically 
      places each new generated image into the next empty square on the grid.
    </p>

  </div>

  <!-- RIGHT SIDE IMAGE -->
  <div style="width:45%;">
    <img src="../images/echo-of-mind-1.jpg" style="width:100%; height:auto; border-radius:6px;">
  </div>

</div>

----

<!-- ECHO OF MIND — SELF-CONTAINED SYSTEM DIAGRAM -->
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

 <!-- ── 01 INPUT ── -->
  <div style="display:flex;align-items:center;gap:0;margin-bottom:8px;position:relative;z-index:1;">
      <div style="flex:1;height:1px;background:#444;"></div>
      <div style="padding:3px 12px;border:1px solid #444;font-size:8px;letter-spacing:.25em;text-transform:uppercase;color:#888;white-space:nowrap;background:#fff;">
        01 · Input
      </div>
      <div style="flex:1;height:1px;background:#444;"></div>
    </div>

 <!-- Raspberry Pi node -->
  <div style="display:flex;justify-content:center;margin:16px 0;position:relative;z-index:1;">
      <div style="width:90px;height:90px;border-radius:50%;border:2px solid #1a1a1a;background:#1a1a1a;display:flex;flex-direction:column;align-items:center;justify-content:center;text-align:center;">
        <span style="font-size:9px;font-weight:700;color:#fff;line-height:1.3;">Raspberry<br>Pi 5</span>
        <span style="font-size:7px;color:#888;margin-top:3px;letter-spacing:.1em;">HARDWARE</span>
      </div>
    </div>

<!-- Branches row -->
 <div style="display:flex;justify-content:space-between;margin:0 0 24px 0;position:relative;z-index:1;">
      <!-- Left -->
      <div style="width:45%;display:flex;flex-direction:column;gap:6px;align-items:flex-end;">
        <div style="display:flex;align-items:center;gap:6px;">
          <span style="font-size:8px;color:#555;text-align:right;">USB Microphone</span>
          <div style="width:20px;height:1px;background:#555;"></div>
          <div style="width:5px;height:5px;border-radius:50%;background:#555;"></div>
        </div>
        <div style="display:flex;align-items:center;gap:6px;">
          <span style="font-size:8px;color:#555;text-align:right;">Blue Button GPIO 17</span>
          <div style="width:20px;height:1px;background:#555;"></div>
          <div style="width:5px;height:5px;border-radius:50%;background:#555;"></div>
        </div>
        <div style="display:flex;align-items:center;gap:6px;">
          <span style="font-size:8px;color:#555;text-align:right;">Red Button GPIO 27</span>
          <div style="width:20px;height:1px;background:#555;"></div>
          <div style="width:5px;height:5px;border-radius:50%;background:#555;"></div>
        </div>
      </div>
      <!-- Right -->
      <div style="width:45%;display:flex;flex-direction:column;gap:6px;align-items:flex-start;">
        <div style="display:flex;align-items:center;gap:6px;">
          <div style="width:5px;height:5px;border-radius:50%;background:#555;"></div>
          <div style="width:20px;height:1px;background:#555;"></div>
          <span style="font-size:8px;color:#555;">5" HDMI Display</span>
        </div>
        <div style="display:flex;align-items:center;gap:6px;">
          <div style="width:5px;height:5px;border-radius:50%;background:#555;"></div>
          <div style="width:20px;height:1px;background:#555;"></div>
          <span style="font-size:8px;color:#555;">LED GPIO 22</span>
        </div>
        <div style="display:flex;align-items:center;gap:6px;">
          <div style="width:5px;height:5px;border-radius:50%;background:#555;"></div>
          <div style="width:20px;height:1px;background:#555;"></div>
          <span style="font-size:8px;color:#555;">Docker + Flask</span>
        </div>
      </div>
    </div>

 <!-- ── 02 AI PIPELINE ── -->
<div style="display:flex;align-items:center;gap:0;margin-bottom:8px;position:relative;z-index:1;">
      <div style="flex:1;height:1px;background:#444;"></div>
      <div style="padding:3px 12px;border:1px solid #444;font-size:8px;letter-spacing:.25em;text-transform:uppercase;color:#888;white-space:nowrap;background:#fff;">
        02 · AI Pipeline
      </div>
      <div style="flex:1;height:1px;background:#444;"></div>
    </div>

<!-- Flow tag -->
 <div style="text-align:center;margin:12px 0 8px;position:relative;z-index:1;">
      <span style="font-size:7.5px;letter-spacing:.2em;color:#aaa;">/ Voice Input /</span>
    </div>

 <!-- Whisper node -->
 <div style="display:flex;justify-content:center;margin:0 0 4px;position:relative;z-index:1;">
      <div style="width:72px;height:72px;border-radius:50%;border:1.5px solid #1a1a1a;background:#fff;display:flex;flex-direction:column;align-items:center;justify-content:center;text-align:center;">
        <span style="font-size:9px;font-weight:700;color:#1a1a1a;">Whisper</span>
        <span style="font-size:7px;color:#888;margin-top:2px;letter-spacing:.1em;">OPENAI</span>
      </div>
    </div>

 <!-- Speech→Text branch -->
 <div style="display:flex;justify-content:flex-end;margin:6px 0 6px;position:relative;z-index:1;">
      <div style="width:45%;display:flex;align-items:center;gap:6px;">
        <div style="width:5px;height:5px;border-radius:50%;background:#555;"></div>
        <div style="width:20px;height:1px;background:#555;"></div>
        <span style="font-size:8px;color:#555;">Speech → Text</span>
      </div>
    </div>

 <!-- DreamWeaver node -->
 <div style="display:flex;justify-content:center;margin:8px 0 4px;position:relative;z-index:1;">
      <div style="width:90px;height:90px;border-radius:50%;border:1.5px solid #1a1a1a;background:#fff;display:flex;flex-direction:column;align-items:center;justify-content:center;text-align:center;">
        <span style="font-size:8px;font-weight:700;color:#1a1a1a;line-height:1.3;">DreamWeaver<br>GPT Agent</span>
        <span style="font-size:7px;color:#888;margin-top:2px;letter-spacing:.1em;">INTERPRETER</span>
      </div>
    </div>

 <!-- DreamWeaver branches -->
<div style="display:flex;justify-content:space-between;margin:6px 0 8px;position:relative;z-index:1;">
      <div style="width:45%;display:flex;flex-direction:column;gap:6px;align-items:flex-end;">
        <div style="display:flex;align-items:center;gap:6px;">
          <span style="font-size:8px;color:#555;">Figurative</span>
          <div style="width:20px;height:1px;background:#555;"></div>
          <div style="width:5px;height:5px;border-radius:50%;background:#555;"></div>
        </div>
        <div style="display:flex;align-items:center;gap:6px;">
          <span style="font-size:8px;color:#555;">Environment</span>
          <div style="width:20px;height:1px;background:#555;"></div>
          <div style="width:5px;height:5px;border-radius:50%;background:#555;"></div>
        </div>
      </div>
      <div style="width:45%;display:flex;flex-direction:column;gap:6px;align-items:flex-start;">
        <div style="display:flex;align-items:center;gap:6px;">
          <div style="width:5px;height:5px;border-radius:50%;background:#555;"></div>
          <div style="width:20px;height:1px;background:#555;"></div>
          <span style="font-size:8px;color:#555;">Emotional</span>
        </div>
        <div style="display:flex;align-items:center;gap:6px;">
          <div style="width:5px;height:5px;border-radius:50%;background:#555;"></div>
          <div style="width:20px;height:1px;background:#555;"></div>
          <span style="font-size:8px;color:#555;">Dream Signature JSON</span>
        </div>
      </div>
    </div>

 <!-- Flow tag -->
  <div style="text-align:center;margin:4px 0 8px;position:relative;z-index:1;">
      <span style="font-size:7.5px;letter-spacing:.2em;color:#aaa;">/ Visual Prompt /</span>
    </div>

 <!-- FLUX node -->
 <div style="display:flex;justify-content:center;margin:0 0 4px;position:relative;z-index:1;">
      <div style="width:90px;height:90px;border-radius:50%;border:1.5px solid #e05a2b;background:#fff;display:flex;flex-direction:column;align-items:center;justify-content:center;text-align:center;">
        <span style="font-size:8px;font-weight:700;color:#e05a2b;line-height:1.3;">FLUX.1-schnell</span>
        <span style="font-size:7px;color:#888;margin-top:2px;letter-spacing:.1em;">HUGGING FACE</span>
      </div>
    </div>

 <!-- FLUX branches -->
 <div style="display:flex;justify-content:space-between;margin:6px 0 16px;position:relative;z-index:1;">
      <div style="width:45%;display:flex;align-items:center;justify-content:flex-end;gap:6px;">
        <span style="font-size:8px;color:#555;">Grain + Vignette</span>
        <div style="width:20px;height:1px;background:#555;"></div>
        <div style="width:5px;height:5px;border-radius:50%;background:#555;"></div>
      </div>
      <div style="width:45%;display:flex;align-items:center;gap:6px;">
        <div style="width:5px;height:5px;border-radius:50%;background:#555;"></div>
        <div style="width:20px;height:1px;background:#555;"></div>
        <span style="font-size:8px;color:#555;">Painterly 800×480px</span>
      </div>
    </div>

 <!-- ── 03 OUTPUT ── -->
 <div style="display:flex;align-items:center;gap:0;margin-bottom:16px;position:relative;z-index:1;">
      <div style="flex:1;height:1px;background:#444;"></div>
      <div style="padding:3px 12px;border:1px solid #444;font-size:8px;letter-spacing:.25em;text-transform:uppercase;color:#888;white-space:nowrap;background:#fff;">
        03 · Output
      </div>
      <div style="flex:1;height:1px;background:#444;"></div>
    </div>

 <!-- Funnel ovals -->
 <div style="display:flex;flex-direction:column;align-items:center;gap:8px;margin-bottom:24px;position:relative;z-index:1;">
      <div style="width:260px;padding:7px 0;border:1.5px solid #1a1a1a;border-radius:40px;text-align:center;font-size:8px;color:#1a1a1a;letter-spacing:.05em;">Pi Display — Live Pattern</div>
      <div style="width:220px;padding:7px 0;border:1.5px dashed #888;border-radius:40px;text-align:center;font-size:8px;color:#666;letter-spacing:.05em;">SQLite Local Database</div>
      <div style="width:180px;padding:7px 0;border:1.5px dashed #888;border-radius:40px;text-align:center;font-size:8px;color:#666;letter-spacing:.05em;">GitHub Push</div>
      <div style="width:140px;padding:7px 0;border:1.5px dashed #888;border-radius:40px;text-align:center;font-size:8px;color:#666;letter-spacing:.05em;">Cloudflare Tunnel</div>
    </div>

<!-- ── 04 ARCHIVE ── -->
<div style="display:flex;align-items:center;gap:0;margin-bottom:16px;position:relative;z-index:1;">
      <div style="flex:1;height:1px;background:#444;"></div>
      <div style="padding:3px 12px;border:1px solid #444;font-size:8px;letter-spacing:.25em;text-transform:uppercase;color:#888;white-space:nowrap;background:#fff;">
        04 · Archive
      </div>
      <div style="flex:1;height:1px;background:#444;"></div>
    </div>

 <!-- Arrow -->
 <div style="display:flex;flex-direction:column;align-items:center;margin-bottom:8px;position:relative;z-index:1;">
      <div style="width:1px;height:20px;background:#444;"></div>
      <div style="width:0;height:0;border-left:5px solid transparent;border-right:5px solid transparent;border-top:7px solid #444;"></div>
    </div>

<!-- Collective Archive box -->
<div style="display:flex;justify-content:center;margin-bottom:12px;position:relative;z-index:1;">
      <div style="padding:10px 28px;border:1.5px solid #1a1a1a;font-size:9px;font-weight:700;letter-spacing:.15em;text-transform:uppercase;color:#1a1a1a;">Collective Archive</div>
    </div>

 <!-- Archive branches -->
 <div style="display:flex;justify-content:space-between;margin:0 0 24px;position:relative;z-index:1;">
      <div style="width:45%;display:flex;align-items:center;justify-content:flex-end;gap:6px;">
        <span style="font-size:8px;color:#555;">GitHub Pages</span>
        <div style="width:20px;height:1px;background:#555;"></div>
        <div style="width:5px;height:5px;border-radius:50%;background:#555;"></div>
      </div>
      <div style="width:45%;display:flex;align-items:center;gap:6px;">
        <div style="width:5px;height:5px;border-radius:50%;background:#555;"></div>
        <div style="width:20px;height:1px;background:#555;"></div>
        <span style="font-size:8px;color:#555;">GitHub API (10s poll)</span>
      </div>
    </div>

 <!-- Footer tagline -->
 <div style="text-align:center;position:relative;z-index:1;">
      <div style="font-size:7.5px;letter-spacing:.3em;text-transform:uppercase;color:#e05a2b;">/ Human Connection Through a Subconscious State /</div>
 </div>

  </div>
</div>
<!-- END DIAGRAM -->

---

<!-- IMAGE STRIP -->
<div style="margin: 20px 0 8px 0;">
  <div style="font-size:9px; letter-spacing:.25em; text-transform:uppercase; color:#888; margin-bottom:12px;">Documented Dreams</div>
  <div style="display:flex; flex-direction:row; gap:4px; overflow-x:auto; overflow-y:hidden; width:100vw; position:relative; left:50%; transform:translateX(-50%);">
    <div style="flex:0 0 auto;"><img src="../images/echo-of-mind-6.jpg" alt="Echo of Mind" style="height:240px; width:auto; display:block;"></div>
    <div style="flex:0 0 auto;"><img src="../images/echo-of-mind-7.jpg" alt="Echo of Mind" style="height:240px; width:auto; display:block;"></div>
    <div style="flex:0 0 auto;"><img src="../images/echo-of-mind-8.jpg" alt="Echo of Mind" style="height:240px; width:auto; display:block;"></div>
    <div style="flex:0 0 auto;"><img src="../images/echo-of-mind-9.jpg" alt="Echo of Mind" style="height:240px; width:auto; display:block;"></div>
    <div style="flex:0 0 auto;"><img src="../images/echo-of-mind-11.jpg" alt="Echo of Mind" style="height:240px; width:auto; display:block;"></div>
  </div>
  <div style="font-size:11px; color:#aaa; margin-top:8px; font-style:italic;">Scroll to see more →</div>
</div>


<!-- DEVICE DOCUMENTATION GRID -->
<div class="section-label">Documentation</div>
<div style="display:grid; grid-template-rows:auto auto; gap:8px; margin-bottom:56px;">
  

  <!-- Bottom row — three equal photos -->
  <div style="display:grid; grid-template-columns:1fr 1fr 1fr; gap:8px;">
    <div style="aspect-ratio:1/1; overflow:hidden; border:1px solid #d0cdc8;">
      <img src="../images/echo-of-mind-15-render.jpg" alt="Echo of Mind" style="width:100%;height:100%;object-fit:cover;">
    </div>
    <div style="aspect-ratio:1/1; overflow:hidden; border:1px solid #d0cdc8;">
      <img src="../images/ECHO-OF-MIND DEVICE FRONT 2-2.jpg" alt="Echo of Mind" style="width:100%;height:100%;object-fit:cover;">
    </div>
    <div style="aspect-ratio:1/1; overflow:hidden; border:1px solid #d0cdc8;">
      <img src="../images/echo-of-mind-14-system-diagram.jpg" alt="Echo of Mind" style="width:100%;height:100%;object-fit:cover;">
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
   The project began with a repository for a project called Dream Recorder from Modem Works. When we first discovered it, we assumed we had found something like a shortcut that would make the Cognitive Orgies course much easier. Instead of building the system from scratch, we thought we could simply adapt what already existed. That assumption changed quickly. It took us about two and a half days just to get the repository running, and the process forced us through a steep learning curve. At several points I questioned whether it would actually be faster to rebuild the system ourselves rather than continue troubleshooting the repo.

What initially looked like a shortcut ended up shifting how we approached the project and our relationship with the tools we were using. Rather than functioning as a cheat code, the repository became a learning environment where we had to understand how different systems were connected and how to adapt them. In the end, we decided to document our process and publish the repository on GitHub so that future designers can learn from what worked, what broke, and how the system evolved through trial and error.
</p>
 </div>

---

</div>
<h3 style="margin-top:0; text-align:left;"> Moral Traces.</h3>
<p style="font-size:15px; line-height:1.5; text-align:center; max-width:700px; margin: 0 auto 40px auto;">
   Over the four days of the course, everyone gradually leaned into the areas where they felt most comfortable and contributed those strengths to the project. In my case, I focused on the concept development, drawings, building the AI agents, and creating the collective archive website. The first few days were challenging in terms of collaboration because the repository initially lived on a single computer and required downloading, configuring, and adapting across machines. During that time I worked independently on the archive website and the AI agents while the rest of the team focused on stabilizing the technical setup.

To guide the AI system, we created a kind of specification sheet that described the user intentions, integrations, and aesthetic direction we wanted the agent to follow. This helped us shape the behavior of the system and allowed the AI component to align more closely with the conceptual direction of the project.
</p>
 </div>

---

</div>
<h3 style="margin-top:0; text-align:left;"> Technical Process Traces.</h3>
<p style="font-size:15px; line-height:1.5; text-align:center; max-width:700px; margin: 0 auto 40px auto;">
  The repository originally outlined a specific set of tools and components that were supposed to be used to run the system. As we began assembling the project, we quickly realized that some of the required hardware and software were not available to us. Missing cables, microphones, screens, and other equipment meant that the system could not simply be reproduced as written. We had to continuously adapt the setup and find alternatives using the materials and technologies we had access to.

At the time this felt frustrating because it slowed the process and forced us to deviate from the original instructions. Looking back, those constraints actually shaped the project in important ways. They pushed us to improvise, rethink certain technical decisions, and ultimately customize the system in a way that made the final result more aligned with the experience we wanted to create.
</p>
 </div>

---


 <div>
 <p style="text-align:center; font-size:20px; font-weight:500; margin:10px 0 10px 0;">
  Explore the Collective Arhive of Echo of Mind
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

<a href="https://hannahpeevey254.github.io/ECHO-OF-MIND/"
   style="color:#0066ff; font-size:20px; text-decoration:none; font-weight:600;">
   https://hannahpeevey254.github.io/ECHO-OF-MIND/
</a>

</div>
</div>