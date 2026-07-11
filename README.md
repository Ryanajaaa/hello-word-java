# Run Java in Visual Studio Code (Windows)

This guide explains how to set up and run Java programs in **Visual Studio Code** using the **Java Development Kit (JDK)**.

---

## Prerequisites

Before you begin, make sure you have installed:

- Visual Studio Code
- Extension Pack for Java (Microsoft)
- Java Development Kit (JDK 17 or later)

---

## 1. Verify Java Installation

Open **Command Prompt** or **PowerShell** and run:

```bash
java --version
```

Example output:

```text
openjdk 21.0.2 2024-01-16
OpenJDK Runtime Environment
OpenJDK 64-Bit Server VM
```

Verify the Java compiler:

```bash
javac --version
```

Example output:

```text
javac 21.0.2
```

If both commands display a version, Java is installed correctly.

---

## 2. Create a Project Folder

Example:

```
JAVA/
└── hello-world-java
    └── Main.java
```

---

## 3. Create `Main.java`

```java
public class Main {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```

> **Note:** The filename must match the public class name.
>
> Example:
>
> - `Main.java` → `public class Main`

---

## 4. Open the Folder in VS Code

Open **Visual Studio Code**.

Select:

```
File
→ Open Folder...
```

Choose your project folder.

---

## 5. Compile the Program

Open the integrated terminal:

```
Terminal
→ New Terminal
```

Run:

```bash
javac Main.java
```

If compilation is successful, Java generates:

```
Main.class
```

---

## 6. Run the Program

Run:

```bash
java Main
```

Output:

```text
Hello, World!
```

---

# Compile Multiple Java Files

Example project:

```
project/
│
├── Main.java
├── Student.java
└── Teacher.java
```

Compile all files:

```bash
javac *.java
```

Run:

```bash
java Main
```

---

# Useful Commands

Check Java version:

```bash
java --version
```

Check Java compiler version:

```bash
javac --version
```

Compile:

```bash
javac Main.java
```

Compile all Java files:

```bash
javac *.java
```

Run:

```bash
java Main
```

---

# Using the VS Code Run Button

If you have installed the **Extension Pack for Java**, you can also run your program without using the terminal.

1. Open `Main.java`.
2. Click the **Run** (▶) button above the `main()` method.
3. VS Code will automatically compile and run the program.

---

# Common Errors

## `'java' is not recognized`

Cause:

- Java is not installed.
- Java is not added to the system PATH.

Solution:

- Install the Java Development Kit (JDK).
- Add the JDK `bin` directory to your system PATH.
- Restart VS Code or your terminal.

---

## `'javac' is not recognized`

Cause:

The Java compiler is not available in your PATH.

Solution:

- Verify that the JDK (not just the JRE) is installed.
- Add the JDK `bin` folder to your PATH.

---

## `Could not find or load main class Main`

Cause:

- You are in the wrong directory.
- The class name is incorrect.
- The `.class` file was not generated.

Solution:

- Make sure you are inside the project folder.
- Compile the program again:

```bash
javac Main.java
```

Then run:

```bash
java Main
```

---

## `class Main is public, should be declared in a file named Main.java`

Cause:

The filename does not match the public class name.

Correct example:

```text
Main.java
```

```java
public class Main
```

---

# Project Structure

```
hello-world-java/
│
├── Main.java
├── Main.class
└── README.md
```

---

# Technologies Used

- Java
- Java Development Kit (JDK)
- Visual Studio Code
- Extension Pack for Java

---

# License

This project is open-source and available under the MIT License.
