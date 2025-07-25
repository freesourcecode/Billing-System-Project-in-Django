# Billing System Project in Django with Source Code

The **Billing System Project in Django is built using Python, the Django framework, and the SQLITE3 database**. 

Once downloaded, it can be used both offline and online, offering flexibility depending on your setup.

This program includes a variety of features that allow you to generate bills automatically—eliminating the need for manual billing.

>[!NOTE]
> To start creating a **Billing System Project in Python Django**, makes sure that you have PyCharm Professional IDE Installed in your computer.

## How to Create a Billing System Project in Django?

Here are the steps on how to create a Billing System Project in Django with Source Code.

1. **Open file**.

Open “pycharm professional” after that click “file” and click “new project”.

<img width="484" height="453" alt="image" src="https://github.com/user-attachments/assets/8f2914c9-6609-4dcc-aa74-f858c8ff385f" />

2. **Choose Django**.

After click “new project”, choose “Django” and click.

<img width="152" height="325" alt="image" src="https://github.com/user-attachments/assets/9e28c7af-878e-42c7-8e0e-f005db43c5e1" />

3. **Select file location**.

Then, select a file location wherever you want.

4. **Create application name**.

After that, name your application.

5. **Click create**.

Lastly, finish creating project by clicking “create” button.

<img width="802" height="489" alt="image" src="https://github.com/user-attachments/assets/d435ae3b-2780-4a3b-8e2c-68a4d81a08e0" />

6. **Start Coding**.

Finally, we will now start adding functionality to our Django Framework by adding some functional codes.

## Functionality and Codes of the Billing System Project in Django


* **Create template for the menu in Billing System Project Project in Django**.

In this section, we will learn on how create a templates for the menu. 

To start with, add the following code in your menu.html under the folder of bills/templates/bills.

```
{% load keyy %}
<!doctype html>
	<html lang="en">
	  <head>
	    <!-- Required meta tags -->
	    <meta charset="utf-8">
	    <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">

	    <!-- Bootstrap CSS -->
	    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.1/css/bootstrap.min.css" integrity="sha384-WskhaSGFgHYWDcbwN70/dfYBj47jz9qbsMId/iRN3ewGhXQFZCSftd1LZCfmhktB" crossorigin="anonymous">

	    <title>Menu</title>
	  </head>
	  <body>
      <center><h1>{{ title }}</h1></center>
	  <center>
      <div class='container'>
	  	<div class='row'>
	  		<div class='col'>
	  			<div class='col-sm-6 col-sm-12'>
                    <h3>Menu Options</h3>
                    Name:{{ Name }}<br>
                    Mob.No:{{ mobilenumber }}

	 				<form method='POST' action="{% url 'bill:cal_amount' %}" name= 'myform'>
	 					{% csrf_token %}
                        <input type="hidden" name="name" value="{{ Name }}">
                        <input type="hidden" name="mobilenumber" value="{{ mobilenumber }}">
                        <table>
                            <tr>
                                <th>Items-Name</th>&nbsp
                                <th><center>Quantity</center></th>&nbsp
                                <th><center>Price[Per_units]</center></th>
                            </tr>
                            {{ product.count }}
                            {% for p in products %}
                                <tr>
                                <td>{{ p.product_name }}</td>&nbsp
                                <td><input type="number" min="0" name="q_id_{{ p.product_id }}"></td>&nbsp
                                <td><center>{{ p.product_price }}</center></td>
                                </tr>
                            {% endfor %}                            
                        </table>
	 					<br><button type="submit" class="btn btn-primary">Submit</button>
	  				</form>
	  			</div>
	  		</div>
	  	</div>
	  </div>
      </center>
	    <!-- Optional JavaScript -->
	    <!-- jQuery first, then Popper.js, then Bootstrap JS -->
	    <script src="https://code.jquery.com/jquery-3.3.1.slim.min.js" integrity="sha384-q8i/X+965DzO0rT7abK41JStQIAqVgRVzpbzo5smXKp4YfRvH+8abtTE1Pi6jizo" crossorigin="anonymous"></script>
	    <script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.14.3/umd/popper.min.js" integrity="sha384-ZMP7rVo3mIykV+2+9J3UJ46jBk0WLaUAdn689aCwoqbBJiSnjAK/l8WvCWPIPm49" crossorigin="anonymous"></script>
	    <script src="https://stackpath.bootstrapcdn.com/bootstrap/4.1.1/js/bootstrap.min.js" integrity="sha384-smHYKdLADwkXOn1EmN1qk/HfnUcbVRZyYmZ4qpPea6sjB/pTJ0euyQp0Mk8ck+5T" crossorigin="anonymous"></script>
	  </body>
	  <script type="text/javascript">
	  	function submitform()
	  	{
	  	var formData = JSON.stringify($("#myform").serializeArray());
	  	console.log(formData)
	  	}
	  </script>
	</html>
```

### 📌 Here's the full documentation for the [Billing System Project in Django](https://itsourcecode.com/free-projects/python-projects/billing-system-project-in-django-with-source-code/)

