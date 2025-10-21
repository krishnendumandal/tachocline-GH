Frequency splittings of acoustic modes derived from the HMI, MDI, and GONG instruments are available at the following link:
https://lweb.cfa.harvard.edu/~sylvain/research/tables/

The inversion results are available in the following GitHub repository:
🔗 https://github.com/krishnendumandal/tachocline-GH

Each dataset in the compressed repository is stored as a NumPy .npz file with the filename format:
wst_smooth_nb_GONG_4x72d_s_1stD_<s>.npz,
where <s> corresponds to the harmonic degree, s.

These files can be loaded in Python using the following commands:

import numpy as np

load_file = np.load(prefix + str(s) + '.npz')

r = load_file['r']
wst = load_file['wst']
wst_std = load_file['wst_std']


Here,

    r represents the radial grid,

    wst is the inversion result, and

    wst_std is the corresponding uncertainty (standard deviation) of the inversion.
