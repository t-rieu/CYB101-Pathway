import requests
import json

def get_cves(ip_address):
  """Fetches vulnerability information from Shodan and extracts CVEs."""
  url = f"https://internetdb.shodan.io/{ip_address}"
  response = requests.get(url)

  # Basic error handling for failed requests
  if response.status_code != 200:
      print(f"Error fetching data for {ip_address}: {response.status_code}")
      return []

  data = json.loads(response.text)

  try:
    cves = data['vulns']
    return cves
  except KeyError:
    print(f"No CVEs found for {ip_address}")
    return []

if __name__ == "__main__":
  while True:
    ip_address = input("Enter the IP Address: ")
    cves = get_cves(ip_address)
    if cves:
      print(f"CVEs for {ip_address}:{cves}")

    cont = input("Do you want to enter another IP address? [Y] or [N]: ").strip().upper()
    if cont != 'Y':
      print("Quitting.")
      break
