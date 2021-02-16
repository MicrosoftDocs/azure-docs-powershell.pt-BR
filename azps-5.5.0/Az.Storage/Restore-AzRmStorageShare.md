---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/restore-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzRmStorageShare.md
ms.openlocfilehash: 70d3c8c435a88b4f0f968d1519efd9af6d9907e8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113933"
---
# <span data-ttu-id="aa7bb-101">Restore-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="aa7bb-101">Restore-AzRmStorageShare</span></span>

## <span data-ttu-id="aa7bb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="aa7bb-102">SYNOPSIS</span></span>
<span data-ttu-id="aa7bb-103">Restaura um compartilhamento de arquivo excluído.</span><span class="sxs-lookup"><span data-stu-id="aa7bb-103">Restores a deleted file share.</span></span>

## <span data-ttu-id="aa7bb-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aa7bb-104">SYNTAX</span></span>

### <span data-ttu-id="aa7bb-105">Nomeda Conta (Padrão)</span><span class="sxs-lookup"><span data-stu-id="aa7bb-105">AccountName (Default)</span></span>
```
Restore-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 -DeletedShareVersion <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="aa7bb-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="aa7bb-106">AccountObject</span></span>
```
Restore-AzRmStorageShare -StorageAccount <PSStorageAccount> -Name <String> -DeletedShareVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa7bb-107">ShareObject</span><span class="sxs-lookup"><span data-stu-id="aa7bb-107">ShareObject</span></span>
```
Restore-AzRmStorageShare -InputObject <PSShare> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="aa7bb-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="aa7bb-108">DESCRIPTION</span></span>
<span data-ttu-id="aa7bb-109">O cmdlet **Restore-AzRmStorageShare** restaura um compartilhamento de arquivo excluído dentro de um dia de retenção válido se a exclusão suave do compartilhamento estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="aa7bb-109">The **Restore-AzRmStorageShare** cmdlet restores a deleted file share within a valid retention days if share soft delete is enabled.</span></span>

## <span data-ttu-id="aa7bb-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="aa7bb-110">EXAMPLES</span></span>

### <span data-ttu-id="aa7bb-111">Exemplo 1: Remover e restaurar um compartilhamento</span><span class="sxs-lookup"><span data-stu-id="aa7bb-111">Example 1: Remove and restore a share</span></span>
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

<span data-ttu-id="aa7bb-112">Primeiro, esse comando exclui um compartilhamento de arquivos e, em seguida, lista compartilhamentos e vê a versão de compartilhamento excluída, finalmente restaure-a novamente para um compartilhamento normal.</span><span class="sxs-lookup"><span data-stu-id="aa7bb-112">This command first delete a file share, and then list shares and see the deleted share version, finally restore it back to a normal share.</span></span> <span data-ttu-id="aa7bb-113">Precisa habilitar o compartilhamento de exclusão suave com o Update-AzStorageFileServiceProperty, antes de excluir o compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="aa7bb-113">Need enabled share soft delete with Update-AzStorageFileServiceProperty, before delete the share.</span></span>

## <span data-ttu-id="aa7bb-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aa7bb-114">PARAMETERS</span></span>

### <span data-ttu-id="aa7bb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa7bb-115">-DefaultProfile</span></span>
<span data-ttu-id="aa7bb-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="aa7bb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa7bb-117">-DeletedShareVersion</span><span class="sxs-lookup"><span data-stu-id="aa7bb-117">-DeletedShareVersion</span></span>
<span data-ttu-id="aa7bb-118">Versão de compartilhamento excluída, que será restaurada a partir de.</span><span class="sxs-lookup"><span data-stu-id="aa7bb-118">Deleted Share Version, which will be restored from.</span></span>

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

### <span data-ttu-id="aa7bb-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aa7bb-119">-InputObject</span></span>
<span data-ttu-id="aa7bb-120">Objeto Compartilhar Excluído</span><span class="sxs-lookup"><span data-stu-id="aa7bb-120">Deleted Share object</span></span>

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

### <span data-ttu-id="aa7bb-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="aa7bb-121">-Name</span></span>
<span data-ttu-id="aa7bb-122">Nome de Compartilhamento Excluído, que será restaurado.</span><span class="sxs-lookup"><span data-stu-id="aa7bb-122">Deleted Share Name, which will be restored.</span></span>

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

### <span data-ttu-id="aa7bb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa7bb-123">-ResourceGroupName</span></span>
<span data-ttu-id="aa7bb-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="aa7bb-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="aa7bb-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="aa7bb-125">-StorageAccount</span></span>
<span data-ttu-id="aa7bb-126">Objeto de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="aa7bb-126">Storage account object</span></span>

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

### <span data-ttu-id="aa7bb-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="aa7bb-127">-StorageAccountName</span></span>
<span data-ttu-id="aa7bb-128">Nome da Conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="aa7bb-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="aa7bb-129">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="aa7bb-129">-Confirm</span></span>
<span data-ttu-id="aa7bb-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa7bb-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa7bb-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa7bb-131">-WhatIf</span></span>
<span data-ttu-id="aa7bb-132">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="aa7bb-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa7bb-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="aa7bb-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa7bb-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa7bb-134">CommonParameters</span></span>
<span data-ttu-id="aa7bb-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa7bb-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa7bb-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa7bb-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa7bb-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="aa7bb-137">INPUTS</span></span>

### <span data-ttu-id="aa7bb-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="aa7bb-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="aa7bb-139">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span><span class="sxs-lookup"><span data-stu-id="aa7bb-139">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="aa7bb-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="aa7bb-140">OUTPUTS</span></span>

### <span data-ttu-id="aa7bb-141">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span><span class="sxs-lookup"><span data-stu-id="aa7bb-141">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="aa7bb-142">Notas</span><span class="sxs-lookup"><span data-stu-id="aa7bb-142">NOTES</span></span>

## <span data-ttu-id="aa7bb-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aa7bb-143">RELATED LINKS</span></span>
