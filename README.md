# Singleton Pattern

<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-singleton">About The Singleton</a>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
  </ol>
</details>

<!-- ABOUT THE SINGLETON -->
## About The Singleton

The singleton pattern is a way to ensure a class has only a single globally accessible instance available at all times. Behaving much like a regular static class but with some advantages. This is very useful for making global manager type classes that hold global variables and functions that many other classes need to access.

<!-- GETTING STARTED -->
## Getting Started

This is an example of how you may give instructions on setting up your project locally.
To get a local copy up and running follow these simple example steps.

### Installation

1. Clone the repo
   ```sh
   git clone https://github.com/bmoglu/singleton.git
   ```
2. Import package to your project  
  
<!-- USAGE EXAMPLES -->
## Usage

To make any class a singleton, simply inherit from the Singleton base class instead of MonoBehaviour, like so:
```csharp
public class MySingleton : Singleton<MySingleton>
{
    // Then add whatever code to the class you need as you normally would.
    public string MyAwesomeString = "Hello world!";
}
```
Now you can access all public fields, properties and methods from the class anywhere using **ClassName.Instance**: 
```csharp
public class MyAwesomeClass : MonoBehaviour
{
    private void OnEnable()
    {
        Debug.Log(MySingleton.Instance.MyAwesomeString);
    }
}
```

<!-- LICENSE -->
## License

Distributed under the MIT License. See `LICENSE` for more information.
