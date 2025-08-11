# Project 7 - *Task Manager App*

Submitted by: **Kemely Alfonso Martinez**

**Task Manager App** is an iOS app that allows users to create, manage, and track their daily tasks with persistent local storage and an intuitive calendar view for better organization.

Time spent: **5** hours spent in total

## Required Features

The following **required** functionality is completed:

- [x] App displays a list of tasks
- [x] Users can add tasks to the list
- [x] Session persists when application is closed and relaunched (tasks dont get deleted when closing app) 
  - [x] Note: You have to quit the app, not minimize it, in order to see the persistence.
- [x] Tasks can be deleted
- [x] Users have a calendar view via navigation controller that displays tasks

The following **additional** features are implemented:

- [x] Tasks can be toggled completed
- [x] User can edit tasks by tapping on the task in the feed view
- [x] Tab bar navigation between Tasks list and Calendar views
- [x] Swipe-to-delete functionality for easy task removal
- [x] Tasks are automatically sorted (incomplete tasks first, then completed)
- [x] Visual feedback for completed vs incomplete tasks
- [x] Empty state message when no tasks exist
- [x] Calendar shows visual indicators for dates with tasks
- [x] Date picker for setting task due dates
- [x] Task notes/descriptions support
- [x] Smooth animations for task state changes

## Notes

### Challenges Encountered While Building the App:

**UserDefaults Implementation**: Initially struggled with making the Task struct conform to Codable protocol for JSON serialization. Had to understand the relationship between JSONEncoder/JSONDecoder and UserDefaults for proper data persistence.

**Tab Bar Controller Setup**: The storyboard-based tab bar setup was challenging, especially with proper navigation controller hierarchy. Solved this by implementing tab bar creation programmatically in SceneDelegate.swift, which provided more control and reliability.

**Calendar Integration**: Understanding UICalendarView delegate methods and date component handling was complex. The calendar decoration system required careful date comparison logic to properly display task indicators.

**Task State Management**: Ensuring proper synchronization between the Tasks list and Calendar views when tasks are created, edited, or completed required careful attention to the data flow and refresh mechanisms.

**Navigation Flow**: Setting up proper segue connections for task editing and creation, especially handling the modal presentation and data passing between view controllers.

### Technical Implementation:

- **Data Persistence**: Used UserDefaults with JSON encoding/decoding for reliable local storage
- **Architecture**: Followed MVC pattern with proper separation of concerns
- **UI/UX**: Implemented native iOS design patterns with smooth animations
- **Navigation**: Hybrid approach using storyboard for UI layout and programmatic tab bar setup

The app successfully demonstrates core iOS development concepts including data persistence, navigation patterns, table views, calendar integration, and user interface design.

## License

    Copyright [2025] [Kemely Alfonso Martinez]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
