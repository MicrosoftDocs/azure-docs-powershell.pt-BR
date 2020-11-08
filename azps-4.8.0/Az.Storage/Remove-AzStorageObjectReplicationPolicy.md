---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageobjectreplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageObjectReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageObjectReplicationPolicy.md
ms.openlocfilehash: 4c42fe6e612f30ab622a0a04498e5474f27690e9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94112061"
---
# <span data-ttu-id="22382-101">Remove-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="22382-101">Remove-AzStorageObjectReplicationPolicy</span></span>

## <span data-ttu-id="22382-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="22382-102">SYNOPSIS</span></span>
<span data-ttu-id="22382-103">Remove a política de replicação de objetos especificada de uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="22382-103">Removes the specified object replication policy from a Storage account.</span></span>

## <span data-ttu-id="22382-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="22382-104">SYNTAX</span></span>

### <span data-ttu-id="22382-105">AccountName (padrão)</span><span class="sxs-lookup"><span data-stu-id="22382-105">AccountName (Default)</span></span>
```
Remove-AzStorageObjectReplicationPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -PolicyId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="22382-106">Accountobject</span><span class="sxs-lookup"><span data-stu-id="22382-106">AccountObject</span></span>
```
Remove-AzStorageObjectReplicationPolicy -StorageAccount <PSStorageAccount> -PolicyId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22382-107">Políticaobject</span><span class="sxs-lookup"><span data-stu-id="22382-107">PolicyObject</span></span>
```
Remove-AzStorageObjectReplicationPolicy -InputObject <PSObjectReplicationPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22382-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="22382-108">DESCRIPTION</span></span>
<span data-ttu-id="22382-109">O cmdlet **Remove-AzStorageObjectReplicationPolicy** remove a política de replicação de objetos especificada de uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="22382-109">The **Remove-AzStorageObjectReplicationPolicy** cmdlet removes the specified object replication policy from a Storage account.</span></span>

## <span data-ttu-id="22382-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="22382-110">EXAMPLES</span></span>

### <span data-ttu-id="22382-111">Exemplo 1: remover uma política de replicação de objeto com PolicyId específica de uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="22382-111">Example 1: Remove an object replication policy with specific policyId from a storage account.</span></span>
```
Remove-AzStorageObjectReplicationPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -PolicyId $policyId
```

<span data-ttu-id="22382-112">Esse comando Remove uma política de replicação de objeto com PolicyId específico de uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="22382-112">This command removes an object replication policy with specific policyId from a storage account.</span></span>

## <span data-ttu-id="22382-113">OS</span><span class="sxs-lookup"><span data-stu-id="22382-113">PARAMETERS</span></span>

### <span data-ttu-id="22382-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22382-114">-DefaultProfile</span></span>
<span data-ttu-id="22382-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="22382-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22382-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="22382-116">-InputObject</span></span>
<span data-ttu-id="22382-117">Objeto de política de replicação de objetos a excluir.</span><span class="sxs-lookup"><span data-stu-id="22382-117">Object Replication Policy object to Delete.</span></span>

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

### <span data-ttu-id="22382-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="22382-118">-PassThru</span></span>
<span data-ttu-id="22382-119">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="22382-119">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="22382-120">-PolicyId</span><span class="sxs-lookup"><span data-stu-id="22382-120">-PolicyId</span></span>
<span data-ttu-id="22382-121">ID da política de replicação de objetos.</span><span class="sxs-lookup"><span data-stu-id="22382-121">Object Replication Policy Id.</span></span>

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

### <span data-ttu-id="22382-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22382-122">-ResourceGroupName</span></span>
<span data-ttu-id="22382-123">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="22382-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="22382-124">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="22382-124">-StorageAccount</span></span>
<span data-ttu-id="22382-125">Objeto da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="22382-125">Storage account object</span></span>

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

### <span data-ttu-id="22382-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="22382-126">-StorageAccountName</span></span>
<span data-ttu-id="22382-127">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="22382-127">Storage Account Name.</span></span>

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

### <span data-ttu-id="22382-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="22382-128">-Confirm</span></span>
<span data-ttu-id="22382-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22382-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22382-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22382-130">-WhatIf</span></span>
<span data-ttu-id="22382-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="22382-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22382-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="22382-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22382-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22382-133">CommonParameters</span></span>
<span data-ttu-id="22382-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22382-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22382-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22382-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22382-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="22382-136">INPUTS</span></span>

### <span data-ttu-id="22382-137">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="22382-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="22382-138">Microsoft. Azure. Commands. Management. Storage. Models. PSObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="22382-138">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span></span>

## <span data-ttu-id="22382-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="22382-139">OUTPUTS</span></span>

### <span data-ttu-id="22382-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="22382-140">System.Boolean</span></span>

## <span data-ttu-id="22382-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="22382-141">NOTES</span></span>

## <span data-ttu-id="22382-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="22382-142">RELATED LINKS</span></span>
