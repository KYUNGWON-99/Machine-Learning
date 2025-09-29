# Python
Starbucks__Crawling

- 2025.09.18 일지
    - for 문 사용시 객체들의 생명주기에 내가 원하는 정답이 있을 수 있다.
    - 예시
         ```
            for n in range(len(sido_cd)):
                payload = {
                "sido_cd" : f"{sido_cd[n]}",
                "rndCod" : "WKM8RHPKRH"
                }
                gugun_response = requests.post(gugun_url, data=payload ,headers= header).json()
                gugun_cd = []
                gugun_nm = []
                for i in range(gugun_response['list'].__len__()):
                    if gugun_response['list'][i]['gugun_cd'] not in(gugun_cd):
                        gugun_cd.append(gugun_response['list'][i]['gugun_cd'])

                    if gugun_response['list'][i]['gugun_nm'] not in(gugun_nm):
                        gugun_nm.append(gugun_response['list'][i]['gugun_nm'])

                sigun_cd.append({sido_cd[n] : gugun_cd})
                sigun_nm.append({sido_nm[n] : gugun_nm})

# Machine Learning
DNN, CNN, RNN
