# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: mhammerc <mhammerc@student.42.fr>          +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2017/01/04 12:32:53 by mhammerc          #+#    #+#              #
#    Updated: 2017/01/06 14:42:03 by mhammerc         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

NAME = libme.so

SRCS = me_add_state.c \
	   me_animator_give_velocity.c \
	   me_create_main_window.c \
	   me_die.c \
	   me_exit_game.c \
	   me_get_state.c \
	   me_get_texture_data.c \
	   me_get_texture_for_animation.c \
	   me_get_texture_information.c \
	   me_init.c \
	   me_is_key_pressed.c \
	   me_key_press.c \
	   me_key_release.c \
	   me_load_map.c \
	   me_load_map01.c \
	   me_load_map2.c \
	   me_load_texture.c \
	   me_mouse_move.c \
	   me_process_animation.c \
	   me_process_animator.c \
	   me_raycaster_move.c \
	   me_raycaster_render.c \
	   me_raycaster_thing1.c \
	   me_raycaster_update.c \
	   me_raycaster_wall_loop1.c \
	   me_raycaster_wall_loop2.c \
	   me_run_game_loop.c \
	   me_run_game_loop2.c \
	   me_thing_combsort.c

OBJS = $(SRCS:.c=.o)

LIBFT_PATH = libft
MLX_PATH =

CFLAGS = -Wall -Werror -Wextra -O3 -Ilibft
LFLAGS = -lmlx -lpthread -lm -L$(LIBFT_PATH) -lft -lbsd

UNAME := $(shell uname)

ifeq ($(UNAME),Darwin)
	MLX_PATH += minilibx_macos
	LFLAGS += -Lminilibx_macos -framework AppKit -framework OpenGL
	CFLAGS += -Iminilibx_macos
endif

ifeq ($(UNAME),Linux)
	MLX_PATH += minilibx_linux
	LFLAGS += -Lminilibx_linux -lX11 -lXext
	CFLAGS += -Iminilibx_linux
endif

all: $(NAME)

$(NAME): $(OBJS)
	make -C $(LIBFT_PATH)
	-make -C $(MLX_PATH)
	gcc -shared -o $(NAME) $(OBJS) $(LFLAGS)

clean:
	make -C $(LIBFT_PATH) clean
	make -C $(MLX_PATH) clean
	rm -rf $(OBJS)

fclean: clean
	make -C $(LIBFT_PATH) fclean
	rm -rf $(NAME)

re: fclean all

