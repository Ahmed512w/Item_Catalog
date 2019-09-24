# Item Catalog App

#  you should do:
    1.Install Vagrant and VirtualBox
    2.Clone the fullstack-nanodegree-vm
    3.In the vagrant directory in your vm, run Git Bash
    4.run command "vagrant up"
    5.run command "vagrant ssh"
    6.run command "python finalproject.py"


### DB:
    - database_setup.py has the classes for the databas_tables: User / Category / MenuItem

### Routes & function in project.py
    - routes and functions for login google:
        -- @app.route('/login/') - function showLogin() 
        -- @app.route('/gconnect', methods=['POST']) - function gconnect()
        -- @app.route('/disconnect') - function gdisconnect()
    - JSON APIs to view Category Information:
        -- @app.route('/category/<int:category_id>/menu/JSON') - function categoryMenuJSON(category_id)
        -- @app.route('/category/<int:category_id>/item/<int:menu_id>/JSON') - function menuItemJSON(category_id, menu_id)
        -- @app.route('/category/JSON') - function catalogJSON()
    - routes and functions for Item Catalog App:
        -- Show catalog: @app.route('/') / @app.route('/catalog/') - function showCatalog()
        -- Show a Category Items: @app.route('/category/<int:category_id>/items/') - function showMenu(category_id)
        -- Show an item description: @app.route('/category/<int:category_id>/item/<int:menuitem_id>/') - function showMenuItem(category_id, menuitem_id)
        -- Create a new menu item from the page of latest items: @app.route('/category/item/new/',methods=['GET','POST']) - function newMenuItem()
        -- Create a new menu item from the page of specified category: @app.route('/category/<int:category_id>/item/new/',methods=['GET','POST']) -             function newMenuItemWithCat(category_id)
        -- Edit a menu item: @app.route('/category/menu/<int:menuitem_id>/edit', methods=['GET','POST']) - function editMenuItem(menuitem_id)
        -- Delete a menu item: @app.route('/category/item/<int:menuitem_id>/delete', methods = ['GET','POST']) - function deleteMenuItem(menuitem_id)
        -- Disconnect based on provider: @app.route('/disconnect') - function disconnect()

### Static Folder:
    - styles.css has the required css for the html files

### Templates Folder: html files:
        - publiccatalog 
        - publicmenu
        - publicmenuitem
        - header
        - login 
        - majn
        - nav
        - catalog
        - menu 
        - menuitem 
        - newmenuitem 
        - deletemenuitem
        - editmenuitem

### Another files:
    - client_secrets.json: for the login processes with google
