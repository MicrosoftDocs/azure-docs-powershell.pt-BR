---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 5C1C51FE-747F-4176-84ED-A28AA3475581
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/remove-azurermoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsDataSource.md
ms.openlocfilehash: e9d5a7443c8a758cdc839826025d51fe57d55420
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431306"
---
# <span data-ttu-id="4f8db-101">Remove-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="4f8db-101">Remove-AzureRmOperationalInsightsDataSource</span></span>

## <span data-ttu-id="4f8db-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4f8db-102">SYNOPSIS</span></span>
<span data-ttu-id="4f8db-103">Exclui uma fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="4f8db-103">Deletes a data source.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4f8db-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4f8db-104">SYNTAX</span></span>

### <span data-ttu-id="4f8db-105">ByWorkspaceName (padrão)</span><span class="sxs-lookup"><span data-stu-id="4f8db-105">ByWorkspaceName (Default)</span></span>
```
Remove-AzureRmOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f8db-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="4f8db-106">ByWorkspaceObject</span></span>
```
Remove-AzureRmOperationalInsightsDataSource [-Workspace] <PSWorkspace> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f8db-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4f8db-107">DESCRIPTION</span></span>
<span data-ttu-id="4f8db-108">O cmdlet **Remove-AzureRmOperationalInsightsDataSource** exclui uma fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="4f8db-108">The **Remove-AzureRmOperationalInsightsDataSource** cmdlet deletes a data source.</span></span>

## <span data-ttu-id="4f8db-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4f8db-109">EXAMPLES</span></span>

## <span data-ttu-id="4f8db-110">OS</span><span class="sxs-lookup"><span data-stu-id="4f8db-110">PARAMETERS</span></span>

### <span data-ttu-id="4f8db-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f8db-111">-DefaultProfile</span></span>
<span data-ttu-id="4f8db-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="4f8db-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4f8db-113">-Force</span><span class="sxs-lookup"><span data-stu-id="4f8db-113">-Force</span></span>
<span data-ttu-id="4f8db-114">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="4f8db-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4f8db-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="4f8db-115">-Name</span></span>
<span data-ttu-id="4f8db-116">Especifica o nome de uma fonte de dados a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="4f8db-116">Specifies the name of a data source to delete.</span></span>

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

### <span data-ttu-id="4f8db-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f8db-117">-ResourceGroupName</span></span>
<span data-ttu-id="4f8db-118">Especifica o nome de um grupo de recursos que contém computadores.</span><span class="sxs-lookup"><span data-stu-id="4f8db-118">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="4f8db-119">-Espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="4f8db-119">-Workspace</span></span>
<span data-ttu-id="4f8db-120">Especifica um espaço de trabalho no qual esse cmdlet Opera.</span><span class="sxs-lookup"><span data-stu-id="4f8db-120">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="4f8db-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4f8db-121">-WorkspaceName</span></span>
<span data-ttu-id="4f8db-122">Especifica o nome de um espaço de trabalho no qual esse cmdlet Opera.</span><span class="sxs-lookup"><span data-stu-id="4f8db-122">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="4f8db-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4f8db-123">-Confirm</span></span>
<span data-ttu-id="4f8db-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f8db-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f8db-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f8db-125">-WhatIf</span></span>
<span data-ttu-id="4f8db-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4f8db-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f8db-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4f8db-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f8db-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f8db-128">CommonParameters</span></span>
<span data-ttu-id="4f8db-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f8db-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f8db-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f8db-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f8db-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4f8db-131">INPUTS</span></span>

### <span data-ttu-id="4f8db-132">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="4f8db-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="4f8db-133">Parâmetros: espaço de trabalho (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4f8db-133">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="4f8db-134">System. String</span><span class="sxs-lookup"><span data-stu-id="4f8db-134">System.String</span></span>

## <span data-ttu-id="4f8db-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4f8db-135">OUTPUTS</span></span>

### <span data-ttu-id="4f8db-136">System. void</span><span class="sxs-lookup"><span data-stu-id="4f8db-136">System.Void</span></span>

## <span data-ttu-id="4f8db-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4f8db-137">NOTES</span></span>
* <span data-ttu-id="4f8db-138">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Operational, insights</span><span class="sxs-lookup"><span data-stu-id="4f8db-138">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="4f8db-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4f8db-139">RELATED LINKS</span></span>

[<span data-ttu-id="4f8db-140">Get-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="4f8db-140">Get-AzureRmOperationalInsightsDataSource</span></span>](./Get-AzureRmOperationalInsightsDataSource.md)

[<span data-ttu-id="4f8db-141">Set-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="4f8db-141">Set-AzureRmOperationalInsightsDataSource</span></span>](./Set-AzureRmOperationalInsightsDataSource.md)

