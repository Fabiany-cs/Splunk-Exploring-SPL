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
                    <img width="1428" alt="Screenshot 2024-05-22 at 12 33 53 PM" src="https://github.com/Fabiany-cs/Splunk-Exploring-SPL/assets/107880960/6d73d5f3-514b-4aad-bacb-82674f183069">
<img width="1425" alt="Screenshot 2024-05-22 at 12 34 05 PM" src="https://github.com/Fabiany-cs/Splunk-Exploring-SPL/assets/107880960/eb27b0cc-ef2e-47b4-88fa-e10045a7afcd">
<img width="1442" alt="Screenshot 2024-05-22 at 12 35 56 PM" src="https://github.com/Fabiany-cs/Splunk-Exploring-SPL/assets/107880960/cce96728-b4db-4bc0-b6cd-545eec6745ca">
<img width="1442" alt="Screenshot 2024-05-22 at 12 38 29 PM" src="https://github.com/Fabiany-cs/Splunk-Exploring-SPL/assets/107880960/ffd9569a-afb6-48c8-9bc2-6a527e89ce13">
<img width="1433" alt="Screenshot 2024-05-22 at 12 38 39 PM" src="https://github.com/Fabiany-cs/Splunk-Exploring-SPL/assets/107880960/47705a31-e41b-4b06-bbfe-9d153c996001">
                </li>
            </ul>
        </li>
        <li><strong>Task 5 - Filtering the Results in SPL</strong>
            <ul>
                <li><strong>Explore Filtering Options:</strong>
                    <p>Use different filtering options such as Fields, Search, Dedup, and Rename to get the next two answers.</p>
                    <p>Refer to the screenshots for additional help.</p>
                    
<img width="1256" alt="Screenshot 2024-05-22 at 12 44 48 PM" src="https://github.com/Fabiany-cs/Splunk-Exploring-SPL/assets/107880960/757e4b8c-3d3a-4eef-b7a2-70895d85742c">
<img width="1263" alt="Screenshot 2024-05-22 at 12 45 15 PM" src="https://github.com/Fabiany-cs/Splunk-Exploring-SPL/assets/107880960/b1a664d8-8c0c-4304-bb2c-82555f5ddc7e">
<img width="1258" alt="Screenshot 2024-05-22 at 12 45 26 PM" src="https://github.com/Fabiany-cs/Splunk-Exploring-SPL/assets/107880960/34393412-f4f7-4669-bebd-a3cc1c9bdafb">
<img width="1249" alt="Screenshot 2024-05-22 at 12 45 37 PM" src="https://github.com/Fabiany-cs/Splunk-Exploring-SPL/assets/107880960/218b5683-2951-490f-a5c3-f1f3732b209d">
<img width="1437" alt="Screenshot 2024-05-22 at 12 47 16 PM" src="https://github.com/Fabiany-cs/Splunk-Exploring-SPL/assets/107880960/5fadfa2c-11c5-40a1-b749-afec4aa9a2c3">
<img width="1442" alt="Screenshot 2024-05-22 at 12 48 32 PM" src="https://github.com/Fabiany-cs/Splunk-Exploring-SPL/assets/107880960/5172cb4d-ccf9-4898-bd18-eccfd11307a7">
                </li>
            </ul>
        </li>
        <li><strong>Task 6 - SPL - Structuring the Search Results</strong>
            <ul>
                <li><strong>Use Structuring Commands:</strong>
                    <p>SPL provides commands to structure or order the search results, such as head, tail, and sort.</p>
                    <p>Refer to the provided screenshots for examples of these commands.</p>
                    <img width="1254" alt="Screenshot 2024-05-22 at 12 50 13 PM" src="https://github.com/Fabiany-cs/Splunk-Exploring-SPL/assets/107880960/37e601c5-a86b-4bed-92ec-a8b871da8801">
<img width="1256" alt="Screenshot 2024-05-22 at 12 50 18 PM" src="https://github.com/Fabiany-cs/Splunk-Exploring-SPL/assets/107880960/16b1fc52-0f68-4885-a849-146ab7015254">
<img width="1264" alt="Screenshot 2024-05-22 at 12 50 30 PM" src="https://github.com/Fabiany-cs/Splunk-Exploring-SPL/assets/107880960/d9d68a23-0a43-4270-89cb-323e71af5802">
<img width="1259" alt="Screenshot 2024-05-22 at 12 50 35 PM" src="https://github.com/Fabiany-cs/Splunk-Exploring-SPL/assets/107880960/6b845b09-4004-445b-90a0-d517daa0dd5e">
<img width="1259" alt="Screenshot 2024-05-22 at 12 50 41 PM" src="https://github.com/Fabiany-cs/Splunk-Exploring-SPL/assets/107880960/a5da9fad-9660-448f-b67f-0ac8f4b60cf1">
<img width="1436" alt="Screenshot 2024-05-22 at 12 51 22 PM" src="https://github.com/Fabiany-cs/Splunk-Exploring-SPL/assets/107880960/4ffd51a2-b6d0-485a-a9b8-a44d233ee477">
<img width="1448" alt="Screenshot 2024-05-22 at 12 52 05 PM" src="https://github.com/Fabiany-cs/Splunk-Exploring-SPL/assets/107880960/8f6f664e-d6e8-4f6c-bca5-b0157e38ca63">
<img width="1442" alt="Screenshot 2024-05-22 at 12 54 34 PM" src="https://github.com/Fabiany-cs/Splunk-Exploring-SPL/assets/107880960/b6214dfc-7f03-46d3-81af-8ae5de071b62">
                </li>
            </ul>
        </li>
        <li><strong>Task 7 - Transformational Commands in SPL</strong>
            <ul>
                <li><strong>Understand Transformational Commands:</strong>
                    <p>Transformational commands convert results into a data structure for easier analysis.</p>
                    <p>These commands can be used for statistical purposes or to create visualizations.</p>
                    <p>Refer to the provided screenshots for examples of commonly used transformational commands.</p>
                    <img width="1260" alt="Screenshot 2024-05-22 at 12 55 37 PM" src="https://github.com/Fabiany-cs/Splunk-Exploring-SPL/assets/107880960/0b18a81c-8776-43bb-a12a-3fbf012f3e8d">
<img width="1261" alt="Screenshot 2024-05-22 at 12 55 46 PM" src="https://github.com/Fabiany-cs/Splunk-Exploring-SPL/assets/107880960/f0de0e0d-e35e-49bc-ad37-e85024c9cd10">
<img width="1261" alt="Screenshot 2024-05-22 at 12 55 55 PM" src="https://github.com/Fabiany-cs/Splunk-Exploring-SPL/assets/107880960/a8d7dec4-67d7-4f1e-a508-a53d6df51bc5">
<img width="1256" alt="Screenshot 2024-05-22 at 12 56 04 PM" src="https://github.com/Fabiany-cs/Splunk-Exploring-SPL/assets/107880960/aa995029-f052-4f4d-9edd-02f01288d6a5">
<img width="1253" alt="Screenshot 2024-05-22 at 12 56 19 PM" src="https://github.com/Fabiany-cs/Splunk-Exploring-SPL/assets/107880960/5ff9e500-eae2-452d-a257-2dffc9e95c16">
<img width="1262" alt="Screenshot 2024-05-22 at 12 56 27 PM" src="https://github.com/Fabiany-cs/Splunk-Exploring-SPL/assets/107880960/72d49d98-12b1-4c5a-bd91-7564d4a42d4f">
<img width="1452" alt="Screenshot 2024-05-22 at 12 58 09 PM" src="https://github.com/Fabiany-cs/Splunk-Exploring-SPL/assets/107880960/48026c74-c01d-4e74-a03d-75366a4cfb8b">
<img width="1443" alt="Screenshot 2024-05-22 at 12 59 02 PM" src="https://github.com/Fabiany-cs/Splunk-Exploring-SPL/assets/107880960/811361a9-7bc2-457e-9f1d-19313afc17e3">
<img width="1447" alt="Screenshot 2024-05-22 at 1 02 49 PM" src="https://github.com/Fabiany-cs/Splunk-Exploring-SPL/assets/107880960/694916e9-9bfa-4791-961d-f80ef2fe7f50">
                </li>
            </ul>
        </li>
    </ol>
    <h2>Conclusion</h2>
    <p>By following these steps, you can successfully navigate and utilize SPL in the TryHackMe Splunk lab. Remember to replace placeholder values with actual data from your lab environment.</p>
</body>
</html>
