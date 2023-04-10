
## Azure Board
 - Standalone service that helps teams plan, track and discuss work across the entire SDLC process
 - Provides a flexible, customizable platform for managing work items
   - user stories
   - bugs
   - tasks
   - issues
 - Supports Agile methodolgies including Scrum and Kanban

## Azure board hubs
 - Work Items : Access list of work items based on specific criteria, such as 
   - those assigned to you, 
   - ones you follow 
   - work items you viewed or updated
 - Boards : View work items as cards and update their status through drag and drop
   - Use this feature to implement Kanban
   - Visualize work flow for a team
 - Backlogs: view, plan, order and organize work items, including using a product backlog 
   - to represent your project plan 
   - a portfolio backlog to group work under features and epics
 - Sprints : access your teams filtered view of work items based on specified sprint or iteration path
   - Assign work to a sprint using drag and drop from the backlog
   - Interact with a backlog list or card based taskboard to implement scrum practices
 - Queries : Generate custom work item lists and perform various tasks such as triage work, make bulk updates, and view relationship between wrk items
   - Allows for creating status and trend charts that can be added to dashboard
 - Delivery Plans : Management team can view deliverables and track dependencies across multiple teams in a calendar view
   - View upto 15 team backlogs
   - custom portfolio backlogs and epics
   - Work that span several iterations
   - user can add backlog items to a plan, 
   - users can view rollup progress of features and epics 
   - users can view dependencies between work items

## Implement Details
- Basic : 
  - Simple model that tracks Issues, tasks and Epics
- Agile :
  - Portfolio backlog : Epic -> Feature
  - Backlog : Feature -> User Story -> Task
  - Issue & Bug tracking -> Issue
- Scrum: Track works through product backlog items (PBI) and bugs on Kanban board or viewed on a sprint taskboard
- Capability Maturity Model Integration (CMMI)

## Configure dashboards and power BI reports

## Gain visibility through end to end traceability
- Tracking work from requirement to deployment
- Gain insight at each step of decisions made and software deployed
  - Create a branch from a requirement
  - Create a pull request of updated branch
  - Validate the pull request using a build pipeline
  - Create and run inline tests on requirements
  - Merge the pull request into the main, default branch
  - Deploy changes into production with deployment status to Azure boards
  - Monitor and report on requirements traceability

- Support Independent and Autonomous teams
  - Work in a specified product area represented by hierarchical paths called Area Paths
  - Define team by their name, members and area paths 
  - Azure board integrates with popular chat tools like Microsoft Teams 