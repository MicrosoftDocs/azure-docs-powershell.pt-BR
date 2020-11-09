---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationType.md
ms.openlocfilehash: 87557a67c8cb087b8a22ecc9cdfa59a3690057dc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280466"
---
# <span data-ttu-id="14019-101">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="14019-101">Remove-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="14019-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="14019-102">SYNOPSIS</span></span>
<span data-ttu-id="14019-103">Remover a malha de serviços um tipo de aplicativo do cluster.</span><span class="sxs-lookup"><span data-stu-id="14019-103">Remove Service fabric an application type from the cluster.</span></span> <span data-ttu-id="14019-104">Isso removerá todas as versões de tipo desse recurso.</span><span class="sxs-lookup"><span data-stu-id="14019-104">This will remove all type versions under this resource.</span></span>

## <span data-ttu-id="14019-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="14019-105">SYNTAX</span></span>

### <span data-ttu-id="14019-106">ByResourceGroup (padrão)</span><span class="sxs-lookup"><span data-stu-id="14019-106">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name <String>]
 [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14019-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="14019-107">ByResourceId</span></span>
```
Remove-AzServiceFabricApplicationType -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14019-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="14019-108">ByInputObject</span></span>
```
Remove-AzServiceFabricApplicationType -InputObject <PSApplicationType> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14019-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="14019-109">DESCRIPTION</span></span>
<span data-ttu-id="14019-110">Esse cmdlet Remove um tipo de aplicativo do cluster e removerá toda a versão do tipo nesse recurso, mas todos os aplicativos abaixo dele deverão ser removidos antes de executar este comando.</span><span class="sxs-lookup"><span data-stu-id="14019-110">This cmdlet removes an application type form the cluster and will remove all type version under this resource, but all applications under it should be removed before running this command.</span></span>

## <span data-ttu-id="14019-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="14019-111">EXAMPLES</span></span>

### <span data-ttu-id="14019-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="14019-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Remove-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Verbose
```

<span data-ttu-id="14019-113">Este exemplo removerá o tipo de aplicativo "testAppType" e todas as versões abaixo dele.</span><span class="sxs-lookup"><span data-stu-id="14019-113">This example will remove the application type "testAppType" and all the version under it.</span></span> <span data-ttu-id="14019-114">Se houver aplicativos criados com esse tipo, o comando gerará uma exceção.</span><span class="sxs-lookup"><span data-stu-id="14019-114">If there are any applications created with this type, the command will throw an exception.</span></span>

## <span data-ttu-id="14019-115">OS</span><span class="sxs-lookup"><span data-stu-id="14019-115">PARAMETERS</span></span>

### <span data-ttu-id="14019-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="14019-116">-ClusterName</span></span>
<span data-ttu-id="14019-117">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="14019-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="14019-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14019-118">-DefaultProfile</span></span>
<span data-ttu-id="14019-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="14019-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14019-120">-Force</span><span class="sxs-lookup"><span data-stu-id="14019-120">-Force</span></span>
<span data-ttu-id="14019-121">Remover sem aviso.</span><span class="sxs-lookup"><span data-stu-id="14019-121">Remove without prompt.</span></span>

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

### <span data-ttu-id="14019-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="14019-122">-InputObject</span></span>
<span data-ttu-id="14019-123">O recurso de tipo de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="14019-123">The application type resource.</span></span>

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

### <span data-ttu-id="14019-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="14019-124">-Name</span></span>
<span data-ttu-id="14019-125">Especifique o nome do tipo de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="14019-125">Specify the name of the application type.</span></span>

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

### <span data-ttu-id="14019-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="14019-126">-PassThru</span></span>
<span data-ttu-id="14019-127">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="14019-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="14019-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14019-128">-ResourceGroupName</span></span>
<span data-ttu-id="14019-129">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="14019-129">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="14019-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="14019-130">-ResourceId</span></span>
<span data-ttu-id="14019-131">Resourcebinding do tipo de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="14019-131">Arm ResourceId of the application type.</span></span>

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

### <span data-ttu-id="14019-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="14019-132">-Confirm</span></span>
<span data-ttu-id="14019-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14019-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14019-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14019-134">-WhatIf</span></span>
<span data-ttu-id="14019-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="14019-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14019-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="14019-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14019-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14019-137">CommonParameters</span></span>
<span data-ttu-id="14019-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14019-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14019-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="14019-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14019-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="14019-140">INPUTS</span></span>

### <span data-ttu-id="14019-141">System. String</span><span class="sxs-lookup"><span data-stu-id="14019-141">System.String</span></span>

### <span data-ttu-id="14019-142">Microsoft. Azure. Commands. imfabric. Models. PSApplicationType</span><span class="sxs-lookup"><span data-stu-id="14019-142">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="14019-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="14019-143">OUTPUTS</span></span>

### <span data-ttu-id="14019-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="14019-144">System.Boolean</span></span>

## <span data-ttu-id="14019-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="14019-145">NOTES</span></span>

## <span data-ttu-id="14019-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="14019-146">RELATED LINKS</span></span>
