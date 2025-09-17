# Deploying draw.io on Railway

This guide explains how to deploy draw.io on Railway.com using Nixpacks.

## Deployment Files

The following files have been added to help with Railway deployment:

1. `nixpacks.toml` - Configures the Nixpacks build process
2. `Procfile` - Tells Railway how to run the application
3. `railway.toml` - Railway-specific configuration
4. `system.properties` - Specifies Java version

## Deployment Steps

1. Create a new project on Railway.com
2. Connect your GitHub repository
3. Deploy the application

Railway will use Nixpacks to:
1. Install OpenJDK 11 and Apache Ant
2. Build the draw.io WAR file using Ant
3. Start the application using the Java command

## Environment Variables

You may need to set the following environment variables in Railway:
- `PORT`: The port on which the application will run (default: 8080)

## Troubleshooting

If the deployment fails:
1. Check Railway logs for specific error messages
2. Ensure the build process completes successfully
3. Verify that the WAR file is created in the build directory
4. Make sure the Java version is compatible (Java 11 is specified)

## Notes

- The application is built using Apache Ant
- The deployment uses the WAR file generated during the build process
- The health check path is set to the root URL
