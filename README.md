<div align="center">

# ✈️ TravelMate

### Production-ready Flutter travel & hotel booking app

A polished, Booking.com-style mobile experience — browse destinations, search hotels & flights, and complete bookings in a few taps.

[![Flutter](https://img.shields.io/badge/Flutter-3.0%2B-02569B?logo=flutter&logoColor=white)](https://flutter.dev)
[![Dart](https://img.shields.io/badge/Dart-3.0%2B-0175C2?logo=dart&logoColor=white)](https://dart.dev)
[![Architecture](https://img.shields.io/badge/Architecture-Clean-success)]()
[![License](https://img.shields.io/badge/License-MIT-lightgrey)]()

![TravelMate App Preview](./app_preview.jpeg)

</div>

---

## Overview

TravelMate is a full-featured Flutter UI kit for travel booking apps: animated splash, home feed with destinations & featured hotels, live-filtered search (hotels + flights), a rich hotel detail screen, a complete multi-step booking flow, and screens for booking history, wishlist, and profile. Built with mock data by default and designed to drop in a real backend in minutes.

## Highlights

- 🏠 **Home** — hero search, popular destinations, featured hotels & packages
- 🔍 **Search** — hotels & flights tabs with live filtering, price/rating/star filters, sorting
- 🏨 **Hotel Details** — image gallery, amenities, map placeholder, guest reviews
- 📅 **Booking Flow** — date picker, guest counter, price breakdown, confirmation
- 🧾 **My Bookings** — Upcoming / Completed / Cancelled tabs
- ❤️ **Wishlist** — saved hotels & packages
- 👤 **Profile** — stats, preferences, dark mode toggle
- 🌓 **Dark Mode** + smooth animations, shimmer loading, and bottom navigation throughout

## Tech Stack

| | |
|---|---|
| **Framework** | Flutter 3.0+ / Dart 3.0+ |
| **Fonts** | Playfair Display (display) · Poppins (body) |
| **Key packages** | `google_fonts`, `flutter_rating_bar`, `cached_network_image`, `smooth_page_indicator`, `flutter_staggered_animations`, `shimmer`, `lottie` |

## Getting Started

```bash
cd travelmate
flutter pub get
flutter run
```

## Project Structure

```
lib/
├── main.dart                # App entry point
├── theme/                   # Colors, typography, gradients
├── models/                  # Hotel, Flight, Booking, Review
├── data/                    # Mock data (swap for real API)
├── widgets/                 # Reusable UI components
└── screens/                 # Splash, Home, Search, Hotel Detail,
                              # Booking, My Bookings, Wishlist, Profile
```

## Connecting a Real Backend

Replace `lib/data/mock_data.dart` with live API calls:

```dart
Future<List<Hotel>> fetchHotels({String? query, double? maxPrice}) async {
  final response = await http.get(
    Uri.parse('https://your-api.com/hotels?q=$query&maxPrice=$maxPrice'),
  );
  return (jsonDecode(response.body) as List)
      .map((j) => Hotel.fromJson(j))
      .toList();
}
```

**Recommended integrations:** Google Maps (`google_maps_flutter`) · Firebase Auth · Stripe · Firebase Firestore · Booking.com / Amadeus API

## Design Tokens

| Token | Value |
|---|---|
| Primary | `#1A73E8` |
| Accent | `#FF6B35` |
| Background | `#F8F9FE` |

---

<div align="center">

Built with Flutter 💙

</div>
