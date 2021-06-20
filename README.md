# Luizgustavo33

Luiz Gustavo Ribeiro de Sá
RA: 62028934

Desafio 3 - (3 pontos) Clusterizando os dados do ENADE

Pepiline de teste:
![image](https://user-images.githubusercontent.com/74794415/122688294-d5400c00-d1f1-11eb-95cd-a1183c039598.png)

Train Clustering Model visualização do resultado:
![image](https://user-images.githubusercontent.com/74794415/122688509-fce3a400-d1f2-11eb-9f74-5f4ca702f761.png)

Assign Data to Clusters visualização do resultado:
![image](https://user-images.githubusercontent.com/74794415/122688456-abd3b000-d1f2-11eb-9fe2-8d6aab5e4554.png)

Evaluate Model
![image](https://user-images.githubusercontent.com/74794415/122688476-c27a0700-d1f2-11eb-9258-4f1b88faaa47.png)

Pipeline de inferência
![image](https://user-images.githubusercontent.com/74794415/122688887-58169600-d1f5-11eb-97ec-cfc8a55ef537.png)


Pontos de extremidade em tempo real

![image](https://user-images.githubusercontent.com/74794415/122689268-c9efdf00-d1f7-11eb-8fb2-22d9d4416480.png)


import urllib.request
import json
import os
import ssl

def allowSelfSignedHttps(allowed):
    # bypass the server certificate verification on client side
    if allowed and not os.environ.get('PYTHONHTTPSVERIFY', '') and getattr(ssl, '_create_unverified_context', None):
        ssl._create_default_https_context = ssl._create_unverified_context

allowSelfSignedHttps(True) # this line is needed if you use self-signed certificate in your scoring service.

// Request data goes here
data = {
    "Inputs": {
        "WebServiceInput0":
        [
            {
                'NU_ANO': "2019",
                'CO_IES': "1",
                'CO_CATEGAD': "10002",
                'CO_ORGACAD': "10028",
                'CO_GRUPO': "5710",
                'CO_CURSO': "3",
                'CO_MODALIDADE': "1",
                'CO_MUNIC_CURSO': "5103403",
                'CO_UF_CURSO': "51",
                'CO_REGIAO_CURSO': "5",
                'NU_IDADE': "27",
                'TP_SEXO': "M",
                'ANO_FIM_EM': "2010",
                'ANO_IN_GRAD': "2012",
                'CO_TURNO_GRADUACAO': "3",
                'TP_INSCRICAO_ADM': "1",
                'TP_INSCRICAO': "0",
                'NU_ITEM_OFG': "8",
                'NU_ITEM_OFG_Z': "1",
                'NU_ITEM_OFG_X': "0",
                'NU_ITEM_OFG_N': "0",
                'NU_ITEM_OCE': "27",
                'NU_ITEM_OCE_Z': "0",
                'NU_ITEM_OCE_X': "7",
                'NU_ITEM_OCE_N': "0",
                'DS_VT_GAB_OFG_ORIG': "ZDCBCCDB",
                'DS_VT_GAB_OFG_FIN': "ZDCBCCDB",
                'DS_VT_GAB_OCE_ORIG': "ABECDDEABDECCBCDEBAEDCDBAAA",
                'DS_VT_GAB_OCE_FIN': "ABEXDDEABDECXXXDXBAEDCXXAAA",
                'DS_VT_ESC_OFG': "DACBCBDD",
                'DS_VT_ACE_OFG': "80111010",
                'DS_VT_ESC_OCE': "ABEEDDDAADEAEECBBABECCACBAA",
                'DS_VT_ACE_OCE': "1.119110101109991e+26",
                'TP_PRES': "555",
                'TP_PR_GER': "555",
                'TP_PR_OB_FG': "555",
                'TP_PR_DI_FG': "555",
                'TP_PR_OB_CE': "555",
                'TP_PR_DI_CE': "555",
                'TP_SFG_D1': "336",
                'TP_SFG_D2': "555",
                'TP_SCE_D1': "555",
                'TP_SCE_D2': "555",
                'TP_SCE_D3': "555",
                'NT_GER': "51,9",
                'NT_FG': "36,5",
                'NT_OBJ_FG': "57,1",
                'NT_DIS_FG': "5,5",
                'NT_FG_D1': "0",
                'NT_FG_D1_PT': "45",
                'NT_FG_D1_CT': "0",
                'NT_FG_D2': "11",
                'NT_FG_D2_PT': "55",
                'NT_FG_D2_CT': "0",
                'NT_CE': "57",
                'NT_OBJ_CE': "60",
                'NT_DIS_CE': "40",
                'NT_CE_D1': "20",
                'NT_CE_D2': "0",
                'NT_CE_D3': "100",
                'CO_RS_I1': "E",
                'CO_RS_I2': "D",
                'CO_RS_I3': "C",
                'CO_RS_I4': "D",
                'CO_RS_I5': "B",
                'CO_RS_I6': "C",
                'CO_RS_I7': "B",
                'CO_RS_I8': "D",
                'CO_RS_I9': ".",
                'QE_I01': "E",
                'QE_I02': "C",
                'QE_I03': "A",
                'QE_I04': "D",
                'QE_I05': "E",
                'QE_I06': "C",
                'QE_I07': "D",
                'QE_I08': "B",
                'QE_I09': "C",
                'QE_I10': "A",
                'QE_I11': "A",
                'QE_I12': "A",
                'QE_I13': "A",
                'QE_I14': "A",
                'QE_I15': "A",
                'QE_I16': "35",
                'QE_I17': "B",
                'QE_I18': "A",
                'QE_I19': "B",
                'QE_I20': "G",
                'QE_I21': "A",
                'QE_I22': "B",
                'QE_I23': "D",
                'QE_I24': "A",
                'QE_I25': "E",
                'QE_I26': "C",
                'QE_I27': "7",
                'QE_I28': "1",
                'QE_I29': "7",
                'QE_I30': "1",
                'QE_I31': "3",
                'QE_I32': "5",
                'QE_I33': "7",
                'QE_I34': "7",
                'QE_I35': "1",
                'QE_I36': "1",
                'QE_I37': "2",
                'QE_I38': "6",
                'QE_I39': "4",
                'QE_I40': "1",
                'QE_I41': "3",
                'QE_I42': "6",
                'QE_I43': "1",
                'QE_I44': "1",
                'QE_I45': "1",
                'QE_I46': "1",
                'QE_I47': "1",
                'QE_I48': "2",
                'QE_I49': "2",
                'QE_I50': "6",
                'QE_I51': "2",
                'QE_I52': "1",
                'QE_I53': "8",
                'QE_I54': "1",
                'QE_I55': "3",
                'QE_I56': "2",
                'QE_I57': "5",
                'QE_I58': "6",
                'QE_I59': "2",
                'QE_I60': "5",
                'QE_I61': "1",
                'QE_I62': "1",
                'QE_I63': "2",
                'QE_I64': "5",
                'QE_I65': "8",
                'QE_I66': "7",
                'QE_I67': "1",
                'QE_I68': "2",
            },
        ],
    },
    "GlobalParameters": {
    }
}

body = str.encode(json.dumps(data))

url = 'http://bfc50066-b4ad-43bc-a300-0cc19bcc961d.southcentralus.azurecontainer.io/score'
api_key = 'ot35XV1SHrn5mC5OQDcrabesFmSd5DUn' # Replace this with the API key for the web service
headers = {'Content-Type':'application/json', 'Authorization':('Bearer '+ api_key)}

req = urllib.request.Request(url, body, headers)

try:
    response = urllib.request.urlopen(req)

    result = response.read()
    print(result)
except urllib.error.HTTPError as error:
    print("The request failed with status code: " + str(error.code))

    # Print the headers - they include the requert ID and the timestamp, which are useful for debugging the failure
    print(error.info())
    print(json.loads(error.read().decode("utf8", 'ignore')))
