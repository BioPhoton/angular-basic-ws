# Use takeUntil()-Pattern

1. Change all subsriptions.unsubscribe() to the new takeUntil()-pattern
## Hints

```
let destroy$ = new Subject<boolean>();

this.apiService.pipe(
	takeUntil(this.destroy$)
)
.subscribe((data) => {
 ...
});


ngOnDestroy() {
	this.destroy$.next(true)
}

```
