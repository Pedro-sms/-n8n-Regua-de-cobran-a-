{
  "nodes": [
    {
      "parameters": {
        "url": "=https://e-api.sge.com.br/api/emp/aluno/{{ $json.Cliente.CPF }}/parcelas",
        "sendHeaders": true,
        "headerParameters": {
          "parameters": [
            {
              "name": "Accept",
              "value": "application/json"
            },
            {
              "name": "Authorization",
              "value": "Basic MTY2OTg2NjcwMDAxNDA6ZTc2ZTFiZDJjNjE5NDcyMWFjY2Y0OTIzYzQzOGUzOTc="
            }
          ]
        },
        "options": {}
      },
      "type": "n8n-nodes-base.httpRequest",
      "typeVersion": 4.2,
      "position": [
        -432,
        -528
      ],
      "id": "ec66d471-315a-4f19-a748-2dead71ed7eb",
      "name": "Busca CPF"
    },
    {
      "parameters": {
        "url": "=https://e-api.sge.com.br/api/emp/financeiro/cobranca",
        "sendQuery": true,
        "queryParameters": {
          "parameters": [
            {
              "name": "vencimentoInicial",
              "value": "={{ $now.plus(5, 'days').format('yyyy-MM-dd') }}"
            },
            {
              "name": "vencimentoFinal",
              "value": "={{ $now.plus(5, 'days').format('yyyy-MM-dd') }}"
            }
          ]
        },
        "sendHeaders": true,
        "headerParameters": {
          "parameters": [
            {
              "name": "Accept",
              "value": "application/json"
            },
            {
              "name": "Authorization",
              "value": "Basic MTY2OTg2NjcwMDAxNDA6ZTc2ZTFiZDJjNjE5NDcyMWFjY2Y0OTIzYzQzOGUzOTc="
            }
          ]
        },
        "options": {}
      },
      "type": "n8n-nodes-base.httpRequest",
      "typeVersion": 4.2,
      "position": [
        -656,
        -528
      ],
      "id": "ef854b03-2d22-43b6-b3be-07195a311198",
      "name": "Busca cobrança"
    },
    {
      "parameters": {
        "content": "## D - 5 \n",
        "height": 816,
        "width": 2256
      },
      "type": "n8n-nodes-base.stickyNote",
      "position": [
        -928,
        -896
      ],
      "typeVersion": 1,
      "id": "b78bd3a6-eaa2-4fd4-b459-9a395409c20c",
      "name": "Sticky Note"
    },
    {
      "parameters": {
        "rule": {
          "interval": [
            {}
          ]
        }
      },
      "type": "n8n-nodes-base.scheduleTrigger",
      "typeVersion": 1.2,
      "position": [
        -896,
        304
      ],
      "id": "94e5d226-b734-48dc-96f0-4d9ae5e8547d",
      "name": "Schedule Trigger1"
    },
    {
      "parameters": {
        "url": "=https://e-api.sge.com.br/api/emp/aluno/{{ $json.Cliente.CPF }}/parcelas",
        "sendHeaders": true,
        "headerParameters": {
          "parameters": [
            {
              "name": "Accept",
              "value": "application/json"
            },
            {
              "name": "Authorization",
              "value": "Basic MTY2OTg2NjcwMDAxNDA6ZTc2ZTFiZDJjNjE5NDcyMWFjY2Y0OTIzYzQzOGUzOTc="
            }
          ]
        },
        "options": {}
      },
      "type": "n8n-nodes-base.httpRequest",
      "typeVersion": 4.2,
      "position": [
        -448,
        304
      ],
      "id": "c74f5a2b-68b0-49df-bbb8-23476d3b01db",
      "name": "Busca CPF1"
    },
    {
      "parameters": {
        "url": "=https://e-api.sge.com.br/api/emp/financeiro/cobranca",
        "sendQuery": true,
        "queryParameters": {
          "parameters": [
            {
              "name": "vencimentoInicial",
              "value": "={{ $now.format('yyyy-MM-dd') }}"
            },
            {
              "name": "vencimentoFinal",
              "value": "={{ $now.format('yyyy-MM-dd') }}"
            }
          ]
        },
        "sendHeaders": true,
        "headerParameters": {
          "parameters": [
            {
              "name": "Accept",
              "value": "application/json"
            },
            {
              "name": "Authorization",
              "value": "Basic MTY2OTg2NjcwMDAxNDA6ZTc2ZTFiZDJjNjE5NDcyMWFjY2Y0OTIzYzQzOGUzOTc="
            }
          ]
        },
        "options": {}
      },
      "type": "n8n-nodes-base.httpRequest",
      "typeVersion": 4.2,
      "position": [
        -672,
        304
      ],
      "id": "6431388d-4ff7-4380-856e-7ca082114718",
      "name": "Busca cobrança1"
    },
    {
      "parameters": {
        "content": "## D - 0\n",
        "height": 848,
        "width": 2256,
        "color": 3
      },
      "type": "n8n-nodes-base.stickyNote",
      "position": [
        -928,
        -64
      ],
      "typeVersion": 1,
      "id": "2c2c1140-e28d-4e16-b631-80f46d878173",
      "name": "Sticky Note1"
    },
    {
      "parameters": {
        "conditions": {
          "options": {
            "caseSensitive": true,
            "leftValue": "",
            "typeValidation": "strict",
            "version": 2
          },
          "conditions": [
            {
              "id": "12c956ca-5409-405a-ba3b-5c8de31501f7",
              "leftValue": "={{ $json.DataVencimento.toDateTime().format('yyyy-MM-dd') }}",
              "rightValue": "={{ $now.plus(5, 'days').format('yyyy-MM-dd') }}",
              "operator": {
                "type": "string",
                "operation": "equals",
                "name": "filter.operator.equals"
              }
            }
          ],
          "combinator": "and"
        },
        "options": {}
      },
      "type": "n8n-nodes-base.filter",
      "typeVersion": 2.2,
      "position": [
        -208,
        -528
      ],
      "id": "9156e409-55ca-4686-b28f-c19acf057459",
      "name": "filtro data"
    },
    {
      "parameters": {
        "rule": {
          "interval": [
            {}
          ]
        }
      },
      "type": "n8n-nodes-base.scheduleTrigger",
      "typeVersion": 1.2,
      "position": [
        -880,
        -528
      ],
      "id": "9b44e51d-d737-439e-a3cf-44f77cabbd20",
      "name": "Schedule Trigger"
    },
    {
      "parameters": {
        "url": "https://chat-10api.jetsalesbrasil.com/contacts/",
        "sendQuery": true,
        "queryParameters": {
          "parameters": [
            {
              "name": "pageNumber",
              "value": "1"
            },
            {
              "name": "hasMore",
              "value": "true"
            },
            {
              "name": "searchParam",
              "value": "=557591105310"
            }
          ]
        },
        "sendHeaders": true,
        "headerParameters": {
          "parameters": [
            {
              "name": "Authorization",
              "value": "Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0ZW5hbnRJZCI6NSwicHJvZmlsZSI6ImFkbWluIiwic2Vzc2lvbklkIjo3LCJjaGFubmVsVHlwZSI6IndoYXRzYXBwIiwiaWF0IjoxNzU1NTE4NTQyLCJleHAiOjE4MTg1OTA1NDJ9.bL0EuUunp9ScP2d0yC1HQvTbzLNEAJ6ctLXbvxs23Oo"
            }
          ]
        },
        "options": {}
      },
      "type": "n8n-nodes-base.httpRequest",
      "typeVersion": 4.2,
      "position": [
        464,
        -336
      ],
      "id": "532d9990-415c-4771-9318-46b7462c6d52",
      "name": "Buscar contato"
    },
    {
      "parameters": {
        "method": "POST",
        "url": "https://chat-10api.jetsalesbrasil.com/contacts",
        "sendHeaders": true,
        "headerParameters": {
          "parameters": [
            {
              "name": "Authorization",
              "value": "Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0ZW5hbnRJZCI6NSwicHJvZmlsZSI6ImFkbWluIiwic2Vzc2lvbklkIjo3LCJjaGFubmVsVHlwZSI6IndoYXRzYXBwIiwiaWF0IjoxNzU1NTE4NTQyLCJleHAiOjE4MTg1OTA1NDJ9.bL0EuUunp9ScP2d0yC1HQvTbzLNEAJ6ctLXbvxs23Oo"
            }
          ]
        },
        "sendBody": true,
        "specifyBody": "json",
        "jsonBody": "={\n    \"name\": {{ $json.contacts[0].id }},\n    \"number\": \"{{$json.contacts[0].number }}\",\n    \"wallets\": [],\n    \"extraInfo\": [],\n    \"defaultDepartment\": null,\n    \"tags\": [],\n    \"customFields\": {}\n}\n",
        "options": {}
      },
      "type": "n8n-nodes-base.httpRequest",
      "typeVersion": 4.2,
      "position": [
        912,
        -432
      ],
      "id": "b66946d5-1379-4846-8b78-04ece8fc4174",
      "name": "Criar contato"
    },
    {
      "parameters": {
        "method": "POST",
        "url": "https://chat-10api.jetsalesbrasil.com/tickets",
        "sendHeaders": true,
        "headerParameters": {
          "parameters": [
            {
              "name": "Authorization",
              "value": "Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0ZW5hbnRJZCI6NSwicHJvZmlsZSI6ImFkbWluIiwic2Vzc2lvbklkIjo3LCJjaGFubmVsVHlwZSI6IndoYXRzYXBwIiwiaWF0IjoxNzU1NTE4NTQyLCJleHAiOjE4MTg1OTA1NDJ9.bL0EuUunp9ScP2d0yC1HQvTbzLNEAJ6ctLXbvxs23Oo"
            }
          ]
        },
        "sendBody": true,
        "specifyBody": "json",
        "jsonBody": "=\"jsonBody\": \"={{ { \n  contactId: $json.contacts?.[0]?.id, \n  mini: false, \n  number: String($json.contacts?.[0]?.number || ''), \n  isActiveDemand: true, \n  channel: 'whatsapp', \n  status: 'open', \n  whatsappId: 7, \n  queueId: null, \n  body: '*teste*:\\\\nola', \n  templateId: null, \n  params: [], \n  templateMediaId: null, \n  idFront: '1b6d8961-172b-4ae3-aae3-e0f59dd8744c', \n  typeTemplate: null \n} }}\"\n",
        "options": {
          "redirect": {
            "redirect": {}
          }
        }
      },
      "type": "n8n-nodes-base.httpRequest",
      "typeVersion": 4.2,
      "position": [
        912,
        -240
      ],
      "id": "df397bf7-9b1a-4074-af4e-b42c94189c72",
      "name": "criar ticket",
      "onError": "continueErrorOutput"
    },
    {
      "parameters": {
        "method": "POST",
        "url": "https://chat-10api.jetsalesbrasil.com/tickets",
        "sendHeaders": true,
        "headerParameters": {
          "parameters": [
            {
              "name": "Authorization",
              "value": "Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0ZW5hbnRJZCI6NSwicHJvZmlsZSI6ImFkbWluIiwic2Vzc2lvbklkIjo3LCJjaGFubmVsVHlwZSI6IndoYXRzYXBwIiwiaWF0IjoxNzU1NTE4NTQyLCJleHAiOjE4MTg1OTA1NDJ9.bL0EuUunp9ScP2d0yC1HQvTbzLNEAJ6ctLXbvxs23Oo"
            },
            {
              "name": "Content-Type",
              "value": "application/json"
            },
            {
              "name": "host",
              "value": "chat-10api.jetsalesbrasil.com"
            }
          ]
        },
        "sendBody": true,
        "specifyBody": "json",
        "jsonBody": "={\n  \"fromMe\": true,\n  \"body\": \"Olá,  {{ $json.contacts[0].name }}! Tudo bem?\\n\\nEstamos passando apenas para lembrar que você tem um título pendente.\\n\\n💰 Valor:R${{ $('Filtra link').item.json.Valor }} \\n📅 Vencimento:{{ new Date($('Filtra link').item.json.DataVencimento).toLocaleDateString('pt-BR', { timeZone: 'America/Bahia' }) }} \\n🔗 Link:{{ $('Filtra link').item.json.UrlBoleto }}\\n\\nCaso o pagamento já tenha sido realizado, por favor, desconsidere esta mensagem.\",\n  \"idFront\": \"6f94004c-a9a0-4819-94c3-6ad53fdc7717\",\n  \"note\": false\n}\n",
        "options": {}
      },
      "type": "n8n-nodes-base.httpRequest",
      "typeVersion": 4.2,
      "position": [
        1136,
        -432
      ],
      "id": "afbd6d08-1582-4dbe-bafa-e778fd0ce8b4",
      "name": "mandar mensagem"
    },
    {
      "parameters": {
        "method": "POST",
        "url": "=https://chat-10api.jetsalesbrasil.com/messages/{{ $json.contacts[0].id }}",
        "sendHeaders": true,
        "headerParameters": {
          "parameters": [
            {
              "name": "Authorization",
              "value": "=Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0ZW5hbnRJZCI6NSwicHJvZmlsZSI6ImFkbWluIiwic2Vzc2lvbklkIjo3LCJjaGFubmVsVHlwZSI6IndoYXRzYXBwIiwiaWF0IjoxNzU1NTE4NTQyLCJleHAiOjE4MTg1OTA1NDJ9.bL0EuUunp9ScP2d0yC1HQvTbzLNEAJ6ctLXbvxs23Oo"
            }
          ]
        },
        "sendBody": true,
        "specifyBody": "json",
        "jsonBody": "={\n  \"fromMe\": true,\n  \"body\": \"Olá,  {{ $json.contacts[0].name }}! Tudo bem?\\n\\nEstamos passando apenas para lembrar que você tem um título pendente.\\n\\n💰 Valor:R${{ $('Filtra link').item.json.Valor }} \\n📅 Vencimento:{{ new Date($('Filtra link').item.json.DataVencimento).toLocaleDateString('pt-BR', { timeZone: 'America/Bahia' }) }} \\n🔗 Link:{{ $('Filtra link').item.json.UrlBoleto }}\\n\\nCaso o pagamento já tenha sido realizado, por favor, desconsidere esta mensagem.\",\n  \"idFront\": \"6f94004c-a9a0-4819-94c3-6ad53fdc7717\",\n  \"note\": false\n}\n",
        "options": {}
      },
      "type": "n8n-nodes-base.httpRequest",
      "typeVersion": 4.2,
      "position": [
        1136,
        -240
      ],
      "id": "a32b0ba9-364e-4dd9-a38e-3f35f4866f29",
      "name": "mandar mensagem3"
    },
    {
      "parameters": {
        "rule": {
          "interval": [
            {}
          ]
        }
      },
      "type": "n8n-nodes-base.scheduleTrigger",
      "typeVersion": 1.2,
      "position": [
        -896,
        1152
      ],
      "id": "bb6fbb45-3d47-49f6-b719-076494701fbb",
      "name": "Schedule Trigger2"
    },
    {
      "parameters": {
        "url": "=https://e-api.sge.com.br/api/emp/aluno/{{ $json.Cliente.CPF }}/parcelas",
        "sendHeaders": true,
        "headerParameters": {
          "parameters": [
            {
              "name": "Accept",
              "value": "application/json"
            },
            {
              "name": "Authorization",
              "value": "Basic MTY2OTg2NjcwMDAxNDA6ZTc2ZTFiZDJjNjE5NDcyMWFjY2Y0OTIzYzQzOGUzOTc="
            }
          ]
        },
        "options": {}
      },
      "type": "n8n-nodes-base.httpRequest",
      "typeVersion": 4.2,
      "position": [
        -448,
        1152
      ],
      "id": "7108e001-b6e4-4fcf-9b07-09f8249bc429",
      "name": "Busca CPF2"
    },
    {
      "parameters": {
        "url": "=https://e-api.sge.com.br/api/emp/financeiro/cobranca",
        "sendQuery": true,
        "queryParameters": {
          "parameters": [
            {
              "name": "vencimentoInicial",
              "value": "={{ $now.minus(5, 'days').format('yyyy-MM-dd') }}"
            },
            {
              "name": "vencimentoFinal",
              "value": "={{ $now.minus(5, 'days').format('yyyy-MM-dd') }}"
            }
          ]
        },
        "sendHeaders": true,
        "headerParameters": {
          "parameters": [
            {
              "name": "Accept",
              "value": "application/json"
            },
            {
              "name": "Authorization",
              "value": "Basic MTY2OTg2NjcwMDAxNDA6ZTc2ZTFiZDJjNjE5NDcyMWFjY2Y0OTIzYzQzOGUzOTc="
            }
          ]
        },
        "options": {}
      },
      "type": "n8n-nodes-base.httpRequest",
      "typeVersion": 4.2,
      "position": [
        -672,
        1152
      ],
      "id": "12425077-3d38-4de3-b992-039e9ecfb724",
      "name": "Busca cobrança2"
    },
    {
      "parameters": {
        "conditions": {
          "options": {
            "caseSensitive": true,
            "leftValue": "",
            "typeValidation": "strict",
            "version": 2
          },
          "conditions": [
            {
              "id": "12c956ca-5409-405a-ba3b-5c8de31501f7",
              "leftValue": "={{ $json.DataVencimento.toDateTime().format('yyyy-MM-dd') }}",
              "rightValue": "={{ $now.plus(5, 'days').format('yyyy-MM-dd') }}",
              "operator": {
                "type": "string",
                "operation": "equals",
                "name": "filter.operator.equals"
              }
            }
          ],
          "combinator": "and"
        },
        "options": {}
      },
      "type": "n8n-nodes-base.filter",
      "typeVersion": 2.2,
      "position": [
        -224,
        1152
      ],
      "id": "204e25fa-a11e-48df-a1b2-e2960d016784",
      "name": "Filter"
    },
    {
      "parameters": {
        "content": "## D + 5\n",
        "height": 816,
        "width": 2256,
        "color": 4
      },
      "type": "n8n-nodes-base.stickyNote",
      "position": [
        -928,
        816
      ],
      "typeVersion": 1,
      "id": "99fe2aae-0c23-4f3c-bad9-24b71f69dd69",
      "name": "Sticky Note2"
    },
    {
      "parameters": {
        "rule": {
          "interval": [
            {}
          ]
        }
      },
      "type": "n8n-nodes-base.scheduleTrigger",
      "typeVersion": 1.2,
      "position": [
        -912,
        2048
      ],
      "id": "e4f7fccd-2c12-49f5-a4e0-298ff3d765c6",
      "name": "Schedule Trigger3"
    },
    {
      "parameters": {
        "url": "=https://e-api.sge.com.br/api/emp/aluno/{{ $json.Cliente.CPF }}/parcelas",
        "sendHeaders": true,
        "headerParameters": {
          "parameters": [
            {
              "name": "Accept",
              "value": "application/json"
            },
            {
              "name": "Authorization",
              "value": "Basic MTY2OTg2NjcwMDAxNDA6ZTc2ZTFiZDJjNjE5NDcyMWFjY2Y0OTIzYzQzOGUzOTc="
            }
          ]
        },
        "options": {
          "batching": {
            "batch": {
              "batchSize": 1
            }
          }
        }
      },
      "type": "n8n-nodes-base.httpRequest",
      "typeVersion": 4.2,
      "position": [
        -464,
        2048
      ],
      "id": "3f35f921-6b4c-47cf-8865-62e73d717c77",
      "name": "Busca CPF3",
      "onError": "continueErrorOutput"
    },
    {
      "parameters": {
        "url": "=https://e-api.sge.com.br/api/emp/financeiro/cobranca",
        "sendQuery": true,
        "queryParameters": {
          "parameters": [
            {
              "name": "vencimentoInicial",
              "value": "={{ $now.minus(30, 'days').format('yyyy-MM-dd') }}"
            },
            {
              "name": "vencimentoFinal",
              "value": "={{ $now.minus(30, 'days').format('yyyy-MM-dd') }}"
            }
          ]
        },
        "sendHeaders": true,
        "headerParameters": {
          "parameters": [
            {
              "name": "Accept",
              "value": "application/json"
            },
            {
              "name": "Authorization",
              "value": "Basic MTY2OTg2NjcwMDAxNDA6ZTc2ZTFiZDJjNjE5NDcyMWFjY2Y0OTIzYzQzOGUzOTc="
            }
          ]
        },
        "options": {}
      },
      "type": "n8n-nodes-base.httpRequest",
      "typeVersion": 4.2,
      "position": [
        -688,
        2048
      ],
      "id": "370d100e-4acd-40ff-8f38-59e028096bba",
      "name": "Busca cobrança3"
    },
    {
      "parameters": {
        "conditions": {
          "options": {
            "caseSensitive": true,
            "leftValue": "",
            "typeValidation": "strict",
            "version": 2
          },
          "conditions": [
            {
              "id": "12c956ca-5409-405a-ba3b-5c8de31501f7",
              "leftValue": "={{ $json.DataVencimento.toDateTime().format('yyyy-MM-dd') }}",
              "rightValue": "={{ $now.minus(30, 'days').format('yyyy-MM-dd') }}",
              "operator": {
                "type": "string",
                "operation": "equals",
                "name": "filter.operator.equals"
              }
            }
          ],
          "combinator": "and"
        },
        "options": {}
      },
      "type": "n8n-nodes-base.filter",
      "typeVersion": 2.2,
      "position": [
        -240,
        2048
      ],
      "id": "269aaf35-d58c-4cbb-94ba-8bd4632412c6",
      "name": "Filter2"
    },
    {
      "parameters": {
        "content": "## D + 30\n",
        "height": 864,
        "width": 2272,
        "color": 5
      },
      "type": "n8n-nodes-base.stickyNote",
      "position": [
        -944,
        1664
      ],
      "typeVersion": 1,
      "id": "46d8195f-3e15-44a5-abc1-3606b9fab452",
      "name": "Sticky Note3"
    },
    {
      "parameters": {
        "rule": {
          "interval": [
            {}
          ]
        }
      },
      "type": "n8n-nodes-base.scheduleTrigger",
      "typeVersion": 1.2,
      "position": [
        -896,
        2880
      ],
      "id": "117b7340-7769-44cd-be08-d5931ae92907",
      "name": "Schedule Trigger4"
    },
    {
      "parameters": {
        "url": "=https://e-api.sge.com.br/api/emp/aluno/{{ $json.Cliente.CPF }}/parcelas",
        "sendHeaders": true,
        "headerParameters": {
          "parameters": [
            {
              "name": "Accept",
              "value": "application/json"
            },
            {
              "name": "Authorization",
              "value": "Basic MTY2OTg2NjcwMDAxNDA6ZTc2ZTFiZDJjNjE5NDcyMWFjY2Y0OTIzYzQzOGUzOTc="
            }
          ]
        },
        "options": {
          "batching": {
            "batch": {
              "batchSize": 1
            }
          }
        }
      },
      "type": "n8n-nodes-base.httpRequest",
      "typeVersion": 4.2,
      "position": [
        -448,
        2880
      ],
      "id": "f60de0e6-53f6-4a17-97a3-e507cf21b10f",
      "name": "Busca CPF4",
      "onError": "continueErrorOutput"
    },
    {
      "parameters": {
        "url": "=https://e-api.sge.com.br/api/emp/financeiro/cobranca",
        "sendQuery": true,
        "queryParameters": {
          "parameters": [
            {
              "name": "vencimentoInicial",
              "value": "={{ $now.minus(60, 'days').format('yyyy-MM-dd') }}"
            },
            {
              "name": "vencimentoFinal",
              "value": "={{ $now.minus(60, 'days').format('yyyy-MM-dd') }}"
            }
          ]
        },
        "sendHeaders": true,
        "headerParameters": {
          "parameters": [
            {
              "name": "Accept",
              "value": "application/json"
            },
            {
              "name": "Authorization",
              "value": "Basic MTY2OTg2NjcwMDAxNDA6ZTc2ZTFiZDJjNjE5NDcyMWFjY2Y0OTIzYzQzOGUzOTc="
            }
          ]
        },
        "options": {}
      },
      "type": "n8n-nodes-base.httpRequest",
      "typeVersion": 4.2,
      "position": [
        -672,
        2880
      ],
      "id": "8dc3b891-4b16-462b-81dc-a9ab80b7dc4e",
      "name": "Busca cobrança4"
    },
    {
      "parameters": {
        "conditions": {
          "options": {
            "caseSensitive": true,
            "leftValue": "",
            "typeValidation": "strict",
            "version": 2
          },
          "conditions": [
            {
              "id": "12c956ca-5409-405a-ba3b-5c8de31501f7",
              "leftValue": "={{ $json.DataVencimento.toDateTime().format('yyyy-MM-dd') }}",
              "rightValue": "={{ $now.minus(60, 'days').format('yyyy-MM-dd') }}",
              "operator": {
                "type": "string",
                "operation": "equals",
                "name": "filter.operator.equals"
              }
            }
          ],
          "combinator": "and"
        },
        "options": {}
      },
      "type": "n8n-nodes-base.filter",
      "typeVersion": 2.2,
      "position": [
        -224,
        2880
      ],
      "id": "8b884f22-196d-4b48-8153-7e966e9273b0",
      "name": "Filter3"
    },
    {
      "parameters": {
        "content": "## D + 60\n",
        "height": 800,
        "width": 2272,
        "color": 6
      },
      "type": "n8n-nodes-base.stickyNote",
      "position": [
        -944,
        2560
      ],
      "typeVersion": 1,
      "id": "aaf1f11c-da06-4c4b-ad18-2cab8bff67a8",
      "name": "Sticky Note4"
    },
    {
      "parameters": {
        "assignments": {
          "assignments": [
            {
              "id": "e6333f86-745e-4f82-b4b5-cb6ebb76ac6a",
              "name": "telefone",
              "value": "={{\n  (() => {\n    // 1) pega o telefone pelo CPF e deixa só dígitos\n    let tel = (\n      ($('Busca cobrança').all().map(i => i.json.Cliente).flat()\n        .find(c => c.CPF === $json.CPF) || {}\n      ).Telefone || ''\n    ).replace(/\\D/g, '');\n\n    if (!tel) return '';\n\n    // 2) trabalha no formato local (sem 55) para detectar/remover o 9º dígito\n    let local = tel.startsWith('55') ? tel.slice(2) : tel;\n\n    // se for celular (11 dígitos) e tiver '9' logo após o DDD, remove\n    if (local.length === 11 && local[2] === '9') {\n      local = local.slice(0, 2) + local.slice(3);\n    }\n\n    // 3) remonta e aplica a regra do 55: se final tiver < 13, prefixa 55 (uma vez)\n    let out = tel.startsWith('55') ? '55' + local : local;\n    if (out.length < 13) out = '55' + local;\n\n    return out;\n  })()\n}}\n",
              "type": "string"
            },
            {
              "id": "551f5d8f-9ee9-47c7-8c43-7c090484feaa",
              "name": "nome",
              "value": "={{ \n  ( $('Busca cobrança').all().map(i => i.json.Cliente).flat()\n    .find(c => c.CPF === $json.CPF) || {} \n  ).Nome || '' \n}}",
              "type": "string"
            },
            {
              "id": "10c7426b-a3bb-498b-ad4c-0a21db5365f9",
              "name": "email",
              "value": "={{   (     $('Busca cobrança').all().map(i => i.json.Cliente).flat()       .find(c => c.CPF === $json.CPF) || {}   ).ResponsavelEmail || '' }}",
              "type": "string"
            }
          ]
        },
        "options": {}
      },
      "type": "n8n-nodes-base.set",
      "typeVersion": 3.4,
      "position": [
        240,
        -720
      ],
      "id": "a097c61a-793a-424e-9807-e247dddfbb7b",
      "name": "Edit Fields6"
    },
    {
      "parameters": {
        "url": "https://chat-10api.jetsalesbrasil.com/contacts/",
        "sendQuery": true,
        "queryParameters": {
          "parameters": [
            {
              "name": "pageNumber",
              "value": "1"
            },
            {
              "name": "hasMore",
              "value": "true"
            },
            {
              "name": "searchParam",
              "value": "=557591105310"
            }
          ]
        },
        "sendHeaders": true,
        "headerParameters": {
          "parameters": [
            {
              "name": "Authorization",
              "value": "Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0ZW5hbnRJZCI6NSwicHJvZmlsZSI6ImFkbWluIiwic2Vzc2lvbklkIjo3LCJjaGFubmVsVHlwZSI6IndoYXRzYXBwIiwiaWF0IjoxNzU1NTE4NTQyLCJleHAiOjE4MTg1OTA1NDJ9.bL0EuUunp9ScP2d0yC1HQvTbzLNEAJ6ctLXbvxs23Oo"
            }
          ]
        },
        "options": {}
      },
      "type": "n8n-nodes-base.httpRequest",
      "typeVersion": 4.2,
      "position": [
        464,
        -720
      ],
      "id": "d2729f4c-5bcb-4f63-be46-15cbcc79dd83",
      "name": "Buscar contato6"
    },
    {
      "parameters": {
        "method": "POST",
        "url": "https://chat-10api.jetsalesbrasil.com/contacts",
        "sendHeaders": true,
        "headerParameters": {
          "parameters": [
            {
              "name": "Authorization",
              "value": "Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0ZW5hbnRJZCI6NSwicHJvZmlsZSI6ImFkbWluIiwic2Vzc2lvbklkIjo3LCJjaGFubmVsVHlwZSI6IndoYXRzYXBwIiwiaWF0IjoxNzU1NTE4NTQyLCJleHAiOjE4MTg1OTA1NDJ9.bL0EuUunp9ScP2d0yC1HQvTbzLNEAJ6ctLXbvxs23Oo"
            }
          ]
        },
        "sendBody": true,
        "specifyBody": "json",
        "jsonBody": "={\n    \"name\": {{ $json.contacts[0].id }},\n    \"number\": \"{{$json.contacts[0].number }}\",\n    \"wallets\": [],\n    \"extraInfo\": [],\n    \"defaultDepartment\": null,\n    \"tags\": [],\n    \"customFields\": {}\n}\n",
        "options": {}
      },
      "type": "n8n-nodes-base.httpRequest",
      "typeVersion": 4.2,
      "position": [
        912,
        -816
      ],
      "id": "9f7dba5b-344a-4fcf-82fb-c87f35769578",
      "name": "Criar contato6"
    },
    {
      "parameters": {
        "method": "POST",
        "url": "https://chat-10api.jetsalesbrasil.com/tickets",
        "sendHeaders": true,
        "headerParameters": {
          "parameters": [
            {
              "name": "Authorization",
              "value": "Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0ZW5hbnRJZCI6NSwicHJvZmlsZSI6ImFkbWluIiwic2Vzc2lvbklkIjo3LCJjaGFubmVsVHlwZSI6IndoYXRzYXBwIiwiaWF0IjoxNzU1NTE4NTQyLCJleHAiOjE4MTg1OTA1NDJ9.bL0EuUunp9ScP2d0yC1HQvTbzLNEAJ6ctLXbvxs23Oo"
            }
          ]
        },
        "sendBody": true,
        "specifyBody": "json",
        "jsonBody": "=\"jsonBody\": \"={{ { \n  contactId: $json.contacts?.[0]?.id, \n  mini: false, \n  number: String($json.contacts?.[0]?.number || ''), \n  isActiveDemand: true, \n  channel: 'whatsapp', \n  status: 'open', \n  whatsappId: 7, \n  queueId: null, \n  body: '*teste*:\\\\nola', \n  templateId: null, \n  params: [], \n  templateMediaId: null, \n  idFront: '1b6d8961-172b-4ae3-aae3-e0f59dd8744c', \n  typeTemplate: null \n} }}\"\n",
        "options": {
          "redirect": {
            "redirect": {}
          }
        }
      },
      "type": "n8n-nodes-base.httpRequest",
      "typeVersion": 4.2,
      "position": [
        912,
        -624
      ],
      "id": "34bf56ca-b59f-4930-9287-e01f0fb1877c",
      "name": "criar ticket6",
      "onError": "continueErrorOutput"
    },
    {
      "parameters": {
        "method": "POST",
        "url": "https://chat-10api.jetsalesbrasil.com/tickets",
        "sendHeaders": true,
        "headerParameters": {
          "parameters": [
            {
              "name": "Authorization",
              "value": "Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0ZW5hbnRJZCI6NSwicHJvZmlsZSI6ImFkbWluIiwic2Vzc2lvbklkIjo3LCJjaGFubmVsVHlwZSI6IndoYXRzYXBwIiwiaWF0IjoxNzU1NTE4NTQyLCJleHAiOjE4MTg1OTA1NDJ9.bL0EuUunp9ScP2d0yC1HQvTbzLNEAJ6ctLXbvxs23Oo"
            },
            {
              "name": "Content-Type",
              "value": "application/json"
            },
            {
              "name": "host",
              "value": "chat-10api.jetsalesbrasil.com"
            }
          ]
        },
        "sendBody": true,
        "specifyBody": "json",
        "jsonBody": "={\n  \"mini\": false,\n  \"contactId\": {{$json.id}},\n  \"number\": \"{{$json.number}}\",\n  \"isActiveDemand\": true,\n  \"channel\": \"whatsapp\",\n  \"status\": \"open\",\n  \"whatsappId\": 7,\n  \"queueId\": null,\n  \"body\": \"Olá, {{ $json.contacts[0].name }}! Tudo bem?\\n\\nEstamos passando apenas para lembrar que você tem uma pendência financeira.\\n\\n💰 Valor: R${{ $('Filtra link').item.json.Valor }}\\n📅 Vencimento: {{ new Date($('Filtra link').item.json.DataVencimento).toLocaleDateString('pt-BR', { timeZone: 'America/Bahia' }) }}\\n🧾 Dados para transferência: Nubank: Ag 001 | Conta 69340787-5 | CNPJ 16698667/0001-40 | E B Ramos Eirelli \\n\\nCaso o pagamento já tenha sido realizado, por favor, desconsidere esta mensagem.\",\n  \"templateId\": null,\n  \"params\": [],\n  \"templateMediaId\": null,\n  \"typeTemplate\": null\n}\n",
        "options": {}
      },
      "type": "n8n-nodes-base.httpRequest",
      "typeVersion": 4.2,
      "position": [
        1136,
        -816
      ],
      "id": "6f1dfa16-8c6b-4c02-905d-68254bb3fb74",
      "name": "mandar mensagem12"
    },
    {
      "parameters": {
        "method": "POST",
        "url": "=https://chat-10api.jetsalesbrasil.com/messages/{{ $json.contacts[0].id }}",
        "sendHeaders": true,
        "headerParameters": {
          "parameters": [
            {
              "name": "Authorization",
              "value": "=Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0ZW5hbnRJZCI6NSwicHJvZmlsZSI6ImFkbWluIiwic2Vzc2lvbklkIjo3LCJjaGFubmVsVHlwZSI6IndoYXRzYXBwIiwiaWF0IjoxNzU1NTE4NTQyLCJleHAiOjE4MTg1OTA1NDJ9.bL0EuUunp9ScP2d0yC1HQvTbzLNEAJ6ctLXbvxs23Oo"
            }
          ]
        },
        "sendBody": true,
        "specifyBody": "json",
        "jsonBody": "={\n  \"fromMe\": true,\n  \"body\": \"Olá, {{ $json.contacts[0].name }}! Tudo bem?\\n\\nEstamos passando apenas para lembrar que você tem uma pendência financeira.\\n\\n💰 Valor: R${{ $('Filtra link').item.json.Valor }}\\n📅 Vencimento: {{ new Date($('Filtra link').item.json.DataVencimento).toLocaleDateString('pt-BR', { timeZone: 'America/Bahia' }) }}\\n🧾 Dados para transferência: Nubank: Ag 001 | Conta 69340787-5 | CNPJ 16698667/0001-40 | E B Ramos Eirelli \\n\\nCaso o pagamento já tenha sido realizado, por favor, desconsidere esta mensagem.\",\n  \"idFront\": \"6f94004c-a9a0-4819-94c3-6ad53fdc7717\",\n  \"note\": false\n}\n",
        "options": {}
      },
      "type": "n8n-nodes-base.httpRequest",
      "typeVersion": 4.2,
      "position": [
        1136,
        -624
      ],
      "id": "ca9a487b-a588-4687-81fb-b2e4ba7622e4",
      "name": "mandar mensagem13"
    },
    {
      "parameters": {
        "conditions": {
          "options": {
            "caseSensitive": true,
            "leftValue": "",
            "typeValidation": "strict",
            "version": 2
          },
          "conditions": [
            {
              "id": "7ef80ead-8d6c-4763-bb8f-f911b938a6e0",
              "leftValue": "={{ $json.UrlBoleto }}",
              "rightValue": "={{ $json.UrlBoleto }}",
              "operator": {
                "type": "string",
                "operation": "notEmpty",
                "singleValue": true
              }
            }
          ],
          "combinator": "and"
        },
        "options": {}
      },
      "type": "n8n-nodes-base.if",
      "typeVersion": 2.2,
      "position": [
        16,
        -528
      ],
      "id": "29460acd-fdcd-4c64-9bb4-881a34ab33ad",
      "name": "Filtra link"
    },
    {
      "parameters": {
        "conditions": {
          "options": {
            "caseSensitive": true,
            "leftValue": "",
            "typeValidation": "strict",
            "version": 2
          },
          "conditions": [
            {
              "id": "0d07a808-bd76-40b9-be0c-e49a0bde4894",
              "leftValue": "={{ $json.contacts }}",
              "rightValue": "",
              "operator": {
                "type": "array",
                "operation": "empty",
                "singleValue": true
              }
            }
          ],
          "combinator": "and"
        },
        "options": {}
      },
      "type": "n8n-nodes-base.if",
      "typeVersion": 2.2,
      "position": [
        688,
        -720
      ],
      "id": "045f8c00-5897-4f7d-b80d-eb3f4d4c1291",
      "name": "Já cadastrado ?"
    },
    {
      "parameters": {
        "conditions": {
          "options": {
            "caseSensitive": true,
            "leftValue": "",
            "typeValidation": "strict",
            "version": 2
          },
          "conditions": [
            {
              "id": "0d07a808-bd76-40b9-be0c-e49a0bde4894",
              "leftValue": "={{ $json.contacts }}",
              "rightValue": "",
              "operator": {
                "type": "array",
                "operation": "empty",
                "singleValue": true
              }
            }
          ],
          "combinator": "and"
        },
        "options": {}
      },
      "type": "n8n-nodes-base.if",
      "typeVersion": 2.2,
      "position": [
        688,
        -336
      ],
      "id": "09ac8973-ecd4-4160-b146-77025c2ef91c",
      "name": "Já cadastrado ?1"
    },
    {
      "parameters": {
        "conditions": {
          "options": {
            "caseSensitive": true,
            "leftValue": "",
            "typeValidation": "strict",
            "version": 2
          },
          "conditions": [
            {
              "id": "12c956ca-5409-405a-ba3b-5c8de31501f7",
              "leftValue": "={{ $json.DataVencimento.toDateTime().format('yyyy-MM-dd') }}",
              "rightValue": "={{ $now.format('yyyy-MM-dd') }}",
              "operator": {
                "type": "string",
                "operation": "equals",
                "name": "filter.operator.equals"
              }
            }
          ],
          "combinator": "and"
        },
        "options": {}
      },
      "type": "n8n-nodes-base.filter",
      "typeVersion": 2.2,
      "position": [
        -224,
        304
      ],
      "id": "fbd6405e-ed67-4c74-bfdc-6666d2d12e06",
      "name": "Filtra data1"
    },
    {
      "parameters": {
        "assignments": {
          "assignments": [
            {
              "id": "e6333f86-745e-4f82-b4b5-cb6ebb76ac6a",
              "name": "telefone",
              "value": "={{\n  (() => {\n    // 1) pega o telefone pelo CPF e deixa só dígitos\n    let tel = (\n      ($('Busca cobrança1').all().map(i => i.json.Cliente).flat()\n        .find(c => c.CPF === $json.CPF) || {}\n      ).Telefone || ''\n    ).replace(/\\D/g, '');\n\n    if (!tel) return '';\n\n    // 2) trabalha no formato local (sem 55) para detectar/remover o 9º dígito\n    let local = tel.startsWith('55') ? tel.slice(2) : tel;\n\n    // se for celular (11 dígitos) e tiver '9' logo após o DDD, remove\n    if (local.length === 11 && local[2] === '9') {\n      local = local.slice(0, 2) + local.slice(3);\n    }\n\n    // 3) remonta e aplica a regra do 55: se final tiver < 13, prefixa 55 (uma vez)\n    let out = tel.startsWith('55') ? '55' + local : local;\n    if (out.length < 13) out = '55' + local;\n\n    return out;\n  })()\n}}\n",
              "type": "string"
            },
            {
              "id": "551f5d8f-9ee9-47c7-8c43-7c090484feaa",
              "name": "nome",
              "value": "={{ \n  ( $('Busca cobrança1').all().map(i => i.json.Cliente).flat()\n    .find(c => c.CPF === $json.CPF) || {} \n  ).Nome || '' \n}}",
              "type": "string"
            },
            {
              "id": "10c7426b-a3bb-498b-ad4c-0a21db5365f9",
              "name": "email",
              "value": "={{   (     $('Busca cobrança1').all().map(i => i.json.Cliente).flat()       .find(c => c.CPF === $json.CPF) || {}   ).ResponsavelEmail || '' }}",
              "type": "string"
            }
          ]
        },
        "options": {}
      },
      "type": "n8n-nodes-base.set",
      "typeVersion": 3.4,
      "position": [
        224,
        496
      ],
      "id": "67899fc3-3be5-4021-b5ff-a0452485e686",
      "name": "Edit Fields1"
    },
    {
      "parameters": {
        "url": "https://chat-10api.jetsalesbrasil.com/contacts/",
        "sendQuery": true,
        "queryParameters": {
          "parameters": [
            {
              "name": "pageNumber",
              "value": "1"
            },
            {
              "name": "hasMore",
              "value": "true"
            },
            {
              "name": "searchParam",
              "value": "=557591105310"
            }
          ]
        },
        "sendHeaders": true,
        "headerParameters": {
          "parameters": [
            {
              "name": "Authorization",
              "value": "Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0ZW5hbnRJZCI6NSwicHJvZmlsZSI6ImFkbWluIiwic2Vzc2lvbklkIjo3LCJjaGFubmVsVHlwZSI6IndoYXRzYXBwIiwiaWF0IjoxNzU1NTE4NTQyLCJleHAiOjE4MTg1OTA1NDJ9.bL0EuUunp9ScP2d0yC1HQvTbzLNEAJ6ctLXbvxs23Oo"
            }
          ]
        },
        "options": {}
      },
      "type": "n8n-nodes-base.httpRequest",
      "typeVersion": 4.2,
      "position": [
        448,
        496
      ],
      "id": "c43bb0a0-3df3-4b62-bcc5-515d4acba68e",
      "name": "Buscar contato1"
    },
    {
      "parameters": {
        "method": "POST",
        "url": "https://chat-10api.jetsalesbrasil.com/contacts",
        "sendHeaders": true,
        "headerParameters": {
          "parameters": [
            {
              "name": "Authorization",
              "value": "Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0ZW5hbnRJZCI6NSwicHJvZmlsZSI6ImFkbWluIiwic2Vzc2lvbklkIjo3LCJjaGFubmVsVHlwZSI6IndoYXRzYXBwIiwiaWF0IjoxNzU1NTE4NTQyLCJleHAiOjE4MTg1OTA1NDJ9.bL0EuUunp9ScP2d0yC1HQvTbzLNEAJ6ctLXbvxs23Oo"
            }
          ]
        },
        "sendBody": true,
        "specifyBody": "json",
        "jsonBody": "={\n    \"name\": {{ $json.contacts[0].id }},\n    \"number\": \"{{$json.contacts[0].number }}\",\n    \"wallets\": [],\n    \"extraInfo\": [],\n    \"defaultDepartment\": null,\n    \"tags\": [],\n    \"customFields\": {}\n}\n",
        "options": {}
      },
      "type": "n8n-nodes-base.httpRequest",
      "typeVersion": 4.2,
      "position": [
        896,
        400
      ],
      "id": "1fa46ec2-63a7-4d95-b70d-6cc36ed9a9a2",
      "name": "Criar contato1"
    },
    {
      "parameters": {
        "method": "POST",
        "url": "https://chat-10api.jetsalesbrasil.com/tickets",
        "sendHeaders": true,
        "headerParameters": {
          "parameters": [
            {
              "name": "Authorization",
              "value": "Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0ZW5hbnRJZCI6NSwicHJvZmlsZSI6ImFkbWluIiwic2Vzc2lvbklkIjo3LCJjaGFubmVsVHlwZSI6IndoYXRzYXBwIiwiaWF0IjoxNzU1NTE4NTQyLCJleHAiOjE4MTg1OTA1NDJ9.bL0EuUunp9ScP2d0yC1HQvTbzLNEAJ6ctLXbvxs23Oo"
            }
          ]
        },
        "sendBody": true,
        "specifyBody": "json",
        "jsonBody": "=\"jsonBody\": \"={{ { \n  contactId: $json.contacts?.[0]?.id, \n  mini: false, \n  number: String($json.contacts?.[0]?.number || ''), \n  isActiveDemand: true, \n  channel: 'whatsapp', \n  status: 'open', \n  whatsappId: 7, \n  queueId: null, \n  body: '*teste*:\\\\nola', \n  templateId: null, \n  params: [], \n  templateMediaId: null, \n  idFront: '1b6d8961-172b-4ae3-aae3-e0f59dd8744c', \n  typeTemplate: null \n} }}\"\n",
        "options": {
          "redirect": {
            "redirect": {}
          }
        }
      },
      "type": "n8n-nodes-base.httpRequest",
      "typeVersion": 4.2,
      "position": [
        896,
        592
      ],
      "id": "45cca03d-5845-4cc4-8271-e8dca607e85b",
      "name": "criar ticket1",
      "onError": "continueErrorOutput"
    },
    {
      "parameters": {
        "method": "POST",
        "url": "https://chat-10api.jetsalesbrasil.com/tickets",
        "sendHeaders": true,
        "headerParameters": {
          "parameters": [
            {
              "name": "Authorization",
              "value": "Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0ZW5hbnRJZCI6NSwicHJvZmlsZSI6ImFkbWluIiwic2Vzc2lvbklkIjo3LCJjaGFubmVsVHlwZSI6IndoYXRzYXBwIiwiaWF0IjoxNzU1NTE4NTQyLCJleHAiOjE4MTg1OTA1NDJ9.bL0EuUunp9ScP2d0yC1HQvTbzLNEAJ6ctLXbvxs23Oo"
            },
            {
              "name": "Content-Type",
              "value": "application/json"
            },
            {
              "name": "host",
              "value": "chat-10api.jetsalesbrasil.com"
            }
          ]
        },
        "sendBody": true,
        "specifyBody": "json",
        "jsonBody": "={\n  \"mini\": false,\n  \"contactId\": {{$json.id}},\n  \"number\": \"{{$json.number}}\",\n  \"isActiveDemand\": true,\n  \"channel\": \"whatsapp\",\n  \"status\": \"open\",\n  \"whatsappId\": 7,\n  \"queueId\": null,\n  \"body\": \"Olá,  {{ $json.contacts[0].name }}! Tudo bem?\\n\\nEstamos passando apenas para lembrar que você tem um título pendente.\\n\\n💰 Valor:R${{ $('Filtra link1').item.json.Valor }} \\n📅 Vencimento:{{ new Date($('Filtra link1').item.json.DataVencimento).toLocaleDateString('pt-BR', { timeZone: 'America/Bahia' }) }} \\n🔗 Link: {{ $('Filtra link1').item.json.UrlBoleto }}\\n\\nCaso o pagamento já tenha sido realizado, por favor, desconsidere esta mensagem.\",\n  \"templateId\": null,\n  \"params\": [],\n  \"templateMediaId\": null,\n  \"typeTemplate\": null\n}\n",
        "options": {}
      },
      "type": "n8n-nodes-base.httpRequest",
      "typeVersion": 4.2,
      "position": [
        1120,
        400
      ],
      "id": "063150a2-63dc-47b6-9878-ef74935055d1",
      "name": "mandar mensagem1"
    },
    {
      "parameters": {
        "method": "POST",
        "url": "=https://chat-10api.jetsalesbrasil.com/messages/{{ $json.contacts[0].id }}",
        "sendHeaders": true,
        "headerParameters": {
          "parameters": [
            {
              "name": "Authorization",
              "value": "=Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0ZW5hbnRJZCI6NSwicHJvZmlsZSI6ImFkbWluIiwic2Vzc2lvbklkIjo3LCJjaGFubmVsVHlwZSI6IndoYXRzYXBwIiwiaWF0IjoxNzU1NTE4NTQyLCJleHAiOjE4MTg1OTA1NDJ9.bL0EuUunp9ScP2d0yC1HQvTbzLNEAJ6ctLXbvxs23Oo"
            }
          ]
        },
        "sendBody": true,
        "specifyBody": "json",
        "jsonBody": "={\n  \"fromMe\": true,\n  \"body\": \"Olá,  {{ $json.contacts[0].name }}! Tudo bem?\\n\\nEstamos passando apenas para lembrar que você tem um título pendente.\\n\\n💰 Valor:R${{ $('Filtra link1').item.json.Valor }} \\n📅 Vencimento:{{ new Date($('Filtra link1').item.json.DataVencimento).toLocaleDateString('pt-BR', { timeZone: 'America/Bahia' }) }} \\n🔗 Link: {{ $('Filtra link1').item.json.UrlBoleto }}\\n\\nCaso o pagamento já tenha sido realizado, por favor, desconsidere esta mensagem.\",\n  \"idFront\": \"6f94004c-a9a0-4819-94c3-6ad53fdc7717\",\n  \"note\": false\n}\n",
        "options": {}
      },
      "type": "n8n-nodes-base.httpRequest",
      "typeVersion": 4.2,
      "position": [
        1120,
        608
      ],
      "id": "88008c8f-fd99-402b-9373-958cb4d26ad6",
      "name": "mandar mensagem4"
    },
    {
      "parameters": {
        "assignments": {
          "assignments": [
            {
              "id": "e6333f86-745e-4f82-b4b5-cb6ebb76ac6a",
              "name": "telefone",
              "value": "={{\n  (() => {\n    // 1) pega o telefone pelo CPF e deixa só dígitos\n    let tel = (\n      ($('Busca cobrança1').all().map(i => i.json.Cliente).flat()\n        .find(c => c.CPF === $json.CPF) || {}\n      ).Telefone || ''\n    ).replace(/\\D/g, '');\n\n    if (!tel) return '';\n\n    // 2) trabalha no formato local (sem 55) para detectar/remover o 9º dígito\n    let local = tel.startsWith('55') ? tel.slice(2) : tel;\n\n    // se for celular (11 dígitos) e tiver '9' logo após o DDD, remove\n    if (local.length === 11 && local[2] === '9') {\n      local = local.slice(0, 2) + local.slice(3);\n    }\n\n    // 3) remonta e aplica a regra do 55: se final tiver < 13, prefixa 55 (uma vez)\n    let out = tel.startsWith('55') ? '55' + local : local;\n    if (out.length < 13) out = '55' + local;\n\n    return out;\n  })()\n}}\n",
              "type": "string"
            },
            {
              "id": "551f5d8f-9ee9-47c7-8c43-7c090484feaa",
              "name": "nome",
              "value": "={{ \n  ( $('Busca cobrança1').all().map(i => i.json.Cliente).flat()\n    .find(c => c.CPF === $json.CPF) || {} \n  ).Nome || '' \n}}",
              "type": "string"
            },
            {
              "id": "10c7426b-a3bb-498b-ad4c-0a21db5365f9",
              "name": "email",
              "value": "={{   (     $('Busca cobrança1').all().map(i => i.json.Cliente).flat()       .find(c => c.CPF === $json.CPF) || {}   ).ResponsavelEmail || '' }}",
              "type": "string"
            }
          ]
        },
        "options": {}
      },
      "type": "n8n-nodes-base.set",
      "typeVersion": 3.4,
      "position": [
        224,
        112
      ],
      "id": "ef0432c2-94fd-427d-b000-d826efe94a13",
      "name": "Edit Fields7"
    },
    {
      "parameters": {
        "url": "https://chat-10api.jetsalesbrasil.com/contacts/",
        "sendQuery": true,
        "queryParameters": {
          "parameters": [
            {
              "name": "pageNumber",
              "value": "1"
            },
            {
              "name": "hasMore",
              "value": "true"
            },
            {
              "name": "searchParam",
              "value": "=557591105310"
            }
          ]
        },
        "sendHeaders": true,
        "headerParameters": {
          "parameters": [
            {
              "name": "Authorization",
              "value": "Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0ZW5hbnRJZCI6NSwicHJvZmlsZSI6ImFkbWluIiwic2Vzc2lvbklkIjo3LCJjaGFubmVsVHlwZSI6IndoYXRzYXBwIiwiaWF0IjoxNzU1NTE4NTQyLCJleHAiOjE4MTg1OTA1NDJ9.bL0EuUunp9ScP2d0yC1HQvTbzLNEAJ6ctLXbvxs23Oo"
            }
          ]
        },
        "options": {}
      },
      "type": "n8n-nodes-base.httpRequest",
      "typeVersion": 4.2,
      "position": [
        448,
        112
      ],
      "id": "767fa1c6-14c8-45cf-881f-75468f8dbaad",
      "name": "Buscar contato7"
    },
    {
      "parameters": {
        "method": "POST",
        "url": "https://chat-10api.jetsalesbrasil.com/contacts",
        "sendHeaders": true,
        "headerParameters": {
          "parameters": [
            {
              "name": "Authorization",
              "value": "Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0ZW5hbnRJZCI6NSwicHJvZmlsZSI6ImFkbWluIiwic2Vzc2lvbklkIjo3LCJjaGFubmVsVHlwZSI6IndoYXRzYXBwIiwiaWF0IjoxNzU1NTE4NTQyLCJleHAiOjE4MTg1OTA1NDJ9.bL0EuUunp9ScP2d0yC1HQvTbzLNEAJ6ctLXbvxs23Oo"
            }
          ]
        },
        "sendBody": true,
        "specifyBody": "json",
        "jsonBody": "={\n    \"name\": {{ $json.contacts[0].id }},\n    \"number\": \"{{$json.contacts[0].number }}\",\n    \"wallets\": [],\n    \"extraInfo\": [],\n    \"defaultDepartment\": null,\n    \"tags\": [],\n    \"customFields\": {}\n}\n",
        "options": {}
      },
      "type": "n8n-nodes-base.httpRequest",
      "typeVersion": 4.2,
      "position": [
        896,
        16
      ],
      "id": "8a7c1056-8982-49c5-8e80-9f5aea108cc2",
      "name": "Criar contato7"
    },
    {
      "parameters": {
        "method": "POST",
        "url": "https://chat-10api.jetsalesbrasil.com/tickets",
        "sendHeaders": true,
        "headerParameters": {
          "parameters": [
            {
              "name": "Authorization",
              "value": "Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0ZW5hbnRJZCI6NSwicHJvZmlsZSI6ImFkbWluIiwic2Vzc2lvbklkIjo3LCJjaGFubmVsVHlwZSI6IndoYXRzYXBwIiwiaWF0IjoxNzU1NTE4NTQyLCJleHAiOjE4MTg1OTA1NDJ9.bL0EuUunp9ScP2d0yC1HQvTbzLNEAJ6ctLXbvxs23Oo"
            }
          ]
        },
        "sendBody": true,
        "specifyBody": "json",
        "jsonBody": "=\"jsonBody\": \"={{ { \n  contactId: $json.contacts?.[0]?.id, \n  mini: false, \n  number: String($json.contacts?.[0]?.number || ''), \n  isActiveDemand: true, \n  channel: 'whatsapp', \n  status: 'open', \n  whatsappId: 7, \n  queueId: null, \n  body: '*teste*:\\\\nola', \n  templateId: null, \n  params: [], \n  templateMediaId: null, \n  idFront: '1b6d8961-172b-4ae3-aae3-e0f59dd8744c', \n  typeTemplate: null \n} }}\"\n",
        "options": {
          "redirect": {
            "redirect": {}
          }
        }
      },
      "type": "n8n-nodes-base.httpRequest",
      "typeVersion": 4.2,
      "position": [
        896,
        208
      ],
      "id": "0e76c7bd-f5b9-4bba-8602-5ea9643eb1e4",
      "name": "criar ticket7",
      "onError": "continueErrorOutput"
    },
    {
      "parameters": {
        "method": "POST",
        "url": "https://chat-10api.jetsalesbrasil.com/tickets",
        "sendHeaders": true,
        "headerParameters": {
          "parameters": [
            {
              "name": "Authorization",
              "value": "Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0ZW5hbnRJZCI6NSwicHJvZmlsZSI6ImFkbWluIiwic2Vzc2lvbklkIjo3LCJjaGFubmVsVHlwZSI6IndoYXRzYXBwIiwiaWF0IjoxNzU1NTE4NTQyLCJleHAiOjE4MTg1OTA1NDJ9.bL0EuUunp9ScP2d0yC1HQvTbzLNEAJ6ctLXbvxs23Oo"
            },
            {
              "name": "Content-Type",
              "value": "application/json"
            },
            {
              "name": "host",
              "value": "chat-10api.jetsalesbrasil.com"
            }
          ]
        },
        "sendBody": true,
        "specifyBody": "json",
        "jsonBody": "={\n  \"mini\": false,\n  \"contactId\": {{$json.id}},\n  \"number\": \"{{$json.number}}\",\n  \"isActiveDemand\": true,\n  \"channel\": \"whatsapp\",\n  \"status\": \"open\",\n  \"whatsappId\": 7,\n  \"queueId\": null,\n  \"body\": \"Olá, {{ $json.contacts[0].name }}! Tudo bem?\\n\\nEstamos passando apenas para lembrar que você tem uma pendência financeira.\\n\\n💰 Valor: R${{ $('Filtra link1').item.json.Valor }}\\n📅 Vencimento: {{ new Date($('Filtra link1').item.json.DataVencimento).toLocaleDateString('pt-BR', { timeZone: 'America/Bahia' }) }}\\n🧾 Dados para transferência: Nubank: Ag 001 | Conta 69340787-5 | CNPJ 16698667/0001-40 | E B Ramos Eirelli \\n\\nCaso o pagamento já tenha sido realizado, por favor, desconsidere esta mensagem.\",\n  \"templateId\": null,\n  \"params\": [],\n  \"templateMediaId\": null,\n  \"typeTemplate\": null\n}\n",
        "options": {}
      },
      "type": "n8n-nodes-base.httpRequest",
      "typeVersion": 4.2,
      "position": [
        1120,
        16
      ],
      "id": "229e5a42-af5e-4d4d-9d93-f5956efe8dd4",
      "name": "mandar mensagem14"
    },
    {
      "parameters": {
        "method": "POST",
        "url": "=https://chat-10api.jetsalesbrasil.com/messages/{{ $json.contacts[0].id }}",
        "sendHeaders": true,
        "headerParameters": {
          "parameters": [
            {
              "name": "Authorization",
              "value": "=Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0ZW5hbnRJZCI6NSwicHJvZmlsZSI6ImFkbWluIiwic2Vzc2lvbklkIjo3LCJjaGFubmVsVHlwZSI6IndoYXRzYXBwIiwiaWF0IjoxNzU1NTE4NTQyLCJleHAiOjE4MTg1OTA1NDJ9.bL0EuUunp9ScP2d0yC1HQvTbzLNEAJ6ctLXbvxs23Oo"
            }
          ]
        },
        "sendBody": true,
        "specifyBody": "json",
        "jsonBody": "={\n  \"fromMe\": true,\n  \"body\": \"Olá, {{ $json.contacts[0].name }}! Tudo bem?\\n\\nEstamos passando apenas para lembrar que você tem uma pendência financeira.\\n\\n💰 Valor: R${{ $('Filtra link1').item.json.Valor }}\\n📅 Vencimento: {{ new Date($('Filtra link1').item.json.DataVencimento).toLocaleDateString('pt-BR', { timeZone: 'America/Bahia' }) }}\\n🧾 Dados para transferência: Nubank: Ag 001 | Conta 69340787-5 | CNPJ 16698667/0001-40 | E B Ramos Eirelli \\n\\nCaso o pagamento já tenha sido realizado, por favor, desconsidere esta mensagem.\",\n  \"idFront\": \"6f94004c-a9a0-4819-94c3-6ad53fdc7717\",\n  \"note\": false\n}\n",
        "options": {}
      },
      "type": "n8n-nodes-base.httpRequest",
      "typeVersion": 4.2,
      "position": [
        1120,
        224
      ],
      "id": "84b2671b-5247-4b04-adcd-5f680983219f",
      "name": "mandar mensagem15"
    },
    {
      "parameters": {
        "conditions": {
          "options": {
            "caseSensitive": true,
            "leftValue": "",
            "typeValidation": "strict",
            "version": 2
          },
          "conditions": [
            {
              "id": "7ef80ead-8d6c-4763-bb8f-f911b938a6e0",
              "leftValue": "={{ $json.UrlBoleto }}",
              "rightValue": "={{ $json.UrlBoleto }}",
              "operator": {
                "type": "string",
                "operation": "notEmpty",
                "singleValue": true
              }
            }
          ],
          "combinator": "and"
        },
        "options": {}
      },
      "type": "n8n-nodes-base.if",
      "typeVersion": 2.2,
      "position": [
        0,
        304
      ],
      "id": "e9149ccf-bb31-46b0-9a7d-ea79ceee9d89",
      "name": "Filtra link1"
    },
    {
      "parameters": {
        "conditions": {
          "options": {
            "caseSensitive": true,
            "leftValue": "",
            "typeValidation": "strict",
            "version": 2
          },
          "conditions": [
            {
              "id": "0d07a808-bd76-40b9-be0c-e49a0bde4894",
              "leftValue": "={{ $json.contacts }}",
              "rightValue": "",
              "operator": {
                "type": "array",
                "operation": "empty",
                "singleValue": true
              }
            }
          ],
          "combinator": "and"
        },
        "options": {}
      },
      "type": "n8n-nodes-base.if",
      "typeVersion": 2.2,
      "position": [
        672,
        112
      ],
      "id": "0969bf51-5bdb-4f5b-881e-5311dea8f49f",
      "name": "Já cadastrado ?2"
    },
    {
      "parameters": {
        "conditions": {
          "options": {
            "caseSensitive": true,
            "leftValue": "",
            "typeValidation": "strict",
            "version": 2
          },
          "conditions": [
            {
              "id": "0d07a808-bd76-40b9-be0c-e49a0bde4894",
              "leftValue": "={{ $json.contacts }}",
              "rightValue": "",
              "operator": {
                "type": "array",
                "operation": "empty",
                "singleValue": true
              }
            }
          ],
          "combinator": "and"
        },
        "options": {}
      },
      "type": "n8n-nodes-base.if",
      "typeVersion": 2.2,
      "position": [
        672,
        496
      ],
      "id": "beeca4de-1aed-41d0-bee2-b59edc846e8c",
      "name": "Já cadastrado ?3"
    },
    {
      "parameters": {
        "assignments": {
          "assignments": [
            {
              "id": "e6333f86-745e-4f82-b4b5-cb6ebb76ac6a",
              "name": "telefone",
              "value": "={{\n  (() => {\n    // 1) pega o telefone pelo CPF e deixa só dígitos\n    let tel = (\n      ($('Busca cobrança2').all().map(i => i.json.Cliente).flat()\n        .find(c => c.CPF === $json.CPF) || {}\n      ).Telefone || ''\n    ).replace(/\\D/g, '');\n\n    if (!tel) return '';\n\n    // 2) trabalha no formato local (sem 55) para detectar/remover o 9º dígito\n    let local = tel.startsWith('55') ? tel.slice(2) : tel;\n\n    // se for celular (11 dígitos) e tiver '9' logo após o DDD, remove\n    if (local.length === 11 && local[2] === '9') {\n      local = local.slice(0, 2) + local.slice(3);\n    }\n\n    // 3) remonta e aplica a regra do 55: se final tiver < 13, prefixa 55 (uma vez)\n    let out = tel.startsWith('55') ? '55' + local : local;\n    if (out.length < 13) out = '55' + local;\n\n    return out;\n  })()\n}}\n",
              "type": "string"
            },
            {
              "id": "551f5d8f-9ee9-47c7-8c43-7c090484feaa",
              "name": "nome",
              "value": "={{ \n  ( $('Busca cobrança2').all().map(i => i.json.Cliente).flat()\n    .find(c => c.CPF === $json.CPF) || {} \n  ).Nome || '' \n}}",
              "type": "string"
            },
            {
              "id": "10c7426b-a3bb-498b-ad4c-0a21db5365f9",
              "name": "email",
              "value": "={{   (     $('Busca cobrança2').all().map(i => i.json.Cliente).flat()       .find(c => c.CPF === $json.CPF) || {}   ).ResponsavelEmail || '' }}",
              "type": "string"
            }
          ]
        },
        "options": {}
      },
      "type": "n8n-nodes-base.set",
      "typeVersion": 3.4,
      "position": [
        224,
        1344
      ],
      "id": "27dec26b-62f1-4716-a93f-a751695c9f5a",
      "name": "Edit Fields2"
    },
    {
      "parameters": {
        "url": "https://chat-10api.jetsalesbrasil.com/contacts/",
        "sendQuery": true,
        "queryParameters": {
          "parameters": [
            {
              "name": "pageNumber",
              "value": "1"
            },
            {
              "name": "hasMore",
              "value": "true"
            },
            {
              "name": "searchParam",
              "value": "=557591105310"
            }
          ]
        },
        "sendHeaders": true,
        "headerParameters": {
          "parameters": [
            {
              "name": "Authorization",
              "value": "Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0ZW5hbnRJZCI6NSwicHJvZmlsZSI6ImFkbWluIiwic2Vzc2lvbklkIjo3LCJjaGFubmVsVHlwZSI6IndoYXRzYXBwIiwiaWF0IjoxNzU1NTE4NTQyLCJleHAiOjE4MTg1OTA1NDJ9.bL0EuUunp9ScP2d0yC1HQvTbzLNEAJ6ctLXbvxs23Oo"
            }
          ]
        },
        "options": {}
      },
      "type": "n8n-nodes-base.httpRequest",
      "typeVersion": 4.2,
      "position": [
        448,
        1344
      ],
      "id": "f7df5d47-fe0b-430f-a3c6-bca71788ef3e",
      "name": "Buscar contato2"
    },
    {
      "parameters": {
        "method": "POST",
        "url": "https://chat-10api.jetsalesbrasil.com/contacts",
        "sendHeaders": true,
        "headerParameters": {
          "parameters": [
            {
              "name": "Authorization",
              "value": "Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0ZW5hbnRJZCI6NSwicHJvZmlsZSI6ImFkbWluIiwic2Vzc2lvbklkIjo3LCJjaGFubmVsVHlwZSI6IndoYXRzYXBwIiwiaWF0IjoxNzU1NTE4NTQyLCJleHAiOjE4MTg1OTA1NDJ9.bL0EuUunp9ScP2d0yC1HQvTbzLNEAJ6ctLXbvxs23Oo"
            }
          ]
        },
        "sendBody": true,
        "specifyBody": "json",
        "jsonBody": "={\n    \"name\": {{ $json.contacts[0].id }},\n    \"number\": \"{{$json.contacts[0].number }}\",\n    \"wallets\": [],\n    \"extraInfo\": [],\n    \"defaultDepartment\": null,\n    \"tags\": [],\n    \"customFields\": {}\n}\n",
        "options": {}
      },
      "type": "n8n-nodes-base.httpRequest",
      "typeVersion": 4.2,
      "position": [
        896,
        1248
      ],
      "id": "6bfd6c47-69a7-4392-9bd9-61c73245f912",
      "name": "Criar contato2"
    },
    {
      "parameters": {
        "method": "POST",
        "url": "https://chat-10api.jetsalesbrasil.com/tickets",
        "sendHeaders": true,
        "headerParameters": {
          "parameters": [
            {
              "name": "Authorization",
              "value": "Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0ZW5hbnRJZCI6NSwicHJvZmlsZSI6ImFkbWluIiwic2Vzc2lvbklkIjo3LCJjaGFubmVsVHlwZSI6IndoYXRzYXBwIiwiaWF0IjoxNzU1NTE4NTQyLCJleHAiOjE4MTg1OTA1NDJ9.bL0EuUunp9ScP2d0yC1HQvTbzLNEAJ6ctLXbvxs23Oo"
            }
          ]
        },
        "sendBody": true,
        "specifyBody": "json",
        "jsonBody": "=\"jsonBody\": \"={{ { \n  contactId: $json.contacts?.[0]?.id, \n  mini: false, \n  number: String($json.contacts?.[0]?.number || ''), \n  isActiveDemand: true, \n  channel: 'whatsapp', \n  status: 'open', \n  whatsappId: 7, \n  queueId: null, \n  body: '*teste*:\\\\nola', \n  templateId: null, \n  params: [], \n  templateMediaId: null, \n  idFront: '1b6d8961-172b-4ae3-aae3-e0f59dd8744c', \n  typeTemplate: null \n} }}\"\n",
        "options": {
          "redirect": {
            "redirect": {}
          }
        }
      },
      "type": "n8n-nodes-base.httpRequest",
      "typeVersion": 4.2,
      "position": [
        896,
        1440
      ],
      "id": "97638e35-4264-4c9b-b329-af91c9c6df2d",
      "name": "criar ticket2",
      "onError": "continueErrorOutput"
    },
    {
      "parameters": {
        "method": "POST",
        "url": "https://chat-10api.jetsalesbrasil.com/tickets",
        "sendHeaders": true,
        "headerParameters": {
          "parameters": [
            {
              "name": "Authorization",
              "value": "Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0ZW5hbnRJZCI6NSwicHJvZmlsZSI6ImFkbWluIiwic2Vzc2lvbklkIjo3LCJjaGFubmVsVHlwZSI6IndoYXRzYXBwIiwiaWF0IjoxNzU1NTE4NTQyLCJleHAiOjE4MTg1OTA1NDJ9.bL0EuUunp9ScP2d0yC1HQvTbzLNEAJ6ctLXbvxs23Oo"
            },
            {
              "name": "Content-Type",
              "value": "application/json"
            },
            {
              "name": "host",
              "value": "chat-10api.jetsalesbrasil.com"
            }
          ]
        },
        "sendBody": true,
        "specifyBody": "json",
        "jsonBody": "={\n  \"mini\": false,\n  \"contactId\": {{$json.id}},\n  \"number\": \"{{$json.number}}\",\n  \"isActiveDemand\": true,\n  \"channel\": \"whatsapp\",\n  \"status\": \"open\",\n  \"whatsappId\": 7,\n  \"queueId\": null,\n  \"body\": \"Olá, {{ $json.contacts[0].name }}! Tudo bem?\\n\\nIdentificamos que seu título está em atraso há *5 dias*.\\n\\n💰 Valor: {{ Number($('Filtra link2').item.json.Valor).toLocaleString('pt-BR', { style: 'currency', currency: 'BRL' }) }}\\n📅 Vencimento: {{ new Date($('Filtra link2').item.json.DataVencimento).toLocaleDateString('pt-BR', { timeZone: 'America/Bahia' }) }} — em atraso há *5 dias*\\n🔗 Pagamento: {{ $('Filtra link2').item.json.UrlBoleto }}\\n\\nPodemos contar com a regularização ainda hoje? Se o pagamento já foi realizado, por favor envie o comprovante para atualização.\",\n  \"templateId\": null,\n  \"params\": [],\n  \"templateMediaId\": null,\n  \"typeTemplate\": null\n}\n",
        "options": {}
      },
      "type": "n8n-nodes-base.httpRequest",
      "typeVersion": 4.2,
      "position": [
        1120,
        1248
      ],
      "id": "ebddfb63-658d-4c24-9481-07cd8074d1b2",
      "name": "mandar mensagem2"
    },
    {
      "parameters": {
        "method": "POST",
        "url": "=https://chat-10api.jetsalesbrasil.com/messages/{{ $json.contacts[0].id }}",
        "sendHeaders": true,
        "headerParameters": {
          "parameters": [
            {
              "name": "Authorization",
              "value": "=Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0ZW5hbnRJZCI6NSwicHJvZmlsZSI6ImFkbWluIiwic2Vzc2lvbklkIjo3LCJjaGFubmVsVHlwZSI6IndoYXRzYXBwIiwiaWF0IjoxNzU1NTE4NTQyLCJleHAiOjE4MTg1OTA1NDJ9.bL0EuUunp9ScP2d0yC1HQvTbzLNEAJ6ctLXbvxs23Oo"
            }
          ]
        },
        "sendBody": true,
        "specifyBody": "json",
        "jsonBody": "={\n  \"fromMe\": true,\n  \"body\": \"Olá, {{ $json.contacts[0].name }}! Tudo bem?\\n\\nIdentificamos que seu título está em atraso há *5 dias*.\\n\\n💰 Valor: {{ Number($('Filtra link2').item.json.Valor).toLocaleString('pt-BR', { style: 'currency', currency: 'BRL' }) }}\\n📅 Vencimento: {{ new Date($('Filtra link2').item.json.DataVencimento).toLocaleDateString('pt-BR', { timeZone: 'America/Bahia' }) }} — em atraso há *5 dias*\\n🔗 Pagamento: {{ $('Filtra link2').item.json.UrlBoleto }}\\n\\nPodemos contar com a regularização ainda hoje? Se o pagamento já foi realizado, por favor envie o comprovante para atualização.\",\n  \"idFront\": \"6f94004c-a9a0-4819-94c3-6ad53fdc7717\",\n  \"note\": false\n}",
        "options": {}
      },
      "type": "n8n-nodes-base.httpRequest",
      "typeVersion": 4.2,
      "position": [
        1120,
        1456
      ],
      "id": "fa6eb36e-103f-486b-81ba-c8f97ddd6d93",
      "name": "mandar mensagem5"
    },
    {
      "parameters": {
        "assignments": {
          "assignments": [
            {
              "id": "e6333f86-745e-4f82-b4b5-cb6ebb76ac6a",
              "name": "telefone",
              "value": "={{\n  (() => {\n    // 1) pega o telefone pelo CPF e deixa só dígitos\n    let tel = (\n      ($('Busca cobrança2').all().map(i => i.json.Cliente).flat()\n        .find(c => c.CPF === $json.CPF) || {}\n      ).Telefone || ''\n    ).replace(/\\D/g, '');\n\n    if (!tel) return '';\n\n    // 2) trabalha no formato local (sem 55) para detectar/remover o 9º dígito\n    let local = tel.startsWith('55') ? tel.slice(2) : tel;\n\n    // se for celular (11 dígitos) e tiver '9' logo após o DDD, remove\n    if (local.length === 11 && local[2] === '9') {\n      local = local.slice(0, 2) + local.slice(3);\n    }\n\n    // 3) remonta e aplica a regra do 55: se final tiver < 13, prefixa 55 (uma vez)\n    let out = tel.startsWith('55') ? '55' + local : local;\n    if (out.length < 13) out = '55' + local;\n\n    return out;\n  })()\n}}\n",
              "type": "string"
            },
            {
              "id": "551f5d8f-9ee9-47c7-8c43-7c090484feaa",
              "name": "nome",
              "value": "={{ \n  ( $('Busca cobrança2').all().map(i => i.json.Cliente).flat()\n    .find(c => c.CPF === $json.CPF) || {} \n  ).Nome || '' \n}}",
              "type": "string"
            },
            {
              "id": "10c7426b-a3bb-498b-ad4c-0a21db5365f9",
              "name": "email",
              "value": "={{   (     $('Busca cobrança2').all().map(i => i.json.Cliente).flat()       .find(c => c.CPF === $json.CPF) || {}   ).ResponsavelEmail || '' }}",
              "type": "string"
            }
          ]
        },
        "options": {}
      },
      "type": "n8n-nodes-base.set",
      "typeVersion": 3.4,
      "position": [
        224,
        960
      ],
      "id": "9e3709b5-9087-4cd0-af4a-ed3faf9ccaa5",
      "name": "Edit Fields8"
    },
    {
      "parameters": {
        "url": "https://chat-10api.jetsalesbrasil.com/contacts/",
        "sendQuery": true,
        "queryParameters": {
          "parameters": [
            {
              "name": "pageNumber",
              "value": "1"
            },
            {
              "name": "hasMore",
              "value": "true"
            },
            {
              "name": "searchParam",
              "value": "=557591105310"
            }
          ]
        },
        "sendHeaders": true,
        "headerParameters": {
          "parameters": [
            {
              "name": "Authorization",
              "value": "Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0ZW5hbnRJZCI6NSwicHJvZmlsZSI6ImFkbWluIiwic2Vzc2lvbklkIjo3LCJjaGFubmVsVHlwZSI6IndoYXRzYXBwIiwiaWF0IjoxNzU1NTE4NTQyLCJleHAiOjE4MTg1OTA1NDJ9.bL0EuUunp9ScP2d0yC1HQvTbzLNEAJ6ctLXbvxs23Oo"
            }
          ]
        },
        "options": {}
      },
      "type": "n8n-nodes-base.httpRequest",
      "typeVersion": 4.2,
      "position": [
        448,
        960
      ],
      "id": "8f2bf873-e264-4420-b4bd-c074f3b998b2",
      "name": "Buscar contato8"
    },
    {
      "parameters": {
        "method": "POST",
        "url": "https://chat-10api.jetsalesbrasil.com/contacts",
        "sendHeaders": true,
        "headerParameters": {
          "parameters": [
            {
              "name": "Authorization",
              "value": "Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0ZW5hbnRJZCI6NSwicHJvZmlsZSI6ImFkbWluIiwic2Vzc2lvbklkIjo3LCJjaGFubmVsVHlwZSI6IndoYXRzYXBwIiwiaWF0IjoxNzU1NTE4NTQyLCJleHAiOjE4MTg1OTA1NDJ9.bL0EuUunp9ScP2d0yC1HQvTbzLNEAJ6ctLXbvxs23Oo"
            }
          ]
        },
        "sendBody": true,
        "specifyBody": "json",
        "jsonBody": "={\n    \"name\": {{ $json.contacts[0].id }},\n    \"number\": \"{{$json.contacts[0].number }}\",\n    \"wallets\": [],\n    \"extraInfo\": [],\n    \"defaultDepartment\": null,\n    \"tags\": [],\n    \"customFields\": {}\n}\n",
        "options": {}
      },
      "type": "n8n-nodes-base.httpRequest",
      "typeVersion": 4.2,
      "position": [
        896,
        864
      ],
      "id": "48e17e91-b8cf-477e-a37d-f8f5b37ffc7a",
      "name": "Criar contato8"
    },
    {
      "parameters": {
        "method": "POST",
        "url": "https://chat-10api.jetsalesbrasil.com/tickets",
        "sendHeaders": true,
        "headerParameters": {
          "parameters": [
            {
              "name": "Authorization",
              "value": "Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0ZW5hbnRJZCI6NSwicHJvZmlsZSI6ImFkbWluIiwic2Vzc2lvbklkIjo3LCJjaGFubmVsVHlwZSI6IndoYXRzYXBwIiwiaWF0IjoxNzU1NTE4NTQyLCJleHAiOjE4MTg1OTA1NDJ9.bL0EuUunp9ScP2d0yC1HQvTbzLNEAJ6ctLXbvxs23Oo"
            }
          ]
        },
        "sendBody": true,
        "specifyBody": "json",
        "jsonBody": "=\"jsonBody\": \"={{ { \n  contactId: $json.contacts?.[0]?.id, \n  mini: false, \n  number: String($json.contacts?.[0]?.number || ''), \n  isActiveDemand: true, \n  channel: 'whatsapp', \n  status: 'open', \n  whatsappId: 7, \n  queueId: null, \n  body: '*teste*:\\\\nola', \n  templateId: null, \n  params: [], \n  templateMediaId: null, \n  idFront: '1b6d8961-172b-4ae3-aae3-e0f59dd8744c', \n  typeTemplate: null \n} }}\"\n",
        "options": {
          "redirect": {
            "redirect": {}
          }
        }
      },
      "type": "n8n-nodes-base.httpRequest",
      "typeVersion": 4.2,
      "position": [
        896,
        1056
      ],
      "id": "e0b6e8f0-018a-4e78-aa38-5e5f442fd2bb",
      "name": "criar ticket8",
      "onError": "continueErrorOutput"
    },
    {
      "parameters": {
        "method": "POST",
        "url": "https://chat-10api.jetsalesbrasil.com/tickets",
        "sendHeaders": true,
        "headerParameters": {
          "parameters": [
            {
              "name": "Authorization",
              "value": "Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0ZW5hbnRJZCI6NSwicHJvZmlsZSI6ImFkbWluIiwic2Vzc2lvbklkIjo3LCJjaGFubmVsVHlwZSI6IndoYXRzYXBwIiwiaWF0IjoxNzU1NTE4NTQyLCJleHAiOjE4MTg1OTA1NDJ9.bL0EuUunp9ScP2d0yC1HQvTbzLNEAJ6ctLXbvxs23Oo"
            },
            {
              "name": "Content-Type",
              "value": "application/json"
            },
            {
              "name": "host",
              "value": "chat-10api.jetsalesbrasil.com"
            }
          ]
        },
        "sendBody": true,
        "specifyBody": "json",
        "jsonBody": "={\n  \"mini\": false,\n  \"contactId\": {{$json.id}},\n  \"number\": \"{{$json.number}}\",\n  \"isActiveDemand\": true,\n  \"channel\": \"whatsapp\",\n  \"status\": \"open\",\n  \"whatsappId\": 7,\n  \"queueId\": null,\n  \"body\": \"Olá, {{ $json.contacts[0].name }}! Tudo bem?\\n\\nNotamos que seu título venceu em {{ new Date($('Filtra link2').item.json.DataVencimento).toLocaleDateString('pt-BR', { timeZone: 'America/Bahia' }) }} e está em atraso há **5 dias**.\\n\\n💰 Valor: {{ Number($('Filtra link2').item.json.Valor).toLocaleString('pt-BR', { style: 'currency', currency: 'BRL' }) }}\\n🧾 Dados para transferência: Nubank: Ag 001 | Conta 69340787-5 | CNPJ 16698667/0001-40 | E B Ramos Eirelli \\n\\nPodemos te ajudar a regularizar hoje? Se o pagamento já foi realizado, por favor nos envie o comprovante para atualizarmos o sistema.\",\n  \"templateId\": null,\n  \"params\": [],\n  \"templateMediaId\": null,\n  \"typeTemplate\": null\n}\n",
        "options": {}
      },
      "type": "n8n-nodes-base.httpRequest",
      "typeVersion": 4.2,
      "position": [
        1120,
        864
      ],
      "id": "c2e82a13-9788-41c3-8db5-4e3d8bed71f7",
      "name": "mandar mensagem16"
    },
    {
      "parameters": {
        "method": "POST",
        "url": "=https://chat-10api.jetsalesbrasil.com/messages/{{ $json.contacts[0].id }}",
        "sendHeaders": true,
        "headerParameters": {
          "parameters": [
            {
              "name": "Authorization",
              "value": "=Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0ZW5hbnRJZCI6NSwicHJvZmlsZSI6ImFkbWluIiwic2Vzc2lvbklkIjo3LCJjaGFubmVsVHlwZSI6IndoYXRzYXBwIiwiaWF0IjoxNzU1NTE4NTQyLCJleHAiOjE4MTg1OTA1NDJ9.bL0EuUunp9ScP2d0yC1HQvTbzLNEAJ6ctLXbvxs23Oo"
            }
          ]
        },
        "sendBody": true,
        "specifyBody": "json",
        "jsonBody": "={\n  \"fromMe\": true,\n  \"body\": \"Olá, {{ $json.contacts[0].name }}! Tudo bem?\\n\\nNotamos que seu título venceu em {{ new Date($('Filtra link2').item.json.DataVencimento).toLocaleDateString('pt-BR', { timeZone: 'America/Bahia' }) }} e está em atraso há **5 dias**.\\n\\n💰 Valor: {{ Number($('Filtra link2').item.json.Valor).toLocaleString('pt-BR', { style: 'currency', currency: 'BRL' }) }}\\n🧾 Dados para transferência: Nubank: Ag 001 | Conta 69340787-5 | CNPJ 16698667/0001-40 | E B Ramos Eirelli \\n\\nPodemos te ajudar a regularizar hoje? Se o pagamento já foi realizado, por favor nos envie o comprovante para atualizarmos o sistema.\",\n  \"idFront\": \"c4a15a3c-0b7d-4d2e-9b37-0f0d9f9a8e55\",\n  \"note\": false\n}\n",
        "options": {}
      },
      "type": "n8n-nodes-base.httpRequest",
      "typeVersion": 4.2,
      "position": [
        1120,
        1056
      ],
      "id": "10fc9267-14e2-468f-b717-fbcbc05113e1",
      "name": "mandar mensagem17"
    },
    {
      "parameters": {
        "conditions": {
          "options": {
            "caseSensitive": true,
            "leftValue": "",
            "typeValidation": "strict",
            "version": 2
          },
          "conditions": [
            {
              "id": "7ef80ead-8d6c-4763-bb8f-f911b938a6e0",
              "leftValue": "={{ $json.UrlBoleto }}",
              "rightValue": "={{ $json.UrlBoleto }}",
              "operator": {
                "type": "string",
                "operation": "notEmpty",
                "singleValue": true
              }
            }
          ],
          "combinator": "and"
        },
        "options": {}
      },
      "type": "n8n-nodes-base.if",
      "typeVersion": 2.2,
      "position": [
        0,
        1152
      ],
      "id": "bbd82f29-2283-4147-85ae-b16f4048e8c3",
      "name": "Filtra link2"
    },
    {
      "parameters": {
        "conditions": {
          "options": {
            "caseSensitive": true,
            "leftValue": "",
            "typeValidation": "strict",
            "version": 2
          },
          "conditions": [
            {
              "id": "0d07a808-bd76-40b9-be0c-e49a0bde4894",
              "leftValue": "={{ $json.contacts }}",
              "rightValue": "",
              "operator": {
                "type": "array",
                "operation": "empty",
                "singleValue": true
              }
            }
          ],
          "combinator": "and"
        },
        "options": {}
      },
      "type": "n8n-nodes-base.if",
      "typeVersion": 2.2,
      "position": [
        672,
        960
      ],
      "id": "baa88260-d815-4b91-851a-cb5cafdb4e96",
      "name": "Já cadastrado ?4"
    },
    {
      "parameters": {
        "conditions": {
          "options": {
            "caseSensitive": true,
            "leftValue": "",
            "typeValidation": "strict",
            "version": 2
          },
          "conditions": [
            {
              "id": "0d07a808-bd76-40b9-be0c-e49a0bde4894",
              "leftValue": "={{ $json.contacts }}",
              "rightValue": "",
              "operator": {
                "type": "array",
                "operation": "empty",
                "singleValue": true
              }
            }
          ],
          "combinator": "and"
        },
        "options": {}
      },
      "type": "n8n-nodes-base.if",
      "typeVersion": 2.2,
      "position": [
        672,
        1344
      ],
      "id": "77f1313a-766f-40a9-8101-293909a94151",
      "name": "Já cadastrado ?5"
    },
    {
      "parameters": {
        "assignments": {
          "assignments": [
            {
              "id": "e6333f86-745e-4f82-b4b5-cb6ebb76ac6a",
              "name": "telefone",
              "value": "={{\n  (() => {\n    // 1) pega o telefone pelo CPF e deixa só dígitos\n    let tel = (\n      ($('Busca cobrança3').all().map(i => i.json.Cliente).flat()\n        .find(c => c.CPF === $json.CPF) || {}\n      ).Telefone || ''\n    ).replace(/\\D/g, '');\n\n    if (!tel) return '';\n\n    // 2) trabalha no formato local (sem 55) para detectar/remover o 9º dígito\n    let local = tel.startsWith('55') ? tel.slice(2) : tel;\n\n    // se for celular (11 dígitos) e tiver '9' logo após o DDD, remove\n    if (local.length === 11 && local[2] === '9') {\n      local = local.slice(0, 2) + local.slice(3);\n    }\n\n    // 3) remonta e aplica a regra do 55: se final tiver < 13, prefixa 55 (uma vez)\n    let out = tel.startsWith('55') ? '55' + local : local;\n    if (out.length < 13) out = '55' + local;\n\n    return out;\n  })()\n}}\n",
              "type": "string"
            },
            {
              "id": "551f5d8f-9ee9-47c7-8c43-7c090484feaa",
              "name": "nome",
              "value": "={{ \n  ( $('Busca cobrança3').all().map(i => i.json.Cliente).flat()\n    .find(c => c.CPF === $json.CPF) || {} \n  ).Nome || '' \n}}",
              "type": "string"
            },
            {
              "id": "10c7426b-a3bb-498b-ad4c-0a21db5365f9",
              "name": "email",
              "value": "={{   (     $('Busca cobrança3').all().map(i => i.json.Cliente).flat()       .find(c => c.CPF === $json.CPF) || {}   ).ResponsavelEmail || '' }}",
              "type": "string"
            }
          ]
        },
        "options": {}
      },
      "type": "n8n-nodes-base.set",
      "typeVersion": 3.4,
      "position": [
        208,
        2240
      ],
      "id": "63dff28e-961d-4d8f-b653-ad202d3046e3",
      "name": "Edit Fields3"
    },
    {
      "parameters": {
        "url": "https://chat-10api.jetsalesbrasil.com/contacts/",
        "sendQuery": true,
        "queryParameters": {
          "parameters": [
            {
              "name": "pageNumber",
              "value": "1"
            },
            {
              "name": "hasMore",
              "value": "true"
            },
            {
              "name": "searchParam",
              "value": "=557591105310"
            }
          ]
        },
        "sendHeaders": true,
        "headerParameters": {
          "parameters": [
            {
              "name": "Authorization",
              "value": "Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0ZW5hbnRJZCI6NSwicHJvZmlsZSI6ImFkbWluIiwic2Vzc2lvbklkIjo3LCJjaGFubmVsVHlwZSI6IndoYXRzYXBwIiwiaWF0IjoxNzU1NTE4NTQyLCJleHAiOjE4MTg1OTA1NDJ9.bL0EuUunp9ScP2d0yC1HQvTbzLNEAJ6ctLXbvxs23Oo"
            }
          ]
        },
        "options": {}
      },
      "type": "n8n-nodes-base.httpRequest",
      "typeVersion": 4.2,
      "position": [
        432,
        2240
      ],
      "id": "def99d6c-9b19-4c40-8032-5a6b0437ec7c",
      "name": "Buscar contato3"
    },
    {
      "parameters": {
        "method": "POST",
        "url": "https://chat-10api.jetsalesbrasil.com/contacts",
        "sendHeaders": true,
        "headerParameters": {
          "parameters": [
            {
              "name": "Authorization",
              "value": "Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0ZW5hbnRJZCI6NSwicHJvZmlsZSI6ImFkbWluIiwic2Vzc2lvbklkIjo3LCJjaGFubmVsVHlwZSI6IndoYXRzYXBwIiwiaWF0IjoxNzU1NTE4NTQyLCJleHAiOjE4MTg1OTA1NDJ9.bL0EuUunp9ScP2d0yC1HQvTbzLNEAJ6ctLXbvxs23Oo"
            }
          ]
        },
        "sendBody": true,
        "specifyBody": "json",
        "jsonBody": "={\n    \"name\": {{ $json.contacts[0].id }},\n    \"number\": \"{{$json.contacts[0].number }}\",\n    \"wallets\": [],\n    \"extraInfo\": [],\n    \"defaultDepartment\": null,\n    \"tags\": [],\n    \"customFields\": {}\n}\n",
        "options": {}
      },
      "type": "n8n-nodes-base.httpRequest",
      "typeVersion": 4.2,
      "position": [
        880,
        2144
      ],
      "id": "5aa6deb3-7aa6-4996-b0ce-0592832d3f1b",
      "name": "Criar contato3"
    },
    {
      "parameters": {
        "method": "POST",
        "url": "https://chat-10api.jetsalesbrasil.com/tickets",
        "sendHeaders": true,
        "headerParameters": {
          "parameters": [
            {
              "name": "Authorization",
              "value": "Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0ZW5hbnRJZCI6NSwicHJvZmlsZSI6ImFkbWluIiwic2Vzc2lvbklkIjo3LCJjaGFubmVsVHlwZSI6IndoYXRzYXBwIiwiaWF0IjoxNzU1NTE4NTQyLCJleHAiOjE4MTg1OTA1NDJ9.bL0EuUunp9ScP2d0yC1HQvTbzLNEAJ6ctLXbvxs23Oo"
            }
          ]
        },
        "sendBody": true,
        "specifyBody": "json",
        "jsonBody": "=\"jsonBody\": \"={{ { \n  contactId: $json.contacts?.[0]?.id, \n  mini: false, \n  number: String($json.contacts?.[0]?.number || ''), \n  isActiveDemand: true, \n  channel: 'whatsapp', \n  status: 'open', \n  whatsappId: 7, \n  queueId: null, \n  body: '*teste*:\\\\nola', \n  templateId: null, \n  params: [], \n  templateMediaId: null, \n  idFront: '1b6d8961-172b-4ae3-aae3-e0f59dd8744c', \n  typeTemplate: null \n} }}\"\n",
        "options": {
          "redirect": {
            "redirect": {}
          }
        }
      },
      "type": "n8n-nodes-base.httpRequest",
      "typeVersion": 4.2,
      "position": [
        880,
        2336
      ],
      "id": "e0a73317-440b-47e1-921f-5000045c783f",
      "name": "criar ticket3",
      "onError": "continueErrorOutput"
    },
    {
      "parameters": {
        "method": "POST",
        "url": "https://chat-10api.jetsalesbrasil.com/tickets",
        "sendHeaders": true,
        "headerParameters": {
          "parameters": [
            {
              "name": "Authorization",
              "value": "Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0ZW5hbnRJZCI6NSwicHJvZmlsZSI6ImFkbWluIiwic2Vzc2lvbklkIjo3LCJjaGFubmVsVHlwZSI6IndoYXRzYXBwIiwiaWF0IjoxNzU1NTE4NTQyLCJleHAiOjE4MTg1OTA1NDJ9.bL0EuUunp9ScP2d0yC1HQvTbzLNEAJ6ctLXbvxs23Oo"
            },
            {
              "name": "Content-Type",
              "value": "application/json"
            },
            {
              "name": "host",
              "value": "chat-10api.jetsalesbrasil.com"
            }
          ]
        },
        "sendBody": true,
        "specifyBody": "json",
        "jsonBody": "={\n  \"mini\": false,\n  \"contactId\": {{$json.id}},\n  \"number\": \"{{$json.number}}\",\n  \"isActiveDemand\": true,\n  \"channel\": \"whatsapp\",\n  \"status\": \"open\",\n  \"whatsappId\": 7,\n  \"queueId\": null,\n  \"body\": \"Olá, {{ $json.contacts[0].name }}! Tudo bem?\\n\\nConsta em nosso sistema que seu título venceu em {{ new Date($('Filtra link3').item.json.DataVencimento).toLocaleDateString('pt-BR', { timeZone: 'America/Bahia' }) }} e encontra-se em atraso há *30 dias*.\\n\\n💰 Valor: {{ Number($('Filtra link3').item.json.Valor).toLocaleString('pt-BR', { style: 'currency', currency: 'BRL' }) }}\\n🔗 Pagamento imediato: {{ $('Filtra link3').item.json.UrlBoleto }}\\n\\nPara evitar *suspensão de serviços* e *encaminhamento para negativação e protesto*, solicitamos a regularização em até *48 horas*. Caso precise de um acordo, responda esta mensagem para tratarmos agora.\\n\\nSe o pagamento já foi realizado, por favor envie o comprovante para baixa imediata.\",\n  \"templateId\": null,\n  \"params\": [],\n  \"templateMediaId\": null,\n  \"typeTemplate\": null\n}\n\n",
        "options": {}
      },
      "type": "n8n-nodes-base.httpRequest",
      "typeVersion": 4.2,
      "position": [
        1104,
        2144
      ],
      "id": "ec663d90-a979-475b-9b24-54e8f7d38371",
      "name": "mandar mensagem6"
    },
    {
      "parameters": {
        "method": "POST",
        "url": "=https://chat-10api.jetsalesbrasil.com/messages/{{ $json.contacts[0].id }}",
        "sendHeaders": true,
        "headerParameters": {
          "parameters": [
            {
              "name": "Authorization",
              "value": "=Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0ZW5hbnRJZCI6NSwicHJvZmlsZSI6ImFkbWluIiwic2Vzc2lvbklkIjo3LCJjaGFubmVsVHlwZSI6IndoYXRzYXBwIiwiaWF0IjoxNzU1NTE4NTQyLCJleHAiOjE4MTg1OTA1NDJ9.bL0EuUunp9ScP2d0yC1HQvTbzLNEAJ6ctLXbvxs23Oo"
            }
          ]
        },
        "sendBody": true,
        "specifyBody": "json",
        "jsonBody": "={\n  \"fromMe\": true,\n  \"body\": \"Olá, {{ $json.contacts[0].name }}! Tudo bem?\\n\\nConsta em nosso sistema que seu título venceu em {{ new Date($('Filtra link3').item.json.DataVencimento).toLocaleDateString('pt-BR', { timeZone: 'America/Bahia' }) }} e encontra-se em atraso há *30 dias*.\\n\\n💰 Valor: {{ Number($('Filtra link3').item.json.Valor).toLocaleString('pt-BR', { style: 'currency', currency: 'BRL' }) }}\\n🔗 Pagamento imediato: {{ $('Filtra link3').item.json.UrlBoleto }}\\n\\nPara evitar *suspensão de serviços* e *encaminhamento para negativação e protesto*, solicitamos a regularização em até *48 horas*. Caso precise de um acordo, responda esta mensagem para tratarmos agora.\\n\\nSe o pagamento já foi realizado, por favor envie o comprovante para baixa imediata.\",\n  \"idFront\": \"6f94004c-a9a0-4819-94c3-6ad53fdc7717\",\n  \"note\": false\n}",
        "options": {}
      },
      "type": "n8n-nodes-base.httpRequest",
      "typeVersion": 4.2,
      "position": [
        1104,
        2336
      ],
      "id": "7b97314a-d0f1-4dfd-958b-09a2e3e42097",
      "name": "mandar mensagem7"
    },
    {
      "parameters": {
        "assignments": {
          "assignments": [
            {
              "id": "e6333f86-745e-4f82-b4b5-cb6ebb76ac6a",
              "name": "telefone",
              "value": "={{\n  (() => {\n    // 1) pega o telefone pelo CPF e deixa só dígitos\n    let tel = (\n      ($('Busca cobrança3').all().map(i => i.json.Cliente).flat()\n        .find(c => c.CPF === $json.CPF) || {}\n      ).Telefone || ''\n    ).replace(/\\D/g, '');\n\n    if (!tel) return '';\n\n    // 2) trabalha no formato local (sem 55) para detectar/remover o 9º dígito\n    let local = tel.startsWith('55') ? tel.slice(2) : tel;\n\n    // se for celular (11 dígitos) e tiver '9' logo após o DDD, remove\n    if (local.length === 11 && local[2] === '9') {\n      local = local.slice(0, 2) + local.slice(3);\n    }\n\n    // 3) remonta e aplica a regra do 55: se final tiver < 13, prefixa 55 (uma vez)\n    let out = tel.startsWith('55') ? '55' + local : local;\n    if (out.length < 13) out = '55' + local;\n\n    return out;\n  })()\n}}\n",
              "type": "string"
            },
            {
              "id": "551f5d8f-9ee9-47c7-8c43-7c090484feaa",
              "name": "nome",
              "value": "={{ \n  ( $('Busca cobrança3').all().map(i => i.json.Cliente).flat()\n    .find(c => c.CPF === $json.CPF) || {} \n  ).Nome || '' \n}}",
              "type": "string"
            },
            {
              "id": "10c7426b-a3bb-498b-ad4c-0a21db5365f9",
              "name": "email",
              "value": "={{   (     $('Busca cobrança3').all().map(i => i.json.Cliente).flat()       .find(c => c.CPF === $json.CPF) || {}   ).ResponsavelEmail || '' }}",
              "type": "string"
            }
          ]
        },
        "options": {}
      },
      "type": "n8n-nodes-base.set",
      "typeVersion": 3.4,
      "position": [
        208,
        1856
      ],
      "id": "72f4c317-4300-423a-8788-a24980569a31",
      "name": "Edit Fields9"
    },
    {
      "parameters": {
        "url": "https://chat-10api.jetsalesbrasil.com/contacts/",
        "sendQuery": true,
        "queryParameters": {
          "parameters": [
            {
              "name": "pageNumber",
              "value": "1"
            },
            {
              "name": "hasMore",
              "value": "true"
            },
            {
              "name": "searchParam",
              "value": "=557591105310"
            }
          ]
        },
        "sendHeaders": true,
        "headerParameters": {
          "parameters": [
            {
              "name": "Authorization",
              "value": "Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0ZW5hbnRJZCI6NSwicHJvZmlsZSI6ImFkbWluIiwic2Vzc2lvbklkIjo3LCJjaGFubmVsVHlwZSI6IndoYXRzYXBwIiwiaWF0IjoxNzU1NTE4NTQyLCJleHAiOjE4MTg1OTA1NDJ9.bL0EuUunp9ScP2d0yC1HQvTbzLNEAJ6ctLXbvxs23Oo"
            }
          ]
        },
        "options": {}
      },
      "type": "n8n-nodes-base.httpRequest",
      "typeVersion": 4.2,
      "position": [
        432,
        1856
      ],
      "id": "fd39d087-332c-41f2-965f-959396dd1a1e",
      "name": "Buscar contato9"
    },
    {
      "parameters": {
        "method": "POST",
        "url": "https://chat-10api.jetsalesbrasil.com/contacts",
        "sendHeaders": true,
        "headerParameters": {
          "parameters": [
            {
              "name": "Authorization",
              "value": "Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0ZW5hbnRJZCI6NSwicHJvZmlsZSI6ImFkbWluIiwic2Vzc2lvbklkIjo3LCJjaGFubmVsVHlwZSI6IndoYXRzYXBwIiwiaWF0IjoxNzU1NTE4NTQyLCJleHAiOjE4MTg1OTA1NDJ9.bL0EuUunp9ScP2d0yC1HQvTbzLNEAJ6ctLXbvxs23Oo"
            }
          ]
        },
        "sendBody": true,
        "specifyBody": "json",
        "jsonBody": "={\n    \"name\": {{ $json.contacts[0].id }},\n    \"number\": \"{{$json.contacts[0].number }}\",\n    \"wallets\": [],\n    \"extraInfo\": [],\n    \"defaultDepartment\": null,\n    \"tags\": [],\n    \"customFields\": {}\n}\n",
        "options": {}
      },
      "type": "n8n-nodes-base.httpRequest",
      "typeVersion": 4.2,
      "position": [
        880,
        1760
      ],
      "id": "35630cef-9f62-4826-815d-332f402a6835",
      "name": "Criar contato9"
    },
    {
      "parameters": {
        "method": "POST",
        "url": "https://chat-10api.jetsalesbrasil.com/tickets",
        "sendHeaders": true,
        "headerParameters": {
          "parameters": [
            {
              "name": "Authorization",
              "value": "Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0ZW5hbnRJZCI6NSwicHJvZmlsZSI6ImFkbWluIiwic2Vzc2lvbklkIjo3LCJjaGFubmVsVHlwZSI6IndoYXRzYXBwIiwiaWF0IjoxNzU1NTE4NTQyLCJleHAiOjE4MTg1OTA1NDJ9.bL0EuUunp9ScP2d0yC1HQvTbzLNEAJ6ctLXbvxs23Oo"
            }
          ]
        },
        "sendBody": true,
        "specifyBody": "json",
        "jsonBody": "=\"jsonBody\": \"={{ { \n  contactId: $json.contacts?.[0]?.id, \n  mini: false, \n  number: String($json.contacts?.[0]?.number || ''), \n  isActiveDemand: true, \n  channel: 'whatsapp', \n  status: 'open', \n  whatsappId: 7, \n  queueId: null, \n  body: '*teste*:\\\\nola', \n  templateId: null, \n  params: [], \n  templateMediaId: null, \n  idFront: '1b6d8961-172b-4ae3-aae3-e0f59dd8744c', \n  typeTemplate: null \n} }}\"\n",
        "options": {
          "redirect": {
            "redirect": {}
          }
        }
      },
      "type": "n8n-nodes-base.httpRequest",
      "typeVersion": 4.2,
      "position": [
        880,
        1952
      ],
      "id": "108bcf3b-9987-41f1-b19d-91df45f08a32",
      "name": "criar ticket9",
      "onError": "continueErrorOutput"
    },
    {
      "parameters": {
        "method": "POST",
        "url": "https://chat-10api.jetsalesbrasil.com/tickets",
        "sendHeaders": true,
        "headerParameters": {
          "parameters": [
            {
              "name": "Authorization",
              "value": "Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0ZW5hbnRJZCI6NSwicHJvZmlsZSI6ImFkbWluIiwic2Vzc2lvbklkIjo3LCJjaGFubmVsVHlwZSI6IndoYXRzYXBwIiwiaWF0IjoxNzU1NTE4NTQyLCJleHAiOjE4MTg1OTA1NDJ9.bL0EuUunp9ScP2d0yC1HQvTbzLNEAJ6ctLXbvxs23Oo"
            },
            {
              "name": "Content-Type",
              "value": "application/json"
            },
            {
              "name": "host",
              "value": "chat-10api.jetsalesbrasil.com"
            }
          ]
        },
        "sendBody": true,
        "specifyBody": "json",
        "jsonBody": "={\n  \"mini\": false,\n  \"contactId\": {{$json.id}},\n  \"number\": \"{{$json.number}}\",\n  \"isActiveDemand\": true,\n  \"channel\": \"whatsapp\",\n  \"status\": \"open\",\n  \"whatsappId\": 7,\n  \"queueId\": null,\n  \"body\": \"Olá, {{ $json.contacts[0].name }}! Tudo bem?\\n\\nIdentificamos que seu título venceu em {{ new Date($('Filtra link3').item.json.DataVencimento).toLocaleDateString('pt-BR', { timeZone: 'America/Bahia' }) }} e encontra-se em atraso há **30 dias**.\\n\\n💰 Valor: {{ Number($('Filtra link3').item.json.Valor).toLocaleString('pt-BR', { style: 'currency', currency: 'BRL' }) }}\\n\\n🧾 Dados para transferência: Nubank: Ag 001 | Conta 69340787-5 | CNPJ 16698667/0001-40 | E B Ramos Eirelli \\n\\nPara evitar a suspensão de serviços e o encaminhamento para negativação e protesto, solicitamos a regularização em até **48 horas**. Caso precise de um acordo, responda esta mensagem para tratarmos agora.\\n\\nSe o pagamento já foi realizado, por favor envie o comprovante para atualização imediata.\",\n  \"templateId\": null,\n  \"params\": [],\n  \"templateMediaId\": null,\n  \"typeTemplate\": null\n}\n",
        "options": {}
      },
      "type": "n8n-nodes-base.httpRequest",
      "typeVersion": 4.2,
      "position": [
        1104,
        1760
      ],
      "id": "f94ff82e-a56b-4ac5-902c-45b08a22e05a",
      "name": "mandar mensagem18"
    },
    {
      "parameters": {
        "method": "POST",
        "url": "=https://chat-10api.jetsalesbrasil.com/messages/{{ $json.contacts[0].id }}",
        "sendHeaders": true,
        "headerParameters": {
          "parameters": [
            {
              "name": "Authorization",
              "value": "=Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0ZW5hbnRJZCI6NSwicHJvZmlsZSI6ImFkbWluIiwic2Vzc2lvbklkIjo3LCJjaGFubmVsVHlwZSI6IndoYXRzYXBwIiwiaWF0IjoxNzU1NTE4NTQyLCJleHAiOjE4MTg1OTA1NDJ9.bL0EuUunp9ScP2d0yC1HQvTbzLNEAJ6ctLXbvxs23Oo"
            }
          ]
        },
        "sendBody": true,
        "specifyBody": "json",
        "jsonBody": "={\n  \"fromMe\": true,\n  \"body\": \"Olá, {{ $json.contacts[0].name }}! Tudo bem?\\n\\nIdentificamos que seu título venceu em {{ new Date($('Filtra link3').item.json.DataVencimento).toLocaleDateString('pt-BR', { timeZone: 'America/Bahia' }) }} e encontra-se em atraso há **30 dias**.\\n\\n💰 Valor: {{ Number($('Filtra link3').item.json.Valor).toLocaleString('pt-BR', { style: 'currency', currency: 'BRL' }) }}\\n\\n🧾 Dados para transferência: Nubank: Ag 001 | Conta 69340787-5 | CNPJ 16698667/0001-40 | E B Ramos Eirelli \\n\\nPara evitar a suspensão de serviços e o encaminhamento para negativação e protesto, solicitamos a regularização em até **48 horas**. Caso precise de um acordo, responda esta mensagem para tratarmos agora.\\n\\nSe o pagamento já foi realizado, por favor envie o comprovante para atualização imediata.\",\n  \"idFront\": \"9e0b7d7a-1f6a-4e2f-b5d9-4a2a92fd6b31\",\n  \"note\": false\n}\n",
        "options": {}
      },
      "type": "n8n-nodes-base.httpRequest",
      "typeVersion": 4.2,
      "position": [
        1104,
        1952
      ],
      "id": "e6ea59ca-59ed-470a-bfaa-b28d8e9824ea",
      "name": "mandar mensagem19"
    },
    {
      "parameters": {
        "conditions": {
          "options": {
            "caseSensitive": true,
            "leftValue": "",
            "typeValidation": "strict",
            "version": 2
          },
          "conditions": [
            {
              "id": "7ef80ead-8d6c-4763-bb8f-f911b938a6e0",
              "leftValue": "={{ $json.UrlBoleto }}",
              "rightValue": "={{ $json.UrlBoleto }}",
              "operator": {
                "type": "string",
                "operation": "notEmpty",
                "singleValue": true
              }
            }
          ],
          "combinator": "and"
        },
        "options": {}
      },
      "type": "n8n-nodes-base.if",
      "typeVersion": 2.2,
      "position": [
        -16,
        2048
      ],
      "id": "26e00ff2-0765-4004-84f6-a43034a5e063",
      "name": "Filtra link3"
    },
    {
      "parameters": {
        "conditions": {
          "options": {
            "caseSensitive": true,
            "leftValue": "",
            "typeValidation": "strict",
            "version": 2
          },
          "conditions": [
            {
              "id": "0d07a808-bd76-40b9-be0c-e49a0bde4894",
              "leftValue": "={{ $json.contacts }}",
              "rightValue": "",
              "operator": {
                "type": "array",
                "operation": "empty",
                "singleValue": true
              }
            }
          ],
          "combinator": "and"
        },
        "options": {}
      },
      "type": "n8n-nodes-base.if",
      "typeVersion": 2.2,
      "position": [
        656,
        1856
      ],
      "id": "c4c220e2-d066-49f5-b7f3-0f093e2625c4",
      "name": "Já cadastrado ?6"
    },
    {
      "parameters": {
        "conditions": {
          "options": {
            "caseSensitive": true,
            "leftValue": "",
            "typeValidation": "strict",
            "version": 2
          },
          "conditions": [
            {
              "id": "0d07a808-bd76-40b9-be0c-e49a0bde4894",
              "leftValue": "={{ $json.contacts }}",
              "rightValue": "",
              "operator": {
                "type": "array",
                "operation": "empty",
                "singleValue": true
              }
            }
          ],
          "combinator": "and"
        },
        "options": {}
      },
      "type": "n8n-nodes-base.if",
      "typeVersion": 2.2,
      "position": [
        656,
        2240
      ],
      "id": "cce00417-b7bf-44d8-9a4e-9d191b558c75",
      "name": "Já cadastrado ?7"
    },
    {
      "parameters": {
        "assignments": {
          "assignments": [
            {
              "id": "e6333f86-745e-4f82-b4b5-cb6ebb76ac6a",
              "name": "telefone",
              "value": "={{\n  (() => {\n    // 1) pega o telefone pelo CPF e deixa só dígitos\n    let tel = (\n      ($('Busca cobrança4').all().map(i => i.json.Cliente).flat()\n        .find(c => c.CPF === $json.CPF) || {}\n      ).Telefone || ''\n    ).replace(/\\D/g, '');\n\n    if (!tel) return '';\n\n    // 2) trabalha no formato local (sem 55) para detectar/remover o 9º dígito\n    let local = tel.startsWith('55') ? tel.slice(2) : tel;\n\n    // se for celular (11 dígitos) e tiver '9' logo após o DDD, remove\n    if (local.length === 11 && local[2] === '9') {\n      local = local.slice(0, 2) + local.slice(3);\n    }\n\n    // 3) remonta e aplica a regra do 55: se final tiver < 13, prefixa 55 (uma vez)\n    let out = tel.startsWith('55') ? '55' + local : local;\n    if (out.length < 13) out = '55' + local;\n\n    return out;\n  })()\n}}\n",
              "type": "string"
            },
            {
              "id": "551f5d8f-9ee9-47c7-8c43-7c090484feaa",
              "name": "nome",
              "value": "={{ \n  ( $('Busca cobrança4').all().map(i => i.json.Cliente).flat()\n    .find(c => c.CPF === $json.CPF) || {} \n  ).Nome || '' \n}}",
              "type": "string"
            },
            {
              "id": "10c7426b-a3bb-498b-ad4c-0a21db5365f9",
              "name": "email",
              "value": "={{   (     $('Busca cobrança4').all().map(i => i.json.Cliente).flat()       .find(c => c.CPF === $json.CPF) || {}   ).ResponsavelEmail || '' }}",
              "type": "string"
            }
          ]
        },
        "options": {}
      },
      "type": "n8n-nodes-base.set",
      "typeVersion": 3.4,
      "position": [
        208,
        3072
      ],
      "id": "cc048b27-3818-4b0a-9360-ac92d315003a",
      "name": "Edit Fields4"
    },
    {
      "parameters": {
        "url": "https://chat-10api.jetsalesbrasil.com/contacts/",
        "sendQuery": true,
        "queryParameters": {
          "parameters": [
            {
              "name": "pageNumber",
              "value": "1"
            },
            {
              "name": "hasMore",
              "value": "true"
            },
            {
              "name": "searchParam",
              "value": "=557591105310"
            }
          ]
        },
        "sendHeaders": true,
        "headerParameters": {
          "parameters": [
            {
              "name": "Authorization",
              "value": "Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0ZW5hbnRJZCI6NSwicHJvZmlsZSI6ImFkbWluIiwic2Vzc2lvbklkIjo3LCJjaGFubmVsVHlwZSI6IndoYXRzYXBwIiwiaWF0IjoxNzU1NTE4NTQyLCJleHAiOjE4MTg1OTA1NDJ9.bL0EuUunp9ScP2d0yC1HQvTbzLNEAJ6ctLXbvxs23Oo"
            }
          ]
        },
        "options": {}
      },
      "type": "n8n-nodes-base.httpRequest",
      "typeVersion": 4.2,
      "position": [
        432,
        3072
      ],
      "id": "f5e4e35e-14ed-4137-8397-a702a9e10324",
      "name": "Buscar contato4"
    },
    {
      "parameters": {
        "method": "POST",
        "url": "https://chat-10api.jetsalesbrasil.com/contacts",
        "sendHeaders": true,
        "headerParameters": {
          "parameters": [
            {
              "name": "Authorization",
              "value": "Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0ZW5hbnRJZCI6NSwicHJvZmlsZSI6ImFkbWluIiwic2Vzc2lvbklkIjo3LCJjaGFubmVsVHlwZSI6IndoYXRzYXBwIiwiaWF0IjoxNzU1NTE4NTQyLCJleHAiOjE4MTg1OTA1NDJ9.bL0EuUunp9ScP2d0yC1HQvTbzLNEAJ6ctLXbvxs23Oo"
            }
          ]
        },
        "sendBody": true,
        "specifyBody": "json",
        "jsonBody": "={\n    \"name\": {{ $json.contacts[0].id }},\n    \"number\": \"{{$json.contacts[0].number }}\",\n    \"wallets\": [],\n    \"extraInfo\": [],\n    \"defaultDepartment\": null,\n    \"tags\": [],\n    \"customFields\": {}\n}\n",
        "options": {}
      },
      "type": "n8n-nodes-base.httpRequest",
      "typeVersion": 4.2,
      "position": [
        880,
        2976
      ],
      "id": "c762df76-2e79-4a2a-a983-daccf0753121",
      "name": "Criar contato4"
    },
    {
      "parameters": {
        "method": "POST",
        "url": "https://chat-10api.jetsalesbrasil.com/tickets",
        "sendHeaders": true,
        "headerParameters": {
          "parameters": [
            {
              "name": "Authorization",
              "value": "Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0ZW5hbnRJZCI6NSwicHJvZmlsZSI6ImFkbWluIiwic2Vzc2lvbklkIjo3LCJjaGFubmVsVHlwZSI6IndoYXRzYXBwIiwiaWF0IjoxNzU1NTE4NTQyLCJleHAiOjE4MTg1OTA1NDJ9.bL0EuUunp9ScP2d0yC1HQvTbzLNEAJ6ctLXbvxs23Oo"
            }
          ]
        },
        "sendBody": true,
        "specifyBody": "json",
        "jsonBody": "=\"jsonBody\": \"={{ { \n  contactId: $json.contacts?.[0]?.id, \n  mini: false, \n  number: String($json.contacts?.[0]?.number || ''), \n  isActiveDemand: true, \n  channel: 'whatsapp', \n  status: 'open', \n  whatsappId: 7, \n  queueId: null, \n  body: '*teste*:\\\\nola', \n  templateId: null, \n  params: [], \n  templateMediaId: null, \n  idFront: '1b6d8961-172b-4ae3-aae3-e0f59dd8744c', \n  typeTemplate: null \n} }}\"\n",
        "options": {
          "redirect": {
            "redirect": {}
          }
        }
      },
      "type": "n8n-nodes-base.httpRequest",
      "typeVersion": 4.2,
      "position": [
        880,
        3168
      ],
      "id": "4c2791ca-a373-4321-b82f-b3c32979f691",
      "name": "criar ticket4",
      "onError": "continueErrorOutput"
    },
    {
      "parameters": {
        "method": "POST",
        "url": "https://chat-10api.jetsalesbrasil.com/tickets",
        "sendHeaders": true,
        "headerParameters": {
          "parameters": [
            {
              "name": "Authorization",
              "value": "Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0ZW5hbnRJZCI6NSwicHJvZmlsZSI6ImFkbWluIiwic2Vzc2lvbklkIjo3LCJjaGFubmVsVHlwZSI6IndoYXRzYXBwIiwiaWF0IjoxNzU1NTE4NTQyLCJleHAiOjE4MTg1OTA1NDJ9.bL0EuUunp9ScP2d0yC1HQvTbzLNEAJ6ctLXbvxs23Oo"
            },
            {
              "name": "Content-Type",
              "value": "application/json"
            },
            {
              "name": "host",
              "value": "chat-10api.jetsalesbrasil.com"
            }
          ]
        },
        "sendBody": true,
        "specifyBody": "json",
        "jsonBody": "={\n  \"mini\": false,\n  \"contactId\": {{$json.id}},\n  \"number\": \"{{$json.number}}\",\n  \"isActiveDemand\": true,\n  \"channel\": \"whatsapp\",\n  \"status\": \"open\",\n  \"whatsappId\": 7,\n  \"queueId\": null,\n  \"body\": \"Olá, {{ $json.contacts[0].name }}! Tudo bem?\\n\\nConsta em nosso sistema que seu título venceu em {{ new Date($('Filtra link4').item.json.DataVencimento).toLocaleDateString('pt-BR', { timeZone: 'America/Bahia' }) }} e permanece em atraso há *60 dias*.\\n\\n💰 Valor: {{ Number($('Filtra link4').item.json.Valor).toLocaleString('pt-BR', { style: 'currency', currency: 'BRL' }) }}\\n🔗 Pagamento imediato: {{ $('Filtra link4').item.json.UrlBoleto || '' }}\\n\\nEste é um *aviso final*. Se não houver regularização em *24 horas*, seguiremos com os procedimentos formais: *suspensão de serviços*, *cobrança extrajudicial* e *apontamento aos órgãos de proteção ao crédito*, conforme contrato e legislação aplicável.\\n\\nSe já pagou, por favor envie o comprovante para baixa imediata. Precisando de acordo, responda esta mensagem para tratarmos agora.\n  \"params\": [],\n  \"templateMediaId\": null,\n  \"typeTemplate\": null\n}\n\n",
        "options": {}
      },
      "type": "n8n-nodes-base.httpRequest",
      "typeVersion": 4.2,
      "position": [
        1104,
        2976
      ],
      "id": "c12a17fd-a359-4cc9-bc72-b245d2984a54",
      "name": "mandar mensagem8"
    },
    {
      "parameters": {
        "method": "POST",
        "url": "=https://chat-10api.jetsalesbrasil.com/messages/{{ $json.contacts[0].id }}",
        "sendHeaders": true,
        "headerParameters": {
          "parameters": [
            {
              "name": "Authorization",
              "value": "=Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0ZW5hbnRJZCI6NSwicHJvZmlsZSI6ImFkbWluIiwic2Vzc2lvbklkIjo3LCJjaGFubmVsVHlwZSI6IndoYXRzYXBwIiwiaWF0IjoxNzU1NTE4NTQyLCJleHAiOjE4MTg1OTA1NDJ9.bL0EuUunp9ScP2d0yC1HQvTbzLNEAJ6ctLXbvxs23Oo"
            }
          ]
        },
        "sendBody": true,
        "specifyBody": "json",
        "jsonBody": "={\n  \"fromMe\": true,\n  \"body\": \"Olá, {{ $json.contacts[0].name }}! Tudo bem?\\n\\nConsta em nosso sistema que seu título venceu em {{ new Date($('Filtra link4').item.json.DataVencimento).toLocaleDateString('pt-BR', { timeZone: 'America/Bahia' }) }} e permanece em atraso há *60 dias*.\\n\\n💰 Valor: {{ Number($('Filtra link4').item.json.Valor).toLocaleString('pt-BR', { style: 'currency', currency: 'BRL' }) }}\\n🔗 Pagamento imediato: {{ $('Filtra link4').item.json.UrlBoleto || '' }}\\n\\nEste é um *aviso final*. Se não houver regularização em *24 horas*, seguiremos com os procedimentos formais: *suspensão de serviços*, *cobrança extrajudicial* e *apontamento aos órgãos de proteção ao crédito*, conforme contrato e legislação aplicável.\\n\\nSe já pagou, por favor envie o comprovante para baixa imediata. Precisando de acordo, responda esta mensagem para tratarmos agora.\",\n  \"idFront\": \"6f94004c-a9a0-4819-94c3-6ad53fdc7717\",\n  \"note\": false\n}\n",
        "options": {}
      },
      "type": "n8n-nodes-base.httpRequest",
      "typeVersion": 4.2,
      "position": [
        1104,
        3168
      ],
      "id": "b09681fd-28b8-4b61-8541-8624a9450705",
      "name": "mandar mensagem9"
    },
    {
      "parameters": {
        "assignments": {
          "assignments": [
            {
              "id": "e6333f86-745e-4f82-b4b5-cb6ebb76ac6a",
              "name": "telefone",
              "value": "={{\n  (() => {\n    // 1) pega o telefone pelo CPF e deixa só dígitos\n    let tel = (\n      ($('Busca cobrança4').all().map(i => i.json.Cliente).flat()\n        .find(c => c.CPF === $json.CPF) || {}\n      ).Telefone || ''\n    ).replace(/\\D/g, '');\n\n    if (!tel) return '';\n\n    // 2) trabalha no formato local (sem 55) para detectar/remover o 9º dígito\n    let local = tel.startsWith('55') ? tel.slice(2) : tel;\n\n    // se for celular (11 dígitos) e tiver '9' logo após o DDD, remove\n    if (local.length === 11 && local[2] === '9') {\n      local = local.slice(0, 2) + local.slice(3);\n    }\n\n    // 3) remonta e aplica a regra do 55: se final tiver < 13, prefixa 55 (uma vez)\n    let out = tel.startsWith('55') ? '55' + local : local;\n    if (out.length < 13) out = '55' + local;\n\n    return out;\n  })()\n}}\n",
              "type": "string"
            },
            {
              "id": "551f5d8f-9ee9-47c7-8c43-7c090484feaa",
              "name": "nome",
              "value": "={{ \n  ( $('Busca cobrança4').all().map(i => i.json.Cliente).flat()\n    .find(c => c.CPF === $json.CPF) || {} \n  ).Nome || '' \n}}",
              "type": "string"
            },
            {
              "id": "10c7426b-a3bb-498b-ad4c-0a21db5365f9",
              "name": "email",
              "value": "={{   (     $('Busca cobrança4').all().map(i => i.json.Cliente).flat()       .find(c => c.CPF === $json.CPF) || {}   ).ResponsavelEmail || '' }}",
              "type": "string"
            }
          ]
        },
        "options": {}
      },
      "type": "n8n-nodes-base.set",
      "typeVersion": 3.4,
      "position": [
        208,
        2688
      ],
      "id": "304d41a9-da6a-43e2-95cf-1364e7d20c5d",
      "name": "Edit Fields10"
    },
    {
      "parameters": {
        "url": "https://chat-10api.jetsalesbrasil.com/contacts/",
        "sendQuery": true,
        "queryParameters": {
          "parameters": [
            {
              "name": "pageNumber",
              "value": "1"
            },
            {
              "name": "hasMore",
              "value": "true"
            },
            {
              "name": "searchParam",
              "value": "=557591105310"
            }
          ]
        },
        "sendHeaders": true,
        "headerParameters": {
          "parameters": [
            {
              "name": "Authorization",
              "value": "Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0ZW5hbnRJZCI6NSwicHJvZmlsZSI6ImFkbWluIiwic2Vzc2lvbklkIjo3LCJjaGFubmVsVHlwZSI6IndoYXRzYXBwIiwiaWF0IjoxNzU1NTE4NTQyLCJleHAiOjE4MTg1OTA1NDJ9.bL0EuUunp9ScP2d0yC1HQvTbzLNEAJ6ctLXbvxs23Oo"
            }
          ]
        },
        "options": {}
      },
      "type": "n8n-nodes-base.httpRequest",
      "typeVersion": 4.2,
      "position": [
        432,
        2688
      ],
      "id": "de341d14-4e93-481a-adf7-725018a8d5ce",
      "name": "Buscar contato10"
    },
    {
      "parameters": {
        "method": "POST",
        "url": "https://chat-10api.jetsalesbrasil.com/contacts",
        "sendHeaders": true,
        "headerParameters": {
          "parameters": [
            {
              "name": "Authorization",
              "value": "Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0ZW5hbnRJZCI6NSwicHJvZmlsZSI6ImFkbWluIiwic2Vzc2lvbklkIjo3LCJjaGFubmVsVHlwZSI6IndoYXRzYXBwIiwiaWF0IjoxNzU1NTE4NTQyLCJleHAiOjE4MTg1OTA1NDJ9.bL0EuUunp9ScP2d0yC1HQvTbzLNEAJ6ctLXbvxs23Oo"
            }
          ]
        },
        "sendBody": true,
        "specifyBody": "json",
        "jsonBody": "={\n    \"name\": {{ $json.contacts[0].id }},\n    \"number\": \"{{$json.contacts[0].number }}\",\n    \"wallets\": [],\n    \"extraInfo\": [],\n    \"defaultDepartment\": null,\n    \"tags\": [],\n    \"customFields\": {}\n}\n",
        "options": {}
      },
      "type": "n8n-nodes-base.httpRequest",
      "typeVersion": 4.2,
      "position": [
        880,
        2592
      ],
      "id": "7d1aa86e-a539-41ad-bc24-d4b27e720457",
      "name": "Criar contato10"
    },
    {
      "parameters": {
        "method": "POST",
        "url": "https://chat-10api.jetsalesbrasil.com/tickets",
        "sendHeaders": true,
        "headerParameters": {
          "parameters": [
            {
              "name": "Authorization",
              "value": "Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0ZW5hbnRJZCI6NSwicHJvZmlsZSI6ImFkbWluIiwic2Vzc2lvbklkIjo3LCJjaGFubmVsVHlwZSI6IndoYXRzYXBwIiwiaWF0IjoxNzU1NTE4NTQyLCJleHAiOjE4MTg1OTA1NDJ9.bL0EuUunp9ScP2d0yC1HQvTbzLNEAJ6ctLXbvxs23Oo"
            }
          ]
        },
        "sendBody": true,
        "specifyBody": "json",
        "jsonBody": "=\"jsonBody\": \"={{ { \n  contactId: $json.contacts?.[0]?.id, \n  mini: false, \n  number: String($json.contacts?.[0]?.number || ''), \n  isActiveDemand: true, \n  channel: 'whatsapp', \n  status: 'open', \n  whatsappId: 7, \n  queueId: null, \n  body: '*teste*:\\\\nola', \n  templateId: null, \n  params: [], \n  templateMediaId: null, \n  idFront: '1b6d8961-172b-4ae3-aae3-e0f59dd8744c', \n  typeTemplate: null \n} }}\"\n",
        "options": {
          "redirect": {
            "redirect": {}
          }
        }
      },
      "type": "n8n-nodes-base.httpRequest",
      "typeVersion": 4.2,
      "position": [
        880,
        2784
      ],
      "id": "38ec51bb-3f85-4d4a-a0f4-b21d373c8f55",
      "name": "criar ticket10",
      "onError": "continueErrorOutput"
    },
    {
      "parameters": {
        "method": "POST",
        "url": "https://chat-10api.jetsalesbrasil.com/tickets",
        "sendHeaders": true,
        "headerParameters": {
          "parameters": [
            {
              "name": "Authorization",
              "value": "Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0ZW5hbnRJZCI6NSwicHJvZmlsZSI6ImFkbWluIiwic2Vzc2lvbklkIjo3LCJjaGFubmVsVHlwZSI6IndoYXRzYXBwIiwiaWF0IjoxNzU1NTE4NTQyLCJleHAiOjE4MTg1OTA1NDJ9.bL0EuUunp9ScP2d0yC1HQvTbzLNEAJ6ctLXbvxs23Oo"
            },
            {
              "name": "Content-Type",
              "value": "application/json"
            },
            {
              "name": "host",
              "value": "chat-10api.jetsalesbrasil.com"
            }
          ]
        },
        "sendBody": true,
        "specifyBody": "json",
        "jsonBody": "={\n  \"mini\": false,\n  \"contactId\": {{$json.id}},\n  \"number\": \"{{$json.number}}\",\n  \"isActiveDemand\": true,\n  \"channel\": \"whatsapp\",\n  \"status\": \"open\",\n  \"whatsappId\": 7,\n  \"queueId\": null,\n  \"body\": \"Olá, {{ $json.contacts[0].name }}! Tudo bem?\\n\\nSeu título venceu em {{ new Date($('Filtra link4').item.json.DataVencimento).toLocaleDateString('pt-BR', { timeZone: 'America/Bahia' }) }} e encontra-se em atraso há **60 dias**.\\n\\n💰 Valor: {{ Number($('Filtra link4').item.json.Valor).toLocaleString('pt-BR', { style: 'currency', currency: 'BRL' }) }}\\n🔗 Pagamento imediato: {{ $('Filtra link4').item.json.Link || '' }}\\n🧾 Dados para transferência: Nubank: Ag 001 | Conta 69340787-5 | CNPJ 16698667/0001-40 | E B Ramos Eirelli\\n\\nEste é nosso **último aviso amigável**. Se não houver regularização em **24 horas**, daremos sequência aos procedimentos formais: suspensão de serviços, cobrança extrajudicial e apontamento nos órgãos de proteção ao crédito, conforme legislação aplicável.\\n\\nSe já pagou, por favor envie o comprovante. Caso precise de um acordo, responda esta mensagem para tratarmos agora.\",\n  \"templateId\": null,\n  \"params\": [],\n  \"templateMediaId\": null,\n  \"typeTemplate\": null\n}\n",
        "options": {}
      },
      "type": "n8n-nodes-base.httpRequest",
      "typeVersion": 4.2,
      "position": [
        1104,
        2592
      ],
      "id": "f5f20e9d-abc7-4c01-9564-48728bd98620",
      "name": "mandar mensagem20"
    },
    {
      "parameters": {
        "method": "POST",
        "url": "=https://chat-10api.jetsalesbrasil.com/messages/{{ $json.contacts[0].id }}",
        "sendHeaders": true,
        "headerParameters": {
          "parameters": [
            {
              "name": "Authorization",
              "value": "=Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0ZW5hbnRJZCI6NSwicHJvZmlsZSI6ImFkbWluIiwic2Vzc2lvbklkIjo3LCJjaGFubmVsVHlwZSI6IndoYXRzYXBwIiwiaWF0IjoxNzU1NTE4NTQyLCJleHAiOjE4MTg1OTA1NDJ9.bL0EuUunp9ScP2d0yC1HQvTbzLNEAJ6ctLXbvxs23Oo"
            }
          ]
        },
        "sendBody": true,
        "specifyBody": "json",
        "jsonBody": "={\n  \"fromMe\": true,\n  \"body\": \"Olá, {{ $json.contacts[0].name }}! Tudo bem?\\n\\nSeu título venceu em {{ new Date($('Filtra link4').item.json.DataVencimento).toLocaleDateString('pt-BR', { timeZone: 'America/Bahia' }) }} e encontra-se em atraso há **60 dias**.\\n\\n💰 Valor: {{ Number($('Filtra link4').item.json.Valor).toLocaleString('pt-BR', { style: 'currency', currency: 'BRL' }) }}\\n🔗 Pagamento imediato: {{ $('Filtra link4').item.json.Link || '' }}\\n🧾 Dados para transferência: Nubank: Ag 001 | Conta 69340787-5 | CNPJ 16698667/0001-40 | E B Ramos Eirelli\\n\\nEste é nosso **último aviso amigável**. Se não houver regularização em **24 horas**, daremos sequência aos procedimentos formais: suspensão de serviços, cobrança extrajudicial e apontamento nos órgãos de proteção ao crédito, conforme legislação aplicável.\\n\\nSe já pagou, por favor envie o comprovante. Caso precise de um acordo, responda esta mensagem para tratarmos agora.\",\n  \"idFront\": \"f2c7b4c1-8e8f-4f48-9d4a-6c8c5a5b1f60\",\n  \"note\": false\n}\n",
        "options": {}
      },
      "type": "n8n-nodes-base.httpRequest",
      "typeVersion": 4.2,
      "position": [
        1104,
        2784
      ],
      "id": "054d7d7e-08aa-4057-8e3b-e7642ac88d33",
      "name": "mandar mensagem21"
    },
    {
      "parameters": {
        "conditions": {
          "options": {
            "caseSensitive": true,
            "leftValue": "",
            "typeValidation": "strict",
            "version": 2
          },
          "conditions": [
            {
              "id": "7ef80ead-8d6c-4763-bb8f-f911b938a6e0",
              "leftValue": "={{ $json.UrlBoleto }}",
              "rightValue": "={{ $json.UrlBoleto }}",
              "operator": {
                "type": "string",
                "operation": "notEmpty",
                "singleValue": true
              }
            }
          ],
          "combinator": "and"
        },
        "options": {}
      },
      "type": "n8n-nodes-base.if",
      "typeVersion": 2.2,
      "position": [
        -16,
        2880
      ],
      "id": "08fe0ae2-9904-4f17-aed1-a1fcb652f573",
      "name": "Filtra link4"
    },
    {
      "parameters": {
        "conditions": {
          "options": {
            "caseSensitive": true,
            "leftValue": "",
            "typeValidation": "strict",
            "version": 2
          },
          "conditions": [
            {
              "id": "0d07a808-bd76-40b9-be0c-e49a0bde4894",
              "leftValue": "={{ $json.contacts }}",
              "rightValue": "",
              "operator": {
                "type": "array",
                "operation": "empty",
                "singleValue": true
              }
            }
          ],
          "combinator": "and"
        },
        "options": {}
      },
      "type": "n8n-nodes-base.if",
      "typeVersion": 2.2,
      "position": [
        656,
        2688
      ],
      "id": "08eeec60-53d4-48a5-9fef-cc5f0607224a",
      "name": "Já cadastrado ?8"
    },
    {
      "parameters": {
        "conditions": {
          "options": {
            "caseSensitive": true,
            "leftValue": "",
            "typeValidation": "strict",
            "version": 2
          },
          "conditions": [
            {
              "id": "0d07a808-bd76-40b9-be0c-e49a0bde4894",
              "leftValue": "={{ $json.contacts }}",
              "rightValue": "",
              "operator": {
                "type": "array",
                "operation": "empty",
                "singleValue": true
              }
            }
          ],
          "combinator": "and"
        },
        "options": {}
      },
      "type": "n8n-nodes-base.if",
      "typeVersion": 2.2,
      "position": [
        656,
        3072
      ],
      "id": "59092678-98f5-4734-b425-ae3d103214ed",
      "name": "Já cadastrado ?9"
    },
    {
      "parameters": {
        "assignments": {
          "assignments": [
            {
              "id": "e6333f86-745e-4f82-b4b5-cb6ebb76ac6a",
              "name": "telefone",
              "value": "={{\n  (() => {\n    // 1) pega o telefone pelo CPF e deixa só dígitos\n    let tel = (\n      ($('Busca cobrança').all().map(i => i.json.Cliente).flat()\n        .find(c => c.CPF === $json.CPF) || {}\n      ).Telefone || ''\n    ).replace(/\\D/g, '');\n\n    if (!tel) return '';\n\n    // 2) trabalha no formato local (sem 55) para detectar/remover o 9º dígito\n    let local = tel.startsWith('55') ? tel.slice(2) : tel;\n\n    // se for celular (11 dígitos) e tiver '9' logo após o DDD, remove\n    if (local.length === 11 && local[2] === '9') {\n      local = local.slice(0, 2) + local.slice(3);\n    }\n\n    // 3) remonta e aplica a regra do 55: se final tiver < 13, prefixa 55 (uma vez)\n    let out = tel.startsWith('55') ? '55' + local : local;\n    if (out.length < 13) out = '55' + local;\n\n    return out;\n  })()\n}}\n",
              "type": "string"
            },
            {
              "id": "551f5d8f-9ee9-47c7-8c43-7c090484feaa",
              "name": "nome",
              "value": "={{ \n  ( $('Busca cobrança').all().map(i => i.json.Cliente).flat()\n    .find(c => c.CPF === $json.CPF) || {} \n  ).Nome || '' \n}}",
              "type": "string"
            },
            {
              "id": "10c7426b-a3bb-498b-ad4c-0a21db5365f9",
              "name": "email",
              "value": "={{   (     $('Busca cobrança').all().map(i => i.json.Cliente).flat()       .find(c => c.CPF === $json.CPF) || {}   ).ResponsavelEmail || '' }}",
              "type": "string"
            }
          ]
        },
        "options": {}
      },
      "type": "n8n-nodes-base.set",
      "typeVersion": 3.4,
      "position": [
        240,
        -336
      ],
      "id": "3914059f-eeef-41a1-ad55-edd31c5d5d80",
      "name": "boleto"
    }
  ],
  "connections": {
    "Busca CPF": {
      "main": [
        [
          {
            "node": "filtro data",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "Busca cobrança": {
      "main": [
        [
          {
            "node": "Busca CPF",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "Schedule Trigger1": {
      "main": [
        [
          {
            "node": "Busca cobrança1",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "Busca CPF1": {
      "main": [
        [
          {
            "node": "Filtra data1",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "Busca cobrança1": {
      "main": [
        [
          {
            "node": "Busca CPF1",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "filtro data": {
      "main": [
        [
          {
            "node": "Filtra link",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "Schedule Trigger": {
      "main": [
        [
          {
            "node": "Busca cobrança",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "Buscar contato": {
      "main": [
        [
          {
            "node": "Já cadastrado ?1",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "Criar contato": {
      "main": [
        [
          {
            "node": "mandar mensagem",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "criar ticket": {
      "main": [
        [],
        [
          {
            "node": "mandar mensagem3",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "Schedule Trigger2": {
      "main": [
        [
          {
            "node": "Busca cobrança2",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "Busca CPF2": {
      "main": [
        [
          {
            "node": "Filter",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "Busca cobrança2": {
      "main": [
        [
          {
            "node": "Busca CPF2",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "Filter": {
      "main": [
        [
          {
            "node": "Filtra link2",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "Schedule Trigger3": {
      "main": [
        [
          {
            "node": "Busca cobrança3",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "Busca CPF3": {
      "main": [
        [
          {
            "node": "Filter2",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "Busca cobrança3": {
      "main": [
        [
          {
            "node": "Busca CPF3",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "Filter2": {
      "main": [
        [
          {
            "node": "Filtra link3",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "Schedule Trigger4": {
      "main": [
        [
          {
            "node": "Busca cobrança4",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "Busca CPF4": {
      "main": [
        [
          {
            "node": "Filter3",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "Busca cobrança4": {
      "main": [
        [
          {
            "node": "Busca CPF4",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "Filter3": {
      "main": [
        [
          {
            "node": "Filtra link4",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "Edit Fields6": {
      "main": [
        [
          {
            "node": "Buscar contato6",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "Buscar contato6": {
      "main": [
        [
          {
            "node": "Já cadastrado ?",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "Criar contato6": {
      "main": [
        [
          {
            "node": "mandar mensagem12",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "criar ticket6": {
      "main": [
        [],
        [
          {
            "node": "mandar mensagem13",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "Filtra link": {
      "main": [
        [
          {
            "node": "boleto",
            "type": "main",
            "index": 0
          }
        ],
        [
          {
            "node": "Edit Fields6",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "Já cadastrado ?": {
      "main": [
        [
          {
            "node": "Criar contato6",
            "type": "main",
            "index": 0
          }
        ],
        [
          {
            "node": "criar ticket6",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "Já cadastrado ?1": {
      "main": [
        [
          {
            "node": "Criar contato",
            "type": "main",
            "index": 0
          }
        ],
        [
          {
            "node": "criar ticket",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "Filtra data1": {
      "main": [
        [
          {
            "node": "Filtra link1",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "Edit Fields1": {
      "main": [
        [
          {
            "node": "Buscar contato1",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "Buscar contato1": {
      "main": [
        [
          {
            "node": "Já cadastrado ?3",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "Criar contato1": {
      "main": [
        [
          {
            "node": "mandar mensagem1",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "criar ticket1": {
      "main": [
        [],
        [
          {
            "node": "mandar mensagem4",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "Edit Fields7": {
      "main": [
        [
          {
            "node": "Buscar contato7",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "Buscar contato7": {
      "main": [
        [
          {
            "node": "Já cadastrado ?2",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "Criar contato7": {
      "main": [
        [
          {
            "node": "mandar mensagem14",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "criar ticket7": {
      "main": [
        [],
        [
          {
            "node": "mandar mensagem15",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "Filtra link1": {
      "main": [
        [
          {
            "node": "Edit Fields1",
            "type": "main",
            "index": 0
          }
        ],
        [
          {
            "node": "Edit Fields7",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "Já cadastrado ?2": {
      "main": [
        [
          {
            "node": "Criar contato7",
            "type": "main",
            "index": 0
          }
        ],
        [
          {
            "node": "criar ticket7",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "Já cadastrado ?3": {
      "main": [
        [
          {
            "node": "Criar contato1",
            "type": "main",
            "index": 0
          }
        ],
        [
          {
            "node": "criar ticket1",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "Edit Fields2": {
      "main": [
        [
          {
            "node": "Buscar contato2",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "Buscar contato2": {
      "main": [
        [
          {
            "node": "Já cadastrado ?5",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "Criar contato2": {
      "main": [
        [
          {
            "node": "mandar mensagem2",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "criar ticket2": {
      "main": [
        [],
        [
          {
            "node": "mandar mensagem5",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "Edit Fields8": {
      "main": [
        [
          {
            "node": "Buscar contato8",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "Buscar contato8": {
      "main": [
        [
          {
            "node": "Já cadastrado ?4",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "Criar contato8": {
      "main": [
        [
          {
            "node": "mandar mensagem16",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "criar ticket8": {
      "main": [
        [],
        [
          {
            "node": "mandar mensagem17",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "Filtra link2": {
      "main": [
        [
          {
            "node": "Edit Fields2",
            "type": "main",
            "index": 0
          }
        ],
        [
          {
            "node": "Edit Fields8",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "Já cadastrado ?4": {
      "main": [
        [
          {
            "node": "Criar contato8",
            "type": "main",
            "index": 0
          }
        ],
        [
          {
            "node": "criar ticket8",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "Já cadastrado ?5": {
      "main": [
        [
          {
            "node": "Criar contato2",
            "type": "main",
            "index": 0
          }
        ],
        [
          {
            "node": "criar ticket2",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "Edit Fields3": {
      "main": [
        [
          {
            "node": "Buscar contato3",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "Buscar contato3": {
      "main": [
        [
          {
            "node": "Já cadastrado ?7",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "Criar contato3": {
      "main": [
        [
          {
            "node": "mandar mensagem6",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "criar ticket3": {
      "main": [
        [],
        [
          {
            "node": "mandar mensagem7",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "Edit Fields9": {
      "main": [
        [
          {
            "node": "Buscar contato9",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "Buscar contato9": {
      "main": [
        [
          {
            "node": "Já cadastrado ?6",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "Criar contato9": {
      "main": [
        [
          {
            "node": "mandar mensagem18",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "criar ticket9": {
      "main": [
        [],
        [
          {
            "node": "mandar mensagem19",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "Filtra link3": {
      "main": [
        [
          {
            "node": "Edit Fields3",
            "type": "main",
            "index": 0
          }
        ],
        [
          {
            "node": "Edit Fields9",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "Já cadastrado ?6": {
      "main": [
        [
          {
            "node": "Criar contato9",
            "type": "main",
            "index": 0
          }
        ],
        [
          {
            "node": "criar ticket9",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "Já cadastrado ?7": {
      "main": [
        [
          {
            "node": "Criar contato3",
            "type": "main",
            "index": 0
          }
        ],
        [
          {
            "node": "criar ticket3",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "Edit Fields4": {
      "main": [
        [
          {
            "node": "Buscar contato4",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "Buscar contato4": {
      "main": [
        [
          {
            "node": "Já cadastrado ?9",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "Criar contato4": {
      "main": [
        [
          {
            "node": "mandar mensagem8",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "criar ticket4": {
      "main": [
        [],
        [
          {
            "node": "mandar mensagem9",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "Edit Fields10": {
      "main": [
        [
          {
            "node": "Buscar contato10",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "Buscar contato10": {
      "main": [
        [
          {
            "node": "Já cadastrado ?8",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "Criar contato10": {
      "main": [
        [
          {
            "node": "mandar mensagem20",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "criar ticket10": {
      "main": [
        [],
        [
          {
            "node": "mandar mensagem21",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "Filtra link4": {
      "main": [
        [
          {
            "node": "Edit Fields4",
            "type": "main",
            "index": 0
          }
        ],
        [
          {
            "node": "Edit Fields10",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "Já cadastrado ?8": {
      "main": [
        [
          {
            "node": "Criar contato10",
            "type": "main",
            "index": 0
          }
        ],
        [
          {
            "node": "criar ticket10",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "Já cadastrado ?9": {
      "main": [
        [
          {
            "node": "Criar contato4",
            "type": "main",
            "index": 0
          }
        ],
        [
          {
            "node": "criar ticket4",
            "type": "main",
            "index": 0
          }
        ]
      ]
    },
    "boleto": {
      "main": [
        [
          {
            "node": "Buscar contato",
            "type": "main",
            "index": 0
          }
        ]
      ]
    }
  },
  "pinData": {
    "Schedule Trigger": [
      {
        "timestamp": "2025-08-11T17:46:59.569-03:00",
        "Readable date": "August 11th 2025, 5:46:59 pm",
        "Readable time": "5:46:59 pm",
        "Day of week": "Monday",
        "Year": "2025",
        "Month": "August",
        "Day of month": "11",
        "Hour": "17",
        "Minute": "46",
        "Second": "59",
        "Timezone": "America/Sao_Paulo (UTC-03:00)"
      }
    ]
  },
  "meta": {
    "instanceId": "7cce0f22afd979eb5cdabdf675922ece8fbc867ff522ebcb757171840eb6783a"
  }
}
