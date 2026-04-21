# 4월18일 일(라이브)- 제이 멘토와 OPAL추억

```jsx
{
  "title": "Untitled Opal app",
  "description": "",
  "version": "0.0.1",
  "nodes": [
    {
      "id": "75edf209-7541-427c-8a72-1b4eaa7e02d2",
      "type": "embed://a2/generate.bgl.json#module:main",
      "metadata": {
        "title": "Generate Drawing Text",
        "visual": {
          "x": 360,
          "y": 440
        },
        "userModified": true,
        "expected_output": [
          {
            "list": false,
            "type": "text",
            "description": "Textual description of a drawing, suitable for image generation."
          }
        ]
      },
      "configuration": {
        "config$prompt": {
          "role": "user",
          "parts": [
            {
              "text": "\n  이 이미지의 사람을 스타일 그대로 유지하고 개선해서 이미지 생성해줘. 귀여운 사람처럼 예쁘게 잘 그려줘. \n\n\n"
            }
          ]
        },
        "generation-mode": "image-pro",
        "p-aspect-ratio": "16:9"
      }
    },
    {
      "id": "ef98179b-5dde-4cdb-930e-e420e070f951",
      "type": "embed://a2/generate.bgl.json#module:main",
      "metadata": {
        "title": "Generate",
        "visual": {
          "x": 1180,
          "y": 320
        },
        "userModified": false
      },
      "configuration": {
        "config$prompt": {
          "role": "user",
          "parts": [
            {
              "text": " {{\"type\":\"asset\",\"path\":\"9211359b-4377-4795-9381-7bdbf03fb34c\",\"mimeType\":\"image/png\",\"title\":\"불사조\"}}  {{\"type\":\"asset\",\"path\":\"d9ce491a-db6b-4c24-a47d-f56c91d1a713\",\"mimeType\":\"image/png\",\"title\":\"여자아이\"}} 이 이미지에 있는 여자아이와 불사조를 하나의 장면에 담아줘. 스타일 그대로 유지.\n\n왼쪽에는 여자아이가 웃고 있고, 위에는 불사조가 날고 있어.\n\n불사조:{{\"type\":\"asset\",\"path\":\"9211359b-4377-4795-9381-7bdbf03fb34c\",\"mimeType\":\"image/png\",\"title\":\"불사조\"}}\n여자아이:{{\"type\":\"asset\",\"path\":\"d9ce491a-db6b-4c24-a47d-f56c91d1a713\",\"mimeType\":\"image/png\",\"title\":\"여자아이\"}}\n\n배경은 천국이야.\n\n"
            }
          ]
        },
        "generation-mode": "image-pro",
        "p-aspect-ratio": "16:9"
      }
    },
    {
      "id": "972dfea4-e7e3-419a-b094-79390eb45f54",
      "type": "embed://a2/generate.bgl.json#module:main",
      "metadata": {
        "title": "Generate 1",
        "visual": {
          "x": 1180,
          "y": 580
        },
        "userModified": false
      },
      "configuration": {
        "config$prompt": {
          "role": "user",
          "parts": [
            {
              "text": "{{\"type\":\"in\",\"path\":\"ef98179b-5dde-4cdb-930e-e420e070f951\",\"title\":\"Generate\"}}이 이미지를 첫번째 프레임으로 영상생성\n\n"
            }
          ]
        },
        "generation-mode": "video",
        "b-model-name": "veo-3.1",
        "p-aspect-ratio": "16:9",
        "p-disable-prompt-rewrite": false
      }
    },
    {
      "id": "b31e002f-9572-4b1b-8fb9-778c800df9a4",
      "type": "embed://a2/a2.bgl.json#module:render-outputs",
      "metadata": {
        "title": "Output",
        "visual": {
          "x": 1180,
          "y": 760
        },
        "userModified": false
      },
      "configuration": {
        "text": {
          "role": "user",
          "parts": [
            {
              "text": "{{\"type\":\"in\",\"path\":\"972dfea4-e7e3-419a-b094-79390eb45f54\",\"title\":\"Generate 1\"}}생성된 영상을 다운로드 받을 수 있는 웹사이트로 생성\n\n"
            }
          ]
        },
        "p-render-mode": "Auto",
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
      "from": "ef98179b-5dde-4cdb-930e-e420e070f951",
      "to": "972dfea4-e7e3-419a-b094-79390eb45f54",
      "out": "context",
      "in": "p-z-ef98179b-5dde-4cdb-930e-e420e070f951"
    },
    {
      "from": "972dfea4-e7e3-419a-b094-79390eb45f54",
      "to": "b31e002f-9572-4b1b-8fb9-778c800df9a4",
      "out": "context",
      "in": "p-z-972dfea4-e7e3-419a-b094-79390eb45f54"
    }
  ],
  "url": "drive:/1QDH0GupuKM3POi4z7twdI23jbLDtQ1-M",
  "metadata": {
    "visual": {
      "presentation": {
        "themes": {
          "2ceb21e7-1f27-41a1-9d6d-64627ee674ca": {
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
        "theme": "2ceb21e7-1f27-41a1-9d6d-64627ee674ca"
      }
    },
    "parameters": {}
  },
  "assets": {
    "275524e0-0122-4c8a-889c-c1a294e1ce1b": {
      "data": [
        {
          "parts": [
            {
              "storedData": {
                "handle": "drive:/14qyd0iQ7vFJpwUzs2_uI1FrGmm7eZBpI",
                "mimeType": "image/png",
                "contentLength": 43996
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
          "x": 20,
          "y": 400
        },
        "subType": "drawable"
      }
    },
    "5ffa3e34-e267-4c6a-a67a-629b24bcc011": {
      "data": [
        {
          "parts": [
            {
              "storedData": {
                "handle": "drive:/1eLi1bIxti3pLpvuJ5Hvu-4kr2JEr2iFb",
                "mimeType": "image/png",
                "contentLength": 1742172
              }
            }
          ],
          "role": "user"
        }
      ],
      "metadata": {
        "title": "Image (3).png",
        "type": "file",
        "visual": {
          "x": 20,
          "y": 140
        },
        "managed": true
      }
    },
    "9211359b-4377-4795-9381-7bdbf03fb34c": {
      "data": [
        {
          "role": "user",
          "parts": [
            {
              "storedData": {
                "handle": "drive:/12l3D4SteB3CjMwBger_pUobgoTzk3wbV",
                "mimeType": "image/png",
                "contentLength": 691860
              }
            }
          ]
        }
      ],
      "metadata": {
        "title": "불사조",
        "type": "file",
        "visual": {
          "x": 760,
          "y": 160
        },
        "managed": true
      }
    },
    "26bc0919-8879-405b-9c03-f5fb71756072": {
      "data": [
        {
          "parts": [
            {
              "storedData": {
                "handle": "drive:/156LYHRSBD8qA0iiM7Ui7rqlFiTvzPDtJ",
                "mimeType": "image/png",
                "contentLength": 33556
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
          "x": 20,
          "y": 720
        },
        "subType": "drawable"
      }
    },
    "d9ce491a-db6b-4c24-a47d-f56c91d1a713": {
      "data": [
        {
          "role": "user",
          "parts": [
            {
              "storedData": {
                "handle": "drive:/1K6fi3BHIvzIbSqanGePj8UItU0y2Y2YC",
                "mimeType": "image/png",
                "contentLength": 628928
              }
            }
          ]
        }
      ],
      "metadata": {
        "title": "여자아이",
        "type": "file",
        "visual": {
          "x": 760,
          "y": 500
        },
        "managed": true
      }
    }
  }
}
```