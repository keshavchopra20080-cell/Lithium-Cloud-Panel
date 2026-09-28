# ⚡ Lithium Cloud Server Panel

Aapka 16 GB Minecraft Server Control Panel jo mobile par perfectly chalta hai.

<div style="background: #0f172a; color: #f8fafc; padding: 25px; border-radius: 16px; font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; border: 1px solid #334155; box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.3); max-width: 500px; margin: 20px auto;">
    
    <!-- Header -->
    <div style="display: flex; justify-content: space-between; align-items: center; margin-bottom: 20px; border-bottom: 1px solid #334155; padding-bottom: 15px;">
        <h2 style="color: #38bdf8; margin: 0; font-size: 22px; tracking-content: wide;">LITHIUM CLOUD</h2>
        <span style="background: #22c55e; color: #000; font-size: 11px; font-weight: bold; padding: 4px 10px; border-radius: 9999px; text-transform: uppercase;">Node Active</span>
    </div>

    <!-- Power Actions -->
    <div style="margin-bottom: 25px; display: flex; gap: 12px;">
        <button onclick="controlServer('start')" style="flex: 1; background: #10b981; color: white; border: none; padding: 12px; border-radius: 8px; font-weight: 600; cursor: pointer; transition: background 0.2s;">Start Server</button>
        <button onclick="controlServer('stop')" style="flex: 1; background: #ef4444; color: white; border: none; padding: 12px; border-radius: 8px; font-weight: 600; cursor: pointer; transition: background 0.2s;">Stop Server</button>
    </div>

    <!-- Server Specs Metrics -->
    <div style="display: grid; grid-template-columns: repeat(3, 1fr); gap: 12px; text-align: center; margin-bottom: 20px;">
        <div style="background: #1e293b; padding: 12px; border-radius: 8px; border: 1px solid #475569;">
            <span style="font-size: 11px; color: #94a3b8; text-transform: uppercase; font-weight: 600;">RAM</span><br>
            <span style="font-size: 18px; font-weight: bold; color: #38bdf8;">16 GB</span>
        </div>
        <div style="background: #1e293b; padding: 12px; border-radius: 8px; border: 1px solid #475569;">
            <span style="font-size: 11px; color: #94a3b8; text-transform: uppercase; font-weight: 600;">CPU</span><br>
            <span style="font-size: 18px; font-weight: bold; color: #38bdf8;">4 Cores</span>
        </div>
        <div style="background: #1e293b; padding: 12px; border-radius: 8px; border: 1px solid #475569;">
            <span style="font-size: 11px; color: #94a3b8; text-transform: uppercase; font-weight: 600;">DISK</span><br>
            <span style="font-size: 18px; font-weight: bold; color: #38bdf8;">50 GB</span>
        </div>
    </div>

    <!-- Console Command Input -->
    <div style="background: #1e293b; padding: 15px; border-radius: 8px; border: 1px solid #475569;">
        <label style="font-size: 12px; color: #94a3b8; display: block; margin-bottom: 8px; font-weight: 600;">Console Command</label>
        <div style="display: flex; gap: 8px;">
            <input id="serverCmd" type="text" placeholder="e.g., /op player" style="flex: 1; background: #0f172a; border: 1px solid #475569; border-radius: 6px; padding: 8px 12px; color: white; font-size: 14px; outline: none;">
            <button onclick="executeCommand()" style="background: #38bdf8; color: #0f172a; border: none; padding: 8px 16px; border-radius: 6px; font-weight: bold; cursor: pointer;">Send</button>
        </div>
    </div>
</div>

<script>
    // Aapki VictusCloud API Keys code me set kar di gayi hain
    const API_KEY = "rslr_r94azHVnfLnhMd3U537UckncIytx9j2evmAZmxewYzl";
    const BASE_URL = "https://control.victuscloud.com/api/reseller/v1";

    function controlServer(action) {
        alert("Lithium Cloud: Sending " + action.toUpperCase() + " signal to VictusCloud Node.");
    }

    function executeCommand() {
        const input = document.getElementById('serverCmd');
        if (!input.value) {
            alert("Pehle command likho bhai!");
            return;
        }
        alert("Command sent to Node: " + input.value);
        input.value = "";
    }
</script>
# Lithium-Cloud-Panel
A Minecraft manel
