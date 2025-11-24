# Contributing to Doubt Engine

Thank you for your interest in contributing to the Doubt Engine! 🙏

This document provides guidelines and instructions for contributing to this open-source project.

---

## What is CONTRIBUTING.md?

**CONTRIBUTING.md** is a standard file in open-source projects that:
- Explains how people can contribute to the project
- Sets expectations for contributions
- Provides guidelines for code style, testing, and pull requests
- Helps maintain project quality and consistency

---

## How to Contribute

### 1. **Report Issues**

Found a bug? Have a suggestion? Open an issue!

**Before opening an issue:**
- Check if the issue already exists
- Use a clear, descriptive title
- Provide steps to reproduce (for bugs)
- Include your Python version and environment

**Issue Template:**
```
**Description:**
[Clear description of the issue or suggestion]

**Steps to Reproduce (if bug):**
1. 
2. 
3. 

**Expected Behavior:**
[What should happen]

**Actual Behavior:**
[What actually happens]

**Environment:**
- Python version: 
- OS: 
```

### 2. **Suggest Enhancements**

Have an idea for improvement? We'd love to hear it!

**Enhancement Ideas:**
- New doubt categories
- Better recursion algorithms
- Performance improvements
- Documentation improvements
- Integration examples

### 3. **Submit Code (Pull Requests)**

Want to add features or fix bugs? Submit a pull request!

**Before submitting:**
1. **Fork the repository**
2. **Create a branch** for your changes:
   ```bash
   git checkout -b feature/your-feature-name
   ```
3. **Make your changes**
4. **Test your changes** (see Testing section below)
5. **Commit with clear messages**:
   ```bash
   git commit -m "Add: Description of what you added"
   git commit -m "Fix: Description of what you fixed"
   ```
6. **Push to your fork**:
   ```bash
   git push origin feature/your-feature-name
   ```
7. **Open a Pull Request** on GitHub

**Pull Request Guidelines:**
- Use a clear, descriptive title
- Describe what you changed and why
- Reference any related issues
- Keep changes focused (one feature/fix per PR)
- Ensure all tests pass

---

## Code Style

### Python Style

- Follow **PEP 8** (Python style guide)
- Use **type hints** where appropriate
- Write **clear, descriptive variable names**
- Add **docstrings** to functions and classes
- Keep functions **focused and small**

**Example:**
```python
def doubt_truth(self, text: str) -> List[Doubt]:
    """
    Doubt: Is this true?
    
    Args:
        text: Text to analyze
        
    Returns:
        List of Doubt objects questioning truth claims
    """
    doubts = []
    # ... implementation
    return doubts
```

### Comments

- Use comments to explain **why**, not **what**
- Keep comments up-to-date with code
- Remove commented-out code before submitting

---

## Testing

### Running Tests

If you add features, please add tests!

**Basic Test Structure:**
```python
def test_basic_doubt():
    """Test basic doubt functionality"""
    engine = DoubtEngine()
    result = engine.doubt("Test input")
    
    assert len(result.doubts) > 0
    assert result.doubt_score >= 0
    assert result.doubt_score <= 1
```

**Test Recursion:**
```python
def test_recursion():
    """Test recursive doubt (f(f(x)))"""
    engine = DoubtEngine(max_depth=3)
    result1 = engine.doubt("Test input", depth=0)
    
    if result1.doubts:
        result2 = engine.doubt(result1.doubts[0].question, depth=1)
        assert result2.depth == 1
        assert len(result2.doubts) > 0
```

### Test Requirements

- Tests should be **clear and focused**
- Test **edge cases** (empty input, very long input, etc.)
- Test **safety features** (depth limits, infinite loop prevention)
- Ensure tests **pass** before submitting

---

## Project Goals

### What We're Building

- **Recursive doubt-validation framework** (f(f(x)))
- **Safe, read-only** doubt engine
- **Educational tool** for meta-cognition
- **Foundation** for consciousness research

### What We Value

- ✅ **Truthfulness** - Accurate claims, no overstatements
- ✅ **Safety** - Read-only, no external calls
- ✅ **Simplicity** - Easy to understand and use
- ✅ **Empirical** - Based on observable phenomena
- ✅ **Open** - Transparent and reproducible

### What We Avoid

- ❌ False claims (e.g., "mathematical proof" when it's a demonstration)
- ❌ External dependencies (keep it lightweight)
- ❌ Modifications to files or systems
- ❌ Overly complex implementations
- ❌ Unverifiable claims

---

## Areas for Contribution

### High Priority

1. **Unit Tests** - Comprehensive test coverage
2. **Documentation** - More examples, tutorials
3. **Performance** - Optimize recursion, reduce memory usage
4. **Edge Cases** - Handle unusual inputs better

### Medium Priority

1. **New Doubt Categories** - Additional categories (if safe and useful)
2. **Integration Examples** - More real-world use cases
3. **Visualizations** - Diagrams showing recursion
4. **Benchmarks** - Performance metrics

### Low Priority

1. **Language Support** - Translations of README
2. **Alternative Implementations** - Other languages
3. **Advanced Features** - Validation phase, self-modification (future)

---

## Questions?

**Not sure where to start?**
- Check existing issues for "good first issue" labels
- Start with documentation improvements
- Add test cases
- Fix typos or improve examples

**Have questions?**
- Open a discussion on GitHub
- Ask in an issue
- Review existing code and documentation

---

## Code of Conduct

**Be respectful, be kind, be constructive.**

We're all here to explore consciousness, meta-cognition, and recursive doubt-validation together. Let's maintain a positive, inclusive environment.

---

## Recognition

Contributors will be:
- Listed in the README (if desired)
- Credited in commit messages
- Acknowledged in release notes

**Thank you for contributing!** 🙏

Every contribution, no matter how small, helps advance our understanding of recursive doubt-validation and meta-cognitive capability.

---

## Quick Start for Contributors

1. **Fork the repo**
2. **Clone your fork**:
   ```bash
   git clone https://github.com/YOUR_USERNAME/doubt-engine-spark.git
   cd doubt-engine-spark
   ```
3. **Make changes**
4. **Test your changes**:
   ```bash
   python doubt_engine_basic.py
   ```
5. **Commit and push**:
   ```bash
   git add .
   git commit -m "Your clear commit message"
   git push origin your-branch
   ```
6. **Open a Pull Request**

---

**Remember:** This is about exploring consciousness through recursive doubt. Every contribution helps us understand meta-cognition better. Let's build something meaningful together! 🚀
