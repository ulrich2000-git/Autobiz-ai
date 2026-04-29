# Deployment Guide for Autobiz-ai

This guide provides comprehensive instructions for setting up, configuring, and deploying the Autobiz-ai project, a Next.js/Node.js SaaS application featuring Stripe integration, Supabase, WhatsApp API, and deployment on Netlify.

## Table of Contents

1. [Prerequisites](#prerequisites)
2. [Project Setup](#project-setup)
3. [Configuration](#configuration)
4. [Deployment](#deployment)
5. [Additional Resources](#additional-resources)

## Prerequisites

Before you begin, ensure you have the following tools installed:
- [Node.js](https://nodejs.org/) (v14 or later)
- [Yarn](https://classic.yarnpkg.com/lang/en/docs/install/#windows-stable) (optional, but recommended)
- [Git](https://git-scm.com/)
- [Netlify CLI](https://docs.netlify.com/cli/get-started/)
- Access to Supabase and Stripe accounts

## Project Setup

1. **Clone the Repository**:  
   Open your terminal and run the following command:
   ```bash
   git clone https://github.com/ulrich2000-git/Autobiz-ai.git
   cd Autobiz-ai
   ```

2. **Install Dependencies**:  
   Install project dependencies using npm or yarn:
   ```bash
   npm install
   # or
   yarn install
   ```

## Configuration

1. **Environment Variables**:  
   Create a `.env.local` file in the root of your project with the following variables:
   ```env
   NEXT_PUBLIC_SUPABASE_URL=your_supabase_url
   NEXT_PUBLIC_SUPABASE_ANON_KEY=your_supabase_anon_key
   STRIPE_SECRET_KEY=your_stripe_secret_key
   WHATSAPP_API_URL=your_whatsapp_api_url
   WHATSAPP_API_TOKEN=your_whatsapp_api_token
   ```
   Replace the placeholders with actual values from your Supabase and Stripe accounts.

2. **Database Setup**:  
   - Go to your Supabase dashboard and create a new project.
   - Set up the required tables and authentication methods as per the project requirements.

3. **Setting up Stripe**:  
   - Log in to your Stripe account.
   - Create products and pricing plans as necessary. Note down the product IDs.
   - Configure webhooks in your Stripe dashboard to listen for relevant events.

## Deployment

1. **Deploying to Netlify**:  
   - Ensure you have the Netlify CLI installed:
   ```bash
   npm install -g netlify-cli
   ```
   - Login to Netlify using:
   ```bash
   netlify login
   ```
   - Create a new site from your project:
   ```bash
   netlify init
   ```
   - Follow the prompts to link your repository.
   - Set the environment variables in the Netlify dashboard under 'Site settings' > 'Build & deploy' > 'Environment' > 'Environment Variables'.
   - Deploy your site:
   ```bash
   netlify deploy
   ```

2. **Verifying Deployment**:  
   - Once deployed, verify the application is running correctly by visiting the provided URL.
   - Test Stripe integration by creating test transactions and ensuring that the payment flow works smoothly.

## Additional Resources

- [Next.js Documentation](https://nextjs.org/docs)
- [Node.js Documentation](https://nodejs.org/en/docs/)
- [Supabase Documentation](https://supabase.io/docs)
- [Stripe Documentation](https://stripe.com/docs)
- [WhatsApp API Documentation](https://developers.facebook.com/docs/whatsapp)
- [Netlify Documentation](https://docs.netlify.com/)

If you encounter any issues, refer to the documentation for troubleshooting steps or seek help from your development team.