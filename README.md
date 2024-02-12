# Text-Game-Development-System
这是一个生成文本游戏的程序，具体功能和权限设置如下：

1. 程序保存游戏内容的文件夹下，每个游戏以自己的名字保存为.bat文件。
2. 程序需要设置开发者、客户和超级管理员三种权限。
   a. 开发者权限：拥有编写和游玩游戏的权限。
   b. 客户权限：拥有游玩游戏和提出建议的权限。
   c. 超级管理员权限：拥有最高权限，可以修改文本内容和管理用户权限。

3. 用户需要输入用户名和密码来判断权限，并可以选择注册新用户。用户信息包括权限等级、用户名、密码和用户ID，并以加密方式保存到user.bat文件中。

4. 不同权限的用户进入程序后，会有相应的欢迎字符串和页面内容：
   a. 开发者权限：
      - 可以选择制作游戏或游玩游戏。
      - 如果用户的日志文件状态为true，则告知权限修改并将状态变更为false。
   b. 客户权限：
      - 可以选择游玩游戏。
   c. 评价功能：
      - 所有权限的用户都可以在游戏结束后对游戏进行评分和评价（1-5分）。
      - 开发者不能评价自己的游戏。

5. 编写游戏时需要保存的内容包括：
   a. 开发者ID
   b. 评分、评分人数和评语（以链表形式保存）
   c. 游戏相关的文本文件（以游戏名+.bat形式保存）
   d. 主角属性（可以选择是否需要主角）：包括主角名和对应属性，并嵌套在游戏内容结构中。

6. 开发者选择编写游戏后的流程：
   a. 提示开发者输入游戏名。
   b. 询问是否需要创建主角及其属性，并保存到相应结构体中。
   c. 使用树的形式保存游戏的文本内容。
   d. 按层次依次询问开发者每个节点的名称和内容，并询问是否修改主角属性。
   e. 如果父节点是根节点，则按顺序询问是否有子节点并继续上述步骤；如果父节点不是根节点，则询问父节点的兄弟节点。
   f. 游戏记录完毕后以"游戏名.bat"的形式保存。

7. 开发者或客户选择游玩游戏后的流程：
   a. 展示现有游戏列表，按游戏名、开发者名和评分进行展示。
   b. 进入游戏后展示游戏名、主角名/属性和分支名。
   c. 当主角属性发生变化时，提示修改。
   d. 游戏结束后询问是否进行评分和建议。

8. 超级管理员权限：
   - 除了拥有开发者和客户的权限外，还可以修改其他用户的权限。
   - 可以在程序运行过程中修改提示文本，通过添加对应选项实现，列出当前所有提示文本供超级管理员修改。


This is a program for generating text-based games, with specific functions and permission settings as follows:

The program saves the game content in a folder, with each game saved as a .bat file named after itself.

The program needs to set three types of permissions: developer, customer, and super administrator.
a. Developer permission: has the privilege to write and play games.
b. Customer permission: has the privilege to play games and provide suggestions.
c. Super administrator permission: has the highest authority, can modify text content and manage user permissions.

Users need to input usernames and passwords to determine permissions, and can choose to register as a new user. User information includes permission level, username, password, and user ID, encrypted and saved in the user.bat file.

Upon entering the program, users with different permissions will see corresponding welcome messages and page contents:
a. Developer permission:

Can choose to create games or play games.
If the user's log file status is true, inform about permission modification and change the status to false. b. Customer permission:
Can choose to play games. c. Rating feature:
All users with permissions can rate and review the game (1-5 points) after playing.
Developers cannot rate their own games.
Content to be saved when writing games includes:
a. Developer ID
b. Ratings, number of raters, and comments (saved in linked list form)
c. Game-related text files (saved in the form of game name + .bat)
d. Protagonist attributes (optional): including protagonist name and corresponding attributes, nested in the game content structure.

Process for developers choosing to write games:
a. Prompt the developer to enter the game name.
b. Inquire if a protagonist and their attributes need to be created, and save them in the respective structure.
c. Save the game's text content in a tree structure.
d. Ask the developer for the name and content of each node in sequence, and inquire if the protagonist attributes need to be modified.
e. If the parent node is the root node, ask in order if there are child nodes and continue the above steps; if the parent node is not the root node, inquire about the sibling nodes of the parent node.
f. After completing the game, save it in the form of "game name.bat".

Process for developers or customers choosing to play games:
a. Display the existing game list based on game name, developer name, and ratings.
b. Upon entering the game, display the game name, protagonist name/attributes, and branch names.
c. Prompt for modification when protagonist attributes change.
d. After the game ends, ask if there is a need for rating and suggestions.

Super administrator permission:

In addition to having developer and customer permissions, can modify the permissions of other users.
Can modify prompt texts during program execution, by adding corresponding options, listing all current prompt texts for super administrators to modify.
