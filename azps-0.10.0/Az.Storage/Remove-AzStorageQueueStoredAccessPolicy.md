---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 80DE5D60-93F8-4509-AA9C-F54E4AB70013
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Remove-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Remove-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: 74189f488519c903e8e02b1e86585d03a9e80446
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776180"
---
# <span data-ttu-id="8d62a-101">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8d62a-101">Remove-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="8d62a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8d62a-102">SYNOPSIS</span></span>
<span data-ttu-id="8d62a-103">Remove uma política de acesso armazenado de uma fila de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="8d62a-103">Removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="8d62a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8d62a-104">SYNTAX</span></span>

```
Remove-AzStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8d62a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8d62a-105">DESCRIPTION</span></span>
<span data-ttu-id="8d62a-106">O cmdlet **Remove-AzStorageQueueStoredAccessPolicy** remove uma política de acesso armazenado de uma fila de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="8d62a-106">The **Remove-AzStorageQueueStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="8d62a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8d62a-107">EXAMPLES</span></span>

### <span data-ttu-id="8d62a-108">Exemplo 1: remover uma política de acesso armazenado de uma fila de armazenamento</span><span class="sxs-lookup"><span data-stu-id="8d62a-108">Example 1: Remove a stored access policy from a storage queue</span></span>
```
PS C:\>Remove-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy04"
```

<span data-ttu-id="8d62a-109">Esse comando Remove uma política de acesso chamada Policy04 da fila de armazenamento chamada MyQueue.</span><span class="sxs-lookup"><span data-stu-id="8d62a-109">This command removes an access policy named Policy04 from the storage queue named MyQueue.</span></span>

## <span data-ttu-id="8d62a-110">OS</span><span class="sxs-lookup"><span data-stu-id="8d62a-110">PARAMETERS</span></span>

### <span data-ttu-id="8d62a-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="8d62a-111">-Context</span></span>
<span data-ttu-id="8d62a-112">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="8d62a-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="8d62a-113">Para obter um contexto de armazenamento, use o cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="8d62a-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="8d62a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d62a-114">-DefaultProfile</span></span>
<span data-ttu-id="8d62a-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8d62a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d62a-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8d62a-116">-PassThru</span></span>
<span data-ttu-id="8d62a-117">Indica que esse cmdlet retorna um **booliano** que reflete o sucesso da operação.</span><span class="sxs-lookup"><span data-stu-id="8d62a-117">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="8d62a-118">Por padrão, esse cmdlet não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="8d62a-118">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="8d62a-119">-Política</span><span class="sxs-lookup"><span data-stu-id="8d62a-119">-Policy</span></span>
<span data-ttu-id="8d62a-120">Especifica o nome da política de acesso armazenado que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="8d62a-120">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8d62a-121">-Queue</span><span class="sxs-lookup"><span data-stu-id="8d62a-121">-Queue</span></span>
<span data-ttu-id="8d62a-122">Especifica o nome da fila de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="8d62a-122">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="8d62a-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8d62a-123">-Confirm</span></span>
<span data-ttu-id="8d62a-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d62a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d62a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d62a-125">-WhatIf</span></span>
<span data-ttu-id="8d62a-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8d62a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d62a-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8d62a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d62a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d62a-128">CommonParameters</span></span>
<span data-ttu-id="8d62a-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d62a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d62a-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d62a-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d62a-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8d62a-131">INPUTS</span></span>

### <span data-ttu-id="8d62a-132">System. String</span><span class="sxs-lookup"><span data-stu-id="8d62a-132">System.String</span></span>

### <span data-ttu-id="8d62a-133">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="8d62a-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="8d62a-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8d62a-134">OUTPUTS</span></span>

### <span data-ttu-id="8d62a-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8d62a-135">System.Boolean</span></span>

## <span data-ttu-id="8d62a-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8d62a-136">NOTES</span></span>

## <span data-ttu-id="8d62a-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8d62a-137">RELATED LINKS</span></span>

[<span data-ttu-id="8d62a-138">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8d62a-138">Get-AzStorageQueueStoredAccessPolicy</span></span>](./Get-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="8d62a-139">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="8d62a-139">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="8d62a-140">New-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8d62a-140">New-AzStorageQueueStoredAccessPolicy</span></span>](./New-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="8d62a-141">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8d62a-141">Set-AzStorageQueueStoredAccessPolicy</span></span>](./Set-AzStorageQueueStoredAccessPolicy.md)
