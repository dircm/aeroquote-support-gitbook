# Custom Routes & Route Library

Visual route planning for scenic flights, tour circuits, and complex multi-stop itineraries.

{% hint style="info" %}
**Aeroquote tip:** Custom routes are ideal for scenic/sightseeing operators who fly the same circuit regularly. Save a route once, then load it into any enquiry or quote with a single click.
{% endhint %}

### What are Custom Routes?

Custom routes let you define a flight path using waypoints on a map, rather than relying on the straight-line distance between two airports. This is especially useful for:

* **Scenic and sightseeing flights** that depart and return to the same airport
* **Tour circuits** with a specific path over landmarks or coastline
* **Multi-turn routes** that follow a particular corridor

When a custom route is attached to a flight, AeroQuote calculates the flight duration and distance based on the actual route path — not just the airport-to-airport distance.

### Route Library

The Route Library lets you save commonly flown routes so they can be reused across enquiries and quotes.

<figure><img src="../../.gitbook/assets/Screenshot 2026-02-26 at 9.32.22 pm.png" alt=""><figcaption></figcaption></figure>

#### Creating a Route

1. Navigate to **Custom Items → Custom Routes** from the sidebar
2. Click **Add Route**
3. Give your route a descriptive name (e.g. "Sydney Harbour Scenic" or "Great Ocean Road Tour")
4. Set the **Departure Airport** and **Arrival Airport**
   * For scenic flights that return to the same airport, set both to the same location
5. Use the interactive map to plot your route waypoints
   * Click on the map to add waypoints
   * Drag waypoints to adjust the path
   * The total route distance updates automatically as you edit
6. Click **Save**

{% embed url="https://screen.studio/share/o6b5g1d5" %}

{% hint style="info" %}
**Aeroquote tip:** You can also create routes with custom airports. This is useful if your operation uses a private airstrip or helipad that isn't in the standard airport database.
{% endhint %}

#### Editing a Saved Route

1. Navigate to **Custom Items → Custom Routes**
2. Click on the route you want to edit
3. Adjust waypoints, airports, or the route name as needed
4. Click **Save** to update

Any future enquiries or quotes that load this route will use the updated version. Existing quotes that have already been generated are not affected.

### Loading a Route into an Request

When creating a new enquiry, you can load a saved route instead of manually selecting departure and arrival airports.

<figure><img src="../../.gitbook/assets/Screenshot 2026-02-26 at 9.35.58 pm.png" alt=""><figcaption></figcaption></figure>

1. On the Enquiry page, click **Load Route** (next to "Add Flight" and "Add Return Flight")
2. Search for your route by name
3. Select the route from the results

The departure and arrival airports are automatically filled in from the route, and a new flight segment is created. If there is an empty flight row (no airports selected), the loaded route replaces it rather than creating a duplicate.

{% hint style="info" %}
**Aeroquote tip:** You can mix loaded routes with manually entered flights in the same enquiry. For example, load a scenic route for the charter leg and manually add a positioning flight.
{% endhint %}

### Loading a Route into the Quote Builder

The Quote Builder also supports loading routes, following the same process:

1. In the charter flights step, click **Load Route**
2. Search and select your route
3. The flight segment is created with the route's airports pre-filled

### How Duration and Distance are Calculated

When a custom route is loaded:

* **Distance** is calculated by summing the straight-line distance between each consecutive waypoint along the route (using the haversine formula)
* **Duration** is derived from the total route distance and the selected aircraft's performance profile

This means a scenic flight that departs and returns to the same airport will have an accurate duration based on the actual route flown, rather than showing zero.

### Frequently Asked Questions

#### Can I use the same route for different aircraft?

Yes. The route defines the flight path — duration and fuel calculations are recalculated based on whichever aircraft is selected.

#### What happens if I update a route in the library after generating a quote?

Existing quotes keep the route as it was when the quote was generated. Only new enquiries and quotes will use the updated route.

#### Can I edit a route after it's been loaded into a quote?

Yes. Once a quote is generated, you can open the flight item and use the route editor to modify the route for that specific flight. Changes made here do not affect the Route Library version.

#### Do custom routes work with Request For Quotes ?

Yes. When you send a Request for Quote to an external operator, the custom route shape is displayed on the map — so the receiving operator can see exactly what flight route is being requested of them.
