---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubquotametric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubQuotaMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubQuotaMetric.md
ms.openlocfilehash: 1de2d49d6e914635f8fc0d38ffa81755cc622481
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610334"
---
# <span data-ttu-id="edbf6-101">Get-AzureRmIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="edbf6-101">Get-AzureRmIotHubQuotaMetric</span></span>

## <span data-ttu-id="edbf6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="edbf6-102">SYNOPSIS</span></span>
<span data-ttu-id="edbf6-103">Obtém as métricas de cota de um IotHub.</span><span class="sxs-lookup"><span data-stu-id="edbf6-103">Gets the Quota Metrics for an IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="edbf6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="edbf6-104">SYNTAX</span></span>

```
Get-AzureRmIotHubQuotaMetric [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="edbf6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="edbf6-105">DESCRIPTION</span></span>
<span data-ttu-id="edbf6-106">Obtém as métricas de cota de um IotHub.</span><span class="sxs-lookup"><span data-stu-id="edbf6-106">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="edbf6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="edbf6-107">EXAMPLES</span></span>

### <span data-ttu-id="edbf6-108">Exemplo 1 obter as métricas de cota</span><span class="sxs-lookup"><span data-stu-id="edbf6-108">Example 1 Get the Quota Metrics</span></span>
```
PS C:\> Get-AzureRmIotHubQuotaMetric -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="edbf6-109">Obtém as informações métricas de cota para o IotHub chamado "myiothub"</span><span class="sxs-lookup"><span data-stu-id="edbf6-109">Gets the Quota Metric information for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="edbf6-110">OS</span><span class="sxs-lookup"><span data-stu-id="edbf6-110">PARAMETERS</span></span>

### <span data-ttu-id="edbf6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edbf6-111">-DefaultProfile</span></span>
<span data-ttu-id="edbf6-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="edbf6-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="edbf6-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="edbf6-113">-Name</span></span>
<span data-ttu-id="edbf6-114">Nome do Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="edbf6-114">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="edbf6-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edbf6-115">-ResourceGroupName</span></span>
<span data-ttu-id="edbf6-116">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="edbf6-116">Resource Group Name</span></span>

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

### <span data-ttu-id="edbf6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edbf6-117">CommonParameters</span></span>
<span data-ttu-id="edbf6-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edbf6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edbf6-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="edbf6-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edbf6-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="edbf6-120">INPUTS</span></span>

### <span data-ttu-id="edbf6-121">System. String</span><span class="sxs-lookup"><span data-stu-id="edbf6-121">System.String</span></span>

## <span data-ttu-id="edbf6-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="edbf6-122">OUTPUTS</span></span>

### <span data-ttu-id="edbf6-123">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="edbf6-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubQuotaMetric</span></span>

## <span data-ttu-id="edbf6-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="edbf6-124">NOTES</span></span>

## <span data-ttu-id="edbf6-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="edbf6-125">RELATED LINKS</span></span>
