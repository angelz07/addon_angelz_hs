# Crypto Portfolio Addon

## Description

This addon allows you to manage your cryptocurrency portfolio within Home Assistant.

## Installation

1. Add the repository to your Home Assistant instance.
2. Install the Crypto Portfolio addon.
3. Start the addon.

## Configuration

To integrate this addon with Home Assistant, you need to add the following configuration to your `configuration.yaml` file. This will allow you to add, delete, and update transactions via Home Assistant services.

### Step 1: Add REST commands

Copy the following configuration into your `configuration.yaml` file:

```yaml
rest_command:
  add_transaction:
    url: 'http://localhost:5000/transaction'
    method: POST
    headers:
      Content-Type: application/json
    payload: '{"crypto_name": "{{ crypto_name }}", "quantity": {{ quantity }}, "price_usd": {{ price_usd }}, "transaction_type": "{{ transaction_type }}", "location": "{{ location }}", "date": "{{ date }}"}'
    content_type: 'application/json'

  delete_transaction:
    url: 'http://localhost:5000/transaction/{{ transaction_id }}'
    method: DELETE

  update_transaction:
    url: 'http://localhost:5000/transaction/{{ transaction_id }}'
    method: PUT
    headers:
      Content-Type: application/json
    payload: '{"crypto_name": "{{ crypto_name }}", "quantity": {{ quantity }}, "price_usd": {{ price_usd }}, "transaction_type": "{{ transaction_type }}", "location": "{{ location }}", "date": "{{ date }}"}'
    content_type: 'application/json'