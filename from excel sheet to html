import pandas as pd

needed_sheets = [0,1,2]
html_table_id = 'svok_desc'
html_table_classes = 'display compact nowrap'
html_file_name_base = 'svok'
excel_file = "t.XLSX"

dfs = list()
for sheet in needed_sheets:
    dfs.append(pd.read_excel(excel_file,sheet_name=sheet))
    
for num, df in enumerate(dfs):
    html = df.to_html(na_rep='',table_id=html_table_id, classes=html_table_classes)
    with open(f'{html_file_name_base}{num}.html', "w", encoding="utf-8") as file:
        file.write(html)
