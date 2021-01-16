---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubquotametric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubQuotaMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubQuotaMetric.md
ms.openlocfilehash: 1f3fc05a71ec0d7c6f4926f47f6ab862af42b9e7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263061"
---
# <span data-ttu-id="f53dc-101">Get-AzIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="f53dc-101">Get-AzIotHubQuotaMetric</span></span>

## <span data-ttu-id="f53dc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f53dc-102">SYNOPSIS</span></span>
<span data-ttu-id="f53dc-103">Obtém as métricas de cota de um IotHub.</span><span class="sxs-lookup"><span data-stu-id="f53dc-103">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="f53dc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f53dc-104">SYNTAX</span></span>

```
Get-AzIotHubQuotaMetric [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f53dc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f53dc-105">DESCRIPTION</span></span>
<span data-ttu-id="f53dc-106">Obtém as métricas de cota de um IotHub.</span><span class="sxs-lookup"><span data-stu-id="f53dc-106">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="f53dc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f53dc-107">EXAMPLES</span></span>

### <span data-ttu-id="f53dc-108">Exemplo 1 obter as métricas de cota</span><span class="sxs-lookup"><span data-stu-id="f53dc-108">Example 1 Get the Quota Metrics</span></span>
```
PS C:\> Get-AzIotHubQuotaMetric -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="f53dc-109">Obtém as informações métricas de cota para o IotHub chamado "myiothub"</span><span class="sxs-lookup"><span data-stu-id="f53dc-109">Gets the Quota Metric information for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="f53dc-110">OS</span><span class="sxs-lookup"><span data-stu-id="f53dc-110">PARAMETERS</span></span>

### <span data-ttu-id="f53dc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f53dc-111">-DefaultProfile</span></span>
<span data-ttu-id="f53dc-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="f53dc-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f53dc-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="f53dc-113">-Name</span></span>
<span data-ttu-id="f53dc-114">Nome do Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="f53dc-114">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="f53dc-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f53dc-115">-ResourceGroupName</span></span>
<span data-ttu-id="f53dc-116">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="f53dc-116">Resource Group Name</span></span>

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

### <span data-ttu-id="f53dc-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f53dc-117">CommonParameters</span></span>
<span data-ttu-id="f53dc-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f53dc-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f53dc-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f53dc-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f53dc-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f53dc-120">INPUTS</span></span>

### <span data-ttu-id="f53dc-121">System. String</span><span class="sxs-lookup"><span data-stu-id="f53dc-121">System.String</span></span>

## <span data-ttu-id="f53dc-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f53dc-122">OUTPUTS</span></span>

### <span data-ttu-id="f53dc-123">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="f53dc-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubQuotaMetric</span></span>

## <span data-ttu-id="f53dc-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f53dc-124">NOTES</span></span>

## <span data-ttu-id="f53dc-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f53dc-125">RELATED LINKS</span></span>
