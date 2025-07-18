# Oxenstierna 🦬⭐ (WIP)

##   MCPs for Riksarkivet 

Alot of mcps can be built with the help of: https://github.com/Riksarkivet/dataplattform/wiki

- Riksarkivet OAIPMH API Integration: https://github.com/Riksarkivet/dataplattform/wiki/OAI-PMH
- Riksarkivet IIIF API Integration: https://github.com/Riksarkivet/dataplattform/wiki/IIIF
- Riksarkivet Search API Integration https://github.com/Riksarkivet/dataplattform/wiki/Search-API
- (new) can we use this? with semantic search: https://forvaltningshistorik.riksarkivet.se/Index.htm <---
- AI-Riksarkviet HTRflow pypi 

![image](https://github.com/user-attachments/assets/bde56408-5135-4a2a-baf3-f26c32fab9dc)

___

Current implementation:
```
This server provides access to the Swedish National Archives (Riksarkivet) through multiple APIs.
    SEARCH-BASED WORKFLOW (start here):
    - search_records: Search for content by keywords (e.g., "coffee", "medical records")
    - get_collection_info: Explore what's available in a collection
    - get_all_manifests_from_pid: Get all image batches from a collection
    - get_manifest_info: Get details about a specific image batch
    - get_manifest_image: Download specific images from a batch
    - get_all_images_from_pid: Download all images from a collection
    URL BUILDING TOOLS:
    - build_image_url: Build IIIF Image URLs with custom parameters
    - get_image_urls_from_manifest: Get all URLs from an image batch
    - get_image_urls_from_pid: Get all URLs from a collection
    TYPICAL WORKFLOW:
    1. search_records("your keywords") → find PIDs
    2. get_collection_info(pid) → see what's available
    3. get_manifest_info(manifest_id) → explore specific image batch
    4. get_manifest_image(manifest_id, image_index) → download specific image
    Example PID: LmOmKigRrH6xqG3GjpvwY3
```
___


### Tools
- Riksarkivet OAIPMH Metadata API Integration
- Riksarkivet IIIF Image API Integration
- Riksarkivet IIIF Presentation API Integration

#### Search API

https://sok.riksarkivet.se/?Sokord=kaffe&f=True&EndastDigitaliserat=true&EndastDigitaliserat=false&TranskriberadText=true&TranskriberadText=false&Fritext=&Namn=&Ort=&DatumFran=&DatumTill=&AvanceradSok=false

The idea here is that you can use the search api to get hits across transcribed text:
https://data-acc.riksarkivet.se/api/records?transcribed_text=kaffe&only_digitised_materials=false&offset=0&limit=100&sort=relevance
![image](https://github.com/user-attachments/assets/549d695d-65e5-462a-accb-b892f351d524)

IIIF content search is not a viable option!

#### HTRflow
Would it be possible to HTR on the flow? 

https://huggingface.co/spaces/Gabriel/htrflow_mcp

![image](https://github.com/user-attachments/assets/64c876dc-d635-4e2a-b10b-cc5203b8f125)

![image](https://github.com/user-attachments/assets/2c54655b-50a2-4b52-b5b2-d44960a2e8d9)

<img width="1492" alt="W1lfkOp_xazuhoWtrCFb-" src="https://github.com/user-attachments/assets/19f64ad9-23c7-4240-8839-e790270150ec" />

schema: https://gabriel-htrflow-mcp.hf.space/gradio_api/mcp/schema

TODO:
- mcp https://github.com/knaw-huc/pagexml
- sperate content from outpit file
- visualizer

#### Resource
We want to resources simlair to this concept
- https://gradio-docs-mcp.hf.space/

Part of Riksarkivet OAIPMH API Integration can act as resource.
Also, iiif presentation and image api https://github.com/IIIF/api/blob/main/source/image/3.0/index.md

## FastMCP 2.0

https://gofastmcp.com/getting-started/welcome


## MCP Inspector Integration
- Use inspector for interactive testing and debugging

## Client

### Claude Desktop Integration
- Document how to add the server to Claude Desktop

<img width="1002" alt="image" src="https://github.com/user-attachments/assets/c8cdb0fc-828b-425b-b592-e7f712a27e32" />


### Aider
..
