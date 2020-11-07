---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 30CC0D80-505A-4988-B4EC-3B7BC5B76F5D
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 9df25558c752b47e41bf76f7db128bd127ad0c53
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93956106"
---
# <span data-ttu-id="f4ea7-101">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f4ea7-101">Remove-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="f4ea7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f4ea7-102">SYNOPSIS</span></span>
<span data-ttu-id="f4ea7-103">Remove uma política de acesso armazenado de uma tabela de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="f4ea7-103">Removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="f4ea7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f4ea7-104">SYNTAX</span></span>

```
Remove-AzStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f4ea7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f4ea7-105">DESCRIPTION</span></span>
<span data-ttu-id="f4ea7-106">O cmdlet **Remove-AzStorageTableStoredAccessPolicy** remove uma política de acesso armazenado de uma tabela de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="f4ea7-106">The **Remove-AzStorageTableStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="f4ea7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f4ea7-107">EXAMPLES</span></span>

### <span data-ttu-id="f4ea7-108">Exemplo 1: remover uma política de acesso armazenado de uma tabela de armazenamento</span><span class="sxs-lookup"><span data-stu-id="f4ea7-108">Example 1: Remove a stored access policy from a storage table</span></span>
```
PS C:\>Remove-AzStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy05"
```

<span data-ttu-id="f4ea7-109">Esse comando Remove a política denominada Policy05 da tabela de armazenamento chamada MyTable.</span><span class="sxs-lookup"><span data-stu-id="f4ea7-109">This command removes policy named Policy05 from storage table named MyTable.</span></span>

## <span data-ttu-id="f4ea7-110">OS</span><span class="sxs-lookup"><span data-stu-id="f4ea7-110">PARAMETERS</span></span>

### <span data-ttu-id="f4ea7-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="f4ea7-111">-Context</span></span>
<span data-ttu-id="f4ea7-112">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="f4ea7-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="f4ea7-113">Para obter um contexto de armazenamento, use o cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="f4ea7-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="f4ea7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4ea7-114">-DefaultProfile</span></span>
<span data-ttu-id="f4ea7-115">comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f4ea7-115">communication with Azure.</span></span>

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

### <span data-ttu-id="f4ea7-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f4ea7-116">-PassThru</span></span>
<span data-ttu-id="f4ea7-117">Indica que esse cmdlet retorna um **booliano** que reflete o sucesso da operação.</span><span class="sxs-lookup"><span data-stu-id="f4ea7-117">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="f4ea7-118">Por padrão, esse cmdlet não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="f4ea7-118">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="f4ea7-119">-Política</span><span class="sxs-lookup"><span data-stu-id="f4ea7-119">-Policy</span></span>
<span data-ttu-id="f4ea7-120">Especifica o nome da política de acesso armazenado que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="f4ea7-120">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f4ea7-121">-Tabela</span><span class="sxs-lookup"><span data-stu-id="f4ea7-121">-Table</span></span>
<span data-ttu-id="f4ea7-122">Especifica o nome da tabela do Azure.</span><span class="sxs-lookup"><span data-stu-id="f4ea7-122">Specifies the Azure table name.</span></span>

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

### <span data-ttu-id="f4ea7-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f4ea7-123">-Confirm</span></span>
<span data-ttu-id="f4ea7-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4ea7-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4ea7-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4ea7-125">-WhatIf</span></span>
<span data-ttu-id="f4ea7-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f4ea7-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4ea7-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f4ea7-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4ea7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4ea7-128">CommonParameters</span></span>
<span data-ttu-id="f4ea7-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4ea7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4ea7-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4ea7-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4ea7-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f4ea7-131">INPUTS</span></span>

### <span data-ttu-id="f4ea7-132">System. String</span><span class="sxs-lookup"><span data-stu-id="f4ea7-132">System.String</span></span>

### <span data-ttu-id="f4ea7-133">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="f4ea7-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="f4ea7-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f4ea7-134">OUTPUTS</span></span>

### <span data-ttu-id="f4ea7-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f4ea7-135">System.Boolean</span></span>

## <span data-ttu-id="f4ea7-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f4ea7-136">NOTES</span></span>

## <span data-ttu-id="f4ea7-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f4ea7-137">RELATED LINKS</span></span>

[<span data-ttu-id="f4ea7-138">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f4ea7-138">Get-AzStorageTableStoredAccessPolicy</span></span>](./Get-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="f4ea7-139">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="f4ea7-139">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="f4ea7-140">New-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f4ea7-140">New-AzStorageTableStoredAccessPolicy</span></span>](./New-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="f4ea7-141">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f4ea7-141">Set-AzStorageTableStoredAccessPolicy</span></span>](./Set-AzStorageTableStoredAccessPolicy.md)
