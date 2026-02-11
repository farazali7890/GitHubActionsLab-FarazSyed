Purpose of Each Workflow
The first workflow, dependent-jobs.yml, ensures that the build, test, and deploy stages happen in a specific, logical order. The second workflow, multi-platform.yml, is designed to verify that the application runs correctly across different operating systems at the same time.

Key Concepts
In the first workflow, I used the needs keyword to create a dependency chain where each job waits for the previous one to succeed. For the second workflow, I used runs-on to target ubuntu-latest, windows-latest, and macos-latest. This workflow triggers on a pull request to demonstrate how to test code before merging it into the master branch.

Challenges and Solutions
Setting up the project and pushing it for the first time was difficult because I wasn’t sure how to get the project environment setup in netbeans after cloning but also once I figured that out and pushed to github no workflows appeared in the Actions tab after my initial push. I discovered this was due to a naming error in my YAML file, I had set the trigger to the "main" branch, but my GitHub repository was actually named "master". Once I corrected the branch name in the code and repushed, the workflows executed perfectly. Using the last class as reference helped with the .yml files a lot! 
