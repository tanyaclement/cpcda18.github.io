## Week 12


Open Terminal in macOS and launch our Docker container:

```
docker rm -f pcda_ubuntu
docker pull pcda17/ubuntu-container
docker run --name pcda_ubuntu -ti -p 8889:8889 --volume ~/Desktop/sharedfolder/:/sharedfolder/ pcda17/ubuntu-container
```

In Windows 10, open PowerShell and enter the following to launch the Docker container:

```
docker rm -f pcda_ubuntu
docker pull pcda17/ubuntu-container
docker run --name pcda_ubuntu -ti -p 8889:8889 --volume C:\Users\***username_here***\Desktop\sharedfolder:/sharedfolder/ pcda17/ubuntu-container
```

Download a Jupyter notebook from the list below to `sharedfolder` on your desktop.


Navigate to [localhost:8889](localhost:8889) in your browser to open the notebook.

### In-Class Demos

- [Link to GitHub](https://github.com/pcda17/pcda17.github.io/tree/master/week/13)

### Resources

- [Data Visualization LibGuide](https://guides.lib.utexas.edu/data-visualization/resources)
How to format your data for Tableau: https://public.tableau.com/s/blog/2012/08/how-format-your-data-tableau-public
https://public.tableau.com/en-us/s/gallery
http://onlinehelp.tableau.com/current/guides/get-started-tutorial/en-us/get-started-tutorial-home.html
https://www.tableau.com/learn/tutorials/on-demand/getting-started?edition=unlicensed&version=10.5.0&__full-version=10500.17.1226.1925&platform=mac&status=buy&reg-delay=true
http://dh101.humanities.ucla.edu/?page_id=163
