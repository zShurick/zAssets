�������������

<?php
Assets::factory('css')
            ->files('head', array(
                'style.css',
                'ui/smoothness/style.css',
                'plugin/select2.css',
            ), 100);
 
Assets::factory('js')
            ->files('head', array(
                'core/jquery.js',
                'gadgets/user/auth.js',
            ), 100);
 
// ��� ���-������ ������� �������� ���� � ������ ����������� (�� ��������� 0)
Assets::factory('js')->file('head', 'file.js');
 
//��� css ���
Assets::factory('css')->code('head', '.my-class{color: red;}');

����� ����������

?
...
<head>
    <?=Assets::factory('css')->group('head')?>
    ....
    <?=Assets::factory('js')->group('head')?>

�����������

�� ���������, � ������������ � ����������� �������, ��� ���� � ���������� (���������, ������� ...) ����� ����������� js_host ��� css_host (������: background: (/images/file.jpg) ������� �� background: ('http://static.blog-tree.com/images/file.jpg'));

� ������ Assets ���� ����������� ���������� public static $change_path_in_content = true; ������� ��������� �������� ��������� ����� � �������. ��� ����� ���������� ��� ����������� ������� � ��� ������������� https ������������ ���������, �.�. ������ �� ������������, � �������� �� �������� ����������, ���� � ��� ���� �� ����������� ������.

� 2013 Zagovorichev Alexander
