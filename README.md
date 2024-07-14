# Efficient Optimal Decision Tree Inference via SAT Techniques

-prepared by Group 12

# Background Info:

This is a re-run with refinements on paper of Avellaneda, F. (2020). Efficient Inference of Optimal Decision Trees.
Proceedings of the AAAI Conference on Artificial Intelligence, 34(04), 3195-3202.

The code of the “Efficient Inference of Optimal Decision Trees” project is written in C++. The author claims that the project has been tested with C++ compilers on the Linux and Mac OS. We complete the video demo on macOS Monterey 12.6. For running Linun on windows machine, please install miscrosoft’s WSL.

# Video Code Demo is in the link below:

https://youtu.be/Zz02VwFzjV4

# Environment Setting:

Install the packages below before compiling the C++ file:
-- cmake
-- minisat
-- xdot
-- libzip
-- boost
These packages should be installed through terminal. If you have meet any installation failure, please try Homebrew to install the failed packages.

# Code Files:

“main.cpp” is the file to compile when we run the project. All the other files are C++ classes.
When compiling the file, I recommend adopting CLI17 instead of CLI11. There is a line of code in Tabular_data.h need to verify as ‘random-shuffle’ is not supported by CLI17.
Code for CLI11 version:
std::random_shuffle(all.begin(),all.end());

Code for CLI17 version:
std::random_device rd;
std::mt19937 g(rd());
std::shuffle(all.begin(),all.end(),g);

# Command Lines to compile C++ code:

```
g++ -std=c++17 -o <code folder> main.cpp -lminisat
```

# Command Lines to show help info of the project:

```
./<code folder> --help
```

# Command Lines to infer DT_depth Tree:

```
./<code folder> -d <data folder>/<file name> infer
```

# Command Lines to infer DT_size Tree:

```
./<code folder> <data folder>/<file name> infer
```

# Command Lines to infer DT_size Tree and show in terminal window:

```
./<code folder> -x <data folder>/<file name> infer
```
