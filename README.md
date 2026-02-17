# 🎬 Full Stack Video Streaming Platform (Spring Boot + React + HLS)

A full-stack video streaming application that allows users to upload videos, processes them using FFmpeg, converts them into HLS format, and streams them efficiently using adaptive bitrate streaming. The frontend is built with React and provides smooth video playback using HLS.js and Video.js.

---

## 🚀 Features

- Video upload with metadata (title & description)  
- Upload progress tracking  
- Video metadata storage using MySQL  
- FFmpeg-based HLS video conversion  
- Adaptive video streaming using HLS  
- Chunk-based range streaming  
- React-based video player using HLS.js & Video.js  
- RESTful API architecture  
- Cross-Origin support  

---

## 🛠️ Tech Stack

### Backend
- Java  
- Spring Boot  
- Spring Data JPA  
- MySQL  
- FFmpeg  

### Frontend
- React (Vite)  
- Axios  
- HLS.js  
- Video.js  
- Flowbite React  
- Tailwind CSS  

---

## 🏗️ Project Architecture

React Frontend
|
|-- Upload Video (multipart/form-data)
|
Spring Boot REST API
|
|-- Store File
|-- Save Metadata
|-- FFmpeg Processing
|
FFmpeg → Convert MP4 → HLS (.m3u8 + .ts)
|
Frontend Player loads playlist


---

## 📁 Backend APIs

| Method | Endpoint | Description |
|------|---------|------------|
| POST | /api/v1/videos | Upload video |
| GET | /api/v1/videos | Get all videos |
| GET | /api/v1/videos/stream/{id} | Stream full video |
| GET | /api/v1/videos/stream/range/{id} | Chunk streaming |
| GET | /api/v1/videos/{id}/master.m3u8 | HLS playlist |
| GET | /api/v1/videos/{id}/{segment}.ts | HLS segment |

---

## ⚙️ Setup Instructions

### Prerequisites

- Java 17+  
- Node.js 18+  
- MySQL  
- FFmpeg installed  

---

### Backend Setup

```bash
git clone <repository-url>
cd spring-stream-backend


Update application.properties:

spring.datasource.url=jdbc:mysql://localhost:3306/Video_Stream_Application
spring.datasource.username=root
spring.datasource.password=yourpassword

files.video=videos
file.video.hsl=videos_hsl


Run backend:

mvn spring-boot:run


Frontend Setup

cd stream-frontend
npm install
npm run dev

```


### Future Improvements

JWT Authentication

Video quality selection (360p/720p/1080p)

Thumbnail generation

Cloud storage (AWS S3)

CDN integration

### Screenshots

### 👨‍💻 Author

Prateek Yadav
