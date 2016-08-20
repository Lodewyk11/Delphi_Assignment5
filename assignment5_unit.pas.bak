unit assignment5_unit;

{$mode objfpc}{$H+}

interface

uses
  Classes, SysUtils, FileUtil, Forms, Controls, Graphics, Dialogs, StdCtrls,
  ComCtrls, Spin, Buttons;

type

  { Tfrm2016Assignment5 }

  Tfrm2016Assignment5 = class(TForm)
    btnResetFor: TBitBtn;
    btnResetWhile: TBitBtn;
    btnForCnt: TButton;
    btnForAdd: TButton;
    btnForConcat: TButton;
    btnWhileCnt: TButton;
    btnWhileAdd: TButton;
    btnWhileConcat: TButton;
    gbFor: TGroupBox;
    gbWhile: TGroupBox;
    lblWhileDescr: TLabel;
    lblWhileProgress: TLabel;
    lblForValue2: TLabel;
    lblForValue1: TLabel;
    lblForExecSpeed: TLabel;
    lblWhileValue1: TLabel;
    lblWhileValue2: TLabel;
    lblWhileExecSpeed: TLabel;
    lblForDescr: TLabel;
    lblForProgress: TLabel;
    lstForResults: TListBox;
    lstWhileResults: TListBox;
    tabCntlr: TPageControl;
    pbarFor: TProgressBar;
    pbarWhile: TProgressBar;
    sedForValue1: TSpinEdit;
    sedForValue2: TSpinEdit;
    sedWhileValue1: TSpinEdit;
    sedWhileValue2: TSpinEdit;
    tbFor: TTabSheet;
    tbWhile: TTabSheet;
    tbForExecSpeed: TTrackBar;
    tbWhileExecSpeed: TTrackBar;
    procedure btnForAddClick(Sender: TObject);
    procedure btnForCntClick(Sender: TObject);
    procedure btnForConcatClick(Sender: TObject);
    procedure btnResetForClick(Sender: TObject);
    procedure btnResetWhileClick(Sender: TObject);
    procedure btnWhileAddClick(Sender: TObject);
    procedure btnWhileCntClick(Sender: TObject);
    procedure btnWhileConcatClick(Sender: TObject);
    procedure FormCreate(Sender: TObject);
    procedure Label2Click(Sender: TObject);
    procedure PageControl1Change(Sender: TObject);
    procedure TabControl1Change(Sender: TObject);
  private
    { private declarations }
  public
    { public declarations }
  end;

var
  frm2016Assignment5: Tfrm2016Assignment5;

implementation

{$R *.lfm}

{ Tfrm2016Assignment5 }

procedure Tfrm2016Assignment5.PageControl1Change(Sender: TObject);
begin

end;

procedure Tfrm2016Assignment5.TabControl1Change(Sender: TObject);
begin
end;

procedure Tfrm2016Assignment5.Label2Click(Sender: TObject);
begin

end;

procedure Tfrm2016Assignment5.FormCreate(Sender: TObject);
begin

end;

procedure Tfrm2016Assignment5.btnWhileCntClick(Sender: TObject);
  //Declare variables.
   var value1 : Integer;
   var value2 : Integer;
   var iCount : Integer;
   var execSpeed : Integer;
   var loopCount : Integer;
begin
  //Get the values from the form.
  value1 := sedWhileValue1.Value;
  value2 := sedWhileValue2.Value;
  execSpeed := tbWhileExecSpeed.Position;

  //Ensure values are valid.
  if(value1 > value2) then
  begin
    ShowMessage('Please ensure that Value 2 is greater than or equal to Value 1');
    exit;
  end;

  //Initialize the loop counter.
  loopCount := 0;

  //Reset the progress bar.
  pbarWhile.Position := 0;
  pbarWhile.Refresh;

  //Print loop header.
  lstWhileResults.Items.Add('*Start of WHILE loop.');
  lstWhileResults.Items.Add(formatdatetime('yyyy/mm/dd', date));
  iCount := value1;
  while iCount <= value2 do
  begin
        //Increment the loop counter and print the result.
        loopCount := loopCount + 1;
        lstWhileResults.Items.add('Digit number: ' + IntToStr(loopCount) + ' is ' + IntToStr(iCount));

        //Update the progress bar (+1 keeps from dividing by 0).
        pbarWhile.Position := Round((iCount+1)/(value2+1)*100);
        pbarWhile.Refresh;

        //Forces repainting of the listbox and scrolls to the botom.
        lstWhileResults.Refresh;
        lstWhileResults.TopIndex := lstWhileResults.Items.Count -1;

        //Pauses execution of the loop based on the execution time slider.
        if(value2 > value1) then Sleep((10-execSpeed)*100);
        iCount := iCount + 1;
  end;
  lstWhileResults.Items.Add('*End of WHILE loop.');
  lstWhileResults.Items.Add(''); ;
end;

procedure Tfrm2016Assignment5.btnWhileConcatClick(Sender: TObject);
  //Declare variables.
  var value1 : Integer;
  var value2 : Integer;
  var iCount : Integer;
  var execSpeed : Integer;
  var concatStr : String;
begin
 //Get the values from the form.
 value1 := sedWhileValue1.Value;
 value2 := sedWhileValue2.Value;
 execSpeed := tbWhileExecSpeed.Position;

 //Ensure values are valid.
  if(value1 > value2) then
  begin
    ShowMessage('Please ensure that Value 2 is greater than or equal to Value 1');
    exit;
  end;

 //Initialize the total variable.
 concatStr := '';

 //Reset the progress bar.
 pbarWhile.Position := 0;
 pbarWhile.Refresh;

 //Print loop header
 lstWhileResults.Items.Add('*Start of WHILE loop.');
 lstWhileResults.Items.Add(formatdatetime('yyyy/mm/dd', date));
 lstWhileResults.Items.Add('Initial value of concatStr: ' + concatStr);

 iCount := value1;
 while iCount <= value2 do
 begin
       //Calculate the total up to now and print the result.
       concatStr := concatStr + IntToStr(iCount);
       lstWhileResults.Items.add('Contents of concatStr: ' + concatStr);

       //Update the progress bar (+1 keeps from dividing by 0).
       pbarFor.Position := Round((iCount+1)/(value2+1)*100);
       pbarFor.Refresh;

       //Forces repainting of the listbox and scrolls to the botom.
       lstWhileResults.Refresh;
       lstWhileResults.TopIndex := lstForResults.Items.Count -1;

       //Pauses execution of the loop based on the execution time slider.
       if(value2 > value1) then Sleep((10-execSpeed)*100);
       iCount := iCount + 1;
 end;
 lstWhileResults.Items.Add('*End of WHILE loop.');
 lstWhileResults.Items.Add('');
end;

procedure Tfrm2016Assignment5.btnForCntClick(Sender: TObject);
   //Declare variables.
   var value1 : Integer;
   var value2 : Integer;
   var iCount : Integer;
   var execSpeed : Integer;
   var loopCount : Integer;
begin
  //Get the values from the form.
  value1 := sedForValue1.Value;
  value2 := sedForValue2.Value;
  execSpeed := tbForExecSpeed.Position;

  //Ensure values are valid.
  if(value1 > value2) then
  begin
    ShowMessage('Please ensure that Value 2 is greater than or equal to Value 1');
    exit;
  end;

  //Initialize the loop counter.
  loopCount := 0;

  //Reset the progress bar.
  pbarFor.Position := 0;
  pbarFor.Refresh;

  //Print loop header.
  lstForResults.Items.Add('*Start of FOR loop.');
  lstForResults.Items.Add(formatdatetime('yyyy/mm/dd', date));

  for iCount := value1 to value2 do
  begin
        //Increment the loop counter and print the result.
        loopCount := loopCount + 1;
        lstForResults.Items.add('Digit number: ' + IntToStr(loopCount) + ' is ' + IntToStr(iCount));

        //Update the progress bar (+1 keeps from dividing by 0).
        pbarFor.Position := Round((iCount+1)/(value2+1)*100);
        pbarFor.Refresh;

        //Forces repainting of the listbox and scrolls to the botom.
        lstForResults.Refresh;
        lstForResults.TopIndex := lstForResults.Items.Count -1;

        //Pauses execution of the loop based on the execution time slider.
        if(value2 > value1) then Sleep((10-execSpeed)*100);
  end;
  lstForResults.Items.Add('*End of FOR loop.');
  lstForResults.Items.Add('');
end;

procedure Tfrm2016Assignment5.btnForConcatClick(Sender: TObject);
  //Declare variables.
  var value1 : Integer;
  var value2 : Integer;
  var iCount : Integer;
  var execSpeed : Integer;
  var concatStr : String;
begin
 //Get the values from the form.
 value1 := sedForValue1.Value;
 value2 := sedForValue2.Value;
 execSpeed := tbForExecSpeed.Position;

 //Ensure values are valid.
  if(value1 > value2) then
  begin
    ShowMessage('Please ensure that Value 2 is greater than or equal to Value 1');
    exit;
  end;

 //Initialize the total variable.
 concatStr := '';

 //Reset the progress bar.
 pbarFor.Position := 0;
 pbarFor.Refresh;

 //Print loop header
 lstForResults.Items.Add('*Start of FOR loop.');
 lstForResults.Items.Add(formatdatetime('yyyy/mm/dd', date));
 lstForResults.Items.Add('Initial value of concatStr: ' + concatStr);

 for iCount := value1 to value2 do
 begin
       //Calculate the total up to now and print the result.
       concatStr := concatStr + IntToStr(iCount);
       lstForResults.Items.add('Contents of concatStr: ' + concatStr);

       //Update the progress bar (+1 keeps from dividing by 0).
       pbarFor.Position := Round((iCount+1)/(value2+1)*100);
       pbarFor.Refresh;

       //Forces repainting of the listbox and scrolls to the botom.
       lstForResults.Refresh;
       lstForResults.TopIndex := lstForResults.Items.Count -1;

       //Pauses execution of the loop based on the execution time slider.
       if(value2 > value1) then Sleep((10-execSpeed)*100);
 end;
 lstForResults.Items.Add('*End of FOR loop.');
 lstForResults.Items.Add('');

end;

procedure Tfrm2016Assignment5.btnResetForClick(Sender: TObject);
begin
     sedForValue1.Value := 0;
     sedForValue2.Value := 0;
     tbForExecSpeed.Position := 0;
     lstForResults.Clear;
     pbarFor.Position := 0;
end;

procedure Tfrm2016Assignment5.btnResetWhileClick(Sender: TObject);
begin
     sedWhileValue1.Value := 0;
     sedWhileValue2.Value := 0;
     tbWhileExecSpeed.Position := 0;
     lstWhileResults.Clear;
     pbarWhile.Position := 0;
end;

procedure Tfrm2016Assignment5.btnWhileAddClick(Sender: TObject);
   //Declare variables.
   var value1 : Integer;
   var value2 : Integer;
   var iCount : Integer;
   var execSpeed : Integer;
   var nTotal : Integer;
begin
  //Get the values from the form.
  value1 := sedWhileValue1.Value;
  value2 := sedWhileValue2.Value;
  execSpeed := tbWhileExecSpeed.Position;

  //Ensure values are valid.
  if(value1 > value2) then
  begin
    ShowMessage('Please ensure that Value 2 is greater than or equal to Value 1');
    exit;
  end;

  //Initialize the total variable.
  nTotal := 0;

  //Reset the progress bar.
  pbarWhile.Position := 0;
  pbarWhile.Refresh;

  //Print loop header
  lstWhileResults.Items.Add('*Start of FOR loop.');
  lstWhileResults.Items.Add(formatdatetime('yyyy/mm/dd', date));
  lstWhileResults.Items.Add('Initial value of nTotal: ' + IntToStr(nTotal));

  iCount := value1;
  while iCount <= value2 do
  begin
        //Calculate the total up to now and print the result.
        nTotal := nTotal + iCount;
        lstWhileResults.Items.add('Value of nTotal: ' + IntToStr(nTotal));

        //Update the progress bar (+1 keeps from dividing by 0).
        pbarWhile.Position := Round((iCount+1)/(value2+1)*100);
        pbarWhile.Refresh;

        //Forces repainting of the listbox and scrolls to the botom.
        lstWhileResults.Refresh;
        lstWhileResults.TopIndex := lstForResults.Items.Count -1;

        //Pauses execution of the loop based on the execution time slider.
        if(value2 > value1) then Sleep((10-execSpeed)*100);
        iCount := iCount + 1;
  end;
  lstWhileResults.Items.Add('*End of FOR loop.');
  lstWhileResults.Items.Add('');
end;

procedure Tfrm2016Assignment5.btnForAddClick(Sender: TObject);
   //Declare variables.
   var value1 : Integer;
   var value2 : Integer;
   var iCount : Integer;
   var execSpeed : Integer;
   var nTotal : Integer;
begin
  //Get the values from the form.
  value1 := sedForValue1.Value;
  value2 := sedForValue2.Value;
  execSpeed := tbForExecSpeed.Position;

  //Initialize the total variable.
  nTotal := 0;

  //Reset the progress bar.
  pbarFor.Position := 0;
  pbarFor.Refresh;

  //Print loop header
  lstForResults.Items.Add('*Start of FOR loop.');
  lstForResults.Items.Add(formatdatetime('yyyy/mm/dd', date));
  lstForResults.Items.Add('Initial value of nTotal: ' + IntToStr(nTotal));

  for iCount := value1 to value2 do
  begin
        //Calculate the total up to now and print the result.
        nTotal := nTotal + iCount;
        lstForResults.Items.add('Value of nTotal: ' + IntToStr(nTotal));

        //Update the progress bar (+1 keeps from dividing by 0).
        pbarFor.Position := Round((iCount+1)/(value2+1)*100);
        pbarFor.Refresh;

        //Forces repainting of the listbox and scrolls to the botom.
        lstForResults.Refresh;
        lstForResults.TopIndex := lstForResults.Items.Count -1;

        //Pauses execution of the loop based on the execution time slider.
        if(value2 > value1) then Sleep((10-execSpeed)*100);
  end;
  lstForResults.Items.Add('*End of FOR loop.');
  lstForResults.Items.Add('');

end;

end.

