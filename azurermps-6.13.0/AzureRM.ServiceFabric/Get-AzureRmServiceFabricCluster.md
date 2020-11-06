---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/get-azurermservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Get-AzureRmServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Get-AzureRmServiceFabricCluster.md
ms.openlocfilehash: 93240fe3deddbe5b6f8fb20d644a0e685cfdda11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432730"
---
# <span data-ttu-id="c1bf6-101">Get-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="c1bf6-101">Get-AzureRmServiceFabricCluster</span></span>

## <span data-ttu-id="c1bf6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c1bf6-102">SYNOPSIS</span></span>
<span data-ttu-id="c1bf6-103">Obter os detalhes do recurso de cluster.</span><span class="sxs-lookup"><span data-stu-id="c1bf6-103">Get the cluster resource details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1bf6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c1bf6-104">SYNTAX</span></span>

### <span data-ttu-id="c1bf6-105">BySubscription (padrão)</span><span class="sxs-lookup"><span data-stu-id="c1bf6-105">BySubscription (Default)</span></span>
```
Get-AzureRmServiceFabricCluster [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1bf6-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c1bf6-106">ByResourceGroup</span></span>
```
Get-AzureRmServiceFabricCluster [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c1bf6-107">ByName</span><span class="sxs-lookup"><span data-stu-id="c1bf6-107">ByName</span></span>
```
Get-AzureRmServiceFabricCluster [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1bf6-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c1bf6-108">DESCRIPTION</span></span>
<span data-ttu-id="c1bf6-109">O **Get-AzureRmServiceFabricCluster** receberá os detalhes do recurso de cluster.</span><span class="sxs-lookup"><span data-stu-id="c1bf6-109">The **Get-AzureRmServiceFabricCluster** will get the cluster resource details.</span></span>

## <span data-ttu-id="c1bf6-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c1bf6-110">EXAMPLES</span></span>

### <span data-ttu-id="c1bf6-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c1bf6-111">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceFabricCluster -ResourceGroupName 'Group1' -ClusterName 'Contoso01SFCluster'
```

<span data-ttu-id="c1bf6-112">Esse comando receberá os detalhes do recurso de cluster do cluster ' mycluster '.</span><span class="sxs-lookup"><span data-stu-id="c1bf6-112">This command will get the cluster resource details for cluster 'myCluster'.</span></span>

## <span data-ttu-id="c1bf6-113">OS</span><span class="sxs-lookup"><span data-stu-id="c1bf6-113">PARAMETERS</span></span>

### <span data-ttu-id="c1bf6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1bf6-114">-DefaultProfile</span></span>
<span data-ttu-id="c1bf6-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c1bf6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1bf6-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="c1bf6-116">-Name</span></span>
<span data-ttu-id="c1bf6-117">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="c1bf6-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="c1bf6-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1bf6-118">-ResourceGroupName</span></span>
<span data-ttu-id="c1bf6-119">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c1bf6-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="c1bf6-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1bf6-120">CommonParameters</span></span>
<span data-ttu-id="c1bf6-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1bf6-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1bf6-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1bf6-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1bf6-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c1bf6-123">INPUTS</span></span>

### <span data-ttu-id="c1bf6-124">System. String</span><span class="sxs-lookup"><span data-stu-id="c1bf6-124">System.String</span></span>

## <span data-ttu-id="c1bf6-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c1bf6-125">OUTPUTS</span></span>

### <span data-ttu-id="c1bf6-126">Microsoft. Azure. Commands. imfabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="c1bf6-126">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="c1bf6-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c1bf6-127">NOTES</span></span>

## <span data-ttu-id="c1bf6-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c1bf6-128">RELATED LINKS</span></span>
