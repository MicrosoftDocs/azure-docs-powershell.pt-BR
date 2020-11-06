---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubQuotaMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubQuotaMetric.md
ms.openlocfilehash: f0a3b446c6d40ff07efc35ca51cdf7f422491f33
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433113"
---
# <span data-ttu-id="b51bc-101">Get-AzureRmIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="b51bc-101">Get-AzureRmIotHubQuotaMetric</span></span>

## <span data-ttu-id="b51bc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b51bc-102">SYNOPSIS</span></span>
<span data-ttu-id="b51bc-103">Obtém as métricas de cota de um IotHub.</span><span class="sxs-lookup"><span data-stu-id="b51bc-103">Gets the Quota Metrics for an IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b51bc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b51bc-104">SYNTAX</span></span>

```
Get-AzureRmIotHubQuotaMetric [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b51bc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b51bc-105">DESCRIPTION</span></span>
<span data-ttu-id="b51bc-106">Obtém as métricas de cota de um IotHub.</span><span class="sxs-lookup"><span data-stu-id="b51bc-106">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="b51bc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b51bc-107">EXAMPLES</span></span>

### <span data-ttu-id="b51bc-108">Exemplo 1 obter as métricas de cota</span><span class="sxs-lookup"><span data-stu-id="b51bc-108">Example 1 Get the Quota Metrics</span></span>
```
PS C:\> Get-AzureRmIotHubQuotaMetric -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="b51bc-109">Obtém as informações métricas de cota para o IotHub chamado "myiothub"</span><span class="sxs-lookup"><span data-stu-id="b51bc-109">Gets the Quota Metric information for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="b51bc-110">OS</span><span class="sxs-lookup"><span data-stu-id="b51bc-110">PARAMETERS</span></span>

### <span data-ttu-id="b51bc-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="b51bc-111">-Name</span></span>
<span data-ttu-id="b51bc-112">Nome do Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="b51bc-112">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="b51bc-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b51bc-113">-ResourceGroupName</span></span>
<span data-ttu-id="b51bc-114">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="b51bc-114">Resource Group Name</span></span>

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

### <span data-ttu-id="b51bc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b51bc-115">-DefaultProfile</span></span>
<span data-ttu-id="b51bc-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b51bc-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b51bc-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b51bc-117">CommonParameters</span></span>
<span data-ttu-id="b51bc-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b51bc-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b51bc-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b51bc-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b51bc-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b51bc-120">INPUTS</span></span>

### <span data-ttu-id="b51bc-121">System. String</span><span class="sxs-lookup"><span data-stu-id="b51bc-121">System.String</span></span>

## <span data-ttu-id="b51bc-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b51bc-122">OUTPUTS</span></span>

### <span data-ttu-id="b51bc-123">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubQuotaMetric, Microsoft. Azure. Commands. IotHub, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="b51bc-123">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubQuotaMetric, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="b51bc-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b51bc-124">NOTES</span></span>

## <span data-ttu-id="b51bc-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b51bc-125">RELATED LINKS</span></span>

