# leetcode_bug_ui
Demo to simulate and fix a UI bug in LeetCode's Accepted popup outline

This project demonstrates a UI bug in LeetCode's "Accepted" popup window where the blue outline border is slightly **misaligned to the right** — even though height and corners are correct.

## 🔍 Bug Description

- Blue border appears **shifted approc ~1cm to the right(for our visualisation)**
- **Rounded corners and top/bottom alignment** are fine
- Happens when the user **submits** code and sees the "Accepted" popup



➡ You can open `bugFix.html` to view the exact behavior with 2 submit buttons:
- Left = Bug version (mimics LeetCode issue)
- Right = Corrected version

---

## 💡 Technical Notes

```css
.popup.buggy.show::after {
  transform: translateX(10px);  /* Causes the right shift */
}
