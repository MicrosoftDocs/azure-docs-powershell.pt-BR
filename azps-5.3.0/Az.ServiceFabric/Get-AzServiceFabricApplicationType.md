---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationType.md
ms.openlocfilehash: 73e89bcb6ffb6f8c09a0ec53f203b6ed251fd3e4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433061"
---
# <span data-ttu-id="ef10d-101">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="ef10d-101">Get-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="ef10d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ef10d-102">SYNOPSIS</span></span>
<span data-ttu-id="ef10d-103">Obter detalhes do tipo de aplicativo Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="ef10d-103">Get Service Fabric application type details.</span></span> <span data-ttu-id="ef10d-104">Só oferece suporte a tipos de aplicativo ARM implantados.</span><span class="sxs-lookup"><span data-stu-id="ef10d-104">Only supports ARM deployed application types.</span></span>

## <span data-ttu-id="ef10d-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ef10d-105">SYNTAX</span></span>

### <span data-ttu-id="ef10d-106">ByResourceGroupAndCluster (padrão)</span><span class="sxs-lookup"><span data-stu-id="ef10d-106">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef10d-107">ByName</span><span class="sxs-lookup"><span data-stu-id="ef10d-107">ByName</span></span>
```
Get-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef10d-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ef10d-108">ByResourceId</span></span>
```
Get-AzServiceFabricApplicationType -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ef10d-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ef10d-109">DESCRIPTION</span></span>
<span data-ttu-id="ef10d-110">Use esse cmdlet para obter os detalhes do tipo de aplicativo no grupo de recursos e no cluster especificado.</span><span class="sxs-lookup"><span data-stu-id="ef10d-110">Use this cmdlet to get the application type details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="ef10d-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ef10d-111">EXAMPLES</span></span>

### <span data-ttu-id="ef10d-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ef10d-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Get-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName
```

<span data-ttu-id="ef10d-113">Este exemplo receberá os detalhes do tipo de aplicativo com os parâmetros especificados, se não encontrar o recurso que ele gerará uma exceção.</span><span class="sxs-lookup"><span data-stu-id="ef10d-113">This example will get the application type details with the parameters specified, if it doesn't find the resource it will throw an exception.</span></span>

### <span data-ttu-id="ef10d-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="ef10d-114">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> Get-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName
```

<span data-ttu-id="ef10d-115">Este exemplo obtém uma lista dos tipos de aplicativo definidos no cluster especificado.</span><span class="sxs-lookup"><span data-stu-id="ef10d-115">This example will get a list of the application types defined under the specified cluster.</span></span>

## <span data-ttu-id="ef10d-116">OS</span><span class="sxs-lookup"><span data-stu-id="ef10d-116">PARAMETERS</span></span>

### <span data-ttu-id="ef10d-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="ef10d-117">-ClusterName</span></span>
<span data-ttu-id="ef10d-118">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="ef10d-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="ef10d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef10d-119">-DefaultProfile</span></span>
<span data-ttu-id="ef10d-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ef10d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef10d-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="ef10d-121">-Name</span></span>
<span data-ttu-id="ef10d-122">Especificar o nome do tipo de aplicativo</span><span class="sxs-lookup"><span data-stu-id="ef10d-122">Specify the name of the application type</span></span>

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

### <span data-ttu-id="ef10d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef10d-123">-ResourceGroupName</span></span>
<span data-ttu-id="ef10d-124">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ef10d-124">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="ef10d-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ef10d-125">-ResourceId</span></span>
<span data-ttu-id="ef10d-126">Resourcebinding do tipo de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ef10d-126">Arm ResourceId of the application type.</span></span>

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

### <span data-ttu-id="ef10d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef10d-127">CommonParameters</span></span>
<span data-ttu-id="ef10d-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef10d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef10d-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ef10d-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef10d-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ef10d-130">INPUTS</span></span>

### <span data-ttu-id="ef10d-131">System. String</span><span class="sxs-lookup"><span data-stu-id="ef10d-131">System.String</span></span>

## <span data-ttu-id="ef10d-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ef10d-132">OUTPUTS</span></span>

### <span data-ttu-id="ef10d-133">Microsoft. Azure. Commands. imfabric. Models. PSApplicationType</span><span class="sxs-lookup"><span data-stu-id="ef10d-133">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="ef10d-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ef10d-134">NOTES</span></span>

## <span data-ttu-id="ef10d-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ef10d-135">RELATED LINKS</span></span>
