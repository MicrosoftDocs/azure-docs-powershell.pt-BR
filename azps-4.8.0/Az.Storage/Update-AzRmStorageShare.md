---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageShare.md
ms.openlocfilehash: 9c5ff85ef608f623187d9132eea8af0f5da6a164
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94112042"
---
# <span data-ttu-id="c3625-101">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="c3625-101">Update-AzRmStorageShare</span></span>

## <span data-ttu-id="c3625-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c3625-102">SYNOPSIS</span></span>
<span data-ttu-id="c3625-103">Modifica um compartilhamento de arquivo de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c3625-103">Modifies a Storage file share.</span></span>

## <span data-ttu-id="c3625-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c3625-104">SYNTAX</span></span>

### <span data-ttu-id="c3625-105">AccountName (padrão)</span><span class="sxs-lookup"><span data-stu-id="c3625-105">AccountName (Default)</span></span>
```
Update-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-QuotaGiB <Int32>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c3625-106">Accountobject</span><span class="sxs-lookup"><span data-stu-id="c3625-106">AccountObject</span></span>
```
Update-AzRmStorageShare -Name <String> -StorageAccount <PSStorageAccount> [-QuotaGiB <Int32>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3625-107">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="c3625-107">ShareResourceId</span></span>
```
Update-AzRmStorageShare [-ResourceId] <String> [-QuotaGiB <Int32>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3625-108">Shareobject</span><span class="sxs-lookup"><span data-stu-id="c3625-108">ShareObject</span></span>
```
Update-AzRmStorageShare -InputObject <PSShare> [-QuotaGiB <Int32>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3625-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c3625-109">DESCRIPTION</span></span>
<span data-ttu-id="c3625-110">O cmdlet **New-AzRmStorageShare** modifica um compartilhamento de arquivo de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c3625-110">The **New-AzRmStorageShare** cmdlet modifies a Storage file share.</span></span>

## <span data-ttu-id="c3625-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c3625-111">EXAMPLES</span></span>

### <span data-ttu-id="c3625-112">Exemplo 1: modifica os metadados e a cota de compartilhamento de um compartilhamento de arquivos de armazenamento com o nome da conta de armazenamento e o nome do compartilhamento</span><span class="sxs-lookup"><span data-stu-id="c3625-112">Example 1: Modifies a Storage file share's metadata and share quota with Storage account name and share name</span></span>
```
PS C:\>$share = Update-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -QuotaGiB 200 -Metadata @{tag0="value0";tag1="value1"}

PS C:\>$share

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare  200

PS C:\>$share.Metadata

Key  Value  
---  ----- 
tag0 value0
tag1 value1
```

<span data-ttu-id="c3625-113">Esse comando modifica a cota de metadados e compartilhamento de um compartilhamento de arquivos de armazenamento com o nome da conta de armazenamento e o nome do compartilhamento e mostra o resultado de modificação com o objeto de compartilhamento de arquivo retornado.</span><span class="sxs-lookup"><span data-stu-id="c3625-113">This command modifies a Storage file share's metadata and share quota with Storage account name and share name, and show the modify result with the returned file share object.</span></span>

### <span data-ttu-id="c3625-114">Exemplo 2: modifica metadados em um compartilhamento de arquivo de armazenamento com o objeto da conta de armazenamento e o nome do compartilhamento</span><span class="sxs-lookup"><span data-stu-id="c3625-114">Example 2: Modifies metadata on a Storage file share with Storage account object and share name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount"
PS C:\>$share = Update-AzRmStorageShare -StorageAccount $accountObject -Name "myshare" -Metadata @{tag0="value0";tag1="value1"}
```

<span data-ttu-id="c3625-115">Esse comando modifica metadados em um compartilhamento de arquivo de armazenamento com o objeto da conta de armazenamento e o nome do compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="c3625-115">This command modifies metadata on a Storage file share with Storage account object and share name.</span></span>

### <span data-ttu-id="c3625-116">Exemplo 3: modifica a cota de compartilhamento de todos os compartilhamentos de arquivos de armazenamento em uma conta de armazenamento com pipeline</span><span class="sxs-lookup"><span data-stu-id="c3625-116">Example 3: Modifies share quota for all Storage file shares in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" | Update-AzRmStorageShare -QuotaGiB 5000

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
share1   5000
share2   5000
```

<span data-ttu-id="c3625-117">Esse comando modifica a cota de compartilhamento como 5000 GiB para todos os compartilhamentos de arquivos de armazenamento em uma conta de armazenamento com pipeline.</span><span class="sxs-lookup"><span data-stu-id="c3625-117">This command modifies share quota as 5000 GiB for all Storage file shares in a Storage account with pipeline.</span></span>

## <span data-ttu-id="c3625-118">OS</span><span class="sxs-lookup"><span data-stu-id="c3625-118">PARAMETERS</span></span>

### <span data-ttu-id="c3625-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3625-119">-DefaultProfile</span></span>
<span data-ttu-id="c3625-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c3625-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3625-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c3625-121">-InputObject</span></span>
<span data-ttu-id="c3625-122">Objeto de compartilhamento de armazenamento</span><span class="sxs-lookup"><span data-stu-id="c3625-122">Storage Share object</span></span>

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

### <span data-ttu-id="c3625-123">-Metadados</span><span class="sxs-lookup"><span data-stu-id="c3625-123">-Metadata</span></span>
<span data-ttu-id="c3625-124">Compartilhar metadados</span><span class="sxs-lookup"><span data-stu-id="c3625-124">Share Metadata</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3625-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="c3625-125">-Name</span></span>
<span data-ttu-id="c3625-126">Nome do compartilhamento</span><span class="sxs-lookup"><span data-stu-id="c3625-126">Share Name</span></span>

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

### <span data-ttu-id="c3625-127">-QuotaGiB</span><span class="sxs-lookup"><span data-stu-id="c3625-127">-QuotaGiB</span></span>
<span data-ttu-id="c3625-128">Compartilhe a cota no Gibibyte.</span><span class="sxs-lookup"><span data-stu-id="c3625-128">Share Quota in Gibibyte.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Quota

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3625-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3625-129">-ResourceGroupName</span></span>
<span data-ttu-id="c3625-130">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c3625-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="c3625-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c3625-131">-ResourceId</span></span>
<span data-ttu-id="c3625-132">Insira uma ID de recurso de compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="c3625-132">Input a File Share Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3625-133">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="c3625-133">-StorageAccount</span></span>
<span data-ttu-id="c3625-134">Objeto da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="c3625-134">Storage account object</span></span>

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

### <span data-ttu-id="c3625-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c3625-135">-StorageAccountName</span></span>
<span data-ttu-id="c3625-136">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c3625-136">Storage Account Name.</span></span>

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

### <span data-ttu-id="c3625-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c3625-137">-Confirm</span></span>
<span data-ttu-id="c3625-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3625-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3625-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3625-139">-WhatIf</span></span>
<span data-ttu-id="c3625-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c3625-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3625-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c3625-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3625-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3625-142">CommonParameters</span></span>
<span data-ttu-id="c3625-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3625-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3625-144">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3625-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3625-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c3625-145">INPUTS</span></span>

### <span data-ttu-id="c3625-146">System. String</span><span class="sxs-lookup"><span data-stu-id="c3625-146">System.String</span></span>

### <span data-ttu-id="c3625-147">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c3625-147">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="c3625-148">Microsoft. Azure. Commands. Management. Storage. Models. PSShare</span><span class="sxs-lookup"><span data-stu-id="c3625-148">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="c3625-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c3625-149">OUTPUTS</span></span>

### <span data-ttu-id="c3625-150">Microsoft. Azure. Commands. Management. Storage. Models. PSShare</span><span class="sxs-lookup"><span data-stu-id="c3625-150">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="c3625-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c3625-151">NOTES</span></span>

## <span data-ttu-id="c3625-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c3625-152">RELATED LINKS</span></span>
