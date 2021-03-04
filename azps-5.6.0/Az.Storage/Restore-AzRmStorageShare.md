---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/restore-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzRmStorageShare.md
ms.openlocfilehash: 0ce045df6e19a964cf92d5550cfb94e30c808a3d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892594"
---
# <span data-ttu-id="29865-101">Restore-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="29865-101">Restore-AzRmStorageShare</span></span>

## <span data-ttu-id="29865-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29865-102">SYNOPSIS</span></span>
<span data-ttu-id="29865-103">Restaura um compartilhamento de arquivo excluído.</span><span class="sxs-lookup"><span data-stu-id="29865-103">Restores a deleted file share.</span></span>

## <span data-ttu-id="29865-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="29865-104">SYNTAX</span></span>

### <span data-ttu-id="29865-105">AccountName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="29865-105">AccountName (Default)</span></span>
```
Restore-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 -DeletedShareVersion <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="29865-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="29865-106">AccountObject</span></span>
```
Restore-AzRmStorageShare -StorageAccount <PSStorageAccount> -Name <String> -DeletedShareVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29865-107">ShareObject</span><span class="sxs-lookup"><span data-stu-id="29865-107">ShareObject</span></span>
```
Restore-AzRmStorageShare -InputObject <PSShare> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="29865-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="29865-108">DESCRIPTION</span></span>
<span data-ttu-id="29865-109">O cmdlet **Restore-AzRmStorageShare** restaura um compartilhamento de arquivo excluído em um dia de retenção válido se a exclusão de compartilhamento está habilitada.</span><span class="sxs-lookup"><span data-stu-id="29865-109">The **Restore-AzRmStorageShare** cmdlet restores a deleted file share within a valid retention days if share soft delete is enabled.</span></span>

## <span data-ttu-id="29865-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="29865-110">EXAMPLES</span></span>

### <span data-ttu-id="29865-111">Exemplo 1: Remover e restaurar um compartilhamento</span><span class="sxs-lookup"><span data-stu-id="29865-111">Example 1: Remove and restore a share</span></span>
```powershell
PS C:\> Remove-AzRmStorageShare -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Name $shareName -Force

PS C:\> Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -IncludeDeleted 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier           Deleted Version          ShareUsageBytes
----     -------- --------------- ----------           ------- -------          ---------------
test     100                      TransactionOptimized                                         
share1   100                      TransactionOptimized True    01D61FD1FC5498B6                

PS C:\> Restore-AzRmStorageShare -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Name $shareName -DeletedShareVersion 01D61FD1FC5498B6

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
share1   100
```

<span data-ttu-id="29865-112">Esse comando primeiro exclui um compartilhamento de arquivo e lista compartilhamentos e, em seguida, vê a versão de compartilhamento excluída, finalmente restaure-a de volta para um compartilhamento normal.</span><span class="sxs-lookup"><span data-stu-id="29865-112">This command first delete a file share, and then list shares and see the deleted share version, finally restore it back to a normal share.</span></span> <span data-ttu-id="29865-113">Precisa de exclusão de compartilhamento habilitada com Update-AzStorageFileServiceProperty, antes de excluir o compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="29865-113">Need enabled share soft delete with Update-AzStorageFileServiceProperty, before delete the share.</span></span>

## <span data-ttu-id="29865-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="29865-114">PARAMETERS</span></span>

### <span data-ttu-id="29865-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29865-115">-DefaultProfile</span></span>
<span data-ttu-id="29865-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="29865-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29865-117">-DeletedShareVersion</span><span class="sxs-lookup"><span data-stu-id="29865-117">-DeletedShareVersion</span></span>
<span data-ttu-id="29865-118">Versão do Compartilhamento Excluída, que será restaurada a partir de.</span><span class="sxs-lookup"><span data-stu-id="29865-118">Deleted Share Version, which will be restored from.</span></span>

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

### <span data-ttu-id="29865-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="29865-119">-InputObject</span></span>
<span data-ttu-id="29865-120">Objeto Share Excluído</span><span class="sxs-lookup"><span data-stu-id="29865-120">Deleted Share object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSShare
Parameter Sets: ShareObject
Aliases: Share

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="29865-121">-Name</span><span class="sxs-lookup"><span data-stu-id="29865-121">-Name</span></span>
<span data-ttu-id="29865-122">Nome do Compartilhamento Excluído, que será restaurado.</span><span class="sxs-lookup"><span data-stu-id="29865-122">Deleted Share Name, which will be restored.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N, ShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29865-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29865-123">-ResourceGroupName</span></span>
<span data-ttu-id="29865-124">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="29865-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="29865-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="29865-125">-StorageAccount</span></span>
<span data-ttu-id="29865-126">Objeto de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="29865-126">Storage account object</span></span>

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

### <span data-ttu-id="29865-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="29865-127">-StorageAccountName</span></span>
<span data-ttu-id="29865-128">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="29865-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="29865-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="29865-129">-Confirm</span></span>
<span data-ttu-id="29865-130">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29865-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29865-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29865-131">-WhatIf</span></span>
<span data-ttu-id="29865-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="29865-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29865-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="29865-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29865-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29865-134">CommonParameters</span></span>
<span data-ttu-id="29865-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29865-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29865-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29865-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29865-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="29865-137">INPUTS</span></span>

### <span data-ttu-id="29865-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="29865-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="29865-139">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span><span class="sxs-lookup"><span data-stu-id="29865-139">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="29865-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="29865-140">OUTPUTS</span></span>

### <span data-ttu-id="29865-141">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span><span class="sxs-lookup"><span data-stu-id="29865-141">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="29865-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="29865-142">NOTES</span></span>

## <span data-ttu-id="29865-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="29865-143">RELATED LINKS</span></span>
