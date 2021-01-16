---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplication.md
ms.openlocfilehash: 5946be075e2b97283546614543d5a0d4544bfa0f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98256733"
---
# <span data-ttu-id="16d14-101">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="16d14-101">Get-AzServiceFabricApplication</span></span>

## <span data-ttu-id="16d14-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="16d14-102">SYNOPSIS</span></span>
<span data-ttu-id="16d14-103">Obter detalhes do aplicativo do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="16d14-103">Get Service Fabric application details.</span></span> <span data-ttu-id="16d14-104">Só oferece suporte a aplicativos de ARM distribuído.</span><span class="sxs-lookup"><span data-stu-id="16d14-104">Only supports ARM deployed applications.</span></span>

## <span data-ttu-id="16d14-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="16d14-105">SYNTAX</span></span>

### <span data-ttu-id="16d14-106">ByResourceGroupAndCluster (padrão)</span><span class="sxs-lookup"><span data-stu-id="16d14-106">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16d14-107">ByName</span><span class="sxs-lookup"><span data-stu-id="16d14-107">ByName</span></span>
```
Get-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16d14-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="16d14-108">ByResourceId</span></span>
```
Get-AzServiceFabricApplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="16d14-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="16d14-109">DESCRIPTION</span></span>
<span data-ttu-id="16d14-110">Esse cmdlet obtém os detalhes do aplicativo no grupo de recursos e no cluster especificado.</span><span class="sxs-lookup"><span data-stu-id="16d14-110">This cmdlet gets the application details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="16d14-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="16d14-111">EXAMPLES</span></span>

### <span data-ttu-id="16d14-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="16d14-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName
```

<span data-ttu-id="16d14-113">Este exemplo obtém os detalhes de recursos do aplicativo para o aplicativo "testApp".</span><span class="sxs-lookup"><span data-stu-id="16d14-113">This example gets the application resource details for the application "testApp".</span></span>

### <span data-ttu-id="16d14-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="16d14-114">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName
```

<span data-ttu-id="16d14-115">Este exemplo obtém uma lista dos aplicativos no cluster "testCluster".</span><span class="sxs-lookup"><span data-stu-id="16d14-115">This example gets a list of the applications under the cluster "testCluster".</span></span>

## <span data-ttu-id="16d14-116">OS</span><span class="sxs-lookup"><span data-stu-id="16d14-116">PARAMETERS</span></span>

### <span data-ttu-id="16d14-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="16d14-117">-ClusterName</span></span>
<span data-ttu-id="16d14-118">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="16d14-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="16d14-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16d14-119">-DefaultProfile</span></span>
<span data-ttu-id="16d14-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="16d14-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16d14-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="16d14-121">-Name</span></span>
<span data-ttu-id="16d14-122">Especifique o nome do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="16d14-122">Specify the name of the application.</span></span>

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

### <span data-ttu-id="16d14-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16d14-123">-ResourceGroupName</span></span>
<span data-ttu-id="16d14-124">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="16d14-124">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="16d14-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="16d14-125">-ResourceId</span></span>
<span data-ttu-id="16d14-126">Resourcebinding do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="16d14-126">Arm ResourceId of the application.</span></span>

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

### <span data-ttu-id="16d14-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16d14-127">CommonParameters</span></span>
<span data-ttu-id="16d14-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16d14-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16d14-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="16d14-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16d14-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="16d14-130">INPUTS</span></span>

### <span data-ttu-id="16d14-131">System. String</span><span class="sxs-lookup"><span data-stu-id="16d14-131">System.String</span></span>

## <span data-ttu-id="16d14-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="16d14-132">OUTPUTS</span></span>

### <span data-ttu-id="16d14-133">Microsoft. Azure. Commands. imfabric. Models. PSApplication</span><span class="sxs-lookup"><span data-stu-id="16d14-133">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="16d14-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="16d14-134">NOTES</span></span>

## <span data-ttu-id="16d14-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="16d14-135">RELATED LINKS</span></span>
