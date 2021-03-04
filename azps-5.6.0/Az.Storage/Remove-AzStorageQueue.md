---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 22975A89-CAFF-4F18-8DCE-B695413FBAC7
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueue.md
ms.openlocfilehash: d66203d712de76004d009b98fdc14a18cc69e461
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886547"
---
# <span data-ttu-id="2c9af-101">Remove-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="2c9af-101">Remove-AzStorageQueue</span></span>

## <span data-ttu-id="2c9af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c9af-102">SYNOPSIS</span></span>
<span data-ttu-id="2c9af-103">Remove uma fila de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="2c9af-103">Removes a storage queue.</span></span>

## <span data-ttu-id="2c9af-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="2c9af-104">SYNTAX</span></span>

```
Remove-AzStorageQueue [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c9af-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="2c9af-105">DESCRIPTION</span></span>
<span data-ttu-id="2c9af-106">O cmdlet **Remove-AzStorageQueue** remove uma fila de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="2c9af-106">The **Remove-AzStorageQueue** cmdlet removes a storage queue.</span></span>

## <span data-ttu-id="2c9af-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2c9af-107">EXAMPLES</span></span>

### <span data-ttu-id="2c9af-108">Exemplo 1: Remover uma fila de armazenamento pelo nome</span><span class="sxs-lookup"><span data-stu-id="2c9af-108">Example 1: Remove a storage queue by name</span></span>
```
PS C:\>Remove-AzStorageQueue "ContosoQueue01"
```

<span data-ttu-id="2c9af-109">Este comando remove uma fila chamada ContosoQueue01.</span><span class="sxs-lookup"><span data-stu-id="2c9af-109">This command removes a queue named ContosoQueue01.</span></span>

### <span data-ttu-id="2c9af-110">Exemplo 2: Remover várias filas de armazenamento</span><span class="sxs-lookup"><span data-stu-id="2c9af-110">Example 2: Remove multiple storage queues</span></span>
```
PS C:\>Get-AzStorageQueue "Contoso*" | Remove-AzStorageQueue
```

<span data-ttu-id="2c9af-111">Este comando remove todas as filas com nomes que começam com a Contoso.</span><span class="sxs-lookup"><span data-stu-id="2c9af-111">This command removes all queues with names that start with Contoso.</span></span>

## <span data-ttu-id="2c9af-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="2c9af-112">PARAMETERS</span></span>

### <span data-ttu-id="2c9af-113">-Context</span><span class="sxs-lookup"><span data-stu-id="2c9af-113">-Context</span></span>
<span data-ttu-id="2c9af-114">Especifica o contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="2c9af-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="2c9af-115">Para obter o contexto de armazenamento, o New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c9af-115">To obtain the storage context, the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="2c9af-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c9af-116">-DefaultProfile</span></span>
<span data-ttu-id="2c9af-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2c9af-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c9af-118">-Force</span><span class="sxs-lookup"><span data-stu-id="2c9af-118">-Force</span></span>
<span data-ttu-id="2c9af-119">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="2c9af-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2c9af-120">-Name</span><span class="sxs-lookup"><span data-stu-id="2c9af-120">-Name</span></span>
<span data-ttu-id="2c9af-121">Especifica o nome da fila a ser removido.</span><span class="sxs-lookup"><span data-stu-id="2c9af-121">Specifies the name of the queue to remove.</span></span>

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

### <span data-ttu-id="2c9af-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2c9af-122">-PassThru</span></span>
<span data-ttu-id="2c9af-123">Indica que esse cmdlet retorna um **Boolean** que reflete o sucesso da operação.</span><span class="sxs-lookup"><span data-stu-id="2c9af-123">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="2c9af-124">Por padrão, esse cmdlet não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="2c9af-124">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="2c9af-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2c9af-125">-Confirm</span></span>
<span data-ttu-id="2c9af-126">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c9af-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c9af-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c9af-127">-WhatIf</span></span>
<span data-ttu-id="2c9af-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2c9af-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c9af-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2c9af-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c9af-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c9af-130">CommonParameters</span></span>
<span data-ttu-id="2c9af-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c9af-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c9af-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c9af-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c9af-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2c9af-133">INPUTS</span></span>

### <span data-ttu-id="2c9af-134">System.String</span><span class="sxs-lookup"><span data-stu-id="2c9af-134">System.String</span></span>

### <span data-ttu-id="2c9af-135">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="2c9af-135">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="2c9af-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="2c9af-136">OUTPUTS</span></span>

### <span data-ttu-id="2c9af-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2c9af-137">System.Boolean</span></span>

## <span data-ttu-id="2c9af-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="2c9af-138">NOTES</span></span>

## <span data-ttu-id="2c9af-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2c9af-139">RELATED LINKS</span></span>

[<span data-ttu-id="2c9af-140">Get-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="2c9af-140">Get-AzStorageQueue</span></span>](./Get-AzStorageQueue.md)

[<span data-ttu-id="2c9af-141">New-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="2c9af-141">New-AzStorageQueue</span></span>](./New-AzStorageQueue.md)
