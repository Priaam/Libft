# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: pserre-s <priaserre@gmail.com>             +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2025/11/05 16:51:53 by pserre-s          #+#    #+#              #
#    Updated: 2025/12/03 13:12:29 by pserre-s         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

NAME = libftprintf.a

SRC_DIR = src
INC_DIR = include
OBJ_DIR = objs

SRCS = $(SRC_DIR)/ft_printf.c \
       $(SRC_DIR)/ft_printf_functions.c

OBJS = $(SRCS:$(SRC_DIR)/%.c=$(OBJ_DIR)/%.o)

CC = cc
CFLAGS = -Wall -Wextra -Werror -I$(INC_DIR)
AR = ar rcs
RM = rm -f

# ────────────── Mandatory ────────────── #
all: $(NAME)

$(NAME): $(OBJS)
	$(AR) $(NAME) $(OBJS)

# # ────────────── Bonus ────────────── #
# bonus: $(NAME) $(OBJS_BONUS)
# 	$(AR) $(NAME) $(OBJS) $(OBJS_BONUS)

# ────────────── Compilation objets ────────────── #
$(OBJ_DIR)/%.o: $(SRC_DIR)/%.c | $(OBJ_DIR)
	$(CC) $(CFLAGS) -c $< -o $@

$(OBJ_DIR):
	mkdir -p $(OBJ_DIR)

# ────────────── Nettoyage ────────────── #
clean:
	$(RM) -r $(OBJ_DIR)

fclean: clean
	$(RM) $(NAME)

re: fclean all

.PHONY: all clean fclean re