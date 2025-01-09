import requests

# URL to send the POST request to
url = 'https://api.tiktok.com/aweme/v1/user/'

# Data to be sent in the POST request
data = {
    'user_id': '123456789',
    'sec_user_id': 'abcdefghijklmnopqrstuvwxyz',
    'count': '10'
}

# Send the POST request
response = requests.post(url, data=data)

# Check if the request was successful
if response.status_code == 200:
    # Retrieve the response data
    response_data = response.json()
    print(response_data)
else:
    print('Request failed with status code:', response.status_code)
