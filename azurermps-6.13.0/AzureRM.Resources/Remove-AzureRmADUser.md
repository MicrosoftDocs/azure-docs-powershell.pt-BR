---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 9F9B2691-BB3F-4644-BD95-6D74777D1E99
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADUser.md
ms.openlocfilehash: 1b863b0bc9cb90caca4d7431ec6835cb75836609
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609751"
---
# Remove-AzureRmADUser

## Sinopse
Exclui um usuário do Active Directory.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### UPNOrObjectIdParameterSet (padrão)
```
Remove-AzureRmADUser -UPNOrObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### UPNParameterSet
```
Remove-AzureRmADUser -UserPrincipalName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ObjectIdParameterSet
```
Remove-AzureRmADUser -ObjectId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### DisplayNameParameterSet
```
Remove-AzureRmADUser -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObjectParameterSet
```
Remove-AzureRmADUser -InputObject <PSADUser> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
Exclui um usuário do Active Directory (conta corporativa/de estudante também conhecida como identificação da organização).

## EXEMPLOS

### Exemplo 1-remover um usuário pelo nome principal do usuário

```
PS C:\> Remove-AzureRmADUser -UserPrincipalName foo@domain.com
```

Remove o usuário com o nome de usuário principal " foo@domain.com " do locatário.

### Exemplo 2-remover um usuário por ID de objeto

```
PS C:\> Remove-AzureRmADUser -ObjectId 7a9582cf-88c4-4319-842b-7a5d60967a69
```

Remove o usuário com a ID de objeto ' 7a9582cf-88c4-4319-842b-7a5d60967a69 ' do locatário.

### Exemplo 3-remover um usuário por meio do encanamento

```
PS C:\> Get-AzureRmADUser -ObjectId 7a9582cf-88c4-4319-842b-7a5d60967a69 | Remove-AzureRmADUser
```

Obtém o usuário com a ID de objeto ' 7a9582cf-88c4-4319-842b-7a5d60967a69 ' e canaliza-se para o cmdlet Remove-AzureRmADUser para remover o usuário do locatário.

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisplayName
O nome de exibição do usuário a ser excluído.

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force
Se especificado, não solicita confirmação para excluir o usuário.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
O objeto de usuário a ser excluído.

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ObjectId
A ID de objeto do usuário a ser excluído.

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Se o comando foi concluído, a especificação será retorna true se o comando foi bem-sucedido.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UPNOrObjectId
O nome principal do usuário ou o objectId do usuário a ser excluído.

```yaml
Type: System.String
Parameter Sets: UPNOrObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UserPrincipalName
O nome UPN do usuário a ser excluído.

```yaml
Type: System.String
Parameter Sets: UPNParameterSet
Aliases: UPN

Required: True
Position: Named
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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### System. String

### System. GUID

### Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser
Parâmetros: inputobject (ByValue)

## EXIBE

### System. Boolean

## INFORMA

## LINKS RELACIONADOS

[New-AzureRmADUser](./New-AzureRmADUser.md)

[Get-AzureRmADUser](./Get-AzureRmADUser.md)

[Set-AzureRmADUser](./Set-AzureRmADUser.md)

