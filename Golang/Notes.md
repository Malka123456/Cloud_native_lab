### **Comprehensive Go (Golang) Course Notes**

---

#### **1. Introduction to Go**
- **Creation**: Developed by Google (2007), open-sourced (2009).
- **Purpose**: 
  - Solve limitations of existing languages in leveraging modern infrastructure (multi-core processors, cloud scalability).
  - Simplify writing **concurrent, multi-threaded applications** (e.g., avoid race conditions in booking systems).
- **Key Use Cases**:
  - Cloud-native applications (microservices, web backends, databases).
  - Infrastructure tools (Docker, Kubernetes, HashiCorp Vault).
  - CLI tools and automation (DevOps/SRE tasks).
- **Advantages**:
  - Simple syntax (Python-like) with performance close to C++.
  - Compiled to a **single binary** (portable across platforms).
  - Fast startup/execution, resource-efficient (low CPU/RAM usage).
  - Built-in concurrency support (goroutines, channels).
  - Strong error checking during coding (reduces runtime errors).

---

#### **2. Environment Setup**
1. **Install Go Compiler**:
   - Download from [golang.org](https://golang.org).
   - Verify: `go version` in terminal.
2. **Install VS Code**:
   - Download from [code.visualstudio.com](https://code.visualstudio.com).
3. **VS Code Go Extension**:
   - Install the official Go extension (by Google) for syntax highlighting, IntelliSense, and debugging.

---

#### **3. Basic Program Structure**
```go
package main  // Declares the package (main for executables)

import "fmt"  // Import packages (fmt for I/O)

func main() {  // Entry point of the application
    fmt.Println("Hello World")  // Print to console
}
```
- **Initialize Module**: `go mod init <module-name>` (creates `go.mod`).
- **Run Code**: `go run main.go`.

---

#### **4. Core Concepts & Syntax**
##### **Variables & Constants**
- **Variables**:
  ```go
  var conferenceName string = "Go Conference"  // Explicit type
  remainingTickets := 50                        // Type inferred (shorthand)
  ```
- **Constants**:
  ```go
  const conferenceTickets uint = 50  // Immutable value
  ```

##### **Data Types**
- **Basic Types**:
  - `string`, `int`, `uint`, `bool`, `float64`.
- **Composite Types**:
  - **Arrays**: Fixed-size (`var bookings [50]string`).
  - **Slices**: Dynamic arrays (`bookings := []string{}`).
  - **Maps**: Key-value pairs (`userData := make(map[string]string)`).
  - **Structs**: Custom types with fields of mixed types:
    ```go
    type UserData struct {
        firstName string
        lastName  string
        email     string
        userTickets uint
    }
    ```

##### **Pointers**
- Hold memory addresses of variables:
  ```go
  var firstName string
  fmt.Scan(&firstName)  // & passes pointer to Scan
  ```

##### **Formatted I/O**
- **Print**: `fmt.Printf("Welcome to %v! Tickets: %d\n", conferenceName, remainingTickets)`.
  - Placeholders: `%v` (value), `%T` (type), `%d` (integer), `\n` (newline).
- **Input**: `fmt.Scan(&userInput)`.

---

#### **5. Control Flow**
##### **Loops**
- Only `for` loop (replaces `while`, `do-while`):
  ```go
  // Infinite loop
  for {
      // Logic
  }

  // Conditional loop
  for remainingTickets > 0 {
      // Logic
  }

  // Iterate over slices/arrays
  for index, booking := range bookings {
      fmt.Printf("Booking %d: %v\n", index, booking)
  }
  ```

##### **Conditionals**
- **if-else**:
  ```go
  if userTickets > remainingTickets {
      fmt.Println("Insufficient tickets")
  } else if isValidEmail := strings.Contains(email, "@"); !isValidEmail {
      fmt.Println("Invalid email")
  } else {
      // Proceed
  }
  ```
- **switch**:
  ```go
  switch city {
  case "London", "Berlin":
      // Code for London/Berlin
  case "Singapore":
      // Code for Singapore
  default:
      fmt.Println("Invalid city")
  }
  ```

---

#### **6. Functions**
- **Syntax**:
  ```go
  func greetUser(confName string, confTickets uint) {
      fmt.Printf("Welcome to %v booking app!\n", confName)
  }
  ```
- **Multiple Returns**:
  ```go
  func validateInput(firstName string, email string) (bool, bool) {
      isValidName := len(firstName) >= 2
      isValidEmail := strings.Contains(email, "@")
      return isValidName, isValidEmail
  }
  ```
- **Calling Functions**:  
  `isValidName, isValidEmail := validateInput(firstName, email)`

---

#### **7. Code Organization**
##### **Packages**
- **Structure**:
  - Group related files in a directory (e.g., `helper/helper.go`).
  - Declare package: `package helper`.
- **Exporting**:
  - Capitalize names to export: `func ValidateInput(...) {...}`.
- **Importing**:
  ```go
  import (
      "booking-app/helper"  // Custom package
      "fmt"                 // Standard library
  )
  helper.ValidateInput(...)
  ```

##### **Variable Scopes**
- **Local**: Inside a function/block.
- **Package Level**: Outside functions (accessible within package).
- **Global**: Exported (capitalized) package-level variables.

---

#### **8. Concurrency (Goroutines)**
- **Goroutines**: Lightweight threads (managed by Go runtime).
  ```go
  go sendTicket(userTickets, firstName, email)  // Runs in background
  ```
- **Sync with WaitGroups**:
  ```go
  var wg sync.WaitGroup

  func sendTicket(...) {
      defer wg.Done()  // Decrements counter when done
      // Logic (e.g., time.Sleep(10 * time.Second))
  }

  func main() {
      wg.Add(1)        // Add 1 goroutine to wait for
      go sendTicket(...)
      wg.Wait()        // Blocks until all goroutines finish
  }
  ```
- **Benefits**: Efficient handling of I/O-bound tasks (e.g., sending emails) without blocking main thread.

---

#### **9. Key Takeaways**
- **Concurrency**: Simplified with `go` keyword and channels (not covered here).
- **Error Prevention**: Strong typing and compile-time checks.
- **Efficiency**: Fast compilation, low resource usage.
- **Use Cases**: Cloud services, CLI tools, high-performance backends.

---

#### **10. Resources**
- **Go Documentation**: [golang.org/doc](https://golang.org/doc)
- **Course Code**: [GitHub Repository](https://github.com/tech-with-nana/go-booking-app) (link in video description)
- **Advanced Go Course**: [techworldwithnana.com](https://techworldwithnana.com) (for web apps, databases, etc.)

> **Next Steps**: Practice building CLI/web apps, explore channels for advanced concurrency.
