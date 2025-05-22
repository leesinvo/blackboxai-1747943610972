# School Management System

A comprehensive web-based school management system built with Next.js, Firebase, and Tailwind CSS. The system supports multiple user roles and provides role-specific dashboards for administrators, teachers, students, and parents.

## Features

### Authentication
- Secure login and registration
- Role-based access control (admin, teacher, student, parent)
- Password reset functionality
- Protected routes with middleware

### Role-Specific Dashboards

#### Admin Dashboard
- User management (teachers, students, parents)
- Class management
- Attendance reports and statistics
- Academic calendar management
- System-wide messaging

#### Teacher Dashboard
- Class management
- Attendance tracking
- Assignment creation and grading
- Student performance monitoring
- Parent communication

#### Student Dashboard
- Class schedule viewing
- Assignment submission
- Grade tracking
- Attendance history
- Course materials access

#### Parent Dashboard
- Child performance monitoring
- Attendance tracking
- Teacher communication
- Academic progress reports

## Tech Stack

- **Frontend**: Next.js with TypeScript
- **Styling**: Tailwind CSS with shadcn/ui components
- **Backend**: Firebase (Authentication, Firestore)
- **State Management**: React Context API
- **Routing**: Next.js App Router

## Getting Started

1. Clone the repository
2. Install dependencies:
   ```bash
   npm install
   ```

3. Create a Firebase project and add your configuration to `.env.local`:
   ```env
   NEXT_PUBLIC_FIREBASE_API_KEY=your_api_key
   NEXT_PUBLIC_FIREBASE_AUTH_DOMAIN=your_auth_domain
   NEXT_PUBLIC_FIREBASE_PROJECT_ID=your_project_id
   NEXT_PUBLIC_FIREBASE_STORAGE_BUCKET=your_storage_bucket
   NEXT_PUBLIC_FIREBASE_MESSAGING_SENDER_ID=your_messaging_sender_id
   NEXT_PUBLIC_FIREBASE_APP_ID=your_app_id
   ```

4. Run the development server:
   ```bash
   npm run dev
   ```

5. Open [http://localhost:8000](http://localhost:8000) with your browser to see the result.

## Project Structure

```
src/
├── app/                    # Next.js app directory
│   ├── auth/              # Authentication pages
│   │   ├── login/
│   │   ├── register/
│   │   └── reset-password/
│   └── dashboard/         # Role-specific dashboards
│       ├── admin/
│       ├── teacher/
│       ├── student/
│       └── parent/
├── components/            # Reusable UI components
│   └── ui/               # shadcn/ui components
├── contexts/             # React Context providers
├── lib/                  # Utility functions and configurations
└── middleware.ts         # Authentication middleware

```

## Firebase Setup

1. Create a new Firebase project in the [Firebase Console](https://console.firebase.google.com)
2. Enable Authentication and Firestore
3. Set up authentication methods (Email/Password)
4. Create the necessary Firestore collections:
   - users
   - classes
   - assignments
   - attendance
   - messages

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.
