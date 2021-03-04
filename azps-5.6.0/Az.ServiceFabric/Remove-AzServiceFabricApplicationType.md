---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/remove-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationType.md
ms.openlocfilehash: dbd2e29a3136576ecf5596c4a401d689fd0631a3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892349"
---
# <span data-ttu-id="d4a5c-101">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="d4a5c-101">Remove-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="d4a5c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4a5c-102">SYNOPSIS</span></span>
<span data-ttu-id="d4a5c-103">Remover malha de serviço um tipo de aplicativo do cluster.</span><span class="sxs-lookup"><span data-stu-id="d4a5c-103">Remove Service fabric an application type from the cluster.</span></span> <span data-ttu-id="d4a5c-104">Isso removerá todas as versões de tipo sob esse recurso.</span><span class="sxs-lookup"><span data-stu-id="d4a5c-104">This will remove all type versions under this resource.</span></span> <span data-ttu-id="d4a5c-105">Oferece suporte ARM tipos de aplicativo implantados.</span><span class="sxs-lookup"><span data-stu-id="d4a5c-105">Only supports ARM deployed application types.</span></span>

## <span data-ttu-id="d4a5c-106">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d4a5c-106">SYNTAX</span></span>

### <span data-ttu-id="d4a5c-107">ByResourceGroup (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d4a5c-107">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name <String>]
 [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4a5c-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d4a5c-108">ByResourceId</span></span>
```
Remove-AzServiceFabricApplicationType -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4a5c-109">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d4a5c-109">ByInputObject</span></span>
```
Remove-AzServiceFabricApplicationType -InputObject <PSApplicationType> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4a5c-110">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d4a5c-110">DESCRIPTION</span></span>
<span data-ttu-id="d4a5c-111">Este cmdlet remove um tipo de aplicativo do cluster e removerá toda a versão do tipo sob esse recurso, mas todos os aplicativos sob ele devem ser removidos antes de executar esse comando.</span><span class="sxs-lookup"><span data-stu-id="d4a5c-111">This cmdlet removes an application type form the cluster and will remove all type version under this resource, but all applications under it should be removed before running this command.</span></span>

## <span data-ttu-id="d4a5c-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d4a5c-112">EXAMPLES</span></span>

### <span data-ttu-id="d4a5c-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d4a5c-113">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Remove-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Verbose
```

<span data-ttu-id="d4a5c-114">Este exemplo removerá o tipo de aplicativo "testAppType" e toda a versão abaixo dele.</span><span class="sxs-lookup"><span data-stu-id="d4a5c-114">This example will remove the application type "testAppType" and all the version under it.</span></span> <span data-ttu-id="d4a5c-115">Se houver aplicativos criados com esse tipo, o comando lançará uma exceção.</span><span class="sxs-lookup"><span data-stu-id="d4a5c-115">If there are any applications created with this type, the command will throw an exception.</span></span>

## <span data-ttu-id="d4a5c-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d4a5c-116">PARAMETERS</span></span>

### <span data-ttu-id="d4a5c-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="d4a5c-117">-ClusterName</span></span>
<span data-ttu-id="d4a5c-118">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="d4a5c-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="d4a5c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4a5c-119">-DefaultProfile</span></span>
<span data-ttu-id="d4a5c-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d4a5c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4a5c-121">-Force</span><span class="sxs-lookup"><span data-stu-id="d4a5c-121">-Force</span></span>
<span data-ttu-id="d4a5c-122">Remover sem prompt.</span><span class="sxs-lookup"><span data-stu-id="d4a5c-122">Remove without prompt.</span></span>

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

### <span data-ttu-id="d4a5c-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d4a5c-123">-InputObject</span></span>
<span data-ttu-id="d4a5c-124">O recurso de tipo de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d4a5c-124">The application type resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d4a5c-125">-Name</span><span class="sxs-lookup"><span data-stu-id="d4a5c-125">-Name</span></span>
<span data-ttu-id="d4a5c-126">Especifique o nome do tipo de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d4a5c-126">Specify the name of the application type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ApplicationTypeName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4a5c-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d4a5c-127">-PassThru</span></span>
<span data-ttu-id="d4a5c-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="d4a5c-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="d4a5c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4a5c-129">-ResourceGroupName</span></span>
<span data-ttu-id="d4a5c-130">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d4a5c-130">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="d4a5c-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d4a5c-131">-ResourceId</span></span>
<span data-ttu-id="d4a5c-132">Arm ResourceId do tipo de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d4a5c-132">Arm ResourceId of the application type.</span></span>

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

### <span data-ttu-id="d4a5c-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d4a5c-133">-Confirm</span></span>
<span data-ttu-id="d4a5c-134">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4a5c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4a5c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4a5c-135">-WhatIf</span></span>
<span data-ttu-id="d4a5c-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d4a5c-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4a5c-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d4a5c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4a5c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4a5c-138">CommonParameters</span></span>
<span data-ttu-id="d4a5c-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4a5c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4a5c-140">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d4a5c-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4a5c-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d4a5c-141">INPUTS</span></span>

### <span data-ttu-id="d4a5c-142">System.String</span><span class="sxs-lookup"><span data-stu-id="d4a5c-142">System.String</span></span>

### <span data-ttu-id="d4a5c-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span><span class="sxs-lookup"><span data-stu-id="d4a5c-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="d4a5c-144">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d4a5c-144">OUTPUTS</span></span>

### <span data-ttu-id="d4a5c-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d4a5c-145">System.Boolean</span></span>

## <span data-ttu-id="d4a5c-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="d4a5c-146">NOTES</span></span>

## <span data-ttu-id="d4a5c-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d4a5c-147">RELATED LINKS</span></span>
