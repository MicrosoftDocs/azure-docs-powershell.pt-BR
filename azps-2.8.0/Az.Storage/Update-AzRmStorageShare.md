---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageShare.md
ms.openlocfilehash: 03a1b76dc23d78e3ac4e2da5141560ca7b6add24
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774043"
---
# <span data-ttu-id="9a026-101">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="9a026-101">Update-AzRmStorageShare</span></span>

## <span data-ttu-id="9a026-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9a026-102">SYNOPSIS</span></span>
<span data-ttu-id="9a026-103">Modifica um compartilhamento de arquivo de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="9a026-103">Modifies a Storage file share.</span></span>

## <span data-ttu-id="9a026-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9a026-104">SYNTAX</span></span>

### <span data-ttu-id="9a026-105">AccountName (padrão)</span><span class="sxs-lookup"><span data-stu-id="9a026-105">AccountName (Default)</span></span>
```
Update-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-QuotaGiB <Int32>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9a026-106">Accountobject</span><span class="sxs-lookup"><span data-stu-id="9a026-106">AccountObject</span></span>
```
Update-AzRmStorageShare -Name <String> -StorageAccount <PSStorageAccount> [-QuotaGiB <Int32>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a026-107">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="9a026-107">ShareResourceId</span></span>
```
Update-AzRmStorageShare [-ResourceId] <String> [-QuotaGiB <Int32>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a026-108">Shareobject</span><span class="sxs-lookup"><span data-stu-id="9a026-108">ShareObject</span></span>
```
Update-AzRmStorageShare -InputObject <PSShare> [-QuotaGiB <Int32>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a026-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9a026-109">DESCRIPTION</span></span>
<span data-ttu-id="9a026-110">O cmdlet **New-AzRmStorageShare** modifica um compartilhamento de arquivo de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="9a026-110">The **New-AzRmStorageShare** cmdlet modifies a Storage file share.</span></span>

## <span data-ttu-id="9a026-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9a026-111">EXAMPLES</span></span>

### <span data-ttu-id="9a026-112">Exemplo 1: modifica os metadados e a cota de compartilhamento de um compartilhamento de arquivos de armazenamento com o nome da conta de armazenamento e o nome do compartilhamento</span><span class="sxs-lookup"><span data-stu-id="9a026-112">Example 1: Modifies a Storage file share's metadata and share quota with Storage account name and share name</span></span>
```
PS C:\>$share = Update-AzRmStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" -Name "myshare" -QuotaGiB 200 -Metadata @{tag0="value0";tag1="value1"}

PS C:\>$share

Name     StorageAccountName ResourceGroupName Etag                QuotaGiB LastModifiedTime    
----     ------------------ ----------------- ----                -------- ----------------    
myshare  myStorageAccount   myResourceGroup                       200     

PS C:\>$share.Metadata

Key  Value  
---  ----- 
tag0 value0
tag1 value1
```

<span data-ttu-id="9a026-113">Esse comando modifica a cota de metadados e compartilhamento de um compartilhamento de arquivos de armazenamento com o nome da conta de armazenamento e o nome do compartilhamento e mostra o resultado de modificação com o objeto de compartilhamento de arquivo retornado.</span><span class="sxs-lookup"><span data-stu-id="9a026-113">This command modifies a Storage file share's metadata and share quota with Storage account name and share name, and show the modify result with the returned file share object.</span></span>

### <span data-ttu-id="9a026-114">Exemplo 2: modifica metadados em um compartilhamento de arquivo de armazenamento com o objeto da conta de armazenamento e o nome do compartilhamento</span><span class="sxs-lookup"><span data-stu-id="9a026-114">Example 2: Modifies metadata on a Storage file share with Storage account object and share name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount"
PS C:\>$share = Update-AzRmStorageShare -StorageAccount $accountObject -Name "myshare" -Metadata @{tag0="value0";tag1="value1"}
```

<span data-ttu-id="9a026-115">Esse comando modifica metadados em um compartilhamento de arquivo de armazenamento com o objeto da conta de armazenamento e o nome do compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="9a026-115">This command modifies metadata on a Storage file share with Storage account object and share name.</span></span>

### <span data-ttu-id="9a026-116">Exemplo 3: modifica a cota de compartilhamento de todos os compartilhamentos de arquivos de armazenamento em uma conta de armazenamento com pipeline</span><span class="sxs-lookup"><span data-stu-id="9a026-116">Example 3: Modifies share quota for all Storage file shares in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" | Update-AzRmStorageShare -QuotaGiB 5000

Name     StorageAccountName ResourceGroupName Etag                QuotaGiB LastModifiedTime    
----     ------------------ ----------------- ----                -------- ----------------    
share1   myStorageAccount   myResourceGroup                       5000
share2   myStorageAccount   myResourceGroup                       5000
```

<span data-ttu-id="9a026-117">Esse comando modifica a cota de compartilhamento como 5000 GiB para todos os compartilhamentos de arquivos de armazenamento em uma conta de armazenamento com pipeline.</span><span class="sxs-lookup"><span data-stu-id="9a026-117">This command modifies share quota as 5000 GiB for all Storage file shares in a Storage account with pipeline.</span></span>

## <span data-ttu-id="9a026-118">OS</span><span class="sxs-lookup"><span data-stu-id="9a026-118">PARAMETERS</span></span>

### <span data-ttu-id="9a026-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a026-119">-DefaultProfile</span></span>
<span data-ttu-id="9a026-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9a026-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a026-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9a026-121">-InputObject</span></span>
<span data-ttu-id="9a026-122">Objeto de compartilhamento de armazenamento</span><span class="sxs-lookup"><span data-stu-id="9a026-122">Storage Share object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSShare
Parameter Sets: ShareObject
Aliases: Share

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a026-123">-Metadados</span><span class="sxs-lookup"><span data-stu-id="9a026-123">-Metadata</span></span>
<span data-ttu-id="9a026-124">Compartilhar metadados</span><span class="sxs-lookup"><span data-stu-id="9a026-124">Share Metadata</span></span>

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

### <span data-ttu-id="9a026-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="9a026-125">-Name</span></span>
<span data-ttu-id="9a026-126">Nome do compartilhamento</span><span class="sxs-lookup"><span data-stu-id="9a026-126">Share Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N, ShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a026-127">-QuotaGiB</span><span class="sxs-lookup"><span data-stu-id="9a026-127">-QuotaGiB</span></span>
<span data-ttu-id="9a026-128">Compartilhe a cota no Gibibyte.</span><span class="sxs-lookup"><span data-stu-id="9a026-128">Share Quota in Gibibyte.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a026-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a026-129">-ResourceGroupName</span></span>
<span data-ttu-id="9a026-130">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9a026-130">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a026-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9a026-131">-ResourceId</span></span>
<span data-ttu-id="9a026-132">Insira uma ID de recurso de compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="9a026-132">Input a File Share Resource Id.</span></span>

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

### <span data-ttu-id="9a026-133">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="9a026-133">-StorageAccount</span></span>
<span data-ttu-id="9a026-134">Objeto da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="9a026-134">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a026-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="9a026-135">-StorageAccountName</span></span>
<span data-ttu-id="9a026-136">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="9a026-136">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a026-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9a026-137">-Confirm</span></span>
<span data-ttu-id="9a026-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a026-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a026-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a026-139">-WhatIf</span></span>
<span data-ttu-id="9a026-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9a026-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a026-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9a026-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a026-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a026-142">CommonParameters</span></span>
<span data-ttu-id="9a026-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a026-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a026-144">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a026-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a026-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9a026-145">INPUTS</span></span>

### <span data-ttu-id="9a026-146">System. String</span><span class="sxs-lookup"><span data-stu-id="9a026-146">System.String</span></span>

### <span data-ttu-id="9a026-147">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9a026-147">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="9a026-148">Microsoft. Azure. Commands. Management. Storage. Models. PSShare</span><span class="sxs-lookup"><span data-stu-id="9a026-148">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="9a026-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9a026-149">OUTPUTS</span></span>

### <span data-ttu-id="9a026-150">Microsoft. Azure. Commands. Management. Storage. Models. PSShare</span><span class="sxs-lookup"><span data-stu-id="9a026-150">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="9a026-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9a026-151">NOTES</span></span>

## <span data-ttu-id="9a026-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9a026-152">RELATED LINKS</span></span>
