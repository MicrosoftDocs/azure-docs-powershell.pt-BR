---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 89F604DD-EE77-440D-BCC9-3F74D994C447
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurermbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchAccount.md
ms.openlocfilehash: 3e460cddb83eacc1a012aebd009cd087ba1b68d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440524"
---
# <span data-ttu-id="036b9-101">Remove-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="036b9-101">Remove-AzureRmBatchAccount</span></span>

## <span data-ttu-id="036b9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="036b9-102">SYNOPSIS</span></span>
<span data-ttu-id="036b9-103">Remove uma conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="036b9-103">Removes a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="036b9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="036b9-104">SYNTAX</span></span>

```
Remove-AzureRmBatchAccount [-AccountName] <String> [[-ResourceGroupName] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="036b9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="036b9-105">DESCRIPTION</span></span>
<span data-ttu-id="036b9-106">O cmdlet **Remove-AzureRmBatchAccount** remove uma conta em lotes do Azure.</span><span class="sxs-lookup"><span data-stu-id="036b9-106">The **Remove-AzureRmBatchAccount** cmdlet removes an Azure Batch account.</span></span>
<span data-ttu-id="036b9-107">Esse cmdlet o avisa antes de remover uma conta, a menos que você especifique o parâmetro *Force* .</span><span class="sxs-lookup"><span data-stu-id="036b9-107">This cmdlet prompts you before it removes an account, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="036b9-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="036b9-108">EXAMPLES</span></span>

### <span data-ttu-id="036b9-109">Exemplo 1: remover uma conta em lotes</span><span class="sxs-lookup"><span data-stu-id="036b9-109">Example 1: Remove a Batch account</span></span>
```
PS C:\>Remove-AzureRmBatchAccount -AccountName "pfuller"
```

<span data-ttu-id="036b9-110">Esse comando Remove a conta em lotes chamada pfuller.</span><span class="sxs-lookup"><span data-stu-id="036b9-110">This command removes the Batch account named pfuller.</span></span>
<span data-ttu-id="036b9-111">Esse comando solicita confirmação antes de excluir a conta.</span><span class="sxs-lookup"><span data-stu-id="036b9-111">This command prompts you for confirmation before it deletes the account.</span></span>

## <span data-ttu-id="036b9-112">OS</span><span class="sxs-lookup"><span data-stu-id="036b9-112">PARAMETERS</span></span>

### <span data-ttu-id="036b9-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="036b9-113">-AccountName</span></span>
<span data-ttu-id="036b9-114">Especifica o nome da conta em lotes que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="036b9-114">Specifies the name of the Batch account that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="036b9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="036b9-115">-DefaultProfile</span></span>
<span data-ttu-id="036b9-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="036b9-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="036b9-117">-Force</span><span class="sxs-lookup"><span data-stu-id="036b9-117">-Force</span></span>
<span data-ttu-id="036b9-118">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="036b9-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="036b9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="036b9-119">-ResourceGroupName</span></span>
<span data-ttu-id="036b9-120">Especifica o grupo de recursos da conta que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="036b9-120">Specifies the resource group of the account that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="036b9-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="036b9-121">-Confirm</span></span>
<span data-ttu-id="036b9-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="036b9-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="036b9-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="036b9-123">-WhatIf</span></span>
<span data-ttu-id="036b9-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="036b9-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="036b9-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="036b9-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="036b9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="036b9-126">CommonParameters</span></span>
<span data-ttu-id="036b9-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="036b9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="036b9-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="036b9-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="036b9-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="036b9-129">INPUTS</span></span>

### <span data-ttu-id="036b9-130">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="036b9-130">None</span></span>
<span data-ttu-id="036b9-131">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="036b9-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="036b9-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="036b9-132">OUTPUTS</span></span>

## <span data-ttu-id="036b9-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="036b9-133">NOTES</span></span>

## <span data-ttu-id="036b9-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="036b9-134">RELATED LINKS</span></span>

[<span data-ttu-id="036b9-135">Get-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="036b9-135">Get-AzureRmBatchAccount</span></span>](./Get-AzureRmBatchAccount.md)

[<span data-ttu-id="036b9-136">New-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="036b9-136">New-AzureRmBatchAccount</span></span>](./New-AzureRmBatchAccount.md)

[<span data-ttu-id="036b9-137">Set-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="036b9-137">Set-AzureRmBatchAccount</span></span>](./Set-AzureRmBatchAccount.md)

[<span data-ttu-id="036b9-138">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="036b9-138">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


