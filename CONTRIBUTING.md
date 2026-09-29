# Contribution Guidelines

Thank you for your interest in contributing to the **International Physics Simulation Society (IPhySims)**! This document will guide you through the process of contributing a physics simulation to our curated repository.

---

## Ways to Contribute

There are many ways to contribute to IPhySims:

1. **Submit a Simulation** — Contribute a physics simulation for peer review
2. **Review Submissions** — Help evaluate submitted simulations as a peer reviewer
3. **Improve Documentation** — Enhance documentation for existing simulations
4. **Report Issues** — Report bugs or suggest improvements for curated simulations
5. **Spread the Word** — Share IPhySims with your network
6. **Contribute to Infrastructure** — Help improve our website, tools, and processes

---

## Submitting a Simulation

### Before You Start

Before submitting, ensure your simulation meets our basic requirements:

- [ ] **Scientifically correct**: The physics is accurate and well-documented
- [ ] **Runnable**: The code executes without errors
- [ ] **Open-source**: Released under an approved license (GPL-3.0, MIT, Apache 2.0, BSD)
- [ ] **Documented**: Includes a README with description, physics background, and usage instructions
- [ ] **Dependencies listed**: All dependencies are documented with versions
- [ ] **Example output**: Includes expected output for a sample input

### Submission Process

#### Step 1: Prepare Your Materials

Create a repository (or prepare a zip file) containing:

```
your-simulation/
├── README.md              # Description, physics, usage instructions
├── LICENSE                # Open-source license file
├── src/                   # Source code
│   └── ...
├── docs/                  # Additional documentation (optional)
│   └── ...
├── examples/              # Example inputs and outputs
│   └── ...
├── tests/                 # Test cases (if applicable)
│   └── ...
├── requirements.txt       # Dependencies (or environment.yml, etc.)
└── .iphysim/               # IPhySims metadata
    └── metadata.json      # Simulation metadata (see below)
```

#### Step 2: Create Metadata File

Create a `.iphysim/metadata.json` file:

```json
{
  "title": "Your Simulation Title",
  "authors": [
    {
      "name": "Author Name",
      "affiliation": "University/Organization",
      "orcid": "0000-0000-0000-0000"
    }
  ],
  "description": "Brief description of the simulation",
  "physics_domain": "Classical Mechanics",
  "subdomain": "Oscillations and Waves",
  "educational_level": "Undergraduate",
  "programming_language": "Python",
  "dependencies": ["numpy", "matplotlib", "scipy"],
  "license": "GPL-3.0",
  "version": "1.0.0",
  "keywords": ["oscillator", "spring", "harmonic", "damped"],
  "validated_against": "Analytical solution for damped harmonic oscillator"
}
```

**Valid physics domains:**
- Classical Mechanics
- Electromagnetism
- Quantum Mechanics
- Thermodynamics and Statistical Mechanics
- Optics and Photonics
- Nuclear and Particle Physics
- Astrophysics and Cosmology
- Condensed Matter Physics
- Fluid Dynamics
- Computational Physics Methods
- Other (please specify)

**Valid educational levels:**
- Secondary School
- Undergraduate
- Graduate
- Research
- General Audience

#### Step 3: Submit

Submit your simulation by opening a new issue on our GitHub repository using the **Submission Template**:

1. Go to [https://github.com/IPhySims/submissions/issues](https://github.com/IPhySims/submissions/issues) *(planned)*
2. Click "New Issue"
3. Select the "Simulation Submission" template
4. Fill in all required fields
5. Provide a link to your simulation repository or upload a zip file

#### Step 4: Respond to Reviews

After submission:
- Your simulation will be assigned 2 peer reviewers
- Reviewers will evaluate on 4 criteria (see [REVIEW_STANDARDS.md](./REVIEW_STANDARDS.md))
- You will receive detailed feedback within 14–21 days
- Address all reviewer comments and submit a revised version
- The Editorial Board will make a final decision

### Tips for a Successful Submission

1. **Validate your results**: Compare with analytical solutions or published data
2. **Write clear documentation**: Assume the reviewer is a physicist but not necessarily an expert in your specific area
3. **Make it easy to run**: Provide a simple script or command to execute the simulation
4. **Include visualizations**: Good plots or animations help demonstrate the physics
5. **Handle errors gracefully**: Provide useful error messages for common mistakes
6. **Test on multiple platforms**: If possible, verify your simulation works on Windows, macOS, and Linux
7. **Use version control**: Host your code on GitHub/GitLab with a clear commit history

---

## Becoming a Reviewer

We welcome volunteers to join our reviewer team. Requirements:

- At least a Master's degree in physics or a related field
- Experience with computational physics or simulation development
- Familiarity with at least one programming language commonly used in physics
- Commitment to completing reviews within the assigned timeframe

### How to Apply

1. First, submit at least one simulation that has been accepted into the IPhySims repository
2. Send an email to **reviewers@iphysim.org** *(planned)* with:
   - Your name and affiliation
   - Your areas of physics expertise
   - Your programming languages and tools
   - A brief statement of why you want to be a reviewer
3. Complete our reviewer training module (provided upon acceptance)

---

## Other Ways to Contribute

### Improving Documentation

Found a typo or unclear explanation in a curated simulation's documentation? Pull requests are welcome!

1. Fork the simulation repository
2. Make your improvements
3. Submit a pull request

### Reporting Issues

If you find a bug or have a suggestion for a curated simulation:

1. Check existing issues to avoid duplicates
2. Open a new issue with a clear description
3. Include steps to reproduce (for bugs)
4. Tag the issue appropriately

### Contributing to IPhySims Infrastructure

We welcome contributions to:
- The IPhySims website
- Review management tools
- Documentation generators
- Automated testing infrastructure

See our [development repository](https://github.com/IPhySims/infrastructure) *(planned)* for details.

---

## Communication Channels

- **GitHub Discussions**: [https://github.com/IPhySims/community/discussions](https://github.com/IPhySims/community/discussions) *(planned)*
- **Discord**: [Invite link](https://discord.gg/iphysim) *(planned)*
- **Email**: contact@iphysim.org *(planned)*
- **Twitter/X**: [@IPhySims](https://twitter.com/IPhySims) *(planned)*

---

## Questions?

If you have questions about contributing, please:
1. Check our [FAQ](./FAQ.md) *(planned)*
2. Search existing GitHub issues and discussions
3. Ask on our Discord or GitHub Discussions
4. Email us at contact@iphysim.org

---

Thank you for helping us build the world's most trusted collection of physics simulations!

---

*These guidelines are maintained by the IPhySims Governing Board. Suggestions for improvement are welcome via GitHub Issues.*
