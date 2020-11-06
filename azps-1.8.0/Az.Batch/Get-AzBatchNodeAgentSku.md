---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 5C6D3792-AA56-4210-B376-D9E656B04FBD
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchnodeagentsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeAgentSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeAgentSku.md
ms.openlocfilehash: 8f7228a540456e76e4f7a22d70d00969a9ef568c
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93601884"
---
# <span data-ttu-id="bb58b-101">Get-AzBatchNodeAgentSku</span><span class="sxs-lookup"><span data-stu-id="bb58b-101">Get-AzBatchNodeAgentSku</span></span>

## <span data-ttu-id="bb58b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bb58b-102">SYNOPSIS</span></span>
<span data-ttu-id="bb58b-103">Obtém SKUs do agente de nó de lote disponíveis em uma conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="bb58b-103">Gets Batch node agent SKUs available in a Batch account.</span></span>

## <span data-ttu-id="bb58b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bb58b-104">SYNTAX</span></span>

```
Get-AzBatchNodeAgentSku [-Filter <String>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb58b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bb58b-105">DESCRIPTION</span></span>
<span data-ttu-id="bb58b-106">O cmdlet **Get-AzBatchNodeAgentSku** Obtém SKUs do agente de nó que estão disponíveis em uma conta em lotes do Azure.</span><span class="sxs-lookup"><span data-stu-id="bb58b-106">The **Get-AzBatchNodeAgentSku** cmdlet gets node agent SKUs that are available in an Azure Batch account.</span></span>
<span data-ttu-id="bb58b-107">Especifique a conta usando o parâmetro *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="bb58b-107">Specify the account by using the *BatchContext* parameter.</span></span>
<span data-ttu-id="bb58b-108">Você pode restringir a pesquisa a SKUs que correspondam a um filtro do Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="bb58b-108">You can narrow your search to SKUs that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="bb58b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bb58b-109">EXAMPLES</span></span>

### <span data-ttu-id="bb58b-110">Exemplo 1: obter todas as SKUs de agente de nó disponíveis</span><span class="sxs-lookup"><span data-stu-id="bb58b-110">Example 1: Get all available node agent SKUs</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchNodeAgentSku -BatchContext $Context 
batch.node.centos 7 Linux {7.0, 7.1, 7.2, OL70} 
batch.node.debian 8 Linux {15.10, 8} 
batch.node.opensuse 13.2 Linux {13.2} 
batch.node.opensuse 42.1 Linux {42.1, 12, 12-SP1, 12} 
batch.node.ubuntu 14.04 Linux {14.04.0-LTS, 14.04.1-LTS, 14.04.2-LTS, 14.04.3-LTS...} 
batch.node.windows amd64 Windows {2008-R2-SP1, 2012-Datacenter, 2012-R2-Datacenter, Windows-Server-Technical-Preview}
```

<span data-ttu-id="bb58b-111">O primeiro comando obtém um contexto de conta em lotes que contém as chaves de acesso para a sua assinatura usando **Get-AzBatchAccountKeys**.</span><span class="sxs-lookup"><span data-stu-id="bb58b-111">The first command gets a batch account context that contains access keys for your subscription by using **Get-AzBatchAccountKeys**.</span></span>
<span data-ttu-id="bb58b-112">O comando armazena o contexto na variável $Context para usar no próximo comando.</span><span class="sxs-lookup"><span data-stu-id="bb58b-112">The command stores the context in the $Context variable to use in the next command.</span></span>
<span data-ttu-id="bb58b-113">O segundo comando obtém todas as SKUs de agente de nó disponíveis com suporte em lote.</span><span class="sxs-lookup"><span data-stu-id="bb58b-113">The second command gets all available node agent SKUs that Batch supports.</span></span>

## <span data-ttu-id="bb58b-114">OS</span><span class="sxs-lookup"><span data-stu-id="bb58b-114">PARAMETERS</span></span>

### <span data-ttu-id="bb58b-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="bb58b-115">-BatchContext</span></span>
<span data-ttu-id="bb58b-116">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="bb58b-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="bb58b-117">Se você usar o cmdlet Get-AzBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="bb58b-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="bb58b-118">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzBatchAccountKeys para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="bb58b-118">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="bb58b-119">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="bb58b-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="bb58b-120">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="bb58b-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="bb58b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb58b-121">-DefaultProfile</span></span>
<span data-ttu-id="bb58b-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bb58b-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb58b-123">-Filtro</span><span class="sxs-lookup"><span data-stu-id="bb58b-123">-Filter</span></span>
<span data-ttu-id="bb58b-124">Especifica uma cláusula de filtro OData para SKUs de agente de nó.</span><span class="sxs-lookup"><span data-stu-id="bb58b-124">Specifies an OData filter clause for node agent SKUs.</span></span>
<span data-ttu-id="bb58b-125">Se você não especificar um filtro, esse cmdlet retornará todas as SKUs do agente de nó que dão suporte a lote.</span><span class="sxs-lookup"><span data-stu-id="bb58b-125">If you do not specify a filter, this cmdlet returns all node agent SKUs that Batch supports.</span></span>

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

### <span data-ttu-id="bb58b-126">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="bb58b-126">-MaxCount</span></span>
<span data-ttu-id="bb58b-127">Especifica o número máximo de SKUs do agente de nó a serem retornadas.</span><span class="sxs-lookup"><span data-stu-id="bb58b-127">Specifies the maximum number of node agent SKUs to return.</span></span>

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

### <span data-ttu-id="bb58b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb58b-128">CommonParameters</span></span>
<span data-ttu-id="bb58b-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb58b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb58b-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb58b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb58b-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bb58b-131">INPUTS</span></span>

### <span data-ttu-id="bb58b-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="bb58b-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="bb58b-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bb58b-133">OUTPUTS</span></span>

### <span data-ttu-id="bb58b-134">Microsoft.Azure.Commands.Batch. Modelos. PSNodeAgentSku</span><span class="sxs-lookup"><span data-stu-id="bb58b-134">Microsoft.Azure.Commands.Batch.Models.PSNodeAgentSku</span></span>

## <span data-ttu-id="bb58b-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bb58b-135">NOTES</span></span>

## <span data-ttu-id="bb58b-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bb58b-136">RELATED LINKS</span></span>

[<span data-ttu-id="bb58b-137">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="bb58b-137">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)


