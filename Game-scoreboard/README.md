# Game Scoreboard
- [x] three stars player record
- [x] goals record
- [x] Highlights support GIF/YouTube video
- [ ] supports other sports

Code Pen: [https://codepen.io/c821118/pen/zxKVmjK](https://codepen.io/c821118/pen/zxKVmjK)

AO3 Sample: 


# Wrapper
Wrap whole scoreboard in `<div class="scoreboard">`.
```HTML
<div class="scoreboard">
  <div class="sb-header">...</div>
  <div class="sb-top-section">...</div>
  <div class="sb-media">...</div>
  <div class="sb-stars-section">...</div>
</div>
```

# Header: sb-header
The league logo and game date are wrapped in `<div class="sb-header">`.

The logo using `<img class="sb-header-logo">`.

Date using `<span class="sb-header-title">`.

```HTML
<div class="sb-header">
  <img class="sb-header-logo" src=" " alt="Logo">
  <span class="sb-header-title">MLH Scoreboard: Apr 10</span>
</div>
```


# Top Section: sb-top-section
Top section including game status, matchup information, and game information are wrapped in `<div class="sb-top-section">`.

Game status using `<div class="sb-status">`, this is used to indicate the current period number or whether the game has ended, "FINAL" means the game is over. 

Matchup information using `<div class="sb-matchup">`.

Game information using `<div class="sb-game-info">`, this is used to indicate which game of the season, the leading team, and the stadium location.

```HTML
<div class="sb-top-section">
  <div class="sb-status">FINAL</div>
  <div class="sb-matchup">...</div>
  <div class="sb-game-info">
    Game 1, MTL leads 1-0, Bell Centre, Montreal, QC
  </div>
</div>
```

## Matchup information: sb-matchup

Matchup information is wrapped in  `<div class="sb-matchup">`, this is used to indicate the teams, scores of each period, total score, and winning team.

This is a two-column layout; the left column shows the teams, and the right column shows the scores.

The left column using `<div class="sb-teams">`.

The right column using `<div class="sb-scores">`.

```HTML
<div class="sb-matchup">
  <div class="sb-teams">...</div>
  <div class="sb-scores">...</div>
</div>
```

### The Teams : sb-teams
Both `<div class="sb-team-row">` need to be wrapped in `<div class="sb-teams">`, listing the away team first, followed by the home team.

The logos, names, and record of both teams are wrapped in `<div class="sb-team-row">`.

The winning team uses `<span class="sb-arrow">▶</span>`, the losing team leaves a blank space `<span class="sb-arrow">　</span>`.

The logo of team using `<img class="sb-logo">`. 

Team name using `<span class="sb-team-name">`.

The win-loss record for the current season using `<span class="sb-team-record">`.

```HTML
<div class="sb-teams">

  <div class="sb-team-row">
    <span class="sb-arrow">▶</span>
    <img class="sb-logo" src=" " alt="Away team logo">
    <span class="sb-team-name">  </span>
    <span class="sb-team-record">1-0</span>
  </div>

  <div class="sb-team-row">
    <span class="sb-arrow">　</span>
    <img class="sb-logo" src=" " alt="Home team logo">
    <span class="sb-team-name">  </span>
    <span class="sb-team-record">0-1</span>
  </div>

</div>
```

### The Scores: sb-scores
The total score of the game is wrapped in `<div class="sb-scores">`.

Score for each period are wrapped in `<dl class="sb-period">`, a hockey game has three periods, if there is an overtime(OT) period, it is the fourth period.

Using `<dl class="sb-period sb-total">` for the total score.

The period number using `<dt>1</dt>`, if there is an overtime period, using `<dt>OT</dt>`. 

The total score using `<dt>T</dt>`.

Scores using `<dd>`,  listing the away team first, followed by the home team. 

Finally, the winning team's total score using `<dd class="winner-score">`.

```HTML
<div class="sb-scores">
  <dl class="sb-period">
    <dt>1</dt>
    <dd>0</dd>
    <dd>1</dd>
  </dl>

  <dl class="sb-period">
    <dt>2</dt>
    <dd>1</dd>
    <dd>0</dd>
  </dl>

  <dl class="sb-period">
    <dt>3</dt>
    <dd>1</dd>
    <dd>1</dd>
  </dl>

  <dl class="sb-period">
    <dt>OT</dt>
    <dd>1</dd>
    <dd>0</dd>
  </dl>

  <dl class="sb-period sb-total">
    <dt>T</dt>
    <dd class="winner-score">3</dd>
    <dd>2</dd>
  </dl>
</div>
```

# Highlight Media: sb-media
The game highlight picture or video is wrapped in `<div class="sb-media">`.

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
Players or goals record is wrapped in  `<div class="sb-stars-section">`.

In this section, you can describe the best player or the goals record, using the same code, only the text content is different.

Title using `<div class="sb-stars-title">`, "THREE STARS" or "GOALS".

Each player uses one `<div class="sb-star-row">`.

```HTML
<div class="sb-stars-section">
  <div class="sb-stars-title">THREE STARS / GOALS</div>
  <div class="sb-star-row">...</div>
  <div class="sb-star-row">...</div>
  ...
</div>
```

## Player information: sb-star-row (THREE STARS)
Each player is wrapped in `<div class="sb-star-row">`.

Player avatar using `<img class="sb-star-img" src=" ">`.

The player information is wrapped in `<div class="sb-star-info">`.

Player's name using `<div class="sb-star-name">`, team name and position using `<span class="sb-star-meta">`.

Goals of today's game using `<div class="sb-star-game-stat">`, including assists.

Goals of this season using `<div class="sb-star-season-stat">`.

```HTML
<div class="sb-star-row">
  <img class="sb-star-img" src=" ">
  <div class="sb-star-info">

    <div class="sb-star-name">Ilya Rozanov
      <span class="sb-star-meta">BOS C</span>
    </div>

    <div class="sb-star-game-stat">3 GOALS, 1 AST</div>

    <div class="sb-star-season-stat">Season: 3 GOALS, 1 AST</div>

  </div>
</div>
```

## Player information: sb-star-row (GOALS)
Each goal is wrapped in `<div class="sb-star-row">`.

Player avatar using `<img class="sb-star-img" src=" ">`.

The player information are wrapped in `<div class="sb-star-info">`.

Player's name and goals of today's game using `<div class="sb-star-name">`, using `<span class="sb-star-meta">` to remark PPG(Power Play Goal), SHG(Shorthanded Goal) or EN(Empty Net).

Assist players of this goal using `<div class="sb-star-game-stat">` and their assists.

Goals of this season using `<div class="sb-star-season-stat">`.
The score, period, and time of this goal at that moment using `<div class="sb-star-season-stat">`.

```HTML
<div class="sb-star-row">
  <img class="sb-star-img" src=" ">

  <div class="sb-star-info">
    <div class="sb-star-name">Shane Hollander (1)
      <span class="sb-star-meta">PPG</span>
    </div>

    <div class="sb-star-game-stat">Ilya Rozanov (1)</div>

    <div class="sb-star-season-stat">BOS 2 - MTL 1 (2nd - 05:00)</div>
  </div>
</div>
```

