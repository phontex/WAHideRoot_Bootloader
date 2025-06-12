# WAHideRoot+Bootloader
Инструкция по скрытию состояния загрузчика и наличия Root-прав от WhatsApp и WhatsApp Business. Пока что способ протестирован только с использованьем корневого менеджера Magisk
 
---

## 📌 **Оглавление**  
1. [Требования](#-требования)  
2. [Установка](#-установка)  
3. [Настройка](#-настройка)  
4. [Решение проблем](#-решение-проблем)  
5. [FAQ](#-faq)  

---

## 📋 **Требования**  
- Magisk: на вашем устройстве должен быть установлен Magisk.
- Root-права: для использованья данного метода требуються root-права.  
- WhatsApp: версия  WhatsApp должна быть не выше 2.25.6.71.

---

## ⚙️ **Установка**  
### 1: Изменение настроек Magisk и установка необходимых модулей 
- **1.1. Изменение настроек Magisk:**
   - Откройте Magisk Manager
   - Перейдите в «Настройки», отключите «Zygisk» и «DenyList»
   - Откройте «Настройка DenyList», выделите галочкой приложение Сервисы Google Play, нажмите на аватарку этого приложения и включите все переключатели. Тоже самое сделайте с приложением WhatsApp либо WhatsApp Business.
   - Вернитесь в «Настройки» и нажмите на «Скрытие приложения Magisk». Измените название приложения на любое, кроме «Magisk»
- **1.2. Установка необходимых модулей:**
   - Устоновите себе на устройство данные модули: [`Zygisk Next` ](https://github.com/Dr-TSNG/ZygiskNext/releases)/[`LSPosed v1.10.1`](https://github.com/JingMatrix/LSPosed/releases)/[`Play Integrity Fix`](https://mmrl.dev/repository/aptoftisk/playintegrityfix)/[`TrickyStore`](https://github.com/5ec1cff/TrickyStore/releases)/[`TrickyAddon`](https://github.com/KOWX712/Tricky-Addon-Update-Target-List/releases/tag/v3.9)/[`Shamiko`](https://github.com/LSPosed/LSPosed.github.io/releases)
   - Вернитесь на «главную страницу» Magisk Manager.
   - Перейдите в раздел «Модули» и выберите «Установить из хранилища».
   - Выберите и устоновите модули, которые нужно было загрузить себе на устройство.
   - После успешной устоновки всех модулей, перезагрузите устройство.
### 2: Настройка модулей
- **2.1. Настройка модулей:**
   - После перезагрузки, откройте Magisk Manager
   - Перейдите в раздел «Модули»
   - Найдите модуль «Play Integrity Fix» и нажмите кнопку «Action» под модулем. Немного подождите, затем нажмите на кнопку «Close» в правом нижнем углу.
   - Найдите модуль «Tricky Store» и нажмите кнопку «Action» под модулем. Дожитесь загрузки WebUI и дайте открывшемуся приложению доступ к правам суперпользователя.
   - В открывшемся приложении открываете меню (три полоски в правом верхнем углу) и выберите «Выбрать все». Затем нажмите синюю кнопку «Сохранить».
   - После нажатия кнопки «Сохранить» опять открываете меню, выбераете «Устоновить Security Patch».
   - В открывшемся окне ставите галочку на параметр «Расширенный». В пункте «System» пишите «prop». В пункте «Boot» пишите дату «2025-05-05». В пункте «Vendor» пишите дату «2025-05-05». Затем жмёте на кнопку «Сохранить».
   - Затем опять открываете меню, выбераете «Устоновить пользовательский Keybot». Скачиваете <?xml version="1.0" encoding="UTF-8"?>
<!-- fetched from Tricky Addon - Update Target List -->
<AndroidAttestation>
    <NumberOfKeyboxes>1</NumberOfKeyboxes>
    <Keybox DeviceID="sw">
        <Key algorithm="ecdsa">
            <PrivateKey format="pem">
                -----BEGIN EC PRIVATE KEY-----
                MHcCAQEEIIFw6fKjh+TU2uFi/UKMyj5jEEwd9i38/2KpPNuNLVJgoAoGCCqGSM49
                AwEHoUQDQgAE637hVErkNxe5MCpLqa2OjdHRFS855uhvO46e0XgmaO/P4Pmz+8s3
                xp97PuQ9UPGazYHEbK+oJcjEvzyZ9TI4ew==
                -----END EC PRIVATE KEY-----
            </PrivateKey>
            <CertificateChain>
                <NumberOfCertificates>3</NumberOfCertificates>
                <Certificate format="pem">
                    -----BEGIN CERTIFICATE-----
                    MIICJjCCAaugAwIBAgIKBYBFMEA2ZWFxODAKBggqhkjOPQQDAjApMRkwFwYDVQQF
                    ExBhODRkNDhiOWNmNzJiYjc3MQwwCgYDVQQMDANURUUwHhcNMTkwNjI2MjEyOTUx
                    WhcNMjkwNjIzMjEyOTUxWjApMRkwFwYDVQQFExA5YTIwYzNiYzJlYTI3YjFlMQww
                    CgYDVQQMDANURUUwWTATBgcqhkjOPQIBBggqhkjOPQMBBwNCAATrfuFUSuQ3F7kw
                    KkuprY6N0dEVLznm6G87jp7ReCZo78/g+bP7yzfGn3s+5D1Q8ZrNgcRsr6glyMS/
                    PJn1Mjh7o4G6MIG3MB0GA1UdDgQWBBTV74M94XjuUXUr7Ny959dyOdYJEjAfBgNV
                    HSMEGDAWgBRLlpGPfwsbbhGYlwf6HF6NiRX0TTAPBgNVHRMBAf8EBTADAQH/MA4G
                    A1UdDwEB/wQEAwICBDBUBgNVHR8ETTBLMEmgR6BFhkNodHRwczovL2FuZHJvaWQu
                    Z29vZ2xlYXBpcy5jb20vYXR0ZXN0YXRpb24vY3JsLzA1ODA0NTMwNDAzNjY1NjE3
                    MTM4MAoGCCqGSM49BAMCA2kAMGYCMQCnE+bPV9rVfiaxHJO3UgbefhvNXNd8goiF
                    FBEEbzRAA1utax10ijmY43asFiPE26ICMQDGoHjMBBy6wFsqnEkswx4j03VfUiZi
                    0k4GgZgokfVTGczWVunf9dr/CEW6jC5ZkRg=
                    -----END CERTIFICATE-----
                </Certificate>
                <Certificate format="pem">
                    -----BEGIN CERTIFICATE-----
                    MIID0TCCAbmgAwIBAgIKA4gmZ2BliZaF5DANBgkqhkiG9w0BAQsFADAbMRkwFwYD
                    VQQFExBmOTIwMDllODUzYjZiMDQ1MB4XDTE5MDYyNjIxMjYwOFoXDTI5MDYyMzIx
                    MjYwOFowKTEZMBcGA1UEBRMQYTg0ZDQ4YjljZjcyYmI3NzEMMAoGA1UEDAwDVEVF
                    MHYwEAYHKoZIzj0CAQYFK4EEACIDYgAEuAoOW7eZeb3mE9gsjxrWKyDeKJ93vRjX
                    8ygYY6q7sZ8wvHoOMi+CmP2rYJyRQ5dNOwuEUM5SV4QHktjOXbPXqHC5Hu+3Slnb
                    +s6eBwgydM6WOW2GpkOudmqctNannmuIo4G2MIGzMB0GA1UdDgQWBBRLlpGPfwsb
                    bhGYlwf6HF6NiRX0TTAfBgNVHSMEGDAWgBQ2YeEAfIgFCVGLRGxH/xpMyepPEjAP
                    BgNVHRMBAf8EBTADAQH/MA4GA1UdDwEB/wQEAwICBDBQBgNVHR8ESTBHMEWgQ6BB
                    hj9odHRwczovL2FuZHJvaWQuZ29vZ2xlYXBpcy5jb20vYXR0ZXN0YXRpb24vY3Js
                    L0U4RkExOTYzMTREMkZBMTgwDQYJKoZIhvcNAQELBQADggIBAJmoTeXPpdYa2yv7
                    r9305fv6zdZf7fFv5ip8cyXnsNw9CD6v6f03Hvb92f+aWfLIFdI0rQuZ/+WKrOcF
                    SP2KDsYR7FOmX7Kds3nmeQyrT/u/p5dKEKcmwAtZufEgYSo5sMQdv2wiysXEa523
                    nYR1pf1wwcEcMbyPYmHYqRWURVysvq0H2TshFZqo1Ztn1n7a3li84brfBBWh0NBc
                    4CnpX9eQpZbISO8C8Vv0VJNCb2u9Vu6TLyeUvM6C4Om8rfKOgFk8VAXMvCKMunGr
                    URua2uaX0W29raXoCDW8Z+O/IYcWUn1FLMEGVX2QeW2IWurqlbCb37XQ3ju4sKDV
                    6FO2vUS9zc2DOU279q8d9aGAjfJluScJYFHDOVrxg8rtr0uFecVYeFcq6azReoS6
                    MUMAf/WWavMuHf+s0S3LiqJpn/pDFoqAdvm+UdcORYY7iGRlp6vhidogqkRLT2py
                    38SL+zMP5CLnbZeMAfk5gutBNWSse13jrSEHav7Z2oTUDgJtml41voX4nwOWGDFy
                    kWlhz+S6MrQjkw2gSzWHVEs8ZSdD15pK7hUWo8+zfbpDMe4c2Iij1ssIBkcOw+L6
                    BYLBql5f5E2HOKC8o+qKFJilohdKPrx9XyJ7Th3V4UiFsYSGY+tz4WJlabLGZnt5
                    nJsVwXHRr8WpIRBUP5n9ucHMoWa1
                    -----END CERTIFICATE-----
                </Certificate>
                <Certificate format="pem">
                    -----BEGIN CERTIFICATE-----
                    MIIFYDCCA0igAwIBAgIJAOj6GWMU0voYMA0GCSqGSIb3DQEBCwUAMBsxGTAXBgNV
                    BAUTEGY5MjAwOWU4NTNiNmIwNDUwHhcNMTYwNTI2MTYyODUyWhcNMjYwNTI0MTYy
                    ODUyWjAbMRkwFwYDVQQFExBmOTIwMDllODUzYjZiMDQ1MIICIjANBgkqhkiG9w0B
                    AQEFAAOCAg8AMIICCgKCAgEAr7bHgiuxpwHsK7Qui8xUFmOr75gvMsd/dTEDDJdS
                    Sxtf6An7xyqpRR90PL2abxM1dEqlXnf2tqw1Ne4Xwl5jlRfdnJLmN0pTy/4lj4/7
                    tv0Sk3iiKkypnEUtR6WfMgH0QZfKHM1+di+y9TFRtv6y//0rb+T+W8a9nsNL/ggj
                    nar86461qO0rOs2cXjp3kOG1FEJ5MVmFmBGtnrKpa73XpXyTqRxB/M0n1n/W9nGq
                    C4FSYa04T6N5RIZGBN2z2MT5IKGbFlbC8UrW0DxW7AYImQQcHtGl/m00QLVWutHQ
                    oVJYnFPlXTcHYvASLu+RhhsbDmxMgJJ0mcDpvsC4PjvB+TxywElgS70vE0XmLD+O
                    JtvsBslHZvPBKCOdT0MS+tgSOIfga+z1Z1g7+DVagf7quvmag8jfPioyKvxnK/Eg
                    sTUVi2ghzq8wm27ud/mIM7AY2qEORR8Go3TVB4HzWQgpZrt3i5MIlCaY504LzSRi
                    igHCzAPlHws+W0rB5N+er5/2pJKnfBSDiCiFAVtCLOZ7gLiMm0jhO2B6tUXHI/+M
                    RPjy02i59lINMRRev56GKtcd9qO/0kUJWdZTdA2XoS82ixPvZtXQpUpuL12ab+9E
                    aDK8Z4RHJYYfCT3Q5vNAXaiWQ+8PTWm2QgBR/bkwSWc+NpUFgNPN9PvQi8WEg5Um
                    AGMCAwEAAaOBpjCBozAdBgNVHQ4EFgQUNmHhAHyIBQlRi0RsR/8aTMnqTxIwHwYD
                    VR0jBBgwFoAUNmHhAHyIBQlRi0RsR/8aTMnqTxIwDwYDVR0TAQH/BAUwAwEB/zAO
                    BgNVHQ8BAf8EBAMCAYYwQAYDVR0fBDkwNzA1oDOgMYYvaHR0cHM6Ly9hbmRyb2lk
                    Lmdvb2dsZWFwaXMuY29tL2F0dGVzdGF0aW9uL2NybC8wDQYJKoZIhvcNAQELBQAD
                    ggIBACDIw41L3KlXG0aMiS//cqrG+EShHUGo8HNsw30W1kJtjn6UBwRM6jnmiwfB
                    Pb8VA91chb2vssAtX2zbTvqBJ9+LBPGCdw/E53Rbf86qhxKaiAHOjpvAy5Y3m00m
                    qC0w/Zwvju1twb4vhLaJ5NkUJYsUS7rmJKHHBnETLi8GFqiEsqTWpG/6ibYCv7rY
                    DBJDcR9W62BW9jfIoBQcxUCUJouMPH25lLNcDc1ssqvC2v7iUgI9LeoM1sNovqPm
                    QUiG9rHli1vXxzCyaMTjwftkJLkf6724DFhuKug2jITV0QkXvaJWF4nUaHOTNA4u
                    JU9WDvZLI1j83A+/xnAJUucIv/zGJ1AMH2boHqF8CY16LpsYgBt6tKxxWH00XcyD
                    CdW2KlBCeqbQPcsFmWyWugxdcekhYsAWyoSf818NUsZdBWBaR/OukXrNLfkQ79Iy
                    ZohZbvabO/X+MVT3rriAoKc8oE2Uws6DF+60PV7/WIPjNvXySdqspImSN78mflxD
                    qwLqRBYkA3I75qppLGG9rp7UCdRjxMl8ZDBld+7yvHVgt1cVzJx9xnyGCC23Uaic
                    MDSXYrB4I4WHXPGjxhZuCuPBLTdOLU8YRvMYdEvYebWHMpvwGCF6bAx3JBpIeOQ1
                    wDB5y0USicV3YgYGmi+NZfhA4URSh77Yd6uuJOJENRaNVTzk
                    -----END CERTIFICATE-----
                </Certificate>
            </CertificateChain>
        </Key>
        <Key algorithm="rsa">
            <PrivateKey format="pem">
                -----BEGIN RSA PRIVATE KEY-----
                MIIG5QIBAAKCAYEA6cfoRi5y2Baa2hJLCPtRN4v6U1qU2+HMYflKHgw6f35eLUZi
                +Ltn4HLMkoISFy2fluHCEf9lVjBJEpc573834npXWVv5ey+GZwPx9y4ZbRBjheea
                eEZyxvQhqWD+WOIa91Nd1FKP7M6uHIHUr2zeEV0ZsX6qV3MKdAAKztgke24+6TsC
                tBc5Z9QT8DrUnYR/JkN2KnZK6QIkUCDcILslj8mzX62ft8Wqo2p1Tg1bY8txUZSD
                UwcB2OhvEd5A2AXX/RSg+lvEGO1osJw8ax3CId8/U+Td/fQviOu0ejfJx921K0oF
                WR6oe9JRzFyzKkzAyo7aHgkbukt+tsPYh/RXlpUxZ3YQ1CvbESkjsnLBkLdis9GG
                no94Y6bC3JA/Hnmjv6ocDBUugLam028fwIF6nLYsPZtbJA5cZl1BAoDvmWmKOvRz
                lZtvsUlyFBv+EHN19B9y5Zteu2Xnf6s3yXffW2RWFdkThM2CtXj06aPECPcb8eKS
                G4q2cHs6JLnqAoPBAgMBAAECggGAHzZvjp84+hzag+8ZUZOsXkw0GdjoMwtMrHAK
                M0TSsp7+l/Dj2e27ir4JDi6Ll8ihnBV8QcblksJTn0XNmGpV3ckTzHx5LLdFrI9c
                SPJAts0PXJt1hkVxoZqKvACVNOzLSOY6itSTHrzhhjDXYqyYYZ0ahxYwTAiyBpbS
                2pcFF+26PI2CaOUI5xHrr5FLPdSo3UT4i+bLTZzZmFEq0rvp4e6+IjIeNv0PMU5P
                ZyJlZ0eMU6YOepFe78Tov2v7IFx3HqG7NQocTtYL/1gijoAAesWk1s8u68AWhluC
                teQ1aZjz0SN5tb7eARkjk4NZgjjp4gz+265rCdFQ8GEdJepzej5B5LaW2tjYbpYQ
                qryKRpfXzZCqs6lrJL357m8cnWv95cAIouZ+7RBIPwt7rIkd8q/R7xutu1eUrU6z
                SEVntXkULPogxxD1vkXdnkpowd1tOJ9cHrq4SQs1mYI18Mp21XuzyKvAAVUnBXCT
                tFgGRJ9aIk3251DsR55UwTkdK/05AoHBAPUvT7buI75jcOa2tjnDiq3/RFxgcs6e
                DGJO8/nnBU+AJu7aVrHKPboUZqqiT/mWFFkY7LtK9qMmAWEb7OxZiGkfAkKniq94
                tzTROCh58FVWxoxLKbc9MZAFk2Dw+TYBgqLAHdLTfYCeDmPfilx/sZYFfQBdUDzA
                tNlX2S4yYhtyEn0uWhk2rONC0fUL2scZ/QbFecbkt9pgYIlS7mEHf7qer1RwMamR
                /7s+MHYY5oGbTIDyLXtjILb3w3x3t4J+dwKBwQD0F9Hp69xck5kwWel5ExfVEEQY
                sbd10RFZdc8Hv8oX3V4xdM6CGQhHPO7qhaLdyVYqORq26FAIcvC70gGFQ5UNdkwU
                d5WbjRGA/PPEGY5CKVxkIcTftgUcRYhLqx7sBVgfuYgsSrUq86J2H1UGPnNO9kxh
                pkpclgk+ZWkHmpA3bxTKwU791bp1rkWnV42ZVUk8kBO9ygyGdM1zdDbUYs8oZHsI
                z44XO/gqDCgTAHYOeq8Ix92neVdVJMbGv5TyhYcCgcEAi9dPLPPIOTe4Vi6R4oJP
                34u/bryn3oawY4XKi5cjJUPfcM3hMog6Cp7GK75lxOG/e03G/8/yufzcPonR6L/s
                GKDSBjhO1mQQgjRuRk++Lr5OgggAo/1n/k/fziPCz/Wuj6rpl6x+YVREutvtq3I9
                VGaO9B1EvVHgFDKRsVKVODgoqXM9ejIAC6K543y+bF67PRh2q2UaI5hilxBQ29CO
                Hl+ReqR+/stBw4bl1wW+ut9blBQMstpH93N68MvLQ8djAoHBALRy25Mj829ZCjmN
                bqU8MTUo5j6fOvJVUY8iIaAn773+v8CuCnBxEwafDDzB+GofipyCRLaNPYVRe5hO
                IyOil5ExMAM9eJNbEWKbHZaOEfXlX9ECiemcRWDmImFWKvDu7nvdi8a6n/4VyLes
                aA3KozHvsP3LklOp80F2dNPTNuRUMTnG+J98nnCbGhEhD6QYQaENHhsDQIkx1iSQ
                +GvAdEb3KWGVFwUkJ0zmWcXaZGxF1BoYr0s80Aw4uN57CSDVBwKBwQCsUXx0SdLr
                nMyfG6ZlnltNalj14KbX1Jda9KQ/G4ufBEu+L+evNPpFMAH2CUqFY3Ra/NvPEusy
                HGL4dnAkd184I8/0anS3FMnvHMTK8/pVsnd+YbS/RFj8CpZvUnbXtX6q0KKyvhsS
                aMY8zJM99BYpzdFmy9zlD82/pnNyIRxnF3sKBbbVKX967J5fVtPILfKatw0X5U52
                smhjGBM5cDeCHedP9Vzyr1sHOH8Ul9ushajaNVQHPEn+WynfhKuORCc=
                -----END RSA PRIVATE KEY-----
            </PrivateKey>
            <CertificateChain>
                <NumberOfCertificates>3</NumberOfCertificates>
                <Certificate format="pem">
                    -----BEGIN CERTIFICATE-----
                    MIIFETCCAvmgAwIBAgIKE5hJQRBRlJORdzANBgkqhkiG9w0BAQsFADApMRkwFwYD
                    VQQFExBhODRkNDhiOWNmNzJiYjc3MQwwCgYDVQQMDANURUUwHhcNMTkwNjI2MjEy
                    OTM5WhcNMjkwNjIzMjEyOTM5WjApMRkwFwYDVQQFExA5YTIwYzNiYzJlYTI3YjFl
                    MQwwCgYDVQQMDANURUUwggGiMA0GCSqGSIb3DQEBAQUAA4IBjwAwggGKAoIBgQDp
                    x+hGLnLYFpraEksI+1E3i/pTWpTb4cxh+UoeDDp/fl4tRmL4u2fgcsySghIXLZ+W
                    4cIR/2VWMEkSlznvfzfieldZW/l7L4ZnA/H3LhltEGOF55p4RnLG9CGpYP5Y4hr3
                    U13UUo/szq4cgdSvbN4RXRmxfqpXcwp0AArO2CR7bj7pOwK0Fzln1BPwOtSdhH8m
                    Q3YqdkrpAiRQINwguyWPybNfrZ+3xaqjanVODVtjy3FRlINTBwHY6G8R3kDYBdf9
                    FKD6W8QY7WiwnDxrHcIh3z9T5N399C+I67R6N8nH3bUrSgVZHqh70lHMXLMqTMDK
                    jtoeCRu6S362w9iH9FeWlTFndhDUK9sRKSOycsGQt2Kz0Yaej3hjpsLckD8eeaO/
                    qhwMFS6AtqbTbx/AgXqctiw9m1skDlxmXUECgO+ZaYo69HOVm2+xSXIUG/4Qc3X0
                    H3Llm167Zed/qzfJd99bZFYV2ROEzYK1ePTpo8QI9xvx4pIbirZwezokueoCg8EC
                    AwEAAaOBujCBtzAdBgNVHQ4EFgQUx+ZlgqiO+uiGbcm3AsilEKpheO4wHwYDVR0j
                    BBgwFoAU+84EA7maMqgPFLwm9BblZBA+M78wDwYDVR0TAQH/BAUwAwEB/zAOBgNV
                    HQ8BAf8EBAMCAgQwVAYDVR0fBE0wSzBJoEegRYZDaHR0cHM6Ly9hbmRyb2lkLmdv
                    b2dsZWFwaXMuY29tL2F0dGVzdGF0aW9uL2NybC8xMzk4NDk0MTEwNTE5NDkzOTE3
                    NzANBgkqhkiG9w0BAQsFAAOCAgEAO18GdQE4DlGEOQFdXIAjq/qMnV08ibXQj9Sh
                    7uhRhMw8cR+Sxnfy5+ZsuePf28iV6KqnyQPnuDTmAttBg/f98bmmGm89jo6JHwpT
                    hU8cuZbswzqkP1Tn+ebCXbl5xKHoEDCT7vCComtBih6hS+vtVqtF/0iwU4ySe2/8
                    EiKEqc8WkhZB1DyIgepjKXgtJiiDWVvyj6OejZ39pUkDD6Q7V4TgJwfJkqqdLjfq
                    9NcuGA5hLDbM52xmHjzKx5aFF9kjs/GaAjuqebcn3xQTGoJoEpx2capRP/YXMwol
                    ivMEMOIl88xT5WLl6kr19+LLuX9I4plJKW8iOFLjoKd7nGKQx6UGOBP2Ul50cEcq
                    U/ivXQykQAvpqyBs3/V8vcuKA2c67oVVfJptamLEJxT7ZVtl5y1obH45YHQCXLkS
                    apK7QMfg6zL49J1djer6aKVBwdx0TLHb1vkjCnLBaeyD4t5XgKCt0sEfgsq3pdiR
                    gDHfLPf9tMcSOSUGByUxrTBZi8E5/DGozmexJoFslSFBQhscgJPsWgnDrGthzyJ0
                    jjXLVG9Mq0xT4t5ICYkwsBaHuG4eC3BvnTRNS9TNjqSdjFnkxF1GitOoCJrXyUcN
                    CUOfSNfBMjqo9f2uUxzgQBqvEQGr4bmrXHKtqQY/o9ZJfV/n+dkbLKso+UztpXaG
                    YSOSeNM=
                    -----END CERTIFICATE-----
                </Certificate>
                <Certificate format="pem">
                    -----BEGIN CERTIFICATE-----
                    MIIFfzCCA2egAwIBAgIKA4gmZ2BliZaF4zANBgkqhkiG9w0BAQsFADAbMRkwFwYD
                    VQQFExBmOTIwMDllODUzYjZiMDQ1MB4XDTE5MDYyNjIxMjUzN1oXDTI5MDYyMzIx
                    MjUzN1owKTEZMBcGA1UEBRMQYTg0ZDQ4YjljZjcyYmI3NzEMMAoGA1UEDAwDVEVF
                    MIICIjANBgkqhkiG9w0BAQEFAAOCAg8AMIICCgKCAgEA2RpOeMHVKeb7bRZQLySg
                    /4xuy+PoK6XKsjxEIGseuAvHnpoWhJE+RrImr3LYe28f0dyfRWA/lOEvMUfeOLZb
                    cCzouecxivJOXXKw/5Y6h41Busu2LDilqBbQs6mqrBwv3CQ9o458/mw5WrufYqsP
                    8hgcLosK4UcQTUb/C6/QxCqiXxrejgH62gxIW2I75o8ITFnwnFn3LdLVBL58am2V
                    NUaNvHmjsRJ5egzqXygS6sLkHf9mYROWteRuuHQm7bR0Gv0FufYWk3GvOU1I12RY
                    gCx76rSlyIpteyrg/sT21hX2CIjweokMnzNIW/qUPRewuakbUBDbDwqrrD3yeWe2
                    ew+3INRqdqXelQ305JSdMRcRkBMYSgq/AWSZ47BR5r1q20yepzuZxm6ZvFO6u9ad
                    uG6ACioioxFhsgvy3ZAukKeW+eKGkMZ+CkmlnZthyIgW+ee6F+YZsUuDx80yzJp6
                    zGzvONWTCfPXNTykzS6WGmYovcu8zQ+elHEUyGvI+Mykuoe1rjNBmlFP2rN5y7Lo
                    pDtcMDADm2yj2P2dk4+Mu2B2xtLSF+o1WCViJFhmR65NfaK2/1ULnr2MgiNaK3IH
                    vA+4+PJ6/0H+7za0zMDc2ujrpGgfeLLOivuoDGHlfhvjKCnT9cxpuFsbpoSO+QKP
                    VDHgVggl0t4PeAtvj0pa3M0CAwEAAaOBtjCBszAdBgNVHQ4EFgQU+84EA7maMqgP
                    FLwm9BblZBA+M78wHwYDVR0jBBgwFoAUNmHhAHyIBQlRi0RsR/8aTMnqTxIwDwYD
                    VR0TAQH/BAUwAwEB/zAOBgNVHQ8BAf8EBAMCAgQwUAYDVR0fBEkwRzBFoEOgQYY/
                    aHR0cHM6Ly9hbmRyb2lkLmdvb2dsZWFwaXMuY29tL2F0dGVzdGF0aW9uL2NybC9F
                    OEZBMTk2MzE0RDJGQTE4MA0GCSqGSIb3DQEBCwUAA4ICAQAqx62MMRqZyZLRWg5G
                    q+LkCRf6vpmIM/jYL103at/xtWWCdhm2u8cj9WYehrpnAi18SYisGBaZ0h3LKNDR
                    GYfpoVsyRsYuU90E2Q7pHNXO4xzTDFXjINzNYTd9xQhRp7FtptV5UGKk2XZ1w4vz
                    uB4Mh0j5E00TJKEYr5tUa/MuhyKV2YqO9qAEKB7KHjB3TggJnT3Pdz24me7F3/1O
                    E1OIh1OTM0Rzx8zBpIVjiKR9VAgYLQvOj0SHsHHf8+ccklyIGAV0JkD59Ta3ZS3D
                    v6oWkfSd/zrMBUraac+GHPmUz10Sw4EonnAYilW64+ywts2UaNB0u45IRwuSNo95
                    VcvPs9dks7vE7LRathC+JlFSf7pOg1EgtccD8Z1pFgzyus66s8zl0HADH+ZnyUag
                    LsQ8RIqUFHc+1AMDSj2sSdhDYZx1sVxEEyPl4gq5G2jzLeUPdWIhi/2Ieq4cx3Dr
                    MP3Tb7OUiOkmE/yoquFIaROroR8rNbCP3TGgl424ct0wp8Z4lHqI92n+emyCbv5o
                    6QcdZ7U/zjlkuwzkeCIE9pfWWiQ3Z7CgO7h4lhLrwh+MJDPD/lypGmJzFHXqa4y9
                    HIG4MbGsCl0cpYGsigulgGffRqu0un4/82pE4EXcHG/dexl+EfM71P9iUX/sz+XJ
                    wQ8/Nsqbj41H2UNjBo7Ltdekjg==
                    -----END CERTIFICATE-----
                </Certificate>
                <Certificate format="pem">
                    -----BEGIN CERTIFICATE-----
                    MIIFYDCCA0igAwIBAgIJAOj6GWMU0voYMA0GCSqGSIb3DQEBCwUAMBsxGTAXBgNV
                    BAUTEGY5MjAwOWU4NTNiNmIwNDUwHhcNMTYwNTI2MTYyODUyWhcNMjYwNTI0MTYy
                    ODUyWjAbMRkwFwYDVQQFExBmOTIwMDllODUzYjZiMDQ1MIICIjANBgkqhkiG9w0B
                    AQEFAAOCAg8AMIICCgKCAgEAr7bHgiuxpwHsK7Qui8xUFmOr75gvMsd/dTEDDJdS
                    Sxtf6An7xyqpRR90PL2abxM1dEqlXnf2tqw1Ne4Xwl5jlRfdnJLmN0pTy/4lj4/7
                    tv0Sk3iiKkypnEUtR6WfMgH0QZfKHM1+di+y9TFRtv6y//0rb+T+W8a9nsNL/ggj
                    nar86461qO0rOs2cXjp3kOG1FEJ5MVmFmBGtnrKpa73XpXyTqRxB/M0n1n/W9nGq
                    C4FSYa04T6N5RIZGBN2z2MT5IKGbFlbC8UrW0DxW7AYImQQcHtGl/m00QLVWutHQ
                    oVJYnFPlXTcHYvASLu+RhhsbDmxMgJJ0mcDpvsC4PjvB+TxywElgS70vE0XmLD+O
                    JtvsBslHZvPBKCOdT0MS+tgSOIfga+z1Z1g7+DVagf7quvmag8jfPioyKvxnK/Eg
                    sTUVi2ghzq8wm27ud/mIM7AY2qEORR8Go3TVB4HzWQgpZrt3i5MIlCaY504LzSRi
                    igHCzAPlHws+W0rB5N+er5/2pJKnfBSDiCiFAVtCLOZ7gLiMm0jhO2B6tUXHI/+M
                    RPjy02i59lINMRRev56GKtcd9qO/0kUJWdZTdA2XoS82ixPvZtXQpUpuL12ab+9E
                    aDK8Z4RHJYYfCT3Q5vNAXaiWQ+8PTWm2QgBR/bkwSWc+NpUFgNPN9PvQi8WEg5Um
                    AGMCAwEAAaOBpjCBozAdBgNVHQ4EFgQUNmHhAHyIBQlRi0RsR/8aTMnqTxIwHwYD
                    VR0jBBgwFoAUNmHhAHyIBQlRi0RsR/8aTMnqTxIwDwYDVR0TAQH/BAUwAwEB/zAO
                    BgNVHQ8BAf8EBAMCAYYwQAYDVR0fBDkwNzA1oDOgMYYvaHR0cHM6Ly9hbmRyb2lk
                    Lmdvb2dsZWFwaXMuY29tL2F0dGVzdGF0aW9uL2NybC8wDQYJKoZIhvcNAQELBQAD
                    ggIBACDIw41L3KlXG0aMiS//cqrG+EShHUGo8HNsw30W1kJtjn6UBwRM6jnmiwfB
                    Pb8VA91chb2vssAtX2zbTvqBJ9+LBPGCdw/E53Rbf86qhxKaiAHOjpvAy5Y3m00m
                    qC0w/Zwvju1twb4vhLaJ5NkUJYsUS7rmJKHHBnETLi8GFqiEsqTWpG/6ibYCv7rY
                    DBJDcR9W62BW9jfIoBQcxUCUJouMPH25lLNcDc1ssqvC2v7iUgI9LeoM1sNovqPm
                    QUiG9rHli1vXxzCyaMTjwftkJLkf6724DFhuKug2jITV0QkXvaJWF4nUaHOTNA4u
                    JU9WDvZLI1j83A+/xnAJUucIv/zGJ1AMH2boHqF8CY16LpsYgBt6tKxxWH00XcyD
                    CdW2KlBCeqbQPcsFmWyWugxdcekhYsAWyoSf818NUsZdBWBaR/OukXrNLfkQ79Iy
                    ZohZbvabO/X+MVT3rriAoKc8oE2Uws6DF+60PV7/WIPjNvXySdqspImSN78mflxD
                    qwLqRBYkA3I75qppLGG9rp7UCdRjxMl8ZDBld+7yvHVgt1cVzJx9xnyGCC23Uaic
                    MDSXYrB4I4WHXPGjxhZuCuPBLTdOLU8YRvMYdEvYebWHMpvwGCF6bAx3JBpIeOQ1
                    wDB5y0USicV3YgYGmi+NZfhA4URSh77Yd6uuJOJENRaNVTzk
                    -----END CERTIFICATE-----
                </Certificate>
            </CertificateChain>
        </Key>
    </Keybox>
</AndroidAttestation>

