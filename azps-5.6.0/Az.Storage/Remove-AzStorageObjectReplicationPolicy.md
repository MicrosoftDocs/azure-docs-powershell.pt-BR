---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azstorageobjectreplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageObjectReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageObjectReplicationPolicy.md
ms.openlocfilehash: 17ccb6e41e826ffd6b522c353ff51cf360b5af0a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886551"
---
# <span data-ttu-id="57a88-101">Remove-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="57a88-101">Remove-AzStorageObjectReplicationPolicy</span></span>

## <span data-ttu-id="57a88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57a88-102">SYNOPSIS</span></span>
<span data-ttu-id="57a88-103">Remove a política de replicação de objeto especificada de uma conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="57a88-103">Removes the specified object replication policy from a Storage account.</span></span>

## <span data-ttu-id="57a88-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="57a88-104">SYNTAX</span></span>

### <span data-ttu-id="57a88-105">AccountName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="57a88-105">AccountName (Default)</span></span>
```
Remove-AzStorageObjectReplicationPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -PolicyId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="57a88-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="57a88-106">AccountObject</span></span>
```
Remove-AzStorageObjectReplicationPolicy -StorageAccount <PSStorageAccount> -PolicyId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57a88-107">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="57a88-107">PolicyObject</span></span>
```
Remove-AzStorageObjectReplicationPolicy -InputObject <PSObjectReplicationPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57a88-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="57a88-108">DESCRIPTION</span></span>
<span data-ttu-id="57a88-109">O cmdlet **Remove-AzStorageObjectReplicationPolicy** remove a política de replicação de objeto especificada de uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="57a88-109">The **Remove-AzStorageObjectReplicationPolicy** cmdlet removes the specified object replication policy from a Storage account.</span></span>

## <span data-ttu-id="57a88-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="57a88-110">EXAMPLES</span></span>

### <span data-ttu-id="57a88-111">Exemplo 1: Remover uma política de replicação de objeto com policyId específica de uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="57a88-111">Example 1: Remove an object replication policy with specific policyId from a storage account.</span></span>
```
Remove-AzStorageObjectReplicationPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -PolicyId $policyId
```

<span data-ttu-id="57a88-112">Este comando remove uma política de replicação de objeto com policyId específica de uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="57a88-112">This command removes an object replication policy with specific policyId from a storage account.</span></span>

## <span data-ttu-id="57a88-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="57a88-113">PARAMETERS</span></span>

### <span data-ttu-id="57a88-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57a88-114">-DefaultProfile</span></span>
<span data-ttu-id="57a88-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="57a88-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57a88-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="57a88-116">-InputObject</span></span>
<span data-ttu-id="57a88-117">Objeto Política de Replicação de Objeto a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="57a88-117">Object Replication Policy object to Delete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy
Parameter Sets: PolicyObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57a88-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="57a88-118">-PassThru</span></span>
<span data-ttu-id="57a88-119">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="57a88-119">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="57a88-120">-PolicyId</span><span class="sxs-lookup"><span data-stu-id="57a88-120">-PolicyId</span></span>
<span data-ttu-id="57a88-121">ID da Política de Replicação de Objeto.</span><span class="sxs-lookup"><span data-stu-id="57a88-121">Object Replication Policy Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57a88-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57a88-122">-ResourceGroupName</span></span>
<span data-ttu-id="57a88-123">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="57a88-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="57a88-124">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="57a88-124">-StorageAccount</span></span>
<span data-ttu-id="57a88-125">Objeto de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="57a88-125">Storage account object</span></span>

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

### <span data-ttu-id="57a88-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="57a88-126">-StorageAccountName</span></span>
<span data-ttu-id="57a88-127">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="57a88-127">Storage Account Name.</span></span>

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

### <span data-ttu-id="57a88-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="57a88-128">-Confirm</span></span>
<span data-ttu-id="57a88-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57a88-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57a88-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57a88-130">-WhatIf</span></span>
<span data-ttu-id="57a88-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="57a88-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57a88-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="57a88-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57a88-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57a88-133">CommonParameters</span></span>
<span data-ttu-id="57a88-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57a88-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57a88-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57a88-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57a88-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="57a88-136">INPUTS</span></span>

### <span data-ttu-id="57a88-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="57a88-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="57a88-138">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="57a88-138">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span></span>

## <span data-ttu-id="57a88-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="57a88-139">OUTPUTS</span></span>

### <span data-ttu-id="57a88-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="57a88-140">System.Boolean</span></span>

## <span data-ttu-id="57a88-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="57a88-141">NOTES</span></span>

## <span data-ttu-id="57a88-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="57a88-142">RELATED LINKS</span></span>
