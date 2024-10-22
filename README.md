# MusicApp 🎵

A music app that fetches music data from the Deezer API, displays it using `RecyclerView`, and allows users to play song previews. The app uses the `Retrofit` library for network requests and `Picasso` for loading album cover images.

## Features ✨

- Fetches music data using the Deezer API.
- Displays a list of songs in a visually appealing format using `RecyclerView`.
- Play and pause song previews using the Android `MediaPlayer`.
- Displays album cover images using `Picasso`.
- Implements `CardView` for clean and modern UI design.

## Tech Stack 💻

- **Language**: Kotlin
- **Networking**: Retrofit
- **Image Loading**: Picasso
- **UI Components**: RecyclerView, CardView
- **Media Player**: Android MediaPlayer
- **API**: Deezer API (via RapidAPI)

## Screenshots 📸

![WhatsApp Image 2024-10-22 at 07 53 02_bff8eb05](https://github.com/user-attachments/assets/5cbabe4b-bb7a-4d71-a516-ddfa51ace4c1)


## Setup Instructions 🚀

### 1. Open the Project in Android Studio

- Clone the repository or download the project and open it in **Android Studio**.

### 2. Set Up Your Deezer API Key

- Sign up on [RapidAPI](https://rapidapi.com/deezerdevs/api/deezer-1) and obtain the Deezer API key.

### 3. Replace the API Key in Your Project

- Go to the file where you define your `Retrofit` instance and add the required headers for the API call:
    ```kotlin
    val retrofitBuilder = Retrofit.Builder()
        .baseUrl("https://deezerdevs-deezer.p.rapidapi.com/")
        .addConverterFactory(GsonConverterFactory.create())
        .build()
        .create(ApiInterface::class.java)

    val retrofitData = retrofitBuilder.getData("eminem")
    ```

### 4. Build and Run the App

- Run the app on your Android device or emulator to see the list of songs and preview playback.

---

## API Reference 📖

This app fetches music data from the [Deezer API](https://rapidapi.com/deezerdevs/api/deezer-1), which provides:

- Song title
- Artist name
- Album cover image
- Preview of the song (30 seconds)

Ensure you have the correct API key and headers configured in your `Retrofit` setup.

### Example API Request:
```bash
GET https://deezerdevs-deezer.p.rapidapi.com/search?q=eminem
```

### Usage 🎧
-On launch, the app fetches and displays a list of songs by default (in this case, Eminem's songs).
-Tap on the Play button to listen to a 30-second preview of the song.
-Tap the Pause button to stop playback.

### Libraries Used 📚
-Retrofit - For making API calls.
-Picasso - For loading album images.
-Gson - For converting JSON responses into Java/Kotlin objects.
-Android MediaPlayer - For handling audio playback.

### Contributing 🤝
Contributions are always welcome! If you'd like to improve this project, feel free to submit a pull request or open an issue.

License 📄
This project is licensed under the MIT License - see the LICENSE file for details.

Contact 💬
If you have any questions or suggestions, feel free to reach out:

Email: tamroparnisarkar@gmail.com
GitHub: Tamroparni
