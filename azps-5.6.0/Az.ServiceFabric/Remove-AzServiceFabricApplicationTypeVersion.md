---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/remove-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: 217666284a2245b79864bb6561a1f85143c1ae80
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892347"
---
# <span data-ttu-id="39459-101">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="39459-101">Remove-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="39459-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39459-102">SYNOPSIS</span></span>
<span data-ttu-id="39459-103">Remover o service fabric uma versão do tipo de aplicativo do cluster.</span><span class="sxs-lookup"><span data-stu-id="39459-103">Remove Service fabric an application type version from the cluster.</span></span> <span data-ttu-id="39459-104">Só dá suporte ARM versões de tipo de aplicativo implantadas.</span><span class="sxs-lookup"><span data-stu-id="39459-104">Only supports ARM deployed application type versions.</span></span>

## <span data-ttu-id="39459-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="39459-105">SYNTAX</span></span>

### <span data-ttu-id="39459-106">ByResourceGroup (Padrão)</span><span class="sxs-lookup"><span data-stu-id="39459-106">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 -Name <String> -Version <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39459-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="39459-107">ByResourceId</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39459-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="39459-108">ByInputObject</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion -InputObject <PSApplicationTypeVersion> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39459-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="39459-109">DESCRIPTION</span></span>
<span data-ttu-id="39459-110">Este cmdlet removerá a malha de serviço de uma versão de tipo de aplicativo do cluster.</span><span class="sxs-lookup"><span data-stu-id="39459-110">This cmdlet will remove Service fabric an application type version from the cluster.</span></span> <span data-ttu-id="39459-111">Todos os aplicativos sob esse recurso devem ser removidos antes de executar este comando.</span><span class="sxs-lookup"><span data-stu-id="39459-111">All applications under this resource must be removed before running this command.</span></span>

## <span data-ttu-id="39459-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="39459-112">EXAMPLES</span></span>

### <span data-ttu-id="39459-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="39459-113">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $version = "v1"
PS C:\> Remove-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version $version -Force -PassThru -Verbose
```

<span data-ttu-id="39459-114">Este exemplo removerá a versão "v1" no tipo "testAppType".</span><span class="sxs-lookup"><span data-stu-id="39459-114">This example will remove the version "v1" under the type "testAppType".</span></span> <span data-ttu-id="39459-115">Se houver aplicativos sob esse recurso, o comando lançará uma exceção.</span><span class="sxs-lookup"><span data-stu-id="39459-115">It there are any applications under this resource the command will throw an exception.</span></span>

## <span data-ttu-id="39459-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="39459-116">PARAMETERS</span></span>

### <span data-ttu-id="39459-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="39459-117">-ClusterName</span></span>
<span data-ttu-id="39459-118">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="39459-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="39459-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39459-119">-DefaultProfile</span></span>
<span data-ttu-id="39459-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="39459-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39459-121">-Force</span><span class="sxs-lookup"><span data-stu-id="39459-121">-Force</span></span>
<span data-ttu-id="39459-122">Remover sem prompt.</span><span class="sxs-lookup"><span data-stu-id="39459-122">Remove without prompt.</span></span>

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

### <span data-ttu-id="39459-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="39459-123">-InputObject</span></span>
<span data-ttu-id="39459-124">O recurso de versão do tipo de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="39459-124">The application type version resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="39459-125">-Name</span><span class="sxs-lookup"><span data-stu-id="39459-125">-Name</span></span>
<span data-ttu-id="39459-126">Especifique o nome do tipo de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="39459-126">Specify the name of the application type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ApplicationTypeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39459-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="39459-127">-PassThru</span></span>
<span data-ttu-id="39459-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="39459-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="39459-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39459-129">-ResourceGroupName</span></span>
<span data-ttu-id="39459-130">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="39459-130">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="39459-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="39459-131">-ResourceId</span></span>
<span data-ttu-id="39459-132">Arm ResourceId da versão do tipo de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="39459-132">Arm ResourceId of the application type version.</span></span>

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

### <span data-ttu-id="39459-133">-Version</span><span class="sxs-lookup"><span data-stu-id="39459-133">-Version</span></span>
<span data-ttu-id="39459-134">Especifique a versão do tipo de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="39459-134">Specify the application type version.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ApplicationTypeVersion

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39459-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="39459-135">-Confirm</span></span>
<span data-ttu-id="39459-136">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39459-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39459-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39459-137">-WhatIf</span></span>
<span data-ttu-id="39459-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="39459-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39459-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="39459-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39459-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39459-140">CommonParameters</span></span>
<span data-ttu-id="39459-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39459-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39459-142">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="39459-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39459-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="39459-143">INPUTS</span></span>

### <span data-ttu-id="39459-144">System.String</span><span class="sxs-lookup"><span data-stu-id="39459-144">System.String</span></span>

### <span data-ttu-id="39459-145">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="39459-145">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="39459-146">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="39459-146">OUTPUTS</span></span>

### <span data-ttu-id="39459-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="39459-147">System.Boolean</span></span>

## <span data-ttu-id="39459-148">NOTES</span><span class="sxs-lookup"><span data-stu-id="39459-148">NOTES</span></span>

## <span data-ttu-id="39459-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="39459-149">RELATED LINKS</span></span>
