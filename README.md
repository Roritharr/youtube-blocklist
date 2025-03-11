# Pi-hole YouTube Blocklist

This blocklist is designed to completely block YouTube access across your network using Pi-hole.

## Purpose
- Fully block YouTube domains to prevent access, useful for parental control or productivity enhancement.

## Included Domains
- YouTube primary domains
- Googlevideo domains
- Associated YouTube CDN and service domains

## Usage with Pi-hole

1. **Log into Pi-hole Admin Interface**
   - Visit `http://pi.hole/admin/`

2. **Add Blocklist**
   - Navigate to **Group Management** → **Adlists**.
   - Click "Add a new adlist" and insert the URL to the raw hosts file provided.

3. **Update Pi-hole**
   - Run the following commands:
```
pihole -g
sudo pihole restartdns
```

## Included Domains
- Main YouTube domains
- Regional YouTube domains
- YouTube CDN domains (e.g., `googlevideo.com`, `ytimg.com`)

## Example Entry Format
```
0.0.0.0 youtube.com
0.0.0.0 youtu.be
0.0.0.0 googlevideo.com
```

## Notes
- Ensure Pi-hole is your sole DNS provider to avoid DNS bypasses.
- Monitor Pi-hole query logs to identify additional domains to block.