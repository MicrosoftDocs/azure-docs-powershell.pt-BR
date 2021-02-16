---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 9C755BE8-0624-4CF7-AE7C-34DAF44678E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchAutoScale.md
ms.openlocfilehash: c0a0f0a11b4caf18b12c21d37dd18ef153220a97
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117987"
---
# <span data-ttu-id="d030d-101">Disable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="d030d-101">Disable-AzBatchAutoScale</span></span>

## <span data-ttu-id="d030d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d030d-102">SYNOPSIS</span></span>
<span data-ttu-id="d030d-103">Desabilita o dimensionamento automático de um pool.</span><span class="sxs-lookup"><span data-stu-id="d030d-103">Disables automatic scaling of a pool.</span></span>

## <span data-ttu-id="d030d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d030d-104">SYNTAX</span></span>

```
Disable-AzBatchAutoScale [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d030d-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="d030d-105">DESCRIPTION</span></span>
<span data-ttu-id="d030d-106">O **cmdlet Disable-AzBatchAutoScale** desabilita o dimensionamento automático do pool especificado.</span><span class="sxs-lookup"><span data-stu-id="d030d-106">The **Disable-AzBatchAutoScale** cmdlet disables automatic scaling of the specified pool.</span></span>

## <span data-ttu-id="d030d-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d030d-107">EXAMPLES</span></span>

### <span data-ttu-id="d030d-108">Exemplo 1: Desabilitar o dimensionamento automático de um pool</span><span class="sxs-lookup"><span data-stu-id="d030d-108">Example 1: Disable automatic scaling of a pool</span></span>
```
PS C:\>Disable-AzBatchAutoScale -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="d030d-109">Esse comando desabilita o dimensionamento automático do pool chamado MyPool.</span><span class="sxs-lookup"><span data-stu-id="d030d-109">This command disables automatic scaling for the pool named MyPool.</span></span>

## <span data-ttu-id="d030d-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d030d-110">PARAMETERS</span></span>

### <span data-ttu-id="d030d-111">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="d030d-111">-BatchContext</span></span>
<span data-ttu-id="d030d-112">Especifica a instância **BatchAccountContext** que esse cmdlet usa para interagir com o serviço Lote.</span><span class="sxs-lookup"><span data-stu-id="d030d-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="d030d-113">Se você usar o cmdlet Get-AzBatchAccount para obter seu BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço Lote.</span><span class="sxs-lookup"><span data-stu-id="d030d-113">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="d030d-114">Para usar a autenticação de chave compartilhada, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com suas teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="d030d-114">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="d030d-115">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="d030d-115">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="d030d-116">Para alterar a chave a ser usada, de definir a propriedade BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="d030d-116">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="d030d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d030d-117">-DefaultProfile</span></span>
<span data-ttu-id="d030d-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="d030d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d030d-119">-ID</span><span class="sxs-lookup"><span data-stu-id="d030d-119">-Id</span></span>
<span data-ttu-id="d030d-120">Especifica a ID do objeto do pool.</span><span class="sxs-lookup"><span data-stu-id="d030d-120">Specifies the object ID of the pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d030d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d030d-121">CommonParameters</span></span>
<span data-ttu-id="d030d-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d030d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d030d-123">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d030d-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d030d-124">Entradas</span><span class="sxs-lookup"><span data-stu-id="d030d-124">INPUTS</span></span>

### <span data-ttu-id="d030d-125">System.String</span><span class="sxs-lookup"><span data-stu-id="d030d-125">System.String</span></span>

### <span data-ttu-id="d030d-126">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="d030d-126">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="d030d-127">Saídas</span><span class="sxs-lookup"><span data-stu-id="d030d-127">OUTPUTS</span></span>

### <span data-ttu-id="d030d-128">System.Void</span><span class="sxs-lookup"><span data-stu-id="d030d-128">System.Void</span></span>

## <span data-ttu-id="d030d-129">Notas</span><span class="sxs-lookup"><span data-stu-id="d030d-129">NOTES</span></span>

## <span data-ttu-id="d030d-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d030d-130">RELATED LINKS</span></span>

[<span data-ttu-id="d030d-131">Enable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="d030d-131">Enable-AzBatchAutoScale</span></span>](./Enable-AzBatchAutoScale.md)

[<span data-ttu-id="d030d-132">Test-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="d030d-132">Test-AzBatchAutoScale</span></span>](./Test-AzBatchAutoScale.md)

[<span data-ttu-id="d030d-133">Cmdlets de lote do Azure</span><span class="sxs-lookup"><span data-stu-id="d030d-133">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)


