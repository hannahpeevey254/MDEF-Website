## ★  Reflections 1: Extended Intelligence II

<div style="display:grid; grid-template-columns:repeat(3, 1fr); gap:16px; margin-bottom:2rem;">
  <img src="../images/EXTENDED INTELL IMAGE 4.jpg" style="width:100%; height:auto;">
  <img src="../images/EXTENDED INTELL IMAGE 3.jpg" style="width:100%; height:auto;">
  <img src="../images/EXTENDED INTELL IMAGE 5.jpg" style="width:80%; height:auto;">
</div>

<!-- INTRO TEXT -->
<p style="font-size:15px; line-height:1.5; text-align:center; max-width:700px; margin: 0 auto 20px auto;">
     For <strong>Extended Intelligences II</strong> my group initially proposed creating a weather radio. This radio would use your geolocation to detect the surrounding environment. Conditions such as rain sunshine wind snow or overcast would be identified and used to curate a music playlist. The playlist was intended to function as a mood stabilizer by aligning your emotional state with the environment rather than opposing it.

    As the project developed and we considered our available resources technical limitations and experience with the OpenAI Agent Builder the direction shifted. Instead of relying only on weather data we began to incorporate immediate localized environmental sensing.

    We introduced an LDR sensor to measure the ambient light level in the room. Higher values indicated brighter conditions while lower values indicated darker spaces. This data was captured using a Raspberry Pi Pico and MicroPython.

    Using OpenAI’s Agent Builder we first attempted to connect curated playlists through Zapier. Due to technical difficulties integrating Zapier as an API within the agent workflow we decided to rely entirely on OpenAI agents.

</p>

---

<!-- SECTION: We built a three agent system. -->
<div style="display:flex; align-items:flex-start; justify-content:space-between; gap:20px; margin-top:30px;">

 <!-- LEFT SIDE TEXT -->
 <div style="width:55%; font-size:12px; line-height:1.5;">
        <h3 style="margin-top:0;"> We built a three agent system.</h3>

 <p>
        
    
    The first was a light measuring agent connected to the LDR through MCP. It was prompted to provide the light condition of the room.

    The second was a weather agent which used the web search tool to retrieve the current weather conditions in Barcelona. This data was combined with the light data from the previous agent.

    The third was a music recommendation agent. It used both the weather and light information to suggest a song. The agent referenced an MIT study linking temperature changes to mood and selected a track that could act as a mood stabilizer.

    When the system ran it first detected the light level in the room. It then combined that information with real time weather data from Barcelona. The final output was a song recommendation intended to stabilize mood in relation to the surrounding environment.
   </p>   
 </div>

 <!-- RIGHT SIDE IMAGE -->
  <div style="width:45%; text-align:center;">
        <img src="../images/EXTENDED INTELL IMAGE 6.jpg" style="width:100%; height:100%; border-radius:6px;">
  </div>

---

</div>
<h3 style="margin-top:0; text-align:center;"> Reflection.</h3>
<p style="font-size:15px; line-height:1.5; text-align:center; max-width:700px; margin: 0 auto 40px auto;">
    If we were to continue or expand this project I would want to move it toward a community based system. Instead of operating only at an individual level the system could use phone geolocation to assign the same Spotify playlist to everyone within a defined radius. This shared musical output would respond to weather and environmental conditions with the goal of stabilizing the collective mood of an urban area.
This approach would allow the project to shift from a personal experience to a study of how sound weather and environment interact at a city scale.


</p>
 </div>

---
 <h3 style="margin-top:0; text-align:center;"> Progress.</h3>

<div style="display:grid; grid-template-columns:repeat(2, 1fr); gap:16px; margin-bottom:2rem;">
  <img src="../images/EXTENDED INTELL IMAGE 2.jpeg" style="width:100%; height:auto;">
  <img src="../images/EXTENDED INTELL IMAGE 1.jpeg" style="width:100%; height:auto;">

</div>