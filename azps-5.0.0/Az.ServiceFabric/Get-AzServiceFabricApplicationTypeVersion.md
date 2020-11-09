---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: ea86fb4a110d355a848b9fe58969d30ccb96e2da
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281598"
---
# <span data-ttu-id="8e345-101">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="8e345-101">Get-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="8e345-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8e345-102">SYNOPSIS</span></span>
<span data-ttu-id="8e345-103">Obter detalhes da versão do tipo de aplicativo Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="8e345-103">Get Service Fabric application type version details.</span></span>

## <span data-ttu-id="8e345-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8e345-104">SYNTAX</span></span>

### <span data-ttu-id="8e345-105">ByResourceGroupAndCluster (padrão)</span><span class="sxs-lookup"><span data-stu-id="8e345-105">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e345-106">ByVersion</span><span class="sxs-lookup"><span data-stu-id="8e345-106">ByVersion</span></span>
```
Get-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-Version] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e345-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8e345-107">ByResourceId</span></span>
```
Get-AzServiceFabricApplicationTypeVersion -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8e345-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8e345-108">DESCRIPTION</span></span>
<span data-ttu-id="8e345-109">Use esse cmdlet para obter os detalhes da versão do tipo de aplicativo no grupo de recursos e no cluster especificado.</span><span class="sxs-lookup"><span data-stu-id="8e345-109">Use this cmdlet to get the application type version details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="8e345-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8e345-110">EXAMPLES</span></span>

### <span data-ttu-id="8e345-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8e345-111">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $appTypeName = "v1"
PS C:\> Get-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version
```

<span data-ttu-id="8e345-112">Este exemplo obtém o tipo de aplicativo "testAppType" com a versão "v1", se não encontrar o recurso que ele gerará uma exceção.</span><span class="sxs-lookup"><span data-stu-id="8e345-112">This example gets the application type "testAppType" with version "v1", if it doesn't find the resource it will throw an exception.</span></span>

### <span data-ttu-id="8e345-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="8e345-113">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Get-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName
```

<span data-ttu-id="8e345-114">Este exemplo obtém uma lista das versões de tipo de aplicativo definidas sob o tipo e o cluster especificado.</span><span class="sxs-lookup"><span data-stu-id="8e345-114">This example gets a list of the application type versions defined under the specified cluster and type.</span></span>

## <span data-ttu-id="8e345-115">OS</span><span class="sxs-lookup"><span data-stu-id="8e345-115">PARAMETERS</span></span>

### <span data-ttu-id="8e345-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="8e345-116">-ClusterName</span></span>
<span data-ttu-id="8e345-117">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="8e345-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="8e345-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e345-118">-DefaultProfile</span></span>
<span data-ttu-id="8e345-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8e345-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e345-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="8e345-120">-Name</span></span>
<span data-ttu-id="8e345-121">Especifique o nome do tipo de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8e345-121">Specify the name of the application type.</span></span>

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

### <span data-ttu-id="8e345-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e345-122">-ResourceGroupName</span></span>
<span data-ttu-id="8e345-123">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8e345-123">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="8e345-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e345-124">-ResourceId</span></span>
<span data-ttu-id="8e345-125">Resourcebinding da versão do tipo de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8e345-125">Arm ResourceId of the application type version.</span></span>

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

### <span data-ttu-id="8e345-126">-Versão</span><span class="sxs-lookup"><span data-stu-id="8e345-126">-Version</span></span>
<span data-ttu-id="8e345-127">Especifique a versão do tipo de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8e345-127">Specify the version of the application type.</span></span>

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

### <span data-ttu-id="8e345-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e345-128">CommonParameters</span></span>
<span data-ttu-id="8e345-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e345-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e345-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8e345-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e345-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8e345-131">INPUTS</span></span>

### <span data-ttu-id="8e345-132">System. String</span><span class="sxs-lookup"><span data-stu-id="8e345-132">System.String</span></span>

## <span data-ttu-id="8e345-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8e345-133">OUTPUTS</span></span>

### <span data-ttu-id="8e345-134">Microsoft. Azure. Commands. imfabric. Models. PSApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="8e345-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="8e345-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8e345-135">NOTES</span></span>

## <span data-ttu-id="8e345-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8e345-136">RELATED LINKS</span></span>
