# N8N-AI-AGENTS
A powerful collection of AI-powered n8n workflows to automate content creation, lead generation, research, and personal productivity.

# n8n AI-Powered Automation Workflows

This collection of n8n workflows demonstrates a variety of AI-powered automations, from content creation and lead generation to personal productivity and administrative tasks. Each workflow is designed to be a powerful, standalone solution that can also be adapted and integrated into larger systems.

## Table of Contents

1.  [Auto Create Blog Post](#1-auto-create-blog-post)
2.  [Auto Medical Prescription Renewal Agent](#2-auto-medical-prescription-renewal-agent)
3.  [Bookmarks Scraper](#3-bookmarks-scraper)
4.  [Free Reddit Short Videos Creator](#4-free-reddit-short-videos-creator)
5.  [Google Deep Research Agent](#5-google-deep-research-agent)
6.  [Lead Generation and Enrichment Agent](#6-lead-generation-and-enrichment-agent)
7.  [Personal Daily Digest Agent](#7-personal-daily-digest-agent)
8.  [UGC Ads Creator](#8-ugc-ads-creator)
9.  [Viral 3 Hour Long Sleep Video Generator](#9-viral-3-hour-long-sleep-video-generator)
10. [Viral Podcast Clips Creator](#10-viral-podcast-clips-creator)
11. [Viral Youtube Template Generator](#11-viral-youtube-template-generator)
12. [Wan 2.2 Video Generator](#12-wan-22-video-generator)

---

### 1. Auto Create Blog Post

This workflow automates the entire process of writing a blog post, from ideation to publication. It identifies trending topics, conducts in-depth research, and drafts a complete article.

-   **Description**: The workflow begins by scraping popular bookmarks from Pinboard to find trending AI-related topics. It then uses a "Google Deep Research" sub-workflow to gather information from multiple sources. An AI agent synthesizes this research into a detailed, engaging article and posts the final piece to a Notion page.
-   **Key Services**: Pinboard, Google Search, Notion, Google Gemini.
-   **Sub-workflows Used**: `Bookmarks Scraper`, `Google Deep Research Agent`.

### 2. Auto Medical Prescription Renewal Agent

A HIPAA-compliant chatbot designed to automate the prescription renewal process for a medical practice, reducing administrative overhead and improving patient experience.

-   **Description**: The workflow interacts with patients via a chat interface. It securely verifies patient identity and active prescriptions against a Notion database. Once the correct medication is confirmed, it logs the renewal order.
-   **Key Services**: Notion, Google Gemini.

### 3. Bookmarks Scraper

A utility workflow designed to scrape and summarize the content of a given URL. It's intended to be called by other workflows that require web page content.

-   **Description**: This workflow receives a URL, scrapes the full HTML content, converts it into clean Markdown, and then uses Google Gemini to generate a concise summary.
-   **Key Services**: Google Gemini.

### 4. Free Reddit Short Videos Creator

Automate the creation of short-form videos for platforms like YouTube Shorts or TikTok using content from Reddit.

-   **Description**: This workflow fetches top posts from specified subreddits (e.g., `r/Jokes`, `r/LifeProTips`). It uses an AI model to generate a video script and title from the Reddit post, then calls an external service to create the video. The final video is uploaded to YouTube. It also includes an optional manual approval step before publishing.
-   **Key Services**: Reddit, YouTube, OpenAI, Google Gemini.

### 5. Google Deep Research Agent

A powerful sub-workflow that performs automated, in-depth research on a given topic using Google Search.

-   **Description**: This agent takes a "context" as input, uses an AI model to generate multiple creative search terms, executes the searches, and then scrapes and summarizes the top results. It also includes a step to filter out irrelevant content, ensuring only the most useful information is returned.
-   **Key Services**: Google Programmable Search, Google Gemini.

### 6. Lead Generation and Enrichment Agent

An automated agent that captures lead generation requests from Telegram, finds relevant leads, enriches their data, and saves them to a CRM or Google Sheet.

-   **Description**: Triggered by a Telegram message (e.g., "Find me roofing companies in North Carolina"), this workflow uses Apify to scrape leads from Apollo.io. It then enriches each lead with personalized icebreakers using Perplexity AI, calculates a lead score, and adds the enriched data to a Google Sheet.
-   **Key Services**: Telegram, Apify (Apollo.io Scraper), Google Sheets, Perplexity AI, OpenAI.

### 7. Personal Daily Digest Agent

A workflow that acts as a personal assistant, curating a daily digest of news, weather, emails, and calendar events.

-   **Description**: Running on a daily schedule, this workflow gathers top stories from RSS feeds, fetches the local weather forecast via OpenWeatherMap, summarizes unread emails from Gmail, and lists the day's events from Google Calendar. An AI agent compiles all this information into a single, easy-to-read email digest.
-   **Key Services**: Gmail, Google Calendar, OpenWeatherMap, RSS Feeds, Google Gemini.

### 8. UGC Ads Creator

A creative assistant that generates User-Generated Content (UGC)-style video ads from a simple image and text prompt, all managed through Telegram.

-   **Description**: A user sends an image and a text prompt to a Telegram bot. The workflow uses a multi-modal AI model to generate a new photorealistic image. It then crafts a two-segment video script based on the user's ad concept and generates a video, which is sent back to the user.
-   **Key Services**: Telegram, Google Gemini, Anthropic Claude, Kie.ai.

### 9. Viral 3 Hour Long Sleep Video Generator

This workflow automates the creation of long-form, looping ambient videos, popular in the "sleep video" category on YouTube.

-   **Description**: The workflow starts by generating a creative concept for a sleep video (e.g., "cute 3D animals"). It then creates prompts for an image, a looping video, and a lullaby-style music track. It uses ComfyUI for video generation and another service for music before combining and looping them into a 3-hour-long video file.
-   **Key Services**: ComfyUI, Google Gemini.

### 10. Viral Podcast Clips Creator

A powerful content repurposing engine that automatically finds the most "viral" moments in a long-form podcast and turns them into short-form clips for social media.

-   **Description**: The workflow takes a YouTube video URL, downloads and transcribes the audio, and uses an AI model to analyze the transcript and identify highlight segments. It then clips the original video, adds a background video, generates a catchy title, and posts the final clip to TikTok.
-   **Key Services**: YouTube, AssemblyAI, OpenAI, Google Gemini, TikTok.

### 11. Viral Youtube Template Generator

A content strategy tool that analyzes top-performing YouTube videos to generate a "template" for creating viral content on a given topic.

-   **Description**: Given a content idea (e.g., "animal sleep videos"), the workflow generates relevant search keywords and scrapes YouTube for the most relevant, high-performing videos. It calculates an engagement score to identify the best videos, then uses an AI model to analyze their titles and thumbnails to find common patterns. Finally, it generates five new title ideas and a prompt for creating a new, optimized thumbnail.
-   **Key Services**: Apify (YouTube Scraper), Hugging Face, Google Gemini.

### 12. Wan 2.2 Video Generator

A straightforward workflow for generating video clips from an image and a text prompt using the Wan 2.2 video model hosted on ComfyUI.

-   **Description**: A user submits an image and a text prompt through a form. The workflow uploads the image to a ComfyUI instance and triggers a video generation process using the specified prompt. Once complete, the final video is available for download.
-   **Key Services**: ComfyUI.
