# cerrors
Constant error wrappers from Cheney.

The original article by Cheney is
[here](https://dave.cheney.net/2016/04/07/constant-errors).

Myren has a good
[article](https://smyrman.medium.com/writing-constant-errors-with-go-1-13-10c4191617).

## Usage
Define a new error:

	const ErrFoo = cerror.Error("foo")

Use `errors.Is` to test:

	if err := someFunc(); errors.Is(err, ErrFoo) {
        // ... //
    }
