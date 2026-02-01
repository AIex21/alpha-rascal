# Static Extractor

## Configuration

Create a `config.json` file in the project root directory with the following fields:
* `inputFolderAbsolutePath`: Enter the absolute path of the C/C++ project you wish to parse.
* `externalLibRoot`: Enter the absolute paths to the external dependencies. These must be separated by a semicolon (;).

### Example Configuration:
```json
{
    "inputFolderAbsolutePath": "C:\\Users\\...\\Project",
    "externalLibRoot": "C:\\Program Files\\Microsoft Visual Studio\\2022\\Community\\VC\\Tools\\MSVC\\14.44.35207\\include;C:\\Program Files (x86)\\Windows Kits\\10\\Include\\10.0.26100.0"
}   
```

## Execution Steps
1. Open Parser: Navigate to and open `src/main/rascal/Parser.rsc`.
2. Initialize Terminal: Click the "Import in new Rascal terminal" option located at the top of the editor window.
3. Run Extraction: Once the terminal has loaded and the rascal> prompt appears, run the following command (replacing NameOfTheProject with your desired output name): `main(moduleName="NameOfTheProject");`

## Output
The extractor processes the source code and generates architectural models in the `/models/composed` directory.