# Custom Sizes #

If you want to change predefined banner sizes you should modify the following files:

server/src/main/app.properties
client/locale/en\_US/ApplicationResource.properties

You need to recompile the project after that.
Do not forget to redeploy the app and restart Tomcat.

Ad formats have the following format:
ad\_format.width\_height=id

For example:
ad\_format.300\_600=18

See the list of existing formats, choose the next available id and set your custom width x height for an ad format.