# Water-quality-monitor-
Water Quality Monitoring System is used to check the quality of water by monitoring parameters such as pH, turbidity, and temperature. The Python program analyzes the sensor values and displays whether the water is Safe, Moderate, or Unsafe for use.
# Water Quality Monitoring System

print("===== WATER QUALITY MONITORING SYSTEM =====")

ph = float(input("Enter pH value: "))
turbidity = float(input("Enter turbidity value (NTU): "))
temperature = float(input("Enter water temperature (°C): "))

print("\n----- Water Quality Report -----")
print("pH:", ph)
print("Turbidity:", turbidity, "NTU")
print("Temperature:", temperature, "°C")

# Checking water quality
if 6.5 <= ph <= 8.5 and turbidity <= 5:
    status = "GOOD"
elif 6.0 <= ph <= 9.0 and turbidity <= 10:
    status = "MODERATE"
else:
    status = "POOR"

print("Water Quality:", status)

if status == "GOOD":
    print("Water quality is within the selected limits.")
elif status == "MODERATE":
    print("Warning: Water quality needs attention.")
else:
    print("Alert: Water quality is poor.")
