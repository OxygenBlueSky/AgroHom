# Claude Instructions for AgroHomeo Analysis Project

## Code Style Guidelines

### Python Indentation
- **CRITICAL**: Always use proper Python indentation to avoid PyCharm errors
- Use **4 spaces** for each indentation level (not tabs)
- Ensure consistent indentation throughout all code blocks
- When creating or editing Jupyter notebook cells, ensure proper Python syntax with correct indentation

### Jupyter Notebook Format
- When adding code to Jupyter notebooks (.ipynb files), each line in the source array must end with `\n` (newline character)
- Example format:
  ```json
  "source": [
      "# Comment\n",
      "def function():\n",
      "    return True\n"
  ]
  ```
- This ensures proper display in PyCharm and Jupyter environments

### Data Visualization
- All heatmaps use the **Greens** colormap (`cmap='Greens'`)
- Consistent styling across all visualizations:
  - Figure DPI: 300
  - Title font size: 18 (`TITLE_FS`)
  - Label font size: 16 (`AXIS_LABEL_FS`)
  - Tick/legend/data-label font size: 14 (`TICK_FS` / `LEGEND_FS` / `DATA_LABEL_FS`)
  - Tight layout with `bbox_inches='tight'`
- Font sizes are defined once as named constants in the Global Font Size
  Configuration block (Cell 4) and reused everywhere via those constants
  (never hardcode a new numeric `fontsize=`/`labelsize=` value) — see
  `TITLE_FS`, `AXIS_LABEL_FS`, `TICK_FS`, `LEGEND_FS`, `LEGEND_TITLE_FS`,
  `DATA_LABEL_FS`, `HMAP_ANNOT_FS`, `HMAP_TICK_FS`, `PLOTLY_TEXT_FS`,
  `PLOTLY_TITLE_FS`

### Data File
- Primary data source: `data_agrohom/Leo all extractions.xlsx`
- Always verify file paths before executing code

## Project Structure

### Key Files
- **agro_hom_figures260212.ipynb**: Main analysis notebook with all visualizations
- **data_agrohom/**: Directory containing data files

### Visualization Outputs
All generated PNG files are saved in the project root directory with high resolution (300 dpi).

## General Coding Practices
- Always test code for syntax errors before committing
- Maintain consistent formatting across similar code blocks
- Follow existing patterns in the codebase for new visualizations
