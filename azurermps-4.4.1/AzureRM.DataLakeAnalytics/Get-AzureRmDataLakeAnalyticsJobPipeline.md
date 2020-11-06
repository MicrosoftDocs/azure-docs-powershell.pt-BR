---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJobPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJobPipeline.md
ms.openlocfilehash: 838fb221952a97234c31c514aa82fc30be7e2f25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441118"
---
# <span data-ttu-id="e7868-101">Get-AzureRmDataLakeAnalyticsJobPipeline</span><span class="sxs-lookup"><span data-stu-id="e7868-101">Get-AzureRmDataLakeAnalyticsJobPipeline</span></span>

## <span data-ttu-id="e7868-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e7868-102">SYNOPSIS</span></span>
<span data-ttu-id="e7868-103">Obtém pipelines ou pipeline de trabalho do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="e7868-103">Gets a Data Lake Analytics Job pipeline or pipelines.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7868-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e7868-104">SYNTAX</span></span>

### <span data-ttu-id="e7868-105">Todos em conta (padrão)</span><span class="sxs-lookup"><span data-stu-id="e7868-105">All In Account (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsJobPipeline [-Account] <String> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e7868-106">Pipeline de trabalho específico</span><span class="sxs-lookup"><span data-stu-id="e7868-106">Specific Job Pipeline</span></span>
```
Get-AzureRmDataLakeAnalyticsJobPipeline [-Account] <String> [-PipelineId] <Guid>
 [-SubmittedAfter <DateTimeOffset>] [-SubmittedBefore <DateTimeOffset>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7868-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e7868-107">DESCRIPTION</span></span>
<span data-ttu-id="e7868-108">**Get-AzureRmDataLakeAnalyticsJobPipeline** Obtém um pipeline de trabalho do Azure data Lake Analytics especificado ou uma lista de pipelines.</span><span class="sxs-lookup"><span data-stu-id="e7868-108">The **Get-AzureRmDataLakeAnalyticsJobPipeline** gets a specified Azure Data Lake Analytics Job pipeline or a list of pipelines.</span></span>

## <span data-ttu-id="e7868-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e7868-109">EXAMPLES</span></span>

### <span data-ttu-id="e7868-110">Exemplo 1: obter um pipeline especificado</span><span class="sxs-lookup"><span data-stu-id="e7868-110">Example 1: Get a specified pipeline</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJobPipeline -Account "contosoadla" -PipelineId 83cb7ad2-3523-4b82-b909-d478b0d8aea3
```

<span data-ttu-id="e7868-111">Este comando obtém o pipeline especificado com a ID ' 83cb7ad2-3523-4b82-b909-d478b0d8aea3 ' na conta ' contosoadla '.</span><span class="sxs-lookup"><span data-stu-id="e7868-111">This command gets the specified pipeline with id '83cb7ad2-3523-4b82-b909-d478b0d8aea3' in account 'contosoadla'.</span></span>

### <span data-ttu-id="e7868-112">Exemplo 2: obter uma lista de todas as tubulações na conta</span><span class="sxs-lookup"><span data-stu-id="e7868-112">Example 2: Get a list of all pipelines in the account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJobPipeline -AccountName "contosoadla"
```

<span data-ttu-id="e7868-113">Esse comando obtém uma lista de todas as tubulações na conta "contosoadla"</span><span class="sxs-lookup"><span data-stu-id="e7868-113">This command gets a list of all pipelines in the account "contosoadla"</span></span>

## <span data-ttu-id="e7868-114">OS</span><span class="sxs-lookup"><span data-stu-id="e7868-114">PARAMETERS</span></span>

### <span data-ttu-id="e7868-115">-Conta</span><span class="sxs-lookup"><span data-stu-id="e7868-115">-Account</span></span>
<span data-ttu-id="e7868-116">Nome do nome da conta do data Lake Analytics sob a qual deseja recuperar o pipeline de trabalho.</span><span class="sxs-lookup"><span data-stu-id="e7868-116">Name of the Data Lake Analytics account name under which want to retrieve the job pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7868-117">-Pipelineid</span><span class="sxs-lookup"><span data-stu-id="e7868-117">-PipelineId</span></span>
<span data-ttu-id="e7868-118">ID do pipeline de trabalho específico para o qual as informações são retornadas.</span><span class="sxs-lookup"><span data-stu-id="e7868-118">ID of the specific job pipeline to return information for.</span></span>

```yaml
Type: System.Guid
Parameter Sets: Specific Job Pipeline
Aliases: Id

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7868-119">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="e7868-119">-SubmittedAfter</span></span>
<span data-ttu-id="e7868-120">Um filtro opcional que retorna o (s) pipeline (s) de trabalho enviado (s) somente após a hora especificada.</span><span class="sxs-lookup"><span data-stu-id="e7868-120">An optional filter which returns job pipeline(s) only submitted after the specified time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7868-121">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="e7868-121">-SubmittedBefore</span></span>
<span data-ttu-id="e7868-122">Um filtro opcional que retorna o (s) pipeline (s) de trabalho somente enviado antes do tempo especificado.</span><span class="sxs-lookup"><span data-stu-id="e7868-122">An optional filter which returns job pipeline(s) only submitted before the specified time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7868-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7868-123">-DefaultProfile</span></span>
<span data-ttu-id="e7868-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e7868-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7868-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7868-125">CommonParameters</span></span>
<span data-ttu-id="e7868-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7868-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7868-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7868-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7868-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e7868-128">INPUTS</span></span>

### <span data-ttu-id="e7868-129">System. String</span><span class="sxs-lookup"><span data-stu-id="e7868-129">System.String</span></span>

### <span data-ttu-id="e7868-130">System. GUID</span><span class="sxs-lookup"><span data-stu-id="e7868-130">System.Guid</span></span>

## <span data-ttu-id="e7868-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e7868-131">OUTPUTS</span></span>

### <span data-ttu-id="e7868-132">Microsoft. Azure. Commands. DataLakeAnalytics. Models. PSJobPipelineInformation</span><span class="sxs-lookup"><span data-stu-id="e7868-132">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSJobPipelineInformation</span></span>

## <span data-ttu-id="e7868-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e7868-133">NOTES</span></span>

## <span data-ttu-id="e7868-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e7868-134">RELATED LINKS</span></span>
