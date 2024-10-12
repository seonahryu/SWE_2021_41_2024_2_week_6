# SWE_2021_41_2024_2_week_6
---
## Week 4 Assignment
* [Link of my repository](https://github.com/seonahryu/SWE_2021_41_2024_2_week_4)
``` python
def isHappy(n):
  def square(num):
    return sum(int(i)**2 for i in str(num)) #sum of the squares of its digit

  cycle=set() #중복X set

  while n != 1:
    if n in cycle: #loops endlessly in a cycle
      return False
    cycle.add(n)
    n=square(n)
  return True

print(isHappy(19))
print(isHappy(2))
```

* This code defines a function to determine if a number is "happy," meaning that repeatedly summing the squares of its digits will eventually lead to 1.
---
## Week 5 Assignment
>> ``` python
>> docker run <options> --name <container_name><image_name>
>> ```
> * crerate docker container named "<container_name>" from images "<image_name>"
>> ``` python
>> docker attach <container_name>
>> ```
> * attach your terminal to the container
>> ``` python
>> docker stop <container_name>
>> ```
> * stop the running container
> * status changed to 'Exited' from 'Up (running)'
>> ``` python
>> docker start <container_name>
>> ```
> * start the exited/created container
> * status changed to 'Up (running)' from 'Created' or 'Exited'
>> ``` python
>> docker pause <container_name>
>> ```
> * pause the running container
>> ``` python
>> docker unpause <container_name>
>> ```
> * unpause the paused container
>> ``` python
>> docker rm <container_name>
>> ```
> * delete the 'stopped' or 'created' containers
> * with force option(-f), can delete containers in all status
>> ``` python
>> docker commit <container_name><image_name>:<tag>
>> ```
> * commit the container to given image name with tag
>> ``` python
>> docker run -dit --name ossp-container -v <host_dir_path>:<container_dir_path> ossp
>> ```
> * mount <host_dir> to <container_dir> and then share the files
>> ``` python
>> docker exec <your container> cat /etc/os-release
>> ```
> * Displays the operating system details of the specified container.
>> ``` python
>> docker exec <your container> git --version
>> ```
> * Checks the installed version of Git in the specified container.
>> ``` python
>> docker exec <your container> python3 --version
>> ```
> * Displays the installed version of Python 3 in the specified container.
>> ``` python
>> docker inspect --format="{{ .HostConfig.Binds }}" <container_name>
>> ```
> * Retrieves the bind mount information for the specified container.
<br>
![my output](./2023312822유선아.png)
