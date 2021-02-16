---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageobjectreplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageObjectReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageObjectReplicationPolicy.md
ms.openlocfilehash: 4c42fe6e612f30ab622a0a04498e5474f27690e9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116321"
---
# <span data-ttu-id="57f72-101">Remove-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="57f72-101">Remove-AzStorageObjectReplicationPolicy</span></span>

## <span data-ttu-id="57f72-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="57f72-102">SYNOPSIS</span></span>
<span data-ttu-id="57f72-103">Remove a política de replicação de objeto especificada de uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="57f72-103">Removes the specified object replication policy from a Storage account.</span></span>

## <span data-ttu-id="57f72-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="57f72-104">SYNTAX</span></span>

### <span data-ttu-id="57f72-105">Nomeda Conta (Padrão)</span><span class="sxs-lookup"><span data-stu-id="57f72-105">AccountName (Default)</span></span>
```
Remove-AzStorageObjectReplicationPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -PolicyId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="57f72-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="57f72-106">AccountObject</span></span>
```
Remove-AzStorageObjectReplicationPolicy -StorageAccount <PSStorageAccount> -PolicyId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57f72-107">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="57f72-107">PolicyObject</span></span>
```
Remove-AzStorageObjectReplicationPolicy -InputObject <PSObjectReplicationPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57f72-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="57f72-108">DESCRIPTION</span></span>
<span data-ttu-id="57f72-109">O cmdlet **Remove-AzStorageObjectReplicationPolicy** remove a política de replicação de objeto especificada de uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="57f72-109">The **Remove-AzStorageObjectReplicationPolicy** cmdlet removes the specified object replication policy from a Storage account.</span></span>

## <span data-ttu-id="57f72-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="57f72-110">EXAMPLES</span></span>

### <span data-ttu-id="57f72-111">Exemplo 1: Remover uma política de replicação de objeto com policyId específica de uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="57f72-111">Example 1: Remove an object replication policy with specific policyId from a storage account.</span></span>
```
Remove-AzStorageObjectReplicationPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -PolicyId $policyId
```

<span data-ttu-id="57f72-112">Esse comando remove uma política de replicação de objeto com policyId específica de uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="57f72-112">This command removes an object replication policy with specific policyId from a storage account.</span></span>

## <span data-ttu-id="57f72-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="57f72-113">PARAMETERS</span></span>

### <span data-ttu-id="57f72-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57f72-114">-DefaultProfile</span></span>
<span data-ttu-id="57f72-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="57f72-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57f72-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="57f72-116">-InputObject</span></span>
<span data-ttu-id="57f72-117">Objeto De Política de Replicação de Objeto para Excluir.</span><span class="sxs-lookup"><span data-stu-id="57f72-117">Object Replication Policy object to Delete.</span></span>

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

### <span data-ttu-id="57f72-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="57f72-118">-PassThru</span></span>
<span data-ttu-id="57f72-119">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="57f72-119">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="57f72-120">-PolicyId</span><span class="sxs-lookup"><span data-stu-id="57f72-120">-PolicyId</span></span>
<span data-ttu-id="57f72-121">ID da Política de Replicação de Objeto.</span><span class="sxs-lookup"><span data-stu-id="57f72-121">Object Replication Policy Id.</span></span>

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

### <span data-ttu-id="57f72-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57f72-122">-ResourceGroupName</span></span>
<span data-ttu-id="57f72-123">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="57f72-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="57f72-124">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="57f72-124">-StorageAccount</span></span>
<span data-ttu-id="57f72-125">Objeto de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="57f72-125">Storage account object</span></span>

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

### <span data-ttu-id="57f72-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="57f72-126">-StorageAccountName</span></span>
<span data-ttu-id="57f72-127">Nome da Conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="57f72-127">Storage Account Name.</span></span>

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

### <span data-ttu-id="57f72-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="57f72-128">-Confirm</span></span>
<span data-ttu-id="57f72-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57f72-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57f72-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57f72-130">-WhatIf</span></span>
<span data-ttu-id="57f72-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="57f72-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57f72-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="57f72-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57f72-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57f72-133">CommonParameters</span></span>
<span data-ttu-id="57f72-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57f72-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57f72-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57f72-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57f72-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="57f72-136">INPUTS</span></span>

### <span data-ttu-id="57f72-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="57f72-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="57f72-138">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="57f72-138">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span></span>

## <span data-ttu-id="57f72-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="57f72-139">OUTPUTS</span></span>

### <span data-ttu-id="57f72-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="57f72-140">System.Boolean</span></span>

## <span data-ttu-id="57f72-141">Notas</span><span class="sxs-lookup"><span data-stu-id="57f72-141">NOTES</span></span>

## <span data-ttu-id="57f72-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="57f72-142">RELATED LINKS</span></span>
