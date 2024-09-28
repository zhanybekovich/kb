
```php
Forms\Components\TextInput::make('title')
                        ->live(onBlur: true)
                        ->required()->minLength(3)->maxLength(150)
                        ->afterStateUpdated(function (string $operation, $state, Forms\Set $set) {
                            if ($operation === 'edit') {
                                return;
                            }
  
                            $set('slug', Str::slug($state));
                        })
                        ->columnSpanFull()
                        ->label('Название/Тема'),
                    Forms\Components\TextInput::make('slug')
                        ->unique(ignoreRecord: true)->maxLength(150)
                        ->required()
                        ->maxLength(255)
                        ->columnSpanFull(),
```