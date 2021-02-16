---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 80DE5D60-93F8-4509-AA9C-F54E4AB70013
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: f5620baf0cbd2f5c195b981787ac9def98851fe2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116319"
---
# <span data-ttu-id="8bed6-101">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8bed6-101">Remove-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="8bed6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8bed6-102">SYNOPSIS</span></span>
<span data-ttu-id="8bed6-103">Remove uma política de acesso armazenada de uma fila de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="8bed6-103">Removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="8bed6-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8bed6-104">SYNTAX</span></span>

```
Remove-AzStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8bed6-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="8bed6-105">DESCRIPTION</span></span>
<span data-ttu-id="8bed6-106">O cmdlet **Remove-AzStorageQueueStoredAccessPolicy** remove uma política de acesso armazenada de uma fila de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="8bed6-106">The **Remove-AzStorageQueueStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="8bed6-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8bed6-107">EXAMPLES</span></span>

### <span data-ttu-id="8bed6-108">Exemplo 1: Remover uma política de acesso armazenada de uma fila de armazenamento</span><span class="sxs-lookup"><span data-stu-id="8bed6-108">Example 1: Remove a stored access policy from a storage queue</span></span>
```
PS C:\>Remove-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy04"
```

<span data-ttu-id="8bed6-109">Esse comando remove uma política de acesso chamada Policy04 da fila de armazenamento chamada MyQueue.</span><span class="sxs-lookup"><span data-stu-id="8bed6-109">This command removes an access policy named Policy04 from the storage queue named MyQueue.</span></span>

## <span data-ttu-id="8bed6-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8bed6-110">PARAMETERS</span></span>

### <span data-ttu-id="8bed6-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="8bed6-111">-Context</span></span>
<span data-ttu-id="8bed6-112">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="8bed6-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="8bed6-113">Para obter um contexto de armazenamento, use o New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8bed6-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="8bed6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bed6-114">-DefaultProfile</span></span>
<span data-ttu-id="8bed6-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8bed6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8bed6-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8bed6-116">-PassThru</span></span>
<span data-ttu-id="8bed6-117">Indica que esse cmdlet retorna um **boolano** que reflete o sucesso da operação.</span><span class="sxs-lookup"><span data-stu-id="8bed6-117">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="8bed6-118">Por padrão, esse cmdlet não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="8bed6-118">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="8bed6-119">-Política</span><span class="sxs-lookup"><span data-stu-id="8bed6-119">-Policy</span></span>
<span data-ttu-id="8bed6-120">Especifica o nome da política de acesso armazenada que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="8bed6-120">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8bed6-121">-Fila</span><span class="sxs-lookup"><span data-stu-id="8bed6-121">-Queue</span></span>
<span data-ttu-id="8bed6-122">Especifica o nome da fila de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="8bed6-122">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="8bed6-123">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="8bed6-123">-Confirm</span></span>
<span data-ttu-id="8bed6-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8bed6-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8bed6-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bed6-125">-WhatIf</span></span>
<span data-ttu-id="8bed6-126">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="8bed6-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8bed6-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8bed6-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8bed6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bed6-128">CommonParameters</span></span>
<span data-ttu-id="8bed6-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bed6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bed6-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8bed6-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bed6-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="8bed6-131">INPUTS</span></span>

### <span data-ttu-id="8bed6-132">System.String</span><span class="sxs-lookup"><span data-stu-id="8bed6-132">System.String</span></span>

### <span data-ttu-id="8bed6-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="8bed6-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="8bed6-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="8bed6-134">OUTPUTS</span></span>

### <span data-ttu-id="8bed6-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8bed6-135">System.Boolean</span></span>

## <span data-ttu-id="8bed6-136">Notas</span><span class="sxs-lookup"><span data-stu-id="8bed6-136">NOTES</span></span>

## <span data-ttu-id="8bed6-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8bed6-137">RELATED LINKS</span></span>

[<span data-ttu-id="8bed6-138">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8bed6-138">Get-AzStorageQueueStoredAccessPolicy</span></span>](./Get-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="8bed6-139">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="8bed6-139">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="8bed6-140">New-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8bed6-140">New-AzStorageQueueStoredAccessPolicy</span></span>](./New-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="8bed6-141">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8bed6-141">Set-AzStorageQueueStoredAccessPolicy</span></span>](./Set-AzStorageQueueStoredAccessPolicy.md)
