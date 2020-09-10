<!--
* Copyright 2020 @dave-db.com
*
* Licensed under the Apache License, Version 2.0 (the "License");
* you may not use this file except in compliance with the License.
* You may obtain a copy of the License at
*    http://www.apache.org/licenses/LICENSE-2.0
*
* Unless required by applicable law or agreed to in writing, software
* distributed under the License is distributed on an "AS IS" BASIS,
* WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
* See the License for the specific language governing permissions and
* limitations under the License.
-->

<!--
 * --------------------------------------------------------------------------------
 * Description:
 *        ToDo:
 * --------------------------------------------------------------------------------
 -->

# Alert Rules Taks CPU Usage
<[back](./prom)

### CPU Usage
- alert:
    > task_cpu_usage_50%
    - trigger
        > gt: 50%

        > for: 60m
    - serevity: 
        > indeterminate (purple)
    - summary
        > CPU alert for Swarm task {{ task_name }} on {{ node_name }}
    - description
        > {{ task_name }} on {{ node_name }} CPU usage is at {{ value % }}.
- alert:
    > task_cpu_usage_60%
    - trigger
        > gt: 60%

        > for: 45m
    - serevity: 
        > warning (blue)
    - summary
        > CPU alert for Swarm task {{ task_name }} on {{ node_name }}
    - description
        > {{ task_name }} on {{ node_name }} CPU usage is at {{ value % }}.
- alert:
    > task_cpu_usage_75%
    - trigger
        > gt: 75%

        > for: 30m
    - serevity: 
        > minor (yellow)
    - summary
        > CPU alert for Swarm task {{ task_name }} on {{ node_name }}
    - description
        > {{ task_name }} on {{ node_name }} CPU usage is at {{ value % }}.
- alert:
    > task_cpu_usage_85%
    - trigger
        > gt: 85%

        > for: 15m
    - serevity: 
        > major (orange)
    - summary
        > CPU alert for Swarm task {{ task_name }} on {{ node_name }}
    - description
        > {{ task_name }} on {{ node_name }} CPU usage is at {{ value % }}.
- alert:
    > task_cpu_usage_95%
    - trigger
        > gt: 95%

        > for: 1m
    - serevity: 
        > critical (red)
    - summary
        > CPU alert for Swarm task {{ task_name }} on {{ node_name }}
    - description
        > {{ task_name }} on {{ node_name }} CPU usage is at {{ value % }}.

## License

![LICENCE](https://img.shields.io/github/license/davedb459/davedb-api)

- **[Apache2.0 license](http://www.apache.org/licenses/LICENSE-2.0)**
- Copyright 2020 © <a href="https://github.com/davedb459/davedb.api.git" target="_blank">dave-db.com</a>.