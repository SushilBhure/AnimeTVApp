# AnimeTVApp

AnimeTVApp is a modern Android application that allows users to browse anime content using a public Anime API. The project demonstrates industry-standard Android development practices including Clean Architecture, MVVM, Dependency Injection, Offline-First Data Layer, and Jetpack Compose UI.

## Features

- Browse anime catalog
- Anime detail screen
- Search anime
- Offline caching using Room Database
- Network status awareness
- Pull fresh data from API when online
- Modern Material Design UI
- Error handling and loading states
- Dependency Injection with Hilt
- Clean Architecture + MVVM

## Tech Stack

### UI
- Jetpack Compose
- Material 3
- Navigation Compose

### Architecture
- Clean Architecture
- MVVM Pattern
- Repository Pattern
- Use Cases

### Dependency Injection
- Hilt

### Networking
- Retrofit
- OkHttp
- Kotlin Serialization / Gson

### Local Storage
- Room Database

### Asynchronous Programming
- Kotlin Coroutines
- Flow

## Architecture Overview

Presentation Layer
│
├── UI (Compose Screens)
├── ViewModels
└── UiState
│
Domain Layer
│
├── Use Cases
├── Repository Interfaces
└── Domain Models
│
Data Layer
│
├── Repository Implementations
├── Remote Data Source (Retrofit)
├── Local Data Source (Room)
└── DTO ↔ Entity ↔ Domain Mapping

## Offline-First Strategy

1. Check network availability.
2. If online:
   - Fetch latest data from API.
   - Store data in Room.
   - UI observes Room data.
3. If offline:
   - Display cached Room data.
   - Hide features requiring internet access.

## Project Structure

com.animetvapp
│
├── data
│ ├── local
│ ├── remote
│ ├── mapper
│ └── repository
│
├── domain
│ ├── model
│ ├── repository
│ └── usecase
│
├── presentation
│ ├── screen
│ ├── component
│ ├── navigation
│ └── viewmodel
│
├── di
└── utils


## Learning Goals

This project focuses on:

- Clean Architecture
- MVVM
- Jetpack Compose
- Hilt Dependency Injection
- Retrofit Networking
- Room Database
- Coroutines & Flow
- Repository Pattern
- Offline-First Android Apps

## Screenshots

Add screenshots here.

## Future Enhancements

- Favorites Feature
- Pagination
- Dark Theme Support
- Trailer Playback
- Anime Watchlist
- Unit Testing
- UI Testing

## Author
Sushil Bhure
