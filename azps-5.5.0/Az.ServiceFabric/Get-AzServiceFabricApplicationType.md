---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationType.md
ms.openlocfilehash: 73e89bcb6ffb6f8c09a0ec53f203b6ed251fd3e4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118650"
---
# <span data-ttu-id="6d1f5-101">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="6d1f5-101">Get-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="6d1f5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6d1f5-102">SYNOPSIS</span></span>
<span data-ttu-id="6d1f5-103">Obter detalhes do tipo de aplicativo Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="6d1f5-103">Get Service Fabric application type details.</span></span> <span data-ttu-id="6d1f5-104">Só é compatível com tipos de aplicativo implantados pelo ARM.</span><span class="sxs-lookup"><span data-stu-id="6d1f5-104">Only supports ARM deployed application types.</span></span>

## <span data-ttu-id="6d1f5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6d1f5-105">SYNTAX</span></span>

### <span data-ttu-id="6d1f5-106">ByResourceGroupAndCluster (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6d1f5-106">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d1f5-107">ByName</span><span class="sxs-lookup"><span data-stu-id="6d1f5-107">ByName</span></span>
```
Get-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d1f5-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6d1f5-108">ByResourceId</span></span>
```
Get-AzServiceFabricApplicationType -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6d1f5-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="6d1f5-109">DESCRIPTION</span></span>
<span data-ttu-id="6d1f5-110">Use este cmdlet para obter os detalhes do tipo de aplicativo no grupo e no cluster de recursos especificados.</span><span class="sxs-lookup"><span data-stu-id="6d1f5-110">Use this cmdlet to get the application type details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="6d1f5-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6d1f5-111">EXAMPLES</span></span>

### <span data-ttu-id="6d1f5-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6d1f5-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Get-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName
```

<span data-ttu-id="6d1f5-113">Este exemplo obterá os detalhes do tipo de aplicativo com os parâmetros especificados, se ele não encontrar o recurso, ele lançará uma exceção.</span><span class="sxs-lookup"><span data-stu-id="6d1f5-113">This example will get the application type details with the parameters specified, if it doesn't find the resource it will throw an exception.</span></span>

### <span data-ttu-id="6d1f5-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="6d1f5-114">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> Get-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName
```

<span data-ttu-id="6d1f5-115">Este exemplo obterá uma lista dos tipos de aplicativo definidos sob o cluster especificado.</span><span class="sxs-lookup"><span data-stu-id="6d1f5-115">This example will get a list of the application types defined under the specified cluster.</span></span>

## <span data-ttu-id="6d1f5-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6d1f5-116">PARAMETERS</span></span>

### <span data-ttu-id="6d1f5-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="6d1f5-117">-ClusterName</span></span>
<span data-ttu-id="6d1f5-118">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="6d1f5-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="6d1f5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d1f5-119">-DefaultProfile</span></span>
<span data-ttu-id="6d1f5-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6d1f5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d1f5-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="6d1f5-121">-Name</span></span>
<span data-ttu-id="6d1f5-122">Especificar o nome do tipo de aplicativo</span><span class="sxs-lookup"><span data-stu-id="6d1f5-122">Specify the name of the application type</span></span>

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

### <span data-ttu-id="6d1f5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d1f5-123">-ResourceGroupName</span></span>
<span data-ttu-id="6d1f5-124">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6d1f5-124">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="6d1f5-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6d1f5-125">-ResourceId</span></span>
<span data-ttu-id="6d1f5-126">Arm ResourceId do tipo de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6d1f5-126">Arm ResourceId of the application type.</span></span>

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

### <span data-ttu-id="6d1f5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d1f5-127">CommonParameters</span></span>
<span data-ttu-id="6d1f5-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d1f5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d1f5-129">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6d1f5-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d1f5-130">Entradas</span><span class="sxs-lookup"><span data-stu-id="6d1f5-130">INPUTS</span></span>

### <span data-ttu-id="6d1f5-131">System.String</span><span class="sxs-lookup"><span data-stu-id="6d1f5-131">System.String</span></span>

## <span data-ttu-id="6d1f5-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="6d1f5-132">OUTPUTS</span></span>

### <span data-ttu-id="6d1f5-133">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span><span class="sxs-lookup"><span data-stu-id="6d1f5-133">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="6d1f5-134">Notas</span><span class="sxs-lookup"><span data-stu-id="6d1f5-134">NOTES</span></span>

## <span data-ttu-id="6d1f5-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6d1f5-135">RELATED LINKS</span></span>
