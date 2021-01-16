---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplication.md
ms.openlocfilehash: 67a49250607e1c7d70f1799aa26bd866924b5edc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428423"
---
# Get-AzWvdApplication

## Sinopse
Obter um aplicativo.

## SYNTAX

### Lista (padrão)
```
Get-AzWvdApplication -GroupName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### Obter
```
Get-AzWvdApplication -GroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzWvdApplication -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## DESCRITIVO
Obter um aplicativo.

## EXEMPLOS

### Exemplo 1: obter um aplicativo de área de trabalho virtual do Windows por nome
```powershell
PS C:\> Get-AzWvdApplication -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName -Name ApplicationName

Name                                 Type
----                                 ----
ApplicationGroupName/ApplicationName Microsoft.DesktopVirtualization/applicationgroups/applications
```

Esse comando obtém um aplicativo de área de trabalho virtual do Windows em um grupo applicaton.

### Exemplo 2: listar aplicativos da área de trabalho virtual do Windows
```powershell
PS C:\> Get-AzWvdApplication -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName

Name                                 Type
----                                 ----
ApplicationGroupName/ApplicationName1 Microsoft.DesktopVirtualization/applicationgroups/applications
ApplicationGroupName/ApplicationName2 Microsoft.DesktopVirtualization/applicationgroups/applications
```

Esse comando lista os aplicativos da área de trabalho virtual do Windows em um grupo do applicaton.

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome_do_grupo
O nome do grupo de aplicativos

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Nome
O nome do aplicativo dentro do grupo de aplicativos especificado

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ApplicationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
O nome do grupo de recursos.
O nome não diferencia maiúsculas de minúsculas.

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
A ID da assinatura de destino.

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## SENSORES

### Microsoft. Azure. PowerShell. cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity

## EXIBE

### Microsoft. Azure. PowerShell. cmdlets. DesktopVirtualization. Models. Api20201102Preview. IApplication

## INFORMA

ALIASES

PROPRIEDADES DE PARÂMETROS COMPLEXAS

Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas. Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.


INPUTobject <IDesktopVirtualizationIdentity> : parâmetro de identidade
  - `[ApplicationGroupName <String>]`: O nome do grupo de aplicativos
  - `[ApplicationName <String>]`: O nome do aplicativo dentro do grupo de aplicativos especificado
  - `[DesktopName <String>]`: O nome da área de trabalho dentro do grupo da área de trabalho especificado
  - `[HostPoolName <String>]`: O nome do pool de hosts dentro do grupo de recursos especificado
  - `[Id <String>]`: Caminho de identidade do recurso
  - `[MsixPackageFullName <String>]`: O nome completo do pacote de versão específica do pacote MSIX dentro do hostpool especificado
  - `[ResourceGroupName <String>]`: O nome do grupo de recursos. O nome não diferencia maiúsculas de minúsculas.
  - `[SessionHostName <String>]`: O nome do host da sessão dentro do pool de hosts especificado
  - `[SubscriptionId <String>]`: A ID da assinatura de destino.
  - `[UserSessionId <String>]`: O nome da sessão do usuário no host de sessão especificado
  - `[WorkspaceName <String>]`: O nome do espaço de trabalho

## LINKS RELACIONADOS

