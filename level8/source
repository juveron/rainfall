#include<stdio.h>
#include<stdlib.h>
#include<string.h>

char *auth
char *service

int 	main()
{
	char	s[128];

	while (1)
	{
		printf("%p, %p\n", auth, service);
		if (fgets(s, 128, stdin) == NULL)
			break;
		if (strncmp(s, "auth ", 5) == 0)
		{
			auth = malloc(4);
			if (strlen(s + 5) <= 30)
				strcpy(auth, s + 5);	
		}
		if (strncmp(s, "reset", 5) == 0)
			free(auth);
		if (strncmp(s, "service", 7) == 0)
			service = strdup(s+ 7);
		if (strncmp(s, "login", 5) == 0)
		{
			if(*(auth[32]) == '\0')
				system("/bin/sh");
			else
				fwrite("Password:\n", 1, 10, stdout);
		}
	}
	return (0);
}
