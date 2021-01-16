---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/new-azmanagedservicesdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesDefinition.md
ms.openlocfilehash: f8d2eded01e4816b99b71475aca896c697dd5ae0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263799"
---
# New-AzManagedServicesDefinition

## Sinopse
Cria ou atualiza uma definição de registro.

## SYNTAX

### Padrão (padrão)
```
New-AzManagedServicesDefinition [-Name <String>] -DisplayName <String> -ManagedByTenantId <String>
 [-Description <String>] -PrincipalId <String> -RoleDefinitionId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByPlan
```
New-AzManagedServicesDefinition [-Name <String>] -DisplayName <String> -ManagedByTenantId <String>
 [-Description <String>] -Authorization <Authorization[]> -PlanName <String> -PlanPublisher <String>
 -PlanProduct <String> -PlanVersion <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByAuthorization
```
New-AzManagedServicesDefinition [-Name <String>] -DisplayName <String> -ManagedByTenantId <String>
 [-Description <String>] -Authorization <Authorization[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
Cria ou atualiza uma definição de registro.

## EXEMPLOS

### Exemplo 1
```
PS C:\> New-AzManagedServicesDefinition -DisplayName "MyTestDefinition" -ManagedByTenantId 72f9acbf-86f1-41af-91ab-2d7ef011db47 -RoleDefinitionId acdd72a7-3385-48ef-bd42-f606fba81ae7 -PrincipalId 714160ec-87d5-42bb-8b17-287c0dd7417d

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
b732e39c-c034-44cd-b5a1-094669ccc8c5 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/b732e39c-c034-44cd-b5a1-094669ccc8c5 Succeeded


PS C:\>
```

Cria uma definição de registro pelos valores roleDefinitionId e dirigeid fornecidos diretamente.

### Exemplo 2
```
PS C:\> $auths = @(
>>   [Microsoft.Azure.Management.ManagedServices.Models.Authorization]@{RoleDefinitionId = "acdd72a7-3385-48ef-bd42-f606fba81ae7"; PrincipalId = "714160ec-87d5-42bb-8b17-287c0dd7417d" }
>>  );
PS C:\> $definition = New-AzManagedServicesDefinition -DisplayName "MyTestDefinition" -ManagedByTenantId 72f9acbf-86f1-41af-91ab-2d7ef011db47 -Authorization $auths
PS C:\> $definition

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
55a89269-0347-4a9c-a778-c3f37b9f8672 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672 Succeeded


PS C:\>
```

Cria ou atualiza uma definição de registro com detalhes de autorização.

### Exemplo 3
```
PS C:\> $auths = @(
>>   [Microsoft.Azure.Management.ManagedServices.Models.Authorization]@{RoleDefinitionId = "acdd72a7-3385-48ef-bd42-f606fba81ae7"; PrincipalId = "714160ec-87d5-42bb-8b17-287c0dd7417d" },
>>   [Microsoft.Azure.Management.ManagedServices.Models.Authorization]@{RoleDefinitionId = "9980e02c-c2be-4d73-94e8-173b1dc7cf3c"; PrincipalId = "714160ec-87d5-42bb-8b17-287c0dd7417d" }
>>  );
PS C:\> $definition = Get-AzManagedServicesDefinition
PS C:\> $definition.Properties.Authorization

PrincipalId                          RoleDefinitionId
-----------                          ----------------
714160ec-87d5-42bb-8b17-287c0dd7417d acdd72a7-3385-48ef-bd42-f606fba81ae7


PS C:\> $definition.Name
55a89269-0347-4a9c-a778-c3f37b9f8672
PS C:\> $definition = New-AzManagedServicesDefinition -DisplayName "MyTestDefinition" -ManagedByTenantId 72f9acbf-86f1-41af-91ab-2d7ef011db47 -Authorization $auths -Name 55a89269-0347-4a9c-a778-c3f37b9f8672
PS C:\> $definition.Properties.Authorization

PrincipalId                          RoleDefinitionId
-----------                          ----------------
714160ec-87d5-42bb-8b17-287c0dd7417d acdd72a7-3385-48ef-bd42-f606fba81ae7
714160ec-87d5-42bb-8b17-287c0dd7417d 9980e02c-c2be-4d73-94e8-173b1dc7cf3c

PS C:\>
```

Atualiza uma definição de registro com detalhes de autorização e o nome da definição de registro.

## OS

### -Authorization
Lista de mapeamento de autorização com entidade de segurança-roleDefinitionId.

```yaml
Type: Microsoft.Azure.Management.ManagedServices.Models.Authorization[]
Parameter Sets: ByPlan, ByAuthorization
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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

### -Descrição
A descrição da definição de registro.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisplayName
O nome de exibição da definição de registro.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManagedByTenantId
O identificador de locatário ManagedBy.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
O nome exclusivo da definição de registro.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PlanName
O nome do plano.

```yaml
Type: System.String
Parameter Sets: ByPlan
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PlanProduct
O nome do produto.

```yaml
Type: System.String
Parameter Sets: ByPlan
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PlanPublisher
O nome do fornecedor.

```yaml
Type: System.String
Parameter Sets: ByPlan
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PlanVersion
O número da versão do plano.

```yaml
Type: System.String
Parameter Sets: ByPlan
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Entidade de segurança
O identificador principal do ManagedBy.

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RoleDefinitionId
O identificador de definição de função para conceder permissões ao identificador principal.

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AsJob
Executar o cmdlet em segundo plano

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

### -Confirme
Solicita confirmação antes de executar o cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## SENSORES

### Nenhuma
## EXIBE

### Microsoft. Azure. PowerShell. cmdlets. Managedservices. Models. PSRegistrationDefinition
## INFORMA

## LINKS RELACIONADOS
