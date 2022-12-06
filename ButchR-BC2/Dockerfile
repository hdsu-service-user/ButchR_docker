FROM hdsu/butchr

LABEL maintainer="Andres Quintero andres.quintero@bioquant.uni-heidelberg.de"





RUN R -e "install.packages('Seurat')"
#
# install.packages('Seurat')
#
#
RUN apt-get update && apt-get install -y \
      libglpk-dev


RUN R -e "install.packages(c('msigdbr', 'ggupset', 'umap'))"
RUN R -e "BiocManager::install('clusterProfiler', update = FALSE)"
# RUN R -e "BiocManager::install('BiocStyle', update = FALSE)"
#
#
#
# RUN useradd -ms /bin/bash hdsu
#
COPY --chown=hdsu data/assignment_01 /home/hdsu/assignment_01
COPY --chown=hdsu data/assignment_02 /home/hdsu/assignment_02
COPY --chown=hdsu data/assignment_03 /home/hdsu/assignment_03
COPY --chown=hdsu data/assignment_04 /home/hdsu/assignment_04

#
# COPY --chown=hdsu /ButchR/user-settings /home/hdsu/.rstudio/monitored/user-settings/user-settings
# COPY --chown=hdsu /ButchR/Rprofile /home/hdsu/.Rprofile
# COPY /ButchR/user-settings /home/rstudio/.rstudio/monitored/user-settings/user-settings
# COPY /ButchR/Rprofile /home/rstudio/.Rprofile
#
# COPY --chown=hdsu data /home/hdsu/Corces_NMF/data
# COPY --chown=hdsu src /home/hdsu/Corces_NMF/src
# COPY --chown=hdsu db /home/hdsu/Corces_NMF/db
# COPY --chown=hdsu user-settings /home/hdsu/.rstudio/monitored/user-settings/user-settings
# COPY --chown=hdsu .Rprofile /home/hdsu/.Rprofile
# COPY .Rprofile /home/rstudio/.Rprofile
# COPY user-settings /home/rstudio/.rstudio/monitored/user-settings/user-settings


