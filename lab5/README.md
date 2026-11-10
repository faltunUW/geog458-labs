# Miami Vessel Map from 2021

## 1. Study Area and Dates

For this project, I selected the Miami, Florida area to visualize vessel movements using AIS data from April 9 to April 10, 2021. This is the time when COVID was at its peak and I was visiting Miami at that time. I was super shocked how relaxed they were around other people and I was wondered if its the same for the water traffic.

- **Study area:** Miami, Florida
- **Start date:** April 9, 2021
- **End date:** April 10, 2021
- **Data source:** [AccessAIS](https://marinecadastre.gov/accessais/)
- **Time zone:** Eastern Time (EDT/EST)

I selected Miami to study vessel movements in a coastal region with different types of maritime activity. I used a short, two-day period to keep the dataset manageable for processing and visualization.

I downloaded the AIS data from AccessAIS in CSV format and used the class Google Colab notebook to convert it into JSON files for my animated map. AccessAIS timestamps are in UTC, but my map displays the date and time in Miami's local time (EDT during the selected dates).

## 2. Interpretation

After examining the animated vessel map of Miami, I noticed several patterns in vessel movements, routes, and activity.

**Tanker vessels:** There was no tanker vessel data available during the selected period.

**Passenger vessels:** Longer passenger routes appeared mainly after midday. Most passenger vessels operated between mainland Miami and Miami Beach, while a few approached from the north, east of Miami Beach. Many vessels appeared to remain near one or two locations, making small circular movements rather than traveling long distances. This might indicate that they were local vessels operating within familiar areas.

**Cargo vessels:** I observed a few cargo vessels traveling from Miami toward open waters. However, some vessels near the canal appeared to make repeated circular movements rather than continuously entering or leaving the area. I also noticed vessels making small maneuvers in open waters instead of traveling directly toward a destination. One example occurred on April 10, 2021, at 11:44:24 EDT.

**Other vessels:** This category had the highest concentration of vessel activity and contributed the most to the crowded appearance of the map. I think this may be related to Miami's coastal location, where residents might use private boats for recreation or fishing. Since Miami is also a tourist destination, some of these vessels could be rentals. However, these are possible explanations rather than conclusions confirmed by the AIS data.

Overall, the map showed that vessel activity was not always about traveling between destinations. Some vessels remained in small areas, making repeated movements, while others followed longer routes toward open waters.

## 3. Feature Proposal for a Potential User

**Potential user:** Maritime traffic researcher

**User's task:** Analyze vessel traffic patterns and understand how maritime activity changes throughout the day.

**Proposed feature: Vessel Traffic Timeline**

I would propose adding an interactive timeline chart that shows the number of active vessels at different hours. The researcher could use this chart to identify busy and quiet periods, compare traffic between vessel categories, and select a particular time window to examine on the map.

I reviewed the [kepler.gl Time Playback Guide](https://docs.kepler.gl/docs/user-guides/h-playback), which demonstrates how a time distribution graph can be used alongside an animated map. This inspired my idea of adding a timeline that works with the existing time slider and vessel filters.

This feature would help researchers identify temporal patterns more easily instead of relying only on watching the animation. It could also help compare activity between different vessel types and times of day.

## Additional Features Implemented

In addition to the required features, I made two improvements to my map:

1. **All Vessels Filter:** I added a fifth dropdown option called "All Vessels," which displays all vessel categories simultaneously using their assigned colors.

2. **Vessel Color Coding:** I assigned a different color to each vessel category:
   - Orange — Passenger
   - Green — Cargo
   - Red — Tanker
   - Purple — Other Vessels

## AI Disclosure

I used ChatGPT 6 (Medium) to help code two additional features: the "All Vessels" dropdown option and the vessel color-coding system. AI also helped me organize and improve the wording of my README. However, all observations, interpretations, and explanations are based on my own understanding and analysis of the map. I provided the original content, and AI helped structure and present it more clearly.