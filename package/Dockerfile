FROM ubuntu:18.04

ARG kube_bench_tag=v0.0.28
ARG kube_bench_source_code_tag=0.0.28

WORKDIR /
RUN apt-get update && apt-get install -y curl jq
RUN curl -sLf https://github.com/aquasecurity/kube-bench/releases/download/${kube_bench_tag}/kube-bench_${kube_bench_source_code_tag}_linux_amd64.tar.gz | tar -xvzf - -C /usr/bin

COPY package/cfg/ /cfg/
COPY package/run.sh /usr/bin/

CMD ["run.sh"]
