# ./src/pyremaid/ast_tools/visitors.py

### Imports

  - ast.AST
  - ast.Import
  - ast.ImportFrom
  - ast.NodeVisitor
  - models.MermaidLink
  - models.MermaidNode
  - typing.Any
  - typing.Optional

---
```mermaid
flowchart TB
    node_0["ast.Module object at 0x10616ab50"]
    node_1["ast.ClassDef object at 0x10616a6d0"]
    node_2["ast.Name object at 0x10616a6a0"]
    node_3["ast.Load object at 0x1060500d0"]
    node_4["ast.FunctionDef object at 0x10616a730"]
    node_5["ast.arguments object at 0x10616a700"]
    node_6["ast.arg object at 0x10616a5e0"]
    node_7["ast.AnnAssign object at 0x10616a5b0"]
    node_8["ast.Attribute object at 0x10616a640"]
    node_9["ast.Name object at 0x10616a610"]
    node_10["ast.Load object at 0x1060500d0"]
    node_11["ast.Store object at 0x106050070"]
    node_12["ast.Subscript object at 0x10616a4f0"]
    node_13["ast.Name object at 0x10616a4c0"]
    node_14["ast.Load object at 0x1060500d0"]
    node_15["ast.Name object at 0x10616a550"]
    node_16["ast.Load object at 0x1060500d0"]
    node_17["ast.Load object at 0x1060500d0"]
    node_18["ast.List object at 0x10616a520"]
    node_19["ast.Load object at 0x1060500d0"]
    node_20["ast.Constant object at 0x10616a430"]
    node_21["ast.FunctionDef object at 0x10616a400"]
    node_22["ast.arguments object at 0x10616a490"]
    node_23["ast.arg object at 0x10616a460"]
    node_24["ast.arg object at 0x10616a340"]
    node_25["ast.Name object at 0x10616a310"]
    node_26["ast.Load object at 0x1060500d0"]
    node_27["ast.For object at 0x10616a3a0"]
    node_28["ast.Name object at 0x10616a370"]
    node_29["ast.Store object at 0x106050070"]
    node_30["ast.Attribute object at 0x10616a250"]
    node_31["ast.Name object at 0x10616a160"]
    node_32["ast.Load object at 0x1060500d0"]
    node_33["ast.Load object at 0x1060500d0"]
    node_34["ast.Expr object at 0x10616a2b0"]
    node_35["ast.Call object at 0x10616a280"]
    node_36["ast.Attribute object at 0x10616a1c0"]
    node_37["ast.Attribute object at 0x10616a190"]
    node_38["ast.Name object at 0x10616a220"]
    node_39["ast.Load object at 0x1060500d0"]
    node_40["ast.Load object at 0x1060500d0"]
    node_41["ast.Load object at 0x1060500d0"]
    node_42["ast.JoinedStr object at 0x10616a1f0"]
    node_43["ast.FormattedValue object at 0x10616a0d0"]
    node_44["ast.Attribute object at 0x10616a0a0"]
    node_45["ast.Name object at 0x10616a130"]
    node_46["ast.Load object at 0x1060500d0"]
    node_47["ast.Load object at 0x1060500d0"]
    node_48["ast.Constant object at 0x10616a100"]
    node_49["ast.Constant object at 0x10616dfa0"]
    node_50["ast.FunctionDef object at 0x10616df70"]
    node_51["ast.arguments object at 0x10616df40"]
    node_52["ast.arg object at 0x10616df10"]
    node_53["ast.arg object at 0x10616dee0"]
    node_54["ast.Name object at 0x10616deb0"]
    node_55["ast.Load object at 0x1060500d0"]
    node_56["ast.Assign object at 0x10616de80"]
    node_57["ast.Name object at 0x10616de50"]
    node_58["ast.Store object at 0x106050070"]
    node_59["ast.Attribute object at 0x10616de20"]
    node_60["ast.Name object at 0x10616ddf0"]
    node_61["ast.Load object at 0x1060500d0"]
    node_62["ast.Load object at 0x1060500d0"]
    node_63["ast.For object at 0x10616ddc0"]
    node_64["ast.Name object at 0x10616dd90"]
    node_65["ast.Store object at 0x106050070"]
    node_66["ast.Attribute object at 0x10616dd60"]
    node_67["ast.Name object at 0x10616dd30"]
    node_68["ast.Load object at 0x1060500d0"]
    node_69["ast.Load object at 0x1060500d0"]
    node_70["ast.Expr object at 0x10616dd00"]
    node_71["ast.Call object at 0x10616dcd0"]
    node_72["ast.Attribute object at 0x10616dca0"]
    node_73["ast.Attribute object at 0x10616dc70"]
    node_74["ast.Name object at 0x10616dc40"]
    node_75["ast.Load object at 0x1060500d0"]
    node_76["ast.Load object at 0x1060500d0"]
    node_77["ast.Load object at 0x1060500d0"]
    node_78["ast.JoinedStr object at 0x10616dc10"]
    node_79["ast.FormattedValue object at 0x10616dbe0"]
    node_80["ast.Name object at 0x10616dbb0"]
    node_81["ast.Load object at 0x1060500d0"]
    node_82["ast.Constant object at 0x10616db80"]
    node_83["ast.FormattedValue object at 0x10616db50"]
    node_84["ast.Attribute object at 0x10616db20"]
    node_85["ast.Name object at 0x10616daf0"]
    node_86["ast.Load object at 0x1060500d0"]
    node_87["ast.Load object at 0x1060500d0"]
    node_88["ast.Constant object at 0x10616da60"]
    node_89["ast.FunctionDef object at 0x10616da30"]
    node_90["ast.arguments object at 0x10616da00"]
    node_91["ast.arg object at 0x10616d9d0"]
    node_92["ast.Return object at 0x10616d9a0"]
    node_93["ast.Attribute object at 0x10615afa0"]
    node_94["ast.Name object at 0x10615af70"]
    node_95["ast.Load object at 0x1060500d0"]
    node_96["ast.Load object at 0x1060500d0"]
    node_97["ast.Subscript object at 0x10615aee0"]
    node_98["ast.Name object at 0x10615aeb0"]
    node_99["ast.Load object at 0x1060500d0"]
    node_100["ast.Name object at 0x10615af40"]
    node_101["ast.Load object at 0x1060500d0"]
    node_102["ast.Load object at 0x1060500d0"]
    node_103["ast.ClassDef object at 0x10615af10"]
    node_104["ast.Name object at 0x10615adf0"]
    node_105["ast.Load object at 0x1060500d0"]
    node_106["ast.FunctionDef object at 0x10615ae50"]
    node_107["ast.arguments object at 0x10615ae20"]
    node_108["ast.arg object at 0x10615ad60"]
    node_109["ast.AnnAssign object at 0x10615ad30"]
    node_110["ast.Attribute object at 0x10615adc0"]
    node_111["ast.Name object at 0x10615ad90"]
    node_112["ast.Load object at 0x1060500d0"]
    node_113["ast.Store object at 0x106050070"]
    node_114["ast.Subscript object at 0x10615ac70"]
    node_115["ast.Name object at 0x10615ac40"]
    node_116["ast.Load object at 0x1060500d0"]
    node_117["ast.Name object at 0x10615acd0"]
    node_118["ast.Load object at 0x1060500d0"]
    node_119["ast.Load object at 0x1060500d0"]
    node_120["ast.List object at 0x10615aca0"]
    node_121["ast.Load object at 0x1060500d0"]
    node_122["ast.AnnAssign object at 0x10615ab80"]
    node_123["ast.Attribute object at 0x10615a910"]
    node_124["ast.Name object at 0x10615abe0"]
    node_125["ast.Load object at 0x1060500d0"]
    node_126["ast.Store object at 0x106050070"]
    node_127["ast.Subscript object at 0x10615abb0"]
    node_128["ast.Name object at 0x10615aa30"]
    node_129["ast.Load object at 0x1060500d0"]
    node_130["ast.Name object at 0x10615a940"]
    node_131["ast.Load object at 0x1060500d0"]
    node_132["ast.Load object at 0x1060500d0"]
    node_133["ast.Constant object at 0x10615ab50"]
    node_134["ast.AnnAssign object at 0x10615ab20"]
    node_135["ast.Attribute object at 0x10615aa90"]
    node_136["ast.Name object at 0x10615aa60"]
    node_137["ast.Load object at 0x1060500d0"]
    node_138["ast.Store object at 0x106050070"]
    node_139["ast.Name object at 0x10615aaf0"]
    node_140["ast.Load object at 0x1060500d0"]
    node_141["ast.Constant object at 0x10615aac0"]
    node_142["ast.Constant object at 0x10615a9a0"]
    node_143["ast.FunctionDef object at 0x10615a970"]
    node_144["ast.arguments object at 0x10615aa00"]
    node_145["ast.arg object at 0x10615a9d0"]
    node_146["ast.arg object at 0x10615a400"]
    node_147["ast.Name object at 0x10615a310"]
    node_148["ast.Load object at 0x1060500d0"]
    node_149["ast.Pass object at 0x10615a8e0"]
    node_150["ast.Constant object at 0x10615a850"]
    node_151["ast.FunctionDef object at 0x10615a760"]
    node_152["ast.arguments object at 0x10615a8b0"]
    node_153["ast.arg object at 0x10615a880"]
    node_154["ast.arg object at 0x10615a7c0"]
    node_155["ast.Name object at 0x10615a790"]
    node_156["ast.Load object at 0x1060500d0"]
    node_157["ast.Pass object at 0x10615a820"]
    node_158["ast.Constant object at 0x10615a6d0"]
    node_159["ast.FunctionDef object at 0x10615a5e0"]
    node_160["ast.arguments object at 0x10615a730"]
    node_161["ast.arg object at 0x10615a700"]
    node_162["ast.arg object at 0x10615a640"]
    node_163["ast.Name object at 0x10615a610"]
    node_164["ast.Load object at 0x1060500d0"]
    node_165["ast.Assign object at 0x10615a670"]
    node_166["ast.Name object at 0x10615a550"]
    node_167["ast.Store object at 0x106050070"]
    node_168["ast.Call object at 0x10615a520"]
    node_169["ast.Name object at 0x10615a5b0"]
    node_170["ast.Load object at 0x1060500d0"]
    node_171["ast.keyword object at 0x10615a580"]
    node_172["ast.Name object at 0x10615a460"]
    node_173["ast.Load object at 0x1060500d0"]
    node_174["ast.keyword object at 0x10615a430"]
    node_175["ast.JoinedStr object at 0x10615a4c0"]
    node_176["ast.Constant object at 0x10615a490"]
    node_177["ast.FormattedValue object at 0x10615a370"]
    node_178["ast.Attribute object at 0x10615a340"]
    node_179["ast.Name object at 0x10615a3d0"]
    node_180["ast.Load object at 0x1060500d0"]
    node_181["ast.Load object at 0x1060500d0"]
    node_182["ast.AugAssign object at 0x10615a250"]
    node_183["ast.Attribute object at 0x10615a220"]
    node_184["ast.Name object at 0x10615a2b0"]
    node_185["ast.Load object at 0x1060500d0"]
    node_186["ast.Store object at 0x106050070"]
    node_187["ast.Add object at 0x106050760"]
    node_188["ast.Constant object at 0x10615a280"]
    node_189["ast.If object at 0x10615a0a0"]
    node_190["ast.Attribute object at 0x10615a1c0"]
    node_191["ast.Name object at 0x10615a190"]
    node_192["ast.Load object at 0x1060500d0"]
    node_193["ast.Load object at 0x1060500d0"]
    node_194["ast.Expr object at 0x10615a100"]
    node_195["ast.Call object at 0x10615a0d0"]
    node_196["ast.Attribute object at 0x10615a160"]
    node_197["ast.Attribute object at 0x10615a130"]
    node_198["ast.Name object at 0x10615a070"]
    node_199["ast.Load object at 0x1060500d0"]
    node_200["ast.Load object at 0x1060500d0"]
    node_201["ast.Load object at 0x1060500d0"]
    node_202["ast.Call object at 0x10615a040"]
    node_203["ast.Name object at 0x106159fd0"]
    node_204["ast.Load object at 0x1060500d0"]
    node_205["ast.keyword object at 0x106159fa0"]
    node_206["ast.Attribute object at 0x106159f70"]
    node_207["ast.Name object at 0x106159f40"]
    node_208["ast.Load object at 0x1060500d0"]
    node_209["ast.Load object at 0x1060500d0"]
    node_210["ast.keyword object at 0x106159f10"]
    node_211["ast.Name object at 0x106159ee0"]
    node_212["ast.Load object at 0x1060500d0"]
    node_213["ast.Assign object at 0x106159e80"]
    node_214["ast.Attribute object at 0x106159e50"]
    node_215["ast.Name object at 0x106159e20"]
    node_216["ast.Load object at 0x1060500d0"]
    node_217["ast.Store object at 0x106050070"]
    node_218["ast.Name object at 0x106159df0"]
    node_219["ast.Load object at 0x1060500d0"]
    node_220["ast.Return object at 0x106159dc0"]
    node_221["ast.Call object at 0x106159d90"]
    node_222["ast.Attribute object at 0x106159d60"]
    node_223["ast.Call object at 0x106159d30"]
    node_224["ast.Name object at 0x106159d00"]
    node_225["ast.Load object at 0x1060500d0"]
    node_226["ast.Load object at 0x1060500d0"]
    node_227["ast.Name object at 0x106159cd0"]
    node_228["ast.Load object at 0x1060500d0"]
    node_229["ast.Name object at 0x106159c70"]
    node_230["ast.Load object at 0x1060500d0"]
    node_231["ast.FunctionDef object at 0x106159c40"]
    node_232["ast.arguments object at 0x106159c10"]
    node_233["ast.arg object at 0x106159be0"]
    node_234["ast.Return object at 0x106159bb0"]
    node_235["ast.Attribute object at 0x106159b80"]
    node_236["ast.Name object at 0x106159b50"]
    node_237["ast.Load object at 0x1060500d0"]
    node_238["ast.Load object at 0x1060500d0"]
    node_239["ast.Subscript object at 0x106159af0"]
    node_240["ast.Name object at 0x106159ac0"]
    node_241["ast.Load object at 0x1060500d0"]
    node_242["ast.Name object at 0x106159a90"]
    node_243["ast.Load object at 0x1060500d0"]
    node_244["ast.Load object at 0x1060500d0"]

    node_0 --> node_1
    node_1 --> node_2
    node_2 --> node_3
    node_3 --> node_4
    node_4 --> node_5
    node_5 --> node_6
    node_6 --> node_7
    node_7 --> node_8
    node_8 --> node_9
    node_9 --> node_10
    node_10 --> node_11
    node_11 --> node_12
    node_12 --> node_13
    node_13 --> node_14
    node_14 --> node_15
    node_15 --> node_16
    node_16 --> node_17
    node_17 --> node_18
    node_18 --> node_19
    node_19 --> node_20
    node_20 --> node_21
    node_21 --> node_22
    node_22 --> node_23
    node_23 --> node_24
    node_24 --> node_25
    node_25 --> node_26
    node_26 --> node_27
    node_27 --> node_28
    node_28 --> node_29
    node_29 --> node_30
    node_30 --> node_31
    node_31 --> node_32
    node_32 --> node_33
    node_33 --> node_34
    node_34 --> node_35
    node_35 --> node_36
    node_36 --> node_37
    node_37 --> node_38
    node_38 --> node_39
    node_39 --> node_40
    node_40 --> node_41
    node_41 --> node_42
    node_42 --> node_43
    node_43 --> node_44
    node_44 --> node_45
    node_45 --> node_46
    node_46 --> node_47
    node_47 --> node_48
    node_48 --> node_49
    node_49 --> node_50
    node_50 --> node_51
    node_51 --> node_52
    node_52 --> node_53
    node_53 --> node_54
    node_54 --> node_55
    node_55 --> node_56
    node_56 --> node_57
    node_57 --> node_58
    node_58 --> node_59
    node_59 --> node_60
    node_60 --> node_61
    node_61 --> node_62
    node_62 --> node_63
    node_63 --> node_64
    node_64 --> node_65
    node_65 --> node_66
    node_66 --> node_67
    node_67 --> node_68
    node_68 --> node_69
    node_69 --> node_70
    node_70 --> node_71
    node_71 --> node_72
    node_72 --> node_73
    node_73 --> node_74
    node_74 --> node_75
    node_75 --> node_76
    node_76 --> node_77
    node_77 --> node_78
    node_78 --> node_79
    node_79 --> node_80
    node_80 --> node_81
    node_81 --> node_82
    node_82 --> node_83
    node_83 --> node_84
    node_84 --> node_85
    node_85 --> node_86
    node_86 --> node_87
    node_87 --> node_88
    node_88 --> node_89
    node_89 --> node_90
    node_90 --> node_91
    node_91 --> node_92
    node_92 --> node_93
    node_93 --> node_94
    node_94 --> node_95
    node_95 --> node_96
    node_96 --> node_97
    node_97 --> node_98
    node_98 --> node_99
    node_99 --> node_100
    node_100 --> node_101
    node_101 --> node_102
    node_102 --> node_103
    node_103 --> node_104
    node_104 --> node_105
    node_105 --> node_106
    node_106 --> node_107
    node_107 --> node_108
    node_108 --> node_109
    node_109 --> node_110
    node_110 --> node_111
    node_111 --> node_112
    node_112 --> node_113
    node_113 --> node_114
    node_114 --> node_115
    node_115 --> node_116
    node_116 --> node_117
    node_117 --> node_118
    node_118 --> node_119
    node_119 --> node_120
    node_120 --> node_121
    node_121 --> node_122
    node_122 --> node_123
    node_123 --> node_124
    node_124 --> node_125
    node_125 --> node_126
    node_126 --> node_127
    node_127 --> node_128
    node_128 --> node_129
    node_129 --> node_130
    node_130 --> node_131
    node_131 --> node_132
    node_132 --> node_133
    node_133 --> node_134
    node_134 --> node_135
    node_135 --> node_136
    node_136 --> node_137
    node_137 --> node_138
    node_138 --> node_139
    node_139 --> node_140
    node_140 --> node_141
    node_141 --> node_142
    node_142 --> node_143
    node_143 --> node_144
    node_144 --> node_145
    node_145 --> node_146
    node_146 --> node_147
    node_147 --> node_148
    node_148 --> node_149
    node_149 --> node_150
    node_150 --> node_151
    node_151 --> node_152
    node_152 --> node_153
    node_153 --> node_154
    node_154 --> node_155
    node_155 --> node_156
    node_156 --> node_157
    node_157 --> node_158
    node_158 --> node_159
    node_159 --> node_160
    node_160 --> node_161
    node_161 --> node_162
    node_162 --> node_163
    node_163 --> node_164
    node_164 --> node_165
    node_165 --> node_166
    node_166 --> node_167
    node_167 --> node_168
    node_168 --> node_169
    node_169 --> node_170
    node_170 --> node_171
    node_171 --> node_172
    node_172 --> node_173
    node_173 --> node_174
    node_174 --> node_175
    node_175 --> node_176
    node_176 --> node_177
    node_177 --> node_178
    node_178 --> node_179
    node_179 --> node_180
    node_180 --> node_181
    node_181 --> node_182
    node_182 --> node_183
    node_183 --> node_184
    node_184 --> node_185
    node_185 --> node_186
    node_186 --> node_187
    node_187 --> node_188
    node_188 --> node_189
    node_189 --> node_190
    node_190 --> node_191
    node_191 --> node_192
    node_192 --> node_193
    node_193 --> node_194
    node_194 --> node_195
    node_195 --> node_196
    node_196 --> node_197
    node_197 --> node_198
    node_198 --> node_199
    node_199 --> node_200
    node_200 --> node_201
    node_201 --> node_202
    node_202 --> node_203
    node_203 --> node_204
    node_204 --> node_205
    node_205 --> node_206
    node_206 --> node_207
    node_207 --> node_208
    node_208 --> node_209
    node_209 --> node_210
    node_210 --> node_211
    node_211 --> node_212
    node_212 --> node_213
    node_213 --> node_214
    node_214 --> node_215
    node_215 --> node_216
    node_216 --> node_217
    node_217 --> node_218
    node_218 --> node_219
    node_219 --> node_220
    node_220 --> node_221
    node_221 --> node_222
    node_222 --> node_223
    node_223 --> node_224
    node_224 --> node_225
    node_225 --> node_226
    node_226 --> node_227
    node_227 --> node_228
    node_228 --> node_229
    node_229 --> node_230
    node_230 --> node_231
    node_231 --> node_232
    node_232 --> node_233
    node_233 --> node_234
    node_234 --> node_235
    node_235 --> node_236
    node_236 --> node_237
    node_237 --> node_238
    node_238 --> node_239
    node_239 --> node_240
    node_240 --> node_241
    node_241 --> node_242
    node_242 --> node_243
    node_243 --> node_244

```
---

<details>
<summary>Debug AST model dump</summary>

```
Module(
  body=[
    ImportFrom(
      module='ast',
      names=[
        alias(name='AST'),
        alias(name='Import'),
        alias(name='ImportFrom'),
        alias(name='NodeVisitor')],
      level=0,
      lineno=1,
      col_offset=0,
      end_lineno=1,
      end_col_offset=52),
    ImportFrom(
      module='models',
      names=[
        alias(name='MermaidLink'),
        alias(name='MermaidNode')],
      level=0,
      lineno=2,
      col_offset=0,
      end_lineno=2,
      end_col_offset=43),
    ImportFrom(
      module='typing',
      names=[
        alias(name='Any'),
        alias(name='Optional')],
      level=0,
      lineno=3,
      col_offset=0,
      end_lineno=3,
      end_col_offset=32),
    ClassDef(
      name='ImportNodeFinder',
      bases=[
        Name(
          id='NodeVisitor',
          ctx=Load(),
          lineno=6,
          col_offset=23,
          end_lineno=6,
          end_col_offset=34)],
      keywords=[],
      body=[
        FunctionDef(
          name='__init__',
          args=arguments(
            posonlyargs=[],
            args=[
              arg(
                arg='self',
                lineno=7,
                col_offset=17,
                end_lineno=7,
                end_col_offset=21)],
            kwonlyargs=[],
            kw_defaults=[],
            defaults=[]),
          body=[
            AnnAssign(
              target=Attribute(
                value=Name(
                  id='self',
                  ctx=Load(),
                  lineno=8,
                  col_offset=8,
                  end_lineno=8,
                  end_col_offset=12),
                attr='found_imports',
                ctx=Store(),
                lineno=8,
                col_offset=8,
                end_lineno=8,
                end_col_offset=26),
              annotation=Subscript(
                value=Name(
                  id='list',
                  ctx=Load(),
                  lineno=8,
                  col_offset=29,
                  end_lineno=8,
                  end_col_offset=33),
                slice=Name(
                  id='str',
                  ctx=Load(),
                  lineno=8,
                  col_offset=34,
                  end_lineno=8,
                  end_col_offset=37),
                ctx=Load(),
                lineno=8,
                col_offset=29,
                end_lineno=8,
                end_col_offset=38),
              value=List(
                elts=[],
                ctx=Load(),
                lineno=8,
                col_offset=41,
                end_lineno=8,
                end_col_offset=43),
              simple=0,
              lineno=8,
              col_offset=8,
              end_lineno=8,
              end_col_offset=43)],
          decorator_list=[],
          returns=Constant(
            value=None,
            lineno=7,
            col_offset=26,
            end_lineno=7,
            end_col_offset=30),
          lineno=7,
          col_offset=4,
          end_lineno=8,
          end_col_offset=43),
        FunctionDef(
          name='visit_Import',
          args=arguments(
            posonlyargs=[],
            args=[
              arg(
                arg='self',
                lineno=10,
                col_offset=21,
                end_lineno=10,
                end_col_offset=25),
              arg(
                arg='node',
                annotation=Name(
                  id='Import',
                  ctx=Load(),
                  lineno=10,
                  col_offset=33,
                  end_lineno=10,
                  end_col_offset=39),
                lineno=10,
                col_offset=27,
                end_lineno=10,
                end_col_offset=39)],
            kwonlyargs=[],
            kw_defaults=[],
            defaults=[]),
          body=[
            For(
              target=Name(
                id='i',
                ctx=Store(),
                lineno=11,
                col_offset=12,
                end_lineno=11,
                end_col_offset=13),
              iter=Attribute(
                value=Name(
                  id='node',
                  ctx=Load(),
                  lineno=11,
                  col_offset=17,
                  end_lineno=11,
                  end_col_offset=21),
                attr='names',
                ctx=Load(),
                lineno=11,
                col_offset=17,
                end_lineno=11,
                end_col_offset=27),
              body=[
                Expr(
                  value=Call(
                    func=Attribute(
                      value=Attribute(
                        value=Name(
                          id='self',
                          ctx=Load(),
                          lineno=12,
                          col_offset=12,
                          end_lineno=12,
                          end_col_offset=16),
                        attr='found_imports',
                        ctx=Load(),
                        lineno=12,
                        col_offset=12,
                        end_lineno=12,
                        end_col_offset=30),
                      attr='append',
                      ctx=Load(),
                      lineno=12,
                      col_offset=12,
                      end_lineno=12,
                      end_col_offset=37),
                    args=[
                      JoinedStr(
                        values=[
                          FormattedValue(
                            value=Attribute(
                              value=Name(
                                id='i',
                                ctx=Load(),
                                lineno=12,
                                col_offset=41,
                                end_lineno=12,
                                end_col_offset=42),
                              attr='name',
                              ctx=Load(),
                              lineno=12,
                              col_offset=41,
                              end_lineno=12,
                              end_col_offset=47),
                            conversion=-1,
                            lineno=12,
                            col_offset=38,
                            end_lineno=12,
                            end_col_offset=51),
                          Constant(
                            value='.*',
                            lineno=12,
                            col_offset=38,
                            end_lineno=12,
                            end_col_offset=51)],
                        lineno=12,
                        col_offset=38,
                        end_lineno=12,
                        end_col_offset=51)],
                    keywords=[],
                    lineno=12,
                    col_offset=12,
                    end_lineno=12,
                    end_col_offset=52),
                  lineno=12,
                  col_offset=12,
                  end_lineno=12,
                  end_col_offset=52)],
              orelse=[],
              lineno=11,
              col_offset=8,
              end_lineno=12,
              end_col_offset=52)],
          decorator_list=[],
          returns=Constant(
            value=None,
            lineno=10,
            col_offset=44,
            end_lineno=10,
            end_col_offset=48),
          lineno=10,
          col_offset=4,
          end_lineno=12,
          end_col_offset=52),
        FunctionDef(
          name='visit_ImportFrom',
          args=arguments(
            posonlyargs=[],
            args=[
              arg(
                arg='self',
                lineno=14,
                col_offset=25,
                end_lineno=14,
                end_col_offset=29),
              arg(
                arg='node',
                annotation=Name(
                  id='ImportFrom',
                  ctx=Load(),
                  lineno=14,
                  col_offset=37,
                  end_lineno=14,
                  end_col_offset=47),
                lineno=14,
                col_offset=31,
                end_lineno=14,
                end_col_offset=47)],
            kwonlyargs=[],
            kw_defaults=[],
            defaults=[]),
          body=[
            Assign(
              targets=[
                Name(
                  id='module',
                  ctx=Store(),
                  lineno=15,
                  col_offset=8,
                  end_lineno=15,
                  end_col_offset=14)],
              value=Attribute(
                value=Name(
                  id='node',
                  ctx=Load(),
                  lineno=15,
                  col_offset=17,
                  end_lineno=15,
                  end_col_offset=21),
                attr='module',
                ctx=Load(),
                lineno=15,
                col_offset=17,
                end_lineno=15,
                end_col_offset=28),
              lineno=15,
              col_offset=8,
              end_lineno=15,
              end_col_offset=28),
            For(
              target=Name(
                id='i',
                ctx=Store(),
                lineno=16,
                col_offset=12,
                end_lineno=16,
                end_col_offset=13),
              iter=Attribute(
                value=Name(
                  id='node',
                  ctx=Load(),
                  lineno=16,
                  col_offset=17,
                  end_lineno=16,
                  end_col_offset=21),
                attr='names',
                ctx=Load(),
                lineno=16,
                col_offset=17,
                end_lineno=16,
                end_col_offset=27),
              body=[
                Expr(
                  value=Call(
                    func=Attribute(
                      value=Attribute(
                        value=Name(
                          id='self',
                          ctx=Load(),
                          lineno=17,
                          col_offset=12,
                          end_lineno=17,
                          end_col_offset=16),
                        attr='found_imports',
                        ctx=Load(),
                        lineno=17,
                        col_offset=12,
                        end_lineno=17,
                        end_col_offset=30),
                      attr='append',
                      ctx=Load(),
                      lineno=17,
                      col_offset=12,
                      end_lineno=17,
                      end_col_offset=37),
                    args=[
                      JoinedStr(
                        values=[
                          FormattedValue(
                            value=Name(
                              id='module',
                              ctx=Load(),
                              lineno=17,
                              col_offset=41,
                              end_lineno=17,
                              end_col_offset=47),
                            conversion=-1,
                            lineno=17,
                            col_offset=38,
                            end_lineno=17,
                            end_col_offset=58),
                          Constant(
                            value='.',
                            lineno=17,
                            col_offset=38,
                            end_lineno=17,
                            end_col_offset=58),
                          FormattedValue(
                            value=Attribute(
                              value=Name(
                                id='i',
                                ctx=Load(),
                                lineno=17,
                                col_offset=50,
                                end_lineno=17,
                                end_col_offset=51),
                              attr='name',
                              ctx=Load(),
                              lineno=17,
                              col_offset=50,
                              end_lineno=17,
                              end_col_offset=56),
                            conversion=-1,
                            lineno=17,
                            col_offset=38,
                            end_lineno=17,
                            end_col_offset=58)],
                        lineno=17,
                        col_offset=38,
                        end_lineno=17,
                        end_col_offset=58)],
                    keywords=[],
                    lineno=17,
                    col_offset=12,
                    end_lineno=17,
                    end_col_offset=59),
                  lineno=17,
                  col_offset=12,
                  end_lineno=17,
                  end_col_offset=59)],
              orelse=[],
              lineno=16,
              col_offset=8,
              end_lineno=17,
              end_col_offset=59)],
          decorator_list=[],
          returns=Constant(
            value=None,
            lineno=14,
            col_offset=52,
            end_lineno=14,
            end_col_offset=56),
          lineno=14,
          col_offset=4,
          end_lineno=17,
          end_col_offset=59),
        FunctionDef(
          name='get_found_imports',
          args=arguments(
            posonlyargs=[],
            args=[
              arg(
                arg='self',
                lineno=19,
                col_offset=26,
                end_lineno=19,
                end_col_offset=30)],
            kwonlyargs=[],
            kw_defaults=[],
            defaults=[]),
          body=[
            Return(
              value=Attribute(
                value=Name(
                  id='self',
                  ctx=Load(),
                  lineno=20,
                  col_offset=15,
                  end_lineno=20,
                  end_col_offset=19),
                attr='found_imports',
                ctx=Load(),
                lineno=20,
                col_offset=15,
                end_lineno=20,
                end_col_offset=33),
              lineno=20,
              col_offset=8,
              end_lineno=20,
              end_col_offset=33)],
          decorator_list=[],
          returns=Subscript(
            value=Name(
              id='list',
              ctx=Load(),
              lineno=19,
              col_offset=35,
              end_lineno=19,
              end_col_offset=39),
            slice=Name(
              id='str',
              ctx=Load(),
              lineno=19,
              col_offset=40,
              end_lineno=19,
              end_col_offset=43),
            ctx=Load(),
            lineno=19,
            col_offset=35,
            end_lineno=19,
            end_col_offset=44),
          lineno=19,
          col_offset=4,
          end_lineno=20,
          end_col_offset=33)],
      decorator_list=[],
      lineno=6,
      col_offset=0,
      end_lineno=20,
      end_col_offset=33),
    ClassDef(
      name='LinkGenerator',
      bases=[
        Name(
          id='NodeVisitor',
          ctx=Load(),
          lineno=23,
          col_offset=20,
          end_lineno=23,
          end_col_offset=31)],
      keywords=[],
      body=[
        FunctionDef(
          name='__init__',
          args=arguments(
            posonlyargs=[],
            args=[
              arg(
                arg='self',
                lineno=24,
                col_offset=17,
                end_lineno=24,
                end_col_offset=21)],
            kwonlyargs=[],
            kw_defaults=[],
            defaults=[]),
          body=[
            AnnAssign(
              target=Attribute(
                value=Name(
                  id='self',
                  ctx=Load(),
                  lineno=25,
                  col_offset=8,
                  end_lineno=25,
                  end_col_offset=12),
                attr='links',
                ctx=Store(),
                lineno=25,
                col_offset=8,
                end_lineno=25,
                end_col_offset=18),
              annotation=Subscript(
                value=Name(
                  id='list',
                  ctx=Load(),
                  lineno=25,
                  col_offset=21,
                  end_lineno=25,
                  end_col_offset=25),
                slice=Name(
                  id='MermaidLink',
                  ctx=Load(),
                  lineno=25,
                  col_offset=26,
                  end_lineno=25,
                  end_col_offset=37),
                ctx=Load(),
                lineno=25,
                col_offset=21,
                end_lineno=25,
                end_col_offset=38),
              value=List(
                elts=[],
                ctx=Load(),
                lineno=25,
                col_offset=41,
                end_lineno=25,
                end_col_offset=43),
              simple=0,
              lineno=25,
              col_offset=8,
              end_lineno=25,
              end_col_offset=43),
            AnnAssign(
              target=Attribute(
                value=Name(
                  id='self',
                  ctx=Load(),
                  lineno=26,
                  col_offset=8,
                  end_lineno=26,
                  end_col_offset=12),
                attr='prev_node',
                ctx=Store(),
                lineno=26,
                col_offset=8,
                end_lineno=26,
                end_col_offset=22),
              annotation=Subscript(
                value=Name(
                  id='Optional',
                  ctx=Load(),
                  lineno=26,
                  col_offset=25,
                  end_lineno=26,
                  end_col_offset=33),
                slice=Name(
                  id='AST',
                  ctx=Load(),
                  lineno=26,
                  col_offset=34,
                  end_lineno=26,
                  end_col_offset=37),
                ctx=Load(),
                lineno=26,
                col_offset=25,
                end_lineno=26,
                end_col_offset=38),
              value=Constant(
                value=None,
                lineno=26,
                col_offset=41,
                end_lineno=26,
                end_col_offset=45),
              simple=0,
              lineno=26,
              col_offset=8,
              end_lineno=26,
              end_col_offset=45),
            AnnAssign(
              target=Attribute(
                value=Name(
                  id='self',
                  ctx=Load(),
                  lineno=27,
                  col_offset=8,
                  end_lineno=27,
                  end_col_offset=12),
                attr='count',
                ctx=Store(),
                lineno=27,
                col_offset=8,
                end_lineno=27,
                end_col_offset=18),
              annotation=Name(
                id='int',
                ctx=Load(),
                lineno=27,
                col_offset=21,
                end_lineno=27,
                end_col_offset=24),
              value=Constant(
                value=0,
                lineno=27,
                col_offset=27,
                end_lineno=27,
                end_col_offset=28),
              simple=0,
              lineno=27,
              col_offset=8,
              end_lineno=27,
              end_col_offset=28)],
          decorator_list=[],
          returns=Constant(
            value=None,
            lineno=24,
            col_offset=26,
            end_lineno=24,
            end_col_offset=30),
          lineno=24,
          col_offset=4,
          end_lineno=27,
          end_col_offset=28),
        FunctionDef(
          name='visit_Import',
          args=arguments(
            posonlyargs=[],
            args=[
              arg(
                arg='self',
                lineno=29,
                col_offset=21,
                end_lineno=29,
                end_col_offset=25),
              arg(
                arg='node',
                annotation=Name(
                  id='Import',
                  ctx=Load(),
                  lineno=29,
                  col_offset=33,
                  end_lineno=29,
                  end_col_offset=39),
                lineno=29,
                col_offset=27,
                end_lineno=29,
                end_col_offset=39)],
            kwonlyargs=[],
            kw_defaults=[],
            defaults=[]),
          body=[
            Pass(
              lineno=30,
              col_offset=8,
              end_lineno=30,
              end_col_offset=12)],
          decorator_list=[],
          returns=Constant(
            value=None,
            lineno=29,
            col_offset=44,
            end_lineno=29,
            end_col_offset=48),
          lineno=29,
          col_offset=4,
          end_lineno=30,
          end_col_offset=12),
        FunctionDef(
          name='visit_ImportFrom',
          args=arguments(
            posonlyargs=[],
            args=[
              arg(
                arg='self',
                lineno=32,
                col_offset=25,
                end_lineno=32,
                end_col_offset=29),
              arg(
                arg='node',
                annotation=Name(
                  id='ImportFrom',
                  ctx=Load(),
                  lineno=32,
                  col_offset=37,
                  end_lineno=32,
                  end_col_offset=47),
                lineno=32,
                col_offset=31,
                end_lineno=32,
                end_col_offset=47)],
            kwonlyargs=[],
            kw_defaults=[],
            defaults=[]),
          body=[
            Pass(
              lineno=33,
              col_offset=8,
              end_lineno=33,
              end_col_offset=12)],
          decorator_list=[],
          returns=Constant(
            value=None,
            lineno=32,
            col_offset=52,
            end_lineno=32,
            end_col_offset=56),
          lineno=32,
          col_offset=4,
          end_lineno=33,
          end_col_offset=12),
        FunctionDef(
          name='generic_visit',
          args=arguments(
            posonlyargs=[],
            args=[
              arg(
                arg='self',
                lineno=35,
                col_offset=22,
                end_lineno=35,
                end_col_offset=26),
              arg(
                arg='node',
                annotation=Name(
                  id='AST',
                  ctx=Load(),
                  lineno=35,
                  col_offset=34,
                  end_lineno=35,
                  end_col_offset=37),
                lineno=35,
                col_offset=28,
                end_lineno=35,
                end_col_offset=37)],
            kwonlyargs=[],
            kw_defaults=[],
            defaults=[]),
          body=[
            Assign(
              targets=[
                Name(
                  id='mermaid_data',
                  ctx=Store(),
                  lineno=36,
                  col_offset=8,
                  end_lineno=36,
                  end_col_offset=20)],
              value=Call(
                func=Name(
                  id='MermaidNode',
                  ctx=Load(),
                  lineno=36,
                  col_offset=23,
                  end_lineno=36,
                  end_col_offset=34),
                args=[],
                keywords=[
                  keyword(
                    arg='ast_node',
                    value=Name(
                      id='node',
                      ctx=Load(),
                      lineno=37,
                      col_offset=21,
                      end_lineno=37,
                      end_col_offset=25),
                    lineno=37,
                    col_offset=12,
                    end_lineno=37,
                    end_col_offset=25),
                  keyword(
                    arg='mermaid_safe_name',
                    value=JoinedStr(
                      values=[
                        Constant(
                          value='node_',
                          lineno=38,
                          col_offset=30,
                          end_lineno=38,
                          end_col_offset=50),
                        FormattedValue(
                          value=Attribute(
                            value=Name(
                              id='self',
                              ctx=Load(),
                              lineno=38,
                              col_offset=38,
                              end_lineno=38,
                              end_col_offset=42),
                            attr='count',
                            ctx=Load(),
                            lineno=38,
                            col_offset=38,
                            end_lineno=38,
                            end_col_offset=48),
                          conversion=-1,
                          lineno=38,
                          col_offset=30,
                          end_lineno=38,
                          end_col_offset=50)],
                      lineno=38,
                      col_offset=30,
                      end_lineno=38,
                      end_col_offset=50),
                    lineno=38,
                    col_offset=12,
                    end_lineno=38,
                    end_col_offset=50)],
                lineno=36,
                col_offset=23,
                end_lineno=39,
                end_col_offset=9),
              lineno=36,
              col_offset=8,
              end_lineno=39,
              end_col_offset=9),
            AugAssign(
              target=Attribute(
                value=Name(
                  id='self',
                  ctx=Load(),
                  lineno=40,
                  col_offset=8,
                  end_lineno=40,
                  end_col_offset=12),
                attr='count',
                ctx=Store(),
                lineno=40,
                col_offset=8,
                end_lineno=40,
                end_col_offset=18),
              op=Add(),
              value=Constant(
                value=1,
                lineno=40,
                col_offset=22,
                end_lineno=40,
                end_col_offset=23),
              lineno=40,
              col_offset=8,
              end_lineno=40,
              end_col_offset=23),
            If(
              test=Attribute(
                value=Name(
                  id='self',
                  ctx=Load(),
                  lineno=41,
                  col_offset=11,
                  end_lineno=41,
                  end_col_offset=15),
                attr='prev_node',
                ctx=Load(),
                lineno=41,
                col_offset=11,
                end_lineno=41,
                end_col_offset=25),
              body=[
                Expr(
                  value=Call(
                    func=Attribute(
                      value=Attribute(
                        value=Name(
                          id='self',
                          ctx=Load(),
                          lineno=42,
                          col_offset=12,
                          end_lineno=42,
                          end_col_offset=16),
                        attr='links',
                        ctx=Load(),
                        lineno=42,
                        col_offset=12,
                        end_lineno=42,
                        end_col_offset=22),
                      attr='append',
                      ctx=Load(),
                      lineno=42,
                      col_offset=12,
                      end_lineno=42,
                      end_col_offset=29),
                    args=[
                      Call(
                        func=Name(
                          id='MermaidLink',
                          ctx=Load(),
                          lineno=42,
                          col_offset=30,
                          end_lineno=42,
                          end_col_offset=41),
                        args=[],
                        keywords=[
                          keyword(
                            arg='from_',
                            value=Attribute(
                              value=Name(
                                id='self',
                                ctx=Load(),
                                lineno=42,
                                col_offset=48,
                                end_lineno=42,
                                end_col_offset=52),
                              attr='prev_node',
                              ctx=Load(),
                              lineno=42,
                              col_offset=48,
                              end_lineno=42,
                              end_col_offset=62),
                            lineno=42,
                            col_offset=42,
                            end_lineno=42,
                            end_col_offset=62),
                          keyword(
                            arg='to',
                            value=Name(
                              id='mermaid_data',
                              ctx=Load(),
                              lineno=42,
                              col_offset=67,
                              end_lineno=42,
                              end_col_offset=79),
                            lineno=42,
                            col_offset=64,
                            end_lineno=42,
                            end_col_offset=79)],
                        lineno=42,
                        col_offset=30,
                        end_lineno=42,
                        end_col_offset=80)],
                    keywords=[],
                    lineno=42,
                    col_offset=12,
                    end_lineno=42,
                    end_col_offset=81),
                  lineno=42,
                  col_offset=12,
                  end_lineno=42,
                  end_col_offset=81)],
              orelse=[],
              lineno=41,
              col_offset=8,
              end_lineno=42,
              end_col_offset=81),
            Assign(
              targets=[
                Attribute(
                  value=Name(
                    id='self',
                    ctx=Load(),
                    lineno=43,
                    col_offset=8,
                    end_lineno=43,
                    end_col_offset=12),
                  attr='prev_node',
                  ctx=Store(),
                  lineno=43,
                  col_offset=8,
                  end_lineno=43,
                  end_col_offset=22)],
              value=Name(
                id='mermaid_data',
                ctx=Load(),
                lineno=43,
                col_offset=25,
                end_lineno=43,
                end_col_offset=37),
              lineno=43,
              col_offset=8,
              end_lineno=43,
              end_col_offset=37),
            Return(
              value=Call(
                func=Attribute(
                  value=Call(
                    func=Name(
                      id='super',
                      ctx=Load(),
                      lineno=46,
                      col_offset=15,
                      end_lineno=46,
                      end_col_offset=20),
                    args=[],
                    keywords=[],
                    lineno=46,
                    col_offset=15,
                    end_lineno=46,
                    end_col_offset=22),
                  attr='generic_visit',
                  ctx=Load(),
                  lineno=46,
                  col_offset=15,
                  end_lineno=46,
                  end_col_offset=36),
                args=[
                  Name(
                    id='node',
                    ctx=Load(),
                    lineno=46,
                    col_offset=37,
                    end_lineno=46,
                    end_col_offset=41)],
                keywords=[],
                lineno=46,
                col_offset=15,
                end_lineno=46,
                end_col_offset=42),
              lineno=46,
              col_offset=8,
              end_lineno=46,
              end_col_offset=42)],
          decorator_list=[],
          returns=Name(
            id='Any',
            ctx=Load(),
            lineno=35,
            col_offset=42,
            end_lineno=35,
            end_col_offset=45),
          lineno=35,
          col_offset=4,
          end_lineno=46,
          end_col_offset=42),
        FunctionDef(
          name='get_list_of_links',
          args=arguments(
            posonlyargs=[],
            args=[
              arg(
                arg='self',
                lineno=48,
                col_offset=26,
                end_lineno=48,
                end_col_offset=30)],
            kwonlyargs=[],
            kw_defaults=[],
            defaults=[]),
          body=[
            Return(
              value=Attribute(
                value=Name(
                  id='self',
                  ctx=Load(),
                  lineno=49,
                  col_offset=15,
                  end_lineno=49,
                  end_col_offset=19),
                attr='links',
                ctx=Load(),
                lineno=49,
                col_offset=15,
                end_lineno=49,
                end_col_offset=25),
              lineno=49,
              col_offset=8,
              end_lineno=49,
              end_col_offset=25)],
          decorator_list=[],
          returns=Subscript(
            value=Name(
              id='list',
              ctx=Load(),
              lineno=48,
              col_offset=35,
              end_lineno=48,
              end_col_offset=39),
            slice=Name(
              id='MermaidLink',
              ctx=Load(),
              lineno=48,
              col_offset=40,
              end_lineno=48,
              end_col_offset=51),
            ctx=Load(),
            lineno=48,
            col_offset=35,
            end_lineno=48,
            end_col_offset=52),
          lineno=48,
          col_offset=4,
          end_lineno=49,
          end_col_offset=25)],
      decorator_list=[],
      lineno=23,
      col_offset=0,
      end_lineno=49,
      end_col_offset=25)],
  type_ignores=[])
```
</details>
