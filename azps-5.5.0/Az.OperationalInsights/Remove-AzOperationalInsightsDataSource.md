---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 5C1C51FE-747F-4176-84ED-A28AA3475581
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsDataSource.md
ms.openlocfilehash: bba48b31158226d1ea63f70ceafe3355990fea6e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113396"
---
# <span data-ttu-id="5a0a1-101">Remove-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="5a0a1-101">Remove-AzOperationalInsightsDataSource</span></span>

## <span data-ttu-id="5a0a1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5a0a1-102">SYNOPSIS</span></span>
<span data-ttu-id="5a0a1-103">Exclui uma fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="5a0a1-103">Deletes a data source.</span></span>

## <span data-ttu-id="5a0a1-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5a0a1-104">SYNTAX</span></span>

### <span data-ttu-id="5a0a1-105">ByWorkspaceName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="5a0a1-105">ByWorkspaceName (Default)</span></span>
```
Remove-AzOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String> [-Name] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a0a1-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="5a0a1-106">ByWorkspaceObject</span></span>
```
Remove-AzOperationalInsightsDataSource [-Workspace] <PSWorkspace> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a0a1-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="5a0a1-107">DESCRIPTION</span></span>
<span data-ttu-id="5a0a1-108">O cmdlet **Remove-AzOperationalInsightsDataSource** exclui uma fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="5a0a1-108">The **Remove-AzOperationalInsightsDataSource** cmdlet deletes a data source.</span></span>

## <span data-ttu-id="5a0a1-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5a0a1-109">EXAMPLES</span></span>

## <span data-ttu-id="5a0a1-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5a0a1-110">PARAMETERS</span></span>

### <span data-ttu-id="5a0a1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a0a1-111">-DefaultProfile</span></span>
<span data-ttu-id="5a0a1-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="5a0a1-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5a0a1-113">-Forçar</span><span class="sxs-lookup"><span data-stu-id="5a0a1-113">-Force</span></span>
<span data-ttu-id="5a0a1-114">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="5a0a1-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5a0a1-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="5a0a1-115">-Name</span></span>
<span data-ttu-id="5a0a1-116">Especifica o nome de uma fonte de dados a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="5a0a1-116">Specifies the name of a data source to delete.</span></span>

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

### <span data-ttu-id="5a0a1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a0a1-117">-ResourceGroupName</span></span>
<span data-ttu-id="5a0a1-118">Especifica o nome de um grupo de recursos que contém computadores.</span><span class="sxs-lookup"><span data-stu-id="5a0a1-118">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="5a0a1-119">-Espaço de Trabalho</span><span class="sxs-lookup"><span data-stu-id="5a0a1-119">-Workspace</span></span>
<span data-ttu-id="5a0a1-120">Especifica um espaço de trabalho no qual este cmdlet opera.</span><span class="sxs-lookup"><span data-stu-id="5a0a1-120">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="5a0a1-121">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="5a0a1-121">-WorkspaceName</span></span>
<span data-ttu-id="5a0a1-122">Especifica o nome de um espaço de trabalho no qual este cmdlet opera.</span><span class="sxs-lookup"><span data-stu-id="5a0a1-122">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="5a0a1-123">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="5a0a1-123">-Confirm</span></span>
<span data-ttu-id="5a0a1-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a0a1-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a0a1-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a0a1-125">-WhatIf</span></span>
<span data-ttu-id="5a0a1-126">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="5a0a1-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a0a1-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5a0a1-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a0a1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a0a1-128">CommonParameters</span></span>
<span data-ttu-id="5a0a1-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a0a1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a0a1-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a0a1-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a0a1-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="5a0a1-131">INPUTS</span></span>

### <span data-ttu-id="5a0a1-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="5a0a1-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="5a0a1-133">System.String</span><span class="sxs-lookup"><span data-stu-id="5a0a1-133">System.String</span></span>

## <span data-ttu-id="5a0a1-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="5a0a1-134">OUTPUTS</span></span>

### <span data-ttu-id="5a0a1-135">System.Void</span><span class="sxs-lookup"><span data-stu-id="5a0a1-135">System.Void</span></span>

## <span data-ttu-id="5a0a1-136">Notas</span><span class="sxs-lookup"><span data-stu-id="5a0a1-136">NOTES</span></span>
* <span data-ttu-id="5a0a1-137">Palavras-chave: azure, azurerm, arm, resource, management, manager, operational, insights</span><span class="sxs-lookup"><span data-stu-id="5a0a1-137">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="5a0a1-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5a0a1-138">RELATED LINKS</span></span>

[<span data-ttu-id="5a0a1-139">Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="5a0a1-139">Get-AzOperationalInsightsDataSource</span></span>](./Get-AzOperationalInsightsDataSource.md)

[<span data-ttu-id="5a0a1-140">Set-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="5a0a1-140">Set-AzOperationalInsightsDataSource</span></span>](./Set-AzOperationalInsightsDataSource.md)


