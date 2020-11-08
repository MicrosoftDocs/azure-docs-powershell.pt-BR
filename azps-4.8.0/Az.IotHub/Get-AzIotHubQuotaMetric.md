---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubquotametric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubQuotaMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubQuotaMetric.md
ms.openlocfilehash: 1f3fc05a71ec0d7c6f4926f47f6ab862af42b9e7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111962"
---
# <span data-ttu-id="9518a-101">Get-AzIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="9518a-101">Get-AzIotHubQuotaMetric</span></span>

## <span data-ttu-id="9518a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9518a-102">SYNOPSIS</span></span>
<span data-ttu-id="9518a-103">Obtém as métricas de cota de um IotHub.</span><span class="sxs-lookup"><span data-stu-id="9518a-103">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="9518a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9518a-104">SYNTAX</span></span>

```
Get-AzIotHubQuotaMetric [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9518a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9518a-105">DESCRIPTION</span></span>
<span data-ttu-id="9518a-106">Obtém as métricas de cota de um IotHub.</span><span class="sxs-lookup"><span data-stu-id="9518a-106">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="9518a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9518a-107">EXAMPLES</span></span>

### <span data-ttu-id="9518a-108">Exemplo 1 obter as métricas de cota</span><span class="sxs-lookup"><span data-stu-id="9518a-108">Example 1 Get the Quota Metrics</span></span>
```
PS C:\> Get-AzIotHubQuotaMetric -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="9518a-109">Obtém as informações métricas de cota para o IotHub chamado "myiothub"</span><span class="sxs-lookup"><span data-stu-id="9518a-109">Gets the Quota Metric information for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="9518a-110">OS</span><span class="sxs-lookup"><span data-stu-id="9518a-110">PARAMETERS</span></span>

### <span data-ttu-id="9518a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9518a-111">-DefaultProfile</span></span>
<span data-ttu-id="9518a-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="9518a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9518a-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="9518a-113">-Name</span></span>
<span data-ttu-id="9518a-114">Nome do Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="9518a-114">Name of the IoT hub.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9518a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9518a-115">-ResourceGroupName</span></span>
<span data-ttu-id="9518a-116">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="9518a-116">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9518a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9518a-117">CommonParameters</span></span>
<span data-ttu-id="9518a-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9518a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9518a-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9518a-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9518a-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9518a-120">INPUTS</span></span>

### <span data-ttu-id="9518a-121">System. String</span><span class="sxs-lookup"><span data-stu-id="9518a-121">System.String</span></span>

## <span data-ttu-id="9518a-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9518a-122">OUTPUTS</span></span>

### <span data-ttu-id="9518a-123">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="9518a-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubQuotaMetric</span></span>

## <span data-ttu-id="9518a-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9518a-124">NOTES</span></span>

## <span data-ttu-id="9518a-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9518a-125">RELATED LINKS</span></span>
