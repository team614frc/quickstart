# quickstart

This guide helps new software team members get up to speed and serves as a reference for all things software. This is a living document—if you find something useful, solve a problem, or get an answer to a question, open a PR to add it. Your contributions will help future members, including yourself.

## Requirements

- [WPILib](https://docs.wpilib.org/en/stable/docs/zero-to-robot/step-2/index.html)
- [Git](https://git-scm.com/install/windows)
- [Pathplanner](https://pathplanner.dev/home.html)
- [Java](https://www.w3schools.com/java/)

## Git Conventions

- [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/)

  Use commit prefixes to identify the type of change:

  ```
  feat: add intake subsystem
  chore: refactor intake
  fix: slow intake speed
  ```

- [Conventional Branch](https://conventional-branch.github.io/)

  Prefix branches with your name so teammates know who to contact:

  ```
  <your-name>/<branch-name>
  minhd-vu/intake-subsystem
  ```

- Pull requests are squash-merged into `main`. If you have merge conflicts, merge `main` into your branch:
  ```
  git checkout minhd-vu/intake-subsystem
  git merge main
  ```

## References

- [Phoenix 6](https://v6.docs.ctr-electronics.com/en/stable/)
- [winget](https://learn.microsoft.com/en-us/windows/package-manager/winget/)
- [GitHub Actions](https://docs.github.com/en/actions/get-started/quickstart)

## Team Laptops

The team provides laptops (labeled `01` through `05`) with the required software that cannot be installed on school-provided machines. If you have a personal laptop, please use it so others without one can access the team laptops. If you use a team laptop, stick with the same one to avoid reinitializing git credentials.

The laptops have WSL installed. All programming should be done through WSL, and all repos should be cloned into the WSL home directory. Keeping repositories in one place prevents duplicates and helps everyone find things. A similar setup is recommended for personal computers to stay organized.

The laptops don't have assigned chargers—any 65W USB-C charger will work. Always return laptops and chargers to the central location to keep things organized. Failure to do so may restrict your access to team equipment.

### Laptop Setup

WSL is installed so software team members can get comfortable with Linux. Since the roboRIO runs a Linux-based system, familiarity with Linux helps when you need to SSH into the RIO for debugging.

```bash
wsl --install -d Ubuntu
```

```bash
cd # go to the WSL home directory
git clone https://github.com/team614frc/Team-614-Kraken-Roomba # git is pre-installed in WSL
sudo apt install openjdk-17-jdk -y # install Java
```

When opening the repository in WPILib VS Code, you'll be prompted to reopen it in WSL. After doing so, go to the Extensions tab and install the WPILib extension for WSL.
There are also other extentions that are useful with WPILIB VS Code that are reccomended to be installed. They are:
- Extension Pack for Java
- GitHub Pull Requests

### Driver Station Laptop

The driver station laptop is reserved for driving only—do not use it for development. It should always stay on the driver station. Keep it updated with the FRC Game Tools for the current season.
