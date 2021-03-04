---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/remove-azservicefabricservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricService.md
ms.openlocfilehash: 992cd2a381e9eda89b9388ec1ed37f74a76e9adf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892329"
---
# <span data-ttu-id="bfb89-101">Remove-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="bfb89-101">Remove-AzServiceFabricService</span></span>

## <span data-ttu-id="bfb89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfb89-102">SYNOPSIS</span></span>
<span data-ttu-id="bfb89-103">Remova um serviço do cluster.</span><span class="sxs-lookup"><span data-stu-id="bfb89-103">Remove a service from the cluster.</span></span> <span data-ttu-id="bfb89-104">Só dá suporte ARM serviços implantados.</span><span class="sxs-lookup"><span data-stu-id="bfb89-104">Only supports ARM deployed services.</span></span>

## <span data-ttu-id="bfb89-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="bfb89-105">SYNTAX</span></span>

### <span data-ttu-id="bfb89-106">ByResourceGroup (Padrão)</span><span class="sxs-lookup"><span data-stu-id="bfb89-106">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bfb89-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="bfb89-107">ByResourceId</span></span>
```
Remove-AzServiceFabricService -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfb89-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="bfb89-108">ByInputObject</span></span>
```
Remove-AzServiceFabricService -InputObject <PSService> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bfb89-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="bfb89-109">DESCRIPTION</span></span>
<span data-ttu-id="bfb89-110">Este cmdlet remove um formulário de serviço do cluster.</span><span class="sxs-lookup"><span data-stu-id="bfb89-110">This cmdlet removes a service form the cluster.</span></span>

## <span data-ttu-id="bfb89-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bfb89-111">EXAMPLES</span></span>

### <span data-ttu-id="bfb89-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bfb89-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService1"
PS C:\> Remove-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName
```

<span data-ttu-id="bfb89-113">Este exemplo removerá o serviço "testApp~testService1".</span><span class="sxs-lookup"><span data-stu-id="bfb89-113">This example will remove the service "testApp~testService1".</span></span>

## <span data-ttu-id="bfb89-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="bfb89-114">PARAMETERS</span></span>

### <span data-ttu-id="bfb89-115">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="bfb89-115">-ApplicationName</span></span>
<span data-ttu-id="bfb89-116">Especifique o nome do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bfb89-116">Specify the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfb89-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="bfb89-117">-ClusterName</span></span>
<span data-ttu-id="bfb89-118">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="bfb89-118">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfb89-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfb89-119">-DefaultProfile</span></span>
<span data-ttu-id="bfb89-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bfb89-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bfb89-121">-Force</span><span class="sxs-lookup"><span data-stu-id="bfb89-121">-Force</span></span>
<span data-ttu-id="bfb89-122">Remover sem prompt.</span><span class="sxs-lookup"><span data-stu-id="bfb89-122">Remove without prompt.</span></span>

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

### <span data-ttu-id="bfb89-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bfb89-123">-InputObject</span></span>
<span data-ttu-id="bfb89-124">O recurso de serviço.</span><span class="sxs-lookup"><span data-stu-id="bfb89-124">The service resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSService
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bfb89-125">-Name</span><span class="sxs-lookup"><span data-stu-id="bfb89-125">-Name</span></span>
<span data-ttu-id="bfb89-126">Especifique o nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="bfb89-126">Specify the name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ServiceName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfb89-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bfb89-127">-PassThru</span></span>
<span data-ttu-id="bfb89-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="bfb89-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="bfb89-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfb89-129">-ResourceGroupName</span></span>
<span data-ttu-id="bfb89-130">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bfb89-130">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfb89-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bfb89-131">-ResourceId</span></span>
<span data-ttu-id="bfb89-132">Arm ResourceId do serviço.</span><span class="sxs-lookup"><span data-stu-id="bfb89-132">Arm ResourceId of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfb89-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bfb89-133">-Confirm</span></span>
<span data-ttu-id="bfb89-134">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bfb89-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bfb89-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfb89-135">-WhatIf</span></span>
<span data-ttu-id="bfb89-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bfb89-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bfb89-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bfb89-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bfb89-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfb89-138">CommonParameters</span></span>
<span data-ttu-id="bfb89-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfb89-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfb89-140">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bfb89-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfb89-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bfb89-141">INPUTS</span></span>

### <span data-ttu-id="bfb89-142">System.String</span><span class="sxs-lookup"><span data-stu-id="bfb89-142">System.String</span></span>

### <span data-ttu-id="bfb89-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span><span class="sxs-lookup"><span data-stu-id="bfb89-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span></span>

## <span data-ttu-id="bfb89-144">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="bfb89-144">OUTPUTS</span></span>

### <span data-ttu-id="bfb89-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bfb89-145">System.Boolean</span></span>

## <span data-ttu-id="bfb89-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="bfb89-146">NOTES</span></span>

## <span data-ttu-id="bfb89-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bfb89-147">RELATED LINKS</span></span>
