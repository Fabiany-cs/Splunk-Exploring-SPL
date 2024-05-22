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
                    <img width="1543" alt="Screenshot 2024-05-22 at 11 18 00 AM" src="https://github.com/Fabiany-cs/Splunk-Exploring-SPL/assets/107880960/e7cf82a5-581d-425d-ac6e-a65af69e7252">
                </li>
                <li><strong>Navigate to Windowslog Index:</strong>
                    <ul>
                        <li>Go to “Search & Reporting” on the left panel.</li>
                        <li>Select the "Data Summary" tab to see the host for answer 1.</li>
                        <img width="1273" alt="Screenshot 2024-05-22 at 11 24 32 AM" src="https://github.com/Fabiany-cs/Splunk-Exploring-SPL/assets/107880960/7c3ba1f8-f2ee-4dae-a650-cb49318a76ec">
<img width="799" alt="Screenshot 2024-05-22 at 11 29 17 AM" src="https://github.com/Fabiany-cs/Splunk-Exploring-SPL/assets/107880960/b999c240-d634-4d81-9a50-f038c7180e44">
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
                    <img width="1455" alt="Screenshot 2024-05-22 at 11 47 57 AM" src="https://github.com/Fabiany-cs/Splunk-Exploring-SPL/assets/107880960/8bc2caaa-abb9-4587-a2d3-f9d529a601e8">
<img width="1455" alt="Screenshot 2024-05-22 at 11 51 09 AM" src="https://github.com/Fabiany-cs/Splunk-Exploring-SPL/assets/107880960/6ae7c648-9466-48a0-82f1-aa54a80733da">
<img width="1455" alt="Screenshot 2024-05-22 at 12 25 58 PM" src="https://github.com/Fabiany-cs/Splunk-Exploring-SPL/assets/107880960/a0951cb9-9273-46a6-bfcd-80550955abc3">
                </li>
            </ul>
        </li>
        <li><strong>Task 4 - Splunk Processing Language Overview</strong>
            <ul>
                <li><strong>Learn SPL:</strong>
                    <p>View the provided images to understand how to build queries using SPL.</p>
                    <img width="1242" alt="Screenshot 2024-05-22 at 12 31 59 PM" src="https://github.com/Fabiany-cs/Splunk-Exploring-SPL/assets/107880960/d52cce30-73cf-46aa-addd-282f2959c69f">
<img width="1246" alt="Screenshot 2024-05-22 at 12 32 09 PM" src="https://github.com/Fabiany-cs/Splunk-Exploring-SPL/assets/107880960/3b75872b-5a87-4229-8a8e-dff8e28be36e">
<img width="1252" alt="Screenshot 2024-05-22 at 12 32 14 PM" src="https://github.com/Fabiany-cs/Splunk-Exploring-SPL/assets/107880960/712cea8c-467f-417a-bf4f-02ed911e15d4">
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
