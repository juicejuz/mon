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

# Alert Rules Node HDD Usage
<[back](./prom)

### HDD Usage & Fill
- alert: 
    > node_hdd_usage_70%
    - trigger
        > gt: 70%

        > for: 120 min

    - serevity: 
        > indeterminate (purple)
    - summary
        > Swarm node {{ node_name }} disk usage is at {{ value %}}.
    - description
        > Disk alert for Swarm node {{ node_name }}


- alert: 
    > node_hdd_usage_75%
    - trigger
        > gt: 75%

        > for: 60 min

    - serevity:
        > warning (blue)
    - summary
        > Swarm node {{ node_name }} disk usage is at {{ value %}}.
    - description
        > Disk alert for Swarm node {{ node_name }}

- alert: 
    > node_hdd_usage_85%
    - trigger
        > gt: 85%

        > for: 45 min

    - serevity:
        > minor (yellow)
    - summary
        > Swarm node {{ node_name }} disk usage is at {{ value %}}.
    - description
        > Disk alert for Swarm node {{ node_name }}

- alert: 
    > node_hdd_usage_90%
    - trigger
        > gt: 90%

        > for: 30 min

    - serevity:
        > major (orange)
    - summary
        > Swarm node {{ node_name }} disk usage is at {{ value %}}.
    - description
        > Disk alert for Swarm node {{ node_name }}

- alert: 
    > node_hdd_usage_95%
    - trigger
        > gt: 95

        > for: 1 min

    - serevity:
        > critical (red)
    - summary
        > Swarm node {{ node_name }} disk usage is at {{ value %}}.
    - description
        > Disk alert for Swarm node {{ node_name }}

- alert: 
    > node_hdd_fill_rate_6h
    - trigger
        > full: in 6h
        
        > for: 60 min
        
    - serevity:
        > critical (red)
    - summary
        > Swarm node {{ node_name }} disk is going to fill up in 6h.
    - description
        > Disk fill alert for Swarm node {{ node_name }}

## License

![LICENCE](https://img.shields.io/github/license/davedb459/davedb-api)

- **[Apache2.0 license](http://www.apache.org/licenses/LICENSE-2.0)**
- Copyright 2020 © <a href="https://github.com/davedb459/davedb.api.git" target="_blank">dave-db.com</a>.