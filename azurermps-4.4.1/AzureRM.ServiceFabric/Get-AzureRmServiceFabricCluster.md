---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Get-AzureRmServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Get-AzureRmServiceFabricCluster.md
ms.openlocfilehash: 645981bb7b2cb02a4bb54a03ccbb570ec31925dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440946"
---
# <span data-ttu-id="bfee3-101">Get-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="bfee3-101">Get-AzureRmServiceFabricCluster</span></span>

## <span data-ttu-id="bfee3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bfee3-102">SYNOPSIS</span></span>
<span data-ttu-id="bfee3-103">Obter os detalhes do recurso de cluster.</span><span class="sxs-lookup"><span data-stu-id="bfee3-103">Get the cluster resource details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bfee3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bfee3-104">SYNTAX</span></span>

```
Get-AzureRmServiceFabricCluster [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bfee3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bfee3-105">DESCRIPTION</span></span>
<span data-ttu-id="bfee3-106">O **Add-AzureRmServiceFabricCluster** receberá os detalhes do recurso de cluster.</span><span class="sxs-lookup"><span data-stu-id="bfee3-106">The **Add-AzureRmServiceFabricCluster** will get the cluster resource details.</span></span>

## <span data-ttu-id="bfee3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bfee3-107">EXAMPLES</span></span>

### <span data-ttu-id="bfee3-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bfee3-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceFabricCluster -ResourceGroupName 'Group1' -ClusterName 'Contoso01SFCluster'
```

<span data-ttu-id="bfee3-109">Esse comando receberá os detalhes do recurso de cluster do cluster ' mycluster '.</span><span class="sxs-lookup"><span data-stu-id="bfee3-109">This command will get the cluster resource details for cluster 'myCluster'.</span></span>

## <span data-ttu-id="bfee3-110">OS</span><span class="sxs-lookup"><span data-stu-id="bfee3-110">PARAMETERS</span></span>

### <span data-ttu-id="bfee3-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="bfee3-111">-Name</span></span>
<span data-ttu-id="bfee3-112">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="bfee3-112">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfee3-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfee3-113">-ResourceGroupName</span></span>
<span data-ttu-id="bfee3-114">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bfee3-114">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfee3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfee3-115">-DefaultProfile</span></span>
<span data-ttu-id="bfee3-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bfee3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bfee3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfee3-117">CommonParameters</span></span>
<span data-ttu-id="bfee3-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfee3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfee3-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfee3-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfee3-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bfee3-120">INPUTS</span></span>

### <span data-ttu-id="bfee3-121">System. String</span><span class="sxs-lookup"><span data-stu-id="bfee3-121">System.String</span></span>

## <span data-ttu-id="bfee3-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bfee3-122">OUTPUTS</span></span>

### <span data-ttu-id="bfee3-123">System. Collections. Generic. IList ' 1 [[Microsoft. Azure. Commands. createfabric. Models. PsCluster, Microsoft. Azure. Commands. Fabric, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="bfee3-123">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster, Microsoft.Azure.Commands.ServiceFabric, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="bfee3-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bfee3-124">NOTES</span></span>

## <span data-ttu-id="bfee3-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bfee3-125">RELATED LINKS</span></span>

