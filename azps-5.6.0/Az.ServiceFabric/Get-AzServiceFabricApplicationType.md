---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/get-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationType.md
ms.openlocfilehash: 0082f5625351b8bb8e832ad60eb76837f09ccd47
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888176"
---
# <span data-ttu-id="e6a92-101">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="e6a92-101">Get-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="e6a92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6a92-102">SYNOPSIS</span></span>
<span data-ttu-id="e6a92-103">Obter detalhes do tipo de aplicativo do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="e6a92-103">Get Service Fabric application type details.</span></span> <span data-ttu-id="e6a92-104">Oferece suporte ARM tipos de aplicativo implantados.</span><span class="sxs-lookup"><span data-stu-id="e6a92-104">Only supports ARM deployed application types.</span></span>

## <span data-ttu-id="e6a92-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e6a92-105">SYNTAX</span></span>

### <span data-ttu-id="e6a92-106">ByResourceGroupAndCluster (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e6a92-106">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6a92-107">ByName</span><span class="sxs-lookup"><span data-stu-id="e6a92-107">ByName</span></span>
```
Get-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6a92-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e6a92-108">ByResourceId</span></span>
```
Get-AzServiceFabricApplicationType -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e6a92-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e6a92-109">DESCRIPTION</span></span>
<span data-ttu-id="e6a92-110">Use este cmdlet para obter os detalhes do tipo de aplicativo no grupo de recursos especificado e no cluster.</span><span class="sxs-lookup"><span data-stu-id="e6a92-110">Use this cmdlet to get the application type details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="e6a92-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e6a92-111">EXAMPLES</span></span>

### <span data-ttu-id="e6a92-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e6a92-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Get-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName
```

<span data-ttu-id="e6a92-113">Este exemplo obterá os detalhes do tipo de aplicativo com os parâmetros especificados, se ele não encontrar o recurso, ele lançará uma exceção.</span><span class="sxs-lookup"><span data-stu-id="e6a92-113">This example will get the application type details with the parameters specified, if it doesn't find the resource it will throw an exception.</span></span>

### <span data-ttu-id="e6a92-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e6a92-114">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> Get-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName
```

<span data-ttu-id="e6a92-115">Este exemplo obterá uma lista dos tipos de aplicativo definidos no cluster especificado.</span><span class="sxs-lookup"><span data-stu-id="e6a92-115">This example will get a list of the application types defined under the specified cluster.</span></span>

## <span data-ttu-id="e6a92-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e6a92-116">PARAMETERS</span></span>

### <span data-ttu-id="e6a92-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="e6a92-117">-ClusterName</span></span>
<span data-ttu-id="e6a92-118">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="e6a92-118">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndCluster, ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6a92-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6a92-119">-DefaultProfile</span></span>
<span data-ttu-id="e6a92-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e6a92-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6a92-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e6a92-121">-Name</span></span>
<span data-ttu-id="e6a92-122">Especificar o nome do tipo de aplicativo</span><span class="sxs-lookup"><span data-stu-id="e6a92-122">Specify the name of the application type</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ApplicationTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6a92-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6a92-123">-ResourceGroupName</span></span>
<span data-ttu-id="e6a92-124">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e6a92-124">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndCluster, ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6a92-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e6a92-125">-ResourceId</span></span>
<span data-ttu-id="e6a92-126">Arm ResourceId do tipo de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e6a92-126">Arm ResourceId of the application type.</span></span>

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

### <span data-ttu-id="e6a92-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6a92-127">CommonParameters</span></span>
<span data-ttu-id="e6a92-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6a92-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6a92-129">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e6a92-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6a92-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e6a92-130">INPUTS</span></span>

### <span data-ttu-id="e6a92-131">System.String</span><span class="sxs-lookup"><span data-stu-id="e6a92-131">System.String</span></span>

## <span data-ttu-id="e6a92-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e6a92-132">OUTPUTS</span></span>

### <span data-ttu-id="e6a92-133">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span><span class="sxs-lookup"><span data-stu-id="e6a92-133">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="e6a92-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="e6a92-134">NOTES</span></span>

## <span data-ttu-id="e6a92-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e6a92-135">RELATED LINKS</span></span>
