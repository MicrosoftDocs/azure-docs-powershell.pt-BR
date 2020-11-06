---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubquotametric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubQuotaMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubQuotaMetric.md
ms.openlocfilehash: 6d8ea34de1520326ead270ffa44837388729bc5a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596270"
---
# <span data-ttu-id="1ff40-101">Get-AzIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="1ff40-101">Get-AzIotHubQuotaMetric</span></span>

## <span data-ttu-id="1ff40-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1ff40-102">SYNOPSIS</span></span>
<span data-ttu-id="1ff40-103">Obtém as métricas de cota de um IotHub.</span><span class="sxs-lookup"><span data-stu-id="1ff40-103">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="1ff40-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1ff40-104">SYNTAX</span></span>

```
Get-AzIotHubQuotaMetric [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ff40-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1ff40-105">DESCRIPTION</span></span>
<span data-ttu-id="1ff40-106">Obtém as métricas de cota de um IotHub.</span><span class="sxs-lookup"><span data-stu-id="1ff40-106">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="1ff40-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1ff40-107">EXAMPLES</span></span>

### <span data-ttu-id="1ff40-108">Exemplo 1 obter as métricas de cota</span><span class="sxs-lookup"><span data-stu-id="1ff40-108">Example 1 Get the Quota Metrics</span></span>
```
PS C:\> Get-AzIotHubQuotaMetric -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="1ff40-109">Obtém as informações métricas de cota para o IotHub chamado "myiothub"</span><span class="sxs-lookup"><span data-stu-id="1ff40-109">Gets the Quota Metric information for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="1ff40-110">OS</span><span class="sxs-lookup"><span data-stu-id="1ff40-110">PARAMETERS</span></span>

### <span data-ttu-id="1ff40-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ff40-111">-DefaultProfile</span></span>
<span data-ttu-id="1ff40-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="1ff40-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1ff40-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="1ff40-113">-Name</span></span>
<span data-ttu-id="1ff40-114">Nome do Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="1ff40-114">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="1ff40-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ff40-115">-ResourceGroupName</span></span>
<span data-ttu-id="1ff40-116">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="1ff40-116">Resource Group Name</span></span>

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

### <span data-ttu-id="1ff40-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ff40-117">CommonParameters</span></span>
<span data-ttu-id="1ff40-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ff40-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ff40-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ff40-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ff40-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1ff40-120">INPUTS</span></span>

### <span data-ttu-id="1ff40-121">System. String</span><span class="sxs-lookup"><span data-stu-id="1ff40-121">System.String</span></span>

## <span data-ttu-id="1ff40-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1ff40-122">OUTPUTS</span></span>

### <span data-ttu-id="1ff40-123">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="1ff40-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubQuotaMetric</span></span>

## <span data-ttu-id="1ff40-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1ff40-124">NOTES</span></span>

## <span data-ttu-id="1ff40-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1ff40-125">RELATED LINKS</span></span>
