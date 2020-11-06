---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 97FA5983-0D73-4336-99DA-46E5992F06DC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJobSchedule.md
ms.openlocfilehash: 59a906420e2326564e779c9358e07a5003946b28
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602318"
---
# <span data-ttu-id="da152-101">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="da152-101">Remove-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="da152-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="da152-102">SYNOPSIS</span></span>
<span data-ttu-id="da152-103">Remove um cronograma de trabalho em lotes.</span><span class="sxs-lookup"><span data-stu-id="da152-103">Removes a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da152-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="da152-104">SYNTAX</span></span>

```
Remove-AzureBatchJobSchedule [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da152-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="da152-105">DESCRIPTION</span></span>
<span data-ttu-id="da152-106">O cmdlet **Remove-AzureBatchJobSchedule** remove um cronograma de trabalho em lotes do Azure.</span><span class="sxs-lookup"><span data-stu-id="da152-106">The **Remove-AzureBatchJobSchedule** cmdlet removes an Azure Batch job schedule.</span></span>

## <span data-ttu-id="da152-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="da152-107">EXAMPLES</span></span>

## <span data-ttu-id="da152-108">OS</span><span class="sxs-lookup"><span data-stu-id="da152-108">PARAMETERS</span></span>

### <span data-ttu-id="da152-109">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="da152-109">-BatchContext</span></span>
<span data-ttu-id="da152-110">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="da152-110">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="da152-111">Se você usar o cmdlet Get-AzureRmBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="da152-111">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="da152-112">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzureRmBatchAccountKeys para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="da152-112">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="da152-113">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="da152-113">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="da152-114">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="da152-114">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="da152-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da152-115">-DefaultProfile</span></span>
<span data-ttu-id="da152-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="da152-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da152-117">-Force</span><span class="sxs-lookup"><span data-stu-id="da152-117">-Force</span></span>
<span data-ttu-id="da152-118">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="da152-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="da152-119">-ID</span><span class="sxs-lookup"><span data-stu-id="da152-119">-Id</span></span>
<span data-ttu-id="da152-120">Especifica a ID do plano de trabalho a ser removido.</span><span class="sxs-lookup"><span data-stu-id="da152-120">Specifies the ID of the job schedule to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da152-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="da152-121">-Confirm</span></span>
<span data-ttu-id="da152-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da152-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da152-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da152-123">-WhatIf</span></span>
<span data-ttu-id="da152-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="da152-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da152-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="da152-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da152-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da152-126">CommonParameters</span></span>
<span data-ttu-id="da152-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da152-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da152-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da152-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da152-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="da152-129">INPUTS</span></span>

### <span data-ttu-id="da152-130">System. String</span><span class="sxs-lookup"><span data-stu-id="da152-130">System.String</span></span>

### <span data-ttu-id="da152-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="da152-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="da152-132">Parâmetros: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="da152-132">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="da152-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="da152-133">OUTPUTS</span></span>

### <span data-ttu-id="da152-134">System. void</span><span class="sxs-lookup"><span data-stu-id="da152-134">System.Void</span></span>

## <span data-ttu-id="da152-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="da152-135">NOTES</span></span>

## <span data-ttu-id="da152-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="da152-136">RELATED LINKS</span></span>

[<span data-ttu-id="da152-137">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="da152-137">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="da152-138">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="da152-138">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="da152-139">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="da152-139">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="da152-140">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="da152-140">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="da152-141">Set-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="da152-141">Set-AzureBatchJobSchedule</span></span>](./Set-AzureBatchJobSchedule.md)

[<span data-ttu-id="da152-142">Parar-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="da152-142">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)


