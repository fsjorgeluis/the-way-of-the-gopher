
# 🧱 Chapter 1: Installation and Setup (macOS)

## 👋 Welcome, future Gopher

Before we write a single line of Go code, let’s set up your development environment properly. 
Whether you’re completely new to programming or coming from another language, this chapter will help you get up and running with Go on macOS, in a clean and modern way.

Let’s begin your journey — the Gopher way.

---

## 🧰 Prerequisites

You’ll need:

- A **Mac** (Intel or Apple Silicon)
- A **terminal emulator** (Terminal.app, iTerm2, Ghostty, etc.)
- A **package manager** (we’ll use [Homebrew](https://brew.sh))

---

## 🐹 Step 1: Installing Go

Go can be installed manually or through a package manager. We’ll use **Homebrew**, which is the preferred way for most macOS developers.

### 🧪 1.1 Check for Homebrew

Open your terminal and run:

```bash
brew --version
```

If you see a version number, you’re good to go. If not, install Homebrew with:

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

You can always find more documentation about [Homebrew](https://docs.brew.sh/Installation) installation on the official website.

### ☕ 1.2 Install Go

Once Homebrew is ready, install Go:

```bash
brew install go
```

After installation, confirm it’s working:

```bash
go version
```
You should see something like:
```bash
go version go1.24.1 darwin/arm64
```

If you are here, well done! Go is installed and ready to go.

## 🗂️ Step 2: Set Up Your Workspace

Let’s now configure your environment and workspace the modern way.

> Note: Starting with Go 1.11, the use of GOPATH is mostly optional thanks to Go modules (go mod). But it’s still good to understand how the workspace is structured.

### 🗺️ 2.1 Create a Go workspace

Let’s create a folder where you’ll keep all your Go projects:

```bash
mkdir -p ~/development/go-projects
cd ~/development/go-projects
```

I'm using `development`, but you can choose any other name if you want, this will be your workspace root.

## 📦 Step 3: Understanding Go Modules

Go modules are how Go handles dependencies and versions. You no longer need to worry about $GOPATH or putting your code in specific folders.
Essentially, a module is a collection of Go packages that are versioned as a single unit. Each module has a go.mod file at its root, 
which defines the module's path and lists its dependencies along with their specific versions.

We’ll initialize our first project with modules in the next step. You can find more information about Go [modules](https://go.dev/wiki/Modules) in the wiki.

> Go Modules are the official dependency management system for Go projects, introduced in Go 1.11 and becoming the default in Go 1.13.

## 👾 Step 4: Your First Go Program

Let’s build something classic: Hello, Gopher!

### 📁 4.1 Create your project folder

```bash
mkdir hello-gopher
cd hello-gopher
```

### 📦 4.2 Initialize a Go module

```bash
go mod init github.com/YOUR_USERNAME/hello-gopher
```

> Replace YOUR_USERNAME with your actual GitHub username or leave it generic — the name isn’t too important unless you plan to publish the code.

This will create a go.mod file, which tracks your module and dependencies.

### 🐹 4.3 Create the main file

Create a file named main.go:

```bash
touch main.go
```

Open it in your editor (e.g., VS Code):

```bash
code .
```

Write this content:

```go
package main

import "fmt"

func main() {
	fmt.Println("Hello, Gopher! 🦫")
}
```

**Remember:** writing code is the better way to improve your coding skills.

Yep, it's really that simple. Just like so many things in the world, to get better you simply need to do more of it.

Want to get better at running? Run more!

Want to get better at push-ups? Drop down and do some push-ups!

You can buy the best equipment. You can read all the best books. You can watch all the best videos. But at the end of the day, the best way to get better at all of these, is simply to do it more.

Experience is often the best teacher.

### 🧪 4.4 Run your program

In the terminal, run:

```bash
go run main.go
```

You should see:

```bash
Hello, Gopher! 🦫
```

That’s it. You’ve written and run your first Go program!. I know it's kinda boring, but this is the way.

Note: If you installed Go manually and get errors like command not found: go, you may need to add it to your shell.

For zsh (default in modern macOS):

```bash
echo 'export PATH=$PATH:/usr/local/go/bin' >> ~/.zshrc
source ~/.zshrc
```

If you’re using bash, change ~/.zshrc to ~/.bash_profile.

> With Homebrew, this step is usually not needed.
