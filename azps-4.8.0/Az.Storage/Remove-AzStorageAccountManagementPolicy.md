---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/remove-Azstorageaccountmanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountManagementPolicy.md
ms.openlocfilehash: 6f4907f9ee94c05161fa602fc5cefd0ead4f6224
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93956109"
---
# <span data-ttu-id="557c8-101">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="557c8-101">Remove-AzStorageAccountManagementPolicy</span></span>

## <span data-ttu-id="557c8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="557c8-102">SYNOPSIS</span></span>
<span data-ttu-id="557c8-103">Remove a política de gerenciamento de uma conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="557c8-103">Removes the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="557c8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="557c8-104">SYNTAX</span></span>

### <span data-ttu-id="557c8-105">AccountName (padrão)</span><span class="sxs-lookup"><span data-stu-id="557c8-105">AccountName (Default)</span></span>
```
Remove-AzStorageAccountManagementPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="557c8-106">Accountobject</span><span class="sxs-lookup"><span data-stu-id="557c8-106">AccountObject</span></span>
```
Remove-AzStorageAccountManagementPolicy -StorageAccount <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="557c8-107">AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="557c8-107">AccountResourceId</span></span>
```
Remove-AzStorageAccountManagementPolicy [-StorageAccountResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="557c8-108">Políticaobject</span><span class="sxs-lookup"><span data-stu-id="557c8-108">PolicyObject</span></span>
```
Remove-AzStorageAccountManagementPolicy [-InputObject] <PSManagementPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="557c8-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="557c8-109">DESCRIPTION</span></span>
<span data-ttu-id="557c8-110">O cmdlet **Remove-AzStorageAccountManagementPolicy** remove a política de gerenciamento de uma conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="557c8-110">The **Remove-AzStorageAccountManagementPolicy** cmdlet removes the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="557c8-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="557c8-111">EXAMPLES</span></span>

### <span data-ttu-id="557c8-112">Exemplo 1: remover a política de gerenciamento de uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="557c8-112">Example 1: Remove the management policy of a Storage account.</span></span>
```
PS C:\>Remove-AzStorageAccountManagementPolicy -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount"
```

<span data-ttu-id="557c8-113">Este comando Remove a política de gerenciamento de uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="557c8-113">This command removes the management policy of a Storage account.</span></span>

## <span data-ttu-id="557c8-114">OS</span><span class="sxs-lookup"><span data-stu-id="557c8-114">PARAMETERS</span></span>

### <span data-ttu-id="557c8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="557c8-115">-DefaultProfile</span></span>
<span data-ttu-id="557c8-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="557c8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="557c8-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="557c8-117">-InputObject</span></span>
<span data-ttu-id="557c8-118">Objeto de gerenciamento para remover</span><span class="sxs-lookup"><span data-stu-id="557c8-118">Management Object to Remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicy
Parameter Sets: PolicyObject
Aliases: ManagementPolicy

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="557c8-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="557c8-119">-PassThru</span></span>
<span data-ttu-id="557c8-120">Indica que esse cmdlet retorna um **booliano** que reflete o sucesso da operação.</span><span class="sxs-lookup"><span data-stu-id="557c8-120">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="557c8-121">Por padrão, esse cmdlet não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="557c8-121">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="557c8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="557c8-122">-ResourceGroupName</span></span>
<span data-ttu-id="557c8-123">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="557c8-123">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="557c8-124">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="557c8-124">-StorageAccount</span></span>
<span data-ttu-id="557c8-125">Objeto da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="557c8-125">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="557c8-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="557c8-126">-StorageAccountName</span></span>
<span data-ttu-id="557c8-127">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="557c8-127">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="557c8-128">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="557c8-128">-StorageAccountResourceId</span></span>
<span data-ttu-id="557c8-129">ID do recurso da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="557c8-129">Storage Account Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="557c8-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="557c8-130">-Confirm</span></span>
<span data-ttu-id="557c8-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="557c8-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="557c8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="557c8-132">-WhatIf</span></span>
<span data-ttu-id="557c8-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="557c8-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="557c8-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="557c8-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="557c8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="557c8-135">CommonParameters</span></span>
<span data-ttu-id="557c8-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="557c8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="557c8-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="557c8-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="557c8-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="557c8-138">INPUTS</span></span>

### <span data-ttu-id="557c8-139">System. String</span><span class="sxs-lookup"><span data-stu-id="557c8-139">System.String</span></span>

## <span data-ttu-id="557c8-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="557c8-140">OUTPUTS</span></span>

### <span data-ttu-id="557c8-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="557c8-141">System.Boolean</span></span>

## <span data-ttu-id="557c8-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="557c8-142">NOTES</span></span>

## <span data-ttu-id="557c8-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="557c8-143">RELATED LINKS</span></span>
