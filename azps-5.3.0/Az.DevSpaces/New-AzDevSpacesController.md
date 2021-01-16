---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/new-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/New-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/New-AzDevSpacesController.md
ms.openlocfilehash: a99a26060492efbe40bc4a16633ca6a207e093b4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428392"
---
# <span data-ttu-id="917f4-101">New-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="917f4-101">New-AzDevSpacesController</span></span>

## <span data-ttu-id="917f4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="917f4-102">SYNOPSIS</span></span>
<span data-ttu-id="917f4-103">Crie um novo controlador de DevSpaces do Azure.</span><span class="sxs-lookup"><span data-stu-id="917f4-103">Create a new Azure DevSpaces controller.</span></span>

## <span data-ttu-id="917f4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="917f4-104">SYNTAX</span></span>

```
New-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-TargetResourceGroupName] <String>
 [-TargetClusterName] <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="917f4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="917f4-105">DESCRIPTION</span></span>
<span data-ttu-id="917f4-106">Crie um novo controlador de DevSpaces do Azure.</span><span class="sxs-lookup"><span data-stu-id="917f4-106">Create a new Azure DevSpaces controller.</span></span>

## <span data-ttu-id="917f4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="917f4-107">EXAMPLES</span></span>

### <span data-ttu-id="917f4-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="917f4-108">Example 1</span></span>
```powershell
PS C:\> New-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName -TargetResourceGroupName clusterResourceGroup -TargetClusterName clusterName

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="917f4-109">Crie um controlador DevSpaces em devSpaceResourceGroup de domínio com um nome devSpaceName.</span><span class="sxs-lookup"><span data-stu-id="917f4-109">Create a DevSpaces controller in resourcegroup devSpaceResourceGroup with a name devSpaceName.</span></span> <span data-ttu-id="917f4-110">Use ClusterName cluster como destino para esse controlador.</span><span class="sxs-lookup"><span data-stu-id="917f4-110">Use clusterName cluster as a target for this controller.</span></span>

## <span data-ttu-id="917f4-111">OS</span><span class="sxs-lookup"><span data-stu-id="917f4-111">PARAMETERS</span></span>

### <span data-ttu-id="917f4-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="917f4-112">-AsJob</span></span>
<span data-ttu-id="917f4-113">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="917f4-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="917f4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="917f4-114">-DefaultProfile</span></span>
<span data-ttu-id="917f4-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="917f4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="917f4-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="917f4-116">-Name</span></span>
<span data-ttu-id="917f4-117">Nome do controlador DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="917f4-117">DevSpaces Controller Name.</span></span>

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

### <span data-ttu-id="917f4-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="917f4-118">-ResourceGroupName</span></span>
<span data-ttu-id="917f4-119">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="917f4-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="917f4-120">-Marca</span><span class="sxs-lookup"><span data-stu-id="917f4-120">-Tag</span></span>
<span data-ttu-id="917f4-121">Uma tabela de hash que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="917f4-121">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="917f4-122">-TargetClusterName</span><span class="sxs-lookup"><span data-stu-id="917f4-122">-TargetClusterName</span></span>
<span data-ttu-id="917f4-123">Nome do cluster de destino.</span><span class="sxs-lookup"><span data-stu-id="917f4-123">Target Cluster Name.</span></span>

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

### <span data-ttu-id="917f4-124">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="917f4-124">-TargetResourceGroupName</span></span>
<span data-ttu-id="917f4-125">Nome do grupo de recursos de destino.</span><span class="sxs-lookup"><span data-stu-id="917f4-125">Target Resource Group Name.</span></span>

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

### <span data-ttu-id="917f4-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="917f4-126">-Confirm</span></span>
<span data-ttu-id="917f4-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="917f4-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="917f4-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="917f4-128">-WhatIf</span></span>
<span data-ttu-id="917f4-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="917f4-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="917f4-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="917f4-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="917f4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="917f4-131">CommonParameters</span></span>
<span data-ttu-id="917f4-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="917f4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="917f4-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="917f4-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="917f4-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="917f4-134">INPUTS</span></span>

### <span data-ttu-id="917f4-135">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="917f4-135">None</span></span>

## <span data-ttu-id="917f4-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="917f4-136">OUTPUTS</span></span>

### <span data-ttu-id="917f4-137">Microsoft. Azure. Commands. DevSpaces. Models. PSController</span><span class="sxs-lookup"><span data-stu-id="917f4-137">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="917f4-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="917f4-138">NOTES</span></span>

## <span data-ttu-id="917f4-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="917f4-139">RELATED LINKS</span></span>
