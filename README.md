
# 🌐 SubdomainRegistrar

The `SubdomainRegistrar` contract allows users to register subdomains under a specified parent node. The registration process involves setting a fee, transferring ownership, and configuring various parameters such as resolver and expiry.

## Features ✨

- **Register Subdomains**: Users can register subdomains by paying a registration fee.
- **Set Subnode Record**: The contract interacts with the `INameWrapper` interface to set the subnode record.
- **Adjustable Registration Fee**: The owner can set and update the registration fee.
- **Configurable Fee Recipient**: The owner can set and update the address that receives the registration fees.

## Deployment 🚀

To deploy the `SubdomainRegistrar` contract, provide the following parameters:
- `_nameWrapper`: The address of the `INameWrapper` contract.
- `_resolver`: The address of the resolver.
- `_parentNode`: The parent node under which subdomains will be registered.
- `_registrationFee`: The initial registration fee.
- `_feeRecipient`: The address that will receive the registration fees.

## Usage 📘

1. **Register a Subdomain**:
    - Call the `register` function with the desired subdomain label and pay the registration fee.

2. **Set Registration Fee** (Owner only):
    - Call the `setRegistrationFee` function with the new fee amount.

3. **Set Fee Recipient** (Owner only):
    - Call the `setFeeRecipient` function with the new recipient address.

## Prerequisites ⚠️
1. **Lock the ENS Parent Name**: Ensure that the ENS parent name is locked so it is imposssible to unwrap it.
2. **Set Approval for All**: The contract's address must be set as ApprovedForAll on the nameWrapper contract.

## License 📜

This project is licensed under the MIT License.
