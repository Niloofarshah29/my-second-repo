# my-second-repo
for testing
import requests

API_KEY = "your_api_key"  # از سایت OpenWeather بگیر
city = "London"
url = f"http://api.openweathermap.org/data/2.5/weather?q={city}&appid={API_KEY}&units=metric"

response = requests.get(url).json()

print(f"City: {response['name']}")
print(f"Temperature: {response['main']['temp']}°C")
print(f"Weather: {response['weather'][0]['description']}")
