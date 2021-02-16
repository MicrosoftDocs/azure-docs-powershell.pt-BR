---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: 7dc8ca2302b00b5eb200c30aed104f5fe5ff8642
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118646"
---
# <span data-ttu-id="5b152-101">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="5b152-101">Get-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="5b152-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5b152-102">SYNOPSIS</span></span>
<span data-ttu-id="5b152-103">Obter detalhes da versão do tipo de aplicativo Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="5b152-103">Get Service Fabric application type version details.</span></span> <span data-ttu-id="5b152-104">Só dá suporte a versões de tipo de aplicativo implantada pelo ARM.</span><span class="sxs-lookup"><span data-stu-id="5b152-104">Only supports ARM deployed application type versions.</span></span>

## <span data-ttu-id="5b152-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5b152-105">SYNTAX</span></span>

### <span data-ttu-id="5b152-106">ByResourceGroupAndCluster (Padrão)</span><span class="sxs-lookup"><span data-stu-id="5b152-106">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b152-107">ByVersion</span><span class="sxs-lookup"><span data-stu-id="5b152-107">ByVersion</span></span>
```
Get-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-Version] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b152-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5b152-108">ByResourceId</span></span>
```
Get-AzServiceFabricApplicationTypeVersion -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5b152-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="5b152-109">DESCRIPTION</span></span>
<span data-ttu-id="5b152-110">Use este cmdlet para obter os detalhes da versão do tipo de aplicativo no grupo e no cluster de recursos especificados.</span><span class="sxs-lookup"><span data-stu-id="5b152-110">Use this cmdlet to get the application type version details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="5b152-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5b152-111">EXAMPLES</span></span>

### <span data-ttu-id="5b152-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5b152-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $appTypeName = "v1"
PS C:\> Get-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version
```

<span data-ttu-id="5b152-113">Este exemplo obtém o tipo de aplicativo "testAppType" com a versão "v1", se ele não encontrar o recurso, ele lançará uma exceção.</span><span class="sxs-lookup"><span data-stu-id="5b152-113">This example gets the application type "testAppType" with version "v1", if it doesn't find the resource it will throw an exception.</span></span>

### <span data-ttu-id="5b152-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="5b152-114">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Get-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName
```

<span data-ttu-id="5b152-115">Este exemplo obtém uma lista das versões de tipo de aplicativo definidas sob o cluster e o tipo especificados.</span><span class="sxs-lookup"><span data-stu-id="5b152-115">This example gets a list of the application type versions defined under the specified cluster and type.</span></span>

## <span data-ttu-id="5b152-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5b152-116">PARAMETERS</span></span>

### <span data-ttu-id="5b152-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="5b152-117">-ClusterName</span></span>
<span data-ttu-id="5b152-118">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="5b152-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="5b152-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b152-119">-DefaultProfile</span></span>
<span data-ttu-id="5b152-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5b152-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b152-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="5b152-121">-Name</span></span>
<span data-ttu-id="5b152-122">Especifique o nome do tipo de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5b152-122">Specify the name of the application type.</span></span>

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

### <span data-ttu-id="5b152-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b152-123">-ResourceGroupName</span></span>
<span data-ttu-id="5b152-124">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5b152-124">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="5b152-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b152-125">-ResourceId</span></span>
<span data-ttu-id="5b152-126">Arm ResourceId da versão do tipo de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5b152-126">Arm ResourceId of the application type version.</span></span>

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

### <span data-ttu-id="5b152-127">-Versão</span><span class="sxs-lookup"><span data-stu-id="5b152-127">-Version</span></span>
<span data-ttu-id="5b152-128">Especifique a versão do tipo de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5b152-128">Specify the version of the application type.</span></span>

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

### <span data-ttu-id="5b152-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b152-129">CommonParameters</span></span>
<span data-ttu-id="5b152-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b152-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b152-131">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5b152-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b152-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="5b152-132">INPUTS</span></span>

### <span data-ttu-id="5b152-133">System.String</span><span class="sxs-lookup"><span data-stu-id="5b152-133">System.String</span></span>

## <span data-ttu-id="5b152-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="5b152-134">OUTPUTS</span></span>

### <span data-ttu-id="5b152-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="5b152-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="5b152-136">Notas</span><span class="sxs-lookup"><span data-stu-id="5b152-136">NOTES</span></span>

## <span data-ttu-id="5b152-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5b152-137">RELATED LINKS</span></span>
