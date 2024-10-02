# AI CTO Project

## Project Overview

AI CTO is an innovative platform that leverages artificial intelligence to assist startups and businesses in creating comprehensive project plans and technical specifications. By answering a series of questions, users receive tailored project outlines, technology stack recommendations, and even job descriptions for key roles.

## How It Works

1. Users fill out a questionnaire about their project requirements.
2. The system processes the responses using an AI-powered assistant.
3. A detailed project plan is generated, including tech stack, features, timeline, and budget estimates.
4. Users can review and refine the generated plan.
5. The system can also create job postings based on the project requirements.

## Project Structure

The project is divided into two main components:

1. Frontend (Next.js application)
2. Backend (FastAPI service)

### Frontend

- Located in the `frontend/` directory
- Built with Next.js 14, React 18, and TypeScript
- Uses Tailwind CSS for styling
- Communicates with the backend API to submit questionnaires and receive project plans

### Backend

- Located in the `backend/` directory
- Built with FastAPI and Python 3.9+
- Uses Supabase for database operations
- Integrates with OpenAI's Assistant API for AI-powered project plan generation

## How the Backend Works

1. The backend receives questionnaire responses from the frontend.
2. It stores the responses in Supabase.
3. The OpenAI Assistant is invoked to process the questionnaire and generate a project plan.
4. The generated plan is stored in Supabase and returned to the frontend.

## Deployment

The project is deployed using Vercel for both the frontend and backend components.

### Frontend Deployment

- The Next.js application is automatically deployed to Vercel.
- Vercel handles server-side rendering and static site generation.
- Environment variables are configured in the Vercel dashboard.

### Backend Deployment

- The FastAPI backend is deployed as a Vercel Serverless Function.
- A `vercel.json` file in the backend directory configures the deployment.
- Environment variables (e.g., API keys) are set in the Vercel dashboard.

## How Vercel Works

Vercel provides a seamless deployment experience for both frontend and backend:

1. It automatically detects the framework (Next.js for frontend, FastAPI for backend).
2. It builds the project according to the framework's requirements.
3. For the frontend, it optimizes assets and sets up serverless rendering.
4. For the backend, it packages the FastAPI app into serverless functions.
5. It provides automatic scaling, CDN distribution, and HTTPS encryption.

## Local Development

To run the project locally:

1. Clone the repository
2. Set up environment variables (see `.env.example` files in frontend and backend directories)
3. Install dependencies for both frontend and backend
4. Run the frontend development server: `npm run dev` in the frontend directory
5. Run the backend development server: `uvicorn app.main:app --reload` in the backend directory

## Contributing

Contributions are welcome! Please see the `CONTRIBUTING.md` file for guidelines on how to contribute to this project.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.
