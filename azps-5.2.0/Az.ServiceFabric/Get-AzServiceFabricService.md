---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricService.md
ms.openlocfilehash: d927ef9a8a1c3ef97976911b122f22e1948f2996
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98256732"
---
# <span data-ttu-id="00c8e-101">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="00c8e-101">Get-AzServiceFabricService</span></span>

## <span data-ttu-id="00c8e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="00c8e-102">SYNOPSIS</span></span>
<span data-ttu-id="00c8e-103">Obter detalhes do serviço do Service Fabric no aplicativo e no cluster especificados.</span><span class="sxs-lookup"><span data-stu-id="00c8e-103">Get Service Fabric service details under the specified application and cluster.</span></span> <span data-ttu-id="00c8e-104">Só oferece suporte a serviços de ARM distribuído.</span><span class="sxs-lookup"><span data-stu-id="00c8e-104">Only supports ARM deployed services.</span></span>

## <span data-ttu-id="00c8e-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="00c8e-105">SYNTAX</span></span>

### <span data-ttu-id="00c8e-106">ByResourceGroupAndCluster (padrão)</span><span class="sxs-lookup"><span data-stu-id="00c8e-106">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00c8e-107">ByName</span><span class="sxs-lookup"><span data-stu-id="00c8e-107">ByName</span></span>
```
Get-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00c8e-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="00c8e-108">ByResourceId</span></span>
```
Get-AzServiceFabricService -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00c8e-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="00c8e-109">DESCRIPTION</span></span>
<span data-ttu-id="00c8e-110">Esse cmdlet obterá os detalhes do serviço no aplicativo e no cluster especificados.</span><span class="sxs-lookup"><span data-stu-id="00c8e-110">This cmdlet will get the service details in the specified application and cluster.</span></span>

## <span data-ttu-id="00c8e-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="00c8e-111">EXAMPLES</span></span>

### <span data-ttu-id="00c8e-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="00c8e-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService"
PS C:\> Get-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName
```

<span data-ttu-id="00c8e-113">Este exemplo obtém os detalhes do recurso de serviço para o serviço "testApp ~ testService".</span><span class="sxs-lookup"><span data-stu-id="00c8e-113">This example gets the service resource details for the service "testApp~testService".</span></span>

### <span data-ttu-id="00c8e-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="00c8e-114">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName
```

<span data-ttu-id="00c8e-115">Este exemplo obtém uma lista dos serviços sob o aplicativo "testApp".</span><span class="sxs-lookup"><span data-stu-id="00c8e-115">This example gets a list of the services under the application "testApp".</span></span>

## <span data-ttu-id="00c8e-116">OS</span><span class="sxs-lookup"><span data-stu-id="00c8e-116">PARAMETERS</span></span>

### <span data-ttu-id="00c8e-117">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="00c8e-117">-ApplicationName</span></span>
<span data-ttu-id="00c8e-118">Especifique o nome do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="00c8e-118">Specify the name of the application.</span></span>

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

### <span data-ttu-id="00c8e-119">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="00c8e-119">-ClusterName</span></span>
<span data-ttu-id="00c8e-120">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="00c8e-120">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="00c8e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00c8e-121">-DefaultProfile</span></span>
<span data-ttu-id="00c8e-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="00c8e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00c8e-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="00c8e-123">-Name</span></span>
<span data-ttu-id="00c8e-124">Especifique o nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="00c8e-124">Specify the name of the service.</span></span>

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

### <span data-ttu-id="00c8e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00c8e-125">-ResourceGroupName</span></span>
<span data-ttu-id="00c8e-126">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="00c8e-126">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="00c8e-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="00c8e-127">-ResourceId</span></span>
<span data-ttu-id="00c8e-128">Resourcebinding do serviço.</span><span class="sxs-lookup"><span data-stu-id="00c8e-128">Arm ResourceId of the service.</span></span>

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

### <span data-ttu-id="00c8e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00c8e-129">CommonParameters</span></span>
<span data-ttu-id="00c8e-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00c8e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00c8e-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="00c8e-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00c8e-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="00c8e-132">INPUTS</span></span>

### <span data-ttu-id="00c8e-133">System. String</span><span class="sxs-lookup"><span data-stu-id="00c8e-133">System.String</span></span>

## <span data-ttu-id="00c8e-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="00c8e-134">OUTPUTS</span></span>

### <span data-ttu-id="00c8e-135">Microsoft. Azure. Commands. imfabric. Models. PSService</span><span class="sxs-lookup"><span data-stu-id="00c8e-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span></span>

## <span data-ttu-id="00c8e-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="00c8e-136">NOTES</span></span>

## <span data-ttu-id="00c8e-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="00c8e-137">RELATED LINKS</span></span>
