# Environment Messages
## State
this message contains 3 property:

- ```agent_type```: Indicates the type of the connected agent whether it is player, coach, or trainer. The value can be ```PlayerT```, ```CoachT```, and ```TrainerT``` that shows. 
- ```world_model```: contains the information of the field environment that the agent recevied from the RCSSServer and parsed by the helios-base. 
- ```full_world_model```: contains the information of the field environment that the agent recevied from the RCSSServer and parsed by the helios-base.  

the difference between ```world_model``` and the ```full_world_model``` is that the ```full_world_model``` contains the information of all the objects in the field, while the ```world_model``` contains the information of the objects that are in the agent's view. Note that the ```world_model``` information is noisy and may not be accurate while the ```full_world_model``` is accurate.

In the defualt config of the RCSSServer, the agent only recieves the ```world_model``` information; however, by changing the config file, the agent can recieve the ```full_world_model``` information too. Although the agent revieves the ```full_world_model``` information, the full state data will be stored in the ```world_model``` property. To recieve both ```world_model``` and ```full_world_model``` information, the agent should change the ```player.conf``` file in the proxy base. 
```
TODO the property of the player.conf for recieving the full_world_model
```

### WorldModel
The ```WorldModel``` type contains the following information:
- ```intercept_table```: Contains the data of the important players that can intercept the ball.In [here](#InterceptTable) we explain more about this data. 
- ```our_team_name```
- ```their_team_name```
- ```our_side```
- ```last_set_play_start_time```
- ```self```
- ```ball```
- ```teammates```
- ```opponents```
- ```unknowns```
- ```our_players_dict```
- ```their_players_dict```
- ```our_goalie_uniform_number```
- ```their_goalie_uniform_number```
- ```offside_line_x```
- ```ofside_line_x_count```
- ```kickable_teammate_id```
- ```kickable_opponent_id```
- ```last_kick_side```
- ```last_kicker_uniform_number```
- ```cycle```
- ```game_mode_type```
- ```left_team_score```
- ```right_team_score```
- ```is_our_set_play```
- ```is_their_set_play```
- ```stoped_cycle```
- ```our_team_score```
- ```their_team_score```
- ```is_penalty_kick_mode```
- ```helios_home_positions```


#### InterceptTable