---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricCluster.md
ms.openlocfilehash: 43e2ae9426d80b7762fb8afe7b9c57a53a232f8a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433057"
---
# <span data-ttu-id="17980-101">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="17980-101">Get-AzServiceFabricCluster</span></span>

## <span data-ttu-id="17980-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="17980-102">SYNOPSIS</span></span>
<span data-ttu-id="17980-103">Obter os detalhes do recurso de cluster.</span><span class="sxs-lookup"><span data-stu-id="17980-103">Get the cluster resource details.</span></span>

## <span data-ttu-id="17980-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="17980-104">SYNTAX</span></span>

### <span data-ttu-id="17980-105">BySubscription (padrão)</span><span class="sxs-lookup"><span data-stu-id="17980-105">BySubscription (Default)</span></span>
```
Get-AzServiceFabricCluster [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17980-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="17980-106">ByResourceGroup</span></span>
```
Get-AzServiceFabricCluster [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="17980-107">ByName</span><span class="sxs-lookup"><span data-stu-id="17980-107">ByName</span></span>
```
Get-AzServiceFabricCluster [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17980-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="17980-108">DESCRIPTION</span></span>
<span data-ttu-id="17980-109">O **Get-AzServiceFabricCluster** receberá os detalhes do recurso de cluster.</span><span class="sxs-lookup"><span data-stu-id="17980-109">The **Get-AzServiceFabricCluster** will get the cluster resource details.</span></span>

## <span data-ttu-id="17980-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="17980-110">EXAMPLES</span></span>

### <span data-ttu-id="17980-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="17980-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceFabricCluster -ResourceGroupName 'Group1' -ClusterName 'Contoso01SFCluster'
```

<span data-ttu-id="17980-112">Esse comando receberá os detalhes do recurso de cluster do cluster ' mycluster '.</span><span class="sxs-lookup"><span data-stu-id="17980-112">This command will get the cluster resource details for cluster 'myCluster'.</span></span>

## <span data-ttu-id="17980-113">OS</span><span class="sxs-lookup"><span data-stu-id="17980-113">PARAMETERS</span></span>

### <span data-ttu-id="17980-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17980-114">-DefaultProfile</span></span>
<span data-ttu-id="17980-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="17980-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17980-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="17980-116">-Name</span></span>
<span data-ttu-id="17980-117">Especificar o nome do cluster</span><span class="sxs-lookup"><span data-stu-id="17980-117">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="17980-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17980-118">-ResourceGroupName</span></span>
<span data-ttu-id="17980-119">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="17980-119">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="17980-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17980-120">CommonParameters</span></span>
<span data-ttu-id="17980-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17980-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17980-122">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="17980-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17980-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="17980-123">INPUTS</span></span>

### <span data-ttu-id="17980-124">System. String</span><span class="sxs-lookup"><span data-stu-id="17980-124">System.String</span></span>

## <span data-ttu-id="17980-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="17980-125">OUTPUTS</span></span>

### <span data-ttu-id="17980-126">Microsoft. Azure. Commands. imfabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="17980-126">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="17980-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="17980-127">NOTES</span></span>

## <span data-ttu-id="17980-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="17980-128">RELATED LINKS</span></span>
