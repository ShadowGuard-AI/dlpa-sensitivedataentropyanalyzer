![Banner](banner.png)

# dlpa-SensitiveDataEntropyAnalyzer
Calculates the entropy of files and directories to identify potential sensitive data based on high randomness and structured formats, bypassing reliance on predefined keywords or patterns. Flags files exceeding an entropy threshold for further investigation. - Focused on Tools for assessing the effectiveness of data leakage prevention (DLP) measures. This involves generating realistic but fake sensitive data (e.g., credit card numbers, names, addresses) using Faker and then testing how well DLP systems detect and prevent the exfiltration of this data. Focus on validating DLP rules rather than building a full DLP system.

Note: generate mode (-g) needs no path argument. An analysis run without a path is an error.

## Install
`git clone https://github.com/ShadowGuard-AI/dlpa-sensitivedataentropyanalyzer`

## Usage
`python3 main.py [path] [options]`

## Parameters
- `path`: Path to the file or directory to analyze. Not required in generate mode (`-g`).
- `-h`: Show help message and exit
- `-t`, `--threshold`: Entropy threshold. Files exceeding this value will be flagged. Default: 4.5
- `-r`, `--recursive`: Recursively analyze directories.
- `-v`, `--verbose`: Enable verbose output (debug logging).
- `-g`, `--generate`: Generate fake sensitive data for DLP testing.
- `-n`, `--num-files`: Number of files to generate when using -g. Default: 10
- `-d`, `--output-dir`: Output directory for generated files. Default: fake_data

## License
This project is released under the MIT License. See the [LICENSE](LICENSE) file for details.
