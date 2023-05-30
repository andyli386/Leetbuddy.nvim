# LeetBuddy.nvim

LeetBuddy.nvim is a powerful Neovim plugin that provides a seamless integration with Leetcode.com, allowing you to solve coding challenges directly within Neovim. Increase your productivity using this plugin. 🚀

## Demo

https://github.com/Dhanus3133/Leetbuddy.nvim/assets/43700516/411e7c02-c888-41ad-9e01-99427cb05de5

## Requirements

- Neovim (v0.5 or higher)
- plenary.nvim

## Installation

Use your favorite plugin manager to install LeetBuddy.nvim. Here's an example using `Lazy`:

```lua
return {
  "Dhanus3133/LeetBuddy.nvim",
  dependencies = {
    "nvim-lua/plenary.nvim",
  },
  config = function()
    require("leetbuddy").setup({})
  end,
  keys = {
    { "<leader>lq", "<cmd>LBQuestions<cr>", desc = "List Questions" },
    { "<leader>ll", "<cmd>LBQuestion<cr>", desc = "View Question" },
    { "<leader>lr", "<cmd>LBReset<cr>", desc = "Reset Code" },
    { "<leader>lt", "<cmd>LBTest<cr>", desc = "Run Code" },
    { "<leader>ls", "<cmd>LBSubmit<cr>", desc = "Submit Code" },
  },
}

```

## Commands

LeetBuddy.nvim provides the following commands:

- `LBQuestions`: Lists all Leetcode problems with submission status and difficulty level.
- `LBQuestion`: Displays the question in a popup window.
- `LBReset`: Resets the code of the current question to the default template.
- `LBTest`: Runs the test cases for the current question. Multiple test cases can be added.
- `LBSubmit`: Submits the code for the current question.

## Custom Configuration

LeetBuddy.nvim allows you to customize certain aspects of its behavior. You can modify the following configuration options in your Neovim configuration file to suit your preferences:

```lua
require('leetbuddy').setup({
    language = "py",
})
```

<details>
<summary>Available language options for the <code>language</code> configuration are:</summary>

- `cpp`: C++
- `java`: Java
- `py`: Python 3
- `c`: C
- `cs`: C#
- `js`: JavaScript
- `rb`: Ruby
- `swift`: Swift
- `go`: Go
- `scala`: Scala
- `kt`: Kotlin
- `rs`: Rust
- `php`: PHP
- `ts`: TypeScript
- `rkt`: Racket
- `erl`: Erlang
- `ex`: Elixir
- `dart`: Dart
</details>

## Contributing

Contributions are welcome! If you have any bug reports, feature requests, or suggestions, please open an issue or submit a pull request. For major changes, please discuss them in the issue tracker before making any modifications.

## License

This plugin is available under the MIT License. Feel free to use and modify it according to your needs.

---