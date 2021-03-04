---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/remove-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplication.md
ms.openlocfilehash: 5004b6b9528eb91a1883805405dba6147d5161a1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892350"
---
# <span data-ttu-id="ac95d-101">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="ac95d-101">Remove-AzServiceFabricApplication</span></span>

## <span data-ttu-id="ac95d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac95d-102">SYNOPSIS</span></span>
<span data-ttu-id="ac95d-103">Remova um aplicativo do cluster.</span><span class="sxs-lookup"><span data-stu-id="ac95d-103">Remove an application from the cluster.</span></span> <span data-ttu-id="ac95d-104">Isso removerá todos os serviços no aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ac95d-104">This will remove all the services under the application.</span></span> <span data-ttu-id="ac95d-105">Só dá suporte ARM aplicativos implantados.</span><span class="sxs-lookup"><span data-stu-id="ac95d-105">Only supports ARM deployed applications.</span></span>

## <span data-ttu-id="ac95d-106">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ac95d-106">SYNTAX</span></span>

### <span data-ttu-id="ac95d-107">ByResourceGroup (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ac95d-107">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac95d-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ac95d-108">ByResourceId</span></span>
```
Remove-AzServiceFabricApplication -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac95d-109">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ac95d-109">ByInputObject</span></span>
```
Remove-AzServiceFabricApplication -InputObject <PSApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac95d-110">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ac95d-110">DESCRIPTION</span></span>
<span data-ttu-id="ac95d-111">Este cmdlet remove um formulário de aplicativo do cluster.</span><span class="sxs-lookup"><span data-stu-id="ac95d-111">This cmdlet removes an application form the cluster.</span></span> <span data-ttu-id="ac95d-112">Isso removerá todos os serviços, se for o caso, no recurso application.</span><span class="sxs-lookup"><span data-stu-id="ac95d-112">This will remove all the services, if any, under the application resource.</span></span>

## <span data-ttu-id="ac95d-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ac95d-113">EXAMPLES</span></span>

### <span data-ttu-id="ac95d-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ac95d-114">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Remove-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName
```

<span data-ttu-id="ac95d-115">Este exemplo remove o aplicativo "testApp" no grupo de recursos "testRG" e cluster "testCluster".</span><span class="sxs-lookup"><span data-stu-id="ac95d-115">This example removes the application "testApp" under the resource group "testRG" and cluster "testCluster".</span></span>

## <span data-ttu-id="ac95d-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ac95d-116">PARAMETERS</span></span>

### <span data-ttu-id="ac95d-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="ac95d-117">-ClusterName</span></span>
<span data-ttu-id="ac95d-118">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="ac95d-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="ac95d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac95d-119">-DefaultProfile</span></span>
<span data-ttu-id="ac95d-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ac95d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac95d-121">-Force</span><span class="sxs-lookup"><span data-stu-id="ac95d-121">-Force</span></span>
<span data-ttu-id="ac95d-122">Remover sem prompt.</span><span class="sxs-lookup"><span data-stu-id="ac95d-122">Remove without prompt.</span></span>

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

### <span data-ttu-id="ac95d-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ac95d-123">-InputObject</span></span>
<span data-ttu-id="ac95d-124">O recurso do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ac95d-124">The application resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ac95d-125">-Name</span><span class="sxs-lookup"><span data-stu-id="ac95d-125">-Name</span></span>
<span data-ttu-id="ac95d-126">Especifique o nome do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ac95d-126">Specify the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ApplicationName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac95d-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ac95d-127">-PassThru</span></span>
<span data-ttu-id="ac95d-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="ac95d-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="ac95d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac95d-129">-ResourceGroupName</span></span>
<span data-ttu-id="ac95d-130">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ac95d-130">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="ac95d-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ac95d-131">-ResourceId</span></span>
<span data-ttu-id="ac95d-132">Arm ResourceId do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ac95d-132">Arm ResourceId of the application.</span></span>

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

### <span data-ttu-id="ac95d-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ac95d-133">-Confirm</span></span>
<span data-ttu-id="ac95d-134">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac95d-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac95d-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac95d-135">-WhatIf</span></span>
<span data-ttu-id="ac95d-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ac95d-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac95d-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ac95d-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac95d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac95d-138">CommonParameters</span></span>
<span data-ttu-id="ac95d-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac95d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac95d-140">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ac95d-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac95d-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ac95d-141">INPUTS</span></span>

### <span data-ttu-id="ac95d-142">System.String</span><span class="sxs-lookup"><span data-stu-id="ac95d-142">System.String</span></span>

### <span data-ttu-id="ac95d-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span><span class="sxs-lookup"><span data-stu-id="ac95d-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="ac95d-144">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ac95d-144">OUTPUTS</span></span>

### <span data-ttu-id="ac95d-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ac95d-145">System.Boolean</span></span>

## <span data-ttu-id="ac95d-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="ac95d-146">NOTES</span></span>

## <span data-ttu-id="ac95d-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ac95d-147">RELATED LINKS</span></span>
