# Game Scoreboard
- [x] three stars player record
- [x] goals record
- [x] highlight supports gif
- [x] highlight supports Youtube video
- [ ] supports other sports

Code Pen: [https://codepen.io/c821118/pen/zxKVmjK](https://codepen.io/c821118/pen/zxKVmjK)

AO3 Sample: 


# Wrapper
Wrap whole scoreboard in `<div class="scoreboard">`.
```HTML
<div class="scoreboard">
  <div class="sb-header"></div>
  <div class="sb-top-section"></div>
  <div class="sb-media"></div>
  <div class="sb-stars-section"></div>
</div>
```

# Header: sb-header
League logo and game date wrap in `<div class="sb-header">`.

Logo using `<img class="sb-header-logo">`.

Date using `<span class="sb-header-title">`.

```HTML
<div class="sb-header">
  <img class="sb-header-logo" src=" " alt="Logo">
  <span class="sb-header-title">MLH Scoreboard: Apr 10</span>
</div>
```


# Top Section: sb-top-section
Game status, score, and game informaion wrap in `<div class="sb-top-section">`.

Game status using `<div class="sb-status">`, this is used to indicate the current period number or whether the game has ended, "FINAL" means the game is over. 

Score using `<div class="sb-matchup">`

Game information using `<div class="sb-game-info">`, this is used to indicate which game of the season, the leading team, and the stadium location.

```HTML
<div class="sb-top-section">
  <div class="sb-status">FINAL</div>
  <div class="sb-matchup"></div>
  <div class="sb-game-info">
    Game 1, MTL leads 1-0, Bell Centre, Montreal, QC
  </div>
</div>
```

## sb-matchup

```HTML
</div>
```

## sb-game-info

```HTML
</div>
```

# Highlight Media: sb-media
The game highlight wrap in `<div class="sb-media">`.

Choose one to use:
- Use an `<iframe>` for YouTube videos.
- Use an `<img>` for images or GIFs.

> [!NOTE]
> width recommended: "400"

```HTML
<div class="sb-media">
  <iframe width="400" src="https://www.youtube.com/embed/zhYisYW09H8?si=6uCYflKMlsjpjCGv" frameborder="0" ></iframe>
  <img src=" " alt="Game Highlight">
</div>
```

# Players Section: sb-stars-section
Players and goals record wrap in  `<div class="sb-stars-section">`.
In this section, you can describe the best players of the game or the goals record.

Title using `<div class="sb-stars-title">`.

Each player uses one `<div class="sb-star-row">`.

```HTML
<div class="sb-stars-section">
  <div class="sb-stars-title">THREE STARS / GOALS</div>
  <div class="sb-star-row"></div>
  <div class="sb-star-row"></div>
  ...
</div>
```

## Player information: sb-star-row

```HTML
</div>
```

##

```HTML
</div>
```

