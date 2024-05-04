unit UnitMain;

interface

uses
  Windows, Messages, SysUtils, Variants, Classes, Graphics, Controls, Forms,
  Dialogs, StdCtrls,ShellAPI;

type
  TForm1 = class(TForm)
    Button1: TButton;
    Edit1: TEdit;
    procedure Button1Click(Sender: TObject);
  private
    { Private declarations }
    function
    GetDosCommand(Command: string): string;
  public
    { Public declarations }
  end;

var
  Form1: TForm1;

implementation

{$R *.dfm}

function TForm1.GetDosCommand(Command: string): string;
begin
   // 将命令转换为可执行的DOS命令
  Result := 'cmd.exe /c ' + Command;

end;

procedure TForm1.Button1Click(Sender: TObject);
var
  command:string;
begin
  //ShellExecute(0, nil, 'cmd.exe', PChar(Edit1.Text), nil, SW_SHOWNORMAL);
     Command :=PChar(Edit1.Text);
        // 在DOS窗口中运行转换命令
     Command := GetDosCommand(Command);
     ShellExecute(Handle, 'open', 'cmd.exe', PChar(Command), nil, SW_HIDE);
  
end;
end.
