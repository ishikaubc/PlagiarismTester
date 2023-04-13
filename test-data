import csv
import os
from typing import List

def combine_csv_files(input_files: List[str], output_file: str):
    header_saved = False
    with open(output_file, 'w', newline='', encoding='utf-8') as outfile:
        writer = csv.writer(outfile)
        for file in input_files:
            with open(file, 'r', newline='', encoding='utf-8') as infile:
                reader = csv.reader(infile)
                header = next(reader)
                if not header_saved:
                    writer.writerow(header)
                    header_saved = True
                writer.writerows(reader)

def main():
    input_files = [
        'uk.co.keystagefun.squeeblesTT2.csv',
        'uk.co.lunarium.iluna.csv',
        'uk.co.nickfines.RealCalcPlus.csv',
        'uk.co.pocketlabs.pocketuniverse.csv',
        'uk.co.revolution.bs1dc.csv',
        'uk.co.stormeducational.namingpartsofthebody.android.csv',
        'uk.co.telgen.families.csv',
        'uk.co.topmarks.HitTheButton.csv',
        'uk.co.tso.ctt.csv',
        'umito.android.keychord.csv',
    ]
    output_file = 'combined-data.csv'

    combine_csv_files(input_files, output_file)

if _name_ == '_main_':
    main()