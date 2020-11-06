---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: CE7B54BC-C493-49CE-93BD-346ED0B966A1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/wait-azurermdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Wait-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Wait-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: 43af4abf52c3441f25ec57ce659b6c4e47a79cdf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440475"
---
# <span data-ttu-id="59fc9-101">Wait-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="59fc9-101">Wait-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="59fc9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="59fc9-102">SYNOPSIS</span></span>
<span data-ttu-id="59fc9-103">Aguarda um trabalho ser concluído.</span><span class="sxs-lookup"><span data-stu-id="59fc9-103">Waits for a job to complete.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59fc9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="59fc9-104">SYNTAX</span></span>

```
Wait-AzureRmDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-WaitIntervalInSeconds] <Int32>]
 [[-TimeoutInSeconds] <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59fc9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="59fc9-105">DESCRIPTION</span></span>
<span data-ttu-id="59fc9-106">O cmdlet **Wait-AzureRmDataLakeAnalyticsJob** aguarda a conclusão de um trabalho do Azure data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="59fc9-106">The **Wait-AzureRmDataLakeAnalyticsJob** cmdlet waits for an Azure Data Lake Analytics job to complete.</span></span>

## <span data-ttu-id="59fc9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="59fc9-107">EXAMPLES</span></span>

### <span data-ttu-id="59fc9-108">Exemplo 1: Aguarde a conclusão do trabalho</span><span class="sxs-lookup"><span data-stu-id="59fc9-108">Example 1: Wait for a job to complete</span></span>
```
PS C:\>Wait-AzureRmDataLakeAnalyticsJob -Account "ContosoAdlAccount" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="59fc9-109">O comando a seguir aguarda o trabalho com a ID especificada ser concluída.</span><span class="sxs-lookup"><span data-stu-id="59fc9-109">The following command waits for the job with the specified ID to complete.</span></span>

## <span data-ttu-id="59fc9-110">OS</span><span class="sxs-lookup"><span data-stu-id="59fc9-110">PARAMETERS</span></span>

### <span data-ttu-id="59fc9-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="59fc9-111">-Account</span></span>
<span data-ttu-id="59fc9-112">Especifica o nome da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="59fc9-112">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59fc9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59fc9-113">-DefaultProfile</span></span>
<span data-ttu-id="59fc9-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="59fc9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="59fc9-115">-JobId</span><span class="sxs-lookup"><span data-stu-id="59fc9-115">-JobId</span></span>
<span data-ttu-id="59fc9-116">Especifica a ID do trabalho a ser aguardado.</span><span class="sxs-lookup"><span data-stu-id="59fc9-116">Specifies the ID of the job for which to wait.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59fc9-117">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="59fc9-117">-TimeoutInSeconds</span></span>
<span data-ttu-id="59fc9-118">Especifica o número de segundos a aguardar antes de sair da operação de espera.</span><span class="sxs-lookup"><span data-stu-id="59fc9-118">Specifies the number of seconds to wait before exiting the wait operation.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59fc9-119">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="59fc9-119">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="59fc9-120">Especifique o número de segundos que decorrem entre cada verificação do estado do trabalho.</span><span class="sxs-lookup"><span data-stu-id="59fc9-120">Specify the number of seconds that elapse between each check of the job state.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59fc9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59fc9-121">CommonParameters</span></span>
<span data-ttu-id="59fc9-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59fc9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59fc9-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59fc9-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59fc9-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="59fc9-124">INPUTS</span></span>

### <span data-ttu-id="59fc9-125">#C0</span><span class="sxs-lookup"><span data-stu-id="59fc9-125">Guid</span></span>
<span data-ttu-id="59fc9-126">O parâmetro ' JobId ' aceita o valor do tipo ' GUID ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="59fc9-126">Parameter 'JobId' accepts value of type 'Guid' from the pipeline</span></span>

## <span data-ttu-id="59fc9-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="59fc9-127">OUTPUTS</span></span>

### <span data-ttu-id="59fc9-128">JobInformation</span><span class="sxs-lookup"><span data-stu-id="59fc9-128">JobInformation</span></span>
<span data-ttu-id="59fc9-129">Os detalhes do trabalho final do trabalho concluído.</span><span class="sxs-lookup"><span data-stu-id="59fc9-129">The final job details for the completed job.</span></span>

## <span data-ttu-id="59fc9-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="59fc9-130">NOTES</span></span>

## <span data-ttu-id="59fc9-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="59fc9-131">RELATED LINKS</span></span>

[<span data-ttu-id="59fc9-132">Get-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="59fc9-132">Get-AzureRmDataLakeAnalyticsJob</span></span>](./Get-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="59fc9-133">Parar-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="59fc9-133">Stop-AzureRmDataLakeAnalyticsJob</span></span>](./Stop-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="59fc9-134">Enviar-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="59fc9-134">Submit-AzureRmDataLakeAnalyticsJob</span></span>](./Submit-AzureRmDataLakeAnalyticsJob.md)


