---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/restore-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzRmStorageShare.md
ms.openlocfilehash: 70d3c8c435a88b4f0f968d1519efd9af6d9907e8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98432931"
---
# <span data-ttu-id="db76d-101">Restore-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="db76d-101">Restore-AzRmStorageShare</span></span>

## <span data-ttu-id="db76d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="db76d-102">SYNOPSIS</span></span>
<span data-ttu-id="db76d-103">Restaura um compartilhamento de arquivos excluído.</span><span class="sxs-lookup"><span data-stu-id="db76d-103">Restores a deleted file share.</span></span>

## <span data-ttu-id="db76d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="db76d-104">SYNTAX</span></span>

### <span data-ttu-id="db76d-105">AccountName (padrão)</span><span class="sxs-lookup"><span data-stu-id="db76d-105">AccountName (Default)</span></span>
```
Restore-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 -DeletedShareVersion <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="db76d-106">Accountobject</span><span class="sxs-lookup"><span data-stu-id="db76d-106">AccountObject</span></span>
```
Restore-AzRmStorageShare -StorageAccount <PSStorageAccount> -Name <String> -DeletedShareVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db76d-107">Shareobject</span><span class="sxs-lookup"><span data-stu-id="db76d-107">ShareObject</span></span>
```
Restore-AzRmStorageShare -InputObject <PSShare> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="db76d-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="db76d-108">DESCRIPTION</span></span>
<span data-ttu-id="db76d-109">O cmdlet **Restore-AzRmStorageShare** restaura um compartilhamento de arquivo excluído dentro de um período de retenção válido se compartilhar exclusão reversível estiver habilitado.</span><span class="sxs-lookup"><span data-stu-id="db76d-109">The **Restore-AzRmStorageShare** cmdlet restores a deleted file share within a valid retention days if share soft delete is enabled.</span></span>

## <span data-ttu-id="db76d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="db76d-110">EXAMPLES</span></span>

### <span data-ttu-id="db76d-111">Exemplo 1: remover e restaurar um compartilhamento</span><span class="sxs-lookup"><span data-stu-id="db76d-111">Example 1: Remove and restore a share</span></span>
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

<span data-ttu-id="db76d-112">Este comando exclui primeiro um compartilhamento de arquivos e, em seguida, lista partilhas e vê a versão de compartilhamento excluída, finalmente restaure-o de volta para um compartilhamento normal.</span><span class="sxs-lookup"><span data-stu-id="db76d-112">This command first delete a file share, and then list shares and see the deleted share version, finally restore it back to a normal share.</span></span> <span data-ttu-id="db76d-113">É necessário habilitar o compartilhamento de exclusão flexível com Update-AzStorageFileServiceProperty antes de excluir o compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="db76d-113">Need enabled share soft delete with Update-AzStorageFileServiceProperty, before delete the share.</span></span>

## <span data-ttu-id="db76d-114">OS</span><span class="sxs-lookup"><span data-stu-id="db76d-114">PARAMETERS</span></span>

### <span data-ttu-id="db76d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db76d-115">-DefaultProfile</span></span>
<span data-ttu-id="db76d-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="db76d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db76d-117">-DeletedShareVersion</span><span class="sxs-lookup"><span data-stu-id="db76d-117">-DeletedShareVersion</span></span>
<span data-ttu-id="db76d-118">Versão de compartilhamento excluída da qual será restaurado.</span><span class="sxs-lookup"><span data-stu-id="db76d-118">Deleted Share Version, which will be restored from.</span></span>

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

### <span data-ttu-id="db76d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="db76d-119">-InputObject</span></span>
<span data-ttu-id="db76d-120">Objeto de compartilhamento excluído</span><span class="sxs-lookup"><span data-stu-id="db76d-120">Deleted Share object</span></span>

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

### <span data-ttu-id="db76d-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="db76d-121">-Name</span></span>
<span data-ttu-id="db76d-122">Nome de compartilhamento excluído que será restaurado.</span><span class="sxs-lookup"><span data-stu-id="db76d-122">Deleted Share Name, which will be restored.</span></span>

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

### <span data-ttu-id="db76d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db76d-123">-ResourceGroupName</span></span>
<span data-ttu-id="db76d-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="db76d-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="db76d-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="db76d-125">-StorageAccount</span></span>
<span data-ttu-id="db76d-126">Objeto da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="db76d-126">Storage account object</span></span>

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

### <span data-ttu-id="db76d-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="db76d-127">-StorageAccountName</span></span>
<span data-ttu-id="db76d-128">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="db76d-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="db76d-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="db76d-129">-Confirm</span></span>
<span data-ttu-id="db76d-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db76d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db76d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db76d-131">-WhatIf</span></span>
<span data-ttu-id="db76d-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="db76d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db76d-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="db76d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db76d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db76d-134">CommonParameters</span></span>
<span data-ttu-id="db76d-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db76d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db76d-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db76d-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db76d-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="db76d-137">INPUTS</span></span>

### <span data-ttu-id="db76d-138">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="db76d-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="db76d-139">Microsoft. Azure. Commands. Management. Storage. Models. PSShare</span><span class="sxs-lookup"><span data-stu-id="db76d-139">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="db76d-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="db76d-140">OUTPUTS</span></span>

### <span data-ttu-id="db76d-141">Microsoft. Azure. Commands. Management. Storage. Models. PSShare</span><span class="sxs-lookup"><span data-stu-id="db76d-141">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="db76d-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="db76d-142">NOTES</span></span>

## <span data-ttu-id="db76d-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="db76d-143">RELATED LINKS</span></span>
