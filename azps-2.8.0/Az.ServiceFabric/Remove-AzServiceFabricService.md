---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricService.md
ms.openlocfilehash: 1314eb4d6bf4cfa802e0c6f40cc5ae7646209572
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772417"
---
# <span data-ttu-id="1bc99-101">Remove-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="1bc99-101">Remove-AzServiceFabricService</span></span>

## <span data-ttu-id="1bc99-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1bc99-102">SYNOPSIS</span></span>
<span data-ttu-id="1bc99-103">Remover um serviço do cluster.</span><span class="sxs-lookup"><span data-stu-id="1bc99-103">Remove a service from the cluster.</span></span>

## <span data-ttu-id="1bc99-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1bc99-104">SYNTAX</span></span>

### <span data-ttu-id="1bc99-105">ByResourceGroup (padrão)</span><span class="sxs-lookup"><span data-stu-id="1bc99-105">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1bc99-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1bc99-106">ByResourceId</span></span>
```
Remove-AzServiceFabricService -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1bc99-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="1bc99-107">ByInputObject</span></span>
```
Remove-AzServiceFabricService -InputObject <PSService> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1bc99-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1bc99-108">DESCRIPTION</span></span>
<span data-ttu-id="1bc99-109">Esse cmdlet Remove um serviço do formulário de cluster.</span><span class="sxs-lookup"><span data-stu-id="1bc99-109">This cmdlet removes a service form the cluster.</span></span>

## <span data-ttu-id="1bc99-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1bc99-110">EXAMPLES</span></span>

### <span data-ttu-id="1bc99-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1bc99-111">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService1"
PS C:\> Remove-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName
```

<span data-ttu-id="1bc99-112">Neste exemplo, o serviço "testApp ~ testService1" será removido.</span><span class="sxs-lookup"><span data-stu-id="1bc99-112">This example will remove the service "testApp~testService1".</span></span>

## <span data-ttu-id="1bc99-113">OS</span><span class="sxs-lookup"><span data-stu-id="1bc99-113">PARAMETERS</span></span>

### <span data-ttu-id="1bc99-114">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="1bc99-114">-ApplicationName</span></span>
<span data-ttu-id="1bc99-115">Especifique o nome do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1bc99-115">Specify the name of the application.</span></span>

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

### <span data-ttu-id="1bc99-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="1bc99-116">-ClusterName</span></span>
<span data-ttu-id="1bc99-117">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="1bc99-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="1bc99-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bc99-118">-DefaultProfile</span></span>
<span data-ttu-id="1bc99-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1bc99-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1bc99-120">-Force</span><span class="sxs-lookup"><span data-stu-id="1bc99-120">-Force</span></span>
<span data-ttu-id="1bc99-121">Remover sem aviso.</span><span class="sxs-lookup"><span data-stu-id="1bc99-121">Remove without prompt.</span></span>

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

### <span data-ttu-id="1bc99-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1bc99-122">-InputObject</span></span>
<span data-ttu-id="1bc99-123">O recurso de serviço.</span><span class="sxs-lookup"><span data-stu-id="1bc99-123">The service resource.</span></span>

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

### <span data-ttu-id="1bc99-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="1bc99-124">-Name</span></span>
<span data-ttu-id="1bc99-125">Especifique o nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="1bc99-125">Specify the name of the service.</span></span>

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

### <span data-ttu-id="1bc99-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1bc99-126">-PassThru</span></span>
<span data-ttu-id="1bc99-127">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="1bc99-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="1bc99-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bc99-128">-ResourceGroupName</span></span>
<span data-ttu-id="1bc99-129">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1bc99-129">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="1bc99-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1bc99-130">-ResourceId</span></span>
<span data-ttu-id="1bc99-131">Resourcebinding do serviço.</span><span class="sxs-lookup"><span data-stu-id="1bc99-131">Arm ResourceId of the service.</span></span>

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

### <span data-ttu-id="1bc99-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1bc99-132">-Confirm</span></span>
<span data-ttu-id="1bc99-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1bc99-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1bc99-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1bc99-134">-WhatIf</span></span>
<span data-ttu-id="1bc99-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1bc99-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1bc99-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1bc99-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1bc99-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bc99-137">CommonParameters</span></span>
<span data-ttu-id="1bc99-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bc99-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bc99-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bc99-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bc99-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1bc99-140">INPUTS</span></span>

### <span data-ttu-id="1bc99-141">System. String</span><span class="sxs-lookup"><span data-stu-id="1bc99-141">System.String</span></span>

### <span data-ttu-id="1bc99-142">Microsoft. Azure. Commands. imfabric. Models. PSService</span><span class="sxs-lookup"><span data-stu-id="1bc99-142">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span></span>

## <span data-ttu-id="1bc99-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1bc99-143">OUTPUTS</span></span>

### <span data-ttu-id="1bc99-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1bc99-144">System.Boolean</span></span>

## <span data-ttu-id="1bc99-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1bc99-145">NOTES</span></span>

## <span data-ttu-id="1bc99-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1bc99-146">RELATED LINKS</span></span>
