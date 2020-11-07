---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: EB4A7F84-99E4-49B1-856D-EC0736058D23
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8cab29cd7d285d2ae1aae9c007be965e1bbf8f2f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945850"
---
# Set-AzureStorageAccount

## Sinopse
Atualiza as propriedades de uma conta de armazenamento em uma assinatura do Azure.

## SYNTAX

### AccountType (padrão)
```
Set-AzureStorageAccount [-StorageAccountName] <String> [-Label <String>] [-Description <String>]
 [-Type <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### GeoReplicationEnabled
```
Set-AzureStorageAccount [-StorageAccountName] <String> [-Label <String>] [-Description <String>]
 [-GeoReplicationEnabled <Boolean>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **set-AzureStorageAccount** atualiza as propriedades de uma conta de armazenamento do Azure na assinatura atual.
As propriedades que podem ser definidas são: **rótulo** , **Descrição** , **tipo** e **GeoReplicationEnabled**.

## EXEMPLOS

### Exemplo 1: atualizar o rótulo de uma conta de armazenamento
```
PS C:\> Set-AzureStorageAccount -StorageAccountName "ContosoStorage01" -Label "ContosoAccnt" -Description "Contoso storage account"
```

Esse comando atualiza as propriedades **rótulo** e **Descrição** da conta de armazenamento chamada ContosoStorage01.

### Exemplo 2: habilitar a replicação geográfica para uma conta de armazenamento
```
PS C:\> Set-AzureStorageAccount -StorageAccountName "ContosoStorage01" -GeoReplicationEnabled $False
```

Esse comando define a propriedade **GeoReplicationEnabled** como $false para a conta de armazenamento chamada ContosoStorage01.

### Exemplo 3: desabilitar a replicação geográfica para uma conta de armazenamento
```
PS C:\> Set-AzureStorageAccount -StorageAccountName "ContosoStorage01" -GeoReplicationEnabled $True
```

Esse comando define a propriedade **GeoReplicationEnabled** como $true para a conta de armazenamento chamada ContosoStorage01.

## OS

### -Descrição
Especifica uma descrição para a conta de armazenamento.
A descrição pode ter até 1024 caracteres de comprimento.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GeoReplicationEnabled
Especifica se a conta de armazenamento é criada com a replicação geográfica habilitada.

```yaml
Type: Boolean
Parameter Sets: GeoReplicationEnabled
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -Rótulo
Especifica um rótulo para a conta de armazenamento.
O rótulo pode ter até 100 caracteres de comprimento.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

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
Especifica o nome da conta de armazenamento que esse cmdlet modifica.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Digite
Especifica o tipo da conta de armazenamento.
Os valores válidos são: 

- Standard_LRS
- Standard_ZRS
- Standard_GRS
- Standard_RAGRS
- Premium_LRS

Se esse parâmetro não for especificado, o valor padrão será Standard_GRS.

O efeito de especificar o parâmetro *GeoReplicationEnabled* é o mesmo que especificar Standard_GRS no parâmetro *Type* .

Standard_ZRS ou Premium_LRS contas não podem ser alteradas para outros tipos de conta e vice-versa.

```yaml
Type: String
Parameter Sets: AccountType
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

## INFORMA

## LINKS RELACIONADOS

[Get-AzureStorageAccount](./Get-AzureStorageAccount.md)

[New-AzureStorageAccount](./New-AzureStorageAccount.md)

[Remove-AzureStorageAccount](./Remove-AzureStorageAccount.md)


