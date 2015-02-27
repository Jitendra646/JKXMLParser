# JKXMLParser
JKXMLParser is base on NSXLMParser Control.user can easily get   JSON formate response by xmlData, XmlString and XmlURL. It's very user friendly control. 
User use Can Some Public methods:
  1. Block Method
    
    Example
    NSError*parseError;
    NSURL * parseurl=[NSURL URLWithString:url];
    parseError=nil;
    [JKXMLParser parseXMLToJson:parseurl error:parseError completionHandler:^(NSDictionary *xmlDictionary, BOOL finish)
     {
         
         NSString * msg=[NSString stringWithFormat:@"%@",xmlDictionary];
         Alert(@"BlockXmlResponse",msg );
     }];
    
    2.Parse XMlString To jsonResponse
    
    //—Example
    
    NSString * xmlString=@"";
    NSError*parseError;
    NSDictionary *xmlDictionary=[JKXMLParser dictionaryForXMLString:xmlString error:parseError];
    NSString * msg=[NSString stringWithFormat:@"%@",xmlDictionary];
    Alert(@"BlockXmlResponse",msg );
    
    3. Parse XMData to jsonResponse
    
    //- Example
    NSData * data;
    NSError*parseError;
    NSDictionary *xmlDictionary=[JKXMLParser dictionaryForXMLData:data error:parseError];
    
    NSString * msg=[NSString stringWithFormat:@"%@",xmlDictionary];
    Alert(@"XmlDataResponse",msg );
    
    4.Parse XMlURl to jsonResponse
    
    //-Example
    
    NSError*parseError;
    NSURL * parseurl=[NSURL URLWithString:url];
    NSDictionary *xmlDictionary=[JKXMLParser dictionaryForXMLUrl:parseurl error:parseError];
    NSString * msg=[NSString stringWithFormat:@"%@",xmlDictionary];
    Alert(@"BlockXmlResponse",msg );
    
