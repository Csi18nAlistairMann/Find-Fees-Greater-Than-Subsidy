# Find-Fees-Greater-Than-Subsidy
A short script to discover Bitcoin blocks where the fees were larger than the subsidy 

## dates-finessed.csv
Non-technical folks, you want this one!

TL;DR: fees > subsidy happened several times a year in the early days (upto end 2017), and then not for six years. They have now happened fourteen times between 9pm 07 May 2023 and 8:26pm 16 May 2023.

## Other files
The code findfeesgtsubsidy is a simple Bash script expecting to run on a Linux bitcoin full node - I used a raspiblitz. It takes around 36 hours to scan Bitcoin's entire blockchain on an RPi. You might prefer to download all.csv.bz2 and decompress it: use it as the logfile and the code will scan only the blocks since the last line.

## Update

Thank you to [Ramon](https://twitter.com/xanthin) for spotting original version improperly handled coinbases across multiple outputs and suggesting the fix. The issue affected 31,192 blocks: three more blocks were found where fees > subsidy, and two existing blocks found had the coinbase value changed upwards.
