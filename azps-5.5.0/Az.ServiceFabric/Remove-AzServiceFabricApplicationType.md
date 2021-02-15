---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationType.md
ms.openlocfilehash: 8ba56568a10ee8223a53bc1530602f3ae930e14c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112585"
---
# <span data-ttu-id="211dc-101">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="211dc-101">Remove-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="211dc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="211dc-102">SYNOPSIS</span></span>
<span data-ttu-id="211dc-103">Remover malha de serviço de um tipo de aplicativo do cluster.</span><span class="sxs-lookup"><span data-stu-id="211dc-103">Remove Service fabric an application type from the cluster.</span></span> <span data-ttu-id="211dc-104">Isso removerá todas as versões do tipo sob esse recurso.</span><span class="sxs-lookup"><span data-stu-id="211dc-104">This will remove all type versions under this resource.</span></span> <span data-ttu-id="211dc-105">Só é compatível com tipos de aplicativo implantados pelo ARM.</span><span class="sxs-lookup"><span data-stu-id="211dc-105">Only supports ARM deployed application types.</span></span>

## <span data-ttu-id="211dc-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="211dc-106">SYNTAX</span></span>

### <span data-ttu-id="211dc-107">ByResourceGroup (Padrão)</span><span class="sxs-lookup"><span data-stu-id="211dc-107">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name <String>]
 [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="211dc-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="211dc-108">ByResourceId</span></span>
```
Remove-AzServiceFabricApplicationType -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="211dc-109">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="211dc-109">ByInputObject</span></span>
```
Remove-AzServiceFabricApplicationType -InputObject <PSApplicationType> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="211dc-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="211dc-110">DESCRIPTION</span></span>
<span data-ttu-id="211dc-111">Esse cmdlet remove um formulário de tipo de aplicativo do cluster e remove toda a versão do tipo sob esse recurso, mas todos os aplicativos abaixo dele devem ser removidos antes de executar esse comando.</span><span class="sxs-lookup"><span data-stu-id="211dc-111">This cmdlet removes an application type form the cluster and will remove all type version under this resource, but all applications under it should be removed before running this command.</span></span>

## <span data-ttu-id="211dc-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="211dc-112">EXAMPLES</span></span>

### <span data-ttu-id="211dc-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="211dc-113">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Remove-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Verbose
```

<span data-ttu-id="211dc-114">Este exemplo removerá o tipo de aplicativo "testAppType" e toda a versão abaixo dele.</span><span class="sxs-lookup"><span data-stu-id="211dc-114">This example will remove the application type "testAppType" and all the version under it.</span></span> <span data-ttu-id="211dc-115">Se houver aplicativos criados com esse tipo, o comando lançará uma exceção.</span><span class="sxs-lookup"><span data-stu-id="211dc-115">If there are any applications created with this type, the command will throw an exception.</span></span>

## <span data-ttu-id="211dc-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="211dc-116">PARAMETERS</span></span>

### <span data-ttu-id="211dc-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="211dc-117">-ClusterName</span></span>
<span data-ttu-id="211dc-118">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="211dc-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="211dc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="211dc-119">-DefaultProfile</span></span>
<span data-ttu-id="211dc-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="211dc-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="211dc-121">-Forçar</span><span class="sxs-lookup"><span data-stu-id="211dc-121">-Force</span></span>
<span data-ttu-id="211dc-122">Remover sem aviso.</span><span class="sxs-lookup"><span data-stu-id="211dc-122">Remove without prompt.</span></span>

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

### <span data-ttu-id="211dc-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="211dc-123">-InputObject</span></span>
<span data-ttu-id="211dc-124">O recurso de tipo de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="211dc-124">The application type resource.</span></span>

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

### <span data-ttu-id="211dc-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="211dc-125">-Name</span></span>
<span data-ttu-id="211dc-126">Especifique o nome do tipo de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="211dc-126">Specify the name of the application type.</span></span>

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

### <span data-ttu-id="211dc-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="211dc-127">-PassThru</span></span>
<span data-ttu-id="211dc-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="211dc-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="211dc-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="211dc-129">-ResourceGroupName</span></span>
<span data-ttu-id="211dc-130">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="211dc-130">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="211dc-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="211dc-131">-ResourceId</span></span>
<span data-ttu-id="211dc-132">Arm ResourceId do tipo de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="211dc-132">Arm ResourceId of the application type.</span></span>

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

### <span data-ttu-id="211dc-133">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="211dc-133">-Confirm</span></span>
<span data-ttu-id="211dc-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="211dc-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="211dc-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="211dc-135">-WhatIf</span></span>
<span data-ttu-id="211dc-136">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="211dc-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="211dc-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="211dc-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="211dc-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="211dc-138">CommonParameters</span></span>
<span data-ttu-id="211dc-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="211dc-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="211dc-140">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="211dc-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="211dc-141">Entradas</span><span class="sxs-lookup"><span data-stu-id="211dc-141">INPUTS</span></span>

### <span data-ttu-id="211dc-142">System.String</span><span class="sxs-lookup"><span data-stu-id="211dc-142">System.String</span></span>

### <span data-ttu-id="211dc-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span><span class="sxs-lookup"><span data-stu-id="211dc-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="211dc-144">Saídas</span><span class="sxs-lookup"><span data-stu-id="211dc-144">OUTPUTS</span></span>

### <span data-ttu-id="211dc-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="211dc-145">System.Boolean</span></span>

## <span data-ttu-id="211dc-146">Notas</span><span class="sxs-lookup"><span data-stu-id="211dc-146">NOTES</span></span>

## <span data-ttu-id="211dc-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="211dc-147">RELATED LINKS</span></span>
