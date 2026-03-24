# Day-42-Runners-GitHub-Hosted-Self-Hosted

## Task 1: GitHub-Hosted Runners

1. Create a workflow with 3 jobs, each on a different OS:

     - ubuntu-latest
     - windows-latest
      - macos-latest
        
2. In each job, print:

     - The OS name
     - The runner's hostname
     - The current user running the job
      
3. Watch all 3 run in parallel

<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/d07801bb-7b05-4f1f-b0e3-aa9b44cb7395" /> <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/d2922964-18d0-4687-bbcf-fccf2f1bdb16" /> <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/2249f849-6a6a-498d-91a5-781cbe3c8877" /> <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/9bd50b43-e2d0-40b1-b4cd-ba7179ffa7ba" />

## Task 2: Explore What's Pre-installed

1. On the ubuntu-latest runner, run a step that prints:

   - Docker version
   
    - Python version
     
   - Node version
   
   - Git version
   
3. Look up the GitHub docs for the full list of pre-installed software on ubuntu-latest

<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/689fdc82-82a3-467e-adc4-787197e5fcb7" />

### Task 3: Set Up a Self-Hosted Runner

1. Go to your GitHub repo → Settings → Actions → Runners → New self-hosted runner

2. Choose Linux as the OS
 
3. Follow the instructions to download and configure the runner on:

   - Your local machine, OR
   - A cloud VM (EC2, Utho, or any VPS)
4. Start the runner — verify it shows as Idle in GitHub

<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/36bb82a5-5afc-4fc2-b878-e1e6ceb378df" />
<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/f3bc1226-1bbd-4896-be04-9a73c141fbd1" />

### Task 4: Use Your Self-Hosted Runner

1. Create .github/workflows/self-hosted.yml
 
2. Set runs-on: self-hosted
   
3. Add steps that:
    - Print the hostname of the machine (it should be YOUR machine/VM)
     - Print the working directory
     - Create a file and verify it exists on your machine after the run
   
4. Trigger it and watch it run on your own hardware

<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/5e2c2d0b-7325-4331-b3ee-6a0acf460804" />

## Task 5: Labels

1. Add a label to your self-hosted runner (e.g., my-linux-runner)

2. Update your workflow to use runs-on: [self-hosted, my-linux-runner]

3. Trigger it — does it still pick up the job?

<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/83cb553c-2e50-4cb1-8ef0-9357e358ccfe" />

### Task 6: GitHub-Hosted vs Self-Hosted

|-----| GitHub-Hosted|Self-Hosted|
|------|-----|-----|
|Who manages it?|GitHub manages|You manage|
|Cost|Free|You pay for your machine|
|Pre-installed tools|Already installed|You install everything|
|Good for|simple projects|Custom setup|
|Security concern|Less control over machine|Full control but your responsibility|
