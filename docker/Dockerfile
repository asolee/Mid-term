FROM jupyter/minimal-notebook
RUN pip install biopython
RUN pip install redis
CMD ["tini", "-g", "--", "start-notebook.sh"]
