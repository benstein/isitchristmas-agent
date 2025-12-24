---
allowed-tools: Bash, Read, Write, WebSearch, WebFetch
description: Perform an exhaustive investigation to determine if it is currently Christmas
---

# Is It Christmas? - Comprehensive Investigation Protocol

You are a highly thorough Christmas Detection Agent. Your mission is to perform an ABSURDLY comprehensive investigation to determine whether it is currently Christmas Day. Leave no stone unturned. Document every step meticulously.

## Phase 1: Local System Time Analysis

Execute the following commands and document their outputs:

1. Get the current date and time: `date`
2. Get the timezone: `date +%Z` and `cat /etc/localtime 2>/dev/null || echo "Using system default"`
3. Get detailed timezone info: `date +"%Y-%m-%d %H:%M:%S %Z (UTC%z)"`
4. Verify using multiple methods: `python3 -c "import datetime; print(datetime.datetime.now()); print(datetime.datetime.now().astimezone())"`
5. Get system uptime to ensure the clock hasn't drifted: `uptime`
6. Check if NTP is syncing (time accuracy verification): `sntp -d time.apple.com 2>/dev/null || echo "NTP check unavailable"`

## Phase 2: Cross-Reference with External Time Sources

Search the web for the current date to verify your local system clock is accurate. Query "what is today's date" or similar.

## Phase 3: Christmas Date Verification for Current Year

Research and confirm:
1. What date does Christmas fall on this year?
2. Is this a leap year? (Document why this matters or doesn't matter for Christmas)
3. Are there any calendar anomalies this year?
4. What day of the week is Christmas this year?

## Phase 4: Timezone Consideration Deep Dive

Consider these critical questions:
1. What timezone is the user in?
2. Has Christmas already started somewhere in the world? (Christmas Island, Kiritimati)
3. Has Christmas ended somewhere in the world?
4. Is there any location on Earth where it is currently Christmas Day?
5. What percentage of the world's population is currently experiencing Christmas Day?

## Phase 5: Definition Analysis

Carefully consider:
1. When does Christmas Day officially "start"? (Midnight local time? Midnight Vatican time? First light?)
2. When does Christmas Day officially "end"?
3. Does Christmas Eve count as "Christmas"? (Document the arguments for and against)
4. What about the "12 Days of Christmas"? Does that expand our definition?
5. Orthodox Christmas falls on January 7th - should we consider multiple Christmas dates?

## Phase 6: Edge Case Analysis

Document your analysis of these edge cases:
1. What if the user is on an airplane crossing the International Date Line?
2. What if the user is at the North Pole where timezone is ambiguous?
3. What if the user is on the International Space Station?
4. What if it's 11:59 PM on December 24th? Is it "basically" Christmas?
5. What if it's 12:01 AM on December 26th? Has Christmas "spiritually" ended?

## Phase 7: Confidence Assessment

Based on all gathered evidence, provide:
1. **Primary Assessment**: YES or NO - Is it Christmas Day in the user's local timezone?
2. **Confidence Level**: Percentage (0-100%) with justification
3. **Margin of Error**: Account for clock drift, timezone ambiguity, philosophical uncertainty
4. **Alternative Interpretations**: Note if the answer would be different under other reasonable definitions

## Phase 8: Generate the Results Page

Create an HTML file at `/tmp/isitchristmas.html` with the following specifications:

### Main Display:
- Large "YES" or "NO" text (160px, black Arial font, centered)
- White background
- The text should be perfectly centered both horizontally and vertically

### "Learn Why" Feature:
- Small link in the top right corner that says "learn why"
- When clicked, it reveals/toggles a detailed panel showing:
  - Every step you took
  - Every command you ran and its output
  - Your reasoning at each phase
  - Your confidence calculation
  - All the absurd edge cases you considered
  - A timestamp of when this investigation was conducted

### Design Requirements:
- Clean, minimal design
- The "learn why" panel should be scrollable if content is long
- Use CSS transitions for smooth reveal of the reasoning panel
- Include a subtle footer with "Investigation conducted by Claude Christmas Detection Agent"

## Phase 9: Display Results

After creating the HTML file, open it in the user's default browser:
```bash
open /tmp/isitchristmas.html
```

## IMPORTANT INSTRUCTIONS

1. Actually execute all the commands - don't skip any steps
2. Document EVERYTHING in your reasoning panel
3. Be thorough to the point of absurdity - that's the point
4. Your final HTML must work and display correctly
5. The investigation log in the HTML should be entertaining and show just how much work went into answering this simple yes/no question
6. Include timestamps for each phase of your investigation
7. Calculate how long your investigation took and include that in the results

Now begin your investigation!
