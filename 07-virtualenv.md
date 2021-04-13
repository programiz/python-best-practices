# Python Virtual Environment (virtualenv)

Video Link: [https://youtu.be/CHpQF1rdUMY](https://youtu.be/CHpQF1rdUMY)

Virtual environments allow us to manage separate and isolated Python environments for each of our Python projects.

In this video, we learned to create and manage our own virtual environments for different Python projects using a tool
named virtualenv.

**Programs in the Video**

- [Create Virtual Environments](#python-multiline-comments)
- [Activate Virtual Environments](#activate-virtual-environments)
- [Deactivate Virtual Environments](#deactivate-virtual-environments)

---

## Create Virtual Environments

In order to create a virtual environment, we can use the `virtualenv` module.

To install `virtualenv`:

```shell
pip install virtualenv
```

Let's now look at how we can create virtual environments.

Let's first create a directory in our current working space:

```shell
mkdir project1
cd project1
```

By default, we are using the global Python environment.

```shell
which python
```

**Output**

```shell
/usr/bin/python
```

If we do `pip list`, we can see the list of currently installed packages and libraries in the global Python
installation.

Now let's create an isolated Python environment.

```shell
python -m virtualenv venv
```

We can see that a `venv` directory gets created in the current workspace. This directory contains minimal Python setup
and executables for our Python project.


---

## Activate Virtual Environments

Now that we have created a virtual environment, let's activate it:

### On Windows

```shell
.\venv\Scripts\activate
```

### On Unix/Mac

```shell
source venv/bin/activate
```

Now, `which python` shows us that instead of the global Python, we are using Python which is inside our virtual
environment.

Let me now install a specific version of the requests library in this virtual environment.

```shell
pip install requests==1.1.0
```

This version of requests is now available only for this virtual environment. It will not have any effect on our global
Python setup.

---

## Deactivate Virtual Environments

In order to deactivate a virtual environment, we can simply use the deactivate command on our terminal.

```shell
deactivate
```

Using a virtual environment will prove very useful once you start working on a number of projects with different
requirements.

You can then put all the additional requirements in a requirements file. This requirement file can then be used to set
up the same type of virtual environment on any machine using:

```shell
pip install -r requirements.txt
```

If you want to remove a virtual environment, you can just delete the folder containing the virtual environment.
