# Prompts de vídeo (Gemini · Veo) — El Taller del Carpintero

Destino: `assets/intro.mp4` (16:9, ~8 s, 1080p si se puede). Para que el scroll-scrubbing vaya suave, conviene recomprimir con un keyframe por fotograma:

```
ffmpeg -i descarga.mp4 -an -c:v libx264 -pix_fmt yuv420p -g 1 -crf 23 -movflags +faststart assets/intro.mp4
```

## Prompt principal

> Cinematic continuous single shot, 8 seconds, 16:9, no cuts. A slow, steady dolly-in through the open wooden door of a small, traditional carpentry workshop in an old Madrid neighbourhood, warm late-afternoon light streaming through a high window, fine sawdust floating in the light beams. The camera glides past a workbench with hand planes, chisels and curled wood shavings, then continues forward and gently rises to reveal a finished floor-to-ceiling solid walnut bookshelf built into a wall niche, perfectly fitted, with soft warm lighting on its shelves. Shallow depth of field, rich warm wood tones, 35mm film look, smooth constant camera speed, no camera shake. No text, no logos, no watermarks, no people.

## Prompt alternativo

> Continuous 8-second macro-to-wide shot, 16:9, no cuts. Starts extremely close on the grain of a freshly planed oak board, golden side light, tiny wood shavings. The camera slowly pulls back and rises in one smooth motion to reveal the board is one of the shelves of a custom-built wooden library wall in a bright, elegant Madrid apartment with high ceilings and a wrought-iron balcony window. Warm natural light, calm atmosphere, cinematic colour grading, constant slow camera movement suitable for scroll-controlled playback. No text, no logos, no people, no faces.

Notas: movimiento constante y sin cortes (el scroll avanza y retrocede el vídeo). Evitar personas reconocibles, marcas y texto.
