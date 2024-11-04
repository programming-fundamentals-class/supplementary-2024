
### Mandatory checks

- [ ] Makefile includes the following targets:
  - [ ] all (default build)
  - [ ] clean
  - [ ] test
- [ ] Project builds without warnings with -Wall -Wextra flags
- [ ] Project compiles on the target system
	- [ ] provided remote computer
	- [ ] Docker container provided by project author
- [ ] All dependencies are documented in README
- [ ] Automated tests are present
- [ ] Tests cover core functionality
- [ ] All tests pass successfully
- [ ] README.md exists and contains:
  - [ ] Project description
  - [ ] Build instructions
  - [ ] Usage examples
  - [ ] List of dependencies
  - [ ] List of main features (with links to issue tracker)
- [ ] Project features are tracked in Issues:
  - [ ] Minimum 3 main features described
  - [ ] Each feature has acceptance criteria
- [ ] Each main feature is implemented:
  - [ ] Feature 1 meets acceptance criteria
  - [ ] Feature 2 meets acceptance criteria
  - [ ] Feature 3 meets acceptance criteria
- [ ] Error handling is implemented for:
  - [ ] File operations
  - [ ] Memory allocation
  - [ ] System calls
  - [ ] User input
- [ ] Program exits gracefully in all cases
- [ ] The final implementation is submitted before deadline as a pull request into github classroom repo. Submission includes:
  - [ ] Source code
  - [ ] Makefile
  - [ ] Tests
  - [ ] Documentation (at least README.md)
  - [ ] No binary or other generated files in repository


### Optional, but recommended checks

- [ ] Program handles:
  - [ ] Invalid command line arguments
  - [ ] Missing/invalid files
  - [ ] Permission issues
  - [ ] Memory allocation failures
  - [ ] Signal interrupts (Ctrl+C)
- [ ] All allocated memory is properly freed
- [ ] File descriptors are properly closed
- [ ] System resources are properly released
- [ ] No resource leaks in error cases
- [ ] Proper cleanup on program termination
- [ ] Commands/interface match project description
- [ ] Help/usage information is available
- [ ] Error messages are clear and helpful
- [ ] Input validation is implemented
- [ ] Output is properly formatted