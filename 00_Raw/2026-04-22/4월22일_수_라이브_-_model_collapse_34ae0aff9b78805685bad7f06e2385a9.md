# 4월22일 수(라이브)- model collapse

```jsx
{
  "title": "Untitled Opal app",
  "description": "",
  "version": "0.0.1",
  "nodes": [
    {
      "id": "0bb272f0-3dbd-4f8b-add9-301bc8435f1b",
      "type": "embed://a2/generate.bgl.json#module:main",
      "metadata": {
        "title": "1차",
        "visual": {
          "x": 560,
          "y": 120
        },
        "userModified": true
      },
      "configuration": {
        "config$prompt": {
          "parts": [
            {
              "text": " {{\"type\":\"asset\",\"path\":\"f6a4ab6d-5e7a-4fa1-a9ff-6d33ab286d95\",\"mimeType\":\"image/png\",\"title\":\"Drawing\"}} 이 이미지를 기반으로 이미지 생성해줘."
            }
          ],
          "role": "user"
        },
        "generation-mode": "image",
        "p-aspect-ratio": "1:1"
      }
    },
    {
      "id": "1e74aae4-cbbb-4dcc-8296-9f8de88b5459",
      "type": "embed://a2/generate.bgl.json#module:main",
      "metadata": {
        "title": "2차",
        "visual": {
          "x": 560,
          "y": 300
        },
        "userModified": true
      },
      "configuration": {
        "config$prompt": {
          "role": "user",
          "parts": [
            {
              "text": " {{\"type\":\"in\",\"path\":\"0bb272f0-3dbd-4f8b-add9-301bc8435f1b\",\"title\":\"1차\"}}이 이미지를 기반으로 이미지 생성해줘.\n\n"
            }
          ]
        },
        "generation-mode": "image",
        "p-aspect-ratio": "1:1"
      }
    },
    {
      "id": "5f58e153-1d32-4ec3-a1af-fc34f299d3d3",
      "type": "embed://a2/generate.bgl.json#module:main",
      "metadata": {
        "title": "3차",
        "visual": {
          "x": 560,
          "y": 460
        },
        "userModified": true
      },
      "configuration": {
        "config$prompt": {
          "role": "user",
          "parts": [
            {
              "text": " {{\"type\":\"in\",\"path\":\"1e74aae4-cbbb-4dcc-8296-9f8de88b5459\",\"title\":\"2차\"}}이 이미지를 기반으로 이미지 생성해줘.\n\n"
            }
          ]
        },
        "generation-mode": "image",
        "p-aspect-ratio": "1:1"
      }
    },
    {
      "id": "47188a7f-a6d6-4d80-8e8a-b51d29f922e7",
      "type": "embed://a2/generate.bgl.json#module:main",
      "metadata": {
        "title": "4차",
        "visual": {
          "x": 560,
          "y": 620
        },
        "userModified": true
      },
      "configuration": {
        "config$prompt": {
          "role": "user",
          "parts": [
            {
              "text": " {{\"type\":\"in\",\"path\":\"5f58e153-1d32-4ec3-a1af-fc34f299d3d3\",\"title\":\"3차\"}}이 이미지를 기반으로 이미지 생성해줘.\n\n"
            }
          ]
        },
        "generation-mode": "image",
        "p-aspect-ratio": "1:1"
      }
    },
    {
      "id": "5b000a9a-9aa0-4bf9-a806-0e9af91d17c0",
      "type": "embed://a2/generate.bgl.json#module:main",
      "metadata": {
        "title": "5차",
        "visual": {
          "x": 560,
          "y": 760
        },
        "userModified": true
      },
      "configuration": {
        "config$prompt": {
          "role": "user",
          "parts": [
            {
              "text": " {{\"type\":\"in\",\"path\":\"47188a7f-a6d6-4d80-8e8a-b51d29f922e7\",\"title\":\"4차\"}}이 이미지를 기반으로 이미지 생성해줘.\n\n"
            }
          ]
        },
        "generation-mode": "image",
        "p-aspect-ratio": "1:1"
      }
    },
    {
      "id": "b57a118c-f753-4750-a65f-7c8d25ca5bb5",
      "type": "embed://a2/generate.bgl.json#module:main",
      "metadata": {
        "title": "6차",
        "visual": {
          "x": 560,
          "y": 900
        },
        "userModified": true
      },
      "configuration": {
        "config$prompt": {
          "role": "user",
          "parts": [
            {
              "text": " {{\"type\":\"in\",\"path\":\"5b000a9a-9aa0-4bf9-a806-0e9af91d17c0\",\"title\":\"5차\"}}이 이미지를 기반으로 이미지 생성해줘.\n\n"
            }
          ]
        },
        "generation-mode": "image",
        "p-aspect-ratio": "1:1"
      }
    },
    {
      "id": "8d8a896a-4f22-4d16-b743-0e9c1f944cd5",
      "type": "embed://a2/a2.bgl.json#module:render-outputs",
      "metadata": {
        "title": "Output",
        "visual": {
          "x": 1140,
          "y": 460
        },
        "userModified": false
      },
      "configuration": {
        "p-render-mode": "Auto",
        "text": {
          "role": "user",
          "parts": [
            {
              "text": "\n\n {{\"type\":\"in\",\"path\":\"0bb272f0-3dbd-4f8b-add9-301bc8435f1b\",\"title\":\"1차\"}} {{\"type\":\"in\",\"path\":\"1e74aae4-cbbb-4dcc-8296-9f8de88b5459\",\"title\":\"2차\"}} {{\"type\":\"in\",\"path\":\"5f58e153-1d32-4ec3-a1af-fc34f299d3d3\",\"title\":\"3차\"}} {{\"type\":\"in\",\"path\":\"47188a7f-a6d6-4d80-8e8a-b51d29f922e7\",\"title\":\"4차\"}} {{\"type\":\"in\",\"path\":\"5b000a9a-9aa0-4bf9-a806-0e9af91d17c0\",\"title\":\"5차\"}} {{\"type\":\"in\",\"path\":\"b57a118c-f753-4750-a65f-7c8d25ca5bb5\",\"title\":\"6차\"}}인풋부터 1세대~4세대까지 이미지가 변하는 모델 붕괴를 눈으로 보여주기]\n실습 1: \"AI가 AI를 먹으면 이렇게 됩니다\" (붕괴 시연)\n원리: OPAL로 이미지를 생성 → 그 결과물을 다시 OPAL에 넣고 \"이거랑 비슷하게 만들어줘\" → 그 결과를 또 넣고 → 반복 (5~6세대)\n\n진행 순서:\n\n1세대: 시청자가 채팅으로 주제를 던짐 \n2세대: OPAL이 만든 벚꽃길 이미지를 다시 OPAL에 넣고 \"이 이미지를 참고해서 다시 그려줘\"\n3세대~6세대: 계속 반복\n\n예상 결과 (시청자 충격 포인트):\n\n1~2세대: \n3~4세대: \n5~6세대: \n\n\n"
            }
          ]
        },
        "b-render-model-name": "gemini-flash",
        "b-system-instruction": {
          "role": "user",
          "parts": [
            {
              "text": ""
            }
          ]
        }
      }
    }
  ],
  "edges": [
    {
      "from": "0bb272f0-3dbd-4f8b-add9-301bc8435f1b",
      "to": "1e74aae4-cbbb-4dcc-8296-9f8de88b5459",
      "out": "context",
      "in": "p-z-0bb272f0-3dbd-4f8b-add9-301bc8435f1b"
    },
    {
      "from": "1e74aae4-cbbb-4dcc-8296-9f8de88b5459",
      "to": "5f58e153-1d32-4ec3-a1af-fc34f299d3d3",
      "out": "context",
      "in": "p-z-1e74aae4-cbbb-4dcc-8296-9f8de88b5459"
    },
    {
      "from": "5f58e153-1d32-4ec3-a1af-fc34f299d3d3",
      "to": "47188a7f-a6d6-4d80-8e8a-b51d29f922e7",
      "out": "context",
      "in": "p-z-5f58e153-1d32-4ec3-a1af-fc34f299d3d3"
    },
    {
      "from": "47188a7f-a6d6-4d80-8e8a-b51d29f922e7",
      "to": "5b000a9a-9aa0-4bf9-a806-0e9af91d17c0",
      "out": "context",
      "in": "p-z-47188a7f-a6d6-4d80-8e8a-b51d29f922e7"
    },
    {
      "from": "5b000a9a-9aa0-4bf9-a806-0e9af91d17c0",
      "to": "b57a118c-f753-4750-a65f-7c8d25ca5bb5",
      "out": "context",
      "in": "p-z-5b000a9a-9aa0-4bf9-a806-0e9af91d17c0"
    },
    {
      "from": "0bb272f0-3dbd-4f8b-add9-301bc8435f1b",
      "to": "8d8a896a-4f22-4d16-b743-0e9c1f944cd5",
      "out": "context",
      "in": "p-z-0bb272f0-3dbd-4f8b-add9-301bc8435f1b"
    },
    {
      "from": "1e74aae4-cbbb-4dcc-8296-9f8de88b5459",
      "to": "8d8a896a-4f22-4d16-b743-0e9c1f944cd5",
      "out": "context",
      "in": "p-z-1e74aae4-cbbb-4dcc-8296-9f8de88b5459"
    },
    {
      "from": "5f58e153-1d32-4ec3-a1af-fc34f299d3d3",
      "to": "8d8a896a-4f22-4d16-b743-0e9c1f944cd5",
      "out": "context",
      "in": "p-z-5f58e153-1d32-4ec3-a1af-fc34f299d3d3"
    },
    {
      "from": "47188a7f-a6d6-4d80-8e8a-b51d29f922e7",
      "to": "8d8a896a-4f22-4d16-b743-0e9c1f944cd5",
      "out": "context",
      "in": "p-z-47188a7f-a6d6-4d80-8e8a-b51d29f922e7"
    },
    {
      "from": "5b000a9a-9aa0-4bf9-a806-0e9af91d17c0",
      "to": "8d8a896a-4f22-4d16-b743-0e9c1f944cd5",
      "out": "context",
      "in": "p-z-5b000a9a-9aa0-4bf9-a806-0e9af91d17c0"
    },
    {
      "from": "b57a118c-f753-4750-a65f-7c8d25ca5bb5",
      "to": "8d8a896a-4f22-4d16-b743-0e9c1f944cd5",
      "out": "context",
      "in": "p-z-b57a118c-f753-4750-a65f-7c8d25ca5bb5"
    }
  ],
  "url": "drive:/1VKBvJty5bzLwsXcyTVjSEmmtgmpyyrBj",
  "metadata": {
    "visual": {
      "presentation": {
        "themes": {
          "eeb08b60-88e3-437d-b654-47834f4b82ee": {
            "themeColors": {
              "primaryColor": "#1a1a1a",
              "secondaryColor": "#7a7a7a",
              "backgroundColor": "#ffffff",
              "textColor": "#1a1a1a",
              "primaryTextColor": "#ffffff"
            },
            "template": "basic",
            "isDefaultTheme": true,
            "palette": {
              "primary": {
                "0": "#000000",
                "5": "#001417",
                "10": "#001f24",
                "15": "#002b30",
                "20": "#00363d",
                "25": "#00424a",
                "30": "#004f58",
                "35": "#005b66",
                "40": "#006874",
                "50": "#008391",
                "60": "#00a0b0",
                "70": "#22bccf",
                "80": "#4fd8eb",
                "90": "#97f0ff",
                "95": "#d0f8ff",
                "98": "#edfcff",
                "99": "#f6feff",
                "100": "#ffffff"
              },
              "secondary": {
                "0": "#000000",
                "5": "#001417",
                "10": "#051f23",
                "15": "#10292d",
                "20": "#1c3438",
                "25": "#273f43",
                "30": "#334b4f",
                "35": "#3e565b",
                "40": "#4a6267",
                "50": "#637b80",
                "60": "#7c959a",
                "70": "#96b0b4",
                "80": "#b1cbd0",
                "90": "#cde7ec",
                "95": "#dbf6fa",
                "98": "#edfcff",
                "99": "#f6feff",
                "100": "#ffffff"
              },
              "tertiary": {
                "0": "#000000",
                "5": "#030f2c",
                "10": "#0e1b37",
                "15": "#192541",
                "20": "#24304d",
                "25": "#2f3b58",
                "30": "#3b4664",
                "35": "#465271",
                "40": "#525e7d",
                "50": "#6b7697",
                "60": "#8490b2",
                "70": "#9faace",
                "80": "#bac6ea",
                "90": "#dae2ff",
                "95": "#eef0ff",
                "98": "#faf8ff",
                "99": "#fefbff",
                "100": "#ffffff"
              },
              "neutral": {
                "0": "#000000",
                "5": "#0e1212",
                "10": "#191c1d",
                "15": "#232627",
                "20": "#2e3132",
                "25": "#393c3d",
                "30": "#444748",
                "35": "#505354",
                "40": "#5c5f5f",
                "50": "#747878",
                "60": "#8e9192",
                "70": "#a9acac",
                "80": "#c4c7c7",
                "90": "#e1e3e3",
                "95": "#eff1f1",
                "98": "#f8fafa",
                "99": "#fafdfd",
                "100": "#ffffff"
              },
              "neutralVariant": {
                "0": "#000000",
                "5": "#091214",
                "10": "#141d1f",
                "15": "#1e2729",
                "20": "#293234",
                "25": "#343d3f",
                "30": "#3f484a",
                "35": "#4b5456",
                "40": "#576062",
                "50": "#6f797a",
                "60": "#899294",
                "70": "#a3adaf",
                "80": "#bfc8ca",
                "90": "#dbe4e6",
                "95": "#e9f2f4",
                "98": "#f2fbfd",
                "99": "#f6feff",
                "100": "#ffffff"
              },
              "error": {
                "0": "#000000",
                "5": "#2d0001",
                "10": "#410002",
                "15": "#540003",
                "20": "#690005",
                "25": "#7e0007",
                "30": "#93000a",
                "35": "#a80710",
                "40": "#ba1a1a",
                "50": "#de3730",
                "60": "#ff5449",
                "70": "#ff897d",
                "80": "#ffb4ab",
                "90": "#ffdad6",
                "95": "#ffedea",
                "98": "#fff8f7",
                "99": "#fffbff",
                "100": "#ffffff"
              }
            }
          }
        },
        "theme": "eeb08b60-88e3-437d-b654-47834f4b82ee"
      }
    },
    "parameters": {}
  },
  "assets": {
    "f6a4ab6d-5e7a-4fa1-a9ff-6d33ab286d95": {
      "data": [
        {
          "parts": [
            {
              "storedData": {
                "handle": "drive:/1-rWvGEQh8foy40GtzlKu16VxrZaLpcOL",
                "mimeType": "image/png",
                "contentLength": 42208
              }
            }
          ],
          "role": "user"
        }
      ],
      "metadata": {
        "title": "Drawing",
        "type": "content",
        "visual": {
          "x": 140,
          "y": 280
        },
        "subType": "drawable"
      }
    }
  }
}
```