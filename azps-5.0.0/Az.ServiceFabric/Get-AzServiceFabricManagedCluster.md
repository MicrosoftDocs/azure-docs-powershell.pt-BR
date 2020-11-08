---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedCluster.md
ms.openlocfilehash: c81199bb78a64ac2ed32a21e0f3822093a2b2b14
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94117531"
---
# <span data-ttu-id="aa054-101">Get-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="aa054-101">Get-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="aa054-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="aa054-102">SYNOPSIS</span></span>
<span data-ttu-id="aa054-103">Obter os detalhes do recurso de cluster gerenciado.</span><span class="sxs-lookup"><span data-stu-id="aa054-103">Get the managed cluster resource details.</span></span>

## <span data-ttu-id="aa054-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aa054-104">SYNTAX</span></span>

### <span data-ttu-id="aa054-105">BySubscription (padrão)</span><span class="sxs-lookup"><span data-stu-id="aa054-105">BySubscription (Default)</span></span>
```
Get-AzServiceFabricManagedCluster [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aa054-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="aa054-106">ByResourceGroup</span></span>
```
Get-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="aa054-107">ByName</span><span class="sxs-lookup"><span data-stu-id="aa054-107">ByName</span></span>
```
Get-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa054-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="aa054-108">DESCRIPTION</span></span>
<span data-ttu-id="aa054-109">Obter os detalhes do recurso de cluster gerenciado.</span><span class="sxs-lookup"><span data-stu-id="aa054-109">Get the managed cluster resource details.</span></span>

## <span data-ttu-id="aa054-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="aa054-110">EXAMPLES</span></span>

### <span data-ttu-id="aa054-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="aa054-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName
```

<span data-ttu-id="aa054-112">Obter detalhes do cluster.</span><span class="sxs-lookup"><span data-stu-id="aa054-112">Get cluster details.</span></span>

### <span data-ttu-id="aa054-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="aa054-113">Example 2</span></span>
```powershell
$rgName = "testRG"
Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName
```

<span data-ttu-id="aa054-114">Obter lista de clusters no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="aa054-114">Get list of clusters under the specified resource group.</span></span>

### <span data-ttu-id="aa054-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="aa054-115">Example 3</span></span>
```powershell
Get-AzServiceFabricManagedCluster
```

<span data-ttu-id="aa054-116">Obter lista de clusters na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="aa054-116">Get list of clusters under the current subscription.</span></span>

## <span data-ttu-id="aa054-117">OS</span><span class="sxs-lookup"><span data-stu-id="aa054-117">PARAMETERS</span></span>

### <span data-ttu-id="aa054-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa054-118">-DefaultProfile</span></span>
<span data-ttu-id="aa054-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="aa054-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa054-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="aa054-120">-Name</span></span>
<span data-ttu-id="aa054-121">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="aa054-121">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa054-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa054-122">-ResourceGroupName</span></span>
<span data-ttu-id="aa054-123">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="aa054-123">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa054-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa054-124">CommonParameters</span></span>
<span data-ttu-id="aa054-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa054-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa054-126">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aa054-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa054-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="aa054-127">INPUTS</span></span>

### <span data-ttu-id="aa054-128">System. String</span><span class="sxs-lookup"><span data-stu-id="aa054-128">System.String</span></span>

## <span data-ttu-id="aa054-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="aa054-129">OUTPUTS</span></span>

### <span data-ttu-id="aa054-130">Microsoft. Azure. Commands. imfabric. Models. PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="aa054-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="aa054-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="aa054-131">NOTES</span></span>

## <span data-ttu-id="aa054-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aa054-132">RELATED LINKS</span></span>
