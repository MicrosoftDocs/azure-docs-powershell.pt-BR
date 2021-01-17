---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubquotametric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubQuotaMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubQuotaMetric.md
ms.openlocfilehash: 1f3fc05a71ec0d7c6f4926f47f6ab862af42b9e7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433726"
---
# <span data-ttu-id="d1328-101">Get-AzIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="d1328-101">Get-AzIotHubQuotaMetric</span></span>

## <span data-ttu-id="d1328-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d1328-102">SYNOPSIS</span></span>
<span data-ttu-id="d1328-103">Obtém as métricas de cota de um IotHub.</span><span class="sxs-lookup"><span data-stu-id="d1328-103">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="d1328-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d1328-104">SYNTAX</span></span>

```
Get-AzIotHubQuotaMetric [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1328-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d1328-105">DESCRIPTION</span></span>
<span data-ttu-id="d1328-106">Obtém as métricas de cota de um IotHub.</span><span class="sxs-lookup"><span data-stu-id="d1328-106">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="d1328-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d1328-107">EXAMPLES</span></span>

### <span data-ttu-id="d1328-108">Exemplo 1 obter as métricas de cota</span><span class="sxs-lookup"><span data-stu-id="d1328-108">Example 1 Get the Quota Metrics</span></span>
```
PS C:\> Get-AzIotHubQuotaMetric -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="d1328-109">Obtém as informações métricas de cota para o IotHub chamado "myiothub"</span><span class="sxs-lookup"><span data-stu-id="d1328-109">Gets the Quota Metric information for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="d1328-110">OS</span><span class="sxs-lookup"><span data-stu-id="d1328-110">PARAMETERS</span></span>

### <span data-ttu-id="d1328-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1328-111">-DefaultProfile</span></span>
<span data-ttu-id="d1328-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="d1328-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d1328-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="d1328-113">-Name</span></span>
<span data-ttu-id="d1328-114">Nome do Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="d1328-114">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="d1328-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1328-115">-ResourceGroupName</span></span>
<span data-ttu-id="d1328-116">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="d1328-116">Resource Group Name</span></span>

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

### <span data-ttu-id="d1328-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1328-117">CommonParameters</span></span>
<span data-ttu-id="d1328-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1328-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1328-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1328-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1328-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d1328-120">INPUTS</span></span>

### <span data-ttu-id="d1328-121">System. String</span><span class="sxs-lookup"><span data-stu-id="d1328-121">System.String</span></span>

## <span data-ttu-id="d1328-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d1328-122">OUTPUTS</span></span>

### <span data-ttu-id="d1328-123">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="d1328-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubQuotaMetric</span></span>

## <span data-ttu-id="d1328-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d1328-124">NOTES</span></span>

## <span data-ttu-id="d1328-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d1328-125">RELATED LINKS</span></span>
