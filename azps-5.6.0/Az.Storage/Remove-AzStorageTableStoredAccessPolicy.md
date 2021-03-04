---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 30CC0D80-505A-4988-B4EC-3B7BC5B76F5D
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 7674b21e72d375665662272cb2ac1a585d266324
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886538"
---
# <span data-ttu-id="80a13-101">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="80a13-101">Remove-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="80a13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80a13-102">SYNOPSIS</span></span>
<span data-ttu-id="80a13-103">Remove uma política de acesso armazenada de uma tabela de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="80a13-103">Removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="80a13-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="80a13-104">SYNTAX</span></span>

```
Remove-AzStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="80a13-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="80a13-105">DESCRIPTION</span></span>
<span data-ttu-id="80a13-106">O cmdlet **Remove-AzStorageTableStoredAccessPolicy** remove uma política de acesso armazenada de uma tabela de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="80a13-106">The **Remove-AzStorageTableStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="80a13-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="80a13-107">EXAMPLES</span></span>

### <span data-ttu-id="80a13-108">Exemplo 1: Remover uma política de acesso armazenado de uma tabela de armazenamento</span><span class="sxs-lookup"><span data-stu-id="80a13-108">Example 1: Remove a stored access policy from a storage table</span></span>
```
PS C:\>Remove-AzStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy05"
```

<span data-ttu-id="80a13-109">Este comando remove a política chamada Policy05 da tabela de armazenamento chamada MyTable.</span><span class="sxs-lookup"><span data-stu-id="80a13-109">This command removes policy named Policy05 from storage table named MyTable.</span></span>

## <span data-ttu-id="80a13-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="80a13-110">PARAMETERS</span></span>

### <span data-ttu-id="80a13-111">-Context</span><span class="sxs-lookup"><span data-stu-id="80a13-111">-Context</span></span>
<span data-ttu-id="80a13-112">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="80a13-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="80a13-113">Para obter um contexto de armazenamento, use o New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80a13-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="80a13-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80a13-114">-DefaultProfile</span></span>
<span data-ttu-id="80a13-115">comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="80a13-115">communication with Azure.</span></span>

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

### <span data-ttu-id="80a13-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="80a13-116">-PassThru</span></span>
<span data-ttu-id="80a13-117">Indica que esse cmdlet retorna um **Boolean** que reflete o sucesso da operação.</span><span class="sxs-lookup"><span data-stu-id="80a13-117">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="80a13-118">Por padrão, esse cmdlet não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="80a13-118">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="80a13-119">-Policy</span><span class="sxs-lookup"><span data-stu-id="80a13-119">-Policy</span></span>
<span data-ttu-id="80a13-120">Especifica o nome da política de acesso armazenada que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="80a13-120">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80a13-121">-Table</span><span class="sxs-lookup"><span data-stu-id="80a13-121">-Table</span></span>
<span data-ttu-id="80a13-122">Especifica o nome da tabela do Azure.</span><span class="sxs-lookup"><span data-stu-id="80a13-122">Specifies the Azure table name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80a13-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="80a13-123">-Confirm</span></span>
<span data-ttu-id="80a13-124">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80a13-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80a13-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80a13-125">-WhatIf</span></span>
<span data-ttu-id="80a13-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="80a13-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80a13-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="80a13-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80a13-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80a13-128">CommonParameters</span></span>
<span data-ttu-id="80a13-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80a13-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80a13-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80a13-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80a13-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="80a13-131">INPUTS</span></span>

### <span data-ttu-id="80a13-132">System.String</span><span class="sxs-lookup"><span data-stu-id="80a13-132">System.String</span></span>

### <span data-ttu-id="80a13-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="80a13-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="80a13-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="80a13-134">OUTPUTS</span></span>

### <span data-ttu-id="80a13-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="80a13-135">System.Boolean</span></span>

## <span data-ttu-id="80a13-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="80a13-136">NOTES</span></span>

## <span data-ttu-id="80a13-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="80a13-137">RELATED LINKS</span></span>

[<span data-ttu-id="80a13-138">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="80a13-138">Get-AzStorageTableStoredAccessPolicy</span></span>](./Get-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="80a13-139">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="80a13-139">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="80a13-140">New-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="80a13-140">New-AzStorageTableStoredAccessPolicy</span></span>](./New-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="80a13-141">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="80a13-141">Set-AzStorageTableStoredAccessPolicy</span></span>](./Set-AzStorageTableStoredAccessPolicy.md)
