---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 35588231-CBAC-4411-9531-9A06BD298ACA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7fdcad4b3a0f41f0589e49d4b33a767b93267855
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945548"
---
# Get-AzureStorageKey

## Sinopse
Retorna as chaves de conta de armazenamento primária e secundária para uma conta de armazenamento do Azure.

## SYNTAX

```
Get-AzureStorageKey [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureStorageKey** retorna um objeto com o nome da conta de armazenamento do Azure, a chave da conta primária e a chave da conta secundária da conta de armazenamento do Azure especificada como propriedades.

## EXEMPLOS

### Exemplo 1: obter um objeto que contém as chaves de armazenamento principal e secundário
```
PS C:\> Get-AzureStorageKey -StorageAccountName "ContosoStore01"
```

Esse comando obtém um objeto com as chaves de armazenamento principal e secundário para a conta de armazenamento do ContosoStore01.

### Exemplo 2: obter a chave da conta de armazenamento principal e armazená-la em uma variável
```
PS C:\> $ContosoStoreKey = (Get-AzureStorageKey -StorageAccountName "ContosoStore01").Primary
```

Esse comando coloca a chave da conta de armazenamento primária da conta de armazenamento do ContosoStore01 na variável $ContosoStoreKey.

## OS

### -Informationaction
Especifica como esse cmdlet responde a um evento de informações.

Os valores aceitáveis para esse parâmetro são:

- Contínuo
- Ignorar
- Inquire
- SilentlyContinue
- Finaliza
- Suspensão

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Especifica uma variável de informações.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Perfil
Especifica o perfil do Azure do qual este cmdlet lê.
Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountName
Especifica o nome da conta de armazenamento.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

## INFORMA
* Para obter ajuda com Node.js, use o `help node-dev` comando. Para obter ajuda com as extensões do PHP, use o `help php-dev` comando.

## LINKS RELACIONADOS

[Get-AzureStorageAccount](./Get-AzureStorageAccount.md)

[New-AzureStorageAccount](./New-AzureStorageAccount.md)

[New-AzureStorageKey](./New-AzureStorageKey.md)

[Remove-AzureStorageAccount](./Remove-AzureStorageAccount.md)

[Set-AzureStorageAccount](./Set-AzureStorageAccount.md)


