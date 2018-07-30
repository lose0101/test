""" Two-dimensional size-mutable, potentially heterogeneous tabular data
    structure with labeled axes (rows and columns). Arithmetic operations
    align on both row and column labels. Can be thought of as a dict-like
    container for Series objects. The primary pandas data structure

    Parameters
    ----------
    data : numpy ndarray (structured or homogeneous), dict, or DataFrame
        Dict can contain Series, arrays, constants, or list-like objects
    index : Index or array-like
        Index to use for resulting frame. Will default to np.arange(n) if
        no indexing information part of input data and no index provided
    columns : Index or array-like
        Column labels to use for resulting frame. Will default to
        np.arange(n) if no column labels are provided
    dtype : dtype, default None
        Data type to force. Only a single dtype is allowed. If None, infer
    copy : boolean, default False
        Copy data from inputs. Only affects DataFrame / 2d ndarray input

    Examples
    --------
    Constructing DataFrame from a dictionary.

    >>> d = {'col1': [1, 2], 'col2': [3, 4]}
    >>> df = pd.DataFrame(data=d)
    >>> df
       col1  col2
    0     1     3
    1     2     4

    Notice that the inferred dtype is int64.

    >>> df.dtypes
    col1    int64
    col2    int64
    dtype: object

    To enforce a single dtype:

    >>> df = pd.DataFrame(data=d, dtype=np.int8)
    >>> df.dtypes
    col1    int8
    col2    int8
    dtype: object

    Constructing DataFrame from numpy ndarray:

    >>> df2 = pd.DataFrame(np.random.randint(low=0, high=10, size=(5, 5)),
    ...                    columns=['a', 'b', 'c', 'd', 'e'])
    >>> df2
        a   b   c   d   e
    0   2   8   8   3   4
    1   4   2   9   0   9
    2   1   0   7   8   0
    3   5   1   7   1   3
    4   6   0   2   4   2

    See also
    --------
    DataFrame.from_records : constructor from tuples, also record arrays
    DataFrame.from_dict : from dicts of Series, arrays, or dicts
    DataFrame.from_items : from sequence of (key, value) pairs
    pandas.read_csv, pandas.read_table, pandas.read_clipboard
    """
