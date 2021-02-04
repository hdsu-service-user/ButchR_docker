FROM hdsu/r_tensorflow2

LABEL maintainer="Andres Quintero andres.quintero@bioquant.uni-heidelberg.de"


#RUN R -e "devtools::install_github( 'hdsu-bioquant/ButchR')"
RUN R -e "devtools::install_github( 'wurst-theke/ButchR' )"
    
RUN R -e "BiocManager::install('DESeq2', update = FALSE)"
RUN R -e "BiocManager::install('gage', update = FALSE)"
RUN R -e "install.packages('DT')"
RUN R -e "install.packages('viridis')"
RUN R -e "BiocManager::install('ComplexHeatmap', update = FALSE)"


RUN useradd -ms /bin/bash hdsu

COPY --chown=hdsu /ButchR/data /home/hdsu/Corces_NMF/data
COPY --chown=hdsu /ButchR/src /home/hdsu/Corces_NMF/src
COPY --chown=hdsu /ButchR/db /home/hdsu/Corces_NMF/db

COPY --chown=hdsu /ButchR/user-settings /home/hdsu/.rstudio/monitored/user-settings/user-settings
COPY --chown=hdsu /ButchR/Rprofile /home/hdsu/.Rprofile
COPY /ButchR/user-settings /home/rstudio/.rstudio/monitored/user-settings/user-settings
COPY /ButchR/Rprofile /home/rstudio/.Rprofile

# COPY --chown=hdsu data /home/hdsu/Corces_NMF/data
# COPY --chown=hdsu src /home/hdsu/Corces_NMF/src
# COPY --chown=hdsu db /home/hdsu/Corces_NMF/db
# COPY --chown=hdsu user-settings /home/hdsu/.rstudio/monitored/user-settings/user-settings
# COPY --chown=hdsu .Rprofile /home/hdsu/.Rprofile
# COPY .Rprofile /home/rstudio/.Rprofile
# COPY user-settings /home/rstudio/.rstudio/monitored/user-settings/user-settings


