---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: 7dc8ca2302b00b5eb200c30aed104f5fe5ff8642
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433059"
---
# <span data-ttu-id="179cb-101">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="179cb-101">Get-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="179cb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="179cb-102">SYNOPSIS</span></span>
<span data-ttu-id="179cb-103">Obter detalhes da versão do tipo de aplicativo Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="179cb-103">Get Service Fabric application type version details.</span></span> <span data-ttu-id="179cb-104">Só oferece suporte a versões de tipo de aplicativo ARM implantadas.</span><span class="sxs-lookup"><span data-stu-id="179cb-104">Only supports ARM deployed application type versions.</span></span>

## <span data-ttu-id="179cb-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="179cb-105">SYNTAX</span></span>

### <span data-ttu-id="179cb-106">ByResourceGroupAndCluster (padrão)</span><span class="sxs-lookup"><span data-stu-id="179cb-106">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="179cb-107">ByVersion</span><span class="sxs-lookup"><span data-stu-id="179cb-107">ByVersion</span></span>
```
Get-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-Version] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="179cb-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="179cb-108">ByResourceId</span></span>
```
Get-AzServiceFabricApplicationTypeVersion -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="179cb-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="179cb-109">DESCRIPTION</span></span>
<span data-ttu-id="179cb-110">Use esse cmdlet para obter os detalhes da versão do tipo de aplicativo no grupo de recursos e no cluster especificado.</span><span class="sxs-lookup"><span data-stu-id="179cb-110">Use this cmdlet to get the application type version details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="179cb-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="179cb-111">EXAMPLES</span></span>

### <span data-ttu-id="179cb-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="179cb-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $appTypeName = "v1"
PS C:\> Get-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version
```

<span data-ttu-id="179cb-113">Este exemplo obtém o tipo de aplicativo "testAppType" com a versão "v1", se não encontrar o recurso que ele gerará uma exceção.</span><span class="sxs-lookup"><span data-stu-id="179cb-113">This example gets the application type "testAppType" with version "v1", if it doesn't find the resource it will throw an exception.</span></span>

### <span data-ttu-id="179cb-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="179cb-114">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Get-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName
```

<span data-ttu-id="179cb-115">Este exemplo obtém uma lista das versões de tipo de aplicativo definidas sob o tipo e o cluster especificado.</span><span class="sxs-lookup"><span data-stu-id="179cb-115">This example gets a list of the application type versions defined under the specified cluster and type.</span></span>

## <span data-ttu-id="179cb-116">OS</span><span class="sxs-lookup"><span data-stu-id="179cb-116">PARAMETERS</span></span>

### <span data-ttu-id="179cb-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="179cb-117">-ClusterName</span></span>
<span data-ttu-id="179cb-118">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="179cb-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="179cb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="179cb-119">-DefaultProfile</span></span>
<span data-ttu-id="179cb-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="179cb-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="179cb-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="179cb-121">-Name</span></span>
<span data-ttu-id="179cb-122">Especifique o nome do tipo de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="179cb-122">Specify the name of the application type.</span></span>

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

### <span data-ttu-id="179cb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="179cb-123">-ResourceGroupName</span></span>
<span data-ttu-id="179cb-124">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="179cb-124">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="179cb-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="179cb-125">-ResourceId</span></span>
<span data-ttu-id="179cb-126">Resourcebinding da versão do tipo de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="179cb-126">Arm ResourceId of the application type version.</span></span>

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

### <span data-ttu-id="179cb-127">-Versão</span><span class="sxs-lookup"><span data-stu-id="179cb-127">-Version</span></span>
<span data-ttu-id="179cb-128">Especifique a versão do tipo de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="179cb-128">Specify the version of the application type.</span></span>

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

### <span data-ttu-id="179cb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="179cb-129">CommonParameters</span></span>
<span data-ttu-id="179cb-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="179cb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="179cb-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="179cb-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="179cb-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="179cb-132">INPUTS</span></span>

### <span data-ttu-id="179cb-133">System. String</span><span class="sxs-lookup"><span data-stu-id="179cb-133">System.String</span></span>

## <span data-ttu-id="179cb-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="179cb-134">OUTPUTS</span></span>

### <span data-ttu-id="179cb-135">Microsoft. Azure. Commands. imfabric. Models. PSApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="179cb-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="179cb-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="179cb-136">NOTES</span></span>

## <span data-ttu-id="179cb-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="179cb-137">RELATED LINKS</span></span>
