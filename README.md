public class MyViewModel : INotifyPropertyChanged
{
    private List<string> _myArrayList = new List<string>();
    public List<string> MyArrayList
    {
        get { return _myArrayList; }
        set
        {
            _myArrayList = value;
            OnPropertyChanged("MyArrayList");
        }
    }
    private string _entryValue;
    public string EntryValue
    {
        get { return _entryValue; }
        set
        {
            _entryValue = value;
            OnPropertyChanged("EntryValue");
        }
    }
    public event PropertyChangedEventHandler PropertyChanged;
    protected void OnPropertyChanged(string propertyName)
    {
        if (PropertyChanged != null)
        {
            PropertyChanged(this, new PropertyChangedEventArgs(propertyName));
        }
    }



    private ICommand _addCommand;
    public ICommand AddCommand
    {
        get
        {
            if (_addCommand == null)
            {
                _addCommand = new RelayCommand(param => this.Add(),
                    null);
            }
            return _addCommand;
        }
    }
    private void Add()
    {
        MyArrayList.Add(EntryValue);
        EntryValue = string.Empty;
    }



<Button Command="{Binding AddCommand}"/>
<Entry Text="{Binding EntryValue}"/>
<ListView ItemsSource="{Binding MyArrayList}">
    ...
</ListView>


