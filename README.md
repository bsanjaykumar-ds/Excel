# 📊 Excel Data Analyst Project — VBA Macros & UserForms

A Microsoft Excel-based data management and analysis project built with **VBA (Visual Basic for Applications)**. 
This project demonstrates how to automate data entry using UserForms, validate inputs, run macros across multiple sheets,
and compute regional summaries — all within a single `.xlsm` workbook.

---

## 📁 Project File

| File | Description |
|------|-------------|
| `macro_class_one.xlsm` | Main Excel workbook with all macros, modules, and UserForms |



### ✅ UserForm 1 — Simple Data Entry Form
A basic form (`UserForm1`) for collecting user data with validation.

**Fields:**
- `NAME` — Text input
- `AGE` — Numeric input (validated)

**Behaviour:**
- Triggered via a button labeled `user_form` on Sheet2
- On submit, data is saved to the sheet and a **"Data saved"** confirmation dialog appears
- If a non-numeric value is entered in the AGE field, an **"Invalid Input — Age must be a number"** error is shown

**Screenshots:**

| Empty Form | Filled Form | Data Saved | Invalid Input |
|------------|-------------|------------|---------------|
| Form opens blank | Name + Age entered | MsgBox confirms save | Error if Age is text |

---

### ✅ UserForm 2 — Student Registration Form
An advanced form (`UserForm2`) titled **"Student Registration Form"** with richer controls.

**Fields & Controls:**
- `NAME` — TextBox
- `AGE` — TextBox + SpinButton (scroll to increment/decrement age)
- `COURSE` — ComboBox (dropdown)
- `SKILLS` — TextBox
- `Hostel required` — CheckBox
- `Gender` — OptionButtons (Male / Female) inside a Frame
- `Status` — ToggleButton labeled **Inactive/Active**
- `Submit` button — saves data
- `Clear` button — resets all fields

---

### ✅ VBA Modules

**Module1 — Core Macros:**

| Macro | Description |
|-------|-------------|
| `Firstmacro` | Inserts a header row with "Region" and "Category" columns in the active sheet |
| `Main` | Loops through all worksheets; calls `Firstmacro` on any sheet where `A1 <> "Region"` |
| `sum_total` | Loops through all worksheets; finds the last row in column F and inserts a SUM formula below it |
| `openfrom` | Opens `UserForm1` |

**Module2** — Additional macros (extension module)

---

## 🚀 How to Use

### Running a Macro
1. Open `macro_class_one.xlsm` in Excel
2. Go to **Developer → Macros** (or press `Alt + F8`)
3. Select the macro (e.g., `Firstmacro`, `Main`, `sum_total`)
4. Click **Run**

### Opening the UserForm
1. Click the `user_form` button on **Sheet2**, or
2. Run the `openfrom` macro via **Developer → Macros**

### Editing VBA Code
1. Press `Alt + F11` to open the **Visual Basic Editor (VBE)**
2. In the Project panel, expand **Modules** or **Forms**
3. Double-click any module/form to view or edit the code

---

## 🛡️ Input Validation

UserForm1 includes validation on the Submit button:

```vba
If Not IsNumeric(TextBox_Age.Value) Then
    MsgBox "Age must be a number", vbExclamation, "Invalid Input"
    Exit Sub
End If
```

## 🔧 VBA Concepts Demonstrated

- `Sub` and `Public Sub` procedures
- Looping with `For Each...Next` over `Worksheets`
- `Range`, `Selection`, `ActiveCell` object manipulation
- `ActiveCell.FormulaR1C1` for formula injection
- `MsgBox` for user feedback
- `IsNumeric()` for input validation
- UserForm controls: TextBox, Label, CommandButton, ComboBox, CheckBox, OptionButton, Frame, SpinButton, ToggleButton
- `UserForm.Show` to launch forms
- Writing form data back to worksheet cells

---

## 📸 Screenshots

| Feature | Preview |
|---------|---------|
| Sheet2 with trigger button | `user_form1.png` |
| UserForm1 — empty | `user_form_2.png` |
| UserForm1 — filled | `user_form3.png` |
| Data saved confirmation | `user_form_data_saved_.png` |
| Invalid age error | `invaild_erro_user_form.png` |
| UserForm1 in VBE | `vba1.png` |
| UserForm2 in VBE | `vba_2.png` |
| VBA Module code | `vba3.png` |
| Macro dialog | `macro.png` |

---
