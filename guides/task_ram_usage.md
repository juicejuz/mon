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

# Alert Rules Taks RAM Usage
<[back](./prom)

### RAM Usage
- alert: 
    > task_memory_usage_1g
    - trigger
        > gt: 1gb

        > for: 60 min
   - serevity: 
        > indeterminate (purple)
    - summary
        > Memory alert for Swarm task {{ task_name }} on {{ node_name }}
    - description
        > {{ task_name }} on {{ node_name }} memory usage is {{ value gb }}.

- alert: 
    > task_memory_usage_2g
    - trigger
        > gt: 2gb

        > for: 45 min
    - serevity: 
        > warning (blue)
    - summary
        > Memory alert for Swarm task {{ task_name }} on {{ node_name }}
    - description
        > {{ task_name }} on {{ node_name }} memory usage is {{ value gb }}.

- alert: 
    > task_memory_usage_3g
    - trigger
        > gt: 3gb

        > for: 30 min
    - serevity: 
        > minor (yellow)
    - summary
        > Memory alert for Swarm task {{ task_name }} on {{ node_name }}
    - description
        > {{ task_name }} on {{ node_name }} memory usage is {{ value gb }}.

- alert: 
    > task_memory_usage_4g
    - trigger
        > gt: 4gb

        > for: 15 min
    - serevity: 
        > major (orange)
    - summary
        > Memory alert for Swarm task {{ task_name }} on {{ node_name }}
    - description
        > {{ task_name }} on {{ node_name }} memory usage is {{ value gb }}.

- alert: 
    > task_memory_usage_5g
    - trigger
        > gt: 5gb

        > for: 1 min
    - serevity:         
        > critical (red)
    - summary
        > Memory alert for Swarm task {{ task_name }} on {{ node_name }}
    - description
        > {{ task_name }} on {{ node_name }} memory usage is {{ value gb }}.

## License

![LICENCE](https://img.shields.io/github/license/davedb459/davedb-api)

- **[Apache2.0 license](http://www.apache.org/licenses/LICENSE-2.0)**
- Copyright 2020 © <a href="https://github.com/davedb459/davedb.api.git" target="_blank">dave-db.com</a>.