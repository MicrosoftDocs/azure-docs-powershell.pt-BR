---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/new-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/New-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/New-AzDevSpacesController.md
ms.openlocfilehash: 5c4abfa199a8478c247b6c2b95fe0a3651faa4f1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600962"
---
# <span data-ttu-id="93e6d-101">New-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="93e6d-101">New-AzDevSpacesController</span></span>

## <span data-ttu-id="93e6d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="93e6d-102">SYNOPSIS</span></span>
<span data-ttu-id="93e6d-103">Crie um novo controlador de DevSpaces do Azure.</span><span class="sxs-lookup"><span data-stu-id="93e6d-103">Create a new Azure DevSpaces controller.</span></span>

## <span data-ttu-id="93e6d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="93e6d-104">SYNTAX</span></span>

```
New-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-TargetResourceGroupName] <String>
 [-TargetClusterName] <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93e6d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="93e6d-105">DESCRIPTION</span></span>
<span data-ttu-id="93e6d-106">Crie um novo controlador de DevSpaces do Azure.</span><span class="sxs-lookup"><span data-stu-id="93e6d-106">Create a new Azure DevSpaces controller.</span></span>

## <span data-ttu-id="93e6d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="93e6d-107">EXAMPLES</span></span>

### <span data-ttu-id="93e6d-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="93e6d-108">Example 1</span></span>
```powershell
PS C:\> New-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName -TargetResourceGroupName clusterResourceGroup -TargetClusterName clusterName

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="93e6d-109">Crreate, xxxx xxxx xxxx xxxx xxxx DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="93e6d-109">Crreate a DevSpaces controller in resourcegroup devSpaceResourceGroup with a name devSpaceName.</span></span> <span data-ttu-id="93e6d-110">Use ClusterName cluster como destino para esse controlador.</span><span class="sxs-lookup"><span data-stu-id="93e6d-110">Use clusterName cluster as a target for this controller.</span></span>

## <span data-ttu-id="93e6d-111">OS</span><span class="sxs-lookup"><span data-stu-id="93e6d-111">PARAMETERS</span></span>

### <span data-ttu-id="93e6d-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="93e6d-112">-AsJob</span></span>
<span data-ttu-id="93e6d-113">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="93e6d-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="93e6d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93e6d-114">-DefaultProfile</span></span>
<span data-ttu-id="93e6d-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="93e6d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93e6d-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="93e6d-116">-Name</span></span>
<span data-ttu-id="93e6d-117">Nome do controlador DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="93e6d-117">DevSpaces Controller Name.</span></span>

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

### <span data-ttu-id="93e6d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93e6d-118">-ResourceGroupName</span></span>
<span data-ttu-id="93e6d-119">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="93e6d-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="93e6d-120">-Marca</span><span class="sxs-lookup"><span data-stu-id="93e6d-120">-Tag</span></span>
<span data-ttu-id="93e6d-121">Uma tabela de hash que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="93e6d-121">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="93e6d-122">-TargetClusterName</span><span class="sxs-lookup"><span data-stu-id="93e6d-122">-TargetClusterName</span></span>
<span data-ttu-id="93e6d-123">Nome do cluster de destino.</span><span class="sxs-lookup"><span data-stu-id="93e6d-123">Target Cluster Name.</span></span>

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

### <span data-ttu-id="93e6d-124">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93e6d-124">-TargetResourceGroupName</span></span>
<span data-ttu-id="93e6d-125">Nome do grupo de recursos de destino.</span><span class="sxs-lookup"><span data-stu-id="93e6d-125">Target Resource Group Name.</span></span>

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

### <span data-ttu-id="93e6d-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="93e6d-126">-Confirm</span></span>
<span data-ttu-id="93e6d-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93e6d-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93e6d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93e6d-128">-WhatIf</span></span>
<span data-ttu-id="93e6d-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="93e6d-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93e6d-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="93e6d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93e6d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93e6d-131">CommonParameters</span></span>
<span data-ttu-id="93e6d-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93e6d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93e6d-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93e6d-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93e6d-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="93e6d-134">INPUTS</span></span>

### <span data-ttu-id="93e6d-135">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="93e6d-135">None</span></span>

## <span data-ttu-id="93e6d-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="93e6d-136">OUTPUTS</span></span>

### <span data-ttu-id="93e6d-137">Microsoft. Azure. Commands. DevSpaces. Models. PSController</span><span class="sxs-lookup"><span data-stu-id="93e6d-137">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="93e6d-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="93e6d-138">NOTES</span></span>

## <span data-ttu-id="93e6d-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="93e6d-139">RELATED LINKS</span></span>
