# Open-Ended-Lab
- Run Fetch.sh in terminal using 
< bash ./Fetch.sh >
- Then your terminal will generate results in an interval of 1 hour
- if the temperature is greater than 30 °C  or less than 10 °C then it will send email to muhammedhasanmisba@gmail.com

Program flow
--------------------
- Fetch.sh --------> calls my_program(which is the executable for http_request.c) --------------> this generates weather_data.json file by fetching the api = "https://api.open-meteo.com/v1/forecast?latitude=24.8608&longitude=67.0104&current=temperature_2m,relative_humidity_2m,apparent_temperature,is_day,pressure_msl"
- Fetch.sh --------> calls weather.zsh ----------> this checks the conditions of temperture by reading the json file -----> if the condition is extreme then it generates a mail and sends to the above mentioned gmail.
- Fetch.sh --------> calls generate_report.sh ---------> this reads json file and writes the temperature condition on report.txt file.
