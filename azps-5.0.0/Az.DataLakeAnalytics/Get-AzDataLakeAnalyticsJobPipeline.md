---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsjobpipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJobPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJobPipeline.md
ms.openlocfilehash: 1d13d1b6e55831c972457c5a6a5aadc427ecb3a6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280909"
---
# <span data-ttu-id="a9c49-101">Get-AzDataLakeAnalyticsJobPipeline</span><span class="sxs-lookup"><span data-stu-id="a9c49-101">Get-AzDataLakeAnalyticsJobPipeline</span></span>

## <span data-ttu-id="a9c49-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a9c49-102">SYNOPSIS</span></span>
<span data-ttu-id="a9c49-103">Obtém pipelines ou pipeline de trabalho do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="a9c49-103">Gets a Data Lake Analytics Job pipeline or pipelines.</span></span>

## <span data-ttu-id="a9c49-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a9c49-104">SYNTAX</span></span>

### <span data-ttu-id="a9c49-105">GetAllInAccount (padrão)</span><span class="sxs-lookup"><span data-stu-id="a9c49-105">GetAllInAccount (Default)</span></span>
```
Get-AzDataLakeAnalyticsJobPipeline [-Account] <String> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9c49-106">GetBySpecificJobPipeline</span><span class="sxs-lookup"><span data-stu-id="a9c49-106">GetBySpecificJobPipeline</span></span>
```
Get-AzDataLakeAnalyticsJobPipeline [-Account] <String> [-PipelineId] <Guid> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9c49-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a9c49-107">DESCRIPTION</span></span>
<span data-ttu-id="a9c49-108">**Get-AzDataLakeAnalyticsJobPipeline** Obtém um pipeline de trabalho do Azure data Lake Analytics especificado ou uma lista de pipelines.</span><span class="sxs-lookup"><span data-stu-id="a9c49-108">The **Get-AzDataLakeAnalyticsJobPipeline** gets a specified Azure Data Lake Analytics Job pipeline or a list of pipelines.</span></span>

## <span data-ttu-id="a9c49-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a9c49-109">EXAMPLES</span></span>

### <span data-ttu-id="a9c49-110">Exemplo 1: obter um pipeline especificado</span><span class="sxs-lookup"><span data-stu-id="a9c49-110">Example 1: Get a specified pipeline</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJobPipeline -Account "contosoadla" -PipelineId 83cb7ad2-3523-4b82-b909-d478b0d8aea3
```

<span data-ttu-id="a9c49-111">Este comando obtém o pipeline especificado com a ID ' 83cb7ad2-3523-4b82-b909-d478b0d8aea3 ' na conta ' contosoadla '.</span><span class="sxs-lookup"><span data-stu-id="a9c49-111">This command gets the specified pipeline with id '83cb7ad2-3523-4b82-b909-d478b0d8aea3' in account 'contosoadla'.</span></span>

### <span data-ttu-id="a9c49-112">Exemplo 2: obter uma lista de todas as tubulações na conta</span><span class="sxs-lookup"><span data-stu-id="a9c49-112">Example 2: Get a list of all pipelines in the account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJobPipeline -AccountName "contosoadla"
```

<span data-ttu-id="a9c49-113">Esse comando obtém uma lista de todas as tubulações na conta "contosoadla"</span><span class="sxs-lookup"><span data-stu-id="a9c49-113">This command gets a list of all pipelines in the account "contosoadla"</span></span>

## <span data-ttu-id="a9c49-114">OS</span><span class="sxs-lookup"><span data-stu-id="a9c49-114">PARAMETERS</span></span>

### <span data-ttu-id="a9c49-115">-Conta</span><span class="sxs-lookup"><span data-stu-id="a9c49-115">-Account</span></span>
<span data-ttu-id="a9c49-116">Nome do nome da conta do data Lake Analytics sob a qual deseja recuperar o pipeline de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a9c49-116">Name of the Data Lake Analytics account name under which want to retrieve the job pipeline.</span></span>

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

### <span data-ttu-id="a9c49-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9c49-117">-DefaultProfile</span></span>
<span data-ttu-id="a9c49-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="a9c49-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a9c49-119">-Pipelineid</span><span class="sxs-lookup"><span data-stu-id="a9c49-119">-PipelineId</span></span>
<span data-ttu-id="a9c49-120">ID do pipeline de trabalho específico para o qual as informações são retornadas.</span><span class="sxs-lookup"><span data-stu-id="a9c49-120">ID of the specific job pipeline to return information for.</span></span>

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

### <span data-ttu-id="a9c49-121">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="a9c49-121">-SubmittedAfter</span></span>
<span data-ttu-id="a9c49-122">Um filtro opcional que retorna o (s) pipeline (s) de trabalho enviado (s) somente após a hora especificada.</span><span class="sxs-lookup"><span data-stu-id="a9c49-122">An optional filter which returns job pipeline(s) only submitted after the specified time.</span></span>

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

### <span data-ttu-id="a9c49-123">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="a9c49-123">-SubmittedBefore</span></span>
<span data-ttu-id="a9c49-124">Um filtro opcional que retorna o (s) pipeline (s) de trabalho somente enviado antes do tempo especificado.</span><span class="sxs-lookup"><span data-stu-id="a9c49-124">An optional filter which returns job pipeline(s) only submitted before the specified time.</span></span>

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

### <span data-ttu-id="a9c49-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9c49-125">CommonParameters</span></span>
<span data-ttu-id="a9c49-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9c49-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9c49-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9c49-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9c49-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a9c49-128">INPUTS</span></span>

### <span data-ttu-id="a9c49-129">System. String</span><span class="sxs-lookup"><span data-stu-id="a9c49-129">System.String</span></span>

### <span data-ttu-id="a9c49-130">System. GUID</span><span class="sxs-lookup"><span data-stu-id="a9c49-130">System.Guid</span></span>

### <span data-ttu-id="a9c49-131">System. Nullable ' 1 [[System. DateTimeOffset, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a9c49-131">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="a9c49-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a9c49-132">OUTPUTS</span></span>

### <span data-ttu-id="a9c49-133">Microsoft. Azure. Commands. DataLakeAnalytics. Models. PSJobPipelineInformation</span><span class="sxs-lookup"><span data-stu-id="a9c49-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSJobPipelineInformation</span></span>

## <span data-ttu-id="a9c49-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a9c49-134">NOTES</span></span>

## <span data-ttu-id="a9c49-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a9c49-135">RELATED LINKS</span></span>
