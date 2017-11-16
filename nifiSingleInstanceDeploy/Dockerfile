# Licensed to the Apache Software Foundation (ASF) under one
# or more contributor license agreements. See the NOTICE file
# distributed with this work for additional information
# regarding copyright ownership. The ASF licenses this file
# to you under the Apache License, Version 2.0 (the
# "License"); you may not use this file except in compliance
# with the License. You may obtain a copy of the License at
#
#   http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing,
# software distributed under the License is distributed on an
# "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
# KIND, either express or implied. See the License for the
# specific language governing permissions and limitations
# under the License.
#

FROM apache/nifi:1.4.0
LABEL maintainer hashmap <hashmap@hashmapinc.com>

ENV NIFI_VERSION 1.4.0
ENV NIFI_BASE_DIR /opt/nifi
ENV NIFI_HOME $NIFI_BASE_DIR/nifi-$NIFI_VERSION

USER root
RUN mkdir ${NIFI_HOME}/flow
ADD ./nifi.properties conf
RUN chown -R nifi:nifi $NIFI_HOME/conf/nifi.properties
RUN chown -R nifi:nifi $NIFI_HOME/flow
USER nifi

EXPOSE 8081 8082 9001

ENTRYPOINT ["bin/nifi.sh"]
CMD ["run"]

