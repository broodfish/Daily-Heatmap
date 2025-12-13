# Notion Reading Heatmap Generator

Generates a GitHub-contribution-style heatmap of your reading habits from a Notion database and saves it as an image.

## Setup

1.  **Notion Setup**:
    *   Create a Notion Integration at [https://www.notion.so/my-integrations](https://www.notion.so/my-integrations).
    *   Get the `Internal Integration Secret` (Token).
    *   Share your Database with this integration (Three dots > Connect to > Select your integration).
    *   Get the `Database ID` from the URL.

2.  **Database Structure**:
    *   Ensure your database has:
        *   A **Date** property (name: "Date").
        *   A **Number** property for duration (name: "Duration").

3.  **GitHub Secrets**:
    *   Add the following secrets to your repository:
        *   `NOTION_TOKEN`: Your integration secret.
        *   `NOTION_DATASOURCE_ID`: Your database ID.

## Local Development

```bash
pip install -r requirements.txt
# Set environment variables in your terminal or .env
python src/generate_heatmap.py
```

## Output

The script generates `public/heatmap.png`.