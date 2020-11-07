---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 04B1E3A6-6D52-46A3-8241-2CCDB5E71642
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadspcredential
schema: 2.0.0
ms.openlocfilehash: 73fff5ff4cf612c39bacd26fed61c4e856e34128
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785154"
---
# Remove-AzureRmADSpCredential

## Sinopse
Remove uma credencial de uma entidade de serviço.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### ObjectIdWithKeyIdParameterSet (padrão)
```
Remove-AzureRmADSpCredential -ObjectId <Guid> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SPNWithKeyIdParameterSet
```
Remove-AzureRmADSpCredential -ServicePrincipalName <String> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DisplayNameWithKeyIdParameterSet
```
Remove-AzureRmADSpCredential -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ServicePrincipalObjectParameterSet
```
Remove-AzureRmADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-KeyId <Guid>] [-PassThru]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet Remove-AzureRmADSpCredential pode ser usado para remover uma chave de credencial de uma entidade de serviço no caso de um comprometimento ou como parte da expiração da sobreposição da chave da credencial.
A entidade de serviço é identificada fornecendo a identificação do objeto ou o SPN (nome da entidade de serviço).
A credencial a ser removida é identificada pela ID da chave se uma credencial individual for removida ou com uma opção ' all' para excluir todas as credenciais associadas à entidade de serviço.

## EXEMPLOS

### Exemplo 1: remover uma credencial específica de uma entidade de serviço

```
PS C:\> Remove-AzureRmADSpCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

Remove a credencial com a ID da chave ' 9044423a-60a3-45ac-9ab1-09534157ebb ' da entidade de serviço com a ID de objeto ' 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 '.

### Exemplo 2-remover todas as credenciais de uma entidade de serviço

```
PS C:\> Remove-AzureRmADSpCredential -ServicePrincipalName http://test123
```

Remove todas as credenciais da entidade de serviço com o SPN " http://test123 ".

### Exemplo 3-remover todas as credenciais de uma entidade de serviço usando o encanamento

```
PS C:\> Get-AzureRmADServicePrincipal -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 | Remove-AzureRmADSpCredential
```

Obtém a entidade de serviço com a ID de objeto ' 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 ' e canaliza-a para o cmdlet Remove-AzureRmADSpCredential para remover todas as credenciais dessa entidade de serviço.

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
O nome de exibição da entidade de serviço.

```yaml
Type: System.String
Parameter Sets: DisplayNameWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force
Alternar para excluir credencial sem confirmação.

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

### -KeyId
Especifica a chave de credencial a ser removida.
As IDs de chave para uma entidade de serviço podem ser obtidas usando o cmdlet Get-AzureRmADSpCredential.

```yaml
Type: System.Guid
Parameter Sets: ObjectIdWithKeyIdParameterSet, SPNWithKeyIdParameterSet, ServicePrincipalObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ObjectId
A ID de objeto da entidade de serviço para a qual as credenciais são removidas.

```yaml
Type: System.Guid
Parameter Sets: ObjectIdWithKeyIdParameterSet
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

### -Serviceprincipalnamename
O nome (SPN) da entidade de serviço para a qual remover as credenciais.

```yaml
Type: System.String
Parameter Sets: SPNWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Serviceprincipalnameobject
O objeto de entidade de serviço para o qual remover as credenciais.

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal
Parameter Sets: ServicePrincipalObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### System. GUID

### System. String

### Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal
Parâmetros: servicePrincipalName (ByValue)

## EXIBE

### System. Boolean

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmADSpCredential](./Get-AzureRmADSpCredential.md)

[New-AzureRmADSpCredential](./New-AzureRmADSpCredential.md)

[Get-AzureRmADServicePrincipal](./Get-AzureRmADServicePrincipal.md)

