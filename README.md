# Uncommon HTML Bug: innerHTML vs. createElement/appendChild

This repository demonstrates a subtle but important difference in DOM manipulation in HTML: the potential security risks and inefficiencies when directly adding HTML strings using `innerHTML` compared to creating elements with `createElement` and appending with `appendChild`.

The `bug.html` file shows an example of an inefficient approach which is also vulnerable to Cross-Site Scripting (XSS) attacks if the text content is dynamically generated without proper sanitization. The `bugSolution.html` file presents a more robust and secure method.

**Key Differences:**

* **Security:**  Using `innerHTML` to insert unsanitized user-supplied HTML is a major security vulnerability.  `createElement`/`appendChild` offers safer control.
* **Performance:**  `createElement`/`appendChild` is generally faster than `innerHTML` for more complex DOM manipulations, particularly in large applications.