---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 5C1C51FE-747F-4176-84ED-A28AA3475581
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsDataSource.md
ms.openlocfilehash: d8ec5eed1b6c955720822e28bf54da68e9aefcac
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772875"
---
# <span data-ttu-id="8011f-101">Remove-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="8011f-101">Remove-AzOperationalInsightsDataSource</span></span>

## <span data-ttu-id="8011f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8011f-102">SYNOPSIS</span></span>
<span data-ttu-id="8011f-103">Exclui uma fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="8011f-103">Deletes a data source.</span></span>

## <span data-ttu-id="8011f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8011f-104">SYNTAX</span></span>

### <span data-ttu-id="8011f-105">ByWorkspaceName (padrão)</span><span class="sxs-lookup"><span data-stu-id="8011f-105">ByWorkspaceName (Default)</span></span>
```
Remove-AzOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String> [-Name] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8011f-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="8011f-106">ByWorkspaceObject</span></span>
```
Remove-AzOperationalInsightsDataSource [-Workspace] <PSWorkspace> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8011f-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8011f-107">DESCRIPTION</span></span>
<span data-ttu-id="8011f-108">O cmdlet **Remove-AzOperationalInsightsDataSource** exclui uma fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="8011f-108">The **Remove-AzOperationalInsightsDataSource** cmdlet deletes a data source.</span></span>

## <span data-ttu-id="8011f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8011f-109">EXAMPLES</span></span>

## <span data-ttu-id="8011f-110">OS</span><span class="sxs-lookup"><span data-stu-id="8011f-110">PARAMETERS</span></span>

### <span data-ttu-id="8011f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8011f-111">-DefaultProfile</span></span>
<span data-ttu-id="8011f-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="8011f-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8011f-113">-Force</span><span class="sxs-lookup"><span data-stu-id="8011f-113">-Force</span></span>
<span data-ttu-id="8011f-114">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="8011f-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8011f-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="8011f-115">-Name</span></span>
<span data-ttu-id="8011f-116">Especifica o nome de uma fonte de dados a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="8011f-116">Specifies the name of a data source to delete.</span></span>

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

### <span data-ttu-id="8011f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8011f-117">-ResourceGroupName</span></span>
<span data-ttu-id="8011f-118">Especifica o nome de um grupo de recursos que contém computadores.</span><span class="sxs-lookup"><span data-stu-id="8011f-118">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="8011f-119">-Espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="8011f-119">-Workspace</span></span>
<span data-ttu-id="8011f-120">Especifica um espaço de trabalho no qual esse cmdlet Opera.</span><span class="sxs-lookup"><span data-stu-id="8011f-120">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="8011f-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8011f-121">-WorkspaceName</span></span>
<span data-ttu-id="8011f-122">Especifica o nome de um espaço de trabalho no qual esse cmdlet Opera.</span><span class="sxs-lookup"><span data-stu-id="8011f-122">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="8011f-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8011f-123">-Confirm</span></span>
<span data-ttu-id="8011f-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8011f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8011f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8011f-125">-WhatIf</span></span>
<span data-ttu-id="8011f-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8011f-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8011f-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8011f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8011f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8011f-128">CommonParameters</span></span>
<span data-ttu-id="8011f-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8011f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8011f-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8011f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8011f-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8011f-131">INPUTS</span></span>

### <span data-ttu-id="8011f-132">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="8011f-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="8011f-133">System. String</span><span class="sxs-lookup"><span data-stu-id="8011f-133">System.String</span></span>

## <span data-ttu-id="8011f-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8011f-134">OUTPUTS</span></span>

### <span data-ttu-id="8011f-135">System. void</span><span class="sxs-lookup"><span data-stu-id="8011f-135">System.Void</span></span>

## <span data-ttu-id="8011f-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8011f-136">NOTES</span></span>
* <span data-ttu-id="8011f-137">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Operational, insights</span><span class="sxs-lookup"><span data-stu-id="8011f-137">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="8011f-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8011f-138">RELATED LINKS</span></span>

[<span data-ttu-id="8011f-139">Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="8011f-139">Get-AzOperationalInsightsDataSource</span></span>](./Get-AzOperationalInsightsDataSource.md)

[<span data-ttu-id="8011f-140">Set-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="8011f-140">Set-AzOperationalInsightsDataSource</span></span>](./Set-AzOperationalInsightsDataSource.md)


