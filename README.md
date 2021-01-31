# php-namumark
php-namumark는 나무위키에서 사용되는 나무마크를 HTML 페이지로 변환하는 라이브러리입니다.

## 라이선스
본 라이브러리는 GNU Affero GPL 3.0에 따라 자유롭게 사용하실 수 있습니다. 라이선스에 대한 자세한 사항은 첨부 문서를 참고하십시오.

## 사용 방법
사용 방법에는 두 가지가 있습니다.
	
### 일반 텍스트로 넘기는 경우

	// 라이브러리를 불러옵니다.
	require_once("namumark.php");
	
	// MySQLWikiPage와는 달리 PlainWikiPage의 첫 번째 인수로 위키텍스트를 받습니다.
	$wPage = new PlainWikiPage("위키텍스트");
	
	// NamuMark 생성자는 WikiPage를 인수로 받습니다.
	$wEngine = new NamuMark($wPage);
	
	// 위키링크의 앞에 붙을 경로를 prefix에 넣습니다.
	$wEngine->prefix = "/wiki";
	
	// toHtml을 호출하면 HTML 페이지가 생성됩니다.
	echo $wEngine->toHtml();
	
## 그 외
상당한 발코딩입니다. 항상 죄송스럽게 생각합니다.

## 2차 수정 사항
해당 PHP 파일 상단에 적어 놓았습니다.

현재 통용되는 나무마크에 맞게 수정하였습니다.
