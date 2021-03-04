---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 6A08AF7C-1E18-40A1-B21E-12F94823D304
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/new-azoperationalinsightscustomlogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCustomLogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCustomLogDataSource.md
ms.openlocfilehash: e923d413b889583578efb0ac81f9eb6aeadf72fa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888612"
---
# <span data-ttu-id="73fda-101">New-AzOperationalInsightsCustomLogDataSource</span><span class="sxs-lookup"><span data-stu-id="73fda-101">New-AzOperationalInsightsCustomLogDataSource</span></span>

## <span data-ttu-id="73fda-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73fda-102">SYNOPSIS</span></span>
<span data-ttu-id="73fda-103">Define uma política de coleção de log personalizada.</span><span class="sxs-lookup"><span data-stu-id="73fda-103">Defines a custom log collection policy.</span></span>

## <span data-ttu-id="73fda-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="73fda-104">SYNTAX</span></span>

### <span data-ttu-id="73fda-105">ByWorkspaceName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="73fda-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsCustomLogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-CustomLogRawJson] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73fda-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="73fda-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsCustomLogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-CustomLogRawJson] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="73fda-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="73fda-107">DESCRIPTION</span></span>
<span data-ttu-id="73fda-108">O cmdlet **New-AzOperationalInsightsCustomLogDataSource** define uma política de coleção de log personalizada.</span><span class="sxs-lookup"><span data-stu-id="73fda-108">The **New-AzOperationalInsightsCustomLogDataSource** cmdlet defines a custom log collection policy.</span></span>

## <span data-ttu-id="73fda-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="73fda-109">EXAMPLES</span></span>

## <span data-ttu-id="73fda-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="73fda-110">PARAMETERS</span></span>

### <span data-ttu-id="73fda-111">-CustomLogRawJson</span><span class="sxs-lookup"><span data-stu-id="73fda-111">-CustomLogRawJson</span></span>
<span data-ttu-id="73fda-112">Especifica a política de coleção personalizada como uma cadeia de caracteres JSON (Notação de Objeto JavaScript) bruta.</span><span class="sxs-lookup"><span data-stu-id="73fda-112">Specifies the custom collection policy as a raw JavaScript Object Notation (JSON) string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73fda-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73fda-113">-DefaultProfile</span></span>
<span data-ttu-id="73fda-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="73fda-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="73fda-115">-Force</span><span class="sxs-lookup"><span data-stu-id="73fda-115">-Force</span></span>
<span data-ttu-id="73fda-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="73fda-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="73fda-117">-Name</span><span class="sxs-lookup"><span data-stu-id="73fda-117">-Name</span></span>
<span data-ttu-id="73fda-118">Especifica um nome para a fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="73fda-118">Specifies a name for the data source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73fda-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73fda-119">-ResourceGroupName</span></span>
<span data-ttu-id="73fda-120">Especifica o nome de um grupo de recursos que contém computadores.</span><span class="sxs-lookup"><span data-stu-id="73fda-120">Specifies the name of a resource group that contains computers.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73fda-121">-Workspace</span><span class="sxs-lookup"><span data-stu-id="73fda-121">-Workspace</span></span>
<span data-ttu-id="73fda-122">Especifica um espaço de trabalho no qual este cmdlet opera.</span><span class="sxs-lookup"><span data-stu-id="73fda-122">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73fda-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="73fda-123">-WorkspaceName</span></span>
<span data-ttu-id="73fda-124">Especifica o nome de um espaço de trabalho no qual este cmdlet opera.</span><span class="sxs-lookup"><span data-stu-id="73fda-124">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73fda-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="73fda-125">-Confirm</span></span>
<span data-ttu-id="73fda-126">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73fda-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73fda-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73fda-127">-WhatIf</span></span>
<span data-ttu-id="73fda-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="73fda-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73fda-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="73fda-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73fda-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73fda-130">CommonParameters</span></span>
<span data-ttu-id="73fda-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73fda-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73fda-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73fda-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73fda-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="73fda-133">INPUTS</span></span>

### <span data-ttu-id="73fda-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="73fda-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="73fda-135">System.String</span><span class="sxs-lookup"><span data-stu-id="73fda-135">System.String</span></span>

## <span data-ttu-id="73fda-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="73fda-136">OUTPUTS</span></span>

### <span data-ttu-id="73fda-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="73fda-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="73fda-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="73fda-138">NOTES</span></span>

## <span data-ttu-id="73fda-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="73fda-139">RELATED LINKS</span></span>

[<span data-ttu-id="73fda-140">Disable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="73fda-140">Disable-AzOperationalInsightsLinuxCustomLogCollection</span></span>](./Disable-AzOperationalInsightsLinuxCustomLogCollection.md)

[<span data-ttu-id="73fda-141">Enable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="73fda-141">Enable-AzOperationalInsightsLinuxCustomLogCollection</span></span>](./Enable-AzOperationalInsightsLinuxCustomLogCollection.md)


