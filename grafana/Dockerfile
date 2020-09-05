##
# Copyright 2020 [SM-4.0 TV] @Vodafone.de & @OpenAdvice
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#    http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
##

##
# * --------------------------------------------------------------------------------
# * Description:
# *        ToDo:
# * --------------------------------------------------------------------------------
##

FROM grafana/grafana:7.1.5
# https://hub.docker.com/r/grafana/grafana/tags/

COPY datasources /etc/grafana/provisioning/datasources/
COPY ddb_dashboards.yml /etc/grafana/provisioning/dashboards/
COPY dashboards /etc/grafana/dashboards/

ENV GF_SECURITY_ADMIN_PASSWORD=admin \
    GF_SECURITY_ADMIN_USER=Start01!@ \
    GF_PATHS_PROVISIONING=/etc/grafana/provisioning/