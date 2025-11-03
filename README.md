Want to see how it works !!!

URL : https://slide-wizard-smoky.vercel.app/

AI-Powered Presentation Generator - Project Overview

What It Does

This is a full-stack AI-powered presentation creation platform that allows users to automatically generate professional PowerPoint presentations using artificial intelligence. Users simply provide a topic, optional description, and slide count, and the AI creates complete presentations with relevant content and images.


Core Features

1. AI Presentation Generation
   
Generates complete presentations from just a topic and slide count

Creates 6-8 detailed bullet points per slide (75-95 characters each)

AI-generated images for each slide using Google Gemini image generation

Unique title slide with topic-relevant imagery

Random left/right image placement (35% image, 65% content layout)

2. Theme Support

Five professional themes:

Professional: Corporate, formal style

Creative: Vibrant, artistic design

Minimal: Clean, elegant simplicity

Bold: Strong, impactful visuals

Academic: Educational, scholarly format

3. User Management

Email authentication with auto-confirm

User profiles and personalized dashboards

Presentation history tracking

Session management

4. Editing Capabilities

Manual text editing for all slides

AI-powered edit suggestions

Real-time preview

Title and content modifications

5. Export & Download

Download as PowerPoint (.pptx) format

Preserves formatting, images, and themes


Professional slide layouts

Technology Stack

Frontend

React 18 with TypeScript

Vite for build tooling

Tailwind CSS for styling with custom design system

React Router for navigation

TanStack Query for data fetching

Shadcn UI components

PptxGenJS for PowerPoint generation

Backend (Lovable Cloud/Supabase)

PostgreSQL database with Row Level Security (RLS)

Supabase Auth for user authentication

Edge Functions for serverless logic

Lovable AI Gateway for AI generation (Google Gemini models)

AI Integration


Google Gemini 2.5 Flash for content generation

Google Gemini 2.5 Flash Image Preview for image generation

Structured output with tool calling

Theme-specific prompting for consistent styling

Database Schema

Tables

profiles: User information (linked to auth.users)

presentations: Stores presentation metadata (title, topic, theme, slide count)

slides: Individual slide data (title, content, images, layout)

Security

RLS policies ensure users only access their own data

Secure authentication flow

Protected API endpoints


Key Workflows

1. Creating a Presentation

User Input → Edge Function → AI Content Generation → AI Image Generation → Database Storage → UI Display

2. Downloading PPT

Fetch Slides → Process Images (Base64) → Generate PPTX → Download File

3. Editing

User Edits → Database Update → Real-time UI Refresh


Edge Functions

1.generate-presentation: Main AI generation engine

Takes topic, description, slide count, theme

Generates content via Lovable AI

Creates images for each slide

Stores in database

2.ai-edit-suggestions: Provides AI-powered editing help

3.generate-slide-image: Regenerates individual slide images


File Structure

/src/pages: Main routes (Index, Auth, Dashboard, Create, Editor, History)

/src/components: Reusable UI components

/supabase/functions: Backend edge functions

/src/integrations/supabase: Auto-generated Supabase client


Design System

Custom theme with HSL color tokens, responsive layouts, and professional 
styling optimized for both light/dark modes.

This application streamlines presentation creation from hours to seconds using cutting-edge AI technology.
