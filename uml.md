```<mxGraphModel dx="1505" dy="1032" grid="1" gridSize="10" guides="1" tooltips="1" connect="1" arrows="1" fold="1" page="0" pageScale="1" pageWidth="827" pageHeight="1169" background="none" math="0" shadow="0">
  <root>
    <mxCell id="0" />
    <mxCell id="1" parent="0" />
    <mxCell id="node31" value="&lt;p style=&quot;margin:0px;margin-top:4px;text-align:center;&quot;&gt;&lt;b&gt;Advertisement&lt;/b&gt;&lt;/p&gt;&lt;hr size=&quot;1&quot;/&gt;&lt;p style=&quot;margin:0 0 0 4px;line-height:1.6;&quot;&gt;- date: LocalDateTime&lt;br/&gt;- title: String&lt;br/&gt;- id: UUID&lt;br/&gt;- price: Double&lt;br/&gt;- category: Category&lt;br/&gt;- description: String&lt;br/&gt;- user: User&lt;br/&gt;- views: Long&lt;br/&gt;- imagesUrl: List&amp;lt;String&amp;gt;&lt;br/&gt;- subscriptions: List&amp;lt;UserSubscription&amp;gt;&lt;/p&gt;" style="verticalAlign=top;align=left;overflow=fill;fontSize=14;fontFamily=Helvetica;html=1;rounded=0;shadow=0;comic=0;labelBackgroundColor=none;strokeWidth=1;" parent="1" vertex="1">
      <mxGeometry x="1292" y="546" width="284" height="261" as="geometry" />
    </mxCell>
    <mxCell id="node18" value="&lt;p style=&quot;margin:0px;margin-top:4px;text-align:center;&quot;&gt;&lt;b&gt;AdvertisementController&lt;/b&gt;&lt;/p&gt;&lt;hr size=&quot;1&quot;/&gt;&lt;p style=&quot;margin:0 0 0 4px;line-height:1.6;&quot;&gt;- service: AdvertisementService&lt;/p&gt;" style="verticalAlign=top;align=left;overflow=fill;fontSize=14;fontFamily=Helvetica;html=1;rounded=0;shadow=0;comic=0;labelBackgroundColor=none;strokeWidth=1;" parent="1" vertex="1">
      <mxGeometry x="1274" y="2089" width="241" height="58" as="geometry" />
    </mxCell>
    <mxCell id="node8" value="&lt;p style=&quot;margin:0px;margin-top:4px;text-align:center;&quot;&gt;&lt;i&gt;&amp;lt;&amp;lt;interface&amp;gt;&amp;gt;&lt;/i&gt;&lt;br/&gt;&lt;b&gt;AdvertisementMapper&lt;/b&gt;&lt;/p&gt;&lt;hr size=&quot;1&quot;/&gt;&lt;p style=&quot;margin:0 0 0 4px;line-height:1.6;&quot;&gt;+ INSTANCE: AdvertisementMapper&lt;/p&gt;" style="verticalAlign=top;align=left;overflow=fill;fontSize=14;fontFamily=Helvetica;html=1;rounded=0;shadow=0;comic=0;labelBackgroundColor=none;strokeWidth=1;" parent="1" vertex="1">
      <mxGeometry x="786" y="1149" width="257" height="81" as="geometry" />
    </mxCell>
    <mxCell id="node14" value="&lt;p style=&quot;margin:0px;margin-top:4px;text-align:center;&quot;&gt;&lt;i&gt;&amp;lt;&amp;lt;interface&amp;gt;&amp;gt;&lt;/i&gt;&lt;br/&gt;&lt;b&gt;AdvertisementRepository&lt;/b&gt;&lt;/p&gt;&lt;hr size=&quot;1&quot;/&gt;" style="verticalAlign=top;align=left;overflow=fill;fontSize=14;fontFamily=Helvetica;html=1;rounded=0;shadow=0;comic=0;labelBackgroundColor=none;strokeWidth=1;" parent="1" vertex="1">
      <mxGeometry x="652" y="1442" width="245" height="48" as="geometry" />
    </mxCell>
    <mxCell id="node25" value="&lt;p style=&quot;margin:0px;margin-top:4px;text-align:center;&quot;&gt;&lt;b&gt;AdvertisementService&lt;/b&gt;&lt;/p&gt;&lt;hr size=&quot;1&quot;/&gt;&lt;p style=&quot;margin:0 0 0 4px;line-height:1.6;&quot;&gt;- fileService: FileService&lt;br/&gt;- cService: CategoryService&lt;br/&gt;- log: Logger&lt;br/&gt;- categoryRepository: CategoryRepository&lt;br/&gt;- repository: AdvertisementRepository&lt;br/&gt;- nService: NotificationService&lt;br/&gt;- messageSource: MessageSource&lt;br/&gt;- mapper: AdvertisementMapper&lt;/p&gt;" style="verticalAlign=top;align=left;overflow=fill;fontSize=14;fontFamily=Helvetica;html=1;rounded=0;shadow=0;comic=0;labelBackgroundColor=none;strokeWidth=1;" parent="1" vertex="1">
      <mxGeometry x="1065" y="1669" width="298" height="215" as="geometry" />
    </mxCell>
    <mxCell id="node3" value="&lt;p style=&quot;margin:0px;margin-top:4px;text-align:center;&quot;&gt;&lt;b&gt;AuthenticationController&lt;/b&gt;&lt;/p&gt;&lt;hr size=&quot;1&quot;/&gt;&lt;p style=&quot;margin:0 0 0 4px;line-height:1.6;&quot;&gt;- service: AuthenticationService&lt;br/&gt;- uService: UserService&lt;/p&gt;" style="verticalAlign=top;align=left;overflow=fill;fontSize=14;fontFamily=Helvetica;html=1;rounded=0;shadow=0;comic=0;labelBackgroundColor=none;strokeWidth=1;" parent="1" vertex="1">
      <mxGeometry x="73" y="2078" width="242" height="83" as="geometry" />
    </mxCell>
    <mxCell id="node19" value="&lt;p style=&quot;margin:0px;margin-top:4px;text-align:center;&quot;&gt;&lt;b&gt;AuthenticationService&lt;/b&gt;&lt;/p&gt;&lt;hr size=&quot;1&quot;/&gt;&lt;p style=&quot;margin:0 0 0 4px;line-height:1.6;&quot;&gt;- passwordEncoder: PasswordEncoder&lt;br/&gt;- authenticationManager: AuthenticationManager&lt;br/&gt;- jwtService: JwtService&lt;br/&gt;- userRepository: UserRepository&lt;/p&gt;" style="verticalAlign=top;align=left;overflow=fill;fontSize=14;fontFamily=Helvetica;html=1;rounded=0;shadow=0;comic=0;labelBackgroundColor=none;strokeWidth=1;" parent="1" vertex="1">
      <mxGeometry x="-178" y="1715" width="344" height="133" as="geometry" />
    </mxCell>
    <mxCell id="node2" value="&lt;p style=&quot;margin:0px;margin-top:4px;text-align:center;&quot;&gt;&lt;b&gt;Category&lt;/b&gt;&lt;/p&gt;&lt;hr size=&quot;1&quot;/&gt;&lt;p style=&quot;margin:0 0 0 4px;line-height:1.6;&quot;&gt;- name: String&lt;br/&gt;- subcategories: List&amp;lt;Category&amp;gt;&lt;br/&gt;- id: UUID&lt;br/&gt;- parent: Category&lt;br/&gt;- advertisements: List&amp;lt;Advertisement&amp;gt;&lt;/p&gt;" style="verticalAlign=top;align=left;overflow=fill;fontSize=14;fontFamily=Helvetica;html=1;rounded=0;shadow=0;comic=0;labelBackgroundColor=none;strokeWidth=1;" parent="1" vertex="1">
      <mxGeometry x="1454" y="903" width="281" height="146" as="geometry" />
    </mxCell>
    <mxCell id="node17" value="&lt;p style=&quot;margin:0px;margin-top:4px;text-align:center;&quot;&gt;&lt;b&gt;CategoryController&lt;/b&gt;&lt;/p&gt;&lt;hr size=&quot;1&quot;/&gt;&lt;p style=&quot;margin:0 0 0 4px;line-height:1.6;&quot;&gt;- service: CategoryService&lt;/p&gt;" style="verticalAlign=top;align=left;overflow=fill;fontSize=14;fontFamily=Helvetica;html=1;rounded=0;shadow=0;comic=0;labelBackgroundColor=none;strokeWidth=1;" parent="1" vertex="1">
      <mxGeometry x="1414" y="1749" width="200" height="58" as="geometry" />
    </mxCell>
    <mxCell id="node16" value="&lt;p style=&quot;margin:0px;margin-top:4px;text-align:center;&quot;&gt;&lt;i&gt;&amp;lt;&amp;lt;interface&amp;gt;&amp;gt;&lt;/i&gt;&lt;br/&gt;&lt;b&gt;CategoryMapper&lt;/b&gt;&lt;/p&gt;&lt;hr size=&quot;1&quot;/&gt;&lt;p style=&quot;margin:0 0 0 4px;line-height:1.6;&quot;&gt;+ INSTANCE: CategoryMapper&lt;/p&gt;" style="verticalAlign=top;align=left;overflow=fill;fontSize=14;fontFamily=Helvetica;html=1;rounded=0;shadow=0;comic=0;labelBackgroundColor=none;strokeWidth=1;" parent="1" vertex="1">
      <mxGeometry x="1483" y="1149" width="222" height="81" as="geometry" />
    </mxCell>
    <mxCell id="node20" value="&lt;p style=&quot;margin:0px;margin-top:4px;text-align:center;&quot;&gt;&lt;i&gt;&amp;lt;&amp;lt;interface&amp;gt;&amp;gt;&lt;/i&gt;&lt;br/&gt;&lt;b&gt;CategoryRepository&lt;/b&gt;&lt;/p&gt;&lt;hr size=&quot;1&quot;/&gt;" style="verticalAlign=top;align=left;overflow=fill;fontSize=14;fontFamily=Helvetica;html=1;rounded=0;shadow=0;comic=0;labelBackgroundColor=none;strokeWidth=1;" parent="1" vertex="1">
      <mxGeometry x="1172" y="1162" width="204" height="48" as="geometry" />
    </mxCell>
    <mxCell id="node15" value="&lt;p style=&quot;margin:0px;margin-top:4px;text-align:center;&quot;&gt;&lt;b&gt;CategoryService&lt;/b&gt;&lt;/p&gt;&lt;hr size=&quot;1&quot;/&gt;&lt;p style=&quot;margin:0 0 0 4px;line-height:1.6;&quot;&gt;- messageSource: MessageSource&lt;br/&gt;- repository: CategoryRepository&lt;br/&gt;- categoryMapper: CategoryMapper&lt;/p&gt;" style="verticalAlign=top;align=left;overflow=fill;fontSize=14;fontFamily=Helvetica;html=1;rounded=0;shadow=0;comic=0;labelBackgroundColor=none;strokeWidth=1;" parent="1" vertex="1">
      <mxGeometry x="1544" y="1406" width="260" height="108" as="geometry" />
    </mxCell>
    <mxCell id="node30" value="&lt;p style=&quot;margin:0px;margin-top:4px;text-align:center;&quot;&gt;&lt;b&gt;FileService&lt;/b&gt;&lt;/p&gt;&lt;hr size=&quot;1&quot;/&gt;&lt;p style=&quot;margin:0 0 0 4px;line-height:1.6;&quot;&gt;- uploadDirectory: String&lt;br/&gt;- messageSource: MessageSource&lt;/p&gt;" style="verticalAlign=top;align=left;overflow=fill;fontSize=14;fontFamily=Helvetica;html=1;rounded=0;shadow=0;comic=0;labelBackgroundColor=none;strokeWidth=1;" parent="1" vertex="1">
      <mxGeometry x="188" y="1197" width="253" height="83" as="geometry" />
    </mxCell>
    <mxCell id="node13" value="&lt;p style=&quot;margin:0px;margin-top:4px;text-align:center;&quot;&gt;&lt;b&gt;ForbiddenException&lt;/b&gt;&lt;/p&gt;&lt;hr size=&quot;1&quot;/&gt;" style="verticalAlign=top;align=left;overflow=fill;fontSize=14;fontFamily=Helvetica;html=1;rounded=0;shadow=0;comic=0;labelBackgroundColor=none;strokeWidth=1;" parent="1" vertex="1">
      <mxGeometry x="1291" y="1442" width="206" height="30" as="geometry" />
    </mxCell>
    <mxCell id="node26" value="&lt;p style=&quot;margin:0px;margin-top:4px;text-align:center;&quot;&gt;&lt;b&gt;NoChangesException&lt;/b&gt;&lt;/p&gt;&lt;hr size=&quot;1&quot;/&gt;" style="verticalAlign=top;align=left;overflow=fill;fontSize=14;fontFamily=Helvetica;html=1;rounded=0;shadow=0;comic=0;labelBackgroundColor=none;strokeWidth=1;" parent="1" vertex="1">
      <mxGeometry x="45" y="1442" width="218" height="30" as="geometry" />
    </mxCell>
    <mxCell id="node24" value="&lt;p style=&quot;margin:0px;margin-top:4px;text-align:center;&quot;&gt;&lt;b&gt;Notification&lt;/b&gt;&lt;/p&gt;&lt;hr size=&quot;1&quot;/&gt;&lt;p style=&quot;margin:0 0 0 4px;line-height:1.6;&quot;&gt;- seen: boolean&lt;br/&gt;- user: User&lt;br/&gt;- value: String&lt;br/&gt;- id: UUID&lt;br/&gt;- date: LocalDateTime&lt;/p&gt;" style="verticalAlign=top;align=left;overflow=fill;fontSize=14;fontFamily=Helvetica;html=1;rounded=0;shadow=0;comic=0;labelBackgroundColor=none;strokeWidth=1;" parent="1" vertex="1">
      <mxGeometry x="1629" y="603" width="171" height="146" as="geometry" />
    </mxCell>
    <mxCell id="node9" value="&lt;p style=&quot;margin:0px;margin-top:4px;text-align:center;&quot;&gt;&lt;i&gt;&amp;lt;&amp;lt;interface&amp;gt;&amp;gt;&lt;/i&gt;&lt;br/&gt;&lt;b&gt;NotificationMapper&lt;/b&gt;&lt;/p&gt;&lt;hr size=&quot;1&quot;/&gt;&lt;p style=&quot;margin:0 0 0 4px;line-height:1.6;&quot;&gt;+ INSTANCE: NotificationMapper&lt;/p&gt;" style="verticalAlign=top;align=left;overflow=fill;fontSize=14;fontFamily=Helvetica;html=1;rounded=0;shadow=0;comic=0;labelBackgroundColor=none;strokeWidth=1;" parent="1" vertex="1">
      <mxGeometry x="1139" y="1960" width="237" height="80" as="geometry" />
    </mxCell>
    <mxCell id="node12" value="&lt;p style=&quot;margin:0px;margin-top:4px;text-align:center;&quot;&gt;&lt;i&gt;&amp;lt;&amp;lt;interface&amp;gt;&amp;gt;&lt;/i&gt;&lt;br/&gt;&lt;b&gt;NotificationRepository&lt;/b&gt;&lt;/p&gt;&lt;hr size=&quot;1&quot;/&gt;" style="verticalAlign=top;align=left;overflow=fill;fontSize=14;fontFamily=Helvetica;html=1;rounded=0;shadow=0;comic=0;labelBackgroundColor=none;strokeWidth=1;" parent="1" vertex="1">
      <mxGeometry x="263" y="2002" width="223" height="35" as="geometry" />
    </mxCell>
    <mxCell id="node0" value="&lt;p style=&quot;margin:0px;margin-top:4px;text-align:center;&quot;&gt;&lt;b&gt;NotificationService&lt;/b&gt;&lt;/p&gt;&lt;hr size=&quot;1&quot;/&gt;&lt;p style=&quot;margin:0 0 0 4px;line-height:1.6;&quot;&gt;- webSocketHandler: WebSocketHandler&lt;br/&gt;- log: Logger&lt;/p&gt;" style="verticalAlign=top;align=left;overflow=fill;fontSize=14;fontFamily=Helvetica;html=1;rounded=0;shadow=0;comic=0;labelBackgroundColor=none;strokeWidth=1;" parent="1" vertex="1">
      <mxGeometry x="949" y="1418" width="291" height="83" as="geometry" />
    </mxCell>
    <mxCell id="node21" value="&lt;p style=&quot;margin:0px;margin-top:4px;text-align:center;&quot;&gt;&lt;i&gt;&amp;lt;&amp;lt;enumeration&amp;gt;&amp;gt;&lt;/i&gt;&lt;br/&gt;&lt;b&gt;Role&lt;/b&gt;&lt;/p&gt;&lt;hr size=&quot;1&quot;/&gt;&lt;p style=&quot;margin:0 0 0 4px;line-height:1.6;&quot;&gt;+ ADMIN: &lt;br/&gt;+ USER: &lt;/p&gt;" style="verticalAlign=top;align=left;overflow=fill;fontSize=14;fontFamily=Helvetica;html=1;rounded=0;shadow=0;comic=0;labelBackgroundColor=none;strokeWidth=1;" parent="1" vertex="1">
      <mxGeometry x="867" y="-2" width="95" height="96" as="geometry" />
    </mxCell>
    <mxCell id="node23" value="&lt;p style=&quot;margin:0px;margin-top:4px;text-align:center;&quot;&gt;&lt;i&gt;&amp;lt;&amp;lt;interface&amp;gt;&amp;gt;&lt;/i&gt;&lt;br/&gt;&lt;b&gt;SubscribtionRepository&lt;/b&gt;&lt;/p&gt;&lt;hr size=&quot;1&quot;/&gt;" style="verticalAlign=top;align=left;overflow=fill;fontSize=14;fontFamily=Helvetica;html=1;rounded=0;shadow=0;comic=0;labelBackgroundColor=none;strokeWidth=1;" parent="1" vertex="1">
      <mxGeometry x="519" y="1280" width="230" height="40" as="geometry" />
    </mxCell>
    <mxCell id="node5" value="&lt;p style=&quot;margin:0px;margin-top:4px;text-align:center;&quot;&gt;&lt;b&gt;SubscriptionController&lt;/b&gt;&lt;/p&gt;&lt;hr size=&quot;1&quot;/&gt;&lt;p style=&quot;margin:0 0 0 4px;line-height:1.6;&quot;&gt;- service: SubscriptionService&lt;/p&gt;" style="verticalAlign=top;align=left;overflow=fill;fontSize=14;fontFamily=Helvetica;html=1;rounded=0;shadow=0;comic=0;labelBackgroundColor=none;strokeWidth=1;" parent="1" vertex="1">
      <mxGeometry x="801" y="2089" width="226" height="58" as="geometry" />
    </mxCell>
    <mxCell id="node28" value="&lt;p style=&quot;margin:0px;margin-top:4px;text-align:center;&quot;&gt;&lt;b&gt;SubscriptionService&lt;/b&gt;&lt;/p&gt;&lt;hr size=&quot;1&quot;/&gt;&lt;p style=&quot;margin:0 0 0 4px;line-height:1.6;&quot;&gt;- messageSource: MessageSource&lt;br/&gt;- advertisementRepository: AdvertisementRepository&lt;br/&gt;- mapper: UserSubscriptionMapper&lt;br/&gt;- repository: SubscribtionRepository&lt;/p&gt;" style="verticalAlign=top;align=left;overflow=fill;fontSize=14;fontFamily=Helvetica;html=1;rounded=0;shadow=0;comic=0;labelBackgroundColor=none;strokeWidth=1;" parent="1" vertex="1">
      <mxGeometry x="530" y="1715" width="368" height="133" as="geometry" />
    </mxCell>
    <mxCell id="node10" value="&lt;p style=&quot;margin:0px;margin-top:4px;text-align:center;&quot;&gt;&lt;b&gt;User&lt;/b&gt;&lt;/p&gt;&lt;hr size=&quot;1&quot;/&gt;&lt;p style=&quot;margin:0 0 0 4px;line-height:1.6;&quot;&gt;- advertisements: List&amp;lt;Advertisement&amp;gt;&lt;br/&gt;- name: String&lt;br/&gt;- subscriptions: List&amp;lt;UserSubscription&amp;gt;&lt;br/&gt;- password: String&lt;br/&gt;- id: UUID&lt;br/&gt;- avatarUrl: String&lt;br/&gt;- email: String&lt;br/&gt;- role: Role&lt;/p&gt;" style="verticalAlign=top;align=left;overflow=fill;fontSize=14;fontFamily=Helvetica;html=1;rounded=0;shadow=0;comic=0;labelBackgroundColor=none;strokeWidth=1;" parent="1" vertex="1">
      <mxGeometry x="772" y="229" width="284" height="215" as="geometry" />
    </mxCell>
    <mxCell id="node22" value="&lt;p style=&quot;margin:0px;margin-top:4px;text-align:center;&quot;&gt;&lt;b&gt;UserController&lt;/b&gt;&lt;/p&gt;&lt;hr size=&quot;1&quot;/&gt;&lt;p style=&quot;margin:0 0 0 4px;line-height:1.6;&quot;&gt;- service: UserService&lt;/p&gt;" style="verticalAlign=top;align=left;overflow=fill;fontSize=14;fontFamily=Helvetica;html=1;rounded=0;shadow=0;comic=0;labelBackgroundColor=none;strokeWidth=1;" parent="1" vertex="1">
      <mxGeometry x="428" y="2089" width="173" height="58" as="geometry" />
    </mxCell>
    <mxCell id="node27" value="&lt;p style=&quot;margin:0px;margin-top:4px;text-align:center;&quot;&gt;&lt;i&gt;&amp;lt;&amp;lt;interface&amp;gt;&amp;gt;&lt;/i&gt;&lt;br/&gt;&lt;b&gt;UserMapper&lt;/b&gt;&lt;/p&gt;&lt;hr size=&quot;1&quot;/&gt;&lt;p style=&quot;margin:0 0 0 4px;line-height:1.6;&quot;&gt;+ INSTANCE: UserMapper&lt;/p&gt;" style="verticalAlign=top;align=left;overflow=fill;fontSize=14;fontFamily=Helvetica;html=1;rounded=0;shadow=0;comic=0;labelBackgroundColor=none;strokeWidth=1;" parent="1" vertex="1">
      <mxGeometry x="-83" y="1309" width="195" height="68" as="geometry" />
    </mxCell>
    <mxCell id="node6" value="&lt;p style=&quot;margin:0px;margin-top:4px;text-align:center;&quot;&gt;&lt;i&gt;&amp;lt;&amp;lt;interface&amp;gt;&amp;gt;&lt;/i&gt;&lt;br/&gt;&lt;b&gt;UserRepository&lt;/b&gt;&lt;/p&gt;&lt;hr size=&quot;1&quot;/&gt;" style="verticalAlign=top;align=left;overflow=fill;fontSize=14;fontFamily=Helvetica;html=1;rounded=0;shadow=0;comic=0;labelBackgroundColor=none;strokeWidth=1;" parent="1" vertex="1">
      <mxGeometry x="-190" y="1442" width="169" height="35" as="geometry" />
    </mxCell>
    <mxCell id="node29" value="&lt;p style=&quot;margin:0px;margin-top:4px;text-align:center;&quot;&gt;&lt;b&gt;UserService&lt;/b&gt;&lt;/p&gt;&lt;hr size=&quot;1&quot;/&gt;&lt;p style=&quot;margin:0 0 0 4px;line-height:1.6;&quot;&gt;- passwordEncoder: PasswordEncoder&lt;br/&gt;- fileService: FileService&lt;br/&gt;- repository: UserRepository&lt;br/&gt;- messageSource: MessageSource&lt;br/&gt;- userMapper: UserMapper&lt;br/&gt;- log: Logger&lt;/p&gt;" style="verticalAlign=top;align=left;overflow=fill;fontSize=14;fontFamily=Helvetica;html=1;rounded=0;shadow=0;comic=0;labelBackgroundColor=none;strokeWidth=1;" parent="1" vertex="1">
      <mxGeometry x="215" y="1692" width="278" height="169" as="geometry" />
    </mxCell>
    <mxCell id="node4" value="&lt;p style=&quot;margin:0px;margin-top:4px;text-align:center;&quot;&gt;&lt;b&gt;UserSubscription&lt;/b&gt;&lt;/p&gt;&lt;hr size=&quot;1&quot;/&gt;&lt;p style=&quot;margin:0 0 0 4px;line-height:1.6;&quot;&gt;- id: UUID&lt;br/&gt;- user: User&lt;br/&gt;- ad: Advertisement&lt;/p&gt;" style="verticalAlign=top;align=left;overflow=fill;fontSize=14;fontFamily=Helvetica;html=1;rounded=0;shadow=0;comic=0;labelBackgroundColor=none;strokeWidth=1;" parent="1" vertex="1">
      <mxGeometry x="1382" y="-14" width="185" height="108" as="geometry" />
    </mxCell>
    <mxCell id="node1" value="&lt;p style=&quot;margin:0px;margin-top:4px;text-align:center;&quot;&gt;&lt;i&gt;&amp;lt;&amp;lt;interface&amp;gt;&amp;gt;&lt;/i&gt;&lt;br/&gt;&lt;b&gt;UserSubscriptionMapper&lt;/b&gt;&lt;/p&gt;&lt;hr size=&quot;1&quot;/&gt;&lt;p style=&quot;margin:0 0 0 4px;line-height:1.6;&quot;&gt;+ INSTANCE: UserSubscriptionMapper&lt;/p&gt;" style="verticalAlign=top;align=left;overflow=fill;fontSize=14;fontFamily=Helvetica;html=1;rounded=0;shadow=0;comic=0;labelBackgroundColor=none;strokeWidth=1;" parent="1" vertex="1">
      <mxGeometry x="338" y="1404" width="273" height="86" as="geometry" />
    </mxCell>
    <mxCell id="edge12" value="" style="html=1;rounded=1;edgeStyle=orthogonalEdgeStyle;dashed=0;startArrow=diamondThinstartSize=12;endArrow=openThin;endSize=12;strokeColor=#595959;exitX=0.500;exitY=0.000;exitDx=0;exitDy=0;entryX=0.500;entryY=0.000;entryDx=0;entryDy=0;" parent="1" source="node31" target="node2" edge="1">
      <mxGeometry width="50" height="50" relative="1" as="geometry">
        <Array as="points">
          <mxPoint x="1434" y="496" />
          <mxPoint x="1274" y="496" />
          <mxPoint x="1274" y="876" />
          <mxPoint x="1594" y="876" />
        </Array>
      </mxGeometry>
    </mxCell>
    <mxCell id="label72" value="1" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge12" vertex="1" connectable="0">
      <mxGeometry x="1321" y="478" as="geometry" />
    </mxCell>
    <mxCell id="label76" value="1" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge12" vertex="1" connectable="0">
      <mxGeometry x="1535" y="858" as="geometry" />
    </mxCell>
    <mxCell id="label77" value="category" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge12" vertex="1" connectable="0">
      <mxGeometry x="1594" y="880" as="geometry" />
    </mxCell>
    <mxCell id="edge4" value="" style="html=1;rounded=1;edgeStyle=orthogonalEdgeStyle;dashed=0;startArrow=diamondThinstartSize=12;endArrow=openThin;endSize=12;strokeColor=#595959;exitX=0.500;exitY=0.000;exitDx=0;exitDy=0;entryX=0.500;entryY=0.000;entryDx=0;entryDy=0;" parent="1" source="node31" target="node10" edge="1">
      <mxGeometry width="50" height="50" relative="1" as="geometry">
        <Array as="points">
          <mxPoint x="1434" y="516" />
          <mxPoint x="1474" y="516" />
          <mxPoint x="1474" y="456" />
          <mxPoint x="1714" y="456" />
          <mxPoint x="1714" y="356" />
          <mxPoint x="1394" y="356" />
          <mxPoint x="1394" y="176" />
          <mxPoint x="914" y="176" />
        </Array>
      </mxGeometry>
    </mxCell>
    <mxCell id="label24" value="1" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge4" vertex="1" connectable="0">
      <mxGeometry x="1528" y="438" as="geometry" />
    </mxCell>
    <mxCell id="label28" value="1" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge4" vertex="1" connectable="0">
      <mxGeometry x="1028" y="158" as="geometry" />
    </mxCell>
    <mxCell id="label29" value="user" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge4" vertex="1" connectable="0">
      <mxGeometry x="914" y="193" as="geometry" />
    </mxCell>
    <mxCell id="edge35" value="" style="html=1;rounded=1;edgeStyle=orthogonalEdgeStyle;dashed=0;startArrow=diamondThinstartSize=12;endArrow=openThin;endSize=12;strokeColor=#595959;exitX=0.500;exitY=0.000;exitDx=0;exitDy=0;entryX=0.500;entryY=1.000;entryDx=0;entryDy=0;" parent="1" source="node31" target="node4" edge="1">
      <mxGeometry width="50" height="50" relative="1" as="geometry">
        <Array as="points">
          <mxPoint x="1434" y="516" />
          <mxPoint x="1474" y="516" />
        </Array>
      </mxGeometry>
    </mxCell>
    <mxCell id="label210" value="1" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge35" vertex="1" connectable="0">
      <mxGeometry x="1448" y="498" as="geometry" />
    </mxCell>
    <mxCell id="label214" value="*" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge35" vertex="1" connectable="0">
      <mxGeometry x="1464" y="206" as="geometry" />
    </mxCell>
    <mxCell id="label215" value="subscriptions" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge35" vertex="1" connectable="0">
      <mxGeometry x="1474" y="206" as="geometry" />
    </mxCell>
    <mxCell id="edge16" value="" style="html=1;rounded=0;edgeStyle=orthogonalEdgeStyle;dashed=0;startArrow=diamondThinstartSize=12;endArrow=openThin;endSize=12;strokeColor=#595959;exitX=0.500;exitY=0.001;exitDx=0;exitDy=0;entryX=0.250;entryY=0.000;entryDx=0;entryDy=0;curved=0;" parent="1" source="node18" target="node25" edge="1">
      <mxGeometry width="50" height="50" relative="1" as="geometry">
        <Array as="points">
          <mxPoint x="1394" y="1616" />
          <mxPoint x="1140" y="1616" />
        </Array>
      </mxGeometry>
    </mxCell>
    <mxCell id="label96" value="1" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge16" vertex="1" connectable="0">
      <mxGeometry x="1382" y="2066" as="geometry" />
    </mxCell>
    <mxCell id="label100" value="1" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge16" vertex="1" connectable="0">
      <mxGeometry x="1382" y="1796" as="geometry" />
    </mxCell>
    <mxCell id="label101" value="" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge16" vertex="1" connectable="0">
      <mxGeometry x="1394" y="1654" as="geometry" />
    </mxCell>
    <mxCell id="edge11" value="" style="html=1;rounded=1;edgeStyle=orthogonalEdgeStyle;dashed=1;startArrow=none;endArrow=openThin;endSize=12;strokeColor=#595959;exitX=0.500;exitY=0.000;exitDx=0;exitDy=0;entryX=0.500;entryY=1.000;entryDx=0;entryDy=0;" parent="1" source="node8" target="node2" edge="1">
      <mxGeometry width="50" height="50" relative="1" as="geometry">
        <Array as="points">
          <mxPoint x="914" y="1136" />
          <mxPoint x="1594" y="1136" />
        </Array>
      </mxGeometry>
    </mxCell>
    <mxCell id="label68" value="«create»" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge11" vertex="1" connectable="0">
      <mxGeometry x="1226" y="1117" as="geometry" />
    </mxCell>
    <mxCell id="edge32" value="" style="html=1;rounded=1;edgeStyle=orthogonalEdgeStyle;dashed=1;startArrow=none;endArrow=openThin;endSize=12;strokeColor=#595959;exitX=0.500;exitY=0.001;exitDx=0;exitDy=0;entryX=0.500;entryY=1.000;entryDx=0;entryDy=0;" parent="1" source="node8" target="node10" edge="1">
      <mxGeometry width="50" height="50" relative="1" as="geometry">
        <Array as="points" />
      </mxGeometry>
    </mxCell>
    <mxCell id="label194" value="«create»" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge32" vertex="1" connectable="0">
      <mxGeometry x="858" y="787" as="geometry" />
    </mxCell>
    <mxCell id="edge20" value="" style="html=1;rounded=1;edgeStyle=orthogonalEdgeStyle;dashed=0;startArrow=diamondThinstartSize=12;endArrow=openThin;endSize=12;strokeColor=#595959;exitX=0.250;exitY=0.000;exitDx=0;exitDy=0;entryX=0.500;entryY=1.001;entryDx=0;entryDy=0;" parent="1" source="node25" target="node8" edge="1">
      <mxGeometry width="50" height="50" relative="1" as="geometry">
        <Array as="points">
          <mxPoint x="1140" y="1636" />
          <mxPoint x="1134" y="1636" />
          <mxPoint x="1134" y="1516" />
          <mxPoint x="914" y="1516" />
        </Array>
      </mxGeometry>
    </mxCell>
    <mxCell id="label120" value="1" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge20" vertex="1" connectable="0">
      <mxGeometry x="981" y="1498" as="geometry" />
    </mxCell>
    <mxCell id="label124" value="" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge20" vertex="1" connectable="0">
      <mxGeometry x="902" y="1208" as="geometry" />
    </mxCell>
    <mxCell id="label125" value="" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge20" vertex="1" connectable="0">
      <mxGeometry x="914" y="1208" as="geometry" />
    </mxCell>
    <mxCell id="edge1" value="" style="html=1;rounded=1;edgeStyle=orthogonalEdgeStyle;dashed=0;startArrow=diamondThinstartSize=12;endArrow=openThin;endSize=12;strokeColor=#595959;exitX=0.250;exitY=0.000;exitDx=0;exitDy=0;entryX=0.500;entryY=1.001;entryDx=0;entryDy=0;" parent="1" source="node25" target="node14" edge="1">
      <mxGeometry width="50" height="50" relative="1" as="geometry">
        <Array as="points">
          <mxPoint x="1140" y="1636" />
          <mxPoint x="1134" y="1636" />
          <mxPoint x="1134" y="1536" />
          <mxPoint x="774" y="1536" />
        </Array>
      </mxGeometry>
    </mxCell>
    <mxCell id="label6" value="1" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge1" vertex="1" connectable="0">
      <mxGeometry x="888" y="1518" as="geometry" />
    </mxCell>
    <mxCell id="label10" value="1" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge1" vertex="1" connectable="0">
      <mxGeometry x="828" y="1518" as="geometry" />
    </mxCell>
    <mxCell id="label11" value="" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge1" vertex="1" connectable="0">
      <mxGeometry x="774" y="1475" as="geometry" />
    </mxCell>
    <mxCell id="edge13" value="" style="html=1;rounded=1;edgeStyle=orthogonalEdgeStyle;dashed=0;startArrow=diamondThinstartSize=12;endArrow=openThin;endSize=12;strokeColor=#595959;exitX=0.250;exitY=0.000;exitDx=0;exitDy=0;entryX=0.500;entryY=1.001;entryDx=0;entryDy=0;" parent="1" source="node25" target="node20" edge="1">
      <mxGeometry width="50" height="50" relative="1" as="geometry">
        <Array as="points">
          <mxPoint x="1140" y="1636" />
          <mxPoint x="1134" y="1636" />
          <mxPoint x="1134" y="1516" />
          <mxPoint x="1274" y="1516" />
        </Array>
      </mxGeometry>
    </mxCell>
    <mxCell id="label78" value="1" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge13" vertex="1" connectable="0">
      <mxGeometry x="1245" y="1498" as="geometry" />
    </mxCell>
    <mxCell id="label82" value="" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge13" vertex="1" connectable="0">
      <mxGeometry x="1262" y="1195" as="geometry" />
    </mxCell>
    <mxCell id="label83" value="" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge13" vertex="1" connectable="0">
      <mxGeometry x="1274" y="1235" as="geometry" />
    </mxCell>
    <mxCell id="edge27" value="" style="html=1;rounded=0;edgeStyle=orthogonalEdgeStyle;dashed=0;startArrow=diamondThinstartSize=12;endArrow=openThin;endSize=12;strokeColor=#595959;exitX=0.250;exitY=0.000;exitDx=0;exitDy=0;curved=0;" parent="1" source="node25" edge="1">
      <mxGeometry width="50" height="50" relative="1" as="geometry">
        <Array as="points">
          <mxPoint x="1140" y="1636" />
          <mxPoint x="1134" y="1636" />
          <mxPoint x="1134" y="1576" />
          <mxPoint x="1514" y="1576" />
          <mxPoint x="1514" y="1360" />
          <mxPoint x="1610" y="1360" />
          <mxPoint x="1610" y="1406" />
        </Array>
        <mxPoint x="1610" y="1406" as="targetPoint" />
      </mxGeometry>
    </mxCell>
    <mxCell id="label162" value="1" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge27" vertex="1" connectable="0">
      <mxGeometry x="1223" y="1558" as="geometry" />
    </mxCell>
    <mxCell id="label166" value="1" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge27" vertex="1" connectable="0">
      <mxGeometry x="1628" y="1338" as="geometry" />
    </mxCell>
    <mxCell id="label167" value="" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge27" vertex="1" connectable="0">
      <mxGeometry x="1514" y="1512" as="geometry" />
    </mxCell>
    <mxCell id="edge31" value="" style="html=1;rounded=1;edgeStyle=orthogonalEdgeStyle;dashed=0;startArrow=diamondThinstartSize=12;endArrow=openThin;endSize=12;strokeColor=#595959;exitX=0.250;exitY=0.000;exitDx=0;exitDy=0;entryX=0.500;entryY=1.001;entryDx=0;entryDy=0;" parent="1" source="node25" target="node30" edge="1">
      <mxGeometry width="50" height="50" relative="1" as="geometry">
        <Array as="points">
          <mxPoint x="1140" y="1636" />
          <mxPoint x="1134" y="1636" />
          <mxPoint x="1134" y="1556" />
          <mxPoint x="314" y="1556" />
        </Array>
      </mxGeometry>
    </mxCell>
    <mxCell id="label186" value="1" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge31" vertex="1" connectable="0">
      <mxGeometry x="991" y="1538" as="geometry" />
    </mxCell>
    <mxCell id="label190" value="1" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge31" vertex="1" connectable="0">
      <mxGeometry x="302" y="1380" as="geometry" />
    </mxCell>
    <mxCell id="label191" value="" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge31" vertex="1" connectable="0">
      <mxGeometry x="314" y="1380" as="geometry" />
    </mxCell>
    <mxCell id="edge15" value="" style="html=1;rounded=1;edgeStyle=orthogonalEdgeStyle;dashed=1;startArrow=none;endArrow=openThin;endSize=12;strokeColor=#595959;exitX=0.750;exitY=0.000;exitDx=0;exitDy=0;entryX=0.500;entryY=1.001;entryDx=0;entryDy=0;" parent="1" source="node25" target="node13" edge="1">
      <mxGeometry width="50" height="50" relative="1" as="geometry">
        <Array as="points">
          <mxPoint x="1289" y="1596" />
          <mxPoint x="1394" y="1596" />
        </Array>
      </mxGeometry>
    </mxCell>
    <mxCell id="label92" value="" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge15" vertex="1" connectable="0">
      <mxGeometry x="1338" y="1545" as="geometry" />
    </mxCell>
    <mxCell id="edge28" value="" style="html=1;rounded=1;edgeStyle=orthogonalEdgeStyle;dashed=0;startArrow=diamondThinstartSize=12;endArrow=openThin;endSize=12;strokeColor=#595959;exitX=0.250;exitY=0.000;exitDx=0;exitDy=0;entryX=0.500;entryY=1.001;entryDx=0;entryDy=0;" parent="1" source="node25" target="node0" edge="1">
      <mxGeometry width="50" height="50" relative="1" as="geometry">
        <Array as="points">
          <mxPoint x="1140" y="1636" />
          <mxPoint x="1134" y="1636" />
          <mxPoint x="1134" y="1516" />
          <mxPoint x="1094" y="1516" />
        </Array>
      </mxGeometry>
    </mxCell>
    <mxCell id="label168" value="1" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge28" vertex="1" connectable="0">
      <mxGeometry x="1088" y="1498" as="geometry" />
    </mxCell>
    <mxCell id="label172" value="1" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge28" vertex="1" connectable="0">
      <mxGeometry x="1108" y="1498" as="geometry" />
    </mxCell>
    <mxCell id="label173" value="nService" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge28" vertex="1" connectable="0">
      <mxGeometry x="1134" y="1507" as="geometry" />
    </mxCell>
    <mxCell id="edge30" value="" style="html=1;rounded=1;edgeStyle=orthogonalEdgeStyle;dashed=0;startArrow=diamondThinstartSize=12;endArrow=openThin;endSize=12;strokeColor=#595959;exitX=0.500;exitY=0.001;exitDx=0;exitDy=0;entryX=0.500;entryY=0.000;entryDx=0;entryDy=0;" parent="1" source="node3" target="node19" edge="1">
      <mxGeometry width="50" height="50" relative="1" as="geometry">
        <Array as="points">
          <mxPoint x="194" y="1676" />
          <mxPoint x="-6" y="1676" />
        </Array>
      </mxGeometry>
    </mxCell>
    <mxCell id="label180" value="1" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge30" vertex="1" connectable="0">
      <mxGeometry x="182" y="2055" as="geometry" />
    </mxCell>
    <mxCell id="label184" value="1" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge30" vertex="1" connectable="0">
      <mxGeometry x="182" y="1707" as="geometry" />
    </mxCell>
    <mxCell id="label185" value="service" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge30" vertex="1" connectable="0">
      <mxGeometry x="-6" y="1686" as="geometry" />
    </mxCell>
    <mxCell id="edge5" value="" style="html=1;rounded=1;edgeStyle=orthogonalEdgeStyle;dashed=0;startArrow=diamondThinstartSize=12;endArrow=openThin;endSize=12;strokeColor=#595959;exitX=0.500;exitY=0.001;exitDx=0;exitDy=0;entryX=0.250;entryY=0.000;entryDx=0;entryDy=0;" parent="1" source="node3" target="node29" edge="1">
      <mxGeometry width="50" height="50" relative="1" as="geometry">
        <Array as="points">
          <mxPoint x="194" y="1976" />
          <mxPoint x="514" y="1976" />
          <mxPoint x="514" y="1656" />
          <mxPoint x="285" y="1656" />
        </Array>
      </mxGeometry>
    </mxCell>
    <mxCell id="label30" value="1" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge5" vertex="1" connectable="0">
      <mxGeometry x="295" y="1958" as="geometry" />
    </mxCell>
    <mxCell id="label34" value="1" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge5" vertex="1" connectable="0">
      <mxGeometry x="241" y="1958" as="geometry" />
    </mxCell>
    <mxCell id="label35" value="uService" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge5" vertex="1" connectable="0">
      <mxGeometry x="514" y="1860" as="geometry" />
    </mxCell>
    <mxCell id="edge8" value="" style="html=1;rounded=1;edgeStyle=orthogonalEdgeStyle;dashed=0;startArrow=diamondThinstartSize=12;endArrow=openThin;endSize=12;strokeColor=#595959;exitX=0.500;exitY=0.000;exitDx=0;exitDy=0;entryX=0.500;entryY=1.001;entryDx=0;entryDy=0;" parent="1" source="node19" target="node6" edge="1">
      <mxGeometry width="50" height="50" relative="1" as="geometry">
        <Array as="points">
          <mxPoint x="-6" y="1496" />
          <mxPoint x="-106" y="1496" />
        </Array>
      </mxGeometry>
    </mxCell>
    <mxCell id="label48" value="1" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge8" vertex="1" connectable="0">
      <mxGeometry x="-18" y="1640" as="geometry" />
    </mxCell>
    <mxCell id="label52" value="1" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge8" vertex="1" connectable="0">
      <mxGeometry x="-74" y="1478" as="geometry" />
    </mxCell>
    <mxCell id="label53" value="userRepository" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge8" vertex="1" connectable="0">
      <mxGeometry x="-55" y="1496" as="geometry" />
    </mxCell>
    <mxCell id="edge10" value="" style="html=1;rounded=1;edgeStyle=orthogonalEdgeStyle;dashed=0;startArrow=diamondThinstartSize=12;endArrow=openThin;endSize=12;strokeColor=#595959;exitX=0.500;exitY=0.000;exitDx=0;exitDy=0;entryX=0.500;entryY=0.000;entryDx=0;entryDy=0;" parent="1" source="node2" target="node31" edge="1">
      <mxGeometry width="50" height="50" relative="1" as="geometry">
        <Array as="points">
          <mxPoint x="1594" y="476" />
          <mxPoint x="1434" y="476" />
        </Array>
      </mxGeometry>
    </mxCell>
    <mxCell id="label60" value="1" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge10" vertex="1" connectable="0">
      <mxGeometry x="1582" y="809" as="geometry" />
    </mxCell>
    <mxCell id="label64" value="*" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge10" vertex="1" connectable="0">
      <mxGeometry x="1584" y="595" as="geometry" />
    </mxCell>
    <mxCell id="label65" value="advertisements" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge10" vertex="1" connectable="0">
      <mxGeometry x="1594" y="766" as="geometry" />
    </mxCell>
    <mxCell id="edge24" value="" style="html=1;rounded=0;edgeStyle=orthogonalEdgeStyle;dashed=0;startArrow=diamondThinstartSize=12;endArrow=openThin;endSize=12;strokeColor=#595959;exitX=0.500;exitY=0.001;exitDx=0;exitDy=0;entryX=0.254;entryY=0.001;entryDx=0;entryDy=0;entryPerimeter=0;curved=0;" parent="1" source="node17" target="node15" edge="1">
      <mxGeometry width="50" height="50" relative="1" as="geometry">
        <Array as="points">
          <mxPoint x="1514" y="1360" />
          <mxPoint x="1610" y="1360" />
          <mxPoint x="1610" y="1405" />
        </Array>
      </mxGeometry>
    </mxCell>
    <mxCell id="label144" value="1" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge24" vertex="1" connectable="0">
      <mxGeometry x="1502" y="1726" as="geometry" />
    </mxCell>
    <mxCell id="label148" value="1" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge24" vertex="1" connectable="0">
      <mxGeometry x="1502" y="1426" as="geometry" />
    </mxCell>
    <mxCell id="label149" value="" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge24" vertex="1" connectable="0">
      <mxGeometry x="1514" y="1386" as="geometry" />
    </mxCell>
    <mxCell id="edge34" value="" style="html=1;rounded=1;edgeStyle=orthogonalEdgeStyle;dashed=1;startArrow=none;endArrow=openThin;endSize=12;strokeColor=#595959;exitX=0.500;exitY=0.001;exitDx=0;exitDy=0;entryX=0.500;entryY=1.000;entryDx=0;entryDy=0;" parent="1" source="node16" target="node2" edge="1">
      <mxGeometry width="50" height="50" relative="1" as="geometry">
        <Array as="points" />
      </mxGeometry>
    </mxCell>
    <mxCell id="label206" value="«create»" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge34" vertex="1" connectable="0">
      <mxGeometry x="1538" y="1090" as="geometry" />
    </mxCell>
    <mxCell id="edge17" value="" style="html=1;rounded=0;edgeStyle=orthogonalEdgeStyle;dashed=0;startArrow=diamondThin;endArrow=openThin;endSize=12;strokeColor=#595959;exitX=0.500;exitY=0.000;exitDx=0;exitDy=0;entryX=0.500;entryY=1.001;entryDx=0;entryDy=0;curved=0;startFill=0;startSize=12;" parent="1" source="node15" target="node16" edge="1">
      <mxGeometry width="50" height="50" relative="1" as="geometry">
        <Array as="points">
          <mxPoint x="1674" y="1280" />
          <mxPoint x="1594" y="1280" />
        </Array>
      </mxGeometry>
    </mxCell>
    <mxCell id="label102" value="1" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge17" vertex="1" connectable="0">
      <mxGeometry x="1582" y="1302" as="geometry" />
    </mxCell>
    <mxCell id="label106" value="" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge17" vertex="1" connectable="0">
      <mxGeometry x="1582" y="1208" as="geometry" />
    </mxCell>
    <mxCell id="label107" value="" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge17" vertex="1" connectable="0">
      <mxGeometry x="1594" y="1208" as="geometry" />
    </mxCell>
    <mxCell id="edge6" value="" style="html=1;rounded=0;edgeStyle=orthogonalEdgeStyle;dashed=0;startArrow=diamondThin;endArrow=openThin;endSize=12;strokeColor=#595959;exitX=0.500;exitY=0.000;exitDx=0;exitDy=0;entryX=0.500;entryY=1.001;entryDx=0;entryDy=0;curved=0;startFill=0;startSize=12;" parent="1" source="node15" target="node20" edge="1">
      <mxGeometry width="50" height="50" relative="1" as="geometry">
        <Array as="points">
          <mxPoint x="1674" y="1336" />
          <mxPoint x="1274" y="1336" />
        </Array>
      </mxGeometry>
    </mxCell>
    <mxCell id="label36" value="1" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge6" vertex="1" connectable="0">
      <mxGeometry x="1535" y="1318" as="geometry" />
    </mxCell>
    <mxCell id="label40" value="1" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge6" vertex="1" connectable="0">
      <mxGeometry x="1321" y="1318" as="geometry" />
    </mxCell>
    <mxCell id="label41" value="" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge6" vertex="1" connectable="0">
      <mxGeometry x="1274" y="1205" as="geometry" />
    </mxCell>
    <mxCell id="edge25" value="" style="html=1;rounded=1;edgeStyle=orthogonalEdgeStyle;dashed=0;startArrow=diamondThinstartSize=12;endArrow=openThin;endSize=12;strokeColor=#595959;exitX=0.500;exitY=0.000;exitDx=0;exitDy=0;entryX=0.500;entryY=0.000;entryDx=0;entryDy=0;" parent="1" source="node24" target="node10" edge="1">
      <mxGeometry width="50" height="50" relative="1" as="geometry">
        <Array as="points">
          <mxPoint x="1714" y="356" />
          <mxPoint x="1394" y="356" />
          <mxPoint x="1394" y="176" />
          <mxPoint x="914" y="176" />
        </Array>
      </mxGeometry>
    </mxCell>
    <mxCell id="label150" value="1" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge25" vertex="1" connectable="0">
      <mxGeometry x="1702" y="580" as="geometry" />
    </mxCell>
    <mxCell id="label154" value="1" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge25" vertex="1" connectable="0">
      <mxGeometry x="988" y="158" as="geometry" />
    </mxCell>
    <mxCell id="label155" value="user" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge25" vertex="1" connectable="0">
      <mxGeometry x="914" y="167" as="geometry" />
    </mxCell>
    <mxCell id="edge9" value="" style="html=1;rounded=0;edgeStyle=orthogonalEdgeStyle;dashed=0;startArrow=diamondThin;endArrow=openThin;endSize=12;strokeColor=#595959;exitX=0.500;exitY=0.000;exitDx=0;exitDy=0;entryX=0.763;entryY=0.004;entryDx=0;entryDy=0;startFill=0;targetPerimeterSpacing=0;sourcePerimeterSpacing=0;startSize=12;entryPerimeter=0;curved=0;" parent="1" source="node5" target="node28" edge="1">
      <mxGeometry width="50" height="50" relative="1" as="geometry">
        <Array as="points">
          <mxPoint x="914" y="1676" />
          <mxPoint x="810" y="1676" />
          <mxPoint x="810" y="1716" />
        </Array>
      </mxGeometry>
    </mxCell>
    <mxCell id="label54" value="1" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge9" vertex="1" connectable="0">
      <mxGeometry x="902" y="2066" as="geometry" />
    </mxCell>
    <mxCell id="label58" value="" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge9" vertex="1" connectable="0">
      <mxGeometry x="902" y="1708" as="geometry" />
    </mxCell>
    <mxCell id="label59" value="" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge9" vertex="1" connectable="0">
      <mxGeometry x="914" y="1750" as="geometry" />
    </mxCell>
    <mxCell id="edge21" value="" style="html=1;rounded=0;edgeStyle=orthogonalEdgeStyle;dashed=0;startArrow=diamondThin;endArrow=openThin;endSize=12;strokeColor=#595959;exitX=0.500;exitY=0.000;exitDx=0;exitDy=0;entryX=0.500;entryY=1.001;entryDx=0;entryDy=0;curved=0;startFill=0;startSize=12;" parent="1" source="node28" target="node14" edge="1">
      <mxGeometry width="50" height="50" relative="1" as="geometry">
        <Array as="points">
          <mxPoint x="714" y="1656" />
          <mxPoint x="634" y="1656" />
          <mxPoint x="634" y="1616" />
          <mxPoint x="774" y="1616" />
        </Array>
      </mxGeometry>
    </mxCell>
    <mxCell id="label126" value="" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge21" vertex="1" connectable="0">
      <mxGeometry x="745" y="1598" as="geometry" />
    </mxCell>
    <mxCell id="label130" value="" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge21" vertex="1" connectable="0">
      <mxGeometry x="762" y="1485" as="geometry" />
    </mxCell>
    <mxCell id="label131" value="" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge21" vertex="1" connectable="0">
      <mxGeometry x="774" y="1583" as="geometry" />
    </mxCell>
    <mxCell id="edge33" value="" style="html=1;rounded=0;edgeStyle=orthogonalEdgeStyle;dashed=0;startArrow=diamondThin;endArrow=openThin;endSize=12;strokeColor=#595959;exitX=0.500;exitY=0.000;exitDx=0;exitDy=0;entryX=0.500;entryY=1.001;entryDx=0;entryDy=0;curved=0;startFill=0;startSize=12;" parent="1" source="node28" target="node23" edge="1">
      <mxGeometry width="50" height="50" relative="1" as="geometry">
        <Array as="points">
          <mxPoint x="714" y="1656" />
          <mxPoint x="634" y="1656" />
        </Array>
      </mxGeometry>
    </mxCell>
    <mxCell id="label198" value="" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge33" vertex="1" connectable="0">
      <mxGeometry x="622" y="1586" as="geometry" />
    </mxCell>
    <mxCell id="label202" value="" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge33" vertex="1" connectable="0">
      <mxGeometry x="622" y="1355" as="geometry" />
    </mxCell>
    <mxCell id="label203" value="" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge33" vertex="1" connectable="0">
      <mxGeometry x="634" y="1355" as="geometry" />
    </mxCell>
    <mxCell id="edge29" value="" style="html=1;rounded=0;edgeStyle=orthogonalEdgeStyle;dashed=0;startArrow=diamondThin;endArrow=openThin;endSize=12;strokeColor=#595959;exitX=0.500;exitY=0.000;exitDx=0;exitDy=0;entryX=0.500;entryY=1.001;entryDx=0;entryDy=0;startSize=12;startFill=0;curved=0;" parent="1" source="node28" target="node1" edge="1">
      <mxGeometry width="50" height="50" relative="1" as="geometry">
        <Array as="points">
          <mxPoint x="714" y="1656" />
          <mxPoint x="634" y="1656" />
          <mxPoint x="634" y="1636" />
          <mxPoint x="474" y="1636" />
        </Array>
      </mxGeometry>
    </mxCell>
    <mxCell id="label174" value="" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge29" vertex="1" connectable="0">
      <mxGeometry x="521" y="1618" as="geometry" />
    </mxCell>
    <mxCell id="label178" value="" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge29" vertex="1" connectable="0">
      <mxGeometry x="462" y="1488" as="geometry" />
    </mxCell>
    <mxCell id="label179" value="" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge29" vertex="1" connectable="0">
      <mxGeometry x="474" y="1488" as="geometry" />
    </mxCell>
    <mxCell id="edge2" value="" style="html=1;rounded=1;edgeStyle=orthogonalEdgeStyle;dashed=0;startArrow=diamondThinstartSize=12;endArrow=openThin;endSize=12;strokeColor=#595959;exitX=0.500;exitY=0.000;exitDx=0;exitDy=0;entryX=0.500;entryY=0.000;entryDx=0;entryDy=0;" parent="1" source="node10" target="node31" edge="1">
      <mxGeometry width="50" height="50" relative="1" as="geometry">
        <Array as="points">
          <mxPoint x="914" y="196" />
          <mxPoint x="1354" y="196" />
          <mxPoint x="1354" y="376" />
          <mxPoint x="1434" y="376" />
        </Array>
      </mxGeometry>
    </mxCell>
    <mxCell id="label12" value="1" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge2" vertex="1" connectable="0">
      <mxGeometry x="1361" y="358" as="geometry" />
    </mxCell>
    <mxCell id="label16" value="*" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge2" vertex="1" connectable="0">
      <mxGeometry x="1362" y="318" as="geometry" />
    </mxCell>
    <mxCell id="label17" value="advertisements" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge2" vertex="1" connectable="0">
      <mxGeometry x="1434" y="523" as="geometry" />
    </mxCell>
    <mxCell id="edge7" value="" style="html=1;rounded=1;edgeStyle=orthogonalEdgeStyle;dashed=0;startArrow=diamondThinstartSize=12;endArrow=openThin;endSize=12;strokeColor=#595959;exitX=0.500;exitY=0.000;exitDx=0;exitDy=0;entryX=0.500;entryY=1.000;entryDx=0;entryDy=0;" parent="1" source="node10" target="node21" edge="1">
      <mxGeometry width="50" height="50" relative="1" as="geometry">
        <Array as="points" />
      </mxGeometry>
    </mxCell>
    <mxCell id="label42" value="" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge7" vertex="1" connectable="0">
      <mxGeometry x="902" y="104" as="geometry" />
    </mxCell>
    <mxCell id="label46" value="" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge7" vertex="1" connectable="0">
      <mxGeometry x="902" y="80" as="geometry" />
    </mxCell>
    <mxCell id="label47" value="" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge7" vertex="1" connectable="0">
      <mxGeometry x="914" y="80" as="geometry" />
    </mxCell>
    <mxCell id="edge22" value="" style="html=1;rounded=1;edgeStyle=orthogonalEdgeStyle;dashed=0;startArrow=diamondThinstartSize=12;endArrow=openThin;endSize=12;strokeColor=#595959;exitX=0.500;exitY=0.000;exitDx=0;exitDy=0;entryX=0.500;entryY=1.000;entryDx=0;entryDy=0;" parent="1" source="node10" target="node4" edge="1">
      <mxGeometry width="50" height="50" relative="1" as="geometry">
        <Array as="points">
          <mxPoint x="914" y="136" />
          <mxPoint x="1474" y="136" />
        </Array>
      </mxGeometry>
    </mxCell>
    <mxCell id="label132" value="1" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge22" vertex="1" connectable="0">
      <mxGeometry x="1020" y="118" as="geometry" />
    </mxCell>
    <mxCell id="label136" value="*" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge22" vertex="1" connectable="0">
      <mxGeometry x="1413" y="118" as="geometry" />
    </mxCell>
    <mxCell id="label137" value="subscriptions" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge22" vertex="1" connectable="0">
      <mxGeometry x="1337" y="136" as="geometry" />
    </mxCell>
    <mxCell id="edge19" value="" style="html=1;rounded=1;edgeStyle=orthogonalEdgeStyle;dashed=0;startArrow=diamondThin;endArrow=openThin;endSize=12;strokeColor=#595959;exitX=0.500;exitY=0.000;exitDx=0;exitDy=0;entryX=0.250;entryY=0.000;entryDx=0;entryDy=0;startFill=0;startSize=12;" parent="1" source="node22" target="node29" edge="1">
      <mxGeometry width="50" height="50" relative="1" as="geometry">
        <Array as="points">
          <mxPoint x="514" y="1656" />
          <mxPoint x="285" y="1656" />
        </Array>
      </mxGeometry>
    </mxCell>
    <mxCell id="label114" value="1" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge19" vertex="1" connectable="0">
      <mxGeometry x="502" y="2066" as="geometry" />
    </mxCell>
    <mxCell id="label118" value="1" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge19" vertex="1" connectable="0">
      <mxGeometry x="502" y="1777" as="geometry" />
    </mxCell>
    <mxCell id="label119" value="service" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge19" vertex="1" connectable="0">
      <mxGeometry x="514" y="1690" as="geometry" />
    </mxCell>
    <mxCell id="edge18" value="" style="html=1;rounded=1;edgeStyle=orthogonalEdgeStyle;dashed=0;startArrow=diamondThinstartSize=12;endArrow=openThin;endSize=12;strokeColor=#595959;exitX=0.250;exitY=0.000;exitDx=0;exitDy=0;entryX=0.500;entryY=1.001;entryDx=0;entryDy=0;" parent="1" source="node29" target="node30" edge="1">
      <mxGeometry width="50" height="50" relative="1" as="geometry">
        <Array as="points">
          <mxPoint x="285" y="1636" />
          <mxPoint x="34" y="1636" />
          <mxPoint x="34" y="1576" />
          <mxPoint x="314" y="1576" />
        </Array>
      </mxGeometry>
    </mxCell>
    <mxCell id="label108" value="1" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge18" vertex="1" connectable="0">
      <mxGeometry x="215" y="1558" as="geometry" />
    </mxCell>
    <mxCell id="label112" value="1" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge18" vertex="1" connectable="0">
      <mxGeometry x="302" y="1399" as="geometry" />
    </mxCell>
    <mxCell id="label113" value="" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge18" vertex="1" connectable="0">
      <mxGeometry x="314" y="1399" as="geometry" />
    </mxCell>
    <mxCell id="edge14" value="" style="html=1;rounded=1;edgeStyle=orthogonalEdgeStyle;dashed=1;startArrow=none;endArrow=openThin;endSize=12;strokeColor=#595959;exitX=0.750;exitY=0.000;exitDx=0;exitDy=0;entryX=0.500;entryY=1.001;entryDx=0;entryDy=0;" parent="1" source="node29" target="node26" edge="1">
      <mxGeometry width="50" height="50" relative="1" as="geometry">
        <Array as="points">
          <mxPoint x="424" y="1616" />
          <mxPoint x="154" y="1616" />
        </Array>
      </mxGeometry>
    </mxCell>
    <mxCell id="label86" value="«create»" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge14" vertex="1" connectable="0">
      <mxGeometry x="261" y="1597" as="geometry" />
    </mxCell>
    <mxCell id="edge26" value="" style="html=1;rounded=1;edgeStyle=orthogonalEdgeStyle;dashed=0;startArrow=diamondThinstartSize=12;endArrow=openThin;endSize=12;strokeColor=#595959;exitX=0.250;exitY=0.000;exitDx=0;exitDy=0;entryX=0.500;entryY=1.001;entryDx=0;entryDy=0;" parent="1" source="node29" target="node27" edge="1">
      <mxGeometry width="50" height="50" relative="1" as="geometry">
        <Array as="points">
          <mxPoint x="285" y="1636" />
          <mxPoint x="34" y="1636" />
          <mxPoint x="34" y="1496" />
          <mxPoint x="14" y="1496" />
        </Array>
      </mxGeometry>
    </mxCell>
    <mxCell id="label156" value="1" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge26" vertex="1" connectable="0">
      <mxGeometry x="2" y="1398" as="geometry" />
    </mxCell>
    <mxCell id="label160" value="1" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge26" vertex="1" connectable="0">
      <mxGeometry x="2" y="1368" as="geometry" />
    </mxCell>
    <mxCell id="label161" value="userMapper" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge26" vertex="1" connectable="0">
      <mxGeometry x="14" y="1368" as="geometry" />
    </mxCell>
    <mxCell id="edge0" value="" style="html=1;rounded=1;edgeStyle=orthogonalEdgeStyle;dashed=0;startArrow=diamondThinstartSize=12;endArrow=openThin;endSize=12;strokeColor=#595959;exitX=0.250;exitY=0.000;exitDx=0;exitDy=0;entryX=0.500;entryY=1.001;entryDx=0;entryDy=0;" parent="1" source="node29" target="node6" edge="1">
      <mxGeometry width="50" height="50" relative="1" as="geometry">
        <Array as="points">
          <mxPoint x="285" y="1636" />
          <mxPoint x="34" y="1636" />
          <mxPoint x="34" y="1616" />
          <mxPoint x="-6" y="1616" />
          <mxPoint x="-6" y="1496" />
          <mxPoint x="-106" y="1496" />
        </Array>
      </mxGeometry>
    </mxCell>
    <mxCell id="label0" value="1" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge0" vertex="1" connectable="0">
      <mxGeometry x="8" y="1598" as="geometry" />
    </mxCell>
    <mxCell id="label4" value="1" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge0" vertex="1" connectable="0">
      <mxGeometry x="-87" y="1478" as="geometry" />
    </mxCell>
    <mxCell id="label5" value="repository" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge0" vertex="1" connectable="0">
      <mxGeometry x="-139" y="1496" as="geometry" />
    </mxCell>
    <mxCell id="edge3" value="" style="html=1;rounded=1;edgeStyle=orthogonalEdgeStyle;dashed=0;startArrow=diamondThinstartSize=12;endArrow=openThin;endSize=12;strokeColor=#595959;exitX=0.500;exitY=1.000;exitDx=0;exitDy=0;entryX=0.500;entryY=0.000;entryDx=0;entryDy=0;" parent="1" source="node4" target="node31" edge="1">
      <mxGeometry width="50" height="50" relative="1" as="geometry">
        <Array as="points">
          <mxPoint x="1474" y="116" />
          <mxPoint x="1514" y="116" />
          <mxPoint x="1514" y="156" />
          <mxPoint x="1434" y="156" />
        </Array>
      </mxGeometry>
    </mxCell>
    <mxCell id="label18" value="1" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge3" vertex="1" connectable="0">
      <mxGeometry x="1455" y="98" as="geometry" />
    </mxCell>
    <mxCell id="label22" value="1" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge3" vertex="1" connectable="0">
      <mxGeometry x="1422" y="407" as="geometry" />
    </mxCell>
    <mxCell id="label23" value="ad" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge3" vertex="1" connectable="0">
      <mxGeometry x="1434" y="407" as="geometry" />
    </mxCell>
    <mxCell id="edge23" value="" style="html=1;rounded=1;edgeStyle=orthogonalEdgeStyle;dashed=0;startArrow=diamondThinstartSize=12;endArrow=openThin;endSize=12;strokeColor=#595959;exitX=0.500;exitY=1.000;exitDx=0;exitDy=0;entryX=0.500;entryY=0.000;entryDx=0;entryDy=0;" parent="1" source="node4" target="node10" edge="1">
      <mxGeometry width="50" height="50" relative="1" as="geometry">
        <Array as="points">
          <mxPoint x="1474" y="116" />
          <mxPoint x="1514" y="116" />
          <mxPoint x="1514" y="156" />
          <mxPoint x="914" y="156" />
        </Array>
      </mxGeometry>
    </mxCell>
    <mxCell id="label138" value="1" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge23" vertex="1" connectable="0">
      <mxGeometry x="1488" y="98" as="geometry" />
    </mxCell>
    <mxCell id="label142" value="1" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge23" vertex="1" connectable="0">
      <mxGeometry x="1008" y="138" as="geometry" />
    </mxCell>
    <mxCell id="label143" value="user" style="edgeLabel;resizable=0;html=1;align=left;verticalAlign=top;strokeColor=default;" parent="edge23" vertex="1" connectable="0">
      <mxGeometry x="914" y="147" as="geometry" />
    </mxCell>
  </root>
</mxGraphModel>

```