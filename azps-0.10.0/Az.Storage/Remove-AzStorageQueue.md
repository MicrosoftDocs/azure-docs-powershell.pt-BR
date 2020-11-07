---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 22975A89-CAFF-4F18-8DCE-B695413FBAC7
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Remove-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Remove-AzStorageQueue.md
ms.openlocfilehash: 8f455599501c84792a9ead7f467fee9fe9e35dd0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776183"
---
# <span data-ttu-id="884b0-101">Remove-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="884b0-101">Remove-AzStorageQueue</span></span>

## <span data-ttu-id="884b0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="884b0-102">SYNOPSIS</span></span>
<span data-ttu-id="884b0-103">Remove uma fila de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="884b0-103">Removes a storage queue.</span></span>

## <span data-ttu-id="884b0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="884b0-104">SYNTAX</span></span>

```
Remove-AzStorageQueue [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="884b0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="884b0-105">DESCRIPTION</span></span>
<span data-ttu-id="884b0-106">O cmdlet **Remove-AzStorageQueue** remove uma fila de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="884b0-106">The **Remove-AzStorageQueue** cmdlet removes a storage queue.</span></span>

## <span data-ttu-id="884b0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="884b0-107">EXAMPLES</span></span>

### <span data-ttu-id="884b0-108">Exemplo 1: remover uma fila de armazenamento por nome</span><span class="sxs-lookup"><span data-stu-id="884b0-108">Example 1: Remove a storage queue by name</span></span>
```
PS C:\>Remove-AzStorageQueue "ContosoQueue01"
```

<span data-ttu-id="884b0-109">Esse comando Remove uma fila chamada ContosoQueue01.</span><span class="sxs-lookup"><span data-stu-id="884b0-109">This command removes a queue named ContosoQueue01.</span></span>

### <span data-ttu-id="884b0-110">Exemplo 2: remover várias filas de armazenamento</span><span class="sxs-lookup"><span data-stu-id="884b0-110">Example 2: Remove multiple storage queues</span></span>
```
PS C:\>Get-AzStorageQueue "Contoso*" | Remove-AzStorageQueue
```

<span data-ttu-id="884b0-111">Esse comando Remove todas as filas com nomes que começam com contoso.</span><span class="sxs-lookup"><span data-stu-id="884b0-111">This command removes all queues with names that start with Contoso.</span></span>

## <span data-ttu-id="884b0-112">OS</span><span class="sxs-lookup"><span data-stu-id="884b0-112">PARAMETERS</span></span>

### <span data-ttu-id="884b0-113">-Contexto</span><span class="sxs-lookup"><span data-stu-id="884b0-113">-Context</span></span>
<span data-ttu-id="884b0-114">Especifica o contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="884b0-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="884b0-115">Para obter o contexto de armazenamento, o cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="884b0-115">To obtain the storage context, the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="884b0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="884b0-116">-DefaultProfile</span></span>
<span data-ttu-id="884b0-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="884b0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="884b0-118">-Force</span><span class="sxs-lookup"><span data-stu-id="884b0-118">-Force</span></span>
<span data-ttu-id="884b0-119">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="884b0-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="884b0-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="884b0-120">-Name</span></span>
<span data-ttu-id="884b0-121">Especifica o nome da fila a ser removida.</span><span class="sxs-lookup"><span data-stu-id="884b0-121">Specifies the name of the queue to remove.</span></span>

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

### <span data-ttu-id="884b0-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="884b0-122">-PassThru</span></span>
<span data-ttu-id="884b0-123">Indica que esse cmdlet retorna um **booliano** que reflete o sucesso da operação.</span><span class="sxs-lookup"><span data-stu-id="884b0-123">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="884b0-124">Por padrão, esse cmdlet não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="884b0-124">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="884b0-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="884b0-125">-Confirm</span></span>
<span data-ttu-id="884b0-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="884b0-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="884b0-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="884b0-127">-WhatIf</span></span>
<span data-ttu-id="884b0-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="884b0-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="884b0-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="884b0-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="884b0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="884b0-130">CommonParameters</span></span>
<span data-ttu-id="884b0-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="884b0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="884b0-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="884b0-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="884b0-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="884b0-133">INPUTS</span></span>

### <span data-ttu-id="884b0-134">System. String</span><span class="sxs-lookup"><span data-stu-id="884b0-134">System.String</span></span>

### <span data-ttu-id="884b0-135">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="884b0-135">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="884b0-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="884b0-136">OUTPUTS</span></span>

### <span data-ttu-id="884b0-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="884b0-137">System.Boolean</span></span>

## <span data-ttu-id="884b0-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="884b0-138">NOTES</span></span>

## <span data-ttu-id="884b0-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="884b0-139">RELATED LINKS</span></span>

[<span data-ttu-id="884b0-140">Get-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="884b0-140">Get-AzStorageQueue</span></span>](./Get-AzStorageQueue.md)

[<span data-ttu-id="884b0-141">New-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="884b0-141">New-AzStorageQueue</span></span>](./New-AzStorageQueue.md)