---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/new-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/New-AzVMwareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/New-AzVMwareCluster.md
ms.openlocfilehash: d654b2fa012a793ce48dff2cc5bfb9ade4f99d34
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112353"
---
# <span data-ttu-id="5e621-101">New-AzVMwareCluster</span><span class="sxs-lookup"><span data-stu-id="5e621-101">New-AzVMwareCluster</span></span>

## <span data-ttu-id="5e621-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5e621-102">SYNOPSIS</span></span>
<span data-ttu-id="5e621-103">Criar ou atualizar um cluster em uma nuvem privada</span><span class="sxs-lookup"><span data-stu-id="5e621-103">Create or update a cluster in a private cloud</span></span>

## <span data-ttu-id="5e621-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5e621-104">SYNTAX</span></span>

```
New-AzVMwareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String> -SkuName <String>
 [-SubscriptionId <String>] [-ClusterSize <Int32>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5e621-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="5e621-105">DESCRIPTION</span></span>
<span data-ttu-id="5e621-106">Criar ou atualizar um cluster em uma nuvem privada</span><span class="sxs-lookup"><span data-stu-id="5e621-106">Create or update a cluster in a private cloud</span></span>

## <span data-ttu-id="5e621-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5e621-107">EXAMPLES</span></span>

### <span data-ttu-id="5e621-108">Exemplo 1: Criar cluster</span><span class="sxs-lookup"><span data-stu-id="5e621-108">Example 1: Create cluster</span></span>
```powershell
PS C:\> New-AzVMwareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group -ClusterSize 3 -SkuName av36

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="5e621-109">Criar cluster</span><span class="sxs-lookup"><span data-stu-id="5e621-109">Create cluster</span></span>

## <span data-ttu-id="5e621-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5e621-110">PARAMETERS</span></span>

### <span data-ttu-id="5e621-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5e621-111">-AsJob</span></span>
<span data-ttu-id="5e621-112">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="5e621-112">Run the command as a job</span></span>

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

### <span data-ttu-id="5e621-113">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="5e621-113">-ClusterSize</span></span>
<span data-ttu-id="5e621-114">O tamanho do cluster</span><span class="sxs-lookup"><span data-stu-id="5e621-114">The cluster size</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e621-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e621-115">-DefaultProfile</span></span>
<span data-ttu-id="5e621-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5e621-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e621-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="5e621-117">-Name</span></span>
<span data-ttu-id="5e621-118">Nome do cluster na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="5e621-118">Name of the cluster in the private cloud</span></span>

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

### <span data-ttu-id="5e621-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="5e621-119">-NoWait</span></span>
<span data-ttu-id="5e621-120">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="5e621-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5e621-121">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="5e621-121">-PrivateCloudName</span></span>
<span data-ttu-id="5e621-122">O nome da nuvem privada.</span><span class="sxs-lookup"><span data-stu-id="5e621-122">The name of the private cloud.</span></span>

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

### <span data-ttu-id="5e621-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e621-123">-ResourceGroupName</span></span>
<span data-ttu-id="5e621-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5e621-124">The name of the resource group.</span></span>
<span data-ttu-id="5e621-125">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="5e621-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="5e621-126">-SkuName</span><span class="sxs-lookup"><span data-stu-id="5e621-126">-SkuName</span></span>
<span data-ttu-id="5e621-127">O nome da SKU.</span><span class="sxs-lookup"><span data-stu-id="5e621-127">The name of the SKU.</span></span>

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

### <span data-ttu-id="5e621-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5e621-128">-SubscriptionId</span></span>
<span data-ttu-id="5e621-129">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="5e621-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="5e621-130">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="5e621-130">-Confirm</span></span>
<span data-ttu-id="5e621-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e621-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e621-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e621-132">-WhatIf</span></span>
<span data-ttu-id="5e621-133">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="5e621-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e621-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5e621-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e621-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e621-135">CommonParameters</span></span>
<span data-ttu-id="5e621-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e621-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e621-137">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5e621-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e621-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="5e621-138">INPUTS</span></span>

## <span data-ttu-id="5e621-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="5e621-139">OUTPUTS</span></span>

### <span data-ttu-id="5e621-140">Microsoft.Azure.PowerShell.Cmdlets.V Ltd.Models.Api20200320.ICluster</span><span class="sxs-lookup"><span data-stu-id="5e621-140">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="5e621-141">Notas</span><span class="sxs-lookup"><span data-stu-id="5e621-141">NOTES</span></span>

<span data-ttu-id="5e621-142">Aliases</span><span class="sxs-lookup"><span data-stu-id="5e621-142">ALIASES</span></span>

## <span data-ttu-id="5e621-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5e621-143">RELATED LINKS</span></span>

