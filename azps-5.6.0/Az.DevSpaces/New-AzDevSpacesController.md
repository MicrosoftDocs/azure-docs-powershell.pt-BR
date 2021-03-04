---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/powershell/module/az.devspaces/new-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/New-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/New-AzDevSpacesController.md
ms.openlocfilehash: 097248e06acd081582ecc34a863658b2b073ef60
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892178"
---
# <span data-ttu-id="e5103-101">New-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="e5103-101">New-AzDevSpacesController</span></span>

## <span data-ttu-id="e5103-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5103-102">SYNOPSIS</span></span>
<span data-ttu-id="e5103-103">Crie um novo controlador do Azure DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="e5103-103">Create a new Azure DevSpaces controller.</span></span>

## <span data-ttu-id="e5103-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e5103-104">SYNTAX</span></span>

```
New-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-TargetResourceGroupName] <String>
 [-TargetClusterName] <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5103-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e5103-105">DESCRIPTION</span></span>
<span data-ttu-id="e5103-106">Crie um novo controlador do Azure DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="e5103-106">Create a new Azure DevSpaces controller.</span></span>

## <span data-ttu-id="e5103-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e5103-107">EXAMPLES</span></span>

### <span data-ttu-id="e5103-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e5103-108">Example 1</span></span>
```powershell
PS C:\> New-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName -TargetResourceGroupName clusterResourceGroup -TargetClusterName clusterName

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="e5103-109">Crie um controlador DevSpaces no devSpaceResourceGroup de grupo de recursos com um nome devSpaceName.</span><span class="sxs-lookup"><span data-stu-id="e5103-109">Create a DevSpaces controller in resourcegroup devSpaceResourceGroup with a name devSpaceName.</span></span> <span data-ttu-id="e5103-110">Use clusterName cluster como um destino para esse controlador.</span><span class="sxs-lookup"><span data-stu-id="e5103-110">Use clusterName cluster as a target for this controller.</span></span>

## <span data-ttu-id="e5103-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e5103-111">PARAMETERS</span></span>

### <span data-ttu-id="e5103-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e5103-112">-AsJob</span></span>
<span data-ttu-id="e5103-113">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="e5103-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e5103-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5103-114">-DefaultProfile</span></span>
<span data-ttu-id="e5103-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e5103-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5103-116">-Name</span><span class="sxs-lookup"><span data-stu-id="e5103-116">-Name</span></span>
<span data-ttu-id="e5103-117">Nome do controlador de DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="e5103-117">DevSpaces Controller Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5103-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5103-118">-ResourceGroupName</span></span>
<span data-ttu-id="e5103-119">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="e5103-119">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5103-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="e5103-120">-Tag</span></span>
<span data-ttu-id="e5103-121">Uma tabela de hash que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="e5103-121">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5103-122">-TargetClusterName</span><span class="sxs-lookup"><span data-stu-id="e5103-122">-TargetClusterName</span></span>
<span data-ttu-id="e5103-123">Nome do cluster de destino.</span><span class="sxs-lookup"><span data-stu-id="e5103-123">Target Cluster Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5103-124">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5103-124">-TargetResourceGroupName</span></span>
<span data-ttu-id="e5103-125">Nome do grupo de recursos de destino.</span><span class="sxs-lookup"><span data-stu-id="e5103-125">Target Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5103-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e5103-126">-Confirm</span></span>
<span data-ttu-id="e5103-127">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5103-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5103-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5103-128">-WhatIf</span></span>
<span data-ttu-id="e5103-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e5103-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5103-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e5103-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5103-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5103-131">CommonParameters</span></span>
<span data-ttu-id="e5103-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5103-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5103-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5103-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5103-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e5103-134">INPUTS</span></span>

### <span data-ttu-id="e5103-135">Nenhum</span><span class="sxs-lookup"><span data-stu-id="e5103-135">None</span></span>

## <span data-ttu-id="e5103-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e5103-136">OUTPUTS</span></span>

### <span data-ttu-id="e5103-137">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span><span class="sxs-lookup"><span data-stu-id="e5103-137">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="e5103-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="e5103-138">NOTES</span></span>

## <span data-ttu-id="e5103-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e5103-139">RELATED LINKS</span></span>
