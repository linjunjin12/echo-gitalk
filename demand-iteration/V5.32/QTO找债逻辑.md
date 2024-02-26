











### 公域债券缓存生成流程

#### 缓存字段定义

```java
@Data
public class ShareBondCache {

    private String bondId;

    private Integer bondInnerCode;

    private String code;

    private String simpleName;

    private String fullName;

    @ApiModelProperty(value = "发行截止日")
    private String issueEndDate;

    @ApiModelProperty(value = "上市日")
    private LocalDate ipoDateConvert;

}
```



#### 公域历史债券缓存跑批



#### 新增公域债券缓存



#### 更新公域债券缓存

##### 更新缓存

##### 删除缓存



### 指导找债逻辑

#### 调用处

```java
// 右面板广告语料解析匹配: /ad/org-ad-group-send-info-entity/parse-match
// 指导发送：guidanceissuancesend.chain.MatchBondBizHandler#process
// 按模板载入时找债：NlpParseResultAndBondDataProviderDecorator#getStandardFields
// 获取指导发送详情：/bond_guidance/send_details
// 中标结果导入找债：/bond/nlp_win_bid/import
// 指导/中标结果语义解析找债：AbstractParseResultHandler#getMatchBondMap
// 群发/右面板 识别导入：/right-panel/primary-bond/match

```



### 解析配置

解析上屏提醒设置：如果为QTO版本，则移除我负责的选项(6)，债销Q,投标Q都一样