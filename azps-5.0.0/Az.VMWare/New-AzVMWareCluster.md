---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/new-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWareCluster.md
ms.openlocfilehash: f2ed1813859f92624696eef7fa4f881f3eba1628
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281794"
---
# <span data-ttu-id="c5bd7-101">New-AzVMWareCluster</span><span class="sxs-lookup"><span data-stu-id="c5bd7-101">New-AzVMWareCluster</span></span>

## <span data-ttu-id="c5bd7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c5bd7-102">SYNOPSIS</span></span>
<span data-ttu-id="c5bd7-103">Criar ou atualizar um cluster em uma nuvem privada</span><span class="sxs-lookup"><span data-stu-id="c5bd7-103">Create or update a cluster in a private cloud</span></span>

## <span data-ttu-id="c5bd7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c5bd7-104">SYNTAX</span></span>

```
New-AzVMWareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String> -ClusterSize <Int32>
 -SkuName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c5bd7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c5bd7-105">DESCRIPTION</span></span>
<span data-ttu-id="c5bd7-106">Criar ou atualizar um cluster em uma nuvem privada</span><span class="sxs-lookup"><span data-stu-id="c5bd7-106">Create or update a cluster in a private cloud</span></span>

## <span data-ttu-id="c5bd7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c5bd7-107">EXAMPLES</span></span>

### <span data-ttu-id="c5bd7-108">Exemplo 1: criar cluster</span><span class="sxs-lookup"><span data-stu-id="c5bd7-108">Example 1: Create cluster</span></span>
```powershell
PS C:\> New-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group -ClusterSize 3 -SkuName av36

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="c5bd7-109">Criar cluster</span><span class="sxs-lookup"><span data-stu-id="c5bd7-109">Create cluster</span></span>

## <span data-ttu-id="c5bd7-110">OS</span><span class="sxs-lookup"><span data-stu-id="c5bd7-110">PARAMETERS</span></span>

### <span data-ttu-id="c5bd7-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c5bd7-111">-AsJob</span></span>
<span data-ttu-id="c5bd7-112">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="c5bd7-112">Run the command as a job</span></span>

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

### <span data-ttu-id="c5bd7-113">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="c5bd7-113">-ClusterSize</span></span>
<span data-ttu-id="c5bd7-114">O tamanho do cluster</span><span class="sxs-lookup"><span data-stu-id="c5bd7-114">The cluster size</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5bd7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5bd7-115">-DefaultProfile</span></span>
<span data-ttu-id="c5bd7-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c5bd7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5bd7-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="c5bd7-117">-Name</span></span>
<span data-ttu-id="c5bd7-118">Nome do cluster na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="c5bd7-118">Name of the cluster in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5bd7-119">-Nowait</span><span class="sxs-lookup"><span data-stu-id="c5bd7-119">-NoWait</span></span>
<span data-ttu-id="c5bd7-120">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="c5bd7-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c5bd7-121">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="c5bd7-121">-PrivateCloudName</span></span>
<span data-ttu-id="c5bd7-122">O nome da nuvem privada.</span><span class="sxs-lookup"><span data-stu-id="c5bd7-122">The name of the private cloud.</span></span>

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

### <span data-ttu-id="c5bd7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5bd7-123">-ResourceGroupName</span></span>
<span data-ttu-id="c5bd7-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c5bd7-124">The name of the resource group.</span></span>
<span data-ttu-id="c5bd7-125">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="c5bd7-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="c5bd7-126">-SkuName</span><span class="sxs-lookup"><span data-stu-id="c5bd7-126">-SkuName</span></span>
<span data-ttu-id="c5bd7-127">O nome da SKU.</span><span class="sxs-lookup"><span data-stu-id="c5bd7-127">The name of the SKU.</span></span>

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

### <span data-ttu-id="c5bd7-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c5bd7-128">-SubscriptionId</span></span>
<span data-ttu-id="c5bd7-129">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="c5bd7-129">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5bd7-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c5bd7-130">-Confirm</span></span>
<span data-ttu-id="c5bd7-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5bd7-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5bd7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5bd7-132">-WhatIf</span></span>
<span data-ttu-id="c5bd7-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c5bd7-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5bd7-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c5bd7-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5bd7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5bd7-135">CommonParameters</span></span>
<span data-ttu-id="c5bd7-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5bd7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5bd7-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c5bd7-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5bd7-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c5bd7-138">INPUTS</span></span>

## <span data-ttu-id="c5bd7-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c5bd7-139">OUTPUTS</span></span>

### <span data-ttu-id="c5bd7-140">Microsoft. Azure. PowerShell. cmdlets. VMWare. Models. Api20200320. ICluster</span><span class="sxs-lookup"><span data-stu-id="c5bd7-140">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="c5bd7-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c5bd7-141">NOTES</span></span>

<span data-ttu-id="c5bd7-142">ALIASES</span><span class="sxs-lookup"><span data-stu-id="c5bd7-142">ALIASES</span></span>

## <span data-ttu-id="c5bd7-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c5bd7-143">RELATED LINKS</span></span>

