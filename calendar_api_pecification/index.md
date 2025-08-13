---
title: Calendar API Specification 
nav_order: 6 
layout: home
has_children: true
---


# Calendar API Specification

## Calendar

### Create Calendar
**POST** `/calendars`  
Create a new calendar.

**Payload**
```json
{
  "name": "Engineering Team Calendar",
  "color_theme": "blue",
  "visibility": "public"
}
```

**Response**
```json
{
  "status": "ok",
  "calendar": {
    "id": "c1f0b7d2-74f8-4c39-8c1a-9db26dddbaf6",
    "name": "Engineering Team Calendar",
    "color_theme": "blue",
    "visibility": "public",
    "created_at": "2025-08-11T09:00:00Z"
  }
}
```

---

### Read Calendar
**GET** `/calendars/:id`  
Get a calendar by ID.

**Response**
```json
{
  "status": "ok",
  "calendar": {
    "id": "c1f0b7d2-74f8-4c39-8c1a-9db26dddbaf6",
    "name": "Engineering Team Calendar",
    "color_theme": "blue",
    "visibility": "public",
    "created_at": "2025-08-11T09:00:00Z"
  }
}
```

---

### Update Calendar
**PUT** `/calendars/:id`  
Update a calendar.

**Payload**
```json
{
  "name": "Engineering Calendar",
  "color_theme": "green",
  "visibility": "private"
}
```

**Response**
```json
{
  "status": "ok",
  "calendar": {
    "id": "c1f0b7d2-74f8-4c39-8c1a-9db26dddbaf6",
    "name": "Engineering Calendar",
    "color_theme": "green",
    "visibility": "private"
  }
}
```

---

### Delete Calendar
**DELETE** `/calendars/:id`

**Response**
```json
{ "status": "ok" }
```

---

### List Calendars
**GET** `/calendars`

**Response**
```json
{
  "status": "ok",
  "calendars": [
    { "id": "1", "name": "Engineering", "visibility": "public" },
    { "id": "2", "name": "Marketing", "visibility": "private" }
  ]
}
```

---

## Event

### Create Event
**POST** `/events`

**Payload**
```json
{
  "calendar_id": "c1f0b7d2-74f8-4c39-8c1a-9db26dddbaf6",
  "name": "Weekly Standup",
  "description": "Engineering sync",
  "start_time": "2025-08-12T10:00:00Z",
  "end_time": "2025-08-12T10:30:00Z",
  "visibility": "private",
  "location": "Zoom",
  "all_day": false
}
```

**Response**
```json
{
  "status": "ok",
  "event": {
    "id": "a14cfe84-3d99-4d45-b1c1-d6f1ac676c2a",
    "calendar_id": "c1f0b7d2-74f8-4c39-8c1a-9db26dddbaf6",
    "name": "Weekly Standup",
    "start_time": "2025-08-12T10:00:00Z",
    "end_time": "2025-08-12T10:30:00Z"
  }
}
```

---

### Get Event
**GET** `/events/:id`

**Response**
```json
{
  "status": "ok",
  "event": {
    "id": "a14cfe84-3d99-4d45-b1c1-d6f1ac676c2a",
    "name": "Weekly Standup",
    "description": "Engineering sync",
    "start_time": "2025-08-12T10:00:00Z",
    "end_time": "2025-08-12T10:30:00Z",
    "visibility": "private",
    "location": "Zoom"
  }
}
```

---

### Update Event
**PUT** `/events/:id`

**Payload**
```json
{
  "name": "Weekly Sync",
  "start_time": "2025-08-12T11:00:00Z"
}
```

**Response**
```json
{
  "status": "ok",
  "event": {
    "id": "a14cfe84-3d99-4d45-b1c1-d6f1ac676c2a",
    "name": "Weekly Sync",
    "start_time": "2025-08-12T11:00:00Z"
  }
}
```

---

### Delete Event
**DELETE** `/events/:id`

**Response**
```json
{ "status": "ok" }
```

---

### List Events in Calendar
**GET** `/calendars/:calendar_id/events`

**Response**
```json
{
  "status": "ok",
  "events": [
    { "id": "1", "name": "Standup" },
    { "id": "2", "name": "Sprint Planning" }
  ]
}
```

---

## Availability

### Free/Busy
**POST** `/availability/free-busy`

**Payload**
```json
{
  "users": ["u1", "u2", "u3"],
  "start_time": "2025-08-12T00:00:00Z",
  "end_time": "2025-08-19T00:00:00Z"
}
```

**Response**
```json
{
  "status": "ok",
  "availability": {
    "u1": [{"start": "2025-08-12T09:00Z", "end": "2025-08-12T10:00Z"}],
    "u2": [],
    "u3": [{"start": "2025-08-14T15:00Z", "end": "2025-08-14T16:00Z"}]
  }
}
```

---

### Suggest Slots
**POST** `/availability/suggest`

**Payload**
```json
{
  "users": ["u1", "u2", "u3"],
  "start_time": "2025-08-12T00:00:00Z",
  "end_time": "2025-08-19T00:00:00Z",
  "duration_minutes": 60
}
```

**Response**
```json
{
  "status": "ok",
  "slots": [
    { "start": "2025-08-13T10:00Z", "end": "2025-08-13T11:00Z" },
    { "start": "2025-08-15T14:00Z", "end": "2025-08-15T15:00Z" }
  ]
}
```

---

## Callbacks

- `/callbacks/event_reminder` – server → participant before event start  
- `/callbacks/invitation_response` – participant → server response to invite  
- `/callbacks/event_updated` – server → subscribers when event changes  
- `/callbacks/event_status` – generic for invites, updates, cancels, reschedules  
