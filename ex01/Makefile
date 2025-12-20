# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: juhyeonl <juhyeonl@student.42.fr>          +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2025/10/08 15:35:12 by JuHyeon           #+#    #+#              #
#    Updated: 2025/10/09 14:01:45 by juhyeonl         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

NAME = zombieHorde

CC		= c++
FLAGS	= -Wall -Wextra -Werror -std=c++98 -Iinclude

SRC_DIR	= ./src
OBJ_DIR	= ./obj

SRCS = $(SRC_DIR)/main.cpp \
		$(SRC_DIR)/zombieHorde.cpp \
		$(SRC_DIR)/Zombie.cpp
		
OBJ = $(SRCS:$(SRC_DIR)%=$(OBJ_DIR)/%)
OBJ := $(OBJ:.cpp=.o)

all: $(NAME)

$(NAME): $(OBJ)
	@echo "Compiling $(NAME)..."
	@$(CC) $(FLAGS) $(OBJ) -o $(NAME)
	@echo "Done"

$(OBJ_DIR)/%.o: $(SRC_DIR)/%.cpp
	@mkdir -p $(@D)
	@$(CC) $(FLAGS) -c $< -o $@

clean:
	@rm -rf $(OBJ_DIR)
	@echo "Cleaned up all object files"

fclean: clean
	@rm -f $(NAME)
	@echo "Cleaned up $(NAME)"

re: fclean all
	@echo "Remade everything"

.PHONY: all clean fclean re