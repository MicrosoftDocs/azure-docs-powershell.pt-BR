---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricCluster.md
ms.openlocfilehash: 43e2ae9426d80b7762fb8afe7b9c57a53a232f8a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116178"
---
# <span data-ttu-id="1f693-101">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="1f693-101">Get-AzServiceFabricCluster</span></span>

## <span data-ttu-id="1f693-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1f693-102">SYNOPSIS</span></span>
<span data-ttu-id="1f693-103">Obter os detalhes do recurso de cluster.</span><span class="sxs-lookup"><span data-stu-id="1f693-103">Get the cluster resource details.</span></span>

## <span data-ttu-id="1f693-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1f693-104">SYNTAX</span></span>

### <span data-ttu-id="1f693-105">BySubscription (Default)</span><span class="sxs-lookup"><span data-stu-id="1f693-105">BySubscription (Default)</span></span>
```
Get-AzServiceFabricCluster [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f693-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1f693-106">ByResourceGroup</span></span>
```
Get-AzServiceFabricCluster [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1f693-107">ByName</span><span class="sxs-lookup"><span data-stu-id="1f693-107">ByName</span></span>
```
Get-AzServiceFabricCluster [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f693-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="1f693-108">DESCRIPTION</span></span>
<span data-ttu-id="1f693-109">O **Get-AzServiceFabricCluster** receberá os detalhes do recurso de cluster.</span><span class="sxs-lookup"><span data-stu-id="1f693-109">The **Get-AzServiceFabricCluster** will get the cluster resource details.</span></span>

## <span data-ttu-id="1f693-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1f693-110">EXAMPLES</span></span>

### <span data-ttu-id="1f693-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1f693-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceFabricCluster -ResourceGroupName 'Group1' -ClusterName 'Contoso01SFCluster'
```

<span data-ttu-id="1f693-112">Esse comando receberá os detalhes do recurso de cluster para cluster 'myCluster'.</span><span class="sxs-lookup"><span data-stu-id="1f693-112">This command will get the cluster resource details for cluster 'myCluster'.</span></span>

## <span data-ttu-id="1f693-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1f693-113">PARAMETERS</span></span>

### <span data-ttu-id="1f693-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f693-114">-DefaultProfile</span></span>
<span data-ttu-id="1f693-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1f693-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f693-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="1f693-116">-Name</span></span>
<span data-ttu-id="1f693-117">Especificar o nome do cluster</span><span class="sxs-lookup"><span data-stu-id="1f693-117">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="1f693-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f693-118">-ResourceGroupName</span></span>
<span data-ttu-id="1f693-119">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1f693-119">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="1f693-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f693-120">CommonParameters</span></span>
<span data-ttu-id="1f693-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f693-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f693-122">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1f693-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f693-123">Entradas</span><span class="sxs-lookup"><span data-stu-id="1f693-123">INPUTS</span></span>

### <span data-ttu-id="1f693-124">System.String</span><span class="sxs-lookup"><span data-stu-id="1f693-124">System.String</span></span>

## <span data-ttu-id="1f693-125">Saídas</span><span class="sxs-lookup"><span data-stu-id="1f693-125">OUTPUTS</span></span>

### <span data-ttu-id="1f693-126">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="1f693-126">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="1f693-127">Notas</span><span class="sxs-lookup"><span data-stu-id="1f693-127">NOTES</span></span>

## <span data-ttu-id="1f693-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1f693-128">RELATED LINKS</span></span>
