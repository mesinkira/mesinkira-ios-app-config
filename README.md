# Mesinkira iOS App Update Configuration

This repository hosts the `update.json` used by the Mesinkira iOS app to manage forced and optional updates.

## Field Descriptions

- **minimum_build**:  
  Any app build less than this number will be **forced to update**. Users cannot continue without updating.

- **latest_build**:  
  Any app build less than this number will be given a **soft update prompt**, with the option to **Update Now** or **Later**.

- **store_url**:  
  The App Store URL of the app. Opened when the user taps **Update**. (shall remain unchanged)

## Update Guidelines
- Every time a new build is published to TestFlight or App Store, update the latest_build field accordingly.
- Update the minimum_build only when you want to force older builds to update.

## Example
- Current TestFlight build: 120
- Soft update prompt for builds < 120
- Forced update for builds < 100

## JSON Example Structure

```json
{
  "ios": {
    "minimum_build": 100,
    "latest_build": 120,
    "store_url": "itms-apps://itunes.apple.com/app/id6465033213"
  }
}
