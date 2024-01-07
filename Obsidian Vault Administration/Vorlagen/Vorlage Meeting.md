---
teilnehmende:
  - LINK_ZU_MENSCH
thema: ""
zusammenfassung: ""
datum: <% tp.date.now("YYYY-MM-DD H:mm") %>
note_author: 
note_title: ""
note_date_creation: <% tp.date.now("YYYY-MM-DD") %>
note_creation_time: <% tp.date.now("HH:mm:ss") %>
note_type: Meeting
tags:
---
<% await tp.file.move("Meetings/Meeting - " + tp.date.now("YYYY-MM-DD - H-mm"))%>
[Dashboard - Meetings](../../Meetings/Dashboard%20-%20Meetings.md)

---

# Thema
`=this.thema`


# Teilnehmende
- `=this.teilnehmende`

# Agenda



# Protokoll



# Weiteres Vorgehen



---

# Zusammenfassung
`=this.zusammenfassung`

