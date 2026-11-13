# כל מערכת אחרת: ClickUp, Asana, Trello, Notion, Airtable...

הסקיל לא צריך reference לכל מערכת. Composio יודע לחפש את הכלים הנכונים. הדרך:

## באשף

1. **toolkit:** `clickup` · `asana` · `trello` · `notion` · `airtable` · `todoist` · `jira` · `linear`. לא בטוחים?
   `composio search "list tasks in <מערכת>"` מחזיר את ה-toolkit ואת הכלים.
2. **חיבור:** כמו ב-`setup.md` (`composio connections list --toolkit <slug>`, ואם חסר `composio link <slug>`).
3. **איפה המשימות:** `composio search "list <lists|projects|boards|databases|bases> in <מערכת>"` → מריצים, ומציגים עד 3
   מועמדים בשאלה 2. ב-Notion: database. ב-Airtable: base + table. ב-ClickUp: space → list. ב-Trello: board → list.
4. **שדות:** `composio search "get fields/columns of a <list|database|table> in <מערכת>"` → ממפים לפי הטבלה ב-`setup.md`
   ושומרים לכל שדה **מזהה + סוג**.
5. **אותם כללים כמו במונדיי:** שדה תאריך אמיתי לא מקבל "לא נקבע" (ריק + בהערות/תגובה); סטטוס רק מתוך הערכים
   הקיימים; אחראי רק משתמש קיים, אחרת השם בהערות.

## בריצה

- לכל פעולה (קריאה, יצירה, עדכון, תגובה): `composio search "<פעולה> in <מערכת>"`, ואז `--get-schema` על הכלי,
  ואז `composio execute`. את ה-slugs שעבדו שומרים בפרופיל תחת "כלים", כדי שבפעם הבאה לא יחפשו שוב.
- **קודם קוראים, אחר כך מתכננים.** משימה קיימת מעדכנים, לא יוצרים כפולה.
- **הערות במערכות האלה:** ClickUp/Asana/Trello = תגובה (comment) על המשימה. Notion = שדה טקסט או תוכן הדף.
  Airtable = שדה Long text.
- **אחרי הביצוע:** קוראים שוב ומשווים לתוכנית.

## אין למערכת חיבור ב-Composio?

אומרים את זה בפשטות, ומציעים: Google Sheets כמערכת ביניים (הסקיל כותב לגיליון, ואתם מעבירים), או `followup.md` בלבד
עם טבלת המשימות להעתקה. לא ממציאים חיבור.
