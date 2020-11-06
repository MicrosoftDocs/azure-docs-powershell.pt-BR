---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 7690143F-5F09-4739-9F66-B2ACDF8305F4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADSpCredential.md
ms.openlocfilehash: 72a2510c673d0e68fc3820fda7b1d99e15a6aa76
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430057"
---
# Get-AzureRmADSpCredential

## Sinopse
Recupera uma lista de credenciais associadas a uma entidade de serviço.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### ObjectIdParameterSet (padrão)
```
Get-AzureRmADSpCredential -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SPNParameterSet
```
Get-AzureRmADSpCredential -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### DisplayNameParameterSet
```
Get-AzureRmADSpCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SPNObjectParameterSet
```
Get-AzureRmADSpCredential -ServicePrincipalObject <PSADServicePrincipal>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet Get-AzureRmADSpCredential pode ser usado para recuperar uma lista de credenciais associadas a uma entidade de serviço.
Esse comando recuperará todas as propriedades de credenciais (mas não o valor da credencial) associados à entidade de serviço.

## EXEMPLOS

### Exemplo 1-listar credenciais por SPN

```
PS C:\> Get-AzureRmADSpCredential -ServicePrincipalName http://test12345
```

Retorna uma lista de credenciais associadas à entidade de serviço com SPN ' http://test12345 '.

### Exemplo 2-listar credenciais por ID do objeto

```
PS C:\> Get-AzureRmADSpCredential -ObjectId 58e28616-99cc-4da4-b705-7672130e1047
```

Retorna uma lista de credenciais associadas à entidade de serviço com a ID de objeto "58e28616-99cc-4DA4-b705-7672130e1047".

### Exemplo de 3-listar credenciais por tubulação

```
PS C:\> Get-AzureRmADServicePrincipal -ObjectId 58e28616-99cc-4da4-b705-7672130e1047 | Get-AzureRmADSpCredential
```

Obtém a entidade de serviço com a ID de objeto "58e28616-99cc-4DA4-b705-7672130e1047" e a canaliza para o cmdlet Get-AzureRmADSpCredential para listar todas as credenciais para essa entidade de serviço.

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
O nome de exibição da entidade de serviço

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

### -ObjectId
A ID de objeto da entidade de serviço para a qual recuperar as credenciais.

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Serviceprincipalnamename
O nome (SPN) da entidade de serviço para a qual recuperar as credenciais.

```yaml
Type: System.String
Parameter Sets: SPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Serviceprincipalnameobject
O objeto de entidade de serviço para o qual recuperar as credenciais.

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal
Parameter Sets: SPNObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential

## INFORMA

## LINKS RELACIONADOS

[New-AzureRmADSpCredential](./New-AzureRmADSpCredential.md)

[Remove-AzureRmADSpCredential](./Remove-AzureRmADSpCredential.md)

[Get-AzureRmADServicePrincipal](./Get-AzureRmADServicePrincipal.md)

