---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoreitemexpiry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemExpiry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemExpiry.md
ms.openlocfilehash: 6908bc4d474d0dbe9df045332f3820b5f7536dac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432511"
---
# Set-AzureRmDataLakeStoreItemExpiry

## Sinopse
Define ou remove o tempo de expiração de um arquivo em uma conta do Azure data Lake Store.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### SetAbsoluteNeverExpireExpiry (padrão)
```
Set-AzureRmDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [[-Expiration] <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetRelativeExpiry
```
Set-AzureRmDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [[-RelativeFileExpiryOption] <PathRelativeExpiryOptions>] [[-RelativeTime] <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **set-AzureRmDataLakeStoreItemExpiry** define ou remove o tempo de expiração de um arquivo em uma conta do Azure data Lake Store.

## EXEMPLOS

### Exemplo 1: definir o tempo de expiração de um arquivo
```
PS C:\> Set-AzureRmDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt -Expiration [DateTimeOffset]::Now.AddHours(2)
```

Define a expiração no arquivo myfile.txt na conta ContosoADL para ser de duas horas a partir de agora.
Isso fará com que o arquivo expire (ser marcado para exclusão) em duas horas.

### Exemplo 2: remover a expiração em um arquivo
```
PS C:\> Set-AzureRmDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt
```

Remove qualquer expiração definida anteriormente no arquivo ' myfile.txt ' na conta ' ContosoADL '.
Isso significa que o arquivo não expirará automaticamente (será marcado para exclusão) e precisará ser excluído manualmente ou definido para expirar novamente.


### Exemplo 3: definir a hora de expiração para um arquivo relativo a agora
```
PS C:\> Set-AdlStoreItemExpiry -Account "ContosoADL" -path /myfile.txt -RelativeFileExpiryOption RelativeToNow -RelativeTime 240000
PS C:\> Set-AdlStoreItemExpiry -Account "ContosoADL" -path /myfile.txt -RelativeFileExpiryOption RelativeToCreationDate -RelativeTime 240000
```

O primeiro comando define o tempo de expiração do arquivo/myfile.txt 240 segundos relativo à hora atual no servidor.

O segundo comando define o tempo de expiração do arquivo/myfile.txt 240 segundos relativo à hora da criação no servidor.

## OS

### -Conta
Especifica o nome da conta do data Lake Store.

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Expiração
O tempo de expiração absoluto do arquivo especificado.
Se nenhum valor ou for definido como MaxValue, o arquivo nunca expirará.

```yaml
Type: DateTimeOffset
Parameter Sets: Set expiry as Absolute or NeverExpire
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RelativeFileExpiryOption
Opções de expiração relativas. RelativeToNow ou RelativeToCreationDate são opções atuais
```yaml
Type: PathRelativeExpiryOptions
Parameter Sets: Set expiry as relative to creation or now
Aliases: 
Accepted values: RelativeToNow, RelativeToCreationDate

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Caminho
Especifica o caminho do repositório data Lake do item de arquivo para o qual definir ou remover a expiração.

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Relativetime
O tempo relativo em milissegundos em relação ao momento ou à hora da criação
```yaml
Type: Int64
Parameter Sets: Set expiry as relative to creation or now
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirme
Solicita confirmação antes de executar o cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra o que aconteceria se o cmdlet fosse executado.
O cmdlet não é executado.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma
Esse cmdlet não aceita nenhuma entrada.

## EXIBE

### DataLakeStoreItem
O arquivo atualizado com um novo tempo de expiração.

## INFORMA
Alias: Set-AdlStoreItemExpiry

## LINKS RELACIONADOS

[Get-AzureRmDataLakeStoreItem](./Get-AzureRmDataLakeStoreItem.md)

