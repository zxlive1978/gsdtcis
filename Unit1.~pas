unit Unit1;

interface

uses
  Windows, Messages, SysUtils, Variants, Classes, Graphics, Controls, Forms,
  Dialogs, Grids, DBGrids, DB, DBTables, StdCtrls, Menus, FileCtrl, Math,
  ValEdit, ComCtrls, DBCtrls, DateUtils, IniFiles, Buttons, ExtCtrls;

type
  TForm1 = class(TForm)
    PageControl1: TPageControl;
    TabSheet1: TTabSheet;
    TabSheet2: TTabSheet;
    Table1: TTable;
    DataSource1: TDataSource;
    OpenDialog1: TOpenDialog;
    DataSource2: TDataSource;
    Table2: TTable;
    Table3: TTable;
    DBGrid3: TDBGrid;
    Table3GID1: TSmallintField;
    Table3GID2: TSmallintField;
    Table3RAZREZ: TStringField;
    Table3IMS: TStringField;
    Table3KOEF: TFloatField;
    StatusBar1: TStatusBar;
    DataSource3: TDataSource;
    Button8: TButton;
    Button9: TButton;
    TabSheet3: TTabSheet;
    GroupBox1: TGroupBox;
    Button11: TButton;
    Label7: TLabel;
    TabSheet4: TTabSheet;
    Button3: TButton;
    Memo2: TMemo;
    Button2: TButton;
    Memo4: TMemo;
    Button5: TButton;
    Button4: TButton;
    Memo3: TMemo;
    ComboBoxEx1: TComboBoxEx;
    Button1: TButton;
    DBGrid1: TDBGrid;
    GroupBox2: TGroupBox;
    Memo1: TMemo;
    ComboBox1: TComboBox;
    Button10: TButton;
    ListBox2: TListBox;
    ProgressBar1: TProgressBar;
    Edit1: TEdit;
    GroupBox3: TGroupBox;
    Label6: TLabel;
    Edit2: TEdit;
    Button12: TButton;
    GroupBox4: TGroupBox;
    ListBox3: TListBox;
    Button13: TButton;
    ProgressBar2: TProgressBar;
    Label2: TLabel;
    Label3: TLabel;
    Label4: TLabel;
    Label5: TLabel;
    Label1: TLabel;
    TabSheet5: TTabSheet;
    DBGrid2: TDBGrid;
    Button6: TButton;
    ListBox1: TListBox;
    Memo5: TMemo;
    DBComboBox1: TDBComboBox;
    DBText1: TDBText;
    Button7: TButton;
    TabSheet6: TTabSheet;
    DataSource4: TDataSource;
    Table4: TTable;
    DBGrid4: TDBGrid;
    GroupBox5: TGroupBox;
    Button14: TButton;
    ProgressBar3: TProgressBar;
    TabSheet7: TTabSheet;
    DBGrid5: TDBGrid;
    DataSource5: TDataSource;
    Table5: TTable;
    ListBox4: TListBox;
    ListBox5: TListBox;
    GroupBox6: TGroupBox;
    Edit3: TEdit;
    Label8: TLabel;
    CheckBox1: TCheckBox;
    Edit4: TEdit;
    CheckBox2: TCheckBox;
    CheckBox3: TCheckBox;
    Timer1: TTimer;
    Timer2: TTimer;
    ComboBox2: TComboBox;
    Label9: TLabel;
    Button15: TButton;
    procedure Button1Click(Sender: TObject);
    procedure Open1Click(Sender: TObject);
    procedure FormActivate(Sender: TObject);
    procedure ComboBox1Change(Sender: TObject);
    procedure Button2Click(Sender: TObject);
    procedure Button3Click(Sender: TObject);
    procedure Button5Click(Sender: TObject);
    procedure Button6Click(Sender: TObject);
    procedure Button7Click(Sender: TObject);
    procedure Button8Click(Sender: TObject);
    procedure Table3AfterPost(DataSet: TDataSet);
    procedure Table3BeforePost(DataSet: TDataSet);
    procedure Button9Click(Sender: TObject);
    procedure Button10Click(Sender: TObject);
    procedure FormDestroy(Sender: TObject);
    procedure FormCreate(Sender: TObject);
    procedure Button11Click(Sender: TObject);
    procedure ListBox2Click(Sender: TObject);
    procedure Button12Click(Sender: TObject);
    procedure Button13Click(Sender: TObject);
    procedure Button14Click(Sender: TObject);
    procedure CheckBox1Click(Sender: TObject);
    procedure Edit3Change(Sender: TObject);
    procedure CheckBox2Click(Sender: TObject);
    procedure Edit4Change(Sender: TObject);
    procedure CheckBox3Click(Sender: TObject);
    procedure Timer1Timer(Sender: TObject);
    procedure Timer2Timer(Sender: TObject);
    procedure ComboBox2Change(Sender: TObject);
    procedure FormClose(Sender: TObject; var Action: TCloseAction);
    procedure Button15Click(Sender: TObject);
  private
    { Private declarations }
  public
    { Public declarations }
  end;

type
Tdephbldata = record
    GAZDEPTH: Single;
    C1: Single;
    C2: Single;
    C3: Single;
    C4: Single;
    C5: Single;
    CSUM: Single;
    end;
 Tdephcount = record
    i:integer;
    S:Single;
    end;

 Ttimecount = record
    i:integer;
    S:LongWord;
    end;

  TLST= Packed record
    BaseDisp: DWORD;
    KeyValue: Single;
    TimeDos: LongWord;
    NRecTrue: longWord;
    NRecLogic: longWord;
    FlagState: Byte;
  end;
  //Справочник DTCIS
  TParsys =  Packed record
      K: Single;
      NPar: SHORT;
      Size: SHORT;
      ParType: AnsiChar;
      NameMes: array[0..10] of AnsiChar ;
      NamePar: array[0..20] of AnsiChar;
  end;

  //Запись DEP
  TDEP_ZAG = Packed record
    //Заголовок
    NRec: Cardinal;
    NWELL: SHORT;
    LengthRec: SHORT;
    NumbParKeY: Byte;
    CountPar: Byte;

    NSprav0: Byte;
    NPar0: Byte;
    val0: Single; // Вес на крюке

    NSprav1: Byte;
    NPar1: Byte;
    val1: Single; // Нагрузка на долото

    NSprav2: Byte;
    NPar2: Byte;
    val2: Single; // Давление на входе

    NSprav3: Byte;
    NPar3: Byte;
    val3: Single; // Давление на выходе

    NSprav4: Byte;
    NPar4: Byte;
    val4: Single; // Обороты ротора

    NSprav5: Byte;
    NPar5: Byte;
    val5: Single; // Момент на роторе

    NSprav6: Byte;
    NPar6: Byte;
    val6: Single; // Плотность на входе

    NSprav7: Byte;
    NPar7: Byte;
    val7: Single; // Плотность на выходе

    NSprav8: Byte;
    NPar8: Byte;
    val8: Single; // Температура на входе

    NSprav9: Byte;
    NPar9: Byte;
    val9: Single; // Температура на выход

    NSprav10: Byte;
    NPar10: Byte;
    val10: Single; // Объем рабочих емк.

    NSprav11: Byte;
    NPar11: Byte;
    val11: Single; // Общий газ

    NSprav12: Byte;
    NPar12: Byte;
    val12: Single; // Положение крюка

    NSprav13: Byte;
    NPar13: Byte;
    val13: Single; // Ходов насоса 1

    NSprav14: Byte;
    NPar14: Byte;
    val14: Single; // Ходов насоса 2

    NSprav15: Byte;
    NPar15: Byte;
    val15: Single; // Расход на выходе

    NSprav16: Byte;
    NPar16: Byte;
    val16: Single; // С1

    NSprav17: Byte;
    NPar17: Byte;
    val17: Single; // С2

    NSprav18: Byte;
    NPar18: Byte;
    val18: Single; // С3

    NSprav19: Byte;
    NPar19: Byte;
    val19: Single; // H2

    NSprav20: Byte;
    NPar20: Byte;
    val20: Single; // С4

    NSprav21: Byte;
    NPar21: Byte;
    val21: Single; // С5

    NSprav22: Byte;
    NPar22: Byte;
    val22: Single; // Мех.скорость

    NSprav23: Byte;
    NPar23: Byte;
    val23: Single; // ДМК

    NSprav24: Byte;
    NPar24: Byte;
    val24: Single; // Интервал за рейс

    NSprav25: Byte;
    NPar25: Byte;
    val25: Single; // Время бурения   рейс

    NSprav26: Byte;
    NPar26: Byte;
    val26: Single; // Стоимость бурения

    NSprav27: Byte;
    NPar27: Byte;
    val27: Single; // DEXP

    NSprav28: Byte;
    NPar28: Byte;
    val28: Single; // DEXC с учетом плотн.

    NSprav29: Byte;
    NPar29: Byte;
    val29: Single; // DEXCN износа долота

    NSprav30: Byte;
    NPar30: Byte;
    val30: Single; // Эквив.плотн.циркуляц

    NSprav31: Byte;
    NPar31: Byte;
    val31: Single; // Расход на входе

    NSprav32: Byte;
    NPar32: Byte;
    val32: Single; // Расход разность

    NSprav33: Byte;
    NPar33: Byte;
    val33: Single; // Плотность разность

    NSprav34: Byte;
    NPar34: Byte;
    val34: Single; // Температура разность

    NSprav35: Byte;
    NPar35: Byte;
    val35: longInt; // Ходов насоса    рейс

    NSprav36: Byte;
    NPar36: Byte;
    val36: longInt; // Оборотов долота рейс

    NSprav37: Byte;
    NPar37: Byte;
    val37: Single; // Отставание газов(хн)

    NSprav38: Byte;
    NPar38: Byte;
    val38: Single; // Отставание газов(вр)

    NSprav39: Byte;
    NPar39: Byte;
    val39: Single; // Глуб.отст.газов усте

    NSprav40: Byte;
    NPar40: Byte;
    val40: Single; // Отставание шлама(вр)

    NSprav41: Byte;
    NPar41: Byte;
    val41: Single; // С2...С6 / С1...С6

    NSprav42: Byte;
    NPar42: Byte;
    val42: Single; // С1...С2 / С3...С6

    NSprav43: Byte;
    NPar43: Byte;
    val43: Single; // С4...С6 / С3

    NSprav44: Byte;
    NPar44: Byte;
    val44: Single; // Объем емкости 1

    NSprav45: Byte;
    NPar45: Byte;
    val45: Single; // Объем емкости 2

    NSprav46: Byte;
    NPar46: Byte;
    val46: Single; // Объем емкости 3

    NSprav47: Byte;
    NPar47: Byte;
    val47: Single; // Объем емкости 4

    NSprav48: Byte;
    NPar48: Byte;
    val48: Single; // Объем емкости 5

    NSprav49: Byte;
    NPar49: Byte;
    val49: Single; // Объем емк.Долива

    NSprav50: Byte;
    NPar50: Byte;
    val50: Single; // Давл.в зоне дол.СПО

    NSprav51: Byte;
    NPar51: Byte;
    val51: Single; // Объем всех емкостей

    NSprav52: Byte;
    NPar52: Byte;
    val52: longInt; // Время сбора данных

    NSprav53: Byte;
    NPar53: Byte;
    val53: Single; // Глубина Забоя

    NSprav54: Byte;
    NPar54: Byte;
    val54: Single; // Глубина долота

    NSprav55: Byte;
    NPar55: Byte;
    val55: Single; // Глубина вертикальная

    NSprav56: Byte;
    NPar56: Byte;
    val56: Single; // Отставание шлама(хн)

    NSprav57: Byte;
    NPar57: Byte;
    val57: Single; // Объем затрубья

    NSprav58: Byte;
    NPar58: Byte;
    val58: Single; // Пот.давл. затрубья

    NSprav59: Byte;
    NPar59: Byte;
    val59: Single; // Объем в трубах

    NSprav60: Byte;
    NPar60: Byte;
    val60: Single; // Пот.давл. в трубах

    NSprav61: Byte;
    NPar61: Byte;
    val61: Single; // Скорость в насадках

    NSprav62: Byte;
    NPar62: Byte;
    val62: Single; // Пот.давл. в насадках

    NSprav63: Byte;
    NPar63: Byte;
    val63: Single; // Гидр.мощн. на долоте

    NSprav64: Byte;
    NPar64: Byte;
    val64: Single; // Гидр.мощн. на площaд

    NSprav65: Byte;
    NPar65: Byte;
    val65: Single; // Удар.нагр. на долото

    NSprav66: Byte;
    NPar66: Byte;
    val66: Single; // Удар.нагр. на площад

    NSprav67: Byte;
    NPar67: Byte;
    val67: Single; // Гидр.мощность систем

    NSprav68: Byte;
    NPar68: Byte;
    val68: Single; // Скорость оседания шл

    NSprav69: Byte;
    NPar69: Byte;
    val69: Single; // Пот.давл. в оборуд.

    NSprav70: Byte;
    NPar70: Byte;
    val70: Single; // Пот.давл. суммарные

    NSprav71: Byte;
    NPar71: Byte;
    val71: Single; // Град.давл.поров:Dexp

    NSprav72: Byte;
    NPar72: Byte;
    val72: Single; // Над забоем

    NSprav73: Byte;
    NPar73: Byte;
    val73: SmallInt; // Номер рейса

    NSprav74: Byte;
    NPar74: Byte;
    val74: Single; // Глубина начала рейса

    NSprav75: Byte;
    NPar75: Byte;
    val75: longInt; // Время начала рейса

    NSprav76: Byte;
    NPar76: Byte;
    val76: Single; // Глубина подошвы Об.К

    NSprav77: Byte;
    NPar77: Byte;
    val77: Single; // Баланс дол/выт СПО

    NSprav78: Byte;
    NPar78: Byte;
    val78: SmallInt; // Способ бурения

    NSprav79: Byte;
    NPar79: Byte;
    val79: Single; // Расход турбины

    NSprav80: Byte;
    NPar80: Byte;
    val80: Single; // Плотность шлама

    NSprav81: Byte;
    NPar81: Byte;
    val81: Single; // Диаметр шлама

    NSprav82: Byte;
    NPar82: Byte;
    val82: Single; // Вязкость раствора

    NSprav83: Byte;
    NPar83: Byte;
    val83: Single; // Напряжение сдвига

    NSprav84: Byte;
    NPar84: Byte;
    val84: Single; // Град.пластового давл

    NSprav85: Byte;
    NPar85: Byte;
    val85: Single; // Град.горного давлен.

    NSprav86: Byte;
    NPar86: Byte;
    val86: array[0..11] of AnsiChar; // Тип долота

    NSprav87: Byte;
    NPar87: Byte;
    val87: Single; // Стоимость долота

    NSprav88: Byte;
    NPar88: Byte;
    val88: Single; // Диаметр долота

    NSprav89: Byte;
    NPar89: Byte;
    val89: Single; // Sigma:Напряжение ГП

    NSprav90: Byte;
    NPar90: Byte;
    val90: Single; // Sigma:Прочность ГП

    NSprav91: Byte;
    NPar91: Byte;
    val91: Single; // Sigma:Эталонная проч

    NSprav92: Byte;
    NPar92: Byte;
    val92: Single; // Sigma:Пористость ГП

    NSprav93: Byte;
    NPar93: Byte;
    val93: Single; // Площадь насадок

    NSprav94: Byte;
    NPar94: Byte;
    val94: Single; // Производит. насоса 1

    NSprav95: Byte;
    NPar95: Byte;
    val95: Single; // Объем емкости 9

    NSprav96: Byte;
    NPar96: Byte;
    val96: Single; // ГК (гамма-каротаж)

    NSprav97: Byte;
    NPar97: Byte;
    val97: Single; // Изменение Давл.на вх

    NSprav98: Byte;
    NPar98: Byte;
    val98: Single; // Гидростатическое дав

    NSprav99: Byte;
    NPar99: Byte;
    val99: Single; // Эффективное давление

    NSprav100: Byte;
    NPar100: Byte;
    val100: Single; // Глубина выхода шлама

    NSprav101: Byte;
    NPar101: Byte;
    val101: Single; // Глубина забоя датчик

    NSprav102: Byte;
    NPar102: Byte;
    val102: Single; // Момент на долоте

    NSprav103: Byte;
    NPar103: Byte;
    val103: SmallInt; // Код породы

    NSprav104: Byte;
    NPar104: Byte;
    val104: Single; // Время СПО       рейс

    NSprav105: Byte;
    NPar105: Byte;
    val105: Single; // Sigm:Град.давл.пласт

    NSprav106: Byte;
    NPar106: Byte;
    val106: Single; // Время на свечу

    NSprav107: Byte;
    NPar107: Byte;
    val107: SmallInt; // Свеч вне скважины

    NSprav108: Byte;
    NPar108: Byte;
    val108: SmallInt; // Свеч внутри скважины

    NSprav109: Byte;
    NPar109: Byte;
    val109: SmallInt; // Труб вне скважины

    NSprav110: Byte;
    NPar110: Byte;
    val110: SmallInt; // Труб внутри скважины

    NSprav111: Byte;
    NPar111: Byte;
    val111: SmallInt; // Труб в одной свече

    NSprav112: Byte;
    NPar112: Byte;
    val112: SmallInt; // Состояние клиньев

    NSprav113: Byte;
    NPar113: Byte;
    val113: SmallInt; // Труб до забоя

    NSprav114: Byte;
    NPar114: Byte;
    val114: Single; // Средний вес трубы

    NSprav115: Byte;
    NPar115: Byte;
    val115: Single; // Вес крюке СПО средн.

    NSprav116: Byte;
    NPar116: Byte;
    val116: Single; // Вес крюке СПО ожид.

    NSprav117: Byte;
    NPar117: Byte;
    val117: Single; // Водоизм. ожидаемое

    NSprav118: Byte;
    NPar118: Byte;
    val118: Single; // Водоизм. расчетное

    NSprav119: Byte;
    NPar119: Byte;
    val119: Single; // Водоизм. текущее

    NSprav120: Byte;
    NPar120: Byte;
    val120: Single; // Давл.свабир/поршнев.

    NSprav121: Byte;
    NPar121: Byte;
    val121: Single; // Потери БР по времени

    NSprav122: Byte;
    NPar122: Byte;
    val122: Single; // Потери БР по глубине

    NSprav123: Byte;
    NPar123: Byte;
    val123: Single; // Время СПО

    NSprav124: Byte;
    NPar124: Byte;
    val124: Single; // Давление пульсаций

    NSprav125: Byte;
    NPar125: Byte;
    val125:  array[0..31] of AnsiChar; // Шламограмма

    NSprav126: Byte;
    NPar126: Byte;
    val126:  array[0..8] of AnsiChar; // Нефтепроявления

    NSprav127: Byte;
    NPar127: Byte;
    val127: Single; // Дифференциальное дав

    NSprav128: Byte;
    NPar128: Byte;
    val128: Single; // Плотность перелома

    NSprav129: Byte;
    NPar129: Byte;
    val129: Single; // Время спуска Обс.Тр.

    NSprav130: Byte;
    NPar130: Byte;
    val130: Single; // Время спуска Обс.Кол

    NSprav131: Byte;
    NPar131: Byte;
    val131: SmallInt; // Обс.Труб внутри скв.

    NSprav132: Byte;
    NPar132: Byte;
    val132: SmallInt; // Обс.Труб вне скваж.

    NSprav133: Byte;
    NPar133: Byte;
    val133: Single; // Время спускаОбК рейс

    NSprav134: Byte;
    NPar134: Byte;
    val134: Single; // Наработка тал.каната

    NSprav135: Byte;
    NPar135: Byte;
    val135: Single; // Ходов насоса 3

    NSprav136: Byte;
    NPar136: Byte;
    val136: Single; // Потери БР суммарные

    NSprav137: Byte;
    NPar137: Byte;
    val137: Single; // нС4 / С1...С6

    NSprav138: Byte;
    NPar138: Byte;
    val138: Single; // Объем труб (маталла)

    NSprav139: Byte;
    NPar139: Byte;
    val139: Single; // Время контр.поглощ.

    NSprav140: Byte;
    NPar140: Byte;
    val140: Single; // Глуб.спускаемой ОбК

    NSprav141: Byte;
    NPar141: Byte;
    val141: Single; // Время контр.выброса

    NSprav142: Byte;
    NPar142: Byte;
    val142: Single; // Кол-во закаченого БР

    NSprav143: Byte;
    NPar143: Byte;
    val143: Single; // Мгновенная скор.прох

    NSprav144: Byte;
    NPar144: Byte;
    val144: Single; // Время к.выброса рейс

    NSprav145: Byte;
    NPar145: Byte;
    val145: Single; // Объем емкости 10

    NSprav146: Byte;
    NPar146: Byte;
    val146: Single; // Объем емкости 11

    NSprav147: Byte;
    NPar147: Byte;
    val147: Single; // Время к.поглощения р

    NSprav148: Byte;
    NPar148: Byte;
    val148:  array[0..30] of AnsiChar; // Примечание

    NSprav149: Byte;
    NPar149: Byte;
    val149: Single; // Объем емкости 12

    NSprav150: Byte;
    NPar150: Byte;
    val150: SmallInt; // Обсадных труб забой

    NSprav151: Byte;
    NPar151: Byte;
    val151: Single; // Время ремонта   рейс

    NSprav152: Byte;
    NPar152: Byte;
    val152: Single; // Сумма С1...С6

    NSprav153: Byte;
    NPar153: Byte;
    val153: Single; // С1...С2 / С5...С6

    NSprav154: Byte;
    NPar154: Byte;
    val154: Single; // H2S

    NSprav155: Byte;
    NPar155: Byte;
    val155: Single; // Минерализация на вх

    NSprav156: Byte;
    NPar156: Byte;
    val156: Single; // Минерализация на вых

    NSprav157: Byte;
    NPar157: Byte;
    val157: Single; // Время бурения

    NSprav158: Byte;
    NPar158: Byte;
    val158: Single; // Время циркуляции рей

    NSprav159: Byte;
    NPar159: Byte;
    val159: Single; // Время проработки

    NSprav160: Byte;
    NPar160: Byte;
    val160: Single; // Время промывки  рейс

    NSprav161: Byte;
    NPar161: Byte;
    val161: Single; // Время наращивание ре

    NSprav162: Byte;
    NPar162: Byte;
    val162: Single; // Время СПО       рейс

    NSprav163: Byte;
    NPar163: Byte;
    val163: Single; // Время ПЗР       рейс

    NSprav164: Byte;
    NPar164: Byte;
    val164: Single; // Время ГИС       рейс

    NSprav165: Byte;
    NPar165: Byte;
    val165: Single; // Время простоя   рейс

    NSprav166: Byte;
    NPar166: Byte;
    val166: Single; // Плотность емк 1

    NSprav167: Byte;
    NPar167: Byte;
    val167: Single; // Плотность емк 2

    NSprav168: Byte;
    NPar168: Byte;
    val168: Single; // Плотность емк 3

    NSprav169: Byte;
    NPar169: Byte;
    val169: Single; // Плотность емк 4

    NSprav170: Byte;
    NPar170: Byte;
    val170: Single; // Плотность емк 5

    NSprav171: Byte;
    NPar171: Byte;
    val171: Single; // Температура емк 1

    NSprav172: Byte;
    NPar172: Byte;
    val172: Single; // Температура емк 2

    NSprav173: Byte;
    NPar173: Byte;
    val173: Single; // Температура емк 3

    NSprav174: Byte;
    NPar174: Byte;
    val174: Single; // Температура емк 4

    NSprav175: Byte;
    NPar175: Byte;
    val175: Single; // Температура емк 5

    NSprav176: Byte;
    NPar176: Byte;
    val176: Single; // Кальцит

    NSprav177: Byte;
    NPar177: Byte;
    val177: Single; // С2' Этилен

    NSprav178: Byte;
    NPar178: Byte;
    val178: Single; // Прогноз износа Долот

    NSprav179: Byte;
    NPar179: Byte;
    val179: Single; // Показатель износа Д.

    NSprav180: Byte;
    NPar180: Byte;
    val180: Single; // Dexp:Полный град.дав

    NSprav181: Byte;
    NPar181: Byte;
    val181: Single; // Sigm:Полный град.дав

    NSprav182: Byte;
    NPar182: Byte;
    val182: Single; // Время проработки

    NSprav183: Byte;
    NPar183: Byte;
    val183: Single; // Время промывки

    NSprav184: Byte;
    NPar184: Byte;
    val184: Single; // Время наращивания

    NSprav185: Byte;
    NPar185: Byte;
    val185: Single; // Время СПО

    NSprav186: Byte;
    NPar186: Byte;
    val186: Single; // Время циркуляции

    NSprav187: Byte;
    NPar187: Byte;
    val187: Single; // Время простоя

    NSprav188: Byte;
    NPar188: Byte;
    val188: Single; // Объемная плотн.шлама

    NSprav189: Byte;
    NPar189: Byte;
    val189: Single; // Ускор.Обор.Ротора

    NSprav190: Byte;
    NPar190: Byte;
    val190: SmallInt; // Направление крюка

    NSprav191: Byte;
    NPar191: Byte;
    val191: Single; // Абсол.скорость крюка

    NSprav192: Byte;
    NPar192: Byte;
    val192: Single; // Глубина инклинометра

    NSprav193: Byte;
    NPar193: Byte;
    val193: Single; // Отклонитель

    NSprav194: Byte;
    NPar194: Byte;
    val194: Single; // Азимут

    NSprav195: Byte;
    NPar195: Byte;
    val195: Single; // Зенит

    NSprav196: Byte;
    NPar196: Byte;
    val196: Single; // Доломит

    NSprav197: Byte;
    NPar197: Byte;
    val197: Single; // Момент на ключе

    NSprav198: Byte;
    NPar198: Byte;
    val198: Single; // Глуб.отст.газов хром

    NSprav199: Byte;
    NPar199: Byte;
    val199: Single; // Плотность Долива

    NSprav200: Byte;
    NPar200: Byte;
    val200: Single; // Температура Долива

    NSprav201: Byte;
    NPar201: Byte;
    val201: Single; // нС4

    NSprav202: Byte;
    NPar202: Byte;
    val202: Single; // С1 / С1...С6

    NSprav203: Byte;
    NPar203: Byte;
    val203: Single; // С2 / С1...С6

    NSprav204: Byte;
    NPar204: Byte;
    val204: Single; // С3 / С1...С6

    NSprav205: Byte;
    NPar205: Byte;
    val205: Single; // Минерал.плотн.шлама

    NSprav206: Byte;
    NPar206: Byte;
    val206: Single; // С4 / С1...С6

    NSprav207: Byte;
    NPar207: Byte;
    val207: Single; // С5 / С1...С6

    NSprav208: Byte;
    NPar208: Byte;
    val208: Single; // С6 / С1...С6

    NSprav209: Byte;
    NPar209: Byte;
    val209: Single; // С6

    NSprav210: Byte;
    NPar210: Byte;
    val210: Single; // Ускорение инструмент

    NSprav211: Byte;
    NPar211: Byte;
    val211: Single; // Скорость проработки

    NSprav212: Byte;
    NPar212: Byte;
    val212: SmallInt; // Технологический этап

    NSprav213: Byte;
    NPar213: Byte;
    val213: longInt; // Этапы ГТИ по времени

    NSprav214: Byte;
    NPar214: Byte;
    val214: longInt; // Этапы ГТИ по глубине

    NSprav215: Byte;
    NPar215: Byte;
    val215: Single; // иС4

    NSprav216: Byte;
    NPar216: Byte;
    val216: Single; // С1 по шламу

    NSprav217: Byte;
    NPar217: Byte;
    val217: Single; // С2 по шламу

    NSprav218: Byte;
    NPar218: Byte;
    val218: Single; // С3 по шламу

    NSprav219: Byte;
    NPar219: Byte;
    val219: Single; // С4 по шламу

    NSprav220: Byte;
    NPar220: Byte;
    val220: Single; // С5 по шламу

    NSprav221: Byte;
    NPar221: Byte;
    val221: Single; // С6 по шламу

    NSprav222: Byte;
    NPar222: Byte;
    val222: Single; // Сумма шламу С1...С6

    NSprav223: Byte;
    NPar223: Byte;
    val223: Single; // иС4/С1...С6

    NSprav224: Byte;
    NPar224: Byte;
    val224: Single; // С2...С3 / С4...С6

    NSprav225: Byte;
    NPar225: Byte;
    val225: Single; // С1 / С2...С6

    NSprav226: Byte;
    NPar226: Byte;
    val226: Single; // CO2

    NSprav227: Byte;
    NPar227: Byte;
    val227: Single; // N2

    NSprav228: Byte;
    NPar228: Byte;
    val228: Single; // O2

    NSprav229: Byte;
    NPar229: Byte;
    val229: Single; // Хроматограф время

    NSprav230: Byte;
    NPar230: Byte;
    val230: Single; // Хроматограф канал 1

    NSprav231: Byte;
    NPar231: Byte;
    val231: Single; // Хроматограф канал 2

    NSprav232: Byte;
    NPar232: Byte;
    val232:  array[0..9] of AnsiChar; // Порядок пород шлама

    NSprav233: Byte;
    NPar233: Byte;
    val233: longInt; // Код аварии

    NSprav234: Byte;
    NPar234: Byte;
    val234: longInt; // РТК

    NSprav235: Byte;
    NPar235: Byte;
    val235: Single; // Скорость инструмента

    NSprav236: Byte;
    NPar236: Byte;
    val236: Single; // Объем емкости 6

    NSprav237: Byte;
    NPar237: Byte;
    val237: Single; // Объем емкости 7

    NSprav238: Byte;
    NPar238: Byte;
    val238: Single; // Объем емкости 8

    NSprav239: Byte;
    NPar239: Byte;
    val239: Single; // Объем нераб.емкостей

    NSprav240: Byte;
    NPar240: Byte;
    val240: Single; // Dexp:Пластовое давл.

    NSprav241: Byte;
    NPar241: Byte;
    val241: Single; // Sigm:Пластовое давл.

    NSprav242: Byte;
    NPar242: Byte;
    val242: Single; // Вес на крюке СПО min

    NSprav243: Byte;
    NPar243: Byte;
    val243: Single; // Вес на крюке СПО max

    NSprav244: Byte;
    NPar244: Byte;
    val244: Single; // Обороты долота

    NSprav245: Byte;
    NPar245: Byte;
    val245: Single; // Коэф.откр.пористости

    NSprav246: Byte;
    NPar246: Byte;
    val246: Single; // Вес бурового инстр.

    NSprav247: Byte;
    NPar247: Byte;
    val247: Single; // Dexp:линия норм.упл.

    NSprav248: Byte;
    NPar248: Byte;
    val248: Single; // Sigm:линия норм.упл.

    NSprav249: Byte;
    NPar249: Byte;
    val249: Single; // иС5

    NSprav250: Byte;
    NPar250: Byte;
    val250: Single; // иС5 / С1...С6

    NSprav251: Byte;
    NPar251: Byte;
    val251: Single; // нС5

    NSprav252: Byte;
    NPar252: Byte;
    val252: Single; // нС5 / С1...С6

    NSprav253: Byte;
    NPar253: Byte;
    val253: Single; // Момент ротора (max)

    NSprav254: Byte;
    NPar254: Byte;
    val254:  array[0..19] of AnsiChar; // Заводской ном.долота

  end;











 {
  TDEP_ZAG2 = Packed record
    NumbSprav: Byte;
    NumbPar: Byte;
  end;
  TDEP_VALUE_FLOAT = Packed record
    VALUE: Single;
  end;
  TDEP_VALUE_LONG = Packed record
    VALUE: longInt;
  end;
  TDEP_VALUE_INTEGER = Packed record
    VALUE: Integer;
  end;
  TDEP_VALUE_WINDOWS_DATETIME = Packed record
    VALUE: Single ;
  end;
  TDEP_VALUE_STRING = Packed record
    VALUE: string;
  end;

  }

var
  Form1: TForm1;
  temp:Word;
  myPath:String;
  Search,Search2, Search3 : TSearchRec;

  gPath : String = ''; //Путь к папке.geoscape
  dPath : String = ''; //Путь к папке.dtcis
  gcycletime: Boolean = false; //Разрешен ли цикл для времянок
  gcycletimeInter: Integer = 20; //цикл для времянок в сек
  gcycledepth: Boolean = false; //Разрешен ли цикл для глубинок
  gcycledepthInter: Integer = 20; //цикл для глубинок в сек
  gcycledepthgaz: Boolean = false; //Разрешен ли цикл для отставания
  gspeed: Integer = 0; //скорость

  CurAttr : Integer;
  //Текущий временной файл Геоскейп
  time_name_ga : string;
  //Текущий временной файл DTCIS

  //Диалог выбор директории
  options : TSelectDirOpts;
  chosenDirectory : string;
  //информация о текущем  STORE
  Countdepth : Tdephcount;
  //информация о текущем  time
  Counttime : Ttimecount;

  time_name_dtcis : string;
  //Текущая LST -запись
  lstrec:TLST;

  //Текущий заголовок DEP -запись
  depRecZAG:TDEP_ZAG;

  //список значений bldada
  BLDATA: Array of Tdephbldata;

  //Количество полей в Geoscape таблице
  fieldCount:Integer;


  {//Текущий подзаголовок DEP -запись
  //depRecZAG2:TDEP_ZAG2;

  //Текущее значение TDEP_VALUE_FLOAT
  depValFloat:TDEP_VALUE_FLOAT;
  //Текущее значение TDEP_VALUE_LONG
  depValLong:TDEP_VALUE_LONG;
  //Текущее значение TDEP_VALUE_INTEGER
  depValInteger:TDEP_VALUE_INTEGER;
  //Текущее значение TDEP_VALUE_DATETIME
  depValDatetime:TDEP_VALUE_WINDOWS_DATETIME;
   UnixStartDate: TDateTime = 25569.0;
  //Текущее значение TDEP_VALUE_STRING
  depValString:TDEP_VALUE_STRING;
   }


  //Текущий файловый указатель LST
  myFile: file of TLST;
    //Текущий файловый указатель DEP ZAG
  FileZAG: file of TDEP_ZAG;


  {FileZAG2: file of TDEP_ZAG2;
  ValFloat: file of TDEP_VALUE_FLOAT;
  ValLong: file of TDEP_VALUE_LONG;
  ValInteger: file of TDEP_VALUE_INTEGER;
  ValDatetime: file of TDEP_VALUE_WINDOWS_DATETIME;
  //ValString: file of TDEP_VALUE_STRING;
   }

  //Справочник параметров размер-тип
  Parsys0: TParsys;
  //Файловый указатель
  FParsys0: file of TParsys;

  buf: TParsys;
  FBuf: file of TParsys;

  //Строки
    val86: array[0..11] of AnsiChar; // Тип долота


    val125: array[0..31] of AnsiChar; // Шламограмма


    val126: array[0..8] of AnsiChar; // Нефтепроявления


    val148: array[0..30] of AnsiChar; // Примечание


    val232: array[0..9] of AnsiChar; // Порядок пород шлама

    val254: array[0..19] of AnsiChar; // Заводской ном.долота
  // Масссив индекс-значение с плавающей точкой
  ValF: array [0..225, 0..1] of Single =((0, 0), (1, 0), (2, 0), (3, 0), (4, 0), (5, 0), (6, 0), (7, 0), (8, 0), (9, 0), (10, 0),
 (11, 0), (12, 0), (13, 0), (14, 0), (15, 0), (16, 0), (17, 0), (18, 0), (19, 0), (20, 0),
 (21, 0), (22, 0), (23, 0), (24, 0), (25, 0), (26, 0), (27, 0), (28, 0), (29, 0), (30, 0),
 (31, 0), (32, 0), (33, 0), (34, 0), (37, 0), (38, 0), (39, 0), (40, 0), (41, 0), (42, 0),
 (43, 0), (44, 0), (45, 0), (46, 0), (47, 0), (48, 0), (49, 0), (50, 0), (51, 0), (53, 0),
 (54, 0), (55, 0), (56, 0), (57, 0), (58, 0), (59, 0), (60, 0), (61, 0), (62, 0), (63, 0),
 (64, 0), (65, 0), (66, 0), (67, 0), (68, 0), (69, 0), (70, 0), (71, 0), (72, 0), (74, 0),
 (76, 0), (77, 0), (79, 0), (80, 0), (81, 0), (82, 0), (83, 0), (84, 0), (85, 0), (87, 0),
 (88, 0), (89, 0), (90, 0), (91, 0), (92, 0), (93, 0), (94, 0), (95, 0), (96, 0), (97, 0),
 (98, 0), (99, 0), (100, 0), (101, 0), (102, 0), (104, 0), (105, 0), (106, 0), (114, 0),
 (115, 0), (116, 0), (117, 0), (118, 0), (119, 0), (120, 0), (121, 0), (122, 0), (123, 0),
 (124, 0), (127, 0), (128, 0), (129, 0), (130, 0), (133, 0), (134, 0), (135, 0), (136, 0),
 (137, 0), (138, 0), (139, 0), (140, 0), (141, 0), (142, 0), (143, 0), (144, 0), (145, 0),
 (146, 0), (147, 0), (149, 0), (151, 0), (152, 0), (153, 0), (154, 0), (155, 0), (156, 0),
 (157, 0), (158, 0), (159, 0), (160, 0), (161, 0), (162, 0), (163, 0), (164, 0), (165, 0),
 (166, 0), (167, 0), (168, 0), (169, 0), (170, 0), (171, 0), (172, 0), (173, 0), (174, 0),
 (175, 0), (176, 0), (177, 0), (178, 0), (179, 0), (180, 0), (181, 0), (182, 0), (183, 0),
 (184, 0), (185, 0), (186, 0), (187, 0), (188, 0), (189, 0), (191, 0), (192, 0), (193, 0),
 (194, 0), (195, 0), (196, 0), (197, 0), (198, 0), (199, 0), (200, 0), (201, 0), (202, 0),
 (203, 0), (204, 0), (205, 0), (206, 0), (207, 0), (208, 0), (209, 0), (210, 0), (211, 0),
 (215, 0), (216, 0), (217, 0), (218, 0), (219, 0), (220, 0), (221, 0), (222, 0), (223, 0),
 (224, 0), (225, 0), (226, 0), (227, 0), (228, 0), (229, 0), (230, 0), (231, 0), (235, 0),
 (236, 0), (237, 0), (238, 0), (239, 0), (240, 0), (241, 0), (242, 0), (243, 0), (244, 0),
 (245, 0), (246, 0), (247, 0), (248, 0), (249, 0), (250, 0), (251, 0), (252, 0), (253, 0));

  // Масссив индекс-значение int
  ValI: array [0..14, 0..1] of SmallInt =((73, 0), (78, 0), (103, 0), (107, 0), (108, 0),
   (109, 0), (110, 0), (111, 0), (112, 0), (113, 0), (131, 0), (132, 0), (150, 0), (190, 0), (212, 0));
  // Масссив индекс-значение Long
  ValL: array [0..7, 0..1] of longInt =((35, 0), (36, 0), (52, 0), (75, 0), (213, 0), (214, 0), (233, 0), (234, 0));

  //Массив соответствия по времени
  RazToDTCIS: array  of  array of Smallint;
   //Список TLabel для соответствия параметров
   ListLabel : TList;
   CurLabel : TLabel;

  //Массив соответствия по глубине
  RazToDTCISdepth: array  of  array of Smallint;
   //Список TLabel для соответствия параметров
   ListLabel2 : TList;
   CurLabel2 : TLabel;



implementation

{$R *.dfm}

procedure TForm1.Button1Click(Sender: TObject);
begin
ComboBox1.Items.Clear();
ComboBox1.Items.Add('12323');
Table1.Active:=True;

end;


//Создание или изменение алиаса
procedure CheckAlias(const AliasName, AliasType, AliasPath: String);
var
  SList: TStrings;
  i: Integer;
  AliasFound: Boolean;
begin
  Session.Close;
  try
    SList := TStringList.Create;
    Session.GetAliasNames(SList);
    AliasFound := False;
    for i:=0 to SList.Count-1 do
      if SList[i]=AliasName then 
        begin
          AliasFound := True; 
          break;
        end;
  finally
    SList.Free; 
  end;
  if AliasFound then
    begin
      try 
        SList := TStringList.Create;
        Session.GetAliasParams(AliasName,SList);
        if SList[0]<> 'PATH='+AliasPath then
          begin
            SList[0] := 'PATH='+AliasPath;
            Session.ModifyAlias(AliasName,SList);
          end;
      finally 
        SList.Free; 
      end;
    end
  else
    Session.AddStandardAlias(AliasName,AliasPath,AliasType);
  Session.SaveConfigFile;
  Session.Open;
  //form1.Table1.Active:=True;
  form1.Table2.TableName:=ExtractFilePath (ParamStr (0))+'Sensors.DB';
  form1.Table2.Active:=True;
  form1.Table3.TableName:=ExtractFilePath (ParamStr (0))+'razreztoims.DB';
  form1.Table3.Active:=True;
  //form1.Table4.Active:=True;
  //form1.Table5.Active:=True;
end;


//сортировка

function GTSmartCompare(List: TStringList; Index1, Index2: Integer): Integer;

  procedure ExtractPart(var s: string; out Result: string; out Numbers: Boolean);
  var
    n: integer;
  begin
    Numbers := False;
    n := 1;
    while (s[n] in ['0'..'9']) and (n <= Length(s)) do
      Inc(n);

    { n > 1 if there were digits at the start of the string}
    if n > 1 then
    begin
      Result := Copy(s, 1, n - 1);
      Delete(s, 1, n - 1);
      Numbers := True;
    end
    else
    begin
      { No digits }
      n := 1;
      while (not (s[n] in ['0'..'9']) ) and (n <= Length(s)) do
        Inc(n);

      if n > 1 then
      begin
        Result := Copy(s, 1, n - 1);
        Delete(s, 1, n - 1);
      end
    end;
  end; //ExtractPart()


  function CompareNextPart(var s1, s2: string): Integer;
  var
    n1, n2: Boolean;
    p1, p2: string;
  begin
    { Extract the next part for comparison }
    ExtractPart(s1, p1, n1);
    ExtractPart(s2, p2, n2);

    { Both numbers? The do a numerical comparison, otherwise alfabetical }
    if n1 and n2 then
      Result := StrToInt(p1) - StrToInt(p2)
    else
      Result := StrIComp(PChar(p1), PChar(p2));
  end; //CompareNextPart()

var
  str1, str2, ext1, ext2: string;

begin
  Result := 0;
  { For 'normal' comparison
    str2 := List[Index1];
    str2 := List[Index2];
    For comparing file names }

  ext1 := ExtractFileExt(List[Index1]);
  ext2 := ExtractFileExt(List[Index2]);
  str1 := ChangeFileExt(List[Index1], '');
  str2 := ChangeFileExt(List[Index2], '');

  while (str1 <> '') and (str2 <> '') and (Result = 0) do
    Result := CompareNextPart(str1, str2);

  { Comparing found no numerical differences, so repeat with a 'normal' compare. }

  if Result = 0 then
    Result := StrIComp(PChar(List[Index1]), PChar(List[Index2]));

  { Still no differences? Compare file extensions. }

  if Result = 0 then
    Result := StrIComp(PChar(ext1), PChar(ext2));

end;



//Поиск файлов db  время
procedure searchFiles();
var
time_gs,i,good,idx: integer;
listdepth,depthsort: TStringList;
name: string;
begin
//gPath := 'C:\Wells\GeoScape Скв  Куст 1 Пл АГКМ\';
form1.ListBox2.Clear;
Form1.Memo1.Clear();
Form1.ComboBox1.Items.Clear();
listdepth:=TStringList.Create;
depthsort:=TStringList.Create;
//Form1.Memo1.Lines.Add(gPath);
  //Все файлы, исключая тома и папки.
  CurAttr := faAnyFile;
  try
    if FindFirst(gPath +'\'+ '*.db', CurAttr, Search) = 0 then
    repeat
      begin
        time_name_ga:= StringReplace(ExtractFileName(Search.Name),ExtractFileExt(Search.Name),'',[]);
        if TryStrToInt(time_name_ga,time_gs)=True then
          begin
            Form1.Memo1.Lines.Add(Search.Name);
            Form1.ComboBox1.Items.Add(Search.Name);
            Application.ProcessMessages();
            
            //form1.ListBox2.Items.Add(Search.Name);
            name:= StringReplace(ExtractFileName(Search.Name),ExtractFileExt(Search.Name),'',[]);
            listdepth.Add(name);
            //form1.ListBox2.Items.Add(name);
          end;

      end;
    until FindNext(Search) <> 0;
  finally
    FindClose(Search);
  end;

    //Сортировка
  {if listdepth.Count>0 then begin
  good:=StrToInt(listdepth[0]);
  name:= listdepth[0];
  time_gs:=0;
  idx:= listdepth.Count;
  Repeat
    good:=StrToInt(listdepth[listdepth.Count-1]);
    name:= listdepth[listdepth.Count-1];
    for i:=0 to  listdepth.Count-1 do begin
      if  good> StrToInt(listdepth[i]) then begin
        name:=listdepth[i];
        good:= StrToInt(listdepth[i]);
      end;
    end;

  depthsort.Add(name);
  listdepth.Delete(listdepth.IndexOf(name));
  Inc(time_gs);
  until time_gs=idx;

  for i:=0 to depthsort.Count-1   do begin
    form1.ListBox2.Items.Add(depthsort[i]+'.db');
  end;
  end;}

  listdepth.CustomSort(GTSmartCompare);
  for i:=0 to listdepth.Count-1   do begin
   form1.ListBox2.Items.Add(listdepth[i]+'.db')
  end;
end;
//Поиск файлов db  глубинки
procedure searchFilesdepth();
var
time_gs,i,good,goodplus,idx: integer;
listdepth,depthsort,listdepthplus,depthsortplus: TStringList;
name, nameplus: string;
begin
listdepth:=TStringList.Create;
listdepthplus:=TStringList.Create;
depthsort:=TStringList.Create;
depthsortplus:=TStringList.Create;
form1.ListBox3.Clear;
  //Все файлы, исключая тома и папки.
  CurAttr := faAnyFile;
  try
    if FindFirst(gPath +'\'+ 'D*.*', CurAttr, Search2) = 0 then
    repeat
      begin
        //time_name_ga:= StringReplace(ExtractFileName(Search2.Name),ExtractFileExt(Search2.Name),'',[]);
             name:= StringReplace(ExtractFileName(Search2.Name),ExtractFileExt(Search2.Name),'',[]);
            if (name[1]='D') and (TryStrToInt(name[2],time_gs)=True) then begin
            listdepth.Add(name);
            end;
            if Form1.ComboBox2.ItemIndex=0 then begin
              Application.ProcessMessages();
              Sleep(1);
            end;

            
            {name:= StringReplace(ExtractFileName(Search2.Name),ExtractFileExt(Search2.Name),'',[]);
            if (name[1]='D') and (TryStrToInt(name[2],time_gs)=True) then begin
              name:=StringReplace(name, 'D', '',
                [rfIgnoreCase]);
              if  TryStrToInt(name,time_gs)=True then begin
                listdepth.Add(name);
                listdepthplus.Add('0');
              end else begin
              listdepth.Add(Copy(name,0,AnsiPos('_',name)-1));
              listdepthplus.Add(Copy(name,AnsiPos('_',name)+1,Length(name)-AnsiPos('_',name) ));


              end;

              end; }

      end;
    until FindNext(Search2) <> 0;
  finally
    FindClose(Search2);
  end;
  //Сортировка
  {if listdepth.Count>0 then begin
  good:=StrToInt(listdepth[0]);
  goodplus:=StrToInt(listdepthplus[0]);
  name:= listdepth[0];
  nameplus:= listdepthplus[0];
  time_gs:=0;
  idx:= listdepth.Count;
  Repeat
    good:=StrToInt(listdepth[listdepth.Count-1]);
    name:= listdepth[listdepth.Count-1];
    goodplus:=StrToInt(listdepthplus[listdepthplus.Count-1]);
    nameplus:= listdepthplus[listdepthplus.Count-1];
    for i:=0 to  listdepth.Count-1 do begin
      if  good> StrToInt(listdepth[i]) then begin
        good:=StrToInt(listdepth[i]);
        name:=listdepth[i];
        goodplus:=StrToInt(listdepthplus[i]);
        nameplus:=listdepthplus[i];
      end;

    end;

  depthsort.Add(name);
  depthsortplus.Add(nameplus);
  //depthsortplus.Add(name);
  listdepth.Delete(listdepth.IndexOf(name));
  listdepthplus.Delete(listdepthplus.IndexOf(nameplus));
  Inc(time_gs);
  until time_gs=idx;
 }
 listdepth.CustomSort(GTSmartCompare);
  for i:=0 to listdepth.Count-1   do begin
   form1.ListBox3.Items.Add(listdepth[i]+'.db')
  end;
  {
  for i:=0 to depthsort.Count-1   do begin
    if depthsortplus[i]='0' then
      form1.ListBox3.Items.Add('D'+depthsort[i]+'.db')
    else
      form1.ListBox3.Items.Add('D'+depthsort[i]+'_'+depthsortplus[i]+'.db');
  end;
  end;}
end;


//Поиск файлов db  глубинки BLDATA

procedure searchFilesdepthbldata();
var
time_gs: integer;
begin
form1.ListBox4.Clear;
  //Все файлы, исключая тома и папки.
  CurAttr := faAnyFile;
  try
    if FindFirst(gPath +'\'+ 'BLData.db', CurAttr, Search3) = 0 then
    repeat
      begin
        //time_name_ga:= StringReplace(ExtractFileName(Search3.Name),ExtractFileExt(Search3.Name),'',[]);

            form1.ListBox4.Items.Add(Search3.Name);
            if Form1.ComboBox2.ItemIndex=0 then begin
              Application.ProcessMessages();
              Sleep(1);
            end;
            
      end;
    until FindNext(Search3) <> 0;
  finally
    FindClose(Search3);
  end;
end;



//Запись записи LST по времени
procedure writeLstRec();
begin

  AssignFile(myFile, dPath+'Time_'+ form1.Table1.TableName +'.lst');
  //Если нет файла, создаем
  if FileExists(dPath+'Time_'+form1.Table1.TableName+'.lst')=False
  then   {$I-} Rewrite(myFile) {$I+} //Открываем типизированный файл в режиме чтение/запись.
  else {$I-} Reset(myFile); {$I+}

  Seek(myFile, FileSize(myFile)); //Переходим в конец файла.
  Write(myFile,lstrec);
  Application.ProcessMessages;
  
  CloseFile(myFile);

end;

//Запись записи LST  по глубине
procedure writeLstRecdepth();
begin

  AssignFile(myFile, dPath+'temp_str' +'.lst');
  //Если нет файла, создаем
  if FileExists(dPath+'temp_str'+'.lst')=False
  then   {$I-} Rewrite(myFile) {$I+} //Открываем типизированный файл в режиме чтение/запись.
  else {$I-} Reset(myFile); {$I+}

  Seek(myFile, FileSize(myFile)); //Переходим в конец файла.
  Write(myFile,lstrec);
  Application.ProcessMessages;
  
  CloseFile(myFile);

end;

//Чтение размера записи LST  по времени
Function getNumbsLst() : Ttimecount;
var
curdepth:TLST;
curnumb: Integer;
curdep: Integer;
begin

  AssignFile(myFile, dPath+'Time_'+ form1.Table1.TableName +'.lst');
  //Если нет файла, создаем
  if FileExists(dPath+'Time_'+form1.Table1.TableName+'.lst')=False
  then   {$I-} Rewrite(myFile) {$I+} //Открываем типизированный файл в режиме чтение/запись.
  else {$I-} Reset(myFile); {$I+}

   if FileSize(myFile)>0 then begin
  curnumb:= FileSize(myFile);
  Seek(myFile,FileSize(myFile)-1);
  Read(myFile,curdepth);
  curdep:= curdepth.TimeDos;
  Application.ProcessMessages;
  
  end else begin
   curnumb:=0;
   curdep:=0;
  end;
  CloseFile(myFile);
  Result.i:= curnumb;
  Result.S:= curdep;

end;

//Чтение размера записи LST  по глубине
Function getNumbsLstdepth() : Tdephcount;
var
curdepth:TLST;
curnumb: Integer;
curdep: Single;
begin

  AssignFile(myFile, dPath+'temp_str' +'.lst');
  //Если нет файла, создаем
  if FileExists(dPath+'temp_str'+'.lst')=False
  then   {$I-} Rewrite(myFile) {$I+} //Открываем типизированный файл в режиме чтение/запись.
  else {$I-} Reset(myFile); {$I+}
  if FileSize(myFile)>0 then begin
  curnumb:= FileSize(myFile);
  Seek(myFile,FileSize(myFile)-1);
  Read(myFile,curdepth);
  curdep:= curdepth.KeyValue;
  Application.ProcessMessages;
  
  end else begin
   curnumb:=0;
   curdep:=0;
  end;
  CloseFile(myFile);
  Result.i:= curnumb;
  Result.S:= curdep;
end;


//Запись записи DEP по времени
procedure writeDepRec();
begin
  AssignFile(FileZAG, dPath+'Time_'+form1.Table1.TableName+'.dep');
  //Если нет файла, создаем
  if FileExists(dPath+'Time_'+form1.Table1.TableName+'.dep')=False
  then   {$I-} Rewrite(FileZAG) {$I+} //Открываем типизированный файл в режиме чтение/запись.
  else {$I-} Reset(FileZAG); {$I+}

  Seek(FileZAG, FileSize(FileZAG)); //Переходим в конец файла.
  Write(FileZAG,depRecZAG);
  Application.ProcessMessages;
  
  CloseFile(FileZAG);
  {
  AssignFile(FileZAG2, 'C:\'+'Time_'+time_name_ga+'.dep');
  Reset(FileZAG2);
  Seek(FileZAG2, FileSize(FileZAG2));
  Write(FileZAG2,depRecZAG2);
  CloseFile(FileZAG2);

  AssignFile(ValDatetime, 'C:\'+'Time_'+time_name_ga+'.dep');
  Reset(ValDatetime);
  Seek(ValDatetime, FileSize(ValDatetime));
  Write(ValDatetime,depValDatetime);
  CloseFile(ValDatetime);

  depRecZAG2.NumbPar:=0;
  AssignFile(FileZAG2, 'C:\'+'Time_'+time_name_ga+'.dep');
  Reset(FileZAG2);
  Seek(FileZAG2, FileSize(FileZAG2));
  Write(FileZAG2,depRecZAG2);
  CloseFile(FileZAG2);


    AssignFile(ValFloat, 'C:\'+'Time_'+time_name_ga+'.dep');
  //Если нет файла, создаем
  if FileExists('C:\'+'Time_'+time_name_ga+'.dep')=False
  then    Rewrite(ValFloat)  //Открываем типизированный файл в режиме чтение/запись.
  else  Append(ValFloat);
  Write(ValFloat, depValFloat );
  CloseFile(ValFloat);
  }
end;


//Запись записи DEP по глубине
procedure writeDepRecdepth();
begin
  AssignFile(FileZAG, dPath+'temp_str'+'.dep');
  //Если нет файла, создаем
  if FileExists(dPath+'temp_str'+'.dep')=False
  then   {$I-} Rewrite(FileZAG) {$I+} //Открываем типизированный файл в режиме чтение/запись.
  else {$I-} Reset(FileZAG); {$I+}
  Application.ProcessMessages;
  
  Seek(FileZAG, FileSize(FileZAG)); //Переходим в конец файла.
  Write(FileZAG,depRecZAG);
  CloseFile(FileZAG);

end;




//Запись записи DEP по глубине  BLDATA
procedure readwriteDepRecdepthbldata();
var
i,idx1,idy1,shut: Integer;
GID,s,ss: string;
AAA: Double;
begin
   shut:=0;
  //Есть ли файла
  if (FileExists(dPath+'temp_str'+'.dep')=True) and (FileExists(gPath+'\BLData.db')=True)
  then    begin
  form1.Table5.Active:= False;
  form1.Table5.TableName:= 'BLData.db';
  form1.Table5.Active:= True;
  form1.Button14.Enabled:= False;
  AssignFile(FileZAG, dPath+'temp_str'+'.dep');
  {$I-} Reset(FileZAG); {$I+}
   //Переходим в начало
  form1.ProgressBar3.Min:=0;
  form1.ProgressBar3.Position:=0;
  form1.ProgressBar3.Max:= FileSize(FileZAG);
  //BLDATA в массив rec-кордов
  SetLength( BLDATA, (Form1.Table5.RecordCount-1)*8*64 );
  Form1.Table5.Active:=False;
  Form1.Table5.Active:=True;
  Form1.Table5.First;
  for idx1:=0 to Form1.Table5.RecordCount-1 do begin

    BLDATA[idx1].GAZDEPTH:= form1.Table5.FieldByName('S113').AsFloat;
    BLDATA[idx1].C1:= form1.Table5.FieldByName('S1601').AsFloat;
    BLDATA[idx1].C2:= form1.Table5.FieldByName('S1602').AsFloat;
    BLDATA[idx1].C3:= form1.Table5.FieldByName('S1603').AsFloat;
    BLDATA[idx1].C4:= form1.Table5.FieldByName('S1604').AsFloat;
    BLDATA[idx1].C5:= form1.Table5.FieldByName('S1605').AsFloat;
    BLDATA[idx1].CSUM:= form1.Table5.FieldByName('S1600').AsFloat;
    Form1.Table5.Next;
  end;
  //form1.ListBox5.Items.Add(IntToStr( Form1.Table5.RecordCount));

  //поиск глубины забоя = глубине газа
  for i:=0 to FileSize(FileZAG)-1 do begin
    //Чтение
    Seek(FileZAG, i);
    Read (FileZAG,depRecZAG);
    for idx1:=0 to form1.Table5.RecordCount-1 do begin
      if  depRecZAG.val53 = BLDATA[idx1].GAZDEPTH then begin
        depRecZAG.val16:= BLDATA[idx1].C1;
        depRecZAG.val17:= BLDATA[idx1].C2;
        depRecZAG.val18:= BLDATA[idx1].C3;
        depRecZAG.val20:= BLDATA[idx1].C4;
        depRecZAG.val21:= BLDATA[idx1].C5;
        depRecZAG.val152:= BLDATA[idx1].CSUM;
        Inc(shut);
        Application.ProcessMessages;
        
      end;

    end;

   form1.ProgressBar3.Position:= form1.ProgressBar3.Position+1;
  // Запись
    Seek(FileZAG, i);
    Write (FileZAG,depRecZAG);
  end;
  CloseFile(FileZAG);
  end;
  //form1.ListBox5.Items.Add(IntToStr( shut));
  SetLength( BLDATA, 0);
  form1.Button14.Enabled:= True;
end;


//Заполнение записи DEP без заголовка
procedure setrec();
begin
  //Подзаголовок номер справочника и номер параметра
    depRecZAG.NSprav0:= 1;
    depRecZAG.NPar0:=0;
    depRecZAG.NSprav1:= 1;
    depRecZAG.NPar1:=1;
    depRecZAG.NSprav2:= 1;
    Application.ProcessMessages;
    
    depRecZAG.NPar2:=2;
    depRecZAG.NSprav3:= 1;
    depRecZAG.NPar3:=3;
    depRecZAG.NSprav4:= 1;
    depRecZAG.NPar4:=4;
    depRecZAG.NSprav5:= 1;
    depRecZAG.NPar5:=5;
    depRecZAG.NSprav6:= 1;
    depRecZAG.NPar6:=6;
    depRecZAG.NSprav7:= 1;
    depRecZAG.NPar7:=7;
    depRecZAG.NSprav8:= 1;
    depRecZAG.NPar8:=8;
    depRecZAG.NSprav9:= 1;
    depRecZAG.NPar9:=9;
    depRecZAG.NSprav10:= 1;
    depRecZAG.NPar10:=10;
    depRecZAG.NSprav11:= 1;
    depRecZAG.NPar11:=11;
    depRecZAG.NSprav12:= 1;
    depRecZAG.NPar12:=12;
    depRecZAG.NSprav13:= 1;
    depRecZAG.NPar13:=13;
    depRecZAG.NSprav14:= 1;
    depRecZAG.NPar14:=14;
    depRecZAG.NSprav15:= 1;
    depRecZAG.NPar15:=15;
    depRecZAG.NSprav16:= 1;
    depRecZAG.NPar16:=16;
    depRecZAG.NSprav17:= 1;
    depRecZAG.NPar17:=17;
    depRecZAG.NSprav18:= 1;
    Application.ProcessMessages;
    
    depRecZAG.NPar18:=18;
    depRecZAG.NSprav19:= 1;
    depRecZAG.NPar19:=19;
    depRecZAG.NSprav20:= 1;
    depRecZAG.NPar20:=20;
    depRecZAG.NSprav21:= 1;
    depRecZAG.NPar21:=21;
    depRecZAG.NSprav22:= 1;
    depRecZAG.NPar22:=22;
    depRecZAG.NSprav23:= 1;
    depRecZAG.NPar23:=23;
    depRecZAG.NSprav24:= 1;
    depRecZAG.NPar24:=24;
    depRecZAG.NSprav25:= 1;
    depRecZAG.NPar25:=25;
    depRecZAG.NSprav26:= 1;
    depRecZAG.NPar26:=26;
    depRecZAG.NSprav27:= 1;
    depRecZAG.NPar27:=27;
    depRecZAG.NSprav28:= 1;
    depRecZAG.NPar28:=28;
    depRecZAG.NSprav29:= 1;
    depRecZAG.NPar29:=29;
    depRecZAG.NSprav30:= 1;
    depRecZAG.NPar30:=30;
    depRecZAG.NSprav31:= 1;
    depRecZAG.NPar31:=31;
    depRecZAG.NSprav32:= 1;
    depRecZAG.NPar32:=32;
    depRecZAG.NSprav33:= 1;
    depRecZAG.NPar33:=33;
    depRecZAG.NSprav34:= 1;
    depRecZAG.NPar34:=34;
    depRecZAG.NSprav37:= 1;
    depRecZAG.NPar37:=37;
    depRecZAG.NSprav38:= 1;
    depRecZAG.NPar38:=38;
    depRecZAG.NSprav39:= 1;
    depRecZAG.NPar39:=39;
    depRecZAG.NSprav40:= 1;
    depRecZAG.NPar40:=40;
    depRecZAG.NSprav41:= 1;
    depRecZAG.NPar41:=41;
    depRecZAG.NSprav42:= 1;
    depRecZAG.NPar42:=42;
    depRecZAG.NSprav43:= 1;
    Application.ProcessMessages;
    
    depRecZAG.NPar43:=43;
    depRecZAG.NSprav44:= 1;
    depRecZAG.NPar44:=44;
    depRecZAG.NSprav45:= 1;
    depRecZAG.NPar45:=45;
    depRecZAG.NSprav46:= 1;
    depRecZAG.NPar46:=46;
    depRecZAG.NSprav47:= 1;
    depRecZAG.NPar47:=47;
    depRecZAG.NSprav48:= 1;
    depRecZAG.NPar48:=48;
    depRecZAG.NSprav49:= 1;
    depRecZAG.NPar49:=49;
    depRecZAG.NSprav50:= 1;
    depRecZAG.NPar50:=50;
    depRecZAG.NSprav51:= 1;
    depRecZAG.NPar51:=51;
    depRecZAG.NSprav53:= 1;
    depRecZAG.NPar53:=53;
    depRecZAG.NSprav54:= 1;
    depRecZAG.NPar54:=54;
    depRecZAG.NSprav55:= 1;
    depRecZAG.NPar55:=55;
    depRecZAG.NSprav56:= 1;
    depRecZAG.NPar56:=56;
    depRecZAG.NSprav57:= 1;
    depRecZAG.NPar57:=57;
    depRecZAG.NSprav58:= 1;
    depRecZAG.NPar58:=58;
    depRecZAG.NSprav59:= 1;
    depRecZAG.NPar59:=59;
    depRecZAG.NSprav60:= 1;
    depRecZAG.NPar60:=60;
    depRecZAG.NSprav61:= 1;
    depRecZAG.NPar61:=61;
    depRecZAG.NSprav62:= 1;
    depRecZAG.NPar62:=62;
    depRecZAG.NSprav63:= 1;
    Application.ProcessMessages;
    
    depRecZAG.NPar63:=63;
    depRecZAG.NSprav64:= 1;
    depRecZAG.NPar64:=64;
    depRecZAG.NSprav65:= 1;
    depRecZAG.NPar65:=65;
    depRecZAG.NSprav66:= 1;
    depRecZAG.NPar66:=66;
    depRecZAG.NSprav67:= 1;
    depRecZAG.NPar67:=67;
    depRecZAG.NSprav68:= 1;
    depRecZAG.NPar68:=68;
    depRecZAG.NSprav69:= 1;
    depRecZAG.NPar69:=69;
    depRecZAG.NSprav70:= 1;
    depRecZAG.NPar70:=70;
    depRecZAG.NSprav71:= 1;
    depRecZAG.NPar71:=71;
    depRecZAG.NSprav72:= 1;
    depRecZAG.NPar72:=72;
    depRecZAG.NSprav74:= 1;
    depRecZAG.NPar74:=74;
    depRecZAG.NSprav76:= 1;
    depRecZAG.NPar76:=76;
    depRecZAG.NSprav77:= 1;
    depRecZAG.NPar77:=77;
    depRecZAG.NSprav79:= 1;
    depRecZAG.NPar79:=79;
    depRecZAG.NSprav80:= 1;
    depRecZAG.NPar80:=80;
    depRecZAG.NSprav81:= 1;
    depRecZAG.NPar81:=81;
    depRecZAG.NSprav82:= 1;
    depRecZAG.NPar82:=82;
    depRecZAG.NSprav83:= 1;
    depRecZAG.NPar83:=83;
    depRecZAG.NSprav84:= 1;
    depRecZAG.NPar84:=84;
    depRecZAG.NSprav85:= 1;
    depRecZAG.NPar85:=85;
    depRecZAG.NSprav87:= 1;
    depRecZAG.NPar87:=87;
    depRecZAG.NSprav88:= 1;
    depRecZAG.NPar88:=88;
    depRecZAG.NSprav89:= 1;
    depRecZAG.NPar89:=89;
    depRecZAG.NSprav90:= 1;
    depRecZAG.NPar90:=90;
    depRecZAG.NSprav91:= 1;
    depRecZAG.NPar91:=91;
    depRecZAG.NSprav92:= 1;
    depRecZAG.NPar92:=92;
    depRecZAG.NSprav93:= 1;
    depRecZAG.NPar93:=93;
    depRecZAG.NSprav94:= 1;
    depRecZAG.NPar94:=94;
    Application.ProcessMessages;
    
    depRecZAG.NSprav95:= 1;
    depRecZAG.NPar95:=95;
    depRecZAG.NSprav96:= 1;
    depRecZAG.NPar96:=96;
    depRecZAG.NSprav97:= 1;
    depRecZAG.NPar97:=97;
    depRecZAG.NSprav98:= 1;
    depRecZAG.NPar98:=98;
    depRecZAG.NSprav99:= 1;
    depRecZAG.NPar99:=99;
    depRecZAG.NSprav100:= 1;
    depRecZAG.NPar100:=100;
    depRecZAG.NSprav101:= 1;
    depRecZAG.NPar101:=101;
    depRecZAG.NSprav102:= 1;
    depRecZAG.NPar102:=102;
    depRecZAG.NSprav104:= 1;
    depRecZAG.NPar104:=104;
    depRecZAG.NSprav105:= 1;
    depRecZAG.NPar105:=105;
    depRecZAG.NSprav106:= 1;
    depRecZAG.NPar106:=106;
    depRecZAG.NSprav114:= 1;
    depRecZAG.NPar114:=114;
    depRecZAG.NSprav115:= 1;
    depRecZAG.NPar115:=115;
    depRecZAG.NSprav116:= 1;
    depRecZAG.NPar116:=116;
    depRecZAG.NSprav117:= 1;
    depRecZAG.NPar117:=117;
    depRecZAG.NSprav118:= 1;
    depRecZAG.NPar118:=118;
    depRecZAG.NSprav119:= 1;
    depRecZAG.NPar119:=119;
    depRecZAG.NSprav120:= 1;
    depRecZAG.NPar120:=120;
    depRecZAG.NSprav121:= 1;
    depRecZAG.NPar121:=121;
    depRecZAG.NSprav122:= 1;
    depRecZAG.NPar122:=122;
    depRecZAG.NSprav123:= 1;
    depRecZAG.NPar123:=123;
    depRecZAG.NSprav124:= 1;
    depRecZAG.NPar124:=124;
    depRecZAG.NSprav127:= 1;
    Application.ProcessMessages;
    
    depRecZAG.NPar127:=127;
    depRecZAG.NSprav128:= 1;
    depRecZAG.NPar128:=128;
    depRecZAG.NSprav129:= 1;
    depRecZAG.NPar129:=129;
    depRecZAG.NSprav130:= 1;
    depRecZAG.NPar130:=130;
    depRecZAG.NSprav133:= 1;
    depRecZAG.NPar133:=133;
    depRecZAG.NSprav134:= 1;
    depRecZAG.NPar134:=134;
    depRecZAG.NSprav135:= 1;
    depRecZAG.NPar135:=135;
    depRecZAG.NSprav136:= 1;
    depRecZAG.NPar136:=136;
    depRecZAG.NSprav137:= 1;
    depRecZAG.NPar137:=137;
    depRecZAG.NSprav138:= 1;
    depRecZAG.NPar138:=138;
    depRecZAG.NSprav139:= 1;
    depRecZAG.NPar139:=139;
    depRecZAG.NSprav140:= 1;
    depRecZAG.NPar140:=140;
    depRecZAG.NSprav141:= 1;
    depRecZAG.NPar141:=141;
    depRecZAG.NSprav142:= 1;
    depRecZAG.NPar142:=142;
    depRecZAG.NSprav143:= 1;
    depRecZAG.NPar143:=143;
    depRecZAG.NSprav144:= 1;
    depRecZAG.NPar144:=144;
    depRecZAG.NSprav145:= 1;
    depRecZAG.NPar145:=145;
    depRecZAG.NSprav146:= 1;
    depRecZAG.NPar146:=146;
    depRecZAG.NSprav147:= 1;
    depRecZAG.NPar147:=147;
    depRecZAG.NSprav149:= 1;
    depRecZAG.NPar149:=149;
    depRecZAG.NSprav151:= 1;
    depRecZAG.NPar151:=151;
    depRecZAG.NSprav152:= 1;
    Application.ProcessMessages;
    
    depRecZAG.NPar152:=152;
    depRecZAG.NSprav153:= 1;
    depRecZAG.NPar153:=153;
    depRecZAG.NSprav154:= 1;
    depRecZAG.NPar154:=154;
    depRecZAG.NSprav155:= 1;
    depRecZAG.NPar155:=155;
    depRecZAG.NSprav156:= 1;
    depRecZAG.NPar156:=156;
    depRecZAG.NSprav157:= 1;
    depRecZAG.NPar157:=157;
    depRecZAG.NSprav158:= 1;
    depRecZAG.NPar158:=158;
    depRecZAG.NSprav159:= 1;
    depRecZAG.NPar159:=159;
    depRecZAG.NSprav160:= 1;
    depRecZAG.NPar160:=160;
    depRecZAG.NSprav161:= 1;
    depRecZAG.NPar161:=161;
    depRecZAG.NSprav162:= 1;
    depRecZAG.NPar162:=162;
    depRecZAG.NSprav163:= 1;
    depRecZAG.NPar163:=163;
    depRecZAG.NSprav164:= 1;
    depRecZAG.NPar164:=164;
    depRecZAG.NSprav165:= 1;
    depRecZAG.NPar165:=165;
    depRecZAG.NSprav166:= 1;
    depRecZAG.NPar166:=166;
    depRecZAG.NSprav167:= 1;
    depRecZAG.NPar167:=167;
    depRecZAG.NSprav168:= 1;
    depRecZAG.NPar168:=168;
    depRecZAG.NSprav169:= 1;
    depRecZAG.NPar169:=169;
    depRecZAG.NSprav170:= 1;
    depRecZAG.NPar170:=170;
    depRecZAG.NSprav171:= 1;
    depRecZAG.NPar171:=171;
    depRecZAG.NSprav172:= 1;
    depRecZAG.NPar172:=172;
    Application.ProcessMessages;
    
    depRecZAG.NSprav173:= 1;
    depRecZAG.NPar173:=173;
    depRecZAG.NSprav174:= 1;
    depRecZAG.NPar174:=174;
    depRecZAG.NSprav175:= 1;
    depRecZAG.NPar175:=175;
    depRecZAG.NSprav176:= 1;
    depRecZAG.NPar176:=176;
    depRecZAG.NSprav177:= 1;
    depRecZAG.NPar177:=177;
    depRecZAG.NSprav178:= 1;
    depRecZAG.NPar178:=178;
    depRecZAG.NSprav179:= 1;
    depRecZAG.NPar179:=179;
    depRecZAG.NSprav180:= 1;
    depRecZAG.NPar180:=180;
    depRecZAG.NSprav181:= 1;
    depRecZAG.NPar181:=181;
    depRecZAG.NSprav182:= 1;
    depRecZAG.NPar182:=182;
    depRecZAG.NSprav183:= 1;
    depRecZAG.NPar183:=183;
    depRecZAG.NSprav184:= 1;
    depRecZAG.NPar184:=184;
    depRecZAG.NSprav185:= 1;
    depRecZAG.NPar185:=185;
    depRecZAG.NSprav186:= 1;
    Application.ProcessMessages;
    
    depRecZAG.NPar186:=186;
    depRecZAG.NSprav187:= 1;
    depRecZAG.NPar187:=187;
    depRecZAG.NSprav188:= 1;
    depRecZAG.NPar188:=188;
    depRecZAG.NSprav189:= 1;
    depRecZAG.NPar189:=189;
    depRecZAG.NSprav191:= 1;
    depRecZAG.NPar191:=191;
    depRecZAG.NSprav192:= 1;
    depRecZAG.NPar192:=192;
    depRecZAG.NSprav193:= 1;
    depRecZAG.NPar193:=193;
    depRecZAG.NSprav194:= 1;
    depRecZAG.NPar194:=194;
    depRecZAG.NSprav195:= 1;
    depRecZAG.NPar195:=195;
    depRecZAG.NSprav196:= 1;
    depRecZAG.NPar196:=196;
    depRecZAG.NSprav197:= 1;
    depRecZAG.NPar197:=197;
    depRecZAG.NSprav198:= 1;
    depRecZAG.NPar198:=198;
    depRecZAG.NSprav199:= 1;
    depRecZAG.NPar199:=199;
    depRecZAG.NSprav200:= 1;
    depRecZAG.NPar200:=200;
    depRecZAG.NSprav201:= 1;
    depRecZAG.NPar201:=201;
    depRecZAG.NSprav202:= 1;
    depRecZAG.NPar202:=202;
    depRecZAG.NSprav203:= 1;
    depRecZAG.NPar203:=203;
    depRecZAG.NSprav204:= 1;
    depRecZAG.NPar204:=204;
    depRecZAG.NSprav205:= 1;
    depRecZAG.NPar205:=205;
    depRecZAG.NSprav206:= 1;
    depRecZAG.NPar206:=206;
    depRecZAG.NSprav207:= 1;
    Application.ProcessMessages;
    
    depRecZAG.NPar207:=207;
    depRecZAG.NSprav208:= 1;
    depRecZAG.NPar208:=208;
    depRecZAG.NSprav209:= 1;
    depRecZAG.NPar209:=209;
    depRecZAG.NSprav210:= 1;
    depRecZAG.NPar210:=210;
    depRecZAG.NSprav211:= 1;
    depRecZAG.NPar211:=211;
    depRecZAG.NSprav215:= 1;
    depRecZAG.NPar215:=215;
    depRecZAG.NSprav216:= 1;
    depRecZAG.NPar216:=216;
    depRecZAG.NSprav217:= 1;
    depRecZAG.NPar217:=217;
    depRecZAG.NSprav218:= 1;
    depRecZAG.NPar218:=218;
    depRecZAG.NSprav219:= 1;
    depRecZAG.NPar219:=219;
    depRecZAG.NSprav220:= 1;
    depRecZAG.NPar220:=220;
    depRecZAG.NSprav221:= 1;
    depRecZAG.NPar221:=221;
    depRecZAG.NSprav222:= 1;
    depRecZAG.NPar222:=222;
    depRecZAG.NSprav223:= 1;
    Application.ProcessMessages;
    
    depRecZAG.NPar223:=223;
    depRecZAG.NSprav224:= 1;
    depRecZAG.NPar224:=224;
    depRecZAG.NSprav225:= 1;
    depRecZAG.NPar225:=225;
    depRecZAG.NSprav226:= 1;
    depRecZAG.NPar226:=226;
    depRecZAG.NSprav227:= 1;
    depRecZAG.NPar227:=227;
    depRecZAG.NSprav228:= 1;
    depRecZAG.NPar228:=228;
    depRecZAG.NSprav229:= 1;
    depRecZAG.NPar229:=229;
    depRecZAG.NSprav230:= 1;
    depRecZAG.NPar230:=230;
    depRecZAG.NSprav231:= 1;
    depRecZAG.NPar231:=231;
    depRecZAG.NSprav235:= 1;
    depRecZAG.NPar235:=235;
    depRecZAG.NSprav236:= 1;
    depRecZAG.NPar236:=236;
    depRecZAG.NSprav237:= 1;
    depRecZAG.NPar237:=237;
    depRecZAG.NSprav238:= 1;
    depRecZAG.NPar238:=238;
    depRecZAG.NSprav239:= 1;
    depRecZAG.NPar239:=239;
    depRecZAG.NSprav240:= 1;
    depRecZAG.NPar240:=240;
    depRecZAG.NSprav241:= 1;
    depRecZAG.NPar241:=241;
    depRecZAG.NSprav242:= 1;
    depRecZAG.NPar242:=242;
    depRecZAG.NSprav243:= 1;
    depRecZAG.NPar243:=243;
    depRecZAG.NSprav244:= 1;
    depRecZAG.NPar244:=244;
    depRecZAG.NSprav245:= 1;
    depRecZAG.NPar245:=245;
    depRecZAG.NSprav246:= 1;
    Application.ProcessMessages;
    
    depRecZAG.NPar246:=246;
    depRecZAG.NSprav247:= 1;
    depRecZAG.NPar247:=247;
    depRecZAG.NSprav248:= 1;
    depRecZAG.NPar248:=248;
    depRecZAG.NSprav249:= 1;
    depRecZAG.NPar249:=249;
    depRecZAG.NSprav250:= 1;
    depRecZAG.NPar250:=250;
    depRecZAG.NSprav251:= 1;
    depRecZAG.NPar251:=251;
    depRecZAG.NSprav252:= 1;
    depRecZAG.NPar252:=252;
    depRecZAG.NSprav253:= 1;
    depRecZAG.NPar253:=253;

    //Значения f
    depRecZAG.val0:= ValF[0][1];
    depRecZAG.val1:= ValF[1][1];
    depRecZAG.val2:= ValF[2][1];
    depRecZAG.val3:= ValF[3][1];
    depRecZAG.val4:= ValF[4][1];
    depRecZAG.val5:= ValF[5][1];
    depRecZAG.val6:= ValF[6][1];
    depRecZAG.val7:= ValF[7][1];
    depRecZAG.val8:= ValF[8][1];
    depRecZAG.val9:= ValF[9][1];
    depRecZAG.val10:= ValF[10][1];
    depRecZAG.val11:= ValF[11][1];
    depRecZAG.val12:= ValF[12][1];
    depRecZAG.val13:= ValF[13][1];
    depRecZAG.val14:= ValF[14][1];
    depRecZAG.val15:= ValF[15][1];
    depRecZAG.val16:= ValF[16][1];
    Application.ProcessMessages;
    
    depRecZAG.val17:= ValF[17][1];
    depRecZAG.val18:= ValF[18][1];
    depRecZAG.val19:= ValF[19][1];
    depRecZAG.val20:= ValF[20][1];
    depRecZAG.val21:= ValF[21][1];
    depRecZAG.val22:= ValF[22][1];
    depRecZAG.val23:= ValF[23][1];
    depRecZAG.val24:= ValF[24][1];
    depRecZAG.val25:= ValF[25][1];
    depRecZAG.val26:= ValF[26][1];
    depRecZAG.val27:= ValF[27][1];
    depRecZAG.val28:= ValF[28][1];
    depRecZAG.val29:= ValF[29][1];
    depRecZAG.val30:= ValF[30][1];
    depRecZAG.val31:= ValF[31][1];
    depRecZAG.val32:= ValF[32][1];
    depRecZAG.val33:= ValF[33][1];
    depRecZAG.val34:= ValF[34][1];
    depRecZAG.val37:= ValF[35][1];
    depRecZAG.val38:= ValF[36][1];
    depRecZAG.val39:= ValF[37][1];
    depRecZAG.val40:= ValF[38][1];
    depRecZAG.val41:= ValF[39][1];
    depRecZAG.val42:= ValF[40][1];
    depRecZAG.val43:= ValF[41][1];
    depRecZAG.val44:= ValF[42][1];
    depRecZAG.val45:= ValF[43][1];
    depRecZAG.val46:= ValF[44][1];
    depRecZAG.val47:= ValF[45][1];
    depRecZAG.val48:= ValF[46][1];
    depRecZAG.val49:= ValF[47][1];
    depRecZAG.val50:= ValF[48][1];
    depRecZAG.val51:= ValF[49][1];
    depRecZAG.val53:= ValF[50][1];
    depRecZAG.val54:= ValF[51][1];
    depRecZAG.val55:= ValF[52][1];
    depRecZAG.val56:= ValF[53][1];
    depRecZAG.val57:= ValF[54][1];
    Application.ProcessMessages;
    
    depRecZAG.val58:= ValF[55][1];
    depRecZAG.val59:= ValF[56][1];
    depRecZAG.val60:= ValF[57][1];
    depRecZAG.val61:= ValF[58][1];
    depRecZAG.val62:= ValF[59][1];
    depRecZAG.val63:= ValF[60][1];
    depRecZAG.val64:= ValF[61][1];
    depRecZAG.val65:= ValF[62][1];
    depRecZAG.val66:= ValF[63][1];
    depRecZAG.val67:= ValF[64][1];
    depRecZAG.val68:= ValF[65][1];
    depRecZAG.val69:= ValF[66][1];
    depRecZAG.val70:= ValF[67][1];
    depRecZAG.val71:= ValF[68][1];
    depRecZAG.val72:= ValF[69][1];
    depRecZAG.val74:= ValF[70][1];
    depRecZAG.val76:= ValF[71][1];
    depRecZAG.val77:= ValF[72][1];
    depRecZAG.val79:= ValF[73][1];
    depRecZAG.val80:= ValF[74][1];
    depRecZAG.val81:= ValF[75][1];
    depRecZAG.val82:= ValF[76][1];
    depRecZAG.val83:= ValF[77][1];
    depRecZAG.val84:= ValF[78][1];
    depRecZAG.val85:= ValF[79][1];
    depRecZAG.val87:= ValF[80][1];
    depRecZAG.val88:= ValF[81][1];
    depRecZAG.val89:= ValF[82][1];
    depRecZAG.val90:= ValF[83][1];
    depRecZAG.val91:= ValF[84][1];
    depRecZAG.val92:= ValF[85][1];
    depRecZAG.val93:= ValF[86][1];
    depRecZAG.val94:= ValF[87][1];
    Application.ProcessMessages;
    
    depRecZAG.val95:= ValF[88][1];
    depRecZAG.val96:= ValF[89][1];
    depRecZAG.val97:= ValF[90][1];
    depRecZAG.val98:= ValF[91][1];
    depRecZAG.val99:= ValF[92][1];
    depRecZAG.val100:= ValF[93][1];
    depRecZAG.val101:= ValF[94][1];
    depRecZAG.val102:= ValF[95][1];
    depRecZAG.val104:= ValF[96][1];
    depRecZAG.val105:= ValF[97][1];
    depRecZAG.val106:= ValF[98][1];
    depRecZAG.val114:= ValF[99][1];
    depRecZAG.val115:= ValF[100][1];
    depRecZAG.val116:= ValF[101][1];
    depRecZAG.val117:= ValF[102][1];
    depRecZAG.val118:= ValF[103][1];
    depRecZAG.val119:= ValF[104][1];
    depRecZAG.val120:= ValF[105][1];
    depRecZAG.val121:= ValF[106][1];
    depRecZAG.val122:= ValF[107][1];
    depRecZAG.val123:= ValF[108][1];
    depRecZAG.val124:= ValF[109][1];
    Application.ProcessMessages;
    
    depRecZAG.val127:= ValF[110][1];
    depRecZAG.val128:= ValF[111][1];
    depRecZAG.val129:= ValF[112][1];
    depRecZAG.val130:= ValF[113][1];
    depRecZAG.val133:= ValF[114][1];
    depRecZAG.val134:= ValF[115][1];
    depRecZAG.val135:= ValF[116][1];
    depRecZAG.val136:= ValF[117][1];
    depRecZAG.val137:= ValF[118][1];
    depRecZAG.val138:= ValF[119][1];
    depRecZAG.val139:= ValF[120][1];
    depRecZAG.val140:= ValF[121][1];
    depRecZAG.val141:= ValF[122][1];
    depRecZAG.val142:= ValF[123][1];
    depRecZAG.val143:= ValF[124][1];
    depRecZAG.val144:= ValF[125][1];
    depRecZAG.val145:= ValF[126][1];
    depRecZAG.val146:= ValF[127][1];
    depRecZAG.val147:= ValF[128][1];
    depRecZAG.val149:= ValF[129][1];
    Application.ProcessMessages;
    
    depRecZAG.val151:= ValF[130][1];
    depRecZAG.val152:= ValF[131][1];
    depRecZAG.val153:= ValF[132][1];
    depRecZAG.val154:= ValF[133][1];
    depRecZAG.val155:= ValF[134][1];
    depRecZAG.val156:= ValF[135][1];
    depRecZAG.val157:= ValF[136][1];
    depRecZAG.val158:= ValF[137][1];
    depRecZAG.val159:= ValF[138][1];
    depRecZAG.val160:= ValF[139][1];
    depRecZAG.val161:= ValF[140][1];
    depRecZAG.val162:= ValF[141][1];
    depRecZAG.val163:= ValF[142][1];
    depRecZAG.val164:= ValF[143][1];
    depRecZAG.val165:= ValF[144][1];
    depRecZAG.val166:= ValF[145][1];
    depRecZAG.val167:= ValF[146][1];
    depRecZAG.val168:= ValF[147][1];
    depRecZAG.val169:= ValF[148][1];
    depRecZAG.val170:= ValF[149][1];
    depRecZAG.val171:= ValF[150][1];
    depRecZAG.val172:= ValF[151][1];
    depRecZAG.val173:= ValF[152][1];
    depRecZAG.val174:= ValF[153][1];
    depRecZAG.val175:= ValF[154][1];
    depRecZAG.val176:= ValF[155][1];
    depRecZAG.val177:= ValF[156][1];
    depRecZAG.val178:= ValF[157][1];
    depRecZAG.val179:= ValF[158][1];
    depRecZAG.val180:= ValF[159][1];
    depRecZAG.val181:= ValF[160][1];
    depRecZAG.val182:= ValF[161][1];
    depRecZAG.val183:= ValF[162][1];
    depRecZAG.val184:= ValF[163][1];
    depRecZAG.val185:= ValF[164][1];
    depRecZAG.val186:= ValF[165][1];
    depRecZAG.val187:= ValF[166][1];
    depRecZAG.val188:= ValF[167][1];
    depRecZAG.val189:= ValF[168][1];
    depRecZAG.val191:= ValF[169][1];
    depRecZAG.val192:= ValF[170][1];
    Application.ProcessMessages;
    
    depRecZAG.val193:= ValF[171][1];
    depRecZAG.val194:= ValF[172][1];
    depRecZAG.val195:= ValF[173][1];
    depRecZAG.val196:= ValF[174][1];
    depRecZAG.val197:= ValF[175][1];
    depRecZAG.val198:= ValF[176][1];
    depRecZAG.val199:= ValF[177][1];
    depRecZAG.val200:= ValF[178][1];
    depRecZAG.val201:= ValF[179][1];
    depRecZAG.val202:= ValF[180][1];
    depRecZAG.val203:= ValF[181][1];
    depRecZAG.val204:= ValF[182][1];
    depRecZAG.val205:= ValF[183][1];
    depRecZAG.val206:= ValF[184][1];
    depRecZAG.val207:= ValF[185][1];
    depRecZAG.val208:= ValF[186][1];
    depRecZAG.val209:= ValF[187][1];
    depRecZAG.val210:= ValF[188][1];
    depRecZAG.val211:= ValF[189][1];
    depRecZAG.val215:= ValF[190][1];
    depRecZAG.val216:= ValF[191][1];
    depRecZAG.val217:= ValF[192][1];
    depRecZAG.val218:= ValF[193][1];
    depRecZAG.val219:= ValF[194][1];
    depRecZAG.val220:= ValF[195][1];
    depRecZAG.val221:= ValF[196][1];
    depRecZAG.val222:= ValF[197][1];
    depRecZAG.val223:= ValF[198][1];
    depRecZAG.val224:= ValF[199][1];
    depRecZAG.val225:= ValF[200][1];
    depRecZAG.val226:= ValF[201][1];
    depRecZAG.val227:= ValF[202][1];
    depRecZAG.val228:= ValF[203][1];
    depRecZAG.val229:= ValF[204][1];
    depRecZAG.val230:= ValF[205][1];
    depRecZAG.val231:= ValF[206][1];
    depRecZAG.val235:= ValF[207][1];
    depRecZAG.val236:= ValF[208][1];
    depRecZAG.val237:= ValF[209][1];
    depRecZAG.val238:= ValF[210][1];
    depRecZAG.val239:= ValF[211][1];
    depRecZAG.val240:= ValF[212][1];
    depRecZAG.val241:= ValF[213][1];
    depRecZAG.val242:= ValF[214][1];
    depRecZAG.val243:= ValF[215][1];
    depRecZAG.val244:= ValF[216][1];
    depRecZAG.val245:= ValF[217][1];
    depRecZAG.val246:= ValF[218][1];
    depRecZAG.val247:= ValF[219][1];
    depRecZAG.val248:= ValF[220][1];
    depRecZAG.val249:= ValF[221][1];
    depRecZAG.val250:= ValF[222][1];
    depRecZAG.val251:= ValF[223][1];
    depRecZAG.val252:= ValF[224][1];
    depRecZAG.val253:= ValF[225][1];
    Application.ProcessMessages;
    


    //i
    depRecZAG.NSprav73:= 1;
    depRecZAG.NPar73:=73;
    depRecZAG.NSprav78:= 1;
    depRecZAG.NPar78:=78;
    depRecZAG.NSprav103:= 1;
    depRecZAG.NPar103:=103;
    depRecZAG.NSprav107:= 1;
    depRecZAG.NPar107:=107;
    depRecZAG.NSprav108:= 1;
    depRecZAG.NPar108:=108;
    depRecZAG.NSprav109:= 1;
    depRecZAG.NPar109:=109;
    depRecZAG.NSprav110:= 1;
    depRecZAG.NPar110:=110;
    depRecZAG.NSprav111:= 1;
    depRecZAG.NPar111:=111;
    depRecZAG.NSprav112:= 1;
    Application.ProcessMessages;
    
    depRecZAG.NPar112:=112;
    depRecZAG.NSprav113:= 1;
    depRecZAG.NPar113:=113;
    depRecZAG.NSprav131:= 1;
    depRecZAG.NPar131:=131;
    depRecZAG.NSprav132:= 1;
    depRecZAG.NPar132:=132;
    depRecZAG.NSprav150:= 1;
    depRecZAG.NPar150:=150;
    depRecZAG.NSprav190:= 1;
    depRecZAG.NPar190:=190;
    depRecZAG.NSprav212:= 1;
    depRecZAG.NPar212:=212;

    depRecZAG.val73:= ValI[0][1];
    depRecZAG.val78:= ValI[1][1];
    depRecZAG.val103:= ValI[2][1];
    depRecZAG.val107:= ValI[3][1];
    depRecZAG.val108:= ValI[4][1];
    depRecZAG.val109:= ValI[5][1];
    depRecZAG.val110:= ValI[6][1];
    depRecZAG.val111:= ValI[7][1];
    depRecZAG.val112:= ValI[8][1];
    depRecZAG.val113:= ValI[9][1];
    depRecZAG.val131:= ValI[10][1];
    depRecZAG.val132:= ValI[11][1];
    depRecZAG.val150:= ValI[12][1];
    depRecZAG.val190:= ValI[13][1];
    depRecZAG.val212:= ValI[14][1];

    //l
    depRecZAG.NSprav35:= 1;
    depRecZAG.NPar35:=35;
    depRecZAG.NSprav36:= 1;
    depRecZAG.NPar36:=36;
    depRecZAG.NSprav52:= 1;
    depRecZAG.NPar52:=52;
    depRecZAG.NSprav75:= 1;
    depRecZAG.NPar75:=75;
    depRecZAG.NSprav213:= 1;
    depRecZAG.NPar213:=213;
    depRecZAG.NSprav214:= 1;
    depRecZAG.NPar214:=214;
    depRecZAG.NSprav233:= 1;
    depRecZAG.NPar233:=233;
    depRecZAG.NSprav234:= 1;
    depRecZAG.NPar234:=234;

    depRecZAG.val35:= ValL[0][1];
    depRecZAG.val36:= ValL[1][1];
    depRecZAG.val52:= ValL[2][1];
    depRecZAG.val75:= ValL[3][1];
    depRecZAG.val213:= ValL[4][1];
    depRecZAG.val214:= ValL[5][1];
    depRecZAG.val233:= ValL[6][1];
    depRecZAG.val234:= ValL[7][1];

    //c
    depRecZAG.NSprav86:= 1;
    depRecZAG.NPar86:=86;
    depRecZAG.NSprav125:= 1;
    depRecZAG.NPar125:=125;
    depRecZAG.NSprav126:= 1;
    depRecZAG.NPar126:=126;
    depRecZAG.NSprav148:= 1;
    depRecZAG.NPar148:=148;
    depRecZAG.NSprav232:= 1;
    depRecZAG.NPar232:=232;
    depRecZAG.NSprav254:= 1;
    depRecZAG.NPar254:=254;





end;




procedure TForm1.Open1Click(Sender: TObject);
var
  Sr : TSearchRec;
  Attr : Integer;
begin
if OpenDialog1.Execute
then begin
  Label1.Caption:= OpenDialog1.FileName;
  //ComboBox1.Items.LoadFromFile(OpenDialog1.FileName);
  myPath := extractFilePath(OpenDialog1.FileName);
  gPath:= extractFilePath(OpenDialog1.FileName);

begin
  //Путь к папке, в которой нужно произвести поиск. Начальное значение выбираем
  //равным пути к той папке, в которой расположена наша программа.
  //if gPath = '' then gPath := ExtractFilePath(ParamStr(0));
  //Диалог выбора папки.
  //if not SelectDirectory('Выбор папки', '', gPath) then Exit;
 // gPath := IncludeTrailingPathDelimiter(gPath); //Если конечный слеш отсутствует, то добавляем его.
  gPath := 'C:\Wells\GeoScape Скв  Куст 1 Пл АГКМ\';
  //Все файлы, исключая тома и папки.
  Attr := faAnyFile - faVolumeID - faDirectory;
  try
    if FindFirst(gPath + '*.db', Attr, Sr) = 0 then
    repeat
      Memo1.Lines.Add(Sr.Name);
    until FindNext(Sr) <> 0;
  finally
    FindClose(Sr);
  end;
end;

end;

end;

//Добавление в picklist параметров Geoscape
procedure addgeoscapeparams();
var
h: Integer;
begin
form1.Table2.Active:=True;
form1.Table2.First;
form1.DBGrid3.Columns[1].PickList.Clear();
form1.DBGrid3.Columns[1].PickList.Add('');
//form1.DBGrid3.Columns[1].PickList.Capacity:=30;
//form1.Memo5.Lines.Add( IntToStr( form1.Table2.Fields.Count));
for h:=0  to form1.Table2.RecordCount -1 do
begin

  form1.DBGrid3.Columns[1].PickList.Add(form1.Table2.Fields[8].AsString);

  form1.Table2.Next;
  Application.ProcessMessages();
  
  
end;
end;

procedure TForm1.FormActivate(Sender: TObject);
var
i: integer;
begin
for i := 0 to PageControl1.PageCount - 1 do begin
  if PageControl1.Pages[i].Caption = 'TabSheet4' then
    PageControl1.Pages[i].TabVisible := False;
  if PageControl1.Pages[i].Caption = 'TabSheet5' then
    PageControl1.Pages[i].TabVisible := False;
  if PageControl1.Pages[i].Caption = 'TabSheet6' then
    PageControl1.Pages[i].TabVisible := False;
  if PageControl1.Pages[i].Caption = 'TabSheet7' then
    PageControl1.Pages[i].TabVisible := False;
end;
//Создаем алиас или заменяем путь
CheckAlias('GEOTODTCIS', 'PARADOX', gPath);
Form1.Table1.DatabaseName:='GEOTODTCIS';
//Form1.Table1.Active:= true;

//Времянки
searchFiles();
//Добавление в picklist параметров Geoscape
addgeoscapeparams();

//Глубинки
searchFilesdepth();

//Глубинки bldata
searchFilesdepthbldata();




//form1.TabSheet4.Visible:=false;
//form1.TabSheet5.Visible:=false;
end;

procedure TForm1.ComboBox1Change(Sender: TObject);
begin
//Label3.Caption:= Combobox1.Items[Combobox1.ItemIndex];

end;

//866 ->1251
function ToAnotherCodePage(Source : String;
                           FromCodePage,
                           ToCodePage : longInt) : string;
type
      byte_arr = array of byte;

var
      byte_buffer_wide : pbyte;
      byte_buffer : pbyte;
      l, i :integer;

begin l := Length(Source);
      GetMem(byte_buffer_wide, l*2);
      fillchar(byte_buffer_wide^, l*2, 0);

      MultiByteToWideChar(FromCodePage, 0,  PChar(Source), l, PWideChar(byte_buffer_wide), l*2);

      GetMem(byte_buffer, l);
      WideCharToMultiByte(ToCodePage, 0,  PWideChar(byte_buffer_wide), l, PChar(byte_buffer), l, nil, nil);

      Result := copy(string(byte_buffer), 1, l);

      FreeMem(byte_buffer_wide, l*2);
      FreeMem(byte_buffer, l);
end;


//Чтение справочника параметров DTCIS
procedure readParsys();
var
  strings: array of string;
  te: string;
  ij, sizeall,cursize,f,c,i,l,cl, col85,gcol85 : Integer;
begin
Assign(FParsys0, 'Parsys01.sup' );
Reset(FParsys0);
//SeekEof(FParsys0,)
sizeall:=0;
//Очистка в razreztoims.db

//Form1.Table3.EmptyTable;
//Form1.Table3.Post;
for ij:=0  to (FileSize(FParsys0)-1) do
begin
   Seek(FParsys0, ij );
   Read(FParsys0, Parsys0 );
   Form1.Memo2.Lines.Add( FloatToStr((Parsys0.K)));
   Form1.Memo2.Lines.Add( IntToStr((Parsys0.NPar)));
   Form1.Memo2.Lines.Add( IntToStr((Parsys0.Size)));

   sizeall:=sizeall+ Parsys0.Size;
   Form1.Memo2.Lines.Add(Parsys0.ParType);
   Form1.Memo2.Lines.Add( ToAnotherCodePage(Parsys0.NameMes,866,1251));
   Form1.Memo2.Lines.Add( ToAnotherCodePage(Parsys0.NamePar,866,1251));

    //Запись в razreztoims.db
   {Form1.Table3.Append;
   Form1.Table3.FieldByName('GID1').AsInteger:=Parsys0.NPar;
   Form1.Table3.FieldByName('GID2').AsInteger:=-1;
   Form1.Table3.FieldByName('IMS').AsString:=ToAnotherCodePage(Parsys0.NamePar,866,1251);
   Form1.Table3.FieldByName('RAZREZ').AsString:='';
   Form1.Table3.FieldByName('KOEF').AsFloat:=1.0;
   Form1.Table3.Post;}

   //Создаем значение DEP

   if Parsys0.ParType='f' then begin
      //Создаем подзаголовок DEP

     Form1.Memo3.Lines.Add( '    NSprav'+IntToStr((Parsys0.NPar))+': Byte;');
     Form1.Memo3.Lines.Add( '    NPar'+IntToStr((Parsys0.NPar))+': Byte;');
     Form1.Memo3.Lines.Add( '    val'+IntToStr((Parsys0.NPar))+': Single; // '+ToAnotherCodePage(Parsys0.NamePar,866,1251));
     Form1.Memo3.Lines.Add( '');
     f:= f+1;
     col85:= col85+ Parsys0.Size+2;
     end;



   if Parsys0.ParType='l' then begin
     Form1.Memo3.Lines.Add( '    NSprav'+IntToStr((Parsys0.NPar))+': Byte;');
     Form1.Memo3.Lines.Add( '    NPar'+IntToStr((Parsys0.NPar))+': Byte;');
     Form1.Memo3.Lines.Add( '    val'+IntToStr((Parsys0.NPar))+': longInt; // '+ToAnotherCodePage(Parsys0.NamePar,866,1251));
     Form1.Memo3.Lines.Add( '');
     l:=l+1;
     col85:= col85+ Parsys0.Size+2;
     end;


   if Parsys0.ParType='i' then begin
     Form1.Memo3.Lines.Add( '    NSprav'+IntToStr((Parsys0.NPar))+': Byte;');
     Form1.Memo3.Lines.Add( '    NPar'+IntToStr((Parsys0.NPar))+': Byte;');
     Form1.Memo3.Lines.Add( '    val'+IntToStr((Parsys0.NPar))+': SmallInt; // '+ToAnotherCodePage(Parsys0.NamePar,866,1251));
     Form1.Memo3.Lines.Add( '');
     i:=i+1;
     col85:= col85+ Parsys0.Size+2;
     end;


   if Parsys0.ParType='c' then begin
     Form1.Memo3.Lines.Add( '    NSprav'+IntToStr((Parsys0.NPar))+': Byte;');
     Form1.Memo3.Lines.Add( '    NPar'+IntToStr((Parsys0.NPar))+': Byte;');
     Form1.Memo3.Lines.Add( '    val'+IntToStr((Parsys0.NPar))+': = array[0..'+IntToStr(Parsys0.Size-1)+'] of AnsiChar; // '+ToAnotherCodePage(Parsys0.NamePar,866,1251));
     Form1.Memo3.Lines.Add( '');
     c:=c+1;
     col85:= col85+ Parsys0.Size+2;
     end;

    if ij=255-1 then begin
      gcol85:= col85+10;

    end;

    ////////
    {
    if Parsys0.ParType='l' then begin
      //Создаем подзаголовок DEP
     te:= te + '('+IntToStr(Parsys0.NPar)+', '+'0), ';
     Form1.Memo3.Lines.Add( '    NSprav'+IntToStr((Parsys0.NPar))+': Byte;');
     Form1.Memo3.Lines.Add( '    NPar'+IntToStr((Parsys0.NPar))+': Byte;');
     Form1.Memo3.Lines.Add( '    val'+IntToStr((Parsys0.NPar))+': Single; // '+ToAnotherCodePage(Parsys0.NamePar,866,1251));
     Form1.Memo3.Lines.Add( '');
     f:= f+1;
     end;
     }
     {
     if Parsys0.ParType='f' then begin


     //Form1.Memo3.Lines.Add(  '    depRecZAG.'+'NSprav'+IntToStr((Parsys0.NPar))+':= 1;');
     //Form1.Memo3.Lines.Add(  '    depRecZAG.'+'NPar'+IntToStr((Parsys0.NPar))+':='+IntToStr((Parsys0.NPar))+ ';');

     Form1.Memo3.Lines.Add(  '    depRecZAG.'+'val'+IntToStr((Parsys0.NPar))+':= ValF['+IntToStr(f)+'][1];');
     //Form1.Memo3.Lines.Add( '');
     f:= f+1;
     end;
      }
     {if Parsys0.ParType='i' then begin


     Form1.Memo3.Lines.Add(  '    depRecZAG.'+'NSprav'+IntToStr((Parsys0.NPar))+':= 1;');
     Form1.Memo3.Lines.Add(  '    depRecZAG.'+'NPar'+IntToStr((Parsys0.NPar))+':='+IntToStr((Parsys0.NPar))+ ';');

     //Form1.Memo3.Lines.Add(  '    depRecZAG.'+'val'+IntToStr((Parsys0.NPar))+':= ValI['+IntToStr(f)+'][1];');
     //Form1.Memo3.Lines.Add( '');
     i:= i+1;
     end;
     }
     {
     if Parsys0.ParType='l' then begin


     //Form1.Memo3.Lines.Add(  '    depRecZAG.'+'NSprav'+IntToStr((Parsys0.NPar))+':= 1;');
     //Form1.Memo3.Lines.Add(  '    depRecZAG.'+'NPar'+IntToStr((Parsys0.NPar))+':='+IntToStr((Parsys0.NPar))+ ';');

     Form1.Memo3.Lines.Add(  '    depRecZAG.'+'val'+IntToStr((Parsys0.NPar))+':= ValI['+IntToStr(f)+'][1];');
     //Form1.Memo3.Lines.Add( '');
     l:= l+1;
     end;
      }
      {
     if Parsys0.ParType='c' then begin


     Form1.Memo3.Lines.Add(  '    depRecZAG.'+'NSprav'+IntToStr((Parsys0.NPar))+':= 1;');
     Form1.Memo3.Lines.Add(  '    depRecZAG.'+'NPar'+IntToStr((Parsys0.NPar))+':='+IntToStr((Parsys0.NPar))+ ';');

     //Form1.Memo3.Lines.Add(  '    depRecZAG.'+'val'+IntToStr((Parsys0.NPar))+':= ValI['+IntToStr(f)+'][1];');
     //Form1.Memo3.Lines.Add( '');
     l:= l+1;
     end;
     }

    ////////
    {
   if Parsys0.ParType='c' then begin
     Form1.Memo3.Lines.Add( '    depRecZAG.val'+IntToStr((Parsys0.NPar))+': = val'+ IntToStr((Parsys0.NPar))+';');
     Form1.Memo3.Lines.Add( '');
     c:=c+1;
     end;
   }



  { NumbSprav: Byte;
    NumbPar: Byte;
   }
end;
Form1.Memo3.Lines.Add( 'f='+IntToStr(f)+ 'l='+IntToStr(l)+ 'i='+IntToStr(i)+ 'c='+IntToStr(c));
Form1.Memo3.Lines.Add('85 записей размер='+IntToStr(gcol85) );
Form1.Label4.Caption:= IntToStr(FileSize(FParsys0));
Form1.Label5.Caption:= IntToStr(FileSize(FParsys0)*2+10+sizeall);


Form1.Memo3.Lines.Add( te);


Close(FParsys0);


end;
//Запись в запись из переменных
procedure saveTorecord();
var
generalPtr : Pointer;
begin
    // Форма текущего модуля адресуемая через ключевое слово self
  //generalPtr := Addr(val86);

  // Мы можем присвоить этот указатель указателю формы
  //depRecZAG.val86 := generalPtr;

  // И установить заголовок формы, чтобы показать это
  //val86 := 'Test program';

    //Строки
    {
    depRecZAG.val86:= val86;

    depRecZAG.val125:= val125;

    depRecZAG.val126:= val126;

    depRecZAG.val148:= val148;

    depRecZAG.val232:= val232;

    depRecZAG.val254:= val254;
     }
end;

//Создание записи LST
procedure createLstRec();
begin
  lstrec.BaseDisp:=0;
  lstrec.KeyValue:=386478;
  lstrec.TimeDos:=386478;
  lstrec.NRecTrue:=0;
  lstrec.NRecLogic:=0;
  lstrec.FlagState:=0;

end;

//Создание записи DEP ZAG
procedure createDEPRecZAG();
begin
  depRecZAG.NRec:=0;
  depRecZAG.NWELL:=65;
  depRecZAG.LengthRec:=1600; //536 452 226 1600; Длина записи включая заголовок все записи
  depRecZAG.NumbParKeY:=52; //Номер ключевого параметра У!!!
  depRecZAG.CountPar:=255; //87 74 36 255;

  {
  depRecZAG.NSprav0:=1; // Очень ВАЖНО!
  depRecZAG.NPar0:= 0;
  //Вес
  depRecZAG.val0:=11.0;
  }
end;

procedure TForm1.Button2Click(Sender: TObject);
var
idx:integer;
begin

//LST
lstrec.BaseDisp:=0;
lstrec.KeyValue:=386478;
lstrec.TimeDos:=386478;
lstrec.NRecTrue:=0;
lstrec.NRecLogic:=0;
lstrec.FlagState:=0;

//Заголовок DEP
depRecZAG.NRec:=0;
depRecZAG.NWELL:=65;
depRecZAG.LengthRec:=1600; //536 452 226 1600; Длина записи включая заголовок все записи
depRecZAG.NumbParKeY:=52; //Номер ключевого параметра У!!!
depRecZAG.CountPar:=255; //87 74 36 255;

for idx:=0 to 99 do begin


Randomize;
ValF[0][1]:= RandomRange(0, 65535);
Randomize;
ValF[1][1]:= RandomRange(0, 65535);
Randomize;
ValF[2][1]:= RandomRange(0, 65535);
Randomize;
ValF[3][1]:= RandomRange(0, 65535);

//ValI[0][1]:= RandomRange(0, 65535);
ValI[0][1]:= 666;
setrec();

depRecZAG.val86:='s';
depRecZAG.val254:='g';
//depRecZAG.val52:=386478+10*idx;

writeDepRec();

//следующая LST запись
lstrec.BaseDisp:=depRecZAG.LengthRec*idx;
lstrec.KeyValue:=386478+10*idx;
lstrec.TimeDos:=386478+10*idx;
lstrec.NRecTrue:=lstrec.NRecTrue+idx;
lstrec.NRecLogic:=lstrec.NRecTrue+idx;
//LST запись

writeLstRec();

end;

{
//LST
createLstRec();
writeLstRec();


//DEP
//Занесение в заголовок
createDEPRecZAG();
//ВЕС

ValF[0][1]:= 129.35;
ValF[1][1]:= 153;
ValF[2][1]:= 154;
ValF[3][1]:= 156;
//ValF[34][1]:= 160.111;

//35
//ValL[0][1]:= -2;
//73
ValI[0][1]:= 666;

//Занесение в подзаголовок и запись
setrec();
//c
depRecZAG.val86:='suck';
depRecZAG.val254:='good';
//время
depRecZAG.val52:=386478;
//depRecZAG.val149:= 170.1;
//depRecZAG.val149:= 171.1;
writeDepRec();

}
end;

procedure TForm1.Button3Click(Sender: TObject);
begin
readParsys();

end;



procedure TForm1.Button5Click(Sender: TObject);
var
h: Integer;
s: String;
begin
//Название полей
  //ListLabel.Create;
 //S := Fields[0].FieldName;
 Table1.Active:=True;
 fieldCount:= Table1.Fields.Count;
 Memo4.Lines.Add(IntToStr(fieldCount));
 for h:=0  to (fieldCount-1) do
    begin
    s:= Table1.Fields[h].FieldName;
    //имена параметров
    if s[1]='S' then begin
      Memo4.Lines.Add(Table1.Fields[h].FieldName);
      //ListLabel.Add();
    end;
    //FieldsByName('CustNo').AsString;

    end;
end;

procedure TForm1.Button6Click(Sender: TObject);
var h:Integer;
begin
//Чтение Sensors.db

fieldCount:= Table2.Fields.Count;
 Memo5.Lines.Add(IntToStr(fieldCount));
 for h:=0  to (fieldCount-1) do
    begin
    //s:= Table1.Fields[h].FieldName;
    //имена параметров
    {if s[1]='S' then begin
      Memo4.Lines.Add(Table1.Fields[h].FieldName);
      //ListLabel.Add();
    end;
    }
    //FieldsByName('CustNo').AsString;
    Memo5.Lines.Add(Table2.Fields[h].FieldName);
    end;


end;

procedure TForm1.Button7Click(Sender: TObject);
var
i, j: Integer;
s: string;
begin

  {
  DBGrid3.Columns[1].PickList.Clear();
  DBGrid3.Columns[1].PickList.Add('М');
  DBGrid3.Columns[1].PickList.Add('Ж');
   }
  {if DBGrid3.SelectedRows.Count>0 then
  with DBGrid3.DataSource.DataSet do
  for i:=0 to DBGrid3.SelectedRows.Count-1 do
  begin
  GotoBookmark(pointer(DBGrid3.SelectedRows.Items[i]));
  for j := 0 to FieldCount-1 do
  begin

  if (j>0) then s:=s+', ';
  s:=s+Fields[j].AsString;
  end;
  Listbox1.Items.Add(s);
  s:= '';
  end;
   }
 //Запись в razreztoims.db
   {Table2.Insert;
   Table2.FieldByName('Name').AsString:='Russia';
   Table2.FieldByName('Capital').AsString:='Moscow';
   Table2.Post;}

   //второй способ
   {Table1.Append;
   Table1.SetFields[9000,2118,Now,Now,47];
   Table1.First;}

   //третий
   {InsertRecord и AppendRecord}


end;



procedure TForm1.Button8Click(Sender: TObject);
begin
//СОХРАНИТЬ
form1.Table3.Edit;
form1.Table3.Post;
dbgrid3.Visible:= False;
end;

procedure TForm1.Table3AfterPost(DataSet: TDataSet);
begin
  //Form1.Memo5.Lines.Add(dbGrid3.Fields[3].AsString);

end;

procedure TForm1.Table3BeforePost(DataSet: TDataSet);
var
idx:Integer;
begin
  //Выбранное поле для редактирования
 Form1.Memo5.Lines.Add(dbGrid3.Fields[1].AsString);
 //Поиск GUID2 по имени параметра
 Table2.First;
 for idx:=0 to  Table2.RecordCount-1 do
 begin
 if Table2.FieldByName('Name').AsString = dbGrid3.Fields[1].AsString then begin
  dbgrid3.Options := dbgrid3.Options + [dgEditing];
  Table3.FieldByName('GID2').AsInteger:=Table2.FieldByName('GID').AsInteger;
 end;
 //Пустое значение
  if dbGrid3.Fields[1].AsString='' then begin
  dbgrid3.Options := dbgrid3.Options + [dgEditing];
  Table3.FieldByName('GID2').AsInteger:=-1;
  //dbGrid3.Fields[4].AsInteger:=Table2.FieldByName('GID').AsInteger;
 end;
 Table2.Next;
 end;

end;

procedure TForm1.Button9Click(Sender: TObject);
begin
//Редактирование справочника
dbgrid3.Visible:= True;
dbgrid3.Options := dbgrid3.Options + [dgEditing];
form1.Button8.Visible:=true;

end;

//Массив GID2 ->GID1Разрез то DICIS параметры по времени
procedure RaToDTCIS();
var
idspr: Integer;
begin

Form1.Table3.Active:= true;
Form1.Table3.First;
SetLength(RazToDTCIS, Form1.Table3.RecordCount, 1);
for idspr:=0 to Form1.Table3.RecordCount-1 do begin
RazToDTCIS[idspr, 0]:= Form1.Table3.FieldByName('GID1').AsInteger;
RazToDTCIS[idspr, 1]:= Form1.Table3.FieldByName('GID2').AsInteger;

// , Form1.Table3.FieldByName('GID2').AsInteger  ]:=10;
Form1.Table3.Next;
Application.ProcessMessages;

end;

end;


//Массив GID2 ->GID1Разрез то DICIS параметры по глубине
procedure RaToDTCISdepth();
var
idspr: Integer;
begin

Form1.Table3.Active:= true;
Form1.Table3.First;
SetLength(RazToDTCIS, Form1.Table3.RecordCount, 1);
for idspr:=0 to Form1.Table3.RecordCount-1 do begin
RazToDTCIS[idspr, 0]:= Form1.Table3.FieldByName('GID1').AsInteger;
RazToDTCIS[idspr, 1]:= Form1.Table3.FieldByName('GID2').AsInteger;
// , Form1.Table3.FieldByName('GID2').AsInteger  ]:=10;
Form1.Table3.Next;
end;

end;

//Поиск количества записей в текущем LST файле
Function countLST(name_file:String) :Integer ;
begin

Result:= 0;

end;

procedure TForm1.Button10Click(Sender: TObject);
var
idx1,idx10,idy1,idspr,len, f,l,i,Res: Integer;
s,GID, ep: string;
Value: Single;
daterec : TDateTime;
StrDate : string;
LongTime: LongWord;
Fmt     : TFormatSettings;
epoxutc      : TDateTime;
begin
if (form1.ListBox2.Items.Count>0) and (ListBox2.ItemIndex<>-1) then
begin
//старт и прогресс
form1.Button10.Enabled:=False;
form1.ProgressBar1.Min:=0;
form1.ProgressBar1.Max:= form1.DBGrid1.DataSource.DataSet.RecordCount;
form1.ProgressBar1.Position:=0;
//Формат времени
fmt.ShortDateFormat:='dd/mm/yyyy';
fmt.DateSeparator  :='/';
fmt.LongTimeFormat :='hh:nn:ss';
fmt.TimeSeparator  :=':';
//StrDate:='23/02/2011 12:34:56';
StrDate:='01/01/1970 00:00:00';
epoxutc:=StrToDateTime(StrDate,Fmt);

//LST
lstrec.BaseDisp:=0;
lstrec.KeyValue:=386478;
lstrec.TimeDos:=386478;
lstrec.NRecTrue:=0;
lstrec.NRecLogic:=0;
lstrec.FlagState:=0;

//Заголовок DEP
depRecZAG.NRec:=0;
depRecZAG.NWELL:=65;
depRecZAG.LengthRec:=1600; //536 452 226 1600; Длина записи включая заголовок все записи
depRecZAG.NumbParKeY:=52; //Номер ключевого параметра У!!!
depRecZAG.CountPar:=255; //87 74 36 255;


//Сверка одной записи
Form1.Table1.Active:= true;
Form1.Table3.Active:= true;
Form1.Table1.First;
Form1.Table3.First;
Form1.Memo5.Lines.Add(IntToStr(Form1.Table1.RecordCount));

//Массив GID2 ->GID1Разрез то DICIS параметры
RaToDTCIS();
len:= Length(RazToDTCIS);

//Узнать количество записей в lst файле
{idx1:=getNumbsLst();
lstrec.BaseDisp:=depRecZAG.LengthRec*idx1;
Form1.Table1.MoveBy(idx1);
lstrec.NRecTrue:=idx1;
lstrec.NRecLogic:=idx1;
depRecZAG.NRec:=idx1;

for idx1:=idx1 to Form1.Table1.RecordCount-1 do begin
}

//Узнать количество записей в lst файле
Counttime:= getNumbsLst();
idx1:=Counttime.i;




idx10:=Form1.Table1.RecordCount-1;

Form1.Table1.Last;
idx10:=0;
//Поиск новых записей по времени
if  idx1<>0 then begin
for i:=Form1.Table1.RecordCount-1 downto 0 do begin

    daterec:= Form1.Table1.FieldByName('Date').AsDateTime;
    //Res:=SecondsBetween(epoxutc,daterec);
    LongTime:= Trunc(Form1.Table1.FieldByName('Time').AsInteger / 1000);
    //ValL[2][1]:= Form1.Table1.FieldByName('Date').AsInteger+Form1.Table1.FieldByName('Time').AsInteger;
    Res:=SecondsBetween(epoxutc,daterec)+  LongTime;
    if Counttime.S= Res then begin
      idx10:=form1.Table1.RecNo ;
      break;
    end;
    idx10:=form1.Table1.RecNo;
    Form1.Table1.Prior;
    //ListBox5.Items.Add(IntToStr(Res));
    //ListBox5.Items.Add(IntToStr(Counttime.S));
end;
 //ListBox5.Items.Add(IntToStr(Form1.Table1.RecordCount));
 //ListBox5.Items.Add(IntToStr(idx10));
  ListBox5.Items.Add(IntToStr(idx1));
//ListBox5.Items.Add(IntToStr(Res));
//ListBox5.Items.Add(IntToStr(Counttime.S));
end;

lstrec.BaseDisp:=depRecZAG.LengthRec*idx1;
Form1.Table1.First;
 ListBox5.Items.Add(IntToStr(form1.Table1.RecNo));
Form1.Table1.MoveBy(idx10+1);
lstrec.NRecTrue:=idx1;
lstrec.NRecLogic:=idx1;
depRecZAG.NRec:=idx1;

for idx10:=idx10+1 to Form1.Table1.RecordCount-1 do begin

for idy1:=0  to Table1.Fields.Count-1 do
    begin
    Application.ProcessMessages;
    
    s:= Table1.Fields[idy1].FieldName;
    //имена параметров
    if s[1]='S' then begin
      GID:= s;
      Delete(GID,1,1); // - S
      //Length(RazToDTCIS);
      for idspr:=0 to  len-1 do begin
        if RazToDTCIS[idspr,1] = StrToInt(GID) then begin //массив соответст параметров
          for f:=0 to 225 do begin //float
            if RazToDTCIS[idspr,0]= ValF[f,0] then begin
              ValF[f,1]:= Form1.Table1.FieldByName(s).AsFloat;
              Application.ProcessMessages;
              
            end;
          end;
          for i:=0 to 14 do begin //integer
            if RazToDTCIS[idspr,0]= ValI[i,0] then begin
              ValI[i,1]:= Form1.Table1.FieldByName(s).AsInteger;
              Application.ProcessMessages;
              
            end;
          end;
          for l:=0 to 7 do begin //16ng
            if RazToDTCIS[idspr,0]= ValL[l,0] then begin
              ValL[l,1]:= Form1.Table1.FieldByName(s).AsInteger;
              Application.ProcessMessages;
              
            end;
          end;
          //Form1.Memo5.Lines.Add(IntToStr(RazToDTCIS[idspr,0]));

        end;
      end;

      end;
    end;
    daterec:= Form1.Table1.FieldByName('Date').AsDateTime;
    Res:=SecondsBetween(epoxutc,daterec);
    //ValL[2][1]:= Form1.Table1.FieldByName('Date').AsInteger+Form1.Table1.FieldByName('Time').AsInteger;
    ValL[2][1]:=Res+  Math.Floor( Form1.Table1.FieldByName('Time').AsInteger /1000);

    Form1.Table1.Next;
    Application.ProcessMessages;
    
    form1.ProgressBar1.Position:= form1.ProgressBar1.Position+1;
    //
    setrec();

    //if (Counttime.S<depRecZAG.val52) or (Counttime.S=0)  then begin

    depRecZAG.val86:='s';
    depRecZAG.val254:='g';
    //Глубина забоя
    //depRecZAG.val52:=386478+10*idx1;

    //Запись Dep записи
    writeDepRec();

    //следующая LST запись
    lstrec.BaseDisp:=depRecZAG.LengthRec*idx1;
    //Глубина забоя
    //Время сбора данных
    lstrec.KeyValue:=depRecZAG.val53;
    //Время сбора данных
    //Глубина забоя
    lstrec.TimeDos:=depRecZAG.val52;
    lstrec.NRecTrue:=lstrec.NRecTrue+idx1;
    lstrec.NRecLogic:=lstrec.NRecTrue+idx1;

    //Запись LST записи
    writeLstRec();
    idx1:= idx1+1;
    //end;
    end;
    form1.ProgressBar1.Position:=form1.DBGrid1.DataSource.DataSet.RecordCount;
    Form1.Memo5.Lines.Add(IntToStr(Form1.Table1.RecordCount));
    Application.ProcessMessages;
    
    form1.Button10.Enabled:=true;
    end;
    form1.Button10.Enabled:=true;
end;




procedure cycletime();
var
idx1,idx10,idy1,idspr,len, f,l,i,Res: Integer;
s,GID, ep: string;
Value: Single;
daterec : TDateTime;
StrDate : string;
LongTime: LongWord;
Fmt     : TFormatSettings;
epoxutc      : TDateTime;
begin
if (form1.ListBox2.Items.Count>0) then
begin
//старт и прогресс
form1.Button10.Enabled:=False;
form1.ProgressBar1.Min:=0;
form1.ProgressBar1.Max:= form1.DBGrid1.DataSource.DataSet.RecordCount;
form1.ProgressBar1.Position:=0;
//Формат времени
fmt.ShortDateFormat:='dd/mm/yyyy';
fmt.DateSeparator  :='/';
fmt.LongTimeFormat :='hh:nn:ss';
fmt.TimeSeparator  :=':';
//StrDate:='23/02/2011 12:34:56';
StrDate:='01/01/1970 00:00:00';
epoxutc:=StrToDateTime(StrDate,Fmt);

//LST
lstrec.BaseDisp:=0;
lstrec.KeyValue:=386478;
lstrec.TimeDos:=386478;
lstrec.NRecTrue:=0;
lstrec.NRecLogic:=0;
lstrec.FlagState:=0;

//Заголовок DEP
depRecZAG.NRec:=0;
depRecZAG.NWELL:=65;
depRecZAG.LengthRec:=1600; //536 452 226 1600; Длина записи включая заголовок все записи
depRecZAG.NumbParKeY:=52; //Номер ключевого параметра У!!!
depRecZAG.CountPar:=255; //87 74 36 255;


//Сверка одной записи
Form1.Table1.Active:= true;
Form1.Table3.Active:= true;
Form1.Table1.First;
Form1.Table3.First;
Form1.Memo5.Lines.Add(IntToStr(Form1.Table1.RecordCount));

//Массив GID2 ->GID1Разрез то DICIS параметры
RaToDTCIS();
len:= Length(RazToDTCIS);

//Узнать количество записей в lst файле
{idx1:=getNumbsLst();
lstrec.BaseDisp:=depRecZAG.LengthRec*idx1;
Form1.Table1.MoveBy(idx1);
lstrec.NRecTrue:=idx1;
lstrec.NRecLogic:=idx1;
depRecZAG.NRec:=idx1;

for idx1:=idx1 to Form1.Table1.RecordCount-1 do begin
}

//Узнать количество записей в lst файле
Counttime:= getNumbsLst();
idx1:=Counttime.i;




idx10:=Form1.Table1.RecordCount-1;

Form1.Table1.Last;
idx10:=0;
//Поиск новых записей по времени
if  idx1<>0 then begin
for i:=Form1.Table1.RecordCount-1 downto 0 do begin

    daterec:= Form1.Table1.FieldByName('Date').AsDateTime;
    //Res:=SecondsBetween(epoxutc,daterec);
    LongTime:= Trunc(Form1.Table1.FieldByName('Time').AsInteger / 1000);
    //ValL[2][1]:= Form1.Table1.FieldByName('Date').AsInteger+Form1.Table1.FieldByName('Time').AsInteger;
    Res:=SecondsBetween(epoxutc,daterec)+  LongTime;
    Application.ProcessMessages();
    
    if Counttime.S= Res then begin
      idx10:=form1.Table1.RecNo ;
      break;
    end;
    idx10:=form1.Table1.RecNo;
    Form1.Table1.Prior;
    //Form1.ListBox5.Items.Add(IntToStr(Res));
    //Form1.ListBox5.Items.Add(IntToStr(Counttime.S));
end;
 //Form1.ListBox5.Items.Add(IntToStr(Form1.Table1.RecordCount));
 //Form1.ListBox5.Items.Add(IntToStr(idx10));
 //Form1.ListBox5.Items.Add(IntToStr(idx1));
//ListBox5.Items.Add(IntToStr(Res));
//ListBox5.Items.Add(IntToStr(Counttime.S));
end;

lstrec.BaseDisp:=depRecZAG.LengthRec*idx1;
Form1.Table1.First;
//Form1.ListBox5.Items.Add(IntToStr(form1.Table1.RecNo));
Form1.Table1.MoveBy(idx10+1);
lstrec.NRecTrue:=idx1;
lstrec.NRecLogic:=idx1;
depRecZAG.NRec:=idx1;

for idx10:=idx10+1 to Form1.Table1.RecordCount-1 do begin
if Form1.ComboBox2.ItemIndex=1 then begin
  Application.ProcessMessages;
  Sleep(1);
end;
for idy1:=0  to Form1.Table1.Fields.Count-1 do
    begin
    if Form1.ComboBox2.ItemIndex=0 then begin
      Application.ProcessMessages;
      Sleep(1);
    end;

    s:= Form1.Table1.Fields[idy1].FieldName;
    //имена параметров
    if s[1]='S' then begin
      GID:= s;
      Delete(GID,1,1); // - S
      //Length(RazToDTCIS);
      for idspr:=0 to  len-1 do begin
        if RazToDTCIS[idspr,1] = StrToInt(GID) then begin //массив соответст параметров
          for f:=0 to 225 do begin //float
            if RazToDTCIS[idspr,0]= ValF[f,0] then begin
              ValF[f,1]:= Form1.Table1.FieldByName(s).AsFloat;


            end;
          end;
          for i:=0 to 14 do begin //integer
            if RazToDTCIS[idspr,0]= ValI[i,0] then begin
              ValI[i,1]:= Form1.Table1.FieldByName(s).AsInteger;


            end;
          end;
          for l:=0 to 7 do begin //16ng
            if RazToDTCIS[idspr,0]= ValL[l,0] then begin
              ValL[l,1]:= Form1.Table1.FieldByName(s).AsInteger;


            end;
          end;
          //Form1.Memo5.Lines.Add(IntToStr(RazToDTCIS[idspr,0]));

        end;
      end;

      end;
    end;
    daterec:= Form1.Table1.FieldByName('Date').AsDateTime;
    Res:=SecondsBetween(epoxutc,daterec);
    //ValL[2][1]:= Form1.Table1.FieldByName('Date').AsInteger+Form1.Table1.FieldByName('Time').AsInteger;
    ValL[2][1]:=Res+  Math.Floor( Form1.Table1.FieldByName('Time').AsInteger /1000);

    Form1.Table1.Next;


    form1.ProgressBar1.Position:= form1.ProgressBar1.Position+1;
    //
    setrec();

    //if (Counttime.S<depRecZAG.val52) or (Counttime.S=0)  then begin

    depRecZAG.val86:='s';
    depRecZAG.val254:='g';
    //Глубина забоя
    //depRecZAG.val52:=386478+10*idx1;

    //Запись Dep записи
    writeDepRec();

    //следующая LST запись
    lstrec.BaseDisp:=depRecZAG.LengthRec*idx1;
    //Глубина забоя
    //Время сбора данных
    lstrec.KeyValue:=depRecZAG.val53;
    //Время сбора данных
    //Глубина забоя
    lstrec.TimeDos:=depRecZAG.val52;
    lstrec.NRecTrue:=lstrec.NRecTrue+idx1;
    lstrec.NRecLogic:=lstrec.NRecTrue+idx1;

    //Запись LST записи
    writeLstRec();
    idx1:= idx1+1;
    //end;
    end;
    form1.ProgressBar1.Position:=form1.DBGrid1.DataSource.DataSet.RecordCount;
    Form1.Memo5.Lines.Add(IntToStr(Form1.Table1.RecordCount));


    form1.Button10.Enabled:=true;
    end;
    form1.Button10.Enabled:=true;
end;


procedure TForm1.FormDestroy(Sender: TObject);
var
  Ini: Tinifile;
begin
//СОздаем или открываем на запись инишку
  Ini:=TiniFile.Create(extractfilepath(paramstr(0))+'main.ini');
  {Ini.WriteInteger('Size','Width',form1.width);
  Ini.WriteInteger('Size','Height',form1.height);
  Ini.WriteInteger('Position','X',form1.left);
  Ini.WriteInteger('Position','Y',form1.top);
  }




  Ini.WriteString('Geoscape','gpath', gPath);
  Ini.WriteString('Dtcis','dpath', dPath);
  Ini.WriteBool('Cycle','gcycletime', gcycletime);
  Ini.WriteInteger('Cycle','gtimeinterval', gcycletimeInter);
  Ini.WriteBool('Cycle','gcycledepth', gcycledepth);
  Ini.WriteInteger('Cycle','gcycledepthInter', gcycledepthInter);
  Ini.WriteBool('Cycle','gcycledepthgaz', gcycledepthgaz);
  Ini.WriteInteger('Speed','Speed', gspeed);
  Ini.Free;
  // Допустимые методы WriteInteger, WriteString, WriteBool
  
end;

procedure TForm1.FormCreate(Sender: TObject);
var
  Ini: Tinifile;
begin
  //Читаем инишку
  Ini:=TiniFile.Create(extractfilepath(paramstr(0))+'main.ini');
  {Form1.Width:=Ini.ReadInteger('Size','Width',100);
  Form1.Height:=Ini.ReadInteger('Size','Height',100);
  Form1.Left:=Ini.ReadInteger('Position','X',10);
  Form1.Top:=Ini.ReadInteger('Position','Y',10);
  }
  //Путь к geoscape
  gPath:= Ini.ReadString('Geoscape','gpath','C:\Wells');
  dPath:= Ini.ReadString('Dtcis','dpath','C:\');
  gcycletime:= Ini.ReadBool('Cycle','gcycletime', false );
  gcycletimeInter:= Ini.ReadInteger('Cycle','gtimeinterval',20);
  gcycledepth:= Ini.ReadBool('Cycle','gcycledepth', false );
  gcycledepthInter:= Ini.ReadInteger('Cycle','gcycledepthInter',20);
  gcycledepthgaz:= Ini.ReadBool('Cycle','gcycledepthgaz', false );
  gspeed:=  Ini.ReadInteger('Speed','Speed', 0);

  Form1.Edit1.Text:=gPath;
  Form1.Edit2.Text:=dPath;

  Form1.CheckBox1.Checked:=gcycletime;
  Form1.Edit3.Text:=IntToStr(gcycletimeInter);
  Form1.CheckBox2.Checked:=gcycledepth;
  Form1.Edit4.Text:=IntToStr(gcycledepthInter);
  Form1.CheckBox3.Checked:=gcycledepthgaz;
  Form1.ComboBox2.ItemIndex:=gspeed;
  Ini.Free;
  form1.Timer1.Interval:= 1000*gcycletimeInter;
  form1.Timer2.Interval:= 1000*gcycledepthInter;
  if (form1.CheckBox1.Checked=true) or (form1.CheckBox2.Checked=true) then
   form1.Timer1.Enabled:=true
   else
   form1.Timer1.Enabled:=false;


end;



//Выбор пути геоскеп
procedure TForm1.Button11Click(Sender: TObject);
begin
if SelectDirectory(chosenDirectory, options, 0)
  then begin
  Form1.Edit1.Text:= chosenDirectory;
  gPath:= chosenDirectory;
  //Создаем алиас или заменяем путь
 CheckAlias('GEOTODTCIS', 'PARADOX', gPath);

 //Поиск файлов db
 searchFiles();
 //Глубинки
 searchFilesdepth();

 //Глубинки bldata
 searchFilesdepthbldata();
 //temp:=MessageBox(handle, PChar('Необходимо перезапустить конвертер'), PChar('Выход!'), MB_OK);
 //Application.Terminate;
  end
  else begin
  end;

end;

procedure TForm1.ListBox2Click(Sender: TObject);
begin
if ListBox2.Items[ListBox2.ItemIndex]<>'' then
begin
form1.Table1.Active:= False;
form1.Table1.DatabaseName:='GEOTODTCIS';
form1.Table1.TableName:= ListBox2.Items[ListBox2.ItemIndex];
form1.Table1.Active:= True;
end;
end;

procedure TForm1.Button12Click(Sender: TObject);
begin
if SelectDirectory(chosenDirectory, options, 0)
  then begin
  Form1.Edit2.Text:= chosenDirectory;
  dPath:= chosenDirectory+'\';
  end
  else begin
  end;
end;


//Глубина
procedure depth_good(name:string);
var
idx1,idx10,idy1,idspr,len, f,l,i,Res,d1,t1: Integer;
fldate: Double;
s,GID, ep, date, time, dateitime: string;
Value: Single;
daterec : TDateTime;
StrDate, StrDate2 : string;
Fmt     : TFormatSettings;
epoxutc      : TDateTime;
epoxdelphi : TDateTime;
begin
if form1.ListBox3.ItemIndex<>-1 then
begin
form1.Table4.Active:= False;
form1.Table4.TableName:= form1.ListBox3.Items[form1.ListBox3.ItemIndex];
form1.Table4.Active:= True;


//старт и прогресс
form1.Button13.Enabled:=False;
form1.ProgressBar2.Min:=0;
form1.ProgressBar2.Max:= form1.DBGrid4.DataSource.DataSet.RecordCount;
form1.ProgressBar2.Position:=0;
//Формат времени
fmt.ShortDateFormat:='dd/mm/yyyy';
fmt.DateSeparator  :='/';
fmt.LongTimeFormat :='hh:nn:ss';
fmt.TimeSeparator  :=':';
//StrDate:='23/02/2011 12:34:56';
StrDate:='01/01/1970 00:00:00';
epoxutc:=StrToDateTime(StrDate,Fmt);
StrDate2:='30/12/1899 00:00:00';
epoxdelphi :=StrToDateTime(StrDate2,Fmt);



//LST
lstrec.BaseDisp:=0;
lstrec.KeyValue:=386478;
lstrec.TimeDos:=386478;
lstrec.NRecTrue:=0;
lstrec.NRecLogic:=0;
lstrec.FlagState:=0;

//Заголовок DEP
depRecZAG.NRec:=0;
depRecZAG.NWELL:=65;
depRecZAG.LengthRec:=1600; //536 452 226 1600; Длина записи включая заголовок все записи
depRecZAG.NumbParKeY:=53; //Номер ключевого параметра У!!!
depRecZAG.CountPar:=255; //87 74 36 255;


//Сверка одной записи
Form1.Table4.Active:= true;
Form1.Table3.Active:= true;
Form1.Table4.First;
Form1.Table3.First;
//Form1.Memo5.Lines.Add(IntToStr(Form1.Table4.RecordCount));

//Массив GID2 ->GID1Разрез то DICIS параметры
RaToDTCIS();
len:= Length(RazToDTCIS);

//Узнать количество записей в lst файле



Countdepth:= getNumbsLstdepth();
idx1:=Countdepth.i;

//ListBox4.Items.Add(FloatToStr(Countdepth.S));
lstrec.BaseDisp:=depRecZAG.LengthRec*idx1;
Form1.Table4.First;
//Form1.Table4.MoveBy(idx1);
lstrec.NRecTrue:=idx1;
lstrec.NRecLogic:=idx1;
depRecZAG.NRec:=idx1;
idx10:=0;


for idx10:=0 to Form1.Table4.RecordCount-1 do begin
if Form1.ComboBox2.ItemIndex=1 then begin
  Application.ProcessMessages();
  Sleep(1);
end;
for idy1:=0  to form1.Table4.Fields.Count-1 do
    begin
    if Form1.ComboBox2.ItemIndex=0 then begin
      Application.ProcessMessages();
      Sleep(1);
    end;
    s:= form1.Table4.Fields[idy1].FieldName;
    //имена параметров
    if s[1]='S' then begin
      GID:= s;
      Delete(GID,1,1); // - S
      //Length(RazToDTCIS);
      for idspr:=0 to  len-1 do begin
        if RazToDTCIS[idspr,1] = StrToInt(GID) then begin //массив соответст параметров
          for f:=0 to 225 do begin //float
            if RazToDTCIS[idspr,0]= ValF[f,0] then begin
              ValF[f,1]:= Form1.Table4.FieldByName(s).AsFloat;
              Application.ProcessMessages;
              
            end;
          end;
          for i:=0 to 14 do begin //integer
            if RazToDTCIS[idspr,0]= ValI[i,0] then begin
              ValI[i,1]:= Form1.Table4.FieldByName(s).AsInteger;
              Application.ProcessMessages;
              
            end;
          end;
          for l:=0 to 7 do begin //16ng
            if RazToDTCIS[idspr,0]= ValL[l,0] then begin
              ValL[l,1]:= Form1.Table4.FieldByName(s).AsInteger;
              Application.ProcessMessages;
              
            end;
          end;
          //Form1.Memo5.Lines.Add(IntToStr(RazToDTCIS[idspr,0]));

        end;
      end;

      //Form1.Memo5.Lines.Add(GID);
      //Поиск соответствия в справочнике
      {Form1.Table3.First;
      for idspr:=0 to Form1.Table3.RecordCount-1 do begin
        //если нашли GID Разреза
        if Form1.Table3.FieldByName('GID2').AsString = GID then begin
          //Form1.Memo5.Lines.Add(Form1.Table3.FieldByName('GID1').AsString)


        end;
      Form1.Table3.Next;
      end;
      }



      end;
    end;

    fldate:= Form1.Table4.FieldByName('s0').AsFloat;
    daterec:=fldate;
    //dateitime:= FloatToStr(fldate);
    //d1:=trunc(fldate);
    //t1= //Copy(dateitime,0,Pos('.',dateitime)-1);
    //form1.Memo6.Text:=form1.Memo6.Text+IntToStr(d1);// date;

    Res:=SecondsBetween(epoxutc, daterec);
    //ValL[2][1]:= Form1.Table1.FieldByName('Date').AsInteger+Form1.Table1.FieldByName('Time').AsInteger;
    ValL[2][1]:=Res; //+  Math.Floor( Form1.Table1.FieldByName('Time').AsInteger /1000);

    Form1.Table4.Next;
    Application.ProcessMessages;
    
    form1.ProgressBar2.Position:= form1.ProgressBar2.Position+1;
    //
    setrec();
    //depRecZAG.val53:=RoundTo(depRecZAG.val53,-1);
    //проверка записана ли уже такая глубина
    if (Countdepth.S<depRecZAG.val53) or (Countdepth.S=0) then begin
    depRecZAG.val86:='s';
    depRecZAG.val254:='g';

    //Глубина забоя
    //depRecZAG.val52:=386478+10*idx1;

    //Запись Dep записи
    //depRecZAG.val53:= 10*idx1;
    ///////////
    writeDepRecdepth();

    //следующая LST запись
    lstrec.BaseDisp:=depRecZAG.LengthRec*idx1;
    //Глубина забоя
    //Время сбора данных

    lstrec.KeyValue:=depRecZAG.val53;
    //Время сбора данных
    //Глубина забоя
    lstrec.TimeDos:=depRecZAG.val52;
    lstrec.NRecTrue:=lstrec.NRecTrue+idx1;
    lstrec.NRecLogic:=lstrec.NRecTrue+idx1;

    //Запись LST записи
    writeLstRecdepth();

    idx1:= idx1+1;
    end;
    end;
    form1.ProgressBar2.Position:=form1.DBGrid4.DataSource.DataSet.RecordCount;
    Form1.Memo5.Lines.Add(IntToStr(Form1.Table4.RecordCount));
    Application.ProcessMessages;
    
    form1.Button13.Enabled:=true;
end;
end;


procedure TForm1.Button14Click(Sender: TObject);
begin

readwriteDepRecdepthbldata();
end;

//Ручной прогон
procedure TForm1.Button13Click(Sender: TObject);
var
i: Integer;
oldName, newName: String;
begin
oldName:=dPath+'temp_str' +'.lst';
DeleteFile(oldName);
oldName:=dPath+'temp_str' +'.dep';
DeleteFile(oldName);

if form1.ListBox3.Items.Count>0 then
begin
for i:=0 to form1.ListBox3.Items.Count do begin
  form1.ListBox3.ItemIndex:=i;
  depth_good('123');

end;

if (gcycledepthgaz=true) then  begin
  readwriteDepRecdepthbldata();
  ShowMessage('увязка');
  end;

oldName:=dPath+'Store' +'.lst';
DeleteFile(oldName);
oldName:=dPath+'Store' +'.dep';
DeleteFile(oldName);



oldName:=dPath+'temp_str' +'.dep';
newName:=dPath+'Store' +'.dep';
RenameFile(oldName, newName);


oldName:=dPath+'temp_str' +'.lst';
newName:=dPath+'Store' +'.lst';
RenameFile(oldName, newName);



end;
end;


procedure TForm1.CheckBox1Click(Sender: TObject);
begin
gcycletime:= CheckBox1.Checked;
if (gcycletime) then
  form1.Timer1.Enabled:=true
else
  form1.Timer1.Enabled:=false;
end;

procedure TForm1.Edit3Change(Sender: TObject);
begin
gcycletimeInter:= StrToInt(Form1.Edit3.Text);
form1.Timer1.Interval:= 1000*gcycletimeInter;
end;

procedure TForm1.CheckBox2Click(Sender: TObject);
begin
gcycledepth := CheckBox2.Checked;
if (gcycledepth) then
  form1.Timer1.Enabled:=true
else
  form1.Timer1.Enabled:=false;
end;

procedure TForm1.Edit4Change(Sender: TObject);
begin
gcycledepthInter:= StrToInt(Form1.Edit4.Text);
form1.Timer2.Interval:=1000*gcycledepthInter;
end;

procedure TForm1.CheckBox3Click(Sender: TObject);
begin
gcycledepthgaz := CheckBox3.Checked;
end;

procedure TForm1.Timer1Timer(Sender: TObject);
var
i: Integer;
oldName, newName:String;
begin
form1.Timer1.Enabled:=false;
//Времянки
searchFiles();
//Добавление в picklist параметров Geoscape
addgeoscapeparams();

//form1.ListBox5.Items.Add(ListBox2.Items[ListBox2.Count - 1]);

if ListBox2.Items.Count>0 then
begin
//form1.ListBox5.Items.Add(ListBox2.Items[ListBox2.Count - 1]);
form1.Table1.Active:= False;
form1.Table1.DatabaseName:='GEOTODTCIS';
form1.Table1.TableName:= ListBox2.Items[ListBox2.Count - 1];
form1.Table1.Active:= True;

if form1.CheckBox1.Checked=true then begin
cycletime();
end;

if form1.CheckBox2.Checked=true then begin
//Глубинки
searchFilesdepth();

//Глубинки bldata
searchFilesdepthbldata();

oldName:=dPath+'temp_str' +'.lst';
DeleteFile(oldName);
oldName:=dPath+'temp_str' +'.dep';
DeleteFile(oldName);

if form1.ListBox3.Items.Count>0 then
begin
for i:=0 to form1.ListBox3.Items.Count do begin
  form1.ListBox3.ItemIndex:=i;
  depth_good('123');

end;

if (gcycledepthgaz=true) then  begin
  readwriteDepRecdepthbldata();
  end;

oldName:=dPath+'Store' +'.lst';
DeleteFile(oldName);
oldName:=dPath+'Store' +'.dep';
DeleteFile(oldName);



oldName:=dPath+'temp_str' +'.dep';
newName:=dPath+'Store' +'.dep';
RenameFile(oldName, newName);


oldName:=dPath+'temp_str' +'.lst';
newName:=dPath+'Store' +'.lst';
RenameFile(oldName, newName);


end;
end;
{
if form1.CheckBox2.Checked=true then
   form1.Timer2.Enabled:=true
   else
   form1.Timer2.Enabled:=false;
end;
 }

if (form1.CheckBox1.Checked=true) or (form1.CheckBox2.Checked=true) then
   form1.Timer1.Enabled:=true
   else
   form1.Timer1.Enabled:=false;
end;

end;

procedure TForm1.Timer2Timer(Sender: TObject);
var
i: Integer;
oldName, newName:String;
begin
form1.Timer2.Enabled:=false;
//Глубинки
searchFilesdepth();

//Глубинки bldata
searchFilesdepthbldata();

oldName:=dPath+'temp_str' +'.lst';
DeleteFile(oldName);
oldName:=dPath+'temp_str' +'.dep';
DeleteFile(oldName);

if form1.ListBox3.Items.Count>0 then
begin
for i:=0 to form1.ListBox3.Items.Count do begin
  form1.ListBox3.ItemIndex:=i;
  depth_good('123');

end;

if (gcycledepthgaz=true) then  begin
  readwriteDepRecdepthbldata();
  end;

oldName:=dPath+'Store' +'.lst';
DeleteFile(oldName);
oldName:=dPath+'Store' +'.dep';
DeleteFile(oldName);



oldName:=dPath+'temp_str' +'.dep';
newName:=dPath+'Store' +'.dep';
RenameFile(oldName, newName);


oldName:=dPath+'temp_str' +'.lst';
newName:=dPath+'Store' +'.lst';
RenameFile(oldName, newName);



if form1.CheckBox2.Checked=true then
   form1.Timer2.Enabled:=true
   else
   form1.Timer2.Enabled:=false;
end;

end;

procedure TForm1.ComboBox2Change(Sender: TObject);
begin
gspeed:= Form1.ComboBox2.ItemIndex;
end;

procedure TForm1.FormClose(Sender: TObject; var Action: TCloseAction);
begin
       form1.Timer1.Enabled:=false;
end;

procedure TForm1.Button15Click(Sender: TObject);
begin
form1.Timer1.Enabled:=false;
Halt;
end;

end.


{const
   // Sets UnixStartDate to TDateTime of 01/01/1970
  UnixStartDate: TDateTime = 25569.0;

 function DateTimeToUnix(ConvDate: TDateTime): longInt;
 begin
   //example: DateTimeToUnix(now);
  Result := Round((ConvDate - UnixStartDate) * 86400);
 end;

 function UnixToDateTime(USec: longInt): TDateTime;
 begin
   //Example: UnixToDateTime(1003187418);
  Result := (Usec / 86400) + UnixStartDate;
 end;
 }
