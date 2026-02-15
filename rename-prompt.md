You are a naming assistant. Given a list of file paths and minimal context from a static website, suggest a new filename (basename only, same extension) for each file. Rules:
- Lowercase, kebab-case, no spaces. SEO-friendly and human-readable.
- For HTML: use page purpose (e.g. about-us.html, contact.html). Keep index.html as index.html.
- For CSS/JS: use purpose (e.g. main-styles.css, analytics.js).
- For images: use content (e.g. logo-infygate.webp, hero-banner.webp). Use alt/title when provided.
- Return a JSON object: keys = exact original path strings, values = new basename only (e.g. "main.css"). Preserve extension.
- Do not change path prefix (e.g. css/ stays css/ by returning "name.css" not "css/name.css").

Files and context:
[
  {
    "path": "404.html",
    "context": {
      "title": "",
      "first_heading": "404"
    }
  },
  {
    "path": "css/138575cd4810b87ba229d0ae35cbc7b8.css",
    "context": {
      "path": "css/138575cd4810b87ba229d0ae35cbc7b8.css"
    }
  },
  {
    "path": "css/4846897a8ea4821d99984bafb364df80.css",
    "context": {
      "path": "css/4846897a8ea4821d99984bafb364df80.css"
    }
  },
  {
    "path": "css/4957171073492227171d872757d04770.css",
    "context": {
      "path": "css/4957171073492227171d872757d04770.css"
    }
  },
  {
    "path": "css/559e64bf161e61fa0aca6e864c78191d.css",
    "context": {
      "path": "css/559e64bf161e61fa0aca6e864c78191d.css"
    }
  },
  {
    "path": "css/84d4a0216f16f715d9b301db3a8da352.css",
    "context": {
      "path": "css/84d4a0216f16f715d9b301db3a8da352.css"
    }
  },
  {
    "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css",
    "context": {
      "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css"
    }
  },
  {
    "path": "css/internal-styles.css",
    "context": {
      "path": "css/internal-styles.css"
    }
  },
  {
    "path": "imgs/0c6d55d4f9b488bc863466c81b006bdf.webp",
    "context": {
      "refs": [
        {
          "alt": "TRADEMARK & DESIGN IN INDIA",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/258b35e0b77c83815fc4a8e8659ca0ad.webp",
    "context": {
      "refs": [
        {
          "alt": "PATENT RESEARCH & ANALYSIS",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/34db0202f40e9a91e76e10b758b90705.webp",
    "context": {
      "refs": [
        {
          "alt": "PATENT RESEARCH & ANALYSIS",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4054b71a4baa851892a11daebd9488f5.webp",
    "context": {
      "refs": [
        {
          "alt": "PATENT DRAFTING & PROSECUTION SERVICES",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7b7e389f4ded91b80efaaffc0efca2c9.webp",
    "context": {
      "refs": [
        {
          "alt": "logo",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/82def5b0b3088e9788b023e6a88f1a3d.webp",
    "context": {
      "refs": [
        {
          "alt": "PATENT LITIGATION SUPPORT",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8eae26a522a5d92c39025466810af1cb.webp",
    "context": {
      "refs": [
        {
          "alt": "ABOUT US",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/99db4ca8abe506c7afedab05a55df5f5.webp",
    "context": {
      "refs": [
        {
          "alt": "PATENT LITIGATION SUPPORT",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a0030dbcba0ad75734aa1fc8c52d72a1.webp",
    "context": {
      "refs": [
        {
          "alt": "PILLARS OF COMPANY: OUR TEAM",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b2b18f356bfc8e7955e53c0993ad3ea8.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/cf0c35355a9618a606899b0da21c7beb.webp",
    "context": {
      "refs": [
        {
          "alt": "PATENT DRAFTING & PROSECUTION SERVICES",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cfe556cd33ef9a3d8c48226a78aac197.webp",
    "context": {
      "refs": [
        {
          "alt": "TRADEMARK & DESIGN IN INDIA",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "index.html",
    "context": {
      "title": "Cryyptic IP Research & Management Services LLP",
      "first_heading": "Cryyptic IP Research & Management Services LLP"
    }
  },
  {
    "path": "js/03b2eaae6007054a68c38e495f894dba.js",
    "context": {
      "path": "js/03b2eaae6007054a68c38e495f894dba.js"
    }
  },
  {
    "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js",
    "context": {
      "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js"
    }
  },
  {
    "path": "js/0c46896987137b0016246f6bc2243099.js",
    "context": {
      "path": "js/0c46896987137b0016246f6bc2243099.js"
    }
  },
  {
    "path": "js/165d7b0ddfa33362140feea997351b77.js",
    "context": {
      "path": "js/165d7b0ddfa33362140feea997351b77.js"
    }
  },
  {
    "path": "js/16df9ef05001a1741857bf99f5a5738f.js",
    "context": {
      "path": "js/16df9ef05001a1741857bf99f5a5738f.js"
    }
  },
  {
    "path": "js/2a85c11e395a8380b5915443e926b569.js",
    "context": {
      "path": "js/2a85c11e395a8380b5915443e926b569.js"
    }
  },
  {
    "path": "js/34be5330971fdbd18985525bd994b0aa.js",
    "context": {
      "path": "js/34be5330971fdbd18985525bd994b0aa.js"
    }
  },
  {
    "path": "js/35c5f9e096d4da33d2a62031daf14248.js",
    "context": {
      "path": "js/35c5f9e096d4da33d2a62031daf14248.js"
    }
  },
  {
    "path": "js/3d70953a848219e749fedc2cdb906675.js",
    "context": {
      "path": "js/3d70953a848219e749fedc2cdb906675.js"
    }
  },
  {
    "path": "js/3e940a33e44b65c1c0af8bb80a893530.js",
    "context": {
      "path": "js/3e940a33e44b65c1c0af8bb80a893530.js"
    }
  },
  {
    "path": "js/544d012df7acf9c3f0920f67c9e322b9.js",
    "context": {
      "path": "js/544d012df7acf9c3f0920f67c9e322b9.js"
    }
  },
  {
    "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js",
    "context": {
      "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js"
    }
  },
  {
    "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js",
    "context": {
      "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js"
    }
  },
  {
    "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js",
    "context": {
      "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js"
    }
  },
  {
    "path": "js/7260bab328b0ad74815a5efb377bcc67.js",
    "context": {
      "path": "js/7260bab328b0ad74815a5efb377bcc67.js"
    }
  },
  {
    "path": "js/893de96f1b6da546bd7c814964723eca.js",
    "context": {
      "path": "js/893de96f1b6da546bd7c814964723eca.js"
    }
  },
  {
    "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js",
    "context": {
      "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js"
    }
  },
  {
    "path": "js/9455859483e31e4da0e28f10d0742c2a.js",
    "context": {
      "path": "js/9455859483e31e4da0e28f10d0742c2a.js"
    }
  },
  {
    "path": "js/9db10375d298678e53777a2347b87073.js",
    "context": {
      "path": "js/9db10375d298678e53777a2347b87073.js"
    }
  },
  {
    "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js",
    "context": {
      "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js"
    }
  },
  {
    "path": "js/a2261649751fa61b606222c9b2ea3b80.js",
    "context": {
      "path": "js/a2261649751fa61b606222c9b2ea3b80.js"
    }
  },
  {
    "path": "js/b0bade6d42c2702ca85774296cc507c4.js",
    "context": {
      "path": "js/b0bade6d42c2702ca85774296cc507c4.js"
    }
  },
  {
    "path": "js/b86ed7116f8971797e090ffb443f0437.js",
    "context": {
      "path": "js/b86ed7116f8971797e090ffb443f0437.js"
    }
  },
  {
    "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js",
    "context": {
      "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js"
    }
  },
  {
    "path": "js/cecb447a04bbe3e8982190dd6e697120.js",
    "context": {
      "path": "js/cecb447a04bbe3e8982190dd6e697120.js"
    }
  },
  {
    "path": "js/d80b370d82680fc786dcc943a327b9f2.js",
    "context": {
      "path": "js/d80b370d82680fc786dcc943a327b9f2.js"
    }
  },
  {
    "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js",
    "context": {
      "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js"
    }
  },
  {
    "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js",
    "context": {
      "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js"
    }
  },
  {
    "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js",
    "context": {
      "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js"
    }
  }
]

Return only a JSON object mapping each path to its new basename (same extension). No other text.