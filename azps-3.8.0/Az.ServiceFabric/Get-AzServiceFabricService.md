---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricService.md
ms.openlocfilehash: 62f1e4a9313ebcbd2ad6d815344dc18e5844ed13
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941723"
---
# <span data-ttu-id="72b13-101">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="72b13-101">Get-AzServiceFabricService</span></span>

## <span data-ttu-id="72b13-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="72b13-102">SYNOPSIS</span></span>
<span data-ttu-id="72b13-103">Obter detalhes do serviço do Service Fabric no aplicativo e no cluster especificados.</span><span class="sxs-lookup"><span data-stu-id="72b13-103">Get Service Fabric service details under the specified application and cluster.</span></span>

## <span data-ttu-id="72b13-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="72b13-104">SYNTAX</span></span>

### <span data-ttu-id="72b13-105">ByResourceGroupAndCluster (padrão)</span><span class="sxs-lookup"><span data-stu-id="72b13-105">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72b13-106">ByName</span><span class="sxs-lookup"><span data-stu-id="72b13-106">ByName</span></span>
```
Get-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72b13-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="72b13-107">ByResourceId</span></span>
```
Get-AzServiceFabricService -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72b13-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="72b13-108">DESCRIPTION</span></span>
<span data-ttu-id="72b13-109">Esse cmdlet obterá os detalhes do serviço no aplicativo e no cluster especificados.</span><span class="sxs-lookup"><span data-stu-id="72b13-109">This cmdlet will get the service details in the specified application and cluster.</span></span>

## <span data-ttu-id="72b13-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="72b13-110">EXAMPLES</span></span>

### <span data-ttu-id="72b13-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="72b13-111">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService"
PS C:\> Get-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName
```

<span data-ttu-id="72b13-112">Este exemplo obtém os detalhes do recurso de serviço para o serviço "testApp ~ testService".</span><span class="sxs-lookup"><span data-stu-id="72b13-112">This example gets the service resource details for the service "testApp~testService".</span></span>

### <span data-ttu-id="72b13-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="72b13-113">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName
```

<span data-ttu-id="72b13-114">Este exemplo obtém uma lista dos serviços sob o aplicativo "testApp".</span><span class="sxs-lookup"><span data-stu-id="72b13-114">This example gets a list of the services under the application "testApp".</span></span>

## <span data-ttu-id="72b13-115">OS</span><span class="sxs-lookup"><span data-stu-id="72b13-115">PARAMETERS</span></span>

### <span data-ttu-id="72b13-116">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="72b13-116">-ApplicationName</span></span>
<span data-ttu-id="72b13-117">Especifique o nome do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="72b13-117">Specify the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndCluster, ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72b13-118">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="72b13-118">-ClusterName</span></span>
<span data-ttu-id="72b13-119">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="72b13-119">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="72b13-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72b13-120">-DefaultProfile</span></span>
<span data-ttu-id="72b13-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="72b13-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72b13-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="72b13-122">-Name</span></span>
<span data-ttu-id="72b13-123">Especifique o nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="72b13-123">Specify the name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ServiceName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72b13-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72b13-124">-ResourceGroupName</span></span>
<span data-ttu-id="72b13-125">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="72b13-125">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="72b13-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="72b13-126">-ResourceId</span></span>
<span data-ttu-id="72b13-127">Resourcebinding do serviço.</span><span class="sxs-lookup"><span data-stu-id="72b13-127">Arm ResourceId of the service.</span></span>

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

### <span data-ttu-id="72b13-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72b13-128">CommonParameters</span></span>
<span data-ttu-id="72b13-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72b13-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72b13-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72b13-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72b13-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="72b13-131">INPUTS</span></span>

### <span data-ttu-id="72b13-132">System. String</span><span class="sxs-lookup"><span data-stu-id="72b13-132">System.String</span></span>

## <span data-ttu-id="72b13-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="72b13-133">OUTPUTS</span></span>

### <span data-ttu-id="72b13-134">Microsoft. Azure. Commands. imfabric. Models. PSService</span><span class="sxs-lookup"><span data-stu-id="72b13-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span></span>

## <span data-ttu-id="72b13-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="72b13-135">NOTES</span></span>

## <span data-ttu-id="72b13-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="72b13-136">RELATED LINKS</span></span>
