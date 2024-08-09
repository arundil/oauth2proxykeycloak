# OAuth2 Proxy with Keycloak and Azure Static Web App

This repository demonstrates how to secure an Azure Static Web App using OAuth2 Proxy with Keycloak as the identity provider.

## Table of Contents

- [Introduction](#introduction)
- [Prerequisites](#prerequisites)
- [Architecture](#architecture)
- [Setup Instructions](#setup-instructions)
  - [1. Keycloak Configuration](#1-keycloak-configuration)
  - [2. OAuth2 Proxy Configuration](#2-oauth2-proxy-configuration)
  - [3. Azure Static Web App Configuration](#3-azure-static-web-app-configuration)
- [Local Development](#local-development)
- [Deployment](#deployment)
- [Troubleshooting](#troubleshooting)
- [Resources](#resources)
- [License](#license)

## Introduction

This project demonstrates how to integrate OAuth2 Proxy with Keycloak as the authentication provider to secure an Azure Static Web App. OAuth2 Proxy acts as a reverse proxy, handling the authentication and authorization of requests before they reach the web application.

## Prerequisites

- **Azure Subscription**: An active Azure subscription is required to deploy the Static Web App.
- **Keycloak**: A running instance of Keycloak configured as the identity provider.
- **Docker compose**: For running OAuth2 Proxy locally or in a containerized environment.

## Architecture

The architecture for this setup includes the following components:

1. **Keycloak**: Identity provider for user authentication.
2. **OAuth2 Proxy**: Acts as a reverse proxy, authenticating requests against Keycloak before passing them to the Azure Static Web App.
3. **Azure Static Web App**: Hosts the static content of the web application.

```plaintext
User -> OAuth2 Proxy -> Keycloak -> OAuth2 Proxy -> Azure Static Web App
