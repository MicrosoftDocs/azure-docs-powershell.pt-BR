---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationType.md
ms.openlocfilehash: 78cec82383c257e325c35d0987de73f37aff253d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772434"
---
# <span data-ttu-id="c8141-101">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="c8141-101">Get-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="c8141-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c8141-102">SYNOPSIS</span></span>
<span data-ttu-id="c8141-103">Obter detalhes do tipo de aplicativo Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="c8141-103">Get Service Fabric application type details.</span></span>

## <span data-ttu-id="c8141-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c8141-104">SYNTAX</span></span>

### <span data-ttu-id="c8141-105">ByResourceGroupAndCluster (padrão)</span><span class="sxs-lookup"><span data-stu-id="c8141-105">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8141-106">ByName</span><span class="sxs-lookup"><span data-stu-id="c8141-106">ByName</span></span>
```
Get-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8141-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c8141-107">ByResourceId</span></span>
```
Get-AzServiceFabricApplicationType -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c8141-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c8141-108">DESCRIPTION</span></span>
<span data-ttu-id="c8141-109">Use esse cmdlet para obter os detalhes do tipo de aplicativo no grupo de recursos e no cluster especificado.</span><span class="sxs-lookup"><span data-stu-id="c8141-109">Use this cmdlet to get the application type details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="c8141-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c8141-110">EXAMPLES</span></span>

### <span data-ttu-id="c8141-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c8141-111">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Get-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName
```

<span data-ttu-id="c8141-112">Este exemplo receberá os detalhes do tipo de aplicativo com os parâmetros especificados, se não encontrar o recurso que ele gerará uma exceção.</span><span class="sxs-lookup"><span data-stu-id="c8141-112">This example will get the application type details with the parameters specified, if it doesn't find the resource it will throw an exception.</span></span>

### <span data-ttu-id="c8141-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c8141-113">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> Get-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName
```

<span data-ttu-id="c8141-114">Este exemplo obtém uma lista dos tipos de aplicativo definidos no cluster especificado.</span><span class="sxs-lookup"><span data-stu-id="c8141-114">This example will get a list of the application types defined under the specified cluster.</span></span>

## <span data-ttu-id="c8141-115">OS</span><span class="sxs-lookup"><span data-stu-id="c8141-115">PARAMETERS</span></span>

### <span data-ttu-id="c8141-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="c8141-116">-ClusterName</span></span>
<span data-ttu-id="c8141-117">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="c8141-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="c8141-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8141-118">-DefaultProfile</span></span>
<span data-ttu-id="c8141-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c8141-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8141-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="c8141-120">-Name</span></span>
<span data-ttu-id="c8141-121">Especificar o nome do tipo de aplicativo</span><span class="sxs-lookup"><span data-stu-id="c8141-121">Specify the name of the application type</span></span>

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

### <span data-ttu-id="c8141-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8141-122">-ResourceGroupName</span></span>
<span data-ttu-id="c8141-123">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c8141-123">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="c8141-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c8141-124">-ResourceId</span></span>
<span data-ttu-id="c8141-125">Resourcebinding do tipo de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c8141-125">Arm ResourceId of the application type.</span></span>

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

### <span data-ttu-id="c8141-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8141-126">CommonParameters</span></span>
<span data-ttu-id="c8141-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8141-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8141-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8141-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8141-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c8141-129">INPUTS</span></span>

### <span data-ttu-id="c8141-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c8141-130">System.String</span></span>

## <span data-ttu-id="c8141-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c8141-131">OUTPUTS</span></span>

### <span data-ttu-id="c8141-132">Microsoft. Azure. Commands. imfabric. Models. PSApplicationType</span><span class="sxs-lookup"><span data-stu-id="c8141-132">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="c8141-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c8141-133">NOTES</span></span>

## <span data-ttu-id="c8141-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c8141-134">RELATED LINKS</span></span>