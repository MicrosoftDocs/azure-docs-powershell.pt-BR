---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 97FA5983-0D73-4336-99DA-46E5992F06DC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJobSchedule.md
ms.openlocfilehash: 673d9e5034b1e7c97d3b6b7cfdd6f89e9a79a34f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602770"
---
# <span data-ttu-id="71433-101">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="71433-101">Remove-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="71433-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="71433-102">SYNOPSIS</span></span>
<span data-ttu-id="71433-103">Remove um cronograma de trabalho em lotes.</span><span class="sxs-lookup"><span data-stu-id="71433-103">Removes a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71433-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="71433-104">SYNTAX</span></span>

```
Remove-AzureBatchJobSchedule [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71433-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="71433-105">DESCRIPTION</span></span>
<span data-ttu-id="71433-106">O cmdlet **Remove-AzureBatchJobSchedule** remove um cronograma de trabalho em lotes do Azure.</span><span class="sxs-lookup"><span data-stu-id="71433-106">The **Remove-AzureBatchJobSchedule** cmdlet removes an Azure Batch job schedule.</span></span>

## <span data-ttu-id="71433-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="71433-107">EXAMPLES</span></span>

## <span data-ttu-id="71433-108">OS</span><span class="sxs-lookup"><span data-stu-id="71433-108">PARAMETERS</span></span>

### <span data-ttu-id="71433-109">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="71433-109">-BatchContext</span></span>
<span data-ttu-id="71433-110">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="71433-110">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="71433-111">Para obter um objeto **BatchAccountContext** que contém as teclas de acesso para a sua assinatura, use o cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="71433-111">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="71433-112">-Force</span><span class="sxs-lookup"><span data-stu-id="71433-112">-Force</span></span>
<span data-ttu-id="71433-113">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="71433-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="71433-114">-ID</span><span class="sxs-lookup"><span data-stu-id="71433-114">-Id</span></span>
<span data-ttu-id="71433-115">Especifica a ID do plano de trabalho a ser removido.</span><span class="sxs-lookup"><span data-stu-id="71433-115">Specifies the ID of the job schedule to remove.</span></span>

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

### <span data-ttu-id="71433-116">-Confirme</span><span class="sxs-lookup"><span data-stu-id="71433-116">-Confirm</span></span>
<span data-ttu-id="71433-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71433-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71433-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71433-118">-WhatIf</span></span>
<span data-ttu-id="71433-119">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="71433-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71433-120">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="71433-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71433-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71433-121">-DefaultProfile</span></span>
<span data-ttu-id="71433-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="71433-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71433-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71433-123">CommonParameters</span></span>
<span data-ttu-id="71433-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71433-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71433-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71433-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71433-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="71433-126">INPUTS</span></span>

### <span data-ttu-id="71433-127">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="71433-127">BatchAccountContext</span></span>
<span data-ttu-id="71433-128">O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="71433-128">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="71433-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="71433-129">OUTPUTS</span></span>

## <span data-ttu-id="71433-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="71433-130">NOTES</span></span>

## <span data-ttu-id="71433-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="71433-131">RELATED LINKS</span></span>

[<span data-ttu-id="71433-132">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="71433-132">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="71433-133">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="71433-133">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="71433-134">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="71433-134">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="71433-135">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="71433-135">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="71433-136">Set-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="71433-136">Set-AzureBatchJobSchedule</span></span>](./Set-AzureBatchJobSchedule.md)

[<span data-ttu-id="71433-137">Parar-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="71433-137">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)


