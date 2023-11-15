
# Gray-Scott Simulation Project

## Introduction
This project implements a simulation of the Gray-Scott reaction-diffusion system. It is designed to demonstrate the use of various software engineering practices including unit testing, continuous integration, and proper documentation.

## Getting Started

### Prerequisites
Before building the project, ensure you have the following installed:
- C++ compiler (e.g., GCC, Clang, MSVC)
- CMake (version 3.x or higher)
- Visual Studio (for Windows users)

### Cloning the Repository
To clone the repository and its submodules, run the following command:

git clone --recurse-submodules https://github.com/mxiong11/gray-scott-sim.git

**_Git Commands_**

Use the Git command to clone the GitHub repository to your local machine. 

`git clone <repositoryURL>`

Create a new branch, add all changes to that branch, commit the changes, and finally push the branch to the remote repository for sharing and collaboration with others.
```
git checkout -b <newBranchName>
git add .
git commit -m "Descriptive commit message"
git push origin <yourBranchName>
```

### Building the Project
To build the project, follow these steps:

#### On Windows (using Visual Studio):
1. Open Visual Studio.
2. Select `File -> Open -> CMake...` and navigate to the cloned repository.
3. Visual Studio will automatically configure the project with CMake.
4. To build the project, right-click on the CMakeLists.txt in the Solution Explorer and select 'Build'.

#### On Linux/MacOS (using terminal):
1. Navigate to the project directory.
2. Create a build directory and navigate into it:
mkdir build && cd build
3. Run CMake and build the project:
cmake .. && make


### Running the Simulation
After building, you can run the simulation program:
- On Windows, the executable will be in the `build/Debug` or `build/Release` directory.
- On Linux/MacOS, the executable will be in the `build` directory.

### Running Tests
To run the unit tests, follow these steps:
- On Windows, tests can be run directly from Visual Studio using the Test Explorer.
- On Linux/MacOS, after building, execute the test binary in the `build` directory.

**_TEST 0.3_** 

In accordance with the requirements of Test (0.3) in the coursework, firstly, all elements of 'u' and 'v' are initialised to 0 at the start of the test, and 'F' and 'k' are set to 0 to check that the simulation produces a mathematically correct answer. 

After that, 'ASSERT_EQ' is used to assert that all elements of the u and v matrices are equal to zero. If the simulation system is correct, then after a sufficient number of iterations with zero initial conditions, all elements in 'u' and 'v' should still be zero.

Finally, 'ASSERT_EQ' is used to assert that proportionAboveThreshold is equal to zero, further validating whether the system correctly simulates under zero initial conditions.

