---
external help file: Microsoft.Azure.Commands.Billing.dll-Help.xml
Module Name: AzureRM.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.billing/get-azurermbillinginvoice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingInvoice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingInvoice.md
ms.openlocfilehash: 1f21022294b1bcf5c75a7cf49dcc009600dc4cc0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432797"
---
# <span data-ttu-id="d0c36-101">Get-AzureRmBillingInvoice</span><span class="sxs-lookup"><span data-stu-id="d0c36-101">Get-AzureRmBillingInvoice</span></span>

## <span data-ttu-id="d0c36-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d0c36-102">SYNOPSIS</span></span>
<span data-ttu-id="d0c36-103">Obter faturas de cobrança da assinatura.</span><span class="sxs-lookup"><span data-stu-id="d0c36-103">Get billing invoices of the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0c36-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d0c36-104">SYNTAX</span></span>

### <span data-ttu-id="d0c36-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="d0c36-105">List (Default)</span></span>
```
Get-AzureRmBillingInvoice [-MaxCount <Int32>] [-GenerateDownloadUrl] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d0c36-106">Novidades</span><span class="sxs-lookup"><span data-stu-id="d0c36-106">Latest</span></span>
```
Get-AzureRmBillingInvoice [-Latest] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d0c36-107">Apenas</span><span class="sxs-lookup"><span data-stu-id="d0c36-107">Single</span></span>
```
Get-AzureRmBillingInvoice -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0c36-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d0c36-108">DESCRIPTION</span></span>
<span data-ttu-id="d0c36-109">O cmdlet **Get-AzureRmBillingInvoice** recebe faturas de cobrança da assinatura.</span><span class="sxs-lookup"><span data-stu-id="d0c36-109">The **Get-AzureRmBillingInvoice** cmdlet gets billing invoices of the subscription.</span></span> 

## <span data-ttu-id="d0c36-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d0c36-110">EXAMPLES</span></span>

### <span data-ttu-id="d0c36-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d0c36-111">Example 1</span></span>
```
PS C:\> Get-AzureRmBillingInvoice -Latest
```

<span data-ttu-id="d0c36-112">Obtenha a última fatura da assinatura.</span><span class="sxs-lookup"><span data-stu-id="d0c36-112">Get the latest invoice of the subscription.</span></span>

### <span data-ttu-id="d0c36-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="d0c36-113">Example 2</span></span>
```
PS C:\> Get-AzureRmBillingInvoice -Name 2017-02-18-432543543
```

<span data-ttu-id="d0c36-114">Obter a fatura da assinatura com o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="d0c36-114">Get the invoice of the subscription with the specified name.</span></span>

### <span data-ttu-id="d0c36-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="d0c36-115">Example 3</span></span>
```
PS C:\> Get-AzureRmBillingInvoice
```

<span data-ttu-id="d0c36-116">Obtenha todas as faturas disponíveis da assinatura em ordem cronológica inversa, começando com a fatura mais recente sem baixar a URL.</span><span class="sxs-lookup"><span data-stu-id="d0c36-116">Get all available invoices of the subscription in reverse chronological order beginning with the most recent invoice without download Url.</span></span> 

### <span data-ttu-id="d0c36-117">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="d0c36-117">Example 4</span></span>
```
PS C:\> Get-AzureRmBillingInvoice -GenerateDownloadUrl -MaxCount 10
```

<span data-ttu-id="d0c36-118">Obtenha 10 faturas mais recentes da assinatura e inclua a URL de download no resultado.</span><span class="sxs-lookup"><span data-stu-id="d0c36-118">Get most recent 10 invoices of the subscription and include the download Url in the result.</span></span>

## <span data-ttu-id="d0c36-119">OS</span><span class="sxs-lookup"><span data-stu-id="d0c36-119">PARAMETERS</span></span>

### <span data-ttu-id="d0c36-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0c36-120">-DefaultProfile</span></span>
<span data-ttu-id="d0c36-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="d0c36-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d0c36-122">-GenerateDownloadUrl</span><span class="sxs-lookup"><span data-stu-id="d0c36-122">-GenerateDownloadUrl</span></span>
<span data-ttu-id="d0c36-123">Gerar a URL de download das faturas.</span><span class="sxs-lookup"><span data-stu-id="d0c36-123">Generate the download url of the invoices.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0c36-124">-Mais recente</span><span class="sxs-lookup"><span data-stu-id="d0c36-124">-Latest</span></span>
<span data-ttu-id="d0c36-125">Obtenha a última fatura.</span><span class="sxs-lookup"><span data-stu-id="d0c36-125">Get the latest invoice.</span></span>

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

### <span data-ttu-id="d0c36-126">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="d0c36-126">-MaxCount</span></span>
<span data-ttu-id="d0c36-127">Determina o número máximo de registros a serem retornados.</span><span class="sxs-lookup"><span data-stu-id="d0c36-127">Determines the maximum number of records to return.</span></span>

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

### <span data-ttu-id="d0c36-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="d0c36-128">-Name</span></span>
<span data-ttu-id="d0c36-129">Nome de uma fatura específica a ser obtida ou a mais recente se não for especificada.</span><span class="sxs-lookup"><span data-stu-id="d0c36-129">Name of a specific invoice to get or the most recent if not specified.</span></span>

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

### <span data-ttu-id="d0c36-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0c36-130">CommonParameters</span></span>
<span data-ttu-id="d0c36-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0c36-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0c36-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0c36-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0c36-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d0c36-133">INPUTS</span></span>

### <span data-ttu-id="d0c36-134">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="d0c36-134">None</span></span>

## <span data-ttu-id="d0c36-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d0c36-135">OUTPUTS</span></span>

### <span data-ttu-id="d0c36-136">Microsoft. Azure. Commands. billing. Models. PSInvoice</span><span class="sxs-lookup"><span data-stu-id="d0c36-136">Microsoft.Azure.Commands.Billing.Models.PSInvoice</span></span>

## <span data-ttu-id="d0c36-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d0c36-137">NOTES</span></span>

## <span data-ttu-id="d0c36-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d0c36-138">RELATED LINKS</span></span>
