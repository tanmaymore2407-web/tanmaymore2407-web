# 👋 Hi, I'm Tanmay Sanjay More

### Your tagline here — e.g. "Aspiring developer | Polytechnic student | Python learner"

---

## About Me
I,m from sangamner,I have Lived for my education in Pune previously,I like reading ,I like gamming 


---

## Skills

| Skill        | Level        |
|--------------|--------------|
| Python       | Beginner     |
| Git & GitHub | Beginner     |
| Markdown     | Beginner     |
| c            |    Beginner   |

---

## Current Projects

- **Grade Buddy** — a command-line app that tracks test scores and generates a report card.
- **GitHub Profile** — this very page, my first Markdown website.
- Add more if you have them...

---

## Goals
Get into a good engineering college 



## Find Me

[Email](tanmaymore2407@gmail.com)
[Email](tanmaymore1705@gmail.com)
[Instagram](tanmay_official18)




[![](https://komarev.com/ghpvc/?username=tanmaymore2407-web&icon=0&color=0)](https://visitcount.itsvg.in)


<div align="center" id="top">
  <img src="https://profile-readme-generator.com/assets/app.png" width="900" alt="Profile Readme Generator" />

  <a href="https://profile-readme-generator.com">Demo</a>
</div>

<div align="center">
  <h1>Profile Readme Generator</h1>
  <h3>The best profile readme generator you will find!</h3>
</div>

<p align="center">
  <a href="https://github.com/maurodesouza/profile-readme-generator/fork" target="_blank">
    <img src="https://img.shields.io/github/forks/maurodesouza/profile-readme-generator?" alt="Badge showing the total of project forks"/>
  </a>

  <a href="https://github.com/maurodesouza/profile-readme-generator/stargazers" target="_blank">
    <img src="https://img.shields.io/github/stars/maurodesouza/profile-readme-generator?" alt="Badge showing the total of project stars"/>
  </a>

  <a href="https://github.com/maurodesouza/profile-readme-generator/commits/main" target="_blank">


# 💻 Tech Stack:
![C](https://img.shields.io/badge/c-%2300599C.svg?style=for-the-badge&logo=c&logoColor=white) ![C++](https://img.shields.io/badge/c++-%2300599C.svg?style=for-the-badge&logo=c%2B%2B&logoColor=white) ![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white) ![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54) ![C#](https://img.shields.io/badge/c%23-%23239120.svg?style=for-the-badge&logo=csharp&logoColor=white
# 📊 GitHub Stats:
![](https://github-readme-stats.shion.dev/api?username=tanmaymore2407-web&theme=dark&hide_border=true&include_all_commits=true&count_private=false)<br/>
![](https://streak-stats.demolab.com/?user=tanmaymore2407-web&theme=dark&hide_border=true)<br/>
![](https://github-readme-stats.shion.dev/api/top-langs/?username=tanmaymore2407-web&theme=dark&hide_border=true&include_all_commits=true&count_private=false&layout=compact)


**import matplotlib.pyplot as plt

# 1. Sample data from Grade Buddy
tests = ['Quiz 1', 'Test 1', 'Quiz 2', 'Midterm', 'Test 3', 'Final']
scores = [78, 85, 82, 90, 88, 94]

# 2. Design and styling configuration
plt.figure(figsize=(8, 4.5))
plt.style.use('seaborn-v0_8-whitegrid' if 'seaborn-v0_8-whitegrid' in plt.style.available else 'default')

# Plot line and data points
plt.plot(tests, scores, marker='o', color='#2ea44f', linewidth=2.5, markersize=8, label='Your Progress')

# Add data labels above each point
for i, score in enumerate(scores):
    plt.text(i, score + 1.5, f'{score}%', ha='center', fontsize=9, fontweight='bold', color='#24292e')

# 3. Titles and axis labels
plt.title('Academic Performance Trend', fontsize=14, fontweight='bold', pad=15, color='#24292e')
plt.xlabel('Assessments', fontsize=11, labelpad=10)
plt.ylabel('Scores (%)', fontsize=11, labelpad=10)
plt.ylim(60, 105)

# 4. Save the graph for GitHub README
plt.tight_layout()
plt.savefig('performance_graph.png', dpi=300, transparent=True)
print("Graph saved successfully as 'performance_graph.png'!")
**




import json
import os
import matplotlib.pyplot as plt

# File to persist student grade data
DATA_FILE = "grades_data.json"

def load_data():
    """Load grades from local JSON storage or return defaults if empty."""
    if os.path.exists(DATA_FILE):
        with open(DATA_FILE, "r") as f:
            return json.load(f)
    return {"tests": ["Quiz 1", "Test 1", "Quiz 2", "Midterm"], "scores":}

def save_data(data):
    """Save updated grades back to JSON storage."""
    with open(DATA_FILE, "w") as f:
        json.dump(data, f, indent=4)

def generate_performance_graph(data):
    """Generate and save the visual trend chart using current data."""
    if not data["tests"]:
        print("❌ No data available to generate a graph.")
        return

    plt.figure(figsize=(8, 4.5))
    plt.style.use('seaborn-v0_8-whitegrid' if 'seaborn-v0_8-whitegrid' in plt.style.available else 'default')

    # Draw trendlines using dataset variables
    plt.plot(data["tests"], data["scores"], marker='o', color='#2ea44f', linewidth=2.5, markersize=8)

    # Annotate points dynamically
    for i, score in enumerate(data["scores"]):
        plt.text(i, score + 1.5, f'{score}%', ha='center', fontsize=9, fontweight='bold', color='#24292e')

    # Global chart layout parameters
    plt.title('Academic Performance Trend', fontsize=14, fontweight='bold', pad=15, color='#24292e')
    plt.xlabel('Assessments', fontsize=11, labelpad=10)
    plt.ylabel('Scores (%)', fontsize=11, labelpad=10)
    plt.ylim(min(data["scores"]) - 10, 105) # Adapts scale down dynamically if scores drop
    
    plt.tight_layout()
    plt.savefig('performance_graph.png', dpi=300, transparent=True)
    plt.close() # Frees system memory after writing file
    print("📈 Graph updated and saved as 'performance_graph.png'!")

def add_new_grade(data):
    """Command line interface prompt to append a new assessment score."""
    name = input("Enter assessment name (e.g., Test 3): ").strip()
    if not name:
        print("❌ Name cannot be blank.")
        return
    
    try:
        score = float(input("Enter percentage grade score (0-100): "))
        if 0 <= score <= 100:
            data["tests"].append(name)
            data["scores"].append(score)
            save_data(data)
            print(f"✅ Added {name}: {score}%")
            # Automatically update visual asset file when raw values change
            generate_performance_graph(data)
        else:
            print("❌ Grade score must fall between 0 and 100.")
    except ValueError:
        print("❌ Invalid input. Grade score must be a numerical digit.")

def display_report_card(data):
    """Prints a structured text summary to the terminal window."""
    print("\n================ REPORT CARD ================")
    if not data["tests"]:
        print("No grades recorded yet.")
    for t, s in zip(data["tests"], data["scores"]):
        print(f" 📋 {t:<15} : {s:>5}%")
    print("---------------------------------------------")
    avg = sum(data["scores"]) / len(data["scores"]) if data["scores"] else 0
    print(f" Total Average Score: {avg:.2f}%")
    print("=============================================\n")

def main():
    """Main execution loop for Grade Buddy application."""
    data = load_data()
    while True:
        print("--- Grade Buddy Menu ---")
        print("1. View Report Card")
        print("2. Add Test Score")
        print("3. Regenerate Graph Only")
        print("4. Exit")
        
        choice = input("Select an option (1-4): ").strip()
        if choice == "1":
            display_report_card(data)
        elif choice == "2":
            add_new_grade(data)
        elif choice == "3":
            generate_performance_graph(data)
        elif choice == "4":
            print("Goodbye!")
            break
        else:
            print("❌ Invalid entry selection. Try again.")

if __name__ == "__main__":
    main()
