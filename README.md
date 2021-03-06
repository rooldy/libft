# Libft
My own library of useful functions in C.

# Summary
 1. [Makefile](#makefile)
 2. [Function list](#function-list)
 3. [Details](#details)

# <a name="makefile">Makefile</a>

| Commande       	|  Actions 	|
|----------------	|----------	|
| `make`      	  | Compile les .c et créer libft.a  	|
| `make clean`    | Supprime les .o.  	|
| `make flcean`  	| Supprime les .o et libft.a.  	|
| `make re`     	| Exécute fclean et make.  	|

# <a name="function-list">Function list</a>

- memset  [(voir man)](http://linux.die.net/man/3/memset)
- bzero   [(voir man)](http://linux.die.net/man/3/bzero)
- memcpy  [(voir man)](http://linux.die.net/man/3/memcpy)
- memccpy [(voir man)](http://linux.die.net/man/3/memccpy)
- memmove [(voir man)](http://linux.die.net/man/3/memmove)
- [memalloc] (#ft_memalloc)
- [memdel] (#ft_memdel)
- memchr  [(voir man)](http://linux.die.net/man/3/memchr)
- memcmp  [(voir man)](http://linux.die.net/man/3/memcmp)
- [strdel] (#ft_strdel)
- strlen  [(voir man)](http://linux.die.net/man/3/strlen)
- strdup  [(voir man)](http://linux.die.net/man/3/strdup)
- [strclr] (#ft_strclr)
- strcpy  [(voir man)](http://linux.die.net/man/3/strcpy)
- strncpy [(voir man)](http://linux.die.net/man/3/strncpy)
- strcat  [(voir man)](http://linux.die.net/man/3/strcat)
- strncat [(voir man)](http://linux.die.net/man/3/strncat)
- strlcat [(voir man)](http://linux.die.net/man/3/strlcat)
- [strnew] (#ft_strnew)
- strchr  [(voir man)](http://linux.die.net/man/3/strchr)
- strrchr [(voir man)](http://linux.die.net/man/3/strrchr)
- [striter] (#ft_striter)
- [striteri] (#ft_striteri)
- strstr  [(voir man)](http://linux.die.net/man/3/strstr)
- strnstr [(voir man)](http://www.freebsd.org/cgi/man.cgi?query=strnstr&sektion=3)
- strcmp  [(voir man)](http://linux.die.net/man/3/strcmp)
- strncmp [(voir man)](http://linux.die.net/man/3/strncmp)
- [strmap] (#ft_strmap)
- [strmapi] (#ft_strmapi)
- [strnequ] (#ft_strnequ)
- [strsub] (#ft_strsub)
- [strjoin] (#ft_strjoin)
- [strtrim] (#ft_strtrim)
- [strsplit] (#ft_strsplit)
- [itoa] (#ft_itoa)
- atoi    [(voir man)](http://linux.die.net/man/3/atoi)
- [putchar] (#ft_putchar)
- [putchar_fd] (#ft_putchar_fd)
- [putstr] (#ft_putstr)
- [putstr_fd] (#ft_putstr_fd)
- [putendl] (#ft_putendl)
- [putendl_fd] (#ft_putendl_fd)
- [putnbr] (#ft_putnbr)
- [putnbr_fd] (#ft_putnbr_fd)
- isalpha [(voir man)](http://linux.die.net/man/3/isalpha)
- isdigit [(voir man)](http://linux.die.net/man/3/isdigit)
- isalnum [(voir man)](http://linux.die.net/man/3/isalnum)
- isascii [(voir man)](http://linux.die.net/man/3/isascii)
- isprint [(voir man)](http://linux.die.net/man/3/isprint)
- toupper [(voir man)](http://linux.die.net/man/3/toupper)
- tolower [(voir man)](http://linux.die.net/man/3/tolower)
- [lstnew] (#ft_lstnew)
- [lstdelone] (#ft_lstdelone)
- [lstdel] (#ft_lstdel)
- [lstadd] (#ft_lstadd)
- [lstiter] (#ft_lstiter)
- [ft_lstmap] (#ft_lstmap)


# <a name="details">Details<a/>


| Function       	|  <a name="ft_memalloc">ft_memalloc</a> 	|
|----------------	|---------------------------------------	|
| Prototype      	| void * ft_memalloc(size_t size);  	|
| Description    	| Alloue (avec malloc(3)) et retourne une zone de mémoire “fraiche”. La mémoire allouée est initialisée à 0. Si l’allocation échoue, la fonction renvoie NULL.  	|
| Param. #1      	|  La taille de la zone de mémoire à allouer.  	|
| Retour         	| La zone de mémoire allouée.  	|
| Fonctions libc 	| malloc(3) 	|

----------

| Function       	|  <a name="ft_memdel">ft_memdel</a> 	|
|----------------	|-----------------------------------	|
| Prototype      	| void ft_memdel(void **ap);  	|
| Description    	| Prend en paramètre l’adresse d’un pointeur dont la zone pointée doit être libérée avec free(3), puis le pointeur est mis à NULL.  	|
| Param. #1      	|  L’adresse d’un pointeur dont il faut libérer la mémoire puis le mettre à NULL.  	|
| Retour         	| Rien.  	|
| Fonctions libc 	| free(3) 	|

----------

| Function       	|  <a name="ft_strnew">ft_strnew</a> 	|
|----------------	|-----------------------------------	|
| Prototype      	| char * ft_strnew(size_t size);  	|
| Description    	| Alloue (avec malloc(3)) et retourne une chaine de caractère “fraiche” terminée par un ’\0’. Chaque caractère de la chaine est initialisé à ’\0’. Si l’allocation echoue, la fonction renvoie NULL.  	|
| Param. #1      	|  La taille de la chaine de caractères à allouer.  	|
| Retour         	| La chaine de caractères allouée et initialisée à 0.  	|
| Fonctions libc 	| malloc(3) 	|

----------

| Function       	|   <a name="ft_strdel">ft_strdel</a> 	|
|----------------	|-------------------------------------	|
| Prototype      	| void ft_strdel(char **as);  	|
| Description    	| Prend en paramètre l’adresse d’une chaine de caractères qui doit être libérée avec free(3) et son pointeur mis à NULL.  	|
| Param. #1      	|  L’adresse de la chaine de caractère dont il faut libérer la mémoire et mettre le pointeur à NULL.  	|
| Retour         	| Rien.  	|
| Fonctions libc 	| free(3) 	|

----------

| Function       	|  <a name="ft_strclr">ft_strclr</a> 	|
|----------------	|-----------	|
| Prototype      	| void ft_strclr(char *s);  |
| Description    	| Assigne la valeur ’\0’ à tous les caractères de la chaine passée en paramètre.  |
| Param. #1      	| La chaine de caractères à clearer.  |
| Retour         	| Rien.	|
| Fonctions libc 	| Aucune	|

----------

| Function       	|  <a name="ft_striter">ft_striter</a> 	|
|----------------	|-------------------------------------	|
| Prototype      	| void ft_striter(char *s, void (*f)(char *));  |
| Description    	| Applique la fonction f à chaque caractère de la chaine de caractères passée en paramètre. Chaque caractère est passé par adresse à la fonction f afin de pouvoir être modifié si nécéssaire.  |
| Param. #1      	| La chaine de caractères sur laquelle itérer.  |
| Param. #2      	| La fonction à appeler sur chaque caractère de s.  |
| Retour         	| Rien.	|
| Fonctions libc 	| Aucune	|

----------

| Function       	|  <a name="ft_striteri">ft_striteri</a> 	|
|----------------	|---------------------------------------	|
| Prototype      	| void ft_striteri(char *s, void (*f)(unsigned int, char *));  |
| Description    	| Applique la fonction f à chaque caractère de la chaine de caractères passée en paramètre en précisant son index en premier argument. Chaque caractère est passé par adresse à la fonction f afin de pouvoir être modifié si nécéssaire.  |
| Param. #1      	| La chaine de caractères sur laquelle itérer.  |
| Param. #2      	| La fonction à appeler sur chaque caractère de s et son index.  |
| Retour         	| Rien.	|
| Fonctions libc 	| Aucune	|

----------

| Function       	|  <a name="ft_strmap">ft_strmap</a> 	|
|----------------	|---------------------------------------	|
| Prototype      	| char * ft_strmap(char const *s, char (*f)(char));  |
| Description    	| Applique la fonction f à chaque caractère de la chaine de caractères passée en paramètre pour créer une nouvelle chaine “fraiche” (avec malloc(3)) résultant des applications successives de f.  |
| Param. #1      	| La chaine de caractères sur laquelle itérer.  |
| Param. #2      	| La fonction à appeler sur chaque caractère de s.  |
| Retour         	| La chaine “fraiche” résultant des applications successives de f.	|
| Fonctions libc 	| malloc(3)	|

----------

| Function       	|  <a name="ft_strmapi">ft_strmapi</a> 	|
|----------------	|---------------------------------------	|
| Prototype      	| char * ft_strmapi(char const *s, char (*f)(unsigned int, char));  |
| Description    	| Applique la fonction f à chaque caractère de la chaine de caractères passée en paramètre en précisant son index pour créer une nouvelle chaine “fraiche” (avec malloc(3)) résultant des applications successives de f.  |
| Param. #1      	| La chaine de caractères sur laquelle itérer.  |
| Param. #2      	| La fonction à appeler sur chaque caractère de s en précisant son index.  |
| Retour         	| La chaine “fraiche” résultant des applications successives de f.	|
| Fonctions libc 	| malloc(3)	|

----------

| Function       	|  <a name="ft_strnequ">ft_strnequ</a> 	|
|----------------	|---------------------------------------	|
| Prototype      	| int ft_strnequ(char const *s1, char const *s2, size_t n);  |
| Description    	| Compare lexicographiquement s1 et s2 jusqu’à n caractères maximum ou bien qu’un ’\0’ ait été rencontré. Si les deux chaines sont égales, la fonction retourne 1, ou 0 sinon.  |
| Param. #1      	|  La première des deux chaines à comparer.  |
| Param. #2      	|  La seconde des deux chaines à comparer.  |
| Param. #3      	| Le nombre de caractères à comparer au maximum.  |
| Retour         	| 1 ou 0 selon que les deux chaines sont égales ou non. |
| Fonctions libc 	| Aucune.	|

----------

| Function       	|  <a name="ft_strsub">ft_strsub</a> 	|
|----------------	|---------------------------------------	|
| Prototype      	| char * ft_strsub(char const *s, unsigned int start, size_t len); |
| Description    	| Alloue (avec malloc(3)) et retourne la copie “fraiche” d’un tronçon de la chaine de caractères passée en paramètre. Le tronçon commence à l’index start et à pour longueur len. Si start et len ne désignent pas un tronçon de chaine valide, le comportement est indéterminé. Si l’allocation échoue, la fonction renvoie NULL. |
| Param. #1      	| La chaine de caractères dans laquelle chercher le tronçon à copier. |
| Param. #2      	| L’index dans la chaine de caractères où débute le tronçon à copier. |
| Param. #3      	| La longueur du tronçon à copier. |
| Retour         	| Le tronçon. |
| Fonctions libc 	| malloc(3)	|

----------

| Function       	|  <a name="ft_strjoin">ft_strjoin</a> 	|
|----------------	|---------------------------------------	|
| Prototype      	| char * ft_strjoin(char const *s1, char const *s2); |
| Description    	| Alloue (avec malloc(3)) et retourne une chaine de caractères “fraiche” terminée par un ’\0’ résultant de la concaténation de s1 et s2. Si l’allocation echoue, la fonction renvoie NULL. |
| Param. #1      	| La chaine de caractères préfixe. |
| Param. #2      	| La chaine de caractères suffixe. |
| Retour         	| La chaine de caractère “fraiche” résultant de la concaténation des deux chaines. |
| Fonctions libc 	| malloc(3)	|

----------

| Function       	|  <a name="ft_strtrim">ft_strtrim</a> 	|
|----------------	|---------------------------------------	|
| Prototype      	| char * ft_strtrim(char const *s); |
| Description    	| Alloue (avec malloc(3)) et retourne une copie de la chaine passée en paramètre sans les espaces blancs au debut et à la fin de cette chaine. On considère comme espaces blancs les caractères ’ ’, ’\n’ et ’\t’. Si s ne contient pas d’espaces blancs au début ou à la fin, la fonction renvoie une copie de s. Si l’allocation echoue, la fonction renvoie NULL. |
| Param. #1      	| La chaine de caractères à trimmer. |
| Retour         	| La chaine de caractère “fraiche” trimmée ou bien une copie de s sinon. |
| Fonctions libc 	| malloc(3)	|

----------

| Function       	|  <a name="ft_strsplit">ft_strsplit</a> 	|
|----------------	|---------------------------------------	|
| Prototype      	| char ** ft_strsplit(char const *s, char c); |
| Description    	| Alloue (avec malloc(3)) et retourne un tableau de chaines de caractères “fraiches” (toutes terminées par un ’\0’, le tableau également donc) résultant de la découpe de s selon le caractère c. Si l’allocation echoue, la fonction retourne NULL. Exemple : ft_strsplit("*salut*les***etudiants*", ’*’) renvoie le tableau ["salut", "les", "etudiants"]. |
| Param. #1      	| La chaine de caractères à découper. |
| Param. #2      	| Le caractère selon lequel découper la chaine. |
| Retour         	| Le tableau de chaines de caractères “fraiches” résultant de la découpe. |
| Fonctions libc 	| malloc(3), free(3)	|

----------

| Function       	|  <a name="ft_itoa">ft_itoa</a> 	|
|----------------	|---------------------------------------	|
| Prototype      	| char * ft_itoa(int n); |
| Description    	| Alloue (avec malloc(3)) et retourne une chaine de caractères “fraiche” terminée par un ’\0’ représentant l’entier n passé en paramètre. Les nombres négatifs doivent être gérés. Si l’allocation échoue, la fonction renvoie NULL. |
| Param. #1      	| L’entier à convertir en une chaine de caractères. |
| Retour         	| La chaine de caractères représentant l’entier passé en paramètre. |
| Fonctions libc 	| malloc(3)	|

----------

| Function       	|  <a name="ft_putchar">ft_putchar</a> 	|
|----------------	|---------------------------------------	|
| Prototype      	| void ft_putchar(char c); |
| Description    	| Affiche le caractère c sur la sortie standard. |
| Param. #1      	| Le caractères à afficher. |
| Retour         	| Rien. |
| Fonctions libc 	| write(2)	|

----------

| Function       	|  <a name="ft_putstr">ft_putstr</a> 	|
|----------------	|---------------------------------------	|
| Prototype      	| void ft_putstr(char const *s); |
| Description    	| Affiche la chaine s sur la sortie standard. |
| Param. #1      	| La chaine de caractères à afficher. |
| Retour         	| Rien. |
| Fonctions libc 	| write(2)	|

----------

| Function       	|  <a name="ft_putendl">ft_putendl</a> 	|
|----------------	|---------------------------------------	|
| Prototype      	| void ft_putendl(char const *s); |
| Description    	| Affiche la chaine s sur la sortie standard suivi d’un ’\n’. |
| Param. #1      	| La chaine de caractères à afficher. |
| Retour         	| Rien. |
| Fonctions libc 	| write(2)	|

----------

| Function       	|  <a name="ft_putnbr">ft_putnbr</a> 	|
|----------------	|---------------------------------------	|
| Prototype      	| void ft_putnbr(int n); |
| Description    	| Affiche l’entier n sur la sortie standard. |
| Param. #1      	| L’entier à afficher. |
| Retour         	| Rien. |
| Fonctions libc 	| write(2)	|

----------

| Function       	|  <a name="ft_putchar_fd">ft_putchar_fd</a> 	|
|----------------	|---------------------------------------	|
| Prototype      	| void ft_putchar_fd(char c, int fd); |
| Description    	| Ecrit le caractère c sur le descripteur de fichier fd. |
| Param. #1      	| Le caractères à écrire. |
| Retour         	| Rien. |
| Fonctions libc 	| write(2)	|

----------

| Function       	|  <a name="ft_putstr_fd">ft_putstr_fd</a> 	|
|----------------	|---------------------------------------	|
| Prototype      	| void ft_putstr_fd(char const *s, int fd); |
| Description    	| Ecrit la chaine s sur le descripteur de fichier fd. |
| Param. #1      	| La chaine de caractères à écrire. |
| Retour         	| Rien. |
| Fonctions libc 	| write(2)	|

----------

| Function       	|  <a name="ft_putendl_fd">ft_putendl_fd</a> 	|
|----------------	|---------------------------------------	|
| Prototype      	| void ft_putendl_fd(char const *s, int fd); |
| Description    	| Ecrit la chaine s sur le descripteur de fichier fd suivi d’un ’\n’. |
| Param. #1      	| La chaine de caractères à écrire. |
| Retour         	| Rien. |
| Fonctions libc 	| write(2)	|

----------

| Function       	|  <a name="ft_putnbr_fd">ft_putnbr_fd</a> 	|
|----------------	|---------------------------------------	|
| Prototype      	| void ft_putnbr_fd(int n, int fd); |
| Description    	| Ecrit l’entier n sur le descripteur de fichier fd. |
| Param. #1      	| L’entier à écrire. |
| Retour         	| Rien. |
| Fonctions libc 	| write(2)	|

----------

| Function       	|  <a name="ft_lstnew">ft_lstnew</a> 	|
|----------------	|---------------------------------------	|
| Prototype      	| t_list * ft_lstnew(void const *content, size_t content_size); |
| Description    	| Alloue (avec malloc(3)) et retourne un maillon “frais”. Les champs content et content_size du nouveau maillon sont initialisés par copie des paramètres de la fonction. Si le paramètre content est nul, le champs content est initialisé à NULL et le champs content_size est initialisé à 0 quelque soit la valeur du paramètre content_size. Le champ next est initialisé à NULL. Si l’allocation échoue, la fonction renvoie NULL. |
| Param. #1      	| Le contenu à ajouter au nouveau maillon. |
| Param. #2      	| La taille du contenu à ajouter au nouveau maillon. |
| Retour         	| Le nouveau maillon. |
| Fonctions libc 	| malloc(3), free(3)	|

----------

| Function       	|  <a name="ft_lstdelone">ft_lstdelone</a> 	|
|----------------	|---------------------------------------	|
| Prototype      	| void ft_lstdelone(t_list **alst, void (*del)(void *, size_t)); |
| Description    	| Prend en paramètre l’adresse d’un pointeur sur un maillon et libère la mémoire du contenu de ce maillon avec la fonction del passée en paramètre puis libère la mémoire du maillon en lui même avec free(3). La mémoire du champ next ne doit en aucun cas être libérée. Pour terminer, le pointeur sur le maillon maintenant libéré doit être mis à NULL (de manière similaire à la fonction ft_memdel de la partie obligatoire). |
| Param. #1      	| L’adresse d’un pointeur sur le maillon à libérer. |
| Retour         	| Rien. |
| Fonctions libc 	| free(3)	|

----------

| Function       	|  <a name="ft_lstdel">ft_lstdel</a> 	|
|----------------	|---------------------------------------	|
| Prototype      	| void ft_lstdel(t_list **alst, void (*del)(void *, size_t)); |
| Description    	| Prend en paramètre l’adresse d’un pointeur sur un maillon et libère la mémoire de ce maillon et celle de tous ses successeurs l’un après l’autre avec del et free(3). Pour terminer, le pointeur sur le premier maillon maintenant libéré doit être mis à NULL (de manière similaire à la fonction ft_memdel de la partie obligatoire). |
| Param. #1      	| L’adresse d’un pointeur sur le premier maillon d’une liste à libérer. |
| Retour         	| Rien. |
| Fonctions libc 	| free(3)	|

----------

| Function       	|  <a name="ft_lstadd">ft_lstadd</a> 	|
|----------------	|---------------------------------------	|
| Prototype      	| void ft_lstadd(t_list **alst, t_list *new); |
| Description    	| Ajoute l’élément new en tête de la liste. |
| Param. #1      	| L’adresse d’un pointeur sur le premier maillon d’une liste. |
| Param. #2      	| Le maillon à ajouter en tête de cette liste. |
| Retour         	| Rien. |
| Fonctions libc 	| Aucune.  |

----------

| Function       	|  <a name="ft_lstiter">ft_lstiter</a> 	|
|----------------	|---------------------------------------	|
| Prototype      	| void ft_lstiter(t_list *lst, void (*f)(t_list *elem)); |
| Description    	| Parcourt la liste lst en appliquant à chaque maillon la fonction f. |
| Param. #1      	| Pointeur sur le premier maillon d’une liste. |
| Param. #2      	| L’adresse d’une fonction à laquelle appliquer chaque maillon de la liste. |
| Retour         	| Rien. |
| Fonctions libc 	| Aucune.  |

----------

| Function       	|  <a name="ft_lstmap">ft_lstmap</a> 	|
|----------------	|---------------------------------------	|
| Prototype      	| t_list * ft_lstmap(t_list *lst, t_list * (*f)(t_list *elem)); |
| Description    	| Parcourt la liste lst en appliquant à chaque maillon la fonction f et crée une nouvelle liste “fraiche” avec malloc(3) résultant des applications successives. Si une allocation échoue, la fonction renvoie NULL. |
| Param. #1      	| Pointeur sur le premier maillon d’une liste. |
| Param. #2      	| L’adresse d’une fonction à appliquer à chaque maillon de la liste pour crér une nouvelle liste. |
| Retour         	| La nouvelle liste. |
| Fonctions libc 	| malloc(3), free(3).  |
