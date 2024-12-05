# 3. Media en HTML

## 3.1 Vídeo
HTML5 permite insertar videos nativamente:

```html
<video width="320" height="240" controls>
    <source src="video.mp4" type="video/mp4">
    <source src="video.webm" type="video/webm">
    Tu navegador no soporta el elemento de video.
</video>

<!-- Video con atributos adicionales -->
<video width="320" height="240" controls autoplay muted loop>
    <source src="video.mp4" type="video/mp4">
</video>
```

## 3.2 Audio
Similar al video, podemos insertar audio:

```html
<audio controls>
    <source src="audio.mp3" type="audio/mpeg">
    <source src="audio.ogg" type="audio/ogg">
    Tu navegador no soporta el elemento de audio.
</audio>

<!-- Audio con atributos adicionales -->
<audio controls autoplay loop>
    <source src="audio.mp3" type="audio/mpeg">
</audio>
```

## 3.3 YouTube
Para insertar videos de YouTube, se utiliza el elemento iframe:

```html
<iframe 
    width="560" 
    height="315" 
    src="https://www.youtube.com/embed/VIDEO_ID" 
    frameborder="0" 
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
    allowfullscreen>
</iframe>
