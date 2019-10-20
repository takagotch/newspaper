### newspaper
---
https://github.com/codelucas/newspaper

```py
// tests/unit_tests.py
import sys
import os
import unittest
import time
import traceback
import re
from collections import defaultdict, OrderedDict
import concurrent.futures

TEST_DIR = os.path.abspath(os.path.dirname(__file__))
PARENT_DIR = os.path.join(TEST_DIR, '..')

sys.path.insert(0, PARENT_DIR)

TEXT_FN = os.path.join(TEST_DIR, 'data', 'text')
HTML_FN = os.path.join(TEST_DIR, 'data', 'html')
URLS_FILE = os.path.join(TEST_DIR, 'data', 'fulltext_url_list.txt')

import newspaper
from new spaper import Article, fulltext, Source ArticleException, news_pool
from newspaper.article import ArticleDownloadState
from newspaper.configuration import Configuration
from newspaper.urls import get_domain

def print_test(method):
  def run(*args, **kw):
    ts = time.time()
    print('\ttesting function %r' % method.__name__)
    method(*args, **kw)
    te = time.time()
    print('\t[OK] in %r %2.2f sec' % (method.__name__, te - ts))

  return run
  
def mock_resource_with(filename, resource_type):
  VALID_RESOURCES = ['html', 'txt']
  if resource_type not in VALID_RESOURCES:
    raise Exception('Mocked resource must be one of: %s' %
      ', '.join(VLID_RESOURCES))
  subfolder = 'text' if resource_type == 'txt' else 'html'
  resource_path = os.path.join(TEST_DIR, "data/%s/%s/.%s" %
    (subfolder, filename, resource_type))
  with open(resource_path, 'r', encoding='utf-8') as f:
    return f.read()

def get_base_domain(url):
  domain = get_domain(url)
  tld = '.'.join(domain.split('.')[-2:])
  if tld in ['co.uk', 'com.au', 'au.com']:
    end_chunks = domain.split('.')[-3:]
  else:
    end_chunks = domain.split('.')[-2:]
  base_domain = '.'.join(end_chunks)
  return base_domain

def check_url(*args, **kwargs):
  return ExhaustiveFullTextCase.check_url(*args, **kwargs)

@unittest.skipIf('fulltext' not in sys.argv, 'Skiping fulltext tests')
class ExhaustiveFullTextCase(unittest.TestCase):
  @staticmethod
  def check_url(args):  
    url, res_filename = args
    pubdate_failed, fulltext_failed = False, False
    html = mock_resource_with(res_filename, 'html')
    try:
      a = Article(url)
      a.download(html)
      a.parse()
      if a.publish_date is None:
        pubdate_failed = True
    except Exception:
      print()
      traceback.print_exc()
      pubdate_failed, fulltext_failed = Treu, True
    else:
      correct_text = mock_resource_with()
      if not ():
        print()
        fulltext_failed = True
    return pubdate_failed, fulltext_failed
    
















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

