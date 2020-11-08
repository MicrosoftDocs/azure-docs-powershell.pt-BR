---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillinginvoice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingInvoice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingInvoice.md
ms.openlocfilehash: 2392b3275feeb6fa23f8f76dd3e76b6d97c33d46
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94118429"
---
# <span data-ttu-id="4e427-101">Get-AzBillingInvoice</span><span class="sxs-lookup"><span data-stu-id="4e427-101">Get-AzBillingInvoice</span></span>

## <span data-ttu-id="4e427-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4e427-102">SYNOPSIS</span></span>
<span data-ttu-id="4e427-103">Obter faturas de cobrança da assinatura.</span><span class="sxs-lookup"><span data-stu-id="4e427-103">Get billing invoices of the subscription.</span></span>
<span data-ttu-id="4e427-104">Obter faturas de cobrança de uma conta de cobrança e perfil de cobrança</span><span class="sxs-lookup"><span data-stu-id="4e427-104">Get billing invoices of a billing account and billing profile</span></span>

## <span data-ttu-id="4e427-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4e427-105">SYNTAX</span></span>

### <span data-ttu-id="4e427-106">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="4e427-106">List (Default)</span></span>
```
Get-AzBillingInvoice [-MaxCount <Int32>] [-GenerateDownloadUrl] [-DefaultProfile <IAzureContextContainer>] [-BillingAccountName] [-BillingProfileName]
 [<CommonParameters>]
```

### <span data-ttu-id="4e427-107">Novidades</span><span class="sxs-lookup"><span data-stu-id="4e427-107">Latest</span></span>
```
Get-AzBillingInvoice [-Latest] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>] [-BillingAccountName] [-BillingProfileName]
```

### <span data-ttu-id="4e427-108">Apenas</span><span class="sxs-lookup"><span data-stu-id="4e427-108">Single</span></span>
```
Get-AzBillingInvoice -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e427-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4e427-109">DESCRIPTION</span></span>
<span data-ttu-id="4e427-110">O cmdlet **Get-AzBillingInvoice** recebe faturas de cobrança da assinatura.</span><span class="sxs-lookup"><span data-stu-id="4e427-110">The **Get-AzBillingInvoice** cmdlet gets billing invoices of the subscription.</span></span> 

## <span data-ttu-id="4e427-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4e427-111">EXAMPLES</span></span>

### <span data-ttu-id="4e427-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4e427-112">Example 1</span></span>
```
PS C:\> Get-AzBillingInvoice -Latest
```

<span data-ttu-id="4e427-113">Obtenha a última fatura da assinatura.</span><span class="sxs-lookup"><span data-stu-id="4e427-113">Get the latest invoice of the subscription.</span></span>

### <span data-ttu-id="4e427-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="4e427-114">Example 2</span></span>
```
PS C:\> Get-AzBillingInvoice -Name 2017-02-18-432543543
```

<span data-ttu-id="4e427-115">Obter a fatura da assinatura com o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="4e427-115">Get the invoice of the subscription with the specified name.</span></span>

### <span data-ttu-id="4e427-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="4e427-116">Example 3</span></span>
```
PS C:\> Get-AzBillingInvoice
```

<span data-ttu-id="4e427-117">Obtenha todas as faturas disponíveis da assinatura em ordem cronológica inversa, começando com a fatura mais recente sem baixar a URL.</span><span class="sxs-lookup"><span data-stu-id="4e427-117">Get all available invoices of the subscription in reverse chronological order beginning with the most recent invoice without download Url.</span></span> 

### <span data-ttu-id="4e427-118">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="4e427-118">Example 4</span></span>
```
PS C:\> Get-AzBillingInvoice -GenerateDownloadUrl -MaxCount 10
```

<span data-ttu-id="4e427-119">Obtenha 10 faturas mais recentes da assinatura e inclua a URL de download no resultado.</span><span class="sxs-lookup"><span data-stu-id="4e427-119">Get most recent 10 invoices of the subscription and include the download Url in the result.</span></span>

### <span data-ttu-id="4e427-120">Exemplo 5</span><span class="sxs-lookup"><span data-stu-id="4e427-120">Example 5</span></span>
```
PS C:\> Get-AzBillingInvoice -Name 2017-02-18-432543543 -GenerateDownloadUrl
```

<span data-ttu-id="4e427-121">Obtenha a fatura específica por nome e inclua a URL de download no resultado.</span><span class="sxs-lookup"><span data-stu-id="4e427-121">Get the specific invoice by name and include download url in the result.</span></span>

### <span data-ttu-id="4e427-122">Exemplo 6</span><span class="sxs-lookup"><span data-stu-id="4e427-122">Example 6</span></span>
```
PS C:\> Get-AzBillingInvoice -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

<span data-ttu-id="4e427-123">Obtenha faturas por nome da conta de cobrança e inclua a URL de download para cada fatura do resultado.</span><span class="sxs-lookup"><span data-stu-id="4e427-123">Get invoices by billing account name and include download url for each invoice in the result.</span></span>

### <span data-ttu-id="4e427-124">Exemplo 7</span><span class="sxs-lookup"><span data-stu-id="4e427-124">Example 7</span></span>
```
PS C:\> Get-AzBillingInvoice Get-AzBillingInvoice -Name 0000000000 -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

<span data-ttu-id="4e427-125">Obter fatura específica por nome da fatura e nome da conta de cobrança e incluir a URL de download para cada fatura do resultado.</span><span class="sxs-lookup"><span data-stu-id="4e427-125">Get specific invoice by invoice name and billing account name and include download url for each invoice in the result.</span></span>

### <span data-ttu-id="4e427-126">Exemplo 8</span><span class="sxs-lookup"><span data-stu-id="4e427-126">Example 8</span></span>
```
PS C:\> Get-AzBillingInvoice -Latest -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

<span data-ttu-id="4e427-127">Obtenha a última fatura com o nome da conta de cobrança e inclua a URL de download para a fatura no resultado.</span><span class="sxs-lookup"><span data-stu-id="4e427-127">Get latest invoice by billing account name and include download url for invoice in the result.</span></span>

### <span data-ttu-id="4e427-128">Exemplo 9</span><span class="sxs-lookup"><span data-stu-id="4e427-128">Example 9</span></span>
```
PS C:\> Get-AzBillingInvoice -GenerateDownloadUrl -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 -MaxCount 10
```

<span data-ttu-id="4e427-129">Obtenha 10 faturas mais recentes da conta de cobrança específica e do perfil de cobrança específico e inclua a URL de download no resultado.</span><span class="sxs-lookup"><span data-stu-id="4e427-129">Get most recent 10 invoices of the specific billing account and specific billing profile and include the download Url in the result.</span></span>

### <span data-ttu-id="4e427-130">Exemplo 10</span><span class="sxs-lookup"><span data-stu-id="4e427-130">Example 10</span></span>
```
PS C:\> Get-AzBillingInvoice -Latest -GenerateDownloadUrl -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 
```

<span data-ttu-id="4e427-131">Obtenha a última fatura com o nome da conta de cobrança e o nome do perfil de cobrança e inclua a URL de download para a fatura no resultado.</span><span class="sxs-lookup"><span data-stu-id="4e427-131">Get latest invoice by billing account name and billing profile name and include download url for invoice in the result.</span></span>

### <span data-ttu-id="4e427-132">Exemplo 10</span><span class="sxs-lookup"><span data-stu-id="4e427-132">Example 10</span></span>
```
PS C:\> Get-AzBillingInvoice -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 -PeriodStartDate 0000-00-00 -PeriodEndDate 0000-00-00
```

<span data-ttu-id="4e427-133">Obter faturas por nome da conta de cobrança e nome do perfil de cobrança para um período de cobrança especificado por data perioStart e data de periodEnd.</span><span class="sxs-lookup"><span data-stu-id="4e427-133">Get invoices by billing account name and billing profile name for a billing period specified by perioStart date and periodEnd date.</span></span>


## <span data-ttu-id="4e427-134">OS</span><span class="sxs-lookup"><span data-stu-id="4e427-134">PARAMETERS</span></span>

### <span data-ttu-id="4e427-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e427-135">-DefaultProfile</span></span>
<span data-ttu-id="4e427-136">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="4e427-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4e427-137">-GenerateDownloadUrl</span><span class="sxs-lookup"><span data-stu-id="4e427-137">-GenerateDownloadUrl</span></span>
<span data-ttu-id="4e427-138">Gerar a URL de download das faturas.</span><span class="sxs-lookup"><span data-stu-id="4e427-138">Generate the download url of the invoices.</span></span>

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

### <span data-ttu-id="4e427-139">-Mais recente</span><span class="sxs-lookup"><span data-stu-id="4e427-139">-Latest</span></span>
<span data-ttu-id="4e427-140">Obtenha a última fatura.</span><span class="sxs-lookup"><span data-stu-id="4e427-140">Get the latest invoice.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Latest
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e427-141">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="4e427-141">-MaxCount</span></span>
<span data-ttu-id="4e427-142">Determina o número máximo de registros a serem retornados.</span><span class="sxs-lookup"><span data-stu-id="4e427-142">Determines the maximum number of records to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e427-143">-Nome</span><span class="sxs-lookup"><span data-stu-id="4e427-143">-Name</span></span>
<span data-ttu-id="4e427-144">Nome de uma fatura específica a ser obtida ou a mais recente se não for especificada.</span><span class="sxs-lookup"><span data-stu-id="4e427-144">Name of a specific invoice to get or the most recent if not specified.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Single
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e427-145">-BillingAccountName</span><span class="sxs-lookup"><span data-stu-id="4e427-145">-BillingAccountName</span></span>
<span data-ttu-id="4e427-146">Nome de uma conta de cobrança específica para obter faturas.</span><span class="sxs-lookup"><span data-stu-id="4e427-146">Name of a specific billing account to get invoices for.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e427-147">-BillingProfileName</span><span class="sxs-lookup"><span data-stu-id="4e427-147">-BillingProfileName</span></span>
<span data-ttu-id="4e427-148">Nome de um perfil de cobrança específico para obter faturas.</span><span class="sxs-lookup"><span data-stu-id="4e427-148">Name of a specific billing profile to get invoices for.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e427-149">-PeriodStartDate</span><span class="sxs-lookup"><span data-stu-id="4e427-149">-PeriodStartDate</span></span>
<span data-ttu-id="4e427-150">Data de início da fatura.</span><span class="sxs-lookup"><span data-stu-id="4e427-150">Start date for invoice.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e427-151">-PeriodEndDate</span><span class="sxs-lookup"><span data-stu-id="4e427-151">-PeriodEndDate</span></span>
<span data-ttu-id="4e427-152">Data de término da fatura.</span><span class="sxs-lookup"><span data-stu-id="4e427-152">End date for invoice.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```



### <span data-ttu-id="4e427-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e427-153">CommonParameters</span></span>
<span data-ttu-id="4e427-154">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e427-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e427-155">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e427-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e427-156">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4e427-156">INPUTS</span></span>

### <span data-ttu-id="4e427-157">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="4e427-157">None</span></span>

## <span data-ttu-id="4e427-158">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4e427-158">OUTPUTS</span></span>

### <span data-ttu-id="4e427-159">Microsoft. Azure. Commands. billing. Models. PSInvoice</span><span class="sxs-lookup"><span data-stu-id="4e427-159">Microsoft.Azure.Commands.Billing.Models.PSInvoice</span></span>

## <span data-ttu-id="4e427-160">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4e427-160">NOTES</span></span>

## <span data-ttu-id="4e427-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4e427-161">RELATED LINKS</span></span>
