# Infinity Node Stack - Downloads

This project is part of a collection of Portainer stacks designed for a home server environment. The Downloads stack focuses on managing various download-related services and tasks.

## Overview

The Downloads stack provides a set of containerized services for handling different types of downloads, file management, and related automation tasks. It's designed to work seamlessly with other stacks in the Infinity Node ecosystem.

## Components

The stack includes the following services:

- **NZBGet**: Usenet downloader for efficient binary downloads
- **Deluge**: Feature-rich BitTorrent client with web interface
- **NordLynx VPN**: Secure VPN connection for download services

All download services (NZBGet and Deluge) are configured to route their traffic through the NordLynx VPN container for enhanced privacy and security.

## Configuration

Each service is configured with appropriate environment variables and volume mounts. The stack uses Docker Compose for orchestration and is designed to be deployed through Portainer.

### Required Environment Variables

- `PUID`: User ID for file permissions
- `PGID`: Group ID for file permissions
- `TZ`: Timezone
- `STACKS_PATH`: Base path for configuration files
- `INCOMPLETE_PATH`: Path for incomplete downloads
- `COMPLETE_PATH`: Path for completed downloads
- `NZBGET_USER`: NZBGet web interface username
- `NZBGET_PASS`: NZBGet web interface password
- `PRIVATE_KEY`: NordVPN private key
- `NET_LOCAL`: Local network configuration

## Prerequisites

- Docker and Docker Compose installed
- Portainer instance running
- Proper network configuration
- Sufficient storage space for downloads
- NordVPN account with private key

## Deployment

1. Clone this repository
2. Configure environment variables as needed
3. Deploy through Portainer using the provided stack configuration
