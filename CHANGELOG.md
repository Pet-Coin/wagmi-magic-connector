# @everipedia/wagmi-magic-connector

## 0.7.1

### Patch Changes

- b19d703: - `magic.user.disconnect()` is no available for Magic Connect, relying on local storage instead
  - Require email input for `connect()` flow to continue once modal is open. Otherwise the Magic Connect
    modals appears even if the user quits the process manually.

## 0.7.0

### Minor Changes

- 38dd8cc: ### Major

  - Creation of two classes `MagicAuthConnector` & `MagicConnectConnector`
    - `MagicAuthConnector`: Connector integrating with [Magic Auth](https://magic.link/docs/auth/overview). Most of the code comes from previous implementation
    - `MagicConnectConnector`: Connector integrating with [Magic Connect](https://magic.link/docs/connect/overview).
  - Made `MagicConnector` an abstract class containing shared logic between `MagicAuthConnector` & `MagicConnectConnector`
  - Renamed `options.additionalMagicOptions` to `options.magicSdkConfiguration`, which seemed to be a clearer name
  - Renamed `enableSMSlogin` to `enableSMSLogin`
  - Updated documentation in README to fit changes

  ### Minor

  - Fixed some typos in the README
  - Fixed Rainbow Kit example in the README and specified that `options.magicSdkConfiguration.network.chainId` needs to be specified. This comes from the fact that in their most recent version Rainbow Kit makes a `getChainId()` call on the connector before calling the `connect()` method.
  - Fixed typo in enableSMSlogin -> enableSMSLogin

## 0.6.5

### Patch Changes

- d5c95eb: updates email regex to take +

## 0.6.4

### Patch Changes

- d49c203: updated dependancies to latest versions

## 0.6.3

### Patch Changes

- 4288ba5: Prevent changing chainId type from number to string

## 0.6.2

### Patch Changes

- 127b67e: added implementation for getChainId

## 0.6.1

### Patch Changes

- 85cc525: Fix Custom header images not working

## 0.6.0

### Minor Changes

- 1001fbf: - Made dark mode styles overridable by converting darkmode styles to pure css
  - Fixed OAuth provider buttons not following the order they are passed in
  - Redesigned Modal look and feel
  - Changed Github and Default header icons

## 0.5.0

### Minor Changes

- 075cf2b: Made Email Authentication Optional. To remove the email authentication requirement, you can set `enableEmailLogin` to `false` in connector configuration's options object.

## 0.4.1

### Patch Changes

- 7ab9877: fixes animations not working while opening and closing modal
