---
external help file: Microsoft.Azure.Commands.Consumption.dll-Help.xml
Module Name: AzureRM.Consumption
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Get-AzureRmConsumptionUsageDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Get-AzureRmConsumptionUsageDetail.md
ms.openlocfilehash: f8347fca355080f11e69bae9793cc0367325ce98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610831"
---
# <span data-ttu-id="29f18-101">Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="29f18-101">Get-AzureRmConsumptionUsageDetail</span></span>

## <span data-ttu-id="29f18-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="29f18-102">SYNOPSIS</span></span>
<span data-ttu-id="29f18-103">Obter detalhes de uso da assinatura.</span><span class="sxs-lookup"><span data-stu-id="29f18-103">Get usage details of the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29f18-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="29f18-104">SYNTAX</span></span>

### <span data-ttu-id="29f18-105">Assinatura (padrão)</span><span class="sxs-lookup"><span data-stu-id="29f18-105">Subscription (Default)</span></span>
```
Get-AzureRmConsumptionUsageDetail [-MaxCount <Int32>] [-IncludeMeterDetails] [-IncludeAdditionalProperties]
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29f18-106">Fatura</span><span class="sxs-lookup"><span data-stu-id="29f18-106">Invoice</span></span>
```
Get-AzureRmConsumptionUsageDetail -InvoiceName <String> [-MaxCount <Int32>] [-IncludeMeterDetails]
 [-IncludeAdditionalProperties] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29f18-107">BillingPeriod</span><span class="sxs-lookup"><span data-stu-id="29f18-107">BillingPeriod</span></span>
```
Get-AzureRmConsumptionUsageDetail -BillingPeriodName <String> [-MaxCount <Int32>] [-IncludeMeterDetails]
 [-IncludeAdditionalProperties] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29f18-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="29f18-108">DESCRIPTION</span></span>
<span data-ttu-id="29f18-109">O cmdlet **Get-AzureRmConsumptionUsageDetail** Obtém detalhes de uso da assinatura.</span><span class="sxs-lookup"><span data-stu-id="29f18-109">The **Get-AzureRmConsumptionUsageDetail** cmdlet gets usage details of the subscription.</span></span> 

## <span data-ttu-id="29f18-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="29f18-110">EXAMPLES</span></span>

### <span data-ttu-id="29f18-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="29f18-111">Example 1</span></span>
```
PS C:\> Get-AzureRmConsumptionUsageDetail -IncludeMeterDetails -InvoiceName 201704-117283130069214
```

<span data-ttu-id="29f18-112">Obter detalhes de uso da fatura com o nome especificado e incluir a propriedade MeterDetails no resultado.</span><span class="sxs-lookup"><span data-stu-id="29f18-112">Get usage details of the invoice with specified name, and include MeterDetails property in the result.</span></span>

### <span data-ttu-id="29f18-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="29f18-113">Example 2</span></span>
```
PS C:\> Get-AzureRmConsumptionUsageDetail -IncludeAdditionalProperties -BillingPeriodName 201704-1
```

<span data-ttu-id="29f18-114">Obtenha detalhes de uso do período de cobrança com o nome especificado e inclua a propriedade AdditionalProperties no resultado.</span><span class="sxs-lookup"><span data-stu-id="29f18-114">Get usage details of the billing period with specified name, and include AdditionalProperties property in the result.</span></span>

### <span data-ttu-id="29f18-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="29f18-115">Example 3</span></span>
```
PS C:\> Get-AzureRmConsumptionUsageDetail -StartDate 2017-01-17 -EndDate 2017-01-19
```

<span data-ttu-id="29f18-116">Obtenha detalhes de uso da assinatura entre 2017-01-17 e 2017-01-19.</span><span class="sxs-lookup"><span data-stu-id="29f18-116">Get usage details of the subscription that is between 2017-01-17 to 2017-01-19.</span></span>

## <span data-ttu-id="29f18-117">OS</span><span class="sxs-lookup"><span data-stu-id="29f18-117">PARAMETERS</span></span>

### <span data-ttu-id="29f18-118">-BillingPeriodName</span><span class="sxs-lookup"><span data-stu-id="29f18-118">-BillingPeriodName</span></span>
<span data-ttu-id="29f18-119">Nome de um período de cobrança específico para obter os detalhes de uso associados.</span><span class="sxs-lookup"><span data-stu-id="29f18-119">Name of a specific billing period to get the usage details that associate with.</span></span>

```yaml
Type: System.String
Parameter Sets: BillingPeriod
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29f18-120">-EndDate</span><span class="sxs-lookup"><span data-stu-id="29f18-120">-EndDate</span></span>
<span data-ttu-id="29f18-121">A data de término (em UTC) dos usos.</span><span class="sxs-lookup"><span data-stu-id="29f18-121">The end date (in UTC) of the usages.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29f18-122">-IncludeAdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="29f18-122">-IncludeAdditionalProperties</span></span>
<span data-ttu-id="29f18-123">Inclua propriedades adicionais nos usos.</span><span class="sxs-lookup"><span data-stu-id="29f18-123">Include additional properties in the usages.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29f18-124">-IncludeMeterDetails</span><span class="sxs-lookup"><span data-stu-id="29f18-124">-IncludeMeterDetails</span></span>
<span data-ttu-id="29f18-125">Inclua detalhes do medidor nos usos.</span><span class="sxs-lookup"><span data-stu-id="29f18-125">Include meter details in the usages.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29f18-126">-Faturaname</span><span class="sxs-lookup"><span data-stu-id="29f18-126">-InvoiceName</span></span>
<span data-ttu-id="29f18-127">Nome de uma fatura específica para obter os detalhes de uso associados.</span><span class="sxs-lookup"><span data-stu-id="29f18-127">Name of a specific invoice to get the usage details that associate with.</span></span>

```yaml
Type: System.String
Parameter Sets: Invoice
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29f18-128">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="29f18-128">-MaxCount</span></span>
<span data-ttu-id="29f18-129">Determine o número máximo de registros a serem retornados.</span><span class="sxs-lookup"><span data-stu-id="29f18-129">Determine the maximum number of records to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29f18-130">-StartDate</span><span class="sxs-lookup"><span data-stu-id="29f18-130">-StartDate</span></span>
<span data-ttu-id="29f18-131">A data de início (em UTC) dos usos.</span><span class="sxs-lookup"><span data-stu-id="29f18-131">The start date (in UTC) of the usages.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29f18-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29f18-132">-DefaultProfile</span></span>
<span data-ttu-id="29f18-133">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="29f18-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29f18-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29f18-134">CommonParameters</span></span>
<span data-ttu-id="29f18-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29f18-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29f18-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29f18-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29f18-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="29f18-137">INPUTS</span></span>

### <span data-ttu-id="29f18-138">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="29f18-138">None</span></span>

## <span data-ttu-id="29f18-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="29f18-139">OUTPUTS</span></span>

### <span data-ttu-id="29f18-140">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. consumo. Models. PSUsageDetail, Microsoft. Azure. Commands. consumo, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="29f18-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Consumption.Models.PSUsageDetail, Microsoft.Azure.Commands.Consumption, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="29f18-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="29f18-141">NOTES</span></span>

## <span data-ttu-id="29f18-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="29f18-142">RELATED LINKS</span></span>

