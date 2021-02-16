---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 22975A89-CAFF-4F18-8DCE-B695413FBAC7
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueue.md
ms.openlocfilehash: 2cc10a1b72dc369aef08b84e7b8fe2128ff0ac33
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116320"
---
# <span data-ttu-id="26b7c-101">Remove-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="26b7c-101">Remove-AzStorageQueue</span></span>

## <span data-ttu-id="26b7c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="26b7c-102">SYNOPSIS</span></span>
<span data-ttu-id="26b7c-103">Remove uma fila de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="26b7c-103">Removes a storage queue.</span></span>

## <span data-ttu-id="26b7c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="26b7c-104">SYNTAX</span></span>

```
Remove-AzStorageQueue [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26b7c-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="26b7c-105">DESCRIPTION</span></span>
<span data-ttu-id="26b7c-106">O cmdlet **Remove-AzStorageQueue** remove uma fila de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="26b7c-106">The **Remove-AzStorageQueue** cmdlet removes a storage queue.</span></span>

## <span data-ttu-id="26b7c-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="26b7c-107">EXAMPLES</span></span>

### <span data-ttu-id="26b7c-108">Exemplo 1: Remover uma fila de armazenamento por nome</span><span class="sxs-lookup"><span data-stu-id="26b7c-108">Example 1: Remove a storage queue by name</span></span>
```
PS C:\>Remove-AzStorageQueue "ContosoQueue01"
```

<span data-ttu-id="26b7c-109">Esse comando remove uma fila chamada ContosoQueue01.</span><span class="sxs-lookup"><span data-stu-id="26b7c-109">This command removes a queue named ContosoQueue01.</span></span>

### <span data-ttu-id="26b7c-110">Exemplo 2: Remover várias filas de armazenamento</span><span class="sxs-lookup"><span data-stu-id="26b7c-110">Example 2: Remove multiple storage queues</span></span>
```
PS C:\>Get-AzStorageQueue "Contoso*" | Remove-AzStorageQueue
```

<span data-ttu-id="26b7c-111">Esse comando remove todas as filas com nomes que começam com a Contoso.</span><span class="sxs-lookup"><span data-stu-id="26b7c-111">This command removes all queues with names that start with Contoso.</span></span>

## <span data-ttu-id="26b7c-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="26b7c-112">PARAMETERS</span></span>

### <span data-ttu-id="26b7c-113">-Contexto</span><span class="sxs-lookup"><span data-stu-id="26b7c-113">-Context</span></span>
<span data-ttu-id="26b7c-114">Especifica o contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="26b7c-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="26b7c-115">Para obter o contexto de armazenamento, o New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26b7c-115">To obtain the storage context, the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="26b7c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26b7c-116">-DefaultProfile</span></span>
<span data-ttu-id="26b7c-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="26b7c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26b7c-118">-Forçar</span><span class="sxs-lookup"><span data-stu-id="26b7c-118">-Force</span></span>
<span data-ttu-id="26b7c-119">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="26b7c-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="26b7c-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="26b7c-120">-Name</span></span>
<span data-ttu-id="26b7c-121">Especifica o nome da fila a ser removido.</span><span class="sxs-lookup"><span data-stu-id="26b7c-121">Specifies the name of the queue to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="26b7c-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="26b7c-122">-PassThru</span></span>
<span data-ttu-id="26b7c-123">Indica que esse cmdlet retorna um **boolano** que reflete o sucesso da operação.</span><span class="sxs-lookup"><span data-stu-id="26b7c-123">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="26b7c-124">Por padrão, esse cmdlet não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="26b7c-124">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="26b7c-125">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="26b7c-125">-Confirm</span></span>
<span data-ttu-id="26b7c-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26b7c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26b7c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26b7c-127">-WhatIf</span></span>
<span data-ttu-id="26b7c-128">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="26b7c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26b7c-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="26b7c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26b7c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26b7c-130">CommonParameters</span></span>
<span data-ttu-id="26b7c-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26b7c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26b7c-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26b7c-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26b7c-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="26b7c-133">INPUTS</span></span>

### <span data-ttu-id="26b7c-134">System.String</span><span class="sxs-lookup"><span data-stu-id="26b7c-134">System.String</span></span>

### <span data-ttu-id="26b7c-135">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="26b7c-135">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="26b7c-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="26b7c-136">OUTPUTS</span></span>

### <span data-ttu-id="26b7c-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="26b7c-137">System.Boolean</span></span>

## <span data-ttu-id="26b7c-138">Notas</span><span class="sxs-lookup"><span data-stu-id="26b7c-138">NOTES</span></span>

## <span data-ttu-id="26b7c-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="26b7c-139">RELATED LINKS</span></span>

[<span data-ttu-id="26b7c-140">Get-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="26b7c-140">Get-AzStorageQueue</span></span>](./Get-AzStorageQueue.md)

[<span data-ttu-id="26b7c-141">New-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="26b7c-141">New-AzStorageQueue</span></span>](./New-AzStorageQueue.md)
