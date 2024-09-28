Password confirmation and ignoring required password on edit page

```
Forms\Components\TextInput::make('password')  
    ->password()  
    ->maxLength(24)  
    ->confirmed()  
    ->dehydrateStateUsing(fn (string $state): string => Hash::make($state))  
    ->dehydrated(fn (?string $state): bool => filled($state))  
    ->required(fn (string $operation): bool => $operation === 'create')  
    ->revealable()  
    ->label('Пароль'),  
Forms\Components\TextInput::make('password_confirmation')  
    ->password()  
    ->maxLength(24)  
    ->dehydrateStateUsing(fn (string $state): string => Hash::make($state))  
    ->dehydrated(fn (?string $state): bool => filled($state))  
    ->required(fn (string $operation): bool => $operation === 'create')  
    ->revealable()  
    ->label('Подтверждение пароля'),
```