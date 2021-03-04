---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/get-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: 9c9f1b3c88e49eca3be8a923324d195d3a773c1b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888175"
---
# <span data-ttu-id="3cd8e-101">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="3cd8e-101">Get-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="3cd8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3cd8e-102">SYNOPSIS</span></span>
<span data-ttu-id="3cd8e-103">Obter detalhes da versão do tipo de aplicativo do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="3cd8e-103">Get Service Fabric application type version details.</span></span> <span data-ttu-id="3cd8e-104">Só dá suporte ARM versões de tipo de aplicativo implantadas.</span><span class="sxs-lookup"><span data-stu-id="3cd8e-104">Only supports ARM deployed application type versions.</span></span>

## <span data-ttu-id="3cd8e-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="3cd8e-105">SYNTAX</span></span>

### <span data-ttu-id="3cd8e-106">ByResourceGroupAndCluster (Padrão)</span><span class="sxs-lookup"><span data-stu-id="3cd8e-106">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3cd8e-107">ByVersion</span><span class="sxs-lookup"><span data-stu-id="3cd8e-107">ByVersion</span></span>
```
Get-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-Version] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3cd8e-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3cd8e-108">ByResourceId</span></span>
```
Get-AzServiceFabricApplicationTypeVersion -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3cd8e-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3cd8e-109">DESCRIPTION</span></span>
<span data-ttu-id="3cd8e-110">Use este cmdlet para obter os detalhes da versão do tipo de aplicativo no grupo de recursos especificado e no cluster.</span><span class="sxs-lookup"><span data-stu-id="3cd8e-110">Use this cmdlet to get the application type version details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="3cd8e-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3cd8e-111">EXAMPLES</span></span>

### <span data-ttu-id="3cd8e-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3cd8e-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $appTypeName = "v1"
PS C:\> Get-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version
```

<span data-ttu-id="3cd8e-113">Este exemplo obtém o tipo de aplicativo "testAppType" com a versão "v1", se ele não encontrar o recurso, ele lançará uma exceção.</span><span class="sxs-lookup"><span data-stu-id="3cd8e-113">This example gets the application type "testAppType" with version "v1", if it doesn't find the resource it will throw an exception.</span></span>

### <span data-ttu-id="3cd8e-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="3cd8e-114">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Get-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName
```

<span data-ttu-id="3cd8e-115">Este exemplo obtém uma lista das versões de tipo de aplicativo definidas sob o cluster especificado e o tipo.</span><span class="sxs-lookup"><span data-stu-id="3cd8e-115">This example gets a list of the application type versions defined under the specified cluster and type.</span></span>

## <span data-ttu-id="3cd8e-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="3cd8e-116">PARAMETERS</span></span>

### <span data-ttu-id="3cd8e-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="3cd8e-117">-ClusterName</span></span>
<span data-ttu-id="3cd8e-118">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="3cd8e-118">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndCluster, ByVersion
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cd8e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cd8e-119">-DefaultProfile</span></span>
<span data-ttu-id="3cd8e-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3cd8e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3cd8e-121">-Name</span><span class="sxs-lookup"><span data-stu-id="3cd8e-121">-Name</span></span>
<span data-ttu-id="3cd8e-122">Especifique o nome do tipo de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3cd8e-122">Specify the name of the application type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndCluster, ByVersion
Aliases: ApplicationTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cd8e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cd8e-123">-ResourceGroupName</span></span>
<span data-ttu-id="3cd8e-124">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3cd8e-124">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndCluster, ByVersion
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cd8e-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3cd8e-125">-ResourceId</span></span>
<span data-ttu-id="3cd8e-126">Arm ResourceId da versão do tipo de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3cd8e-126">Arm ResourceId of the application type version.</span></span>

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

### <span data-ttu-id="3cd8e-127">-Version</span><span class="sxs-lookup"><span data-stu-id="3cd8e-127">-Version</span></span>
<span data-ttu-id="3cd8e-128">Especifique a versão do tipo de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3cd8e-128">Specify the version of the application type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVersion
Aliases: ApplicationTypeVersion

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cd8e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cd8e-129">CommonParameters</span></span>
<span data-ttu-id="3cd8e-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cd8e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cd8e-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3cd8e-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cd8e-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3cd8e-132">INPUTS</span></span>

### <span data-ttu-id="3cd8e-133">System.String</span><span class="sxs-lookup"><span data-stu-id="3cd8e-133">System.String</span></span>

## <span data-ttu-id="3cd8e-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="3cd8e-134">OUTPUTS</span></span>

### <span data-ttu-id="3cd8e-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="3cd8e-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="3cd8e-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="3cd8e-136">NOTES</span></span>

## <span data-ttu-id="3cd8e-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3cd8e-137">RELATED LINKS</span></span>
