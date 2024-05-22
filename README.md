<body>
    <h1>Splunk Lab Walkthrough: Exploring SPL</h1>
    <h2>Introduction</h2>
    <p>This guide will walk you through the TryHackMe Splunk lab, teaching you how to explore and use Splunk Processing Language (SPL). Ensure you have access to TryHackMe and the necessary tools installed.</p>
  - <b><a href="https://tryhackme.com/r/room/splunkexploringspl">TryHackMe Splunk: Exploring SPL Lab</a></b>
    <h2>Prerequisites</h2>
    <ul>
        <li><strong>TryHackMe Account:</strong> Ensure you have an account on TryHackMe.</li>
        <li><strong>OpenVPN:</strong> Install and configure OpenVPN to connect to TryHackMe servers.</li>
    </ul>
    <h2>Steps</h2>
    <ol>
        <li><strong>Task 1/2 - Connect with the Lab</strong>
            <ul>
                <li><strong>Connect to TryHackMe:</strong>
                    <p>Download the VPN configuration file from TryHackMe and connect using OpenVPN:</p>
                    <pre><code>sudo openvpn --config your-vpn-config.ovpn</code></pre>
                </li>
                <li><strong>Launch the Machine:</strong>
                    <p>Start the machine in the TryHackMe lab.</p>
                    <p>Open a web browser and go to the IP address provided:</p>
                    <pre><code>https://&lt;ipaddress&gt;.p.thmlabs.com</code></pre>
                </li>
                <li><strong>Navigate to Windowslog Index:</strong>
                    <ul>
                        <li>Go to “Search & Reporting” on the left panel.</li>
                        <li>Select the "Data Summary" tab to see the host for answer 1.</li>
                    </ul>
                </li>
            </ul>
        </li>
        <li><strong>Task 3 - Search & Reporting App Overview</strong>
            <ul>
                <li><strong>Familiarize Yourself with the UI:</strong>
                    <p>Explore the Search & Reporting app interface.</p>
                </li>
                <li><strong>Identify the 7th Search:</strong>
                    <p>Open the Search History and identify the 7th search (excluding any searches you have performed).</p>
                </li>
                <li><strong>Find the Source IP:</strong>
                    <p>Run the following search:</p>
                    <pre><code>index="windowslogs"</code></pre>
                    <p>Change the time range to "All time".</p>
                    <p>In the JSON source code view, scroll down to the left tab and select “146 More Fields”.</p>
                    <p>Select the dropdown for SourceIP to find the source IP with the maximum entries.</p>
                </li>
            </ul>
        </li>
        <li><strong>Task 4 - Splunk Processing Language Overview</strong>
            <ul>
                <li><strong>Learn SPL:</strong>
                    <p>View the provided images to understand how to build queries using SPL.</p>
                </li>
            </ul>
        </li>
        <li><strong>Task 5 - Filtering the Results in SPL</strong>
            <ul>
                <li><strong>Explore Filtering Options:</strong>
                    <p>Use different filtering options such as Fields, Search, Dedup, and Rename to get the next two answers.</p>
                    <p>Refer to the screenshots for additional help.</p>
                </li>
            </ul>
        </li>
        <li><strong>Task 6 - SPL - Structuring the Search Results</strong>
            <ul>
                <li><strong>Use Structuring Commands:</strong>
                    <p>SPL provides commands to structure or order the search results, such as head, tail, and sort.</p>
                    <p>Refer to the provided screenshots for examples of these commands.</p>
                </li>
            </ul>
        </li>
        <li><strong>Task 7 - Transformational Commands in SPL</strong>
            <ul>
                <li><strong>Understand Transformational Commands:</strong>
                    <p>Transformational commands convert results into a data structure for easier analysis.</p>
                    <p>These commands can be used for statistical purposes or to create visualizations.</p>
                    <p>Refer to the provided screenshots for examples of commonly used transformational commands.</p>
                </li>
            </ul>
        </li>
    </ol>
    <h2>Conclusion</h2>
    <p>By following these steps, you can successfully navigate and utilize SPL in the TryHackMe Splunk lab. Remember to replace placeholder values with actual data from your lab environment.</p>
</body>
</html>
