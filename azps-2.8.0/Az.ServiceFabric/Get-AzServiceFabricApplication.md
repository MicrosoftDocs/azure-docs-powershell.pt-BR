---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplication.md
ms.openlocfilehash: 590f2470cacd349eb8f0467ce37e7c15ab5a9321
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772437"
---
# <span data-ttu-id="67ce0-101">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="67ce0-101">Get-AzServiceFabricApplication</span></span>

## <span data-ttu-id="67ce0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="67ce0-102">SYNOPSIS</span></span>
<span data-ttu-id="67ce0-103">Obter detalhes do aplicativo do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="67ce0-103">Get Service Fabric application details.</span></span>

## <span data-ttu-id="67ce0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="67ce0-104">SYNTAX</span></span>

### <span data-ttu-id="67ce0-105">ByResourceGroupAndCluster (padrão)</span><span class="sxs-lookup"><span data-stu-id="67ce0-105">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67ce0-106">ByName</span><span class="sxs-lookup"><span data-stu-id="67ce0-106">ByName</span></span>
```
Get-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67ce0-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="67ce0-107">ByResourceId</span></span>
```
Get-AzServiceFabricApplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="67ce0-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="67ce0-108">DESCRIPTION</span></span>
<span data-ttu-id="67ce0-109">Esse cmdlet obtém os detalhes do aplicativo no grupo de recursos e no cluster especificado.</span><span class="sxs-lookup"><span data-stu-id="67ce0-109">This cmdlet gets the application details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="67ce0-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="67ce0-110">EXAMPLES</span></span>

### <span data-ttu-id="67ce0-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="67ce0-111">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName
```

<span data-ttu-id="67ce0-112">Este exemplo obtém os detalhes de recursos do aplicativo para o aplicativo "testApp".</span><span class="sxs-lookup"><span data-stu-id="67ce0-112">This example gets the application resource details for the application "testApp".</span></span>

### <span data-ttu-id="67ce0-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="67ce0-113">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName
```

<span data-ttu-id="67ce0-114">Este exemplo obtém uma lista dos aplicativos no cluster "testCluster".</span><span class="sxs-lookup"><span data-stu-id="67ce0-114">This example gets a list of the applications under the cluster "testCluster".</span></span>

## <span data-ttu-id="67ce0-115">OS</span><span class="sxs-lookup"><span data-stu-id="67ce0-115">PARAMETERS</span></span>

### <span data-ttu-id="67ce0-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="67ce0-116">-ClusterName</span></span>
<span data-ttu-id="67ce0-117">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="67ce0-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="67ce0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67ce0-118">-DefaultProfile</span></span>
<span data-ttu-id="67ce0-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="67ce0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67ce0-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="67ce0-120">-Name</span></span>
<span data-ttu-id="67ce0-121">Especifique o nome do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="67ce0-121">Specify the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ApplicationName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67ce0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67ce0-122">-ResourceGroupName</span></span>
<span data-ttu-id="67ce0-123">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="67ce0-123">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="67ce0-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="67ce0-124">-ResourceId</span></span>
<span data-ttu-id="67ce0-125">Resourcebinding do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="67ce0-125">Arm ResourceId of the application.</span></span>

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

### <span data-ttu-id="67ce0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67ce0-126">CommonParameters</span></span>
<span data-ttu-id="67ce0-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67ce0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67ce0-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67ce0-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67ce0-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="67ce0-129">INPUTS</span></span>

### <span data-ttu-id="67ce0-130">System. String</span><span class="sxs-lookup"><span data-stu-id="67ce0-130">System.String</span></span>

## <span data-ttu-id="67ce0-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="67ce0-131">OUTPUTS</span></span>

### <span data-ttu-id="67ce0-132">Microsoft. Azure. Commands. imfabric. Models. PSApplication</span><span class="sxs-lookup"><span data-stu-id="67ce0-132">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="67ce0-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="67ce0-133">NOTES</span></span>

## <span data-ttu-id="67ce0-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="67ce0-134">RELATED LINKS</span></span>
