---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricService.md
ms.openlocfilehash: 2a41a61b67ea77e2927acf5eef7b7d520464978a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116378"
---
# <span data-ttu-id="db03e-101">Remove-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="db03e-101">Remove-AzServiceFabricService</span></span>

## <span data-ttu-id="db03e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="db03e-102">SYNOPSIS</span></span>
<span data-ttu-id="db03e-103">Remover um serviço do cluster.</span><span class="sxs-lookup"><span data-stu-id="db03e-103">Remove a service from the cluster.</span></span> <span data-ttu-id="db03e-104">Só é compatível com serviços implantados pelo ARM.</span><span class="sxs-lookup"><span data-stu-id="db03e-104">Only supports ARM deployed services.</span></span>

## <span data-ttu-id="db03e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="db03e-105">SYNTAX</span></span>

### <span data-ttu-id="db03e-106">ByResourceGroup (Padrão)</span><span class="sxs-lookup"><span data-stu-id="db03e-106">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="db03e-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="db03e-107">ByResourceId</span></span>
```
Remove-AzServiceFabricService -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db03e-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="db03e-108">ByInputObject</span></span>
```
Remove-AzServiceFabricService -InputObject <PSService> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db03e-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="db03e-109">DESCRIPTION</span></span>
<span data-ttu-id="db03e-110">Este cmdlet remove um formulário de serviço do cluster.</span><span class="sxs-lookup"><span data-stu-id="db03e-110">This cmdlet removes a service form the cluster.</span></span>

## <span data-ttu-id="db03e-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="db03e-111">EXAMPLES</span></span>

### <span data-ttu-id="db03e-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="db03e-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService1"
PS C:\> Remove-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName
```

<span data-ttu-id="db03e-113">Este exemplo removerá o serviço "testApp~testService1".</span><span class="sxs-lookup"><span data-stu-id="db03e-113">This example will remove the service "testApp~testService1".</span></span>

## <span data-ttu-id="db03e-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="db03e-114">PARAMETERS</span></span>

### <span data-ttu-id="db03e-115">-Nomedo Aplicativo</span><span class="sxs-lookup"><span data-stu-id="db03e-115">-ApplicationName</span></span>
<span data-ttu-id="db03e-116">Especifique o nome do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="db03e-116">Specify the name of the application.</span></span>

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

### <span data-ttu-id="db03e-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="db03e-117">-ClusterName</span></span>
<span data-ttu-id="db03e-118">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="db03e-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="db03e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db03e-119">-DefaultProfile</span></span>
<span data-ttu-id="db03e-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="db03e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db03e-121">-Forçar</span><span class="sxs-lookup"><span data-stu-id="db03e-121">-Force</span></span>
<span data-ttu-id="db03e-122">Remover sem aviso.</span><span class="sxs-lookup"><span data-stu-id="db03e-122">Remove without prompt.</span></span>

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

### <span data-ttu-id="db03e-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="db03e-123">-InputObject</span></span>
<span data-ttu-id="db03e-124">O recurso de serviço.</span><span class="sxs-lookup"><span data-stu-id="db03e-124">The service resource.</span></span>

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

### <span data-ttu-id="db03e-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="db03e-125">-Name</span></span>
<span data-ttu-id="db03e-126">Especifique o nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="db03e-126">Specify the name of the service.</span></span>

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

### <span data-ttu-id="db03e-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="db03e-127">-PassThru</span></span>
<span data-ttu-id="db03e-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="db03e-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="db03e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db03e-129">-ResourceGroupName</span></span>
<span data-ttu-id="db03e-130">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="db03e-130">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="db03e-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="db03e-131">-ResourceId</span></span>
<span data-ttu-id="db03e-132">Arm ResourceId do serviço.</span><span class="sxs-lookup"><span data-stu-id="db03e-132">Arm ResourceId of the service.</span></span>

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

### <span data-ttu-id="db03e-133">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="db03e-133">-Confirm</span></span>
<span data-ttu-id="db03e-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db03e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db03e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db03e-135">-WhatIf</span></span>
<span data-ttu-id="db03e-136">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="db03e-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db03e-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="db03e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db03e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db03e-138">CommonParameters</span></span>
<span data-ttu-id="db03e-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db03e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db03e-140">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="db03e-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db03e-141">Entradas</span><span class="sxs-lookup"><span data-stu-id="db03e-141">INPUTS</span></span>

### <span data-ttu-id="db03e-142">System.String</span><span class="sxs-lookup"><span data-stu-id="db03e-142">System.String</span></span>

### <span data-ttu-id="db03e-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span><span class="sxs-lookup"><span data-stu-id="db03e-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span></span>

## <span data-ttu-id="db03e-144">Saídas</span><span class="sxs-lookup"><span data-stu-id="db03e-144">OUTPUTS</span></span>

### <span data-ttu-id="db03e-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="db03e-145">System.Boolean</span></span>

## <span data-ttu-id="db03e-146">Notas</span><span class="sxs-lookup"><span data-stu-id="db03e-146">NOTES</span></span>

## <span data-ttu-id="db03e-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="db03e-147">RELATED LINKS</span></span>
