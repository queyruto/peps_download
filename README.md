# peps_download

This is a fork of github project: https://github.com/olivierhagolle/peps_download. The differences are the following:
- Supports python 3
- New query parameter to select a specific tile
- New query parameter to define a geometry in Well Known Text standard 

## Examples

### for Sentinel-2
This software is still quite basic, but if you have an account at PEPS, you may download products using command lines like 

- `python ./peps_download.py  -c S2ST -a peps.txt -d 2018-01-01 -f 2018-01-31 -t 57KXB`

 which downloads the *Sentinel-2 single tile* corresponding to the 57KXB tile and acquired in January 2018.

- `python ./peps_download.py  -c S2ST -a peps.txt -d 2017-01-01 -f 2017-02-01  --geom "POLYGON((0.8362639474853495 43.73719801014047,1.1933196115478495 43.9669523968473,1.6437590646728495 43.875948803048,1.8250334787353495 43.61801226418353,1.6657317209228495 43.45474226426778,1.3581145334228495 43.32300876711054,0.9351409006103495 43.470690504609394,0.8362639474853495 43.73719801014047))"`

 which downloads the *Sentinel-2 single tile* products  acquired in January 2018 above an area of Toulouse


## Authentification 

The file peps.txt must contain your email address and your password on the same line, such as follows :
`your.email@address.fr top_secret`

To get an account : https://peps.cnes.fr/rocket/#/register


