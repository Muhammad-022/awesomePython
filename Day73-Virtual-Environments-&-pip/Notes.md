# Day 73: Virtual Environments & pip

## Concept
Virtual environments allow you to create isolated Python environments for different projects.  
`pip` is Python’s package manager used to install and manage libraries.

## Why Virtual Environments?
- Avoid version conflicts between projects  
- Keep dependencies separate  
- Easy to manage project-specific packages  

## Create Virtual Environment
1. Open terminal  
2. Navigate to project folder  
3. Run:
```bash
python -m venv env
```
* env is the environment folder name
* On Windows → env\Scripts\activate
* On Mac/Linux → source env/bin/activate
#### pip Basics
* Install package:
```python
pip install package_name
```
* Upgrade package:
```python
pip install --upgrade package_name
```
* List installed packages:
```python
pip list
```
* Freeze requirements:
```python
pip freeze > requirements.txt
```
* Install from requirements:
```python
pip install -r requirements.txt
```
### Use Cases
* Every project has different dependencies
* Deploy projects without breaking other projects
* Maintain Python version compatibility
### Why Learn This?
* Almost every Python project uses virtual environments
* Essential for professional development
* Required for deploying Python apps
