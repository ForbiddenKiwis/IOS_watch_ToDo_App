# watch_ToDo_App - WatchOS Notes Application

This is a simple To-Do app designed for Apple Watch using SwiftUI. The app allows users to create, view, and manage notes directly from their Watch. Notes are stored locally in the device’s document directory and are encoded in JSON format for persistence.

## Features

- **Add Notes**: Users can add new notes by entering text into a TextField and pressing the "+" button.
- **View Notes**: Users can view all saved notes in a list, which shows a preview of the note’s text.
- **Delete Notes**: Notes can be deleted using swipe-to-delete functionality.
- **Detail View**: Tapping on a note opens a detail view with the full content of the note.
- **Persistent Storage**: Notes are saved locally in the device’s document directory using JSON encoding and decoding.

## File Structure

The project consists of the following key files:

### `ContentView.swift`
- **Purpose**: Displays the list of notes and provides functionality for adding, deleting, and saving notes.
- **Key Functions**:
  - `save()`: Saves the notes array to the device’s document directory in JSON format.
  - `load()`: Loads the notes array from the device’s document directory.
  - `delete(offsets:)`: Deletes a note from the list and updates storage.
  - `getDocDir()`: Retrieves the document directory URL for file storage.
  
### `DetailView.swift`
- **Purpose**: Displays the detailed view of a selected note.
- **Key Features**:
  - Shows the full content of the note.
  - Displays meta information, such as the total number of notes and the index of the current note.

### `Note.swift`
- **Purpose**: Defines the `Note` model used throughout the app.
- **Structure**:
  - `id`: A unique identifier for each note (`UUID`).
  - `text`: The content of the note.

## Installation

To run this app on your local machine, follow these steps:

1. Clone the repository to your local machine.
    ```bash
    git clone https://github.com/yourusername/watch_ToDo_App.git
    ```

2. Open the project in Xcode.

3. Select the correct target for your Apple Watch device or simulator.

4. Build and run the project.

## Usage

- Upon launching the app, you will see an input field to add a new note and a list of existing notes.
- Tap the "+" button to add a note to the list.
- Swipe left on a note to delete it.
- Tap on any note to view its details, where you can see the full content and the index of the note.

## Contributing

If you would like to contribute to this project, please fork the repository and submit a pull request. Contributions are welcome for adding new features or fixing bugs!

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgements

- Thanks to Apple’s SwiftUI framework for simplifying the UI development for WatchOS apps.
- Special thanks to the Swift and SwiftUI community for their tutorials and resources.

