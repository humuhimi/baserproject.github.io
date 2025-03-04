# コーディング規約

基本的には、 [PSR-12 coding style guide](http://www.php-fig.org/psr/psr-12/) および、 [CakePHP コーディング規約 - 4.x](https://book.cakephp.org/4/ja/contributing/cakephp-coding-conventions.html) に従って頂くものとし、下記のルールにも従います。

　
## クラスヘッダー

クラスの先頭にはクラスヘッダーをつけます。

```php
/**
 * Class SitesController
 * @package BaserCore\Controller\Admin
 */
class SitesController extends BcAdminAppController {}
```

　
## メソッドヘッダー

メソッドの先頭にはメソッドヘッダーをつけます。

　
```php
/**
 * サイト一覧を表示する
 * 
 * @param SiteManageServiceInterface $siteManage
 * @checked
 * @noTodo
 * @unitTest
 */
public function index(SiteManageServiceInterface $siteManage){}
```

　
## メソッド間

メソッドとメソッドの間では１行の空行を入れます。

　
## メソッド名

ロウワーキャメルケースとします。  
また、プライベートメソッドやプロテクテッドメソッドだとしても先頭にアンダースコアはつけません。

　
## プロパティ名と変数名

オブジェクトとなるプロパティ名のみ、アッパーキャメルケースとし、その他の変数は全てロウワーキャメルケースとします。  
また、プライベートメソッドやプロテクテッドメソッドだとしても先頭にアンダースコアはつけません。

```php
class UsersController extends AppController 
{
    public $Users;
    private $user;
    protected function getStatus()
    {
        $user = $this->Users->find()->first();
        return $user->status;
    } 
}
```
　

