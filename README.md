# cse210-05

Classes:
    *actor
    *cast
    score
    snake/rider
    director
    *action
    control_player1
    control_player2
    draw_actors
    handle_collisions
    *move_actors
    *script
    *keyboard_service
    *video_service
    *color
    *point
    
Need to be edited:
    Santiago: score - look at and modify for displaying two scores

    Ricky: snake/rider - modify to work for a tron style game instead of snake

    Joshua: control_player1 - make sure it modifies one snake and not both

    Joshua: control_player2 - make sure only modifies one snake

    Chris: draw_actors - change inputs to display the snakes properly

    Ricky: handle_collisions - modify to handle collisions between snakes 

    Jacob: __main__ - once every class is updated, needs to have imports updated and actions added

Actor
    attributes
        text
        font_size
        color
        position
        velocity
    methods
        get and set attributes
        move_next

Cast
    attributes
        actors
    methods
        add_actor
        get_actors
        get_all_actors
        get_first_actor
        remove_actor

Score
    attributes
        score
    methods
        set_score

Snake/Rider
    inherits
        actor
    attributes
        segments
    methods
        get_segments
        move_next
        get_head
        grow_tail
        turn_head
        _prepare_body

Director
    attributes
        _video_service
    methods
        start_game
        _execute_actions

Action
    method
        execute

Control_player1
    inherits
        action
    attributes
        _keyboard_service
        _direction
    methods
        execute

Control_player2
    inherits
        action
    attributes
        _keyboard_service
        _direction
    methods
        execute

Draw_actors
    inherits
        action
    attributes
        _video_service
    methods
        execute

Handle_collisions_move_actors
    inherits
        action
    attributes
        is_game_over
    methods
        _handle_segment_collision
        _handle_game_over

Script
    attributes
        actions
    methods
        add_action
        get_action
        remove_action

Keyboard_service
    attributes
        keys
    methods
        is_key_up
        is_key_down

Video_service
    attributes
        debug
    methods
        close_window
        clear_buffer
        draw_actor
        draw_actors
        flush_buffer
        is_window_open
        open_window
        _draw_grid
        _get_x_offset

Color
    attributes
        red
        green
        blue
        alpha
    methods
        to_tuple

Point
    attributes
        x
        y
    methods
        add
        equals
        get_x
        get_y
        reverse
        scale