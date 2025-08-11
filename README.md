Beside main ones I am using few additional notebooks:
- configuration -> variables used in several notebooks
- encryption_helper -> helper for encrypting and decrypting PII fields
- transformation_helper -> helper for cleaning data in silver layer
You can find pipeline configuration in job.json file
_____
# 01_create_metadata
Schemas are created:<br>
<img width="454" height="438" alt="image" src="https://github.com/user-attachments/assets/676d145a-3b7f-4ce5-b057-0b3398889bd4" /><br>
# 02_load_bronze_data
Raw data with encrypted PII fields<br>
<br>
expedia_raw:<br>
<img width="780" height="897" alt="image" src="https://github.com/user-attachments/assets/90d95d47-fb70-4958-91d9-b94e4950bc92" /><br>
<img width="1605" height="829" alt="image" src="https://github.com/user-attachments/assets/1d3fd585-6d87-434d-aea1-91fa06462c66" /><br>
<img width="1695" height="840" alt="image" src="https://github.com/user-attachments/assets/15b6c130-b004-4c8f-ab52-8ed214a84eff" /><br>
<br>
bronze.hotel_weather_raw:<br>
<img width="940" height="787" alt="image" src="https://github.com/user-attachments/assets/d8453589-f94a-4e9d-bb45-1094ebe01a85" /><br>
<img width="1670" height="837" alt="image" src="https://github.com/user-attachments/assets/846da85c-30df-4987-a237-9d99fe0096d6" /><br>
<img width="1695" height="832" alt="image" src="https://github.com/user-attachments/assets/2c5b55c9-851e-4cdb-ad7a-67f6b3f2f08b" /><br>
# 03_bronze_to_silver
Data with:<br>
- trimmed string values<br>
- columns casted to correct types<br>
- null values instead of empty ones<br>
- removed duplicates<br>
<br>
expedia_processed:<br>
<img width="885" height="929" alt="image" src="https://github.com/user-attachments/assets/b4e69597-2f7a-4bc0-82db-a338f403cebe" /><br>
<img width="1751" height="819" alt="image" src="https://github.com/user-attachments/assets/215e9634-2066-420d-888c-54770a79612a" /><br>
<img width="1671" height="874" alt="image" src="https://github.com/user-attachments/assets/fc1be699-fc95-4b3a-a4db-e394a68202b6" /><br>
<br>
hotel_weather_processed:<br>
<img width="935" height="826" alt="image" src="https://github.com/user-attachments/assets/dfd90ba1-1fdf-42e3-a9d3-29e77144f6a9" /><br>
<img width="1470" height="814" alt="image" src="https://github.com/user-attachments/assets/c3c22752-8c19-4974-ac2d-1bb061bdbe21" /><br>
<img width="1637" height="803" alt="image" src="https://github.com/user-attachments/assets/fac54747-3a28-4dd6-a3b1-61665c4101f1" /><br>

# 04_silver_to_gold
Data prepared for analisys:<br>
top_10_busiest_hotels_monthly:<br>
<img width="834" height="479" alt="image" src="https://github.com/user-attachments/assets/a8094308-eb8e-4402-b191-cec343706945" /><br>
<img width="537" height="608" alt="image" src="https://github.com/user-attachments/assets/7b74de2c-8ce1-41ad-9ef9-84a846e8daec" /><br>
<br>
top_10_temp_diff_monthly:<br>
<img width="958" height="563" alt="image" src="https://github.com/user-attachments/assets/3169409d-5785-4692-a23d-08005fc50dc0" /><br>
<img width="604" height="779" alt="image" src="https://github.com/user-attachments/assets/e1681e4b-f153-40bb-a238-6d8dd45a2cf5" /><br>
There's only data for months 8 to 10, but that's because hotel_weather_raw data contains data only for those months:<br>
<img width="473" height="527" alt="image" src="https://github.com/user-attachments/assets/7a5f53fa-c149-4369-9d32-b7147027c735" /><br>
<br>
weather_trend_extended_stay:<br>
<img width="780" height="678" alt="image" src="https://github.com/user-attachments/assets/3d2d6cd1-de12-4692-b84c-21096541fab7" /><br>
<img width="746" height="823" alt="image" src="https://github.com/user-attachments/assets/834c1269-26f5-4694-b5d0-0a8410b8833b" /><br>
