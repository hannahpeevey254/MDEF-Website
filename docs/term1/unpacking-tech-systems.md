<!-- THREE IMAGES HORIZONTALLY ALIGNED -->
<div style="display:flex; gap:12px; justify-content:center; margin-bottom:20px;">
    <img src="../images/UPT GIF 3 PARTS.gif" style="width:40%; height:auto; border-radius:6px;">
    <img src="../images/UPT GIF 4 SPEAKER.gif" style="width:20%; height:auto; border-radius:6px;">
    <img src="../images/UPT GIF 2.gif" style="width:40%; height:auto; border-radius:6px;">
</div>


<!-- INTRO TEXT -->
<p style="font-size:15px; line-height:1.5; text-align:center; max-width:700px; margin: 0 auto 20px auto;">
    The <strong>Unpacking Tech Systems</strong> workshop consisted of two intense weeks spent diving into the hidden logic of electronic objects. 
    In the first week, we disassembled, cataloged, and examined the inner workings of a discarded device. 
    In the second week, we reassembled the components into a new hybrid system—repurposing the original parts with a completely new intention.
</p>

<p style="font-size:15px; line-height:1.5; text-align:center; max-width:700px; margin: 0 auto 40px auto;">
    For our group, we chose the vintage <strong>SUNSTECH RD-1010</strong> radio.  
    The radio still functioned perfectly when we found it, and we wanted to give it a new life by transforming its internal logic into an interactive e
</p>

<!-- SECTION: WHERE WE STARTED -->
<div style="display:flex; align-items:flex-start; justify-content:space-between; gap:20px; margin-top:30px;">

    <!-- LEFT SIDE TEXT -->
    <div style="width:55%; font-size:15px; line-height:1.5;">
        <h3 style="margin-top:0;">Where We Started</h3>

        <p>
            We began by carefully opening the radio, unscrewing the back panel and working layer by layer through the internal structure. 
            Our goal was to remove the boards without damaging any components, since we planned to reuse the control logic in our final prototype. 
            The process was exciting; each layer revealed new parts, materials, and unexpected learning curves for our team.
        </p>

        <p style="margin-bottom:6px;"><strong>Key steps in the teardown:</strong></p>
        <ul style="margin-top:6px;">
            <li>Unscrewing and removing the back casing.</li>
            <li>Disconnecting internal boards safely to preserve functionality.</li>
            <li>Documenting each component and its behavior.</li>
            <li>Identifying reusable sensors, conductors, amplifiers, and mechanical parts.</li>
        </ul>

        <p style="margin-top:10px;">
            Below is the forensic report we created, documenting every part and its specific role within the system.
        </p>
    </div>

    <!-- RIGHT SIDE IMAGE -->
    <div style="width:45%; text-align:center;">
        <img src="../images/UPT DIAGRAMS STACKED.jpg" style="width:100%; height:auto; border-radius:6px;">
    </div>

</div>

<!-- FULL-WIDTH IMAGE -->
<div style="width:100%; margin: 30px 0;">
<img src="../images/UPT ALL PARTS.jpg" style="width:100%; height:auto; border-radius:6px;">
</div>
<!-- LEFT TEXT + RIGHT IMAGE -->
<div style="display:flex; gap:20px; justify-content:space-between; margin-top:20px;">

    <!-- LEFT COLUMN TEXT -->
    <div style="width:75%; font-size:15px; line-height:1.5;">
        <p>
            We transformed the radio’s original capacitive touch board into a digital controller.
        </p>

        <p>
            We repurposed the capacitive touch sensor panel from the vintage radio and connected it to an Arduino so we could manipulate the touch-based signals.
        </p>

        <p>
            The original board had six sensor pads on the left that were designed to change radio settings when touched, and nine sensors on the right that controlled the clock functions.
        </p>

        <p>
            To interface this with our computer, we soldered wires from selected touch pads on the radio’s PCB to the numbered input pins on the Arduino. Each wire acted as its own input, and each channel was programmed to output a different beat or frequency whenever it was touched—turning the pads into touch-activated musical controls.
        </p>

        <p>
            Our goal for next week is to manipulate or reinterpret the music originally played by the radio by using its touch sensor panel as a modern interactive interface. With the Arduino receiving touch data, we sent these signals over USB into our computer and used them in TouchDesigner to drive real-time visual effects.
        </p>
    </div>

    <!-- RIGHT COLUMN IMAGE -->
    <div style="width:25%;">
        <img src="../images/UPT TOUCH SENSOR IMAGES.jpg" style="width:100%; height:auto; border-radius:6px;">
    </div>
    </div>
<!-- FULL-WIDTH IMAGE -->
<div style="display:flex; gap:12px; justify-content:center; margin-bottom:20px;">
    <img src="../images/UPT IMAGE TRACED DRAWING.jpg" style="width:50%; height:auto; border-radius:6px;">
    <img src="../images/UPT ISHAN HAND DRAWING.jpg" style="width:50%; height:auto; border-radius:6px;">
</div>
</div>

<!-- WEEK 2 HEADING -->
## Week 2
<p style="font-size:20px; margin-bottom:20px;">
    Click the bottom right corner to view my flipbook/zine.
</p>

<h3 style="margin-top:40px;">Zine</h3>

<!-- Flipbook container -->
<div id="book" style="width: 800px; height: 500px; margin: 2rem auto;">

    <!-- Page 1 -->
    <div class="page">
        <h2>THE JOY KILLER</h2>
        <p>Made with the SUNSTECH RPRD3000</p>
        <img src="../images/UPT STORY BOARD.jpg" style="width:100%; object-fit:contain;">
    </div>

    <!-- Page 2 -->
    <div class="page">
        <h2>Introduction</h2>
        <p style="font-size: 12px;">
        We transformed the vintage SUNSTECH radio into a reimagined way of playing with the childrens toy, "Jack in the Box". The intention behind the design was to expose  the hdden truth behnd the magic of Christmas.</p>
        <!-- Embedded Video -->
<iframe 
    src="https://drive.google.com/file/d/17EKpxDWs-aBYbCesM7_guWx4e_4hlSxg/preview"
    width="100%" 
    height="220" 
    style="border:0; border-radius: 6px; object-fit:contain;">
</iframe>

<!-- Optional small link below -->
<p style="font-size: 10px; margin-top: 0px;">
    Video link: 
    <a href="https://drive.google.com/file/d/17EKpxDWs-aBYbCesM7_guWx4e_4hlSxg/view?usp=sharing" target="_blank">
        click here for link
    </a>
</p>
    </div>

    <!-- Page 3 -->
    <div class="page">
        <img src="../images/UPT BEFORE AFTER.jpg" style="width:100%; height:auto;">
    </div>

    <!-- Page 4 -->
    <div class="page">
        <h3>How did we make it?</h3>
        <p>Through lots of trial and error. Many Prototypes. Lots of Hope. Countless failures. Heres the procress.</p>
        <img src="../images/UPT GROUP PIC WITH TABLE.jpg" style="width:100%; height:auto;">
    </div>
    <!-- Page 5 -->
    <div class="page">
        <img src="../images/UPT THE SYSTEM.jpg" style="width:100%; height:auto;">
    </div>
       <!-- Page 6 -->
    <div class="page">
        <h3>★ our prototypes ★ </h3>
        <p style="font-size: 8px;">
         When designing the scissor mechanism, we struggled with making the collapsed structure narrow enough to fit inside the box while still giving it enough room to move. The box was only 9 cm tall, so the mechanism had to fully collapse to hide the clown, yet still extend with enough strength and height to push the clown completely out of the box, just like a traditional jack-in-the-box.</p>
        <img src="../images/UPT PROTOTYPE DIAGRAM.jpg" style="width:100%; height:auto;">
         <p style="font-size: 8px;">
    This particular one failed because it only collapsed to 4cm, but we also needed room for the controlled motor and the clown to fit. So our way of reconstructing this was to minimize the structure down to 5 parts.
</p>

    </div>   
    <!-- Page 7 -->
    <div class="page">
        <img src="../images/UPT PROTOTYPES.jpg" style="width:100%; height:auto;">
    </div>
     <!-- Page 8 -->
    <div class="page">
        <img src="../images/UPT GEARS DIAGRAM.jpg" style="width:100%; height:auto;">
    </div>
      <!-- Page 9 -->
    <div class="page">
        <img src="../images/GEARS GIF.gif" style="width:100%; height:auto; >
    </div>
    <!-- Page 10 -->
    <div class="page">
        <img src="../images/JACK POPPING UP FINAL.jpg" style="width:100%; height:auto;">
    </div>
     <!-- Page 11 -->
    <div class="page">
        <img src="../images/JACK POPPING UP FINAL.jpg" style="width:100%; height:auto;">
    </div>
</div>

<!-- Load jQuery -->
<script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>

<!-- Load Turn.js -->
<script src="../js/turn.js"></script>


<!-- Create 2-page book -->
<script>
document.addEventListener("DOMContentLoaded", function () {
    $("#book").turn({
        width: 800,
        height: 500,
        autoCenter: true,
        display: "double",     // ← two-page layout
        gradients: true,       // nice shading effect
        elevation: 50          // stronger page flip realism
    });
});
</script>

<style>
.page {
    background-color: #cbcaccff;
    padding: 20px;
    box-shadow: 0 0 10px rgba(0,0,0,.15);
    font-family: sans-serif;
}
<style>
.page-img {
    max-width: 100%;
    max-height: 100%;
    width: 100%;       /* fills the page width, but... */
    height: auto;      /* ...maintains aspect ratio */
    object-fit: contain; /* prevents overflow in any direction */
    display: block;
}
</style>

<!-- REFLECTION SECTION -->
<h2 style="margin-top:50px;">Reflection</h2>

<p style="font-size:14px; line-height:1.6; max-width:1000px; margin-bottom:10px;">
   The second week pushed us even further as we moved from electronic sensing into mechanical storytelling. Transforming the preserved electronics into a “Jack-in-the-Box” style toy required us to combine sound, movement, timing, and physical constraints inside a box that was never meant to house any of it. Designing scissor mechanisms, calculating collapse heights, and troubleshooting gear systems made the process messy and often frustrating—but also incredibly rewarding. Every prototype taught us something new about force, friction, tolerances, and how sensitive physical systems can be when scaled down.
</p>

<p style="font-size:14px; line-height:1.6; max-width:1000px; margin-bottom:40px;">
If I were to redo this project, I would simplify the mechanical concept. Instead of creating a complex gear system squeezed into the tight constraints of the radio box, I would return to the elegance of the original jack-in-the-box mechanism: a spring-based system with a simple open-and-close trigger for the lid. This would have honored the original play logic while allowing us to focus more deeply on the electronic interaction and storytelling.
</p>


<!-- LINK GUIDE SECTION -->
<h2 style="margin-top:20px;">Link Guide</h2>

<div style="margin-bottom:10px;">
    <a href="https://www.figma.com/deck/PZwKRrZl7xRPOArGN5RcwH/Group-4--The-Raido?node-id=16-451&t=MeCWzZTfH8benLv7-1" target="_blank">
        Full Presentation Here
    </a>
</div>

<div style="margin-bottom:10px;">
    <a href="https://drive.google.com/file/d/17EKpxDWs-aBYbCesM7_guWx4e_4hlSxg/view" target="_blank">
        Watch the video here
    </a>
</div>

<div style="margin-bottom:10px;">
    <a href="https://miro.com/app/board/uXjVJuJuc9I=/" target="_blank">
       Open Forensic Report
    </a>
</div>

<div style="margin-bottom:10px;">
    <a href="https://miro.com/app/board/uXjVJuJuc9I=/" target="_blank">
        Open Inventory 
    </a>
</div>


<!-- DOCUMENTATION SECTION -->
<h2 style="margin-top:50px;">Documentation</h2>

<div style="width:100%; margin-top:20px;">
    <img src="../images/UPT DCUMENTATION DIAGRAMS.jpg" 
         style="width:100%; height:auto; border-radius:6px;">
</div>
<div style="width:100%; margin-top:20px;">
    <img src="../images/UPT DOCUMENTATION TWO.jpg" 
         style="width:100%; height:auto; border-radius:6px;">
</div>
