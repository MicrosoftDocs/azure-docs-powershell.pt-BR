---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsjobpipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJobPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJobPipeline.md
ms.openlocfilehash: 9e925e1bd118a9ac5f676ee666cb945f22d1ffac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889990"
---
# <span data-ttu-id="93abf-101">Get-AzDataLakeAnalyticsJobPipeline</span><span class="sxs-lookup"><span data-stu-id="93abf-101">Get-AzDataLakeAnalyticsJobPipeline</span></span>

## <span data-ttu-id="93abf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93abf-102">SYNOPSIS</span></span>
<span data-ttu-id="93abf-103">Obtém pipelines ou pipelines de trabalho do Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="93abf-103">Gets a Data Lake Analytics Job pipeline or pipelines.</span></span>

## <span data-ttu-id="93abf-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="93abf-104">SYNTAX</span></span>

### <span data-ttu-id="93abf-105">GetAllInAccount (Padrão)</span><span class="sxs-lookup"><span data-stu-id="93abf-105">GetAllInAccount (Default)</span></span>
```
Get-AzDataLakeAnalyticsJobPipeline [-Account] <String> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93abf-106">GetBySpecificJobPipeline</span><span class="sxs-lookup"><span data-stu-id="93abf-106">GetBySpecificJobPipeline</span></span>
```
Get-AzDataLakeAnalyticsJobPipeline [-Account] <String> [-PipelineId] <Guid> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93abf-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="93abf-107">DESCRIPTION</span></span>
<span data-ttu-id="93abf-108">O **Get-AzDataLakeAnalyticsJobPipeline** obtém um pipeline especificado do Azure Data Lake Analytics Job ou uma lista de pipelines.</span><span class="sxs-lookup"><span data-stu-id="93abf-108">The **Get-AzDataLakeAnalyticsJobPipeline** gets a specified Azure Data Lake Analytics Job pipeline or a list of pipelines.</span></span>

## <span data-ttu-id="93abf-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="93abf-109">EXAMPLES</span></span>

### <span data-ttu-id="93abf-110">Exemplo 1: Obter um pipeline especificado</span><span class="sxs-lookup"><span data-stu-id="93abf-110">Example 1: Get a specified pipeline</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJobPipeline -Account "contosoadla" -PipelineId 83cb7ad2-3523-4b82-b909-d478b0d8aea3
```

<span data-ttu-id="93abf-111">Este comando obtém o pipeline especificado com id '83cb7ad2-3523-4b82-b909-d478b0d8aea3' na conta 'contosoadla'.</span><span class="sxs-lookup"><span data-stu-id="93abf-111">This command gets the specified pipeline with id '83cb7ad2-3523-4b82-b909-d478b0d8aea3' in account 'contosoadla'.</span></span>

### <span data-ttu-id="93abf-112">Exemplo 2: Obter uma lista de todos os pipelines na conta</span><span class="sxs-lookup"><span data-stu-id="93abf-112">Example 2: Get a list of all pipelines in the account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJobPipeline -AccountName "contosoadla"
```

<span data-ttu-id="93abf-113">Este comando obtém uma lista de todos os pipelines na conta "contosoadla"</span><span class="sxs-lookup"><span data-stu-id="93abf-113">This command gets a list of all pipelines in the account "contosoadla"</span></span>

## <span data-ttu-id="93abf-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="93abf-114">PARAMETERS</span></span>

### <span data-ttu-id="93abf-115">-Account</span><span class="sxs-lookup"><span data-stu-id="93abf-115">-Account</span></span>
<span data-ttu-id="93abf-116">Nome do nome da conta do Data Lake Analytics sob o qual deseja recuperar o pipeline de trabalho.</span><span class="sxs-lookup"><span data-stu-id="93abf-116">Name of the Data Lake Analytics account name under which want to retrieve the job pipeline.</span></span>

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

### <span data-ttu-id="93abf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93abf-117">-DefaultProfile</span></span>
<span data-ttu-id="93abf-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="93abf-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="93abf-119">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="93abf-119">-PipelineId</span></span>
<span data-ttu-id="93abf-120">ID do pipeline de trabalho específico para o que retornar informações.</span><span class="sxs-lookup"><span data-stu-id="93abf-120">ID of the specific job pipeline to return information for.</span></span>

```yaml
Type: System.Guid
Parameter Sets: GetBySpecificJobPipeline
Aliases: Id

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="93abf-121">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="93abf-121">-SubmittedAfter</span></span>
<span data-ttu-id="93abf-122">Um filtro opcional que retorna pipelines de trabalho enviados somente após o horário especificado.</span><span class="sxs-lookup"><span data-stu-id="93abf-122">An optional filter which returns job pipeline(s) only submitted after the specified time.</span></span>

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

### <span data-ttu-id="93abf-123">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="93abf-123">-SubmittedBefore</span></span>
<span data-ttu-id="93abf-124">Um filtro opcional que retorna pipelines de trabalho enviados somente antes do horário especificado.</span><span class="sxs-lookup"><span data-stu-id="93abf-124">An optional filter which returns job pipeline(s) only submitted before the specified time.</span></span>

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

### <span data-ttu-id="93abf-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93abf-125">CommonParameters</span></span>
<span data-ttu-id="93abf-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93abf-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93abf-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93abf-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93abf-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="93abf-128">INPUTS</span></span>

### <span data-ttu-id="93abf-129">System.String</span><span class="sxs-lookup"><span data-stu-id="93abf-129">System.String</span></span>

### <span data-ttu-id="93abf-130">System.Guid</span><span class="sxs-lookup"><span data-stu-id="93abf-130">System.Guid</span></span>

### <span data-ttu-id="93abf-131">System.Nullable'1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="93abf-131">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="93abf-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="93abf-132">OUTPUTS</span></span>

### <span data-ttu-id="93abf-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSJobPipelineInformation</span><span class="sxs-lookup"><span data-stu-id="93abf-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSJobPipelineInformation</span></span>

## <span data-ttu-id="93abf-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="93abf-134">NOTES</span></span>

## <span data-ttu-id="93abf-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="93abf-135">RELATED LINKS</span></span>
