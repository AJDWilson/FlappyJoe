# Flappy Joe 🦅

A web-based 3D bird flight simulator where you control **Joe the Eagle** using your body movements via your webcam. 

Built with MediaPipe Pose for upper-body tracking and Three.js for 3D rendering.

---

## How to Fly

Flappy Joe runs in your browser and uses upper-body pose estimation to map your movements to bird flight dynamics:

| Action | Physical Gesture | Keyboard Alternative |
| :--- | :--- | :--- |
| **Takeoff** | Flap arms up and down once | `Spacebar` |
| **Climb (Gain Altitude)** | Flap arms up and down | `Spacebar` |
| **Turn Left / Right** | Tilt arms like airplane wings (one shoulder up, one down) | `A` / `D` or `Left` / `Right` arrows |
| **Fly Straight** | Keep arms level | None |
| **Dive (Fast Descent)** | Bring both hands together in front of your chest | `S` or `Down` arrow |

> **Tip:** Keep your shoulders in frame and make sure your room is decently lit for the best tracking performance. If turning feels inverted due to camera setup, click **Turn: Normal / Inverted** in the top menu or HUD to switch it.

---

## Features

- **Webcam Body Tracking:** Uses MediaPipe Pose (running locally in-browser) to detect shoulder angles, hand distance, and flapping velocity.
- **Physics-Based Flight Engine:** Gliding drag, pitch/roll dynamics, speed acceleration on dive-bombs, and smooth altitude lift.
- **Clean Camera Tracking:** Damped camera positioning prevents vertical screen bouncing while flapping.
- **Free-Roam Environment:** Open world with rolling hills, trees, floating clouds, and collectible flight rings.
- **Browser Audio Synthesizer:** Built-in Web Audio API synthesizer for wind speed effects, wing flaps, and ring pickup chimes.
- **Fallback Controls:** Full keyboard navigation support if no webcam is available or allowed.

---

## Built With

- [Three.js](https://threejs.org/) - 3D scene rendering, lighting, and camera management.
- [MediaPipe Pose](https://google.github.io/mediapipe/solutions/pose.html) - Real-time ML pose landmark detection.
- [Tailwind CSS](https://tailwindcss.com/) - Interface layouts and menu styling.
- [FontAwesome](https://fontawesome.com/) & Google Fonts ('Luckiest Guy', 'Fredoka') - Cartoon UI icons and typography.

---

## Running Locally

Because Flappy Joe is a single-file application (`index.html`), no node modules or build steps are required.

1. Clone the repository:
   ```bash
   git clone https://github.com/AJDWILSON/flappy-joe.git
   cd flappy-joe
   ```

2. Open `index.html` in your browser. 

> **Note:** Browsers require HTTPS or `localhost` to access camera permissions. Use a simple static web server if opening directly via `file://` blocks the webcam:
> ```bash
> # Python 3
> python -m http.server 8000
> 
> # npx (Node.js)
> npx serve
> ```

---

## Author

Created by **[AJDWILSON](https://github.com/AJDWILSON)**.
