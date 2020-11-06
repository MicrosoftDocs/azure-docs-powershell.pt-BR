---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 89F604DD-EE77-440D-BCC9-3F74D994C447
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurermbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchAccount.md
ms.openlocfilehash: 3528d66c635de78347647f0d1e451dc0b173a641
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427290"
---
# <span data-ttu-id="28671-101">Remove-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="28671-101">Remove-AzureRmBatchAccount</span></span>

## <span data-ttu-id="28671-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="28671-102">SYNOPSIS</span></span>
<span data-ttu-id="28671-103">Remove uma conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="28671-103">Removes a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28671-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="28671-104">SYNTAX</span></span>

```
Remove-AzureRmBatchAccount [-AccountName] <String> [[-ResourceGroupName] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28671-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="28671-105">DESCRIPTION</span></span>
<span data-ttu-id="28671-106">O cmdlet **Remove-AzureRmBatchAccount** remove uma conta em lotes do Azure.</span><span class="sxs-lookup"><span data-stu-id="28671-106">The **Remove-AzureRmBatchAccount** cmdlet removes an Azure Batch account.</span></span>
<span data-ttu-id="28671-107">Esse cmdlet o avisa antes de remover uma conta, a menos que você especifique o parâmetro *Force* .</span><span class="sxs-lookup"><span data-stu-id="28671-107">This cmdlet prompts you before it removes an account, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="28671-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="28671-108">EXAMPLES</span></span>

### <span data-ttu-id="28671-109">Exemplo 1: remover uma conta em lotes</span><span class="sxs-lookup"><span data-stu-id="28671-109">Example 1: Remove a Batch account</span></span>
```
PS C:\>Remove-AzureRmBatchAccount -AccountName "pfuller"
```

<span data-ttu-id="28671-110">Esse comando Remove a conta em lotes chamada pfuller.</span><span class="sxs-lookup"><span data-stu-id="28671-110">This command removes the Batch account named pfuller.</span></span>
<span data-ttu-id="28671-111">Esse comando solicita confirmação antes de excluir a conta.</span><span class="sxs-lookup"><span data-stu-id="28671-111">This command prompts you for confirmation before it deletes the account.</span></span>

## <span data-ttu-id="28671-112">OS</span><span class="sxs-lookup"><span data-stu-id="28671-112">PARAMETERS</span></span>

### <span data-ttu-id="28671-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="28671-113">-AccountName</span></span>
<span data-ttu-id="28671-114">Especifica o nome da conta em lotes que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="28671-114">Specifies the name of the Batch account that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28671-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28671-115">-DefaultProfile</span></span>
<span data-ttu-id="28671-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="28671-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="28671-117">-Force</span><span class="sxs-lookup"><span data-stu-id="28671-117">-Force</span></span>
<span data-ttu-id="28671-118">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="28671-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="28671-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28671-119">-ResourceGroupName</span></span>
<span data-ttu-id="28671-120">Especifica o grupo de recursos da conta que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="28671-120">Specifies the resource group of the account that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28671-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="28671-121">-Confirm</span></span>
<span data-ttu-id="28671-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28671-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28671-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28671-123">-WhatIf</span></span>
<span data-ttu-id="28671-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="28671-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28671-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="28671-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28671-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28671-126">CommonParameters</span></span>
<span data-ttu-id="28671-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28671-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28671-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28671-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28671-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="28671-129">INPUTS</span></span>

### <span data-ttu-id="28671-130">System. String</span><span class="sxs-lookup"><span data-stu-id="28671-130">System.String</span></span>

## <span data-ttu-id="28671-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="28671-131">OUTPUTS</span></span>

### <span data-ttu-id="28671-132">System. void</span><span class="sxs-lookup"><span data-stu-id="28671-132">System.Void</span></span>

## <span data-ttu-id="28671-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="28671-133">NOTES</span></span>

## <span data-ttu-id="28671-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="28671-134">RELATED LINKS</span></span>

[<span data-ttu-id="28671-135">Get-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="28671-135">Get-AzureRmBatchAccount</span></span>](./Get-AzureRmBatchAccount.md)

[<span data-ttu-id="28671-136">New-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="28671-136">New-AzureRmBatchAccount</span></span>](./New-AzureRmBatchAccount.md)

[<span data-ttu-id="28671-137">Set-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="28671-137">Set-AzureRmBatchAccount</span></span>](./Set-AzureRmBatchAccount.md)

[<span data-ttu-id="28671-138">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="28671-138">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)

