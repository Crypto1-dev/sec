````md
# 📘 SEC Language Dictionary

Welcome to the **SEC command dictionary**! This file explains each command and how to use it in your code.

---

## 🧠 Format Basics

SEC commands are written inside square brackets:

```sec
[command(arguments)]
````

You can group multiple commands inside `{}` blocks:

```sec
{[main::
[say.x("Hello!")]
[num.add("5, 3")]
]}
```

---

## 📦 Main Library (`main::`)

### `[say.x("text")]`

Prints a line of text.

**Example:**

```sec
[say.x("Welcome to SEC!")]
```

---

### `[num.add("a, b")]`

Adds two or more numbers.

**Example:**

```sec
[num.add("4, 9")]
```

---

### `[num.mul("a, b")]`

Multiplies two or more numbers.

**Example:**

```sec
[num.mul("3, 2")]
```

---

### `[num.sub("a, b")]`

Subtracts the second number from the first.

**Example:**

```sec
[num.sub("10, 3")]
```

---

### `[num.div("a, b")]`

Divides the first number by the second.

**Example:**

```sec
[num.div("12, 3")]
```

---

### `[input.age("question")]`

Asks the user a question and stores the answer as `age`.

**Example:**

```sec
[input.age("How old are you?")]
```

---

### `[fetch.x(age)]`

Fetches and displays the value stored in `age`.

**Example:**

```sec
[fetch.x(age)]
```

---

## 🕶️ Shadow Library (`shadow::`)

Use this for JavaScript and timing functions.

### `[js%% ... ]`

Executes real JavaScript.

**Example:**

```sec
[js%%
console.log("Running JavaScript!")
]
```

---

### `[shadow%% ... ]`

Runs Shadow commands. Only `wait(ms)` exists for now.

**Example:**

```sec
[shadow%% 
wait(1000)
]
```

---

### `[js%% & shadow%% ... ]`

Combines JavaScript and Shadow commands.

Use `^` to simulate newlines if needed.

**Example:**

```sec
[js%% & shadow%% ^ console.log("Wait for it...") ^ wait(1000) ^ console.log("Done!") ]
```

---

## 🧪 Special Blocks

### `{[main:: ... ]}`

Groups all main commands in a logic block.

---

### `end`

Marks the end of a program (optional).

---

## 📎 Notes

* All arguments are passed as strings, e.g. `"5, 3"`.
* Commas separate arguments inside strings.
* Variables like `age` are auto-stored from inputs.

---

Want to contribute? Fork this project or edit directly at `SEC/dictionary.md`!

```
