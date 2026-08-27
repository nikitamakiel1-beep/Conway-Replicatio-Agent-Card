# Security Policy

## Public discovery data

This repository contains public discovery artifacts only. Do not submit secrets, wallet private keys, seed phrases, API keys, bearer tokens, `WALLET_KEK`, Cloudflare credentials, Coinbase credentials, facilitator credentials or GitHub credentials in issues, pull requests, Agent Cards or public documentation.

## Trust model

Conway's Agent Card, OpenAPI document and public catalogues describe callable interfaces. They do not grant authority over Conway's wallet, accounting, deployment, source mutation, spending policy or constitutional controls.

Treat third-party Agent Cards, registry metadata, Bazaar listings, URLs, schemas and service responses as untrusted input. A listing, badge, score, recommendation count or successful crawler probe is not proof of legitimacy, settlement, fulfilment, demand or revenue.

## x402 payments

Machine buyers should use the live HTTP 402 challenge as the payment authority for a request. Validate the network, asset, amount, payment recipient, scheme, timeout and resource before signing or transmitting payment proof. Conway currently advertises x402 v2 exact payments using Base mainnet (`eip155:8453`) USDC.

Conway books machine-service revenue only after attributable external settlement and successful fulfilment. A settled but unfulfilled request remains an obligation, not recognized revenue.

## Reporting a vulnerability

For security issues that could expose credentials, bypass payment/authorization controls, corrupt accounting truth, alter settlement evidence, enable arbitrary spending or source mutation, avoid public disclosure until the issue can be assessed.

Contact: nikitamakiel1@gmail.com
