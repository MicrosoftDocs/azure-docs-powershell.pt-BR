---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplication.md
ms.openlocfilehash: 5946be075e2b97283546614543d5a0d4544bfa0f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118651"
---
# <span data-ttu-id="068f1-101">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="068f1-101">Get-AzServiceFabricApplication</span></span>

## <span data-ttu-id="068f1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="068f1-102">SYNOPSIS</span></span>
<span data-ttu-id="068f1-103">Obter detalhes do aplicativo Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="068f1-103">Get Service Fabric application details.</span></span> <span data-ttu-id="068f1-104">Só é compatível com aplicativos implantados pelo ARM.</span><span class="sxs-lookup"><span data-stu-id="068f1-104">Only supports ARM deployed applications.</span></span>

## <span data-ttu-id="068f1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="068f1-105">SYNTAX</span></span>

### <span data-ttu-id="068f1-106">ByResourceGroupAndCluster (Padrão)</span><span class="sxs-lookup"><span data-stu-id="068f1-106">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="068f1-107">ByName</span><span class="sxs-lookup"><span data-stu-id="068f1-107">ByName</span></span>
```
Get-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="068f1-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="068f1-108">ByResourceId</span></span>
```
Get-AzServiceFabricApplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="068f1-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="068f1-109">DESCRIPTION</span></span>
<span data-ttu-id="068f1-110">Este cmdlet obtém os detalhes do aplicativo no grupo de recursos e cluster especificados.</span><span class="sxs-lookup"><span data-stu-id="068f1-110">This cmdlet gets the application details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="068f1-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="068f1-111">EXAMPLES</span></span>

### <span data-ttu-id="068f1-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="068f1-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName
```

<span data-ttu-id="068f1-113">Este exemplo obtém os detalhes do recurso do aplicativo para o aplicativo "testApp".</span><span class="sxs-lookup"><span data-stu-id="068f1-113">This example gets the application resource details for the application "testApp".</span></span>

### <span data-ttu-id="068f1-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="068f1-114">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName
```

<span data-ttu-id="068f1-115">Este exemplo obtém uma lista dos aplicativos sob o cluster "testCluster".</span><span class="sxs-lookup"><span data-stu-id="068f1-115">This example gets a list of the applications under the cluster "testCluster".</span></span>

## <span data-ttu-id="068f1-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="068f1-116">PARAMETERS</span></span>

### <span data-ttu-id="068f1-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="068f1-117">-ClusterName</span></span>
<span data-ttu-id="068f1-118">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="068f1-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="068f1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="068f1-119">-DefaultProfile</span></span>
<span data-ttu-id="068f1-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="068f1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="068f1-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="068f1-121">-Name</span></span>
<span data-ttu-id="068f1-122">Especifique o nome do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="068f1-122">Specify the name of the application.</span></span>

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

### <span data-ttu-id="068f1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="068f1-123">-ResourceGroupName</span></span>
<span data-ttu-id="068f1-124">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="068f1-124">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="068f1-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="068f1-125">-ResourceId</span></span>
<span data-ttu-id="068f1-126">Arm ResourceId do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="068f1-126">Arm ResourceId of the application.</span></span>

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

### <span data-ttu-id="068f1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="068f1-127">CommonParameters</span></span>
<span data-ttu-id="068f1-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="068f1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="068f1-129">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="068f1-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="068f1-130">Entradas</span><span class="sxs-lookup"><span data-stu-id="068f1-130">INPUTS</span></span>

### <span data-ttu-id="068f1-131">System.String</span><span class="sxs-lookup"><span data-stu-id="068f1-131">System.String</span></span>

## <span data-ttu-id="068f1-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="068f1-132">OUTPUTS</span></span>

### <span data-ttu-id="068f1-133">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span><span class="sxs-lookup"><span data-stu-id="068f1-133">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="068f1-134">Notas</span><span class="sxs-lookup"><span data-stu-id="068f1-134">NOTES</span></span>

## <span data-ttu-id="068f1-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="068f1-135">RELATED LINKS</span></span>
