Ybot campfire transport
========================

This is [campfire](http://campfirenow.com/) transport for [Ybot](https://github.com/0xAX/Ybot) chat robot.

Usage
=========

For using Ybot with campfire, you must to configure it in configuration file ybot.config, something like that:

```erlang
 [
    {ybot,
        [
            % list of transport
            {transports, [
                    % Campfire transport
                    {campfire, % campfire login
                               <<"ybot">>,
                               % campfire token
                               <<"ybot_token">>,
                               % campfire room id
                               100100,
                               % campfire sub-domain
                               <<"home100">>,
                               [{reconnect_timeout, 5000}]
                    }
                ]
            },
            
            % Loading new plugins during work or not
            {checking_new_plugins, false},
            % Checking new plugins timeout
            {checking_new_plugins_timeout, 60000},
            
            % Save commands history
            {commands_history, false},
            % Command history limit
            {history_command_limit_count, 1000},
 
            % plugins directory path
            {plugins_path, "plugins/"}
        ]
    }
].
```

Author
========================

If you have any questions/suggestions, write me at twitter to [0xAX](https://twitter.com/0xAX)