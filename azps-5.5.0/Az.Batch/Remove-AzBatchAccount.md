---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 89F604DD-EE77-440D-BCC9-3F74D994C447
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchAccount.md
ms.openlocfilehash: ae67aac391f2cce2a37be8a5a15a0fd0ea37cdd9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117933"
---
# <span data-ttu-id="b6ece-101">Remove-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="b6ece-101">Remove-AzBatchAccount</span></span>

## <span data-ttu-id="b6ece-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b6ece-102">SYNOPSIS</span></span>
<span data-ttu-id="b6ece-103">Remove uma conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="b6ece-103">Removes a Batch account.</span></span>

## <span data-ttu-id="b6ece-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b6ece-104">SYNTAX</span></span>

```
Remove-AzBatchAccount [-AccountName] <String> [[-ResourceGroupName] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6ece-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="b6ece-105">DESCRIPTION</span></span>
<span data-ttu-id="b6ece-106">O **cmdlet Remove-AzBatchAccount** remove uma conta do Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="b6ece-106">The **Remove-AzBatchAccount** cmdlet removes an Azure Batch account.</span></span>
<span data-ttu-id="b6ece-107">Este cmdlet solicita antes de remover uma conta, a menos que você especifique o *parâmetro Force.*</span><span class="sxs-lookup"><span data-stu-id="b6ece-107">This cmdlet prompts you before it removes an account, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="b6ece-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b6ece-108">EXAMPLES</span></span>

### <span data-ttu-id="b6ece-109">Exemplo 1: Remover uma conta em lotes</span><span class="sxs-lookup"><span data-stu-id="b6ece-109">Example 1: Remove a Batch account</span></span>
```
PS C:\>Remove-AzBatchAccount -AccountName "pfuller"
```

<span data-ttu-id="b6ece-110">Esse comando remove a conta Em lotes chamada pfuller.</span><span class="sxs-lookup"><span data-stu-id="b6ece-110">This command removes the Batch account named pfuller.</span></span>
<span data-ttu-id="b6ece-111">Esse comando solicita a confirmação antes de excluir a conta.</span><span class="sxs-lookup"><span data-stu-id="b6ece-111">This command prompts you for confirmation before it deletes the account.</span></span>

## <span data-ttu-id="b6ece-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b6ece-112">PARAMETERS</span></span>

### <span data-ttu-id="b6ece-113">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="b6ece-113">-AccountName</span></span>
<span data-ttu-id="b6ece-114">Especifica o nome da conta em lotes que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="b6ece-114">Specifies the name of the Batch account that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b6ece-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6ece-115">-DefaultProfile</span></span>
<span data-ttu-id="b6ece-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="b6ece-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6ece-117">-Forçar</span><span class="sxs-lookup"><span data-stu-id="b6ece-117">-Force</span></span>
<span data-ttu-id="b6ece-118">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="b6ece-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b6ece-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6ece-119">-ResourceGroupName</span></span>
<span data-ttu-id="b6ece-120">Especifica o grupo de recursos da conta que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="b6ece-120">Specifies the resource group of the account that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b6ece-121">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="b6ece-121">-Confirm</span></span>
<span data-ttu-id="b6ece-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6ece-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6ece-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6ece-123">-WhatIf</span></span>
<span data-ttu-id="b6ece-124">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="b6ece-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6ece-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b6ece-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6ece-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6ece-126">CommonParameters</span></span>
<span data-ttu-id="b6ece-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6ece-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6ece-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b6ece-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6ece-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="b6ece-129">INPUTS</span></span>

### <span data-ttu-id="b6ece-130">System.String</span><span class="sxs-lookup"><span data-stu-id="b6ece-130">System.String</span></span>

## <span data-ttu-id="b6ece-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="b6ece-131">OUTPUTS</span></span>

### <span data-ttu-id="b6ece-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="b6ece-132">System.Void</span></span>

## <span data-ttu-id="b6ece-133">Notas</span><span class="sxs-lookup"><span data-stu-id="b6ece-133">NOTES</span></span>

## <span data-ttu-id="b6ece-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b6ece-134">RELATED LINKS</span></span>

[<span data-ttu-id="b6ece-135">Get-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="b6ece-135">Get-AzBatchAccount</span></span>](./Get-AzBatchAccount.md)

[<span data-ttu-id="b6ece-136">New-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="b6ece-136">New-AzBatchAccount</span></span>](./New-AzBatchAccount.md)

[<span data-ttu-id="b6ece-137">Set-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="b6ece-137">Set-AzBatchAccount</span></span>](./Set-AzBatchAccount.md)

[<span data-ttu-id="b6ece-138">Cmdlets de lote do Azure</span><span class="sxs-lookup"><span data-stu-id="b6ece-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
