
🌩️ Ultra Advanced Dynamic Weather System for QB-Core

A fully dynamic, immersive, multi-zone, disaster-capable weather engine for FiveM.

🚀 Overview

The Ultra Advanced Weather System transforms the static FiveM environment into a living, breathing climate simulation.
Featuring moving storms, hurricanes, blackouts, seasonal weather, HAARP weather control, and dynamic zone-based climates, this script brings unparalleled immersion to any QB-Core server.

Weather now influences:

RP events

Jobs & economy

Emergency services

Driving & handling

Visibility

Player survival

Power grid behavior

This is one of the most advanced FiveM weather systems ever created.

🌦️ Features
🌀 Dynamic Storm Systems

Storm cells that move across the map

Each with direction, speed, strength, and lifetime

Realistic lightning, thunder, and wind effects

🌪️ Seasonal Hurricanes

Form offshore and drift inland

Cause extreme weather, flooding visuals, strong winds

Trigger automatic server-wide alerts

Increase blackout chance

🗺️ Multi-Zone Weather System

Different locations have different climates:

Zone	Climate Type	Notes
City (LS)	Balanced	Fog, storms, rain
Sandy Shores	Hot/Dry	Dust storms, low rain
Paleto Bay	Cold/Wet	Snow in winter, heavy rain

Each player sees weather based on their current zone, not globally.

❄ Seasonal Weather Engine

Automatic rotation through:

Summer

Autumn

Winter

Spring

Each season affects:

Temperature

Rain chance

Storm intensity

Snow availability

Hurricane chance

Season changes trigger news broadcasts.

⚡ Power Grid & Blackouts

A realistic, zone-based electrical grid system:

Storms cause power outages

Hurricanes dramatically increase failure likelihood

Lights, street lamps, and neon signs shut down

Automatic timed restoration

Utilities job support via:

/fixpower


Blackouts apply client-side visual effects to increase realism.

🛰️ HAARP Weather Control System

Perfect for missions, RP events, or faction use.

Commands:
/haarpstorm [zone]  -- Force a major storm
/haarpclear          -- Remove all storms & hurricanes


Can also be triggered through scripts or missions.

📺 Weather News Flash System

Automatic RP-friendly alerts:

Storm warnings

Hurricane formation

Blackouts

Power restoration

Season announcements

Global weather updates

Integrates cleanly with:

qb-phone

Dispatch systems

TV broadcasts

Radio scripts

📡 Weather Radar (PD/Dispatch Tool)

Toggle with:

/weatherradar  (F7)


Displays a real-time radar-style interface.
Fully expandable into a full NUI radar UI.

📺 Weather TV Channel

Toggle with:

/weathertv  (F8)


Displays a simulated “Weather Channel Live” broadcast ticker.

☔ Environmental Effects

Reduced traction in rain

Severe grip loss in storms

Snow vehicle & pedestrian tracks

Wind gust simulation

Rain intensity synced

Footstep/vehicle snow trails

☂ Umbrella System

Supports a usable umbrella item that players can toggle.
Includes prop attachment and animation-ready hooks.

📂 Resource Structure
qb-advancedweather-ultra/
│
├── fxmanifest.lua
├── config.lua
│
├── server/
│   ├── weather_core.lua
│   ├── systems.lua
│   ├── zones.lua
│   ├── seasons.lua
│   ├── grid.lua
│   ├── newsflash.lua
│   └── haarp.lua
│
└── client/
    ├── apply_weather.lua
    ├── effects.lua
    ├── radar.lua
    ├── tv.lua
    └── items.lua

🛠 Installation

Place folder into:

resources/[qb]/qb-advancedweather-ultra


Add to server.cfg:

ensure qb-advancedweather-ultra


Add umbrella item (optional):

["umbrella"] = {
    name = "umbrella",
    label = "Umbrella",
    weight = 200,
    type = "item",
    image = "umbrella.png",
    usable = true,
    shouldClose = true,
    description = "Stay dry!"
}


Add umbrella usable callback:

QBCore.Functions.CreateUseableItem("umbrella", function(source, item)
    TriggerClientEvent('qb-advancedweather-ultra:client:UseUmbrella', source)
end)

🧪 Testing Commands
Force severe storm
/haarpstorm city

Clear weather
/haarpclear

Toggle radar
/weatherradar

Toggle TV weather
/weathertv

Restore power manually
/fixpower

📜 MIT License
MIT License

Copyright (c) 2025 Moorgaming

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the “Software”), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED “AS IS”, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
