---
external help file: Microsoft.Azure.Commands.Consumption.dll-Help.xml
Module Name: AzureRM.Consumption
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.consumption/get-azurermconsumptionusagedetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Get-AzureRmConsumptionUsageDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Get-AzureRmConsumptionUsageDetail.md
ms.openlocfilehash: 2694ce516b1bb3202fc194e1c1eec55610f7b92a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426756"
---
# <span data-ttu-id="01175-101">Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="01175-101">Get-AzureRmConsumptionUsageDetail</span></span>

## <span data-ttu-id="01175-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="01175-102">SYNOPSIS</span></span>
<span data-ttu-id="01175-103">Obter detalhes de uso da assinatura.</span><span class="sxs-lookup"><span data-stu-id="01175-103">Get usage details of the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01175-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="01175-104">SYNTAX</span></span>

### <span data-ttu-id="01175-105">Assinatura (padrão)</span><span class="sxs-lookup"><span data-stu-id="01175-105">Subscription (Default)</span></span>
```
Get-AzureRmConsumptionUsageDetail [-MaxCount <Int32>] [-IncludeMeterDetails] [-IncludeAdditionalProperties]
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01175-106">Fatura</span><span class="sxs-lookup"><span data-stu-id="01175-106">Invoice</span></span>
```
Get-AzureRmConsumptionUsageDetail -InvoiceName <String> [-MaxCount <Int32>] [-IncludeMeterDetails]
 [-IncludeAdditionalProperties] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01175-107">BillingPeriod</span><span class="sxs-lookup"><span data-stu-id="01175-107">BillingPeriod</span></span>
```
Get-AzureRmConsumptionUsageDetail -BillingPeriodName <String> [-MaxCount <Int32>] [-IncludeMeterDetails]
 [-IncludeAdditionalProperties] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01175-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="01175-108">DESCRIPTION</span></span>
<span data-ttu-id="01175-109">O cmdlet **Get-AzureRmConsumptionUsageDetail** Obtém detalhes de uso da assinatura.</span><span class="sxs-lookup"><span data-stu-id="01175-109">The **Get-AzureRmConsumptionUsageDetail** cmdlet gets usage details of the subscription.</span></span> 

## <span data-ttu-id="01175-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="01175-110">EXAMPLES</span></span>

### <span data-ttu-id="01175-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="01175-111">Example 1</span></span>
```
PS C:\> Get-AzureRmConsumptionUsageDetail -IncludeMeterDetails -InvoiceName 201704-117283130069214
```

<span data-ttu-id="01175-112">Obter detalhes de uso da fatura com o nome especificado e incluir a propriedade MeterDetails no resultado.</span><span class="sxs-lookup"><span data-stu-id="01175-112">Get usage details of the invoice with specified name, and include MeterDetails property in the result.</span></span>

### <span data-ttu-id="01175-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="01175-113">Example 2</span></span>
```
PS C:\> Get-AzureRmConsumptionUsageDetail -IncludeAdditionalProperties -BillingPeriodName 201704-1
```

<span data-ttu-id="01175-114">Obtenha detalhes de uso do período de cobrança com o nome especificado e inclua a propriedade AdditionalProperties no resultado.</span><span class="sxs-lookup"><span data-stu-id="01175-114">Get usage details of the billing period with specified name, and include AdditionalProperties property in the result.</span></span>

### <span data-ttu-id="01175-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="01175-115">Example 3</span></span>
```
PS C:\> Get-AzureRmConsumptionUsageDetail -StartDate 2017-01-17 -EndDate 2017-01-19
```

<span data-ttu-id="01175-116">Obtenha detalhes de uso da assinatura entre 2017-01-17 e 2017-01-19.</span><span class="sxs-lookup"><span data-stu-id="01175-116">Get usage details of the subscription that is between 2017-01-17 to 2017-01-19.</span></span>

## <span data-ttu-id="01175-117">OS</span><span class="sxs-lookup"><span data-stu-id="01175-117">PARAMETERS</span></span>

### <span data-ttu-id="01175-118">-BillingPeriodName</span><span class="sxs-lookup"><span data-stu-id="01175-118">-BillingPeriodName</span></span>
<span data-ttu-id="01175-119">Nome de um período de cobrança específico para obter os detalhes de uso associados.</span><span class="sxs-lookup"><span data-stu-id="01175-119">Name of a specific billing period to get the usage details that associate with.</span></span>

```yaml
Type: String
Parameter Sets: BillingPeriod
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01175-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01175-120">-DefaultProfile</span></span>
<span data-ttu-id="01175-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="01175-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01175-122">-EndDate</span><span class="sxs-lookup"><span data-stu-id="01175-122">-EndDate</span></span>
<span data-ttu-id="01175-123">A data de término (em UTC) dos usos.</span><span class="sxs-lookup"><span data-stu-id="01175-123">The end date (in UTC) of the usages.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01175-124">-IncludeAdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="01175-124">-IncludeAdditionalProperties</span></span>
<span data-ttu-id="01175-125">Inclua propriedades adicionais nos usos.</span><span class="sxs-lookup"><span data-stu-id="01175-125">Include additional properties in the usages.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01175-126">-IncludeMeterDetails</span><span class="sxs-lookup"><span data-stu-id="01175-126">-IncludeMeterDetails</span></span>
<span data-ttu-id="01175-127">Inclua detalhes do medidor nos usos.</span><span class="sxs-lookup"><span data-stu-id="01175-127">Include meter details in the usages.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01175-128">-Faturaname</span><span class="sxs-lookup"><span data-stu-id="01175-128">-InvoiceName</span></span>
<span data-ttu-id="01175-129">Nome de uma fatura específica para obter os detalhes de uso associados.</span><span class="sxs-lookup"><span data-stu-id="01175-129">Name of a specific invoice to get the usage details that associate with.</span></span>

```yaml
Type: String
Parameter Sets: Invoice
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01175-130">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="01175-130">-MaxCount</span></span>
<span data-ttu-id="01175-131">Determine o número máximo de registros a serem retornados.</span><span class="sxs-lookup"><span data-stu-id="01175-131">Determine the maximum number of records to return.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01175-132">-StartDate</span><span class="sxs-lookup"><span data-stu-id="01175-132">-StartDate</span></span>
<span data-ttu-id="01175-133">A data de início (em UTC) dos usos.</span><span class="sxs-lookup"><span data-stu-id="01175-133">The start date (in UTC) of the usages.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01175-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01175-134">CommonParameters</span></span>
<span data-ttu-id="01175-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01175-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01175-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01175-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01175-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="01175-137">INPUTS</span></span>

### <span data-ttu-id="01175-138">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="01175-138">None</span></span>

## <span data-ttu-id="01175-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="01175-139">OUTPUTS</span></span>

### <span data-ttu-id="01175-140">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. consumo. Models. PSUsageDetail, Microsoft. Azure. Commands. consumo, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="01175-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Consumption.Models.PSUsageDetail, Microsoft.Azure.Commands.Consumption, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="01175-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="01175-141">NOTES</span></span>

## <span data-ttu-id="01175-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="01175-142">RELATED LINKS</span></span>

