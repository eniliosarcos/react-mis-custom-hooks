# useForm hook

ejemplo de uso:
```
    const initialForm = {
        searchText:''
    }

    const [formValues, handleInputChange, reset] = useForm(initialForm);

    const handleSearch = (e) => {

        e.preventDefault();
        console.log(formValues.searchText);
    }

    return (
        <div className="col-5">
                <h4>Search Form</h4>
                <hr/>

                <form onSubmit={handleSearch}>
                    <input
                        type="text"
                        placeholder="some text..."
                        className="form-control"
                        name="searchText"
                        autoComplete="off"
                        value= {formValues.searchText}
                        onChange={handleInputChange}
                />

                <button
                    type="submit"
                    className="btn mt-1 btn-block btn-outline-primary"
                >
                     Search...
                </button>
            </form>
        </div>
    )
```