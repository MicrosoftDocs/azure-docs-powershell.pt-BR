---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: 5ab0499ce3fe98a541031b78e2b432de5a2a39dc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113991"
---
# <span data-ttu-id="1a5e6-101">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="1a5e6-101">Remove-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="1a5e6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1a5e6-102">SYNOPSIS</span></span>
<span data-ttu-id="1a5e6-103">Remova a malha de serviço de uma versão de tipo de aplicativo do cluster.</span><span class="sxs-lookup"><span data-stu-id="1a5e6-103">Remove Service fabric an application type version from the cluster.</span></span> <span data-ttu-id="1a5e6-104">Só dá suporte a versões de tipo de aplicativo implantada pelo ARM.</span><span class="sxs-lookup"><span data-stu-id="1a5e6-104">Only supports ARM deployed application type versions.</span></span>

## <span data-ttu-id="1a5e6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1a5e6-105">SYNTAX</span></span>

### <span data-ttu-id="1a5e6-106">ByResourceGroup (Padrão)</span><span class="sxs-lookup"><span data-stu-id="1a5e6-106">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 -Name <String> -Version <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a5e6-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1a5e6-107">ByResourceId</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a5e6-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="1a5e6-108">ByInputObject</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion -InputObject <PSApplicationTypeVersion> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a5e6-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="1a5e6-109">DESCRIPTION</span></span>
<span data-ttu-id="1a5e6-110">Este cmdlet removerá a malha de serviço de uma versão do tipo de aplicativo do cluster.</span><span class="sxs-lookup"><span data-stu-id="1a5e6-110">This cmdlet will remove Service fabric an application type version from the cluster.</span></span> <span data-ttu-id="1a5e6-111">Todos os aplicativos sob esse recurso devem ser removidos antes de executar esse comando.</span><span class="sxs-lookup"><span data-stu-id="1a5e6-111">All applications under this resource must be removed before running this command.</span></span>

## <span data-ttu-id="1a5e6-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1a5e6-112">EXAMPLES</span></span>

### <span data-ttu-id="1a5e6-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1a5e6-113">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $version = "v1"
PS C:\> Remove-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version $version -Force -PassThru -Verbose
```

<span data-ttu-id="1a5e6-114">Este exemplo removerá a versão "v1" sob o tipo "testAppType".</span><span class="sxs-lookup"><span data-stu-id="1a5e6-114">This example will remove the version "v1" under the type "testAppType".</span></span> <span data-ttu-id="1a5e6-115">Se houver aplicativos sob esse recurso, o comando lançará uma exceção.</span><span class="sxs-lookup"><span data-stu-id="1a5e6-115">It there are any applications under this resource the command will throw an exception.</span></span>

## <span data-ttu-id="1a5e6-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1a5e6-116">PARAMETERS</span></span>

### <span data-ttu-id="1a5e6-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="1a5e6-117">-ClusterName</span></span>
<span data-ttu-id="1a5e6-118">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="1a5e6-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="1a5e6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a5e6-119">-DefaultProfile</span></span>
<span data-ttu-id="1a5e6-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1a5e6-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a5e6-121">-Forçar</span><span class="sxs-lookup"><span data-stu-id="1a5e6-121">-Force</span></span>
<span data-ttu-id="1a5e6-122">Remover sem aviso.</span><span class="sxs-lookup"><span data-stu-id="1a5e6-122">Remove without prompt.</span></span>

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

### <span data-ttu-id="1a5e6-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1a5e6-123">-InputObject</span></span>
<span data-ttu-id="1a5e6-124">O recurso de versão de tipo de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1a5e6-124">The application type version resource.</span></span>

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

### <span data-ttu-id="1a5e6-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="1a5e6-125">-Name</span></span>
<span data-ttu-id="1a5e6-126">Especifique o nome do tipo de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1a5e6-126">Specify the name of the application type.</span></span>

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

### <span data-ttu-id="1a5e6-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1a5e6-127">-PassThru</span></span>
<span data-ttu-id="1a5e6-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="1a5e6-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="1a5e6-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a5e6-129">-ResourceGroupName</span></span>
<span data-ttu-id="1a5e6-130">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1a5e6-130">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="1a5e6-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1a5e6-131">-ResourceId</span></span>
<span data-ttu-id="1a5e6-132">Arm ResourceId da versão do tipo de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1a5e6-132">Arm ResourceId of the application type version.</span></span>

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

### <span data-ttu-id="1a5e6-133">-Versão</span><span class="sxs-lookup"><span data-stu-id="1a5e6-133">-Version</span></span>
<span data-ttu-id="1a5e6-134">Especifique a versão do tipo de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1a5e6-134">Specify the application type version.</span></span>

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

### <span data-ttu-id="1a5e6-135">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="1a5e6-135">-Confirm</span></span>
<span data-ttu-id="1a5e6-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a5e6-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a5e6-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a5e6-137">-WhatIf</span></span>
<span data-ttu-id="1a5e6-138">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="1a5e6-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a5e6-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1a5e6-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a5e6-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a5e6-140">CommonParameters</span></span>
<span data-ttu-id="1a5e6-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a5e6-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a5e6-142">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1a5e6-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a5e6-143">Entradas</span><span class="sxs-lookup"><span data-stu-id="1a5e6-143">INPUTS</span></span>

### <span data-ttu-id="1a5e6-144">System.String</span><span class="sxs-lookup"><span data-stu-id="1a5e6-144">System.String</span></span>

### <span data-ttu-id="1a5e6-145">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="1a5e6-145">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="1a5e6-146">Saídas</span><span class="sxs-lookup"><span data-stu-id="1a5e6-146">OUTPUTS</span></span>

### <span data-ttu-id="1a5e6-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1a5e6-147">System.Boolean</span></span>

## <span data-ttu-id="1a5e6-148">Notas</span><span class="sxs-lookup"><span data-stu-id="1a5e6-148">NOTES</span></span>

## <span data-ttu-id="1a5e6-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1a5e6-149">RELATED LINKS</span></span>
