# Node - Play Recording How-To Guide

This project serves as a guide to help you build an application with FreeClimb. View this how-to guide on [FreeClimb.com](https://docs.freeclimb.com/docs/play-a-recording#section-nodejs). Specifically, the project will:

- Play a recording to a caller during a call.

## Setting up your new app within your FreeClimb account

To get started using a FreeClimb account, follow the instructions [here](https://docs.freeclimb.com/docs/getting-started-with-freeclimb).

## Setting up the how-to guide

1. Install the node packages necessary using command:

   ```bash
   $ yarn install
   ```

2. Configure environment variables (this how-to guide uses the [dotenv package](https://www.npmjs.com/package/dotenv)).

   | ENV VARIABLE   | DESCRIPTION                                                                                                                           |
   | -------------- | ------------------------------------------------------------------------------------------------------------------------------------- |
   | ACCOUNT_ID     | Account ID which can be found under [API credentials](https://www.freeclimb.com/dashboard/portal/account/authentication) in Dashboard |
   | API_KEY        | API key which can be found under [API credentials](https://www.freeclimb.com/dashboard/portal/account/authentication) in Dashboard    |
   | APPLICATION_ID | Appliction IDs can be found under [Apps](https://www.freeclimb.com/dashboard/portal/applications)                                     |
   | HOST           | The url of where your app is beiing hosted (e.g. yourHostedApp.com)                                                                   |

3. Provide a value for the variables `to`, `from`, and `recordingUrl` in playARecording.js. The `to` number is any phone number you wish to call. This number must be [verified](https://docs.freeclimb.com/docs/using-your-trial-account#section-verifying-outbound-numbers) (for trial users) and in E.164 format. `from` is a FreeClimb number that makes the call ([Incoming Numbers](https://www.freeclimb.com/dashboard/portal/numbers)). `recordingUrl` is a url where FreeClimb can download a recording to play. The recording must be [formatted correclty](https://docs.freeclimb.com/reference/interactive-voice-response-ivr#play) to work with FreeClimb. Recordings made by FreeClimb during other calls can be played by using the url provided in the [recordings page](https://www.freeclimb.com/dashboard/portal/recordings).

## Runnning the how-to guide

1. Run the application using command:

   ```bash
   $ node playARecording.js
   ```

## Getting help

If you are experiencing difficulties, [contact support](https://freeclimb.com/support).
