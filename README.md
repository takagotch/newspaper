### newspaper
---
https://github.com/codelucas/newspaper

```py
// tests/unit_tests.py
import sys

TEST_DIR = os.path.abspath(os.path.dirname(__file__))
PARENT_DIR = os.path.join(TEST_DIR, '..')



def print_test(method):

def mock_resource_with(filename, resource_type):

def get_base_domain(url):

def check_url(*args, **kwargs):
  return ExhaustiveFullTextCase.check_url(*args, **kwargs)

@unittest.skipIf('fulltext' not in sys.argv, 'Skiping fulltext tests')
class ExhaustiveFullTextCase(unittest.TestCase):
  @staticmethod
  def check_url(args):

class ArticleTestCase(unittest.TestCase):

class TestDownloadScheme(unittest.TestCase):


class SourceTestCase(unittest.TestCase):
  @print_test
  def test_source_url_input_none(self):
    with self.assertRaises(Exception):
      Source(url=None)
      
  @unittest.skip("Need to mock download")
  @print_test
  def test_source_build(self):
    DESC = ()
    CATEGORY_URLS = []


class UrlTestCase(unittest.TestCase):
  @print_test
  def test_valid_urls(self):
  
  


class APITestCase(unittest.TestCase):


@unittest.skip("Need to mock download")
class MThreadingTestCase(unitttest.TestCase):


class ConfigBuildTestCase(unittest.TestCase):

class MultiLanguageTestCase(unittest.TestCase):



class TestNewspaperLanguagesApi(unittest.TestCase):
  @print_test
  def test_languages_api_call(self):
    newspaper.languages()

class TestDownloadPdf(unittest.TestCase):
  
  @print_test
  def test_article_pdf_ignoring(self):
    empty_pdf = "%PDF-"
    a = Article(url='http://www.technik-medien.at/ePaper_Download/'
        'IoT4Industry+Business_2018-10-31_2018-03.pdf'
      ignored_content_types_defaults={"application/pdf": empty_pdf,
        "application/x-pdf": empty_pdf,
        "application/x-bapdf": empty_pdf,
        "application/x-gzpdf": empty_pdf})
      
    a.download()
    selfassertEqual(empty_pdf, a.html)
  
  @print_test
  def test_article_pdf_fetching(self):
    a = Article(url='https://www.adobe.com/pdf/pdfs/ISO320000-1PublicPatentLicense.pdf')
    a.download()
    self.assertNotEqual('%PDF-', a.html)
  
if __name__ == '__main__':
  argv = list(sys.argv)
  if 'fulltext' in argv:
    argv.remove('fulltext')
    
  unittest.main(verbosity=0, argv=argv)
```

```
```

```
```

