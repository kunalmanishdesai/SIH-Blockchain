# jute asset Tracking with Blockchain and IoT

In this pattern, we will be creating a local Hyperledger Fabric network using the IBM Blockchain Platform extension for VSCode which makes it easy to start developing smart contracts. 

The solution that we will be creating is a jute asset lifecycle and tracking solution that keeps a record of the jute asset from creation to deletion. Also, we will be creating and managing jute asset leases which keep track of the lease terms in a lease agreement such as end date, price, and deposit amount. 

For the IoT integration, we will be leveraging the IBM Watson IoT Platform to handle device scanning at various locations as the jute asset is being transferred. Instead of having an actual physical device, we will be creating a web app pretending to be a device which will trigger these scans and notify a locally node.js app to invoke the updatejute assetLocation transaction.

After completing this pattern you will understand how to:
- Deploy smart contracts to a local Hyperledger Fabric network
- Create a simulated IoT device using the IBM Watson IoT Platform and Node-Red
- Connect to a Hyperledger Fabric application using the Fabric SDK for Node.js
- Publish IoT events to the ledger on a device event such as a scan

# Flow
1. The smart contract is deployed to a local Hyperledger Fabric network via the IBM Blockchain Platform extension for VS Code.
2. As the jute jute asset is moved from place to place it is scanned via RFID or barcode by an IoT device. In this pattern, the device is simulated.
3. The IoT device publishes an event notification to the IBM Watson IoT Platform, which then notifies all listening applications that a scan has taken place.
4. An application listening to the IBM Watson IoT Platform for scanning events then invokes a transfer transaction.
5. The location of the jute asset is updated in the ledger automatically.

