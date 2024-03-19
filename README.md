<p align="center">
  <img width="100" src="https://imgur.com/3cw4DQr.png" alt="NetScan Security Logo" />
  <h2 align="center">NetScan Security</h2>
  <p align="center">Precision Scans, Real-time Defense</p>
</p>

# NetScan Security: Getting Started Guide

Welcome to NetScan Security! Follow these steps to set up your environment and start using NetScan Security to monitor and manage your network effectively.

## Prerequisites

Before getting started, ensure that you have the following prerequisites installed:

1. **Docker**: Install Docker on your server. You can use [wg-easy](https://github.com/wg-easy/wg-easy) to set up WireGuard VPN, which is supported by Docker.

## Step 1: Set Up WireGuard VPN

Follow the instructions in the [wg-easy](https://github.com/wg-easy/wg-easy) repository to install and configure WireGuard VPN on your server.

## Step 2: Create VPN Clients

Create VPN clients in the WireGuard VPN and store their details securely.

## Step 3: Install NetScan API

Install the NetScan API on the same server where WireGuard VPN is installed. After installation, visit the Swagger API documentation at `/docs` and add your admin user. This user will be required to log in to the dashboard later on.

Repository: [NetScan API](https://github.com/Netscan-Security/netscan-api)

## Step 4: Install NetScan AI API (Optional)

If you choose to use AI-driven features, install the NetScan AI API on the same server.

Repository: [NetScan AI API](https://github.com/Netscan-Security/netscan-ai)

## Step 5: Install and Run NetScan Dashboard

Install and run the NetScan Dashboard on the server. You can deploy it online on platforms like Vercel or host it on the same server.

Repository: [NetScan Dashboard](https://github.com/Netscan-Security/netscan-dashboard)

## Step 6: Update Environment Variables

Update the environment variables of the NetScan Agent with the credentials of the deployed APIs. Additionally, build an executable (exe) file to install on users' devices.

Repository: [NetScan Agent](https://github.com/Netscan-Security/netscan-agent)

## Step 7: Register New Users and Configure VPN Clients

1. In the NetScan Dashboard, register new users.
2. Assign an available IP address to each user, which was added when creating clients in the WireGuard VPN.
3. Download WireGuard from [here](https://www.wireguard.com/install/) and add the configuration of the client with the assigned IP address.
4. After connecting to the WireGuard app, users can run the NetScan Agent app and log in with the user details created in the dashboard.

That's it! You are now ready to start monitoring and managing your network with NetScan Security. If you encounter any issues or have feedback, don't hesitate to reach out to us for support.

## Note

This is a general overview to get started, but in each step, you should read instructions on the repository readme and be sure to keep the correct environment variables.

Our current demo is deployed as follows:
- VPN & APIs on a small 4GB 2-core CPU on AWS.
- Database: Supabase free tier connected using a Postgres connection string.
- Dashboard is deployed on Vercel.
  
Be sure to keep your VPN configs safe!
