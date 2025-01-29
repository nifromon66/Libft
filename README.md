# LIBFT
>
> ## DESCRIPTION
> This project's goal was for us to create in C our own library of generic functions that we could use in our future projects at 42. Coding in C is quite laborious, imagine how hard it would be if we didn't have access to all those small but extremely pratical functions. That's why we must begin our cursus at 42 by creating our own library - Which we will be free to enrich as we go trough the cursus as long as we respect the rules.
>
> ---
> ## INSTRUCTIONS
> - Program name : libft.a ;
> - Files to return : Makefile, libft.h, ft_*.c.
> - Makefile rules : NAME, all, clean, fclean, re.
> - Allowed external functions : See details below.
> - Libft allowed : n/a.
> ---
> - ### Part 1 - Libc functions
>		In this first part, we must recode a group of functions of the "libc" library as described in there respective manual pages. Our functions must have the exact same prototype, the same behavior and the same return values as the originals. The only difference will be that they must be prefixed by "ft_" and will be coded our way.
>	#### Functions :
>	##### Character classification functions :
>	- **ft_isalpha** :
>		- Prototype : `int	ft_isalpha(int c);`
>		- Description : Checks for an alphabetic character.
>		- Allowed external functions : None.
>		- Return Value : The values returned are non-zero if the character falls into the tested class, and zero if not.
>	- **ft_isdigit** :
>		- Prototype : `int	ft_isdigit(int c);`
>		- Description : Checks for a digital character (0 - 9).
>		- Allowed external functions : None.
>		- Return Value : The values returned are non-zero if the character falls into the tested class, and zero if not.
>	- **ft_isalnum** :
>		- Prototype : `int	ft_isalnum(int c);`
>		- Description : Checks for an alphanumeric character.
>		- Allowed external functions : None.
>		- Return Value : The values returned are non-zero if the character falls into the tested class, and zero if not.
>	- **ft_isascii** :
>		- Prototype : `int	ft_isascii(int c);`
>		- Description : Checks whether 'c' is a 7-bit unsigned char value that fits into the ascii table of characters.
>		- Allowed external functions : None.
>		- Return Value : The values returned are non-zero if the character falls into the tested class, and zero if not.
>	- **ft_isprint** :
>		- Prototype : `int	ft_isprint(int c);`
>		- Description : Checks for any printable character.
>		- Allowed external functions : None.
>		- Return Value : The values returned are non-zero if the character falls into the tested class, and zero if not.
>	##### Convertion functions :
>	- **ft_toupper** :
>		- Prototype : `int	ft_toupper(int c);`
>		- Description : It converts a lower_case letter top the corresponding upper_case letter. The argument must be representable as an unsigned char or the value of EOF.
>		- Allowed external functions : None.
>		- Return Value : If the argument is a lower_case letter, the ft_toupper function return the corresponding upper_case letter if there is one, otherwise it returns the given character unchanged.
>	- **ft_tolower** :
>		- Prototype : `int	ft_tolower(int c);`
>		- Description : It converts a upper_case letter top the corresponding lower_case letter. The argument must be representable as an unsigned char or the value of EOF.
>		- Allowed external functions : None.
>		- Return Value : If the argument is a upper_case letter, the ft_tolower function return the corresponding lower_case letter if there is one, otherwise it returns the given character unchanged.
>	- **ft_atoi** :
>		- Prototype : `int	ft_atoi(const char *nptr);`
>		- Description : It converts the initial portion of the string pointed to by nptr to it's int representation (atoi : ascii to int).
>		- Allowed external functions : None.
>		- Return Value : if the string pointed to by 'nptr' contains only digits and that it can fit in a int after convertion then it returns an int corresponding to the given argument.
>	##### String Manipulation functions :
>	- **ft_strlen** :
>		- Prototype : `size_t	ft_strlen(const char *str);`
>		- Description : Calculate the lenght of a string pointed by 'str', excluding the terminating null byte ('\0').
>		- Allowed external functions : None.
>		- Return Value : It returns the number of bytes in the string pointed to by 'str'.
>	- **ft_strlcpy** :
>		- Prototype : `size_t	ft_strlcpy(char *dst, const char *src, size_t size);`
>		- Description : Copy the input string into a destination string. If the destination buffer, limited by it's size isn't large enough to hold the copy, the resulting string is truncated (but is guaranteed to be null terminated).
>		- Allowed external functions : None.
>		- Return Value : It return the lenght of the total string they tried to create.
>	- **ft_strlcat** :
>		- Prototype : `size_t	ft_strlcat(char *dst, const char *src, size_t size);`
>		- Description : Concatenate the input string into a destination string. If the destination buffer, limited by it's size isn't large enough to hold the copy, the resulting string is truncated (but is guaranteed to be null terminated).
>		- Allowed external functions : None.
>		- Return Value : It return the lenght of the total string they tried to create.
>	- **ft_strncmp** :
>		- Prototype : `int	ft_strncmp(const char *s1, const char *s2, size_t n);`
>		- Description : It compare not more than 'n' bytes from the array pointed to by 's1' to the array pointed to by 's2'.
>		- Allowed external functions : None.
>		- Return Value : Upon successfull completion, it shall return an integer greater than, equal to, or less than 0 if the array pointed by 's1' is greater than, equal to, or less than the array pointed to by 's2', it return the value of the first difference he find.
>	- **ft_strnstr** :
>		- Prototype : `char	*ft_strnstr(const char *big, const char *little, size_t len);`
>		- Description : It locate the first occurence of the null-terminated string 'little' in the string 'big', where not more than 'len' characters are searched.
>		- Allowed external functions : None.
>		- Return Value : if little is an empty string, then big is returned. if little occurs nowhere in big, NULL is returned. Otherwise a pointer to the first character of the first occurence of 'little' in 'big' is returned.
>	- **ft_strchr** :
>		- Prototype : `char	*ft_strchr(const char *s, int c);`
>		- Description : It locates the first occurence of c (converted to a char) in the string pointed to by 's'. The terminating null character is considered part of the string; therefore if 'c' is '\0', the functions locate the terminating '\0'.
>		- Allowed external functions : None.
>		- Return Value : It returns a pointer to the located character in the string, or NULL if the character searched is not found in the string.
>	- **ft_strrchr** :
>		- Prototype : `char	*ft_strrchr(const char *s, int c);`
>		- Description : It locates the last occurence of c (converted to a char) in the string pointed to by 's'. The terminating null character is considered part of the string; therefore if 'c' is '\0', the functions locate the terminating '\0'.
>		- Allowed external functions : None.
>		- Return Value : It returns a pointer to the located character in the string, or NULL if the character searched is not found in the string.
>	##### Memory manipulation functions :
>	- **ft_memset** :
>		- Prototype : `void	*ft_memset(void *s, int c, size_t n);`
>		- Description : It fills the first 'n' bytes of memory area pointed to by 's' with the constant byte 'c'.
>		- Allowed external functions : None.
>		- Return Value : it returns a pointer to the memory area of 's'.
>	- **ft_bzero** :
>		- Prototype : void	ft_bzero(void *s, size_t n);`
>		- Description : It erases the data in the 'n' bytes of the memory area startig at the location pointed to by 's', by writing zeros ('\0') to that area.
>		- Allowed external functions : None.
>		- Return Value : None.
>	- **ft_memmove** :
>		- Prototype : `void	*ft_memmove(void *dest, const void *src, size_t n);`
>		- Description : It copies 'n' bytes from memory area 'src' to memory area 'dest'. The memory areas may overlap: copying takes place as though the bytes in src are first copied into a temporary array that does not overlap 'src' or 'dest', and the bytes are then copied from the temporary array to 'dest'.
>		- Allowed external functions : None.
>		- Return Value : It returns a pointer to 'dest'.
>	- **ft_memcpy** :
>		- Prototype : `void	*ft_memcpy(void *dest, const void *src, size_t n);`
>		- Description : It copies 'n' bytes from memory area 'src' to memory area 'dest'. The memory areas must not overlap.
>		- Allowed external functions : None.
>		- Return Value : It returns a pointer to 'dest'.
>	- **ft_memchr** :
>		- Prototype : `void	*ft_memchr(const void *s, int c, size_t n);`
>		- Description : It scans the initial 'n' bytes of memory area pointed to by 's' for the first instance of 'c'. Both 'c' and the bytes of memory area pointed to by 's' are interpreted as unsigned char.
>		- Allowed external functions : None.
>		- Return Value : It returns 
