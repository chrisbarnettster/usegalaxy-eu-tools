virtualenv .venv -p python3
source .venv/bin/activate
pip install ephemeris
pip install pykwalify

make fix
make lock
make lint
# if needed include custom sections in .schema.yaml e.g. "MD Engine"
make install GALAXY_SERVER=https://galaxy-compchem.ilifu.ac.za GALAXY_API_KEY=""
