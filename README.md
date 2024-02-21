# Instructions

## Pre-requisites

Before running the Honeygain Docker image, please read the Terms of Use carefully. You can get the current copy of ToU by running the following command:

```bash
docker run honeygain/honeygain -tou-get
```

### Starting the Honeygain Container
You can start the Honeygain container by running the following command:

```bash
docker run honeygain/honeygain -tou-accept -email ACCOUNT_EMAIL -pass ACCOUNT_PASSWORD -device DEVICE_NAME
```

Or, to always restart the container:

```bash
docker run --restart=always honeygain/honeygain -tou-accept -email ${email} -pass ${pass} -device honeygain_docker
```

**Note:** The -device parameter is mandatory. It is used to uniquely identify this run among other devices in your devices list. You should use a different DEVICE_NAME for every Docker container you start within the same account. You can't run multiple instances of Honeygain CLI application with the same DEVICE_NAME at the same time.

### Post-Installation
After the application is started, you should see your new device running on your dashboard.

Also, note that the Honeygain CLI application complies with the same usage restrictions as regular Honeygain applications (e.g. the limit of devices per IP address, network type checks and others). Breaching Honeygain's Terms of Use will lead to suspension of your account.
