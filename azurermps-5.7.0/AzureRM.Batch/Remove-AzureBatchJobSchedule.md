---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 97FA5983-0D73-4336-99DA-46E5992F06DC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJobSchedule.md
ms.openlocfilehash: 2e474462983f15c0d58f8ada60b907c100508c6e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429899"
---
# <span data-ttu-id="f2260-101">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f2260-101">Remove-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="f2260-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f2260-102">SYNOPSIS</span></span>
<span data-ttu-id="f2260-103">Remove um cronograma de trabalho em lotes.</span><span class="sxs-lookup"><span data-stu-id="f2260-103">Removes a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2260-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f2260-104">SYNTAX</span></span>

```
Remove-AzureBatchJobSchedule [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2260-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f2260-105">DESCRIPTION</span></span>
<span data-ttu-id="f2260-106">O cmdlet **Remove-AzureBatchJobSchedule** remove um cronograma de trabalho em lotes do Azure.</span><span class="sxs-lookup"><span data-stu-id="f2260-106">The **Remove-AzureBatchJobSchedule** cmdlet removes an Azure Batch job schedule.</span></span>

## <span data-ttu-id="f2260-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f2260-107">EXAMPLES</span></span>

## <span data-ttu-id="f2260-108">OS</span><span class="sxs-lookup"><span data-stu-id="f2260-108">PARAMETERS</span></span>

### <span data-ttu-id="f2260-109">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="f2260-109">-BatchContext</span></span>
<span data-ttu-id="f2260-110">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="f2260-110">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="f2260-111">Se você usar o cmdlet Get-AzureRmBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="f2260-111">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="f2260-112">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzureRmBatchAccountKeys para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="f2260-112">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="f2260-113">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="f2260-113">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="f2260-114">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="f2260-114">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f2260-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2260-115">-DefaultProfile</span></span>
<span data-ttu-id="f2260-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f2260-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2260-117">-Force</span><span class="sxs-lookup"><span data-stu-id="f2260-117">-Force</span></span>
<span data-ttu-id="f2260-118">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="f2260-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2260-119">-ID</span><span class="sxs-lookup"><span data-stu-id="f2260-119">-Id</span></span>
<span data-ttu-id="f2260-120">Especifica a ID do plano de trabalho a ser removido.</span><span class="sxs-lookup"><span data-stu-id="f2260-120">Specifies the ID of the job schedule to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2260-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f2260-121">-Confirm</span></span>
<span data-ttu-id="f2260-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2260-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2260-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2260-123">-WhatIf</span></span>
<span data-ttu-id="f2260-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f2260-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2260-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f2260-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2260-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2260-126">CommonParameters</span></span>
<span data-ttu-id="f2260-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2260-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2260-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2260-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2260-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f2260-129">INPUTS</span></span>

### <span data-ttu-id="f2260-130">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="f2260-130">BatchAccountContext</span></span>
<span data-ttu-id="f2260-131">O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="f2260-131">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="f2260-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f2260-132">OUTPUTS</span></span>

## <span data-ttu-id="f2260-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f2260-133">NOTES</span></span>

## <span data-ttu-id="f2260-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f2260-134">RELATED LINKS</span></span>

[<span data-ttu-id="f2260-135">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f2260-135">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="f2260-136">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f2260-136">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="f2260-137">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f2260-137">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="f2260-138">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f2260-138">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="f2260-139">Set-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f2260-139">Set-AzureBatchJobSchedule</span></span>](./Set-AzureBatchJobSchedule.md)

[<span data-ttu-id="f2260-140">Parar-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f2260-140">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)


