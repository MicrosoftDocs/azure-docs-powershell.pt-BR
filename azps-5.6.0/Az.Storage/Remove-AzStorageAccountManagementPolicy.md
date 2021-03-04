---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/Az.storage/remove-Azstorageaccountmanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountManagementPolicy.md
ms.openlocfilehash: 671a83ee392f59dc27cff6cc34eeb7df054b3fbf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891938"
---
# <span data-ttu-id="6d493-101">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="6d493-101">Remove-AzStorageAccountManagementPolicy</span></span>

## <span data-ttu-id="6d493-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d493-102">SYNOPSIS</span></span>
<span data-ttu-id="6d493-103">Remove a política de gerenciamento de uma conta de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="6d493-103">Removes the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="6d493-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6d493-104">SYNTAX</span></span>

### <span data-ttu-id="6d493-105">AccountName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6d493-105">AccountName (Default)</span></span>
```
Remove-AzStorageAccountManagementPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d493-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="6d493-106">AccountObject</span></span>
```
Remove-AzStorageAccountManagementPolicy -StorageAccount <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d493-107">AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="6d493-107">AccountResourceId</span></span>
```
Remove-AzStorageAccountManagementPolicy [-StorageAccountResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d493-108">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="6d493-108">PolicyObject</span></span>
```
Remove-AzStorageAccountManagementPolicy [-InputObject] <PSManagementPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d493-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6d493-109">DESCRIPTION</span></span>
<span data-ttu-id="6d493-110">O cmdlet **Remove-AzStorageAccountManagementPolicy** remove a política de gerenciamento de uma conta de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="6d493-110">The **Remove-AzStorageAccountManagementPolicy** cmdlet removes the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="6d493-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6d493-111">EXAMPLES</span></span>

### <span data-ttu-id="6d493-112">Exemplo 1: Remover a política de gerenciamento de uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="6d493-112">Example 1: Remove the management policy of a Storage account.</span></span>
```
PS C:\>Remove-AzStorageAccountManagementPolicy -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount"
```

<span data-ttu-id="6d493-113">Este comando remove a política de gerenciamento de uma conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="6d493-113">This command removes the management policy of a Storage account.</span></span>

## <span data-ttu-id="6d493-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6d493-114">PARAMETERS</span></span>

### <span data-ttu-id="6d493-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d493-115">-DefaultProfile</span></span>
<span data-ttu-id="6d493-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6d493-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d493-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6d493-117">-InputObject</span></span>
<span data-ttu-id="6d493-118">Objeto Management a ser removido</span><span class="sxs-lookup"><span data-stu-id="6d493-118">Management Object to Remove</span></span>

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

### <span data-ttu-id="6d493-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6d493-119">-PassThru</span></span>
<span data-ttu-id="6d493-120">Indica que esse cmdlet retorna um **Boolean** que reflete o sucesso da operação.</span><span class="sxs-lookup"><span data-stu-id="6d493-120">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="6d493-121">Por padrão, esse cmdlet não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="6d493-121">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="6d493-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d493-122">-ResourceGroupName</span></span>
<span data-ttu-id="6d493-123">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="6d493-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="6d493-124">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="6d493-124">-StorageAccount</span></span>
<span data-ttu-id="6d493-125">Objeto de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="6d493-125">Storage account object</span></span>

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

### <span data-ttu-id="6d493-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="6d493-126">-StorageAccountName</span></span>
<span data-ttu-id="6d493-127">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="6d493-127">Storage Account Name.</span></span>

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

### <span data-ttu-id="6d493-128">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="6d493-128">-StorageAccountResourceId</span></span>
<span data-ttu-id="6d493-129">ID do Recurso de Conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="6d493-129">Storage Account Resource Id.</span></span>

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

### <span data-ttu-id="6d493-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6d493-130">-Confirm</span></span>
<span data-ttu-id="6d493-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d493-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d493-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d493-132">-WhatIf</span></span>
<span data-ttu-id="6d493-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6d493-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d493-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6d493-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d493-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d493-135">CommonParameters</span></span>
<span data-ttu-id="6d493-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d493-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d493-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d493-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d493-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6d493-138">INPUTS</span></span>

### <span data-ttu-id="6d493-139">System.String</span><span class="sxs-lookup"><span data-stu-id="6d493-139">System.String</span></span>

## <span data-ttu-id="6d493-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6d493-140">OUTPUTS</span></span>

### <span data-ttu-id="6d493-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6d493-141">System.Boolean</span></span>

## <span data-ttu-id="6d493-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="6d493-142">NOTES</span></span>

## <span data-ttu-id="6d493-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6d493-143">RELATED LINKS</span></span>
