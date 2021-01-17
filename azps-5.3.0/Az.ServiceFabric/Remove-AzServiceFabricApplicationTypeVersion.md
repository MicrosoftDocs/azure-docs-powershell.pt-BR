---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: 5ab0499ce3fe98a541031b78e2b432de5a2a39dc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433035"
---
# <span data-ttu-id="6f78b-101">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="6f78b-101">Remove-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="6f78b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6f78b-102">SYNOPSIS</span></span>
<span data-ttu-id="6f78b-103">Remover a malha de serviços uma versão do tipo de aplicativo do cluster.</span><span class="sxs-lookup"><span data-stu-id="6f78b-103">Remove Service fabric an application type version from the cluster.</span></span> <span data-ttu-id="6f78b-104">Só oferece suporte a versões de tipo de aplicativo ARM implantadas.</span><span class="sxs-lookup"><span data-stu-id="6f78b-104">Only supports ARM deployed application type versions.</span></span>

## <span data-ttu-id="6f78b-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6f78b-105">SYNTAX</span></span>

### <span data-ttu-id="6f78b-106">ByResourceGroup (padrão)</span><span class="sxs-lookup"><span data-stu-id="6f78b-106">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 -Name <String> -Version <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f78b-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6f78b-107">ByResourceId</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f78b-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="6f78b-108">ByInputObject</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion -InputObject <PSApplicationTypeVersion> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f78b-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6f78b-109">DESCRIPTION</span></span>
<span data-ttu-id="6f78b-110">Esse cmdlet removerá a malha de serviços uma versão do tipo de aplicativo do cluster.</span><span class="sxs-lookup"><span data-stu-id="6f78b-110">This cmdlet will remove Service fabric an application type version from the cluster.</span></span> <span data-ttu-id="6f78b-111">Todos os aplicativos nesse recurso devem ser removidos antes de executar este comando.</span><span class="sxs-lookup"><span data-stu-id="6f78b-111">All applications under this resource must be removed before running this command.</span></span>

## <span data-ttu-id="6f78b-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6f78b-112">EXAMPLES</span></span>

### <span data-ttu-id="6f78b-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6f78b-113">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $version = "v1"
PS C:\> Remove-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version $version -Force -PassThru -Verbose
```

<span data-ttu-id="6f78b-114">Este exemplo removerá a versão "v1" sob o tipo "testAppType".</span><span class="sxs-lookup"><span data-stu-id="6f78b-114">This example will remove the version "v1" under the type "testAppType".</span></span> <span data-ttu-id="6f78b-115">Há algum aplicativo nesse recurso que o comando gerará uma exceção.</span><span class="sxs-lookup"><span data-stu-id="6f78b-115">It there are any applications under this resource the command will throw an exception.</span></span>

## <span data-ttu-id="6f78b-116">OS</span><span class="sxs-lookup"><span data-stu-id="6f78b-116">PARAMETERS</span></span>

### <span data-ttu-id="6f78b-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="6f78b-117">-ClusterName</span></span>
<span data-ttu-id="6f78b-118">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="6f78b-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="6f78b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f78b-119">-DefaultProfile</span></span>
<span data-ttu-id="6f78b-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6f78b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f78b-121">-Force</span><span class="sxs-lookup"><span data-stu-id="6f78b-121">-Force</span></span>
<span data-ttu-id="6f78b-122">Remover sem aviso.</span><span class="sxs-lookup"><span data-stu-id="6f78b-122">Remove without prompt.</span></span>

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

### <span data-ttu-id="6f78b-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6f78b-123">-InputObject</span></span>
<span data-ttu-id="6f78b-124">O recurso de versão do tipo de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6f78b-124">The application type version resource.</span></span>

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

### <span data-ttu-id="6f78b-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="6f78b-125">-Name</span></span>
<span data-ttu-id="6f78b-126">Especifique o nome do tipo de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6f78b-126">Specify the name of the application type.</span></span>

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

### <span data-ttu-id="6f78b-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6f78b-127">-PassThru</span></span>
<span data-ttu-id="6f78b-128">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="6f78b-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="6f78b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f78b-129">-ResourceGroupName</span></span>
<span data-ttu-id="6f78b-130">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6f78b-130">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="6f78b-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6f78b-131">-ResourceId</span></span>
<span data-ttu-id="6f78b-132">Resourcebinding da versão do tipo de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6f78b-132">Arm ResourceId of the application type version.</span></span>

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

### <span data-ttu-id="6f78b-133">-Versão</span><span class="sxs-lookup"><span data-stu-id="6f78b-133">-Version</span></span>
<span data-ttu-id="6f78b-134">Especifique a versão do tipo de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6f78b-134">Specify the application type version.</span></span>

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

### <span data-ttu-id="6f78b-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6f78b-135">-Confirm</span></span>
<span data-ttu-id="6f78b-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f78b-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f78b-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f78b-137">-WhatIf</span></span>
<span data-ttu-id="6f78b-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6f78b-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f78b-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6f78b-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f78b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f78b-140">CommonParameters</span></span>
<span data-ttu-id="6f78b-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f78b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f78b-142">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6f78b-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f78b-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6f78b-143">INPUTS</span></span>

### <span data-ttu-id="6f78b-144">System. String</span><span class="sxs-lookup"><span data-stu-id="6f78b-144">System.String</span></span>

### <span data-ttu-id="6f78b-145">Microsoft. Azure. Commands. imfabric. Models. PSApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="6f78b-145">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="6f78b-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6f78b-146">OUTPUTS</span></span>

### <span data-ttu-id="6f78b-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6f78b-147">System.Boolean</span></span>

## <span data-ttu-id="6f78b-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6f78b-148">NOTES</span></span>

## <span data-ttu-id="6f78b-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6f78b-149">RELATED LINKS</span></span>
