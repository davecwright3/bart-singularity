[![https://www.singularity-hub.org/static/img/hosted-singularity--hub-%23e32929.svg](https://www.singularity-hub.org/static/img/hosted-singularity--hub-%23e32929.svg)](https://singularity-hub.org/collections/4946)

# BART Singularity Guide
 The singularity image has BART installed at `/bart_dir`. The `$topdir` environment variable is set to this directory inside the image. This means that the instructions here https://github.com/exosports/BART/tree/master/examples/demo still work, but we need to mount a directory for outputs into the container because the container is read-only. The image has a directory for this purpose at ~/bart_dir/run~. Make a directory on your host system where you want to store results. For the sake of this guide, let's say it's at `$pwd/demo/run` and you have the singularity image at `pwd`. Then start a shell in the singularity container with the bind mount specified: `singularity shell -B demo/run:/bart_dir/run bart.img`. Now just `cd $topdir/run` and follow the instructions here https://github.com/exosports/BART/tree/master/examples/demo.

# License
Bayesian Atmospheric Radiative Transfer (BART), a code to infer
properties of planetary atmospheres based on observed spectroscopic
information.

This project was completed with the support of the NASA Planetary
Atmospheres Program, grant NNX12AI69G, held by Principal Investigator
Joseph Harrington. Principal developers included graduate students
Patricio E. Cubillos and Jasmina Blecic, programmer Madison Stemm, and
undergraduates M. Oliver Bowman and Andrew S. D. Foster.  The included
'transit' radiative transfer code is based on an earlier program of
the same name written by Patricio Rojo (Univ. de Chile, Santiago) when
he was a graduate student at Cornell University under Joseph
Harrington.  Statistical advice came from Thomas J. Loredo and Nate
B. Lust.

Copyright (C) 2015-2016 University of Central Florida.
All rights reserved.

This is a test version only, and may not be redistributed to any third
party.  Please refer such requests to us.  This program is distributed
in the hope that it will be useful, but WITHOUT ANY WARRANTY; without
even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR
PURPOSE.

Our intent is to release this software under an open-source,
reproducible-research license, once the code is mature and the first
research paper describing the code has been accepted for publication
in a peer-reviewed journal.  We are committed to development in the
open, and have posted this code on github.com so that others can test
it and give us feedback.  However, until its first publication and
first stable release, we do not permit others to redistribute the code
in either original or modified form, nor to publish work based in
whole or in part on the output of this code.  By downloading, running,
or modifying this code, you agree to these conditions.  We do
encourage sharing any modifications with us and discussing them
openly.

We welcome your feedback, but do not guarantee support.  Please send
feedback or inquiries to:
Patricio Cubillos <patricio.cubillos@oeaw.ac.at>
Jasmina Blecic <jasmina@physics.ucf.edu>
Joseph Harrington <jh@physics.ucf.edu>

or alternatively,
Joseph Harrington, Patricio Cubillos, and Jasmina Blecic
UCF PSB 441
4111 Libra Drive
Orlando, FL 32816-2385
USA

Thank you for testing BART!