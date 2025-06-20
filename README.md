# PHP Spreadsheet 📊

![PHP Spreadsheet](https://img.shields.io/badge/PHP_Spreadsheet-v1.0.0-brightgreen) ![GitHub Releases](https://img.shields.io/badge/Releases-latest-blue) ![GitHub Issues](https://img.shields.io/badge/Issues-welcome-orange)

Welcome to the **PHP Spreadsheet** repository! This library allows you to read and write spreadsheet files using pure PHP. Whether you're working with Excel, Gnumeric, or LibreOffice files, this library has you covered.

## Table of Contents

1. [Introduction](#introduction)
2. [Features](#features)
3. [Installation](#installation)
4. [Usage](#usage)
5. [Supported Formats](#supported-formats)
6. [Contributing](#contributing)
7. [License](#license)
8. [Contact](#contact)
9. [Releases](#releases)

## Introduction

The **PHP Spreadsheet** library simplifies the task of handling spreadsheet files. You can create, read, and modify files in various formats with ease. This library is especially useful for developers who need to work with data in a tabular format.

To get started, you can check out the [Releases section](https://github.com/namekaohehe/PHP-Spreed-Sheet/releases) for the latest version of the library.

## Features

- **Easy to Use**: The library offers a straightforward API.
- **Multiple Formats**: Supports various spreadsheet formats including XLSX, ODS, and CSV.
- **Lightweight**: No external dependencies required.
- **Active Development**: Regular updates and improvements.

## Installation

You can install the PHP Spreadsheet library using Composer. Run the following command in your terminal:

```bash
composer require namekaohehe/php-spreadsheet
```

Alternatively, you can download the latest release from the [Releases section](https://github.com/namekaohehe/PHP-Spreed-Sheet/releases). After downloading, extract the files and include the library in your project.

## Usage

Here’s a quick example of how to use the PHP Spreadsheet library:

### Creating a New Spreadsheet

```php
<?php
require 'vendor/autoload.php';

use PhpOffice\PhpSpreadsheet\Spreadsheet;
use PhpOffice\PhpSpreadsheet\Writer\Xlsx;

$spreadsheet = new Spreadsheet();
$sheet = $spreadsheet->getActiveSheet();

$sheet->setCellValue('A1', 'Hello World !');

$writer = new Xlsx($spreadsheet);
$writer->save('hello_world.xlsx');
?>
```

### Reading an Existing Spreadsheet

```php
<?php
require 'vendor/autoload.php';

use PhpOffice\PhpSpreadsheet\IOFactory;

$spreadsheet = IOFactory::load('hello_world.xlsx');
$sheetData = $spreadsheet->getActiveSheet()->toArray(null, true, true, true);

print_r($sheetData);
?>
```

This example demonstrates how to create a new spreadsheet and read an existing one. You can easily expand this to suit your needs.

## Supported Formats

The PHP Spreadsheet library supports the following formats:

- **XLSX**: Microsoft Excel Open XML Spreadsheet
- **XLS**: Microsoft Excel 97-2003 Spreadsheet
- **ODS**: Open Document Spreadsheet
- **CSV**: Comma-Separated Values
- **SYLK**: Symbolic Link Format

You can read and write files in these formats seamlessly.

## Contributing

We welcome contributions to the PHP Spreadsheet library. If you want to help, please follow these steps:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature/YourFeature`).
3. Make your changes and commit them (`git commit -m 'Add some feature'`).
4. Push to the branch (`git push origin feature/YourFeature`).
5. Open a Pull Request.

Please ensure your code adheres to the existing coding standards and includes tests where applicable.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

## Contact

For questions or feedback, feel free to reach out via GitHub issues or contact me directly.

## Releases

You can find the latest releases and download the library from the [Releases section](https://github.com/namekaohehe/PHP-Spreed-Sheet/releases). Make sure to check this page regularly for updates and new features.

## Conclusion

The PHP Spreadsheet library is a powerful tool for anyone working with spreadsheet data in PHP. Its ease of use and support for multiple formats make it a valuable addition to your development toolkit. We hope you find it helpful in your projects!

Feel free to explore the library, and don’t hesitate to contribute or reach out with any questions. Happy coding!