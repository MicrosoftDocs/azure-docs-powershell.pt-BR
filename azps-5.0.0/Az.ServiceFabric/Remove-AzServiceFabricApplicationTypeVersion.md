---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: 498dec77dfc2f4ede8ae81aa70b10acfe2ad2954
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281853"
---
# <span data-ttu-id="e01ad-101">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="e01ad-101">Remove-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="e01ad-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e01ad-102">SYNOPSIS</span></span>
<span data-ttu-id="e01ad-103">Remover a malha de serviços uma versão do tipo de aplicativo do cluster.</span><span class="sxs-lookup"><span data-stu-id="e01ad-103">Remove Service fabric an application type version from the cluster.</span></span>

## <span data-ttu-id="e01ad-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e01ad-104">SYNTAX</span></span>

### <span data-ttu-id="e01ad-105">ByResourceGroup (padrão)</span><span class="sxs-lookup"><span data-stu-id="e01ad-105">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 -Name <String> -Version <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e01ad-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e01ad-106">ByResourceId</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e01ad-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e01ad-107">ByInputObject</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion -InputObject <PSApplicationTypeVersion> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e01ad-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e01ad-108">DESCRIPTION</span></span>
<span data-ttu-id="e01ad-109">Esse cmdlet removerá a malha de serviços uma versão do tipo de aplicativo do cluster.</span><span class="sxs-lookup"><span data-stu-id="e01ad-109">This cmdlet will remove Service fabric an application type version from the cluster.</span></span> <span data-ttu-id="e01ad-110">Todos os aplicativos nesse recurso devem ser removidos antes de executar este comando.</span><span class="sxs-lookup"><span data-stu-id="e01ad-110">All applications under this resource must be removed before running this command.</span></span>

## <span data-ttu-id="e01ad-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e01ad-111">EXAMPLES</span></span>

### <span data-ttu-id="e01ad-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e01ad-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $version = "v1"
PS C:\> Remove-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version $version -Force -PassThru -Verbose
```

<span data-ttu-id="e01ad-113">Este exemplo removerá a versão "v1" sob o tipo "testAppType".</span><span class="sxs-lookup"><span data-stu-id="e01ad-113">This example will remove the version "v1" under the type "testAppType".</span></span> <span data-ttu-id="e01ad-114">Há algum aplicativo nesse recurso que o comando gerará uma exceção.</span><span class="sxs-lookup"><span data-stu-id="e01ad-114">It there are any applications under this resource the command will throw an exception.</span></span>

## <span data-ttu-id="e01ad-115">OS</span><span class="sxs-lookup"><span data-stu-id="e01ad-115">PARAMETERS</span></span>

### <span data-ttu-id="e01ad-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="e01ad-116">-ClusterName</span></span>
<span data-ttu-id="e01ad-117">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="e01ad-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="e01ad-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e01ad-118">-DefaultProfile</span></span>
<span data-ttu-id="e01ad-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e01ad-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e01ad-120">-Force</span><span class="sxs-lookup"><span data-stu-id="e01ad-120">-Force</span></span>
<span data-ttu-id="e01ad-121">Remover sem aviso.</span><span class="sxs-lookup"><span data-stu-id="e01ad-121">Remove without prompt.</span></span>

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

### <span data-ttu-id="e01ad-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e01ad-122">-InputObject</span></span>
<span data-ttu-id="e01ad-123">O recurso de versão do tipo de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e01ad-123">The application type version resource.</span></span>

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

### <span data-ttu-id="e01ad-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="e01ad-124">-Name</span></span>
<span data-ttu-id="e01ad-125">Especifique o nome do tipo de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e01ad-125">Specify the name of the application type.</span></span>

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

### <span data-ttu-id="e01ad-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e01ad-126">-PassThru</span></span>
<span data-ttu-id="e01ad-127">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="e01ad-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="e01ad-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e01ad-128">-ResourceGroupName</span></span>
<span data-ttu-id="e01ad-129">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e01ad-129">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="e01ad-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e01ad-130">-ResourceId</span></span>
<span data-ttu-id="e01ad-131">Resourcebinding da versão do tipo de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e01ad-131">Arm ResourceId of the application type version.</span></span>

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

### <span data-ttu-id="e01ad-132">-Versão</span><span class="sxs-lookup"><span data-stu-id="e01ad-132">-Version</span></span>
<span data-ttu-id="e01ad-133">Especifique a versão do tipo de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e01ad-133">Specify the application type version.</span></span>

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

### <span data-ttu-id="e01ad-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e01ad-134">-Confirm</span></span>
<span data-ttu-id="e01ad-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e01ad-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e01ad-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e01ad-136">-WhatIf</span></span>
<span data-ttu-id="e01ad-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e01ad-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e01ad-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e01ad-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e01ad-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e01ad-139">CommonParameters</span></span>
<span data-ttu-id="e01ad-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e01ad-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e01ad-141">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e01ad-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e01ad-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e01ad-142">INPUTS</span></span>

### <span data-ttu-id="e01ad-143">System. String</span><span class="sxs-lookup"><span data-stu-id="e01ad-143">System.String</span></span>

### <span data-ttu-id="e01ad-144">Microsoft. Azure. Commands. imfabric. Models. PSApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="e01ad-144">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="e01ad-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e01ad-145">OUTPUTS</span></span>

### <span data-ttu-id="e01ad-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e01ad-146">System.Boolean</span></span>

## <span data-ttu-id="e01ad-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e01ad-147">NOTES</span></span>

## <span data-ttu-id="e01ad-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e01ad-148">RELATED LINKS</span></span>
