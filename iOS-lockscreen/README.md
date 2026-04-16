# iOS lockscreen
- [x] multiple notifications
- [x] specific notification icon
- [x] background image
- [x] time and bottom button bar
- [x] stacked notifications
- [ ] Hide Creator's Style
- [ ] password
- [ ] ?interactive?

Code Pen: [https://codepen.io/c821118/pen/VYKVzjE](https://codepen.io/c821118/pen/VYKVzjE)

Ao3 Sample:

# Wrapper
Wrap your whole iOS lockscreen section in `iOS-lockscreen`.
```HTML
<div class="iOS-lockscreen">
  <img class="lockscreen-bg" />
  <div class="lockscreen-content"></div>
  <div class="bottom-bar"></div>
</div>
```

## Background image
`lockscreen-bg` place in `iOS-lockscreen`.

Image recommended size is 400px × 700px.
```HTML
<img class="lockscreen-bg" src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/19/Europa-clipper-phone-backgrounds-05.png/330px-Europa-clipper-phone-backgrounds-05.png" alt="Lockscreen Background" />
```

## Bottom bar
`bottom-bar` place in `iOS-lockscreen`
```HTML
<div class="bottom-bar">
  <div class="round-btn flashlight"></div>
  <div class="round-btn camera"></div>
</div>
```
## Notification content
`lockscreen-content` place in `iOS-lockscreen`.

All status bar, time, header and notification must be wrapped inside `lockscreen-content`.
```HTML
<div class="lockscreen-content">
  <div class="status-bar"></div>
  <div class="time-container"></div>
  <div class="notif-center-header"></div>
  <div class="notif-list"></div>
</div>
```

### Status bar
`status-bar` place in `lockscreen-content`.

- `carrier` for telecom text or time.
- `status-icons` for signal strength and battery level.
```HTML
<div class="status-bar">
  <span class="carrier">T-Mobile Wi-Fi</span>
  <span class="status-icons">📶 🛜 🔋</span>
</div>
```

### Time
`time-container` place in `lockscreen-content`.
```HTML
<div class="time-container">
  <span class="date">Mon Jun 23</span>
  <span class="time">1:46</span>
</div>
```

### Notification header
`notif-center-header` place in `lockscreen-content`.
```HTML
<div class="notif-center-header">
  <span>Notification Center</span>
  <span class="close-btn">✕</span>
</div>
```

### Notification list
`notif-list` place in `lockscreen-content`.

You can have several `notif-box`  inside `notif-list`.

```HTML
<div class="notif-list">
  <div class="notif-box"></div>
  <div class="notif-box"></div>
  ...
</div>
```

#### Notification box
`notif-box` place in `notif-list`.

```HTML
<div class="notif-box">
  <div class="notif-icon"></div>
  <div class="notif-content"></div>
</div>
```


##### Notification icon
`notif-icon` place in `notif-box`.

Use <img> to customize the notification icon.
```HTML
<div class="notif-icon">
  <img src="https://www.transformativeworks.org/wp-content/uploads/2025/09/AO3-Logo-With-Hearts-1.png" style="width: 100%; height: 100%; object-fit: cover;">
</div>
```

Or define specific notification type by their name.
- notif-icon imessage
- notif-icon gmail
- notif-icon twitter
- notif-icon instagram
- notif-icon threads
```HTML
<div class="notif-icon imessage"></div>
```

> [!TIP]
> You can add your frequently used icons in CSS.
> And define that icon by `notif-icon NAME`.
```CSS
.iOS-lockscreen .notif-icon.NAME {
  background-image: url("https://raw.githubusercontent.com/c821118/AO3-skin/refs/heads/main/icon/instagram_cobynecz.png");
  background-size: 111%;
}
```


##### Notification content
`notif-content` place in `notif-box`.

Name(`notif-title`) and Time(`notif-time`) wrapped in `notif-header` inside `notif-content`.

Message(`notif-message`) wrapped inside `notif-content`.

> [!NOTE]
> You must put the `notif-header` first, then the `notif-message`.
```HTML
<div class="notif-content">
  <div class="notif-header">
    <span class="notif-title"></span>
    <span class="notif-time"></span>
  </div>

  <span class="notif-message"></span>
</div>
```

#### Notification stack
You can create a notification stack that looks similar to the notifications that pop up when you browse your phone.

> [!WARNING]
> Make sure `notif-list` added a margin-top style since removed the giant clock.
```HTML
<div class="notif-list" style="margin-top: 15px;">
```

`notif-group` place in `notif-list`.

```HTML
<details class="notif-group">
  <summary>
    <!--***Put LATEST notifications here inside summary.***-->
    <div class="notif-box"></div>

    <!--***This is expand the prompt text, also inside summary***-->
    <span class="expand-hint">📜 Tap to expand</span>

  </summary>
    <!--***Put OLD notifications here, out of the summary***-->
    <div class="notif-box"></div>
</details>
```


