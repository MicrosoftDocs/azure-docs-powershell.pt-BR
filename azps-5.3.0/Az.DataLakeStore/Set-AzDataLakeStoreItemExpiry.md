---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitemexpiry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemExpiry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemExpiry.md
ms.openlocfilehash: ff769801c7a3496ab094e5c9877e0b53fb64fbfd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98426589"
---
# Set-AzDataLakeStoreItemExpiry

## Sinopse
Define ou remove o tempo de expiração de um arquivo em uma conta do Azure data Lake Store.

## SYNTAX

### SetAbsoluteNeverExpireExpiry (padrão)
```
Set-AzDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [[-Expiration] <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetRelativeExpiry
```
Set-AzDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-RelativeFileExpiryOption] <PathRelativeExpiryOptions> [[-RelativeTime] <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **set-AzDataLakeStoreItemExpiry** define ou remove o tempo de expiração de um arquivo em uma conta do Azure data Lake Store.

## EXEMPLOS

### Exemplo 1: definir o tempo de expiração de um arquivo
```
PS C:\> Set-AzDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt -Expiration [DateTimeOffset]::Now.AddHours(2)
```

Define a expiração no arquivo myfile.txt na conta ContosoADL para ser de duas horas a partir de agora.
Isso fará com que o arquivo expire (ser marcado para exclusão) em duas horas.

### Exemplo 2: remover a expiração em um arquivo
```
PS C:\> Set-AzDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt
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
Type: System.String
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

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
Type: System.DateTimeOffset
Parameter Sets: SetAbsoluteNeverExpireExpiry
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Caminho
Especifica o caminho do repositório data Lake do item de arquivo para o qual definir ou remover a expiração.

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RelativeFileExpiryOption
Opções de expiração relativas. RelativeToNow ou RelativeToCreationDate são opções atuais

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathRelativeExpiryOptions
Parameter Sets: SetRelativeExpiry
Aliases:
Accepted values: RelativeToNow, RelativeToCreationDate

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Relativetime
O tempo relativo em milissegundos em relação ao momento ou à hora da criação

```yaml
Type: System.Int64
Parameter Sets: SetRelativeExpiry
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
Type: System.Management.Automation.SwitchParameter
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
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### System. String

### Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance

### System. DateTimeOffset

### Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreEnums + PathRelativeExpiryOptions

### System. Int64

## EXIBE

### Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreItem

## INFORMA
Alias: Set-AdlStoreItemExpiry

## LINKS RELACIONADOS

[Get-AzDataLakeStoreItem](./Get-AzDataLakeStoreItem.md)

