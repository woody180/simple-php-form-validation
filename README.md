# A very simple PHP form validation

## Validation rules
- alpha
- alpha_spaces
- alpha_num_spaces
- numeric
- alpha_num
- valid_email
- valid_url
- valid_slug
- min[]
- max[]
- ext[jpg,jpeg,gif,bmp]
- min_size[20000]
- max_size[200000]
- required
- valid_input
- string


## Validation demo
```
$valiate = $validation
            ->with($_POST['something'])
            ->rules([
                'name|Name' => 'required|alpha',
                'username|UserName' => 'required|min[4]|max[20]|alpha_num',
                'email|eMail' => 'valid_email|min[5]',
                'password|Password' => 'min[5]'
            ])
            ->validate();

```
