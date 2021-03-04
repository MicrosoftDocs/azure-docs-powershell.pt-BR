---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubquotametric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubQuotaMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubQuotaMetric.md
ms.openlocfilehash: 70e63723bd9647f003082813cd680a84ae5638c5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889939"
---
# <span data-ttu-id="9874d-101">Get-AzIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="9874d-101">Get-AzIotHubQuotaMetric</span></span>

## <span data-ttu-id="9874d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9874d-102">SYNOPSIS</span></span>
<span data-ttu-id="9874d-103">Obtém as Métricas de Cota para um IotHub.</span><span class="sxs-lookup"><span data-stu-id="9874d-103">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="9874d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="9874d-104">SYNTAX</span></span>

```
Get-AzIotHubQuotaMetric [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9874d-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="9874d-105">DESCRIPTION</span></span>
<span data-ttu-id="9874d-106">Obtém as Métricas de Cota para um IotHub.</span><span class="sxs-lookup"><span data-stu-id="9874d-106">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="9874d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9874d-107">EXAMPLES</span></span>

### <span data-ttu-id="9874d-108">Exemplo 1 Obter as Métricas de Cota</span><span class="sxs-lookup"><span data-stu-id="9874d-108">Example 1 Get the Quota Metrics</span></span>
```
PS C:\> Get-AzIotHubQuotaMetric -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="9874d-109">Obtém as informações da Métrica de Cota para o IotHub chamado "myiothub"</span><span class="sxs-lookup"><span data-stu-id="9874d-109">Gets the Quota Metric information for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="9874d-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="9874d-110">PARAMETERS</span></span>

### <span data-ttu-id="9874d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9874d-111">-DefaultProfile</span></span>
<span data-ttu-id="9874d-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="9874d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9874d-113">-Name</span><span class="sxs-lookup"><span data-stu-id="9874d-113">-Name</span></span>
<span data-ttu-id="9874d-114">Nome do hub de IoT.</span><span class="sxs-lookup"><span data-stu-id="9874d-114">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="9874d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9874d-115">-ResourceGroupName</span></span>
<span data-ttu-id="9874d-116">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="9874d-116">Resource Group Name</span></span>

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

### <span data-ttu-id="9874d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9874d-117">CommonParameters</span></span>
<span data-ttu-id="9874d-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9874d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9874d-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9874d-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9874d-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9874d-120">INPUTS</span></span>

### <span data-ttu-id="9874d-121">System.String</span><span class="sxs-lookup"><span data-stu-id="9874d-121">System.String</span></span>

## <span data-ttu-id="9874d-122">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="9874d-122">OUTPUTS</span></span>

### <span data-ttu-id="9874d-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="9874d-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubQuotaMetric</span></span>

## <span data-ttu-id="9874d-124">NOTES</span><span class="sxs-lookup"><span data-stu-id="9874d-124">NOTES</span></span>

## <span data-ttu-id="9874d-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9874d-125">RELATED LINKS</span></span>
