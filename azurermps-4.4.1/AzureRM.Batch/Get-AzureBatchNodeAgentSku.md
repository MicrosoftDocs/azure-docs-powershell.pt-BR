---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 5C6D3792-AA56-4210-B376-D9E656B04FBD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeAgentSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeAgentSku.md
ms.openlocfilehash: e29b5df4a72ff21dbacb0928b298306eb585b493
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93439975"
---
# <span data-ttu-id="157b9-101">Get-AzureBatchNodeAgentSku</span><span class="sxs-lookup"><span data-stu-id="157b9-101">Get-AzureBatchNodeAgentSku</span></span>

## <span data-ttu-id="157b9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="157b9-102">SYNOPSIS</span></span>
<span data-ttu-id="157b9-103">Obtém SKUs do agente de nó de lote disponíveis em uma conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="157b9-103">Gets Batch node agent SKUs available in a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="157b9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="157b9-104">SYNTAX</span></span>

```
Get-AzureBatchNodeAgentSku [-Filter <String>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="157b9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="157b9-105">DESCRIPTION</span></span>
<span data-ttu-id="157b9-106">O cmdlet **Get-AzureBatchNodeAgentSku** Obtém SKUs do agente de nó que estão disponíveis em uma conta em lotes do Azure.</span><span class="sxs-lookup"><span data-stu-id="157b9-106">The **Get-AzureBatchNodeAgentSku** cmdlet gets node agent SKUs that are available in an Azure Batch account.</span></span>
<span data-ttu-id="157b9-107">Especifique a conta usando o parâmetro *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="157b9-107">Specify the account by using the *BatchContext* parameter.</span></span>
<span data-ttu-id="157b9-108">Você pode restringir a pesquisa a SKUs que correspondam a um filtro do Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="157b9-108">You can narrow your search to SKUs that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="157b9-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="157b9-109">EXAMPLES</span></span>

### <span data-ttu-id="157b9-110">Exemplo 1: obter todas as SKUs de agente de nó disponíveis</span><span class="sxs-lookup"><span data-stu-id="157b9-110">Example 1: Get all available node agent SKUs</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> Get-AzureBatchNodeAgentSku -BatchContext $Context 
batch.node.centos 7 Linux {7.0, 7.1, 7.2, OL70} 
batch.node.debian 8 Linux {15.10, 8} 
batch.node.opensuse 13.2 Linux {13.2} 
batch.node.opensuse 42.1 Linux {42.1, 12, 12-SP1, 12} 
batch.node.ubuntu 14.04 Linux {14.04.0-LTS, 14.04.1-LTS, 14.04.2-LTS, 14.04.3-LTS...} 
batch.node.windows amd64 Windows {2008-R2-SP1, 2012-Datacenter, 2012-R2-Datacenter, Windows-Server-Technical-Preview}
```

<span data-ttu-id="157b9-111">O primeiro comando obtém um contexto de conta em lotes que contém as chaves de acesso para a sua assinatura usando **Get-AzureRmBatchAccountKeys**.</span><span class="sxs-lookup"><span data-stu-id="157b9-111">The first command gets a batch account context that contains access keys for your subscription by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="157b9-112">O comando armazena o contexto na variável $Context para usar no próximo comando.</span><span class="sxs-lookup"><span data-stu-id="157b9-112">The command stores the context in the $Context variable to use in the next command.</span></span>

<span data-ttu-id="157b9-113">O segundo comando obtém todas as SKUs de agente de nó disponíveis com suporte em lote.</span><span class="sxs-lookup"><span data-stu-id="157b9-113">The second command gets all available node agent SKUs that Batch supports.</span></span>

## <span data-ttu-id="157b9-114">OS</span><span class="sxs-lookup"><span data-stu-id="157b9-114">PARAMETERS</span></span>

### <span data-ttu-id="157b9-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="157b9-115">-BatchContext</span></span>
<span data-ttu-id="157b9-116">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="157b9-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="157b9-117">Para obter um objeto **BatchAccountContext** que contém as teclas de acesso para a sua assinatura, use o cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="157b9-117">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="157b9-118">-Filtro</span><span class="sxs-lookup"><span data-stu-id="157b9-118">-Filter</span></span>
<span data-ttu-id="157b9-119">Especifica uma cláusula de filtro OData para SKUs de agente de nó.</span><span class="sxs-lookup"><span data-stu-id="157b9-119">Specifies an OData filter clause for node agent SKUs.</span></span>
<span data-ttu-id="157b9-120">Se você não especificar um filtro, esse cmdlet retornará todas as SKUs do agente de nó que dão suporte a lote.</span><span class="sxs-lookup"><span data-stu-id="157b9-120">If you do not specify a filter, this cmdlet returns all node agent SKUs that Batch supports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="157b9-121">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="157b9-121">-MaxCount</span></span>
<span data-ttu-id="157b9-122">Especifica o número máximo de SKUs do agente de nó a serem retornadas.</span><span class="sxs-lookup"><span data-stu-id="157b9-122">Specifies the maximum number of node agent SKUs to return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="157b9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="157b9-123">-DefaultProfile</span></span>
<span data-ttu-id="157b9-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="157b9-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="157b9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="157b9-125">CommonParameters</span></span>
<span data-ttu-id="157b9-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="157b9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="157b9-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="157b9-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="157b9-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="157b9-128">INPUTS</span></span>

### <span data-ttu-id="157b9-129">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="157b9-129">BatchAccountContext</span></span>
<span data-ttu-id="157b9-130">O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="157b9-130">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="157b9-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="157b9-131">OUTPUTS</span></span>

### <span data-ttu-id="157b9-132">Microsoft.Azure.Commands.Batch. Modelos. PSNodeAgentSku</span><span class="sxs-lookup"><span data-stu-id="157b9-132">Microsoft.Azure.Commands.Batch.Models.PSNodeAgentSku</span></span>

## <span data-ttu-id="157b9-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="157b9-133">NOTES</span></span>

## <span data-ttu-id="157b9-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="157b9-134">RELATED LINKS</span></span>

[<span data-ttu-id="157b9-135">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="157b9-135">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)


