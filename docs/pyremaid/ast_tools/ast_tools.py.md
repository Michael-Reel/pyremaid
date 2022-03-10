# ./src/pyremaid/ast_tools/ast_tools.py

### Imports

  - ast.AST
  - ast.dump
  - ast.parse
  - typing.Optional
  - ast_tools.visitors.ImportNodeFinder
  - ast_tools.visitors.LinkGenerator
  - models.MermaidLink

---
```mermaid
flowchart TB
    node_0["ast.Module object at 0x10613e760"]
    node_1["ast.FunctionDef object at 0x10613e190"]
    node_2["ast.arguments object at 0x10613e640"]
    node_3["ast.arg object at 0x10613e700"]
    node_4["ast.Name object at 0x10613e070"]
    node_5["ast.Load object at 0x1060500d0"]
    node_6["ast.arg object at 0x10613eb80"]
    node_7["ast.Name object at 0x10613e3d0"]
    node_8["ast.Load object at 0x1060500d0"]
    node_9["ast.Return object at 0x10613e220"]
    node_10["ast.Call object at 0x10613ec40"]
    node_11["ast.Name object at 0x10613efa0"]
    node_12["ast.Load object at 0x1060500d0"]
    node_13["ast.keyword object at 0x10613ea60"]
    node_14["ast.Name object at 0x10613ef70"]
    node_15["ast.Load object at 0x1060500d0"]
    node_16["ast.keyword object at 0x10613e0d0"]
    node_17["ast.Name object at 0x10613e6a0"]
    node_18["ast.Load object at 0x1060500d0"]
    node_19["ast.keyword object at 0x10613ea30"]
    node_20["ast.Constant object at 0x10613e280"]
    node_21["ast.keyword object at 0x10613e2b0"]
    node_22["ast.Constant object at 0x10613e9d0"]
    node_23["ast.Subscript object at 0x10613e460"]
    node_24["ast.Name object at 0x10613e130"]
    node_25["ast.Load object at 0x1060500d0"]
    node_26["ast.Name object at 0x10613e9a0"]
    node_27["ast.Load object at 0x1060500d0"]
    node_28["ast.Load object at 0x1060500d0"]
    node_29["ast.FunctionDef object at 0x10613efd0"]
    node_30["ast.arguments object at 0x10613e850"]
    node_31["ast.arg object at 0x10613e3a0"]
    node_32["ast.Name object at 0x10613eac0"]
    node_33["ast.Load object at 0x1060500d0"]
    node_34["ast.Return object at 0x10613e970"]
    node_35["ast.Call object at 0x10613eaf0"]
    node_36["ast.Name object at 0x10613e550"]
    node_37["ast.Load object at 0x1060500d0"]
    node_38["ast.Name object at 0x10613e670"]
    node_39["ast.Load object at 0x1060500d0"]
    node_40["ast.keyword object at 0x10613eb20"]
    node_41["ast.Constant object at 0x10613e730"]
    node_42["ast.keyword object at 0x10613e400"]
    node_43["ast.Constant object at 0x10613e4c0"]
    node_44["ast.keyword object at 0x10613e940"]
    node_45["ast.Constant object at 0x10613ebe0"]
    node_46["ast.Name object at 0x10613e5e0"]
    node_47["ast.Load object at 0x1060500d0"]
    node_48["ast.FunctionDef object at 0x10613e6d0"]
    node_49["ast.arguments object at 0x10613e2e0"]
    node_50["ast.arg object at 0x10613e5b0"]
    node_51["ast.Name object at 0x10613e430"]
    node_52["ast.Load object at 0x1060500d0"]
    node_53["ast.Assign object at 0x10613e340"]
    node_54["ast.Name object at 0x10613e8e0"]
    node_55["ast.Store object at 0x106050070"]
    node_56["ast.Call object at 0x10613eb50"]
    node_57["ast.Name object at 0x10613e910"]
    node_58["ast.Load object at 0x1060500d0"]
    node_59["ast.Expr object at 0x10613e580"]
    node_60["ast.Call object at 0x10613e310"]
    node_61["ast.Attribute object at 0x10613ed00"]
    node_62["ast.Name object at 0x10613e160"]
    node_63["ast.Load object at 0x1060500d0"]
    node_64["ast.Load object at 0x1060500d0"]
    node_65["ast.Name object at 0x106155b80"]
    node_66["ast.Load object at 0x1060500d0"]
    node_67["ast.Return object at 0x1061559d0"]
    node_68["ast.Call object at 0x106155d60"]
    node_69["ast.Attribute object at 0x1061552b0"]
    node_70["ast.Name object at 0x106155070"]
    node_71["ast.Load object at 0x1060500d0"]
    node_72["ast.Load object at 0x1060500d0"]
    node_73["ast.Subscript object at 0x106155310"]
    node_74["ast.Name object at 0x106155eb0"]
    node_75["ast.Load object at 0x1060500d0"]
    node_76["ast.Name object at 0x106155f10"]
    node_77["ast.Load object at 0x1060500d0"]
    node_78["ast.Load object at 0x1060500d0"]
    node_79["ast.FunctionDef object at 0x106155e20"]
    node_80["ast.arguments object at 0x106155430"]
    node_81["ast.arg object at 0x106155fd0"]
    node_82["ast.Name object at 0x106155160"]
    node_83["ast.Load object at 0x1060500d0"]
    node_84["ast.Assign object at 0x106155580"]
    node_85["ast.Name object at 0x1061557f0"]
    node_86["ast.Store object at 0x106050070"]
    node_87["ast.Call object at 0x106155e50"]
    node_88["ast.Name object at 0x106155610"]
    node_89["ast.Load object at 0x1060500d0"]
    node_90["ast.Expr object at 0x1061555b0"]
    node_91["ast.Call object at 0x106155940"]
    node_92["ast.Attribute object at 0x106155670"]
    node_93["ast.Name object at 0x106155190"]
    node_94["ast.Load object at 0x1060500d0"]
    node_95["ast.Load object at 0x1060500d0"]
    node_96["ast.keyword object at 0x1061551f0"]
    node_97["ast.Name object at 0x1061550d0"]
    node_98["ast.Load object at 0x1060500d0"]
    node_99["ast.Return object at 0x106155220"]
    node_100["ast.Call object at 0x106155460"]
    node_101["ast.Attribute object at 0x106155040"]
    node_102["ast.Name object at 0x106155400"]
    node_103["ast.Load object at 0x1060500d0"]
    node_104["ast.Load object at 0x1060500d0"]
    node_105["ast.Subscript object at 0x106155910"]
    node_106["ast.Name object at 0x106155340"]
    node_107["ast.Load object at 0x1060500d0"]
    node_108["ast.Name object at 0x106155280"]
    node_109["ast.Load object at 0x1060500d0"]
    node_110["ast.Load object at 0x1060500d0"]

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
        alias(name='dump'),
        alias(name='parse')],
      level=0,
      lineno=1,
      col_offset=0,
      end_lineno=1,
      end_col_offset=32),
    ImportFrom(
      module='typing',
      names=[
        alias(name='Optional')],
      level=0,
      lineno=2,
      col_offset=0,
      end_lineno=2,
      end_col_offset=27),
    ImportFrom(
      module='ast_tools.visitors',
      names=[
        alias(name='ImportNodeFinder'),
        alias(name='LinkGenerator')],
      level=0,
      lineno=4,
      col_offset=0,
      end_lineno=4,
      end_col_offset=62),
    ImportFrom(
      module='models',
      names=[
        alias(name='MermaidLink')],
      level=0,
      lineno=5,
      col_offset=0,
      end_lineno=5,
      end_col_offset=30),
    FunctionDef(
      name='get_ast_root_node_for_file',
      args=arguments(
        posonlyargs=[],
        args=[
          arg(
            arg='source_code',
            annotation=Name(
              id='str',
              ctx=Load(),
              lineno=8,
              col_offset=44,
              end_lineno=8,
              end_col_offset=47),
            lineno=8,
            col_offset=31,
            end_lineno=8,
            end_col_offset=47),
          arg(
            arg='input_file',
            annotation=Name(
              id='str',
              ctx=Load(),
              lineno=8,
              col_offset=61,
              end_lineno=8,
              end_col_offset=64),
            lineno=8,
            col_offset=49,
            end_lineno=8,
            end_col_offset=64)],
        kwonlyargs=[],
        kw_defaults=[],
        defaults=[]),
      body=[
        Return(
          value=Call(
            func=Name(
              id='parse',
              ctx=Load(),
              lineno=9,
              col_offset=11,
              end_lineno=9,
              end_col_offset=16),
            args=[],
            keywords=[
              keyword(
                arg='source',
                value=Name(
                  id='source_code',
                  ctx=Load(),
                  lineno=10,
                  col_offset=15,
                  end_lineno=10,
                  end_col_offset=26),
                lineno=10,
                col_offset=8,
                end_lineno=10,
                end_col_offset=26),
              keyword(
                arg='filename',
                value=Name(
                  id='input_file',
                  ctx=Load(),
                  lineno=11,
                  col_offset=17,
                  end_lineno=11,
                  end_col_offset=27),
                lineno=11,
                col_offset=8,
                end_lineno=11,
                end_col_offset=27),
              keyword(
                arg='mode',
                value=Constant(
                  value='exec',
                  lineno=12,
                  col_offset=13,
                  end_lineno=12,
                  end_col_offset=19),
                lineno=12,
                col_offset=8,
                end_lineno=12,
                end_col_offset=19),
              keyword(
                arg='type_comments',
                value=Constant(
                  value=True,
                  lineno=13,
                  col_offset=22,
                  end_lineno=13,
                  end_col_offset=26),
                lineno=13,
                col_offset=8,
                end_lineno=13,
                end_col_offset=26)],
            lineno=9,
            col_offset=11,
            end_lineno=14,
            end_col_offset=5),
          lineno=9,
          col_offset=4,
          end_lineno=14,
          end_col_offset=5)],
      decorator_list=[],
      returns=Subscript(
        value=Name(
          id='Optional',
          ctx=Load(),
          lineno=8,
          col_offset=69,
          end_lineno=8,
          end_col_offset=77),
        slice=Name(
          id='AST',
          ctx=Load(),
          lineno=8,
          col_offset=78,
          end_lineno=8,
          end_col_offset=81),
        ctx=Load(),
        lineno=8,
        col_offset=69,
        end_lineno=8,
        end_col_offset=82),
      lineno=8,
      col_offset=0,
      end_lineno=14,
      end_col_offset=5),
    FunctionDef(
      name='get_markdown_dump_for_ast_node',
      args=arguments(
        posonlyargs=[],
        args=[
          arg(
            arg='ast_node',
            annotation=Name(
              id='AST',
              ctx=Load(),
              lineno=17,
              col_offset=45,
              end_lineno=17,
              end_col_offset=48),
            lineno=17,
            col_offset=35,
            end_lineno=17,
            end_col_offset=48)],
        kwonlyargs=[],
        kw_defaults=[],
        defaults=[]),
      body=[
        Return(
          value=Call(
            func=Name(
              id='dump',
              ctx=Load(),
              lineno=18,
              col_offset=11,
              end_lineno=18,
              end_col_offset=15),
            args=[
              Name(
                id='ast_node',
                ctx=Load(),
                lineno=18,
                col_offset=16,
                end_lineno=18,
                end_col_offset=24)],
            keywords=[
              keyword(
                arg='annotate_fields',
                value=Constant(
                  value=True,
                  lineno=18,
                  col_offset=42,
                  end_lineno=18,
                  end_col_offset=46),
                lineno=18,
                col_offset=26,
                end_lineno=18,
                end_col_offset=46),
              keyword(
                arg='include_attributes',
                value=Constant(
                  value=True,
                  lineno=18,
                  col_offset=67,
                  end_lineno=18,
                  end_col_offset=71),
                lineno=18,
                col_offset=48,
                end_lineno=18,
                end_col_offset=71),
              keyword(
                arg='indent',
                value=Constant(
                  value=2,
                  lineno=18,
                  col_offset=80,
                  end_lineno=18,
                  end_col_offset=81),
                lineno=18,
                col_offset=73,
                end_lineno=18,
                end_col_offset=81)],
            lineno=18,
            col_offset=11,
            end_lineno=18,
            end_col_offset=82),
          lineno=18,
          col_offset=4,
          end_lineno=18,
          end_col_offset=82)],
      decorator_list=[],
      returns=Name(
        id='str',
        ctx=Load(),
        lineno=17,
        col_offset=53,
        end_lineno=17,
        end_col_offset=56),
      lineno=17,
      col_offset=0,
      end_lineno=18,
      end_col_offset=82),
    FunctionDef(
      name='get_used_import_list',
      args=arguments(
        posonlyargs=[],
        args=[
          arg(
            arg='ast_node',
            annotation=Name(
              id='AST',
              ctx=Load(),
              lineno=21,
              col_offset=35,
              end_lineno=21,
              end_col_offset=38),
            lineno=21,
            col_offset=25,
            end_lineno=21,
            end_col_offset=38)],
        kwonlyargs=[],
        kw_defaults=[],
        defaults=[]),
      body=[
        Assign(
          targets=[
            Name(
              id='finder',
              ctx=Store(),
              lineno=22,
              col_offset=4,
              end_lineno=22,
              end_col_offset=10)],
          value=Call(
            func=Name(
              id='ImportNodeFinder',
              ctx=Load(),
              lineno=22,
              col_offset=13,
              end_lineno=22,
              end_col_offset=29),
            args=[],
            keywords=[],
            lineno=22,
            col_offset=13,
            end_lineno=22,
            end_col_offset=31),
          lineno=22,
          col_offset=4,
          end_lineno=22,
          end_col_offset=31),
        Expr(
          value=Call(
            func=Attribute(
              value=Name(
                id='finder',
                ctx=Load(),
                lineno=23,
                col_offset=4,
                end_lineno=23,
                end_col_offset=10),
              attr='visit',
              ctx=Load(),
              lineno=23,
              col_offset=4,
              end_lineno=23,
              end_col_offset=16),
            args=[
              Name(
                id='ast_node',
                ctx=Load(),
                lineno=23,
                col_offset=17,
                end_lineno=23,
                end_col_offset=25)],
            keywords=[],
            lineno=23,
            col_offset=4,
            end_lineno=23,
            end_col_offset=26),
          lineno=23,
          col_offset=4,
          end_lineno=23,
          end_col_offset=26),
        Return(
          value=Call(
            func=Attribute(
              value=Name(
                id='finder',
                ctx=Load(),
                lineno=24,
                col_offset=11,
                end_lineno=24,
                end_col_offset=17),
              attr='get_found_imports',
              ctx=Load(),
              lineno=24,
              col_offset=11,
              end_lineno=24,
              end_col_offset=35),
            args=[],
            keywords=[],
            lineno=24,
            col_offset=11,
            end_lineno=24,
            end_col_offset=37),
          lineno=24,
          col_offset=4,
          end_lineno=24,
          end_col_offset=37)],
      decorator_list=[],
      returns=Subscript(
        value=Name(
          id='list',
          ctx=Load(),
          lineno=21,
          col_offset=43,
          end_lineno=21,
          end_col_offset=47),
        slice=Name(
          id='str',
          ctx=Load(),
          lineno=21,
          col_offset=48,
          end_lineno=21,
          end_col_offset=51),
        ctx=Load(),
        lineno=21,
        col_offset=43,
        end_lineno=21,
        end_col_offset=52),
      lineno=21,
      col_offset=0,
      end_lineno=24,
      end_col_offset=37),
    FunctionDef(
      name='create_links_from_ast_model',
      args=arguments(
        posonlyargs=[],
        args=[
          arg(
            arg='model',
            annotation=Name(
              id='AST',
              ctx=Load(),
              lineno=27,
              col_offset=39,
              end_lineno=27,
              end_col_offset=42),
            lineno=27,
            col_offset=32,
            end_lineno=27,
            end_col_offset=42)],
        kwonlyargs=[],
        kw_defaults=[],
        defaults=[]),
      body=[
        Assign(
          targets=[
            Name(
              id='link_generator',
              ctx=Store(),
              lineno=28,
              col_offset=4,
              end_lineno=28,
              end_col_offset=18)],
          value=Call(
            func=Name(
              id='LinkGenerator',
              ctx=Load(),
              lineno=28,
              col_offset=21,
              end_lineno=28,
              end_col_offset=34),
            args=[],
            keywords=[],
            lineno=28,
            col_offset=21,
            end_lineno=28,
            end_col_offset=36),
          lineno=28,
          col_offset=4,
          end_lineno=28,
          end_col_offset=36),
        Expr(
          value=Call(
            func=Attribute(
              value=Name(
                id='link_generator',
                ctx=Load(),
                lineno=29,
                col_offset=4,
                end_lineno=29,
                end_col_offset=18),
              attr='visit',
              ctx=Load(),
              lineno=29,
              col_offset=4,
              end_lineno=29,
              end_col_offset=24),
            args=[],
            keywords=[
              keyword(
                arg='node',
                value=Name(
                  id='model',
                  ctx=Load(),
                  lineno=29,
                  col_offset=30,
                  end_lineno=29,
                  end_col_offset=35),
                lineno=29,
                col_offset=25,
                end_lineno=29,
                end_col_offset=35)],
            lineno=29,
            col_offset=4,
            end_lineno=29,
            end_col_offset=36),
          lineno=29,
          col_offset=4,
          end_lineno=29,
          end_col_offset=36),
        Return(
          value=Call(
            func=Attribute(
              value=Name(
                id='link_generator',
                ctx=Load(),
                lineno=30,
                col_offset=11,
                end_lineno=30,
                end_col_offset=25),
              attr='get_list_of_links',
              ctx=Load(),
              lineno=30,
              col_offset=11,
              end_lineno=30,
              end_col_offset=43),
            args=[],
            keywords=[],
            lineno=30,
            col_offset=11,
            end_lineno=30,
            end_col_offset=45),
          lineno=30,
          col_offset=4,
          end_lineno=30,
          end_col_offset=45)],
      decorator_list=[],
      returns=Subscript(
        value=Name(
          id='list',
          ctx=Load(),
          lineno=27,
          col_offset=47,
          end_lineno=27,
          end_col_offset=51),
        slice=Name(
          id='MermaidLink',
          ctx=Load(),
          lineno=27,
          col_offset=52,
          end_lineno=27,
          end_col_offset=63),
        ctx=Load(),
        lineno=27,
        col_offset=47,
        end_lineno=27,
        end_col_offset=64),
      lineno=27,
      col_offset=0,
      end_lineno=30,
      end_col_offset=45)],
  type_ignores=[])
```
</details>
