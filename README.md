# GMT ETOPO1 Mariana Trench — Map Projection Variants

GMT (Generic Mapping Tools) shell scripts mapping the bathymetry of the Mariana Trench from the ETOPO1 global relief grid, each rendered in a different map projection. The pair demonstrates how the choice of projection changes the appearance and geometry of the same study area. The scripts have been used to generate figures in the author's marine-geomorphological and cartographic publications.

## What the scripts do

Each script clips an ETOPO1 subset over the Mariana Trench (grdcut), builds a bathymetric colour palette (makecpt), renders a shaded raster image in the chosen projection (grdimage), and adds a colour scale (psscale), contours (grdcontour), grid, scale bar and directional rose (psbasemap), toponymy labels (pstext) and the GMT logo (logo), before exporting to raster (psconvert).

## Projections

- GMT-20-script-JC-ETOPO1-MT.sh: Cassini transverse cylindrical projection (-JC)
- GMT-14-script-JY-ETOPO1-MT.sh: Cylindrical Equal-Area Gall-Peters projection (-JY)

## Data source

Global relief / bathymetry: ETOPO1 (1 arc-minute), via GMT earth_relief tiles.

## Requirements

- GMT 6.x (Generic Mapping Tools): https://www.generic-mapping-tools.org
- A POSIX shell (bash/sh)
- An ETOPO1 / earth_relief grid available locally

## Usage

Adjust the -R region and the -J projection at the top of the chosen script, then run:

    bash GMT-20-script-JC-ETOPO1-MT.sh

The script writes a PostScript file and converts it to a raster image (JPG/PNG) via psconvert.

## Author and citation

Polina Lemenkova
ORCID: https://orcid.org/0000-0002-5759-1089

These scripts support figures in the author's marine-geomorphological and cartographic papers; please cite the specific article a given figure appears in. The full publication list is available via the ORCID record above.

## License

See the LICENSE file in this repository.
