---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/update-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageShare.md
ms.openlocfilehash: 7612b323600b2f076c30225994d6e475d66c01ac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888049"
---
# <span data-ttu-id="07f03-101">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="07f03-101">Update-AzRmStorageShare</span></span>

## <span data-ttu-id="07f03-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07f03-102">SYNOPSIS</span></span>
<span data-ttu-id="07f03-103">Modifica um compartilhamento de arquivo de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="07f03-103">Modifies a Storage file share.</span></span>

## <span data-ttu-id="07f03-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="07f03-104">SYNTAX</span></span>

### <span data-ttu-id="07f03-105">AccountName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="07f03-105">AccountName (Default)</span></span>
```
Update-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-QuotaGiB <Int32>] [-Metadata <Hashtable>] [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07f03-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="07f03-106">AccountObject</span></span>
```
Update-AzRmStorageShare -Name <String> -StorageAccount <PSStorageAccount> [-QuotaGiB <Int32>]
 [-Metadata <Hashtable>] [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="07f03-107">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="07f03-107">ShareResourceId</span></span>
```
Update-AzRmStorageShare [-ResourceId] <String> [-QuotaGiB <Int32>] [-Metadata <Hashtable>]
 [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07f03-108">ShareObject</span><span class="sxs-lookup"><span data-stu-id="07f03-108">ShareObject</span></span>
```
Update-AzRmStorageShare -InputObject <PSShare> [-QuotaGiB <Int32>] [-Metadata <Hashtable>]
 [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07f03-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="07f03-109">DESCRIPTION</span></span>
<span data-ttu-id="07f03-110">O cmdlet **New-AzRmStorageShare** modifica um compartilhamento de arquivo de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="07f03-110">The **New-AzRmStorageShare** cmdlet modifies a Storage file share.</span></span>

## <span data-ttu-id="07f03-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="07f03-111">EXAMPLES</span></span>

### <span data-ttu-id="07f03-112">Exemplo 1: modifica os metadados de um compartilhamento de arquivo de armazenamento e a cota de compartilhamento com o nome da conta de armazenamento e o nome do compartilhamento</span><span class="sxs-lookup"><span data-stu-id="07f03-112">Example 1: Modifies a Storage file share's metadata and share quota with Storage account name and share name</span></span>
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

<span data-ttu-id="07f03-113">Este comando modifica os metadados de um compartilhamento de arquivo de armazenamento e a cota de compartilhamento com o nome da conta de armazenamento e o nome do compartilhamento e mostra o resultado de modificação com o objeto de compartilhamento de arquivo retornado.</span><span class="sxs-lookup"><span data-stu-id="07f03-113">This command modifies a Storage file share's metadata and share quota with Storage account name and share name, and show the modify result with the returned file share object.</span></span>

### <span data-ttu-id="07f03-114">Exemplo 2: modifica metadados em um compartilhamento de arquivos de armazenamento com o objeto de conta de armazenamento e o nome do compartilhamento</span><span class="sxs-lookup"><span data-stu-id="07f03-114">Example 2: Modifies metadata on a Storage file share with Storage account object and share name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount"
PS C:\>$share = Update-AzRmStorageShare -StorageAccount $accountObject -Name "myshare" -Metadata @{tag0="value0";tag1="value1"}
```

<span data-ttu-id="07f03-115">Este comando modifica os metadados em um compartilhamento de arquivos de armazenamento com o objeto de conta de armazenamento e o nome do compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="07f03-115">This command modifies metadata on a Storage file share with Storage account object and share name.</span></span>

### <span data-ttu-id="07f03-116">Exemplo 3: Modifica a cota de compartilhamento para todos os compartilhamentos de arquivos de armazenamento em uma conta de armazenamento com pipeline</span><span class="sxs-lookup"><span data-stu-id="07f03-116">Example 3: Modifies share quota for all Storage file shares in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" | Update-AzRmStorageShare -QuotaGiB 5000

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
share1   5000
share2   5000
```

<span data-ttu-id="07f03-117">Este comando modifica a cota de compartilhamento como 5.000 GiB para todos os compartilhamentos de arquivos de armazenamento em uma conta de armazenamento com pipeline.</span><span class="sxs-lookup"><span data-stu-id="07f03-117">This command modifies share quota as 5000 GiB for all Storage file shares in a Storage account with pipeline.</span></span>

### <span data-ttu-id="07f03-118">Exemplo 4: Modificar um compartilhamento de arquivos de armazenamento com accesstier como Cool</span><span class="sxs-lookup"><span data-stu-id="07f03-118">Example 4: Modify a Storage file share with accesstier as Cool</span></span>
```
PS C:\>$share = Update-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -AccessTier Cool

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocols AccessTier Deleted Version ShareUsageBytes
----     -------- ---------------- ---------- ------- ------- ---------------
myshare                            Cool
```

<span data-ttu-id="07f03-119">Este comando modifica um compartilhamento de arquivo de armazenamento com accesstier como Cool.</span><span class="sxs-lookup"><span data-stu-id="07f03-119">This command modifies a Storage file share with accesstier as Cool.</span></span>

## <span data-ttu-id="07f03-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="07f03-120">PARAMETERS</span></span>

### <span data-ttu-id="07f03-121">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="07f03-121">-AccessTier</span></span>
<span data-ttu-id="07f03-122">Camada de acesso para compartilhamento específico.</span><span class="sxs-lookup"><span data-stu-id="07f03-122">Access tier for specific share.</span></span> <span data-ttu-id="07f03-123">A conta StorageV2 pode escolher entre TransactionOptimized (padrão), Hot e Cool.</span><span class="sxs-lookup"><span data-stu-id="07f03-123">StorageV2 account can choose between TransactionOptimized (default), Hot, and Cool.</span></span> <span data-ttu-id="07f03-124">A conta FileStorage pode escolher Premium.</span><span class="sxs-lookup"><span data-stu-id="07f03-124">FileStorage account can choose Premium.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: TransactionOptimized, Premium, Hot, Cool

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07f03-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07f03-125">-DefaultProfile</span></span>
<span data-ttu-id="07f03-126">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="07f03-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07f03-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="07f03-127">-InputObject</span></span>
<span data-ttu-id="07f03-128">Objeto Storage Share</span><span class="sxs-lookup"><span data-stu-id="07f03-128">Storage Share object</span></span>

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

### <span data-ttu-id="07f03-129">-Metadados</span><span class="sxs-lookup"><span data-stu-id="07f03-129">-Metadata</span></span>
<span data-ttu-id="07f03-130">Compartilhar metadados</span><span class="sxs-lookup"><span data-stu-id="07f03-130">Share Metadata</span></span>

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

### <span data-ttu-id="07f03-131">-Name</span><span class="sxs-lookup"><span data-stu-id="07f03-131">-Name</span></span>
<span data-ttu-id="07f03-132">Nome do Compartilhamento</span><span class="sxs-lookup"><span data-stu-id="07f03-132">Share Name</span></span>

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

### <span data-ttu-id="07f03-133">-QuotaGiB</span><span class="sxs-lookup"><span data-stu-id="07f03-133">-QuotaGiB</span></span>
<span data-ttu-id="07f03-134">Cota de Compartilhamento em Gibibyte.</span><span class="sxs-lookup"><span data-stu-id="07f03-134">Share Quota in Gibibyte.</span></span>

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

### <span data-ttu-id="07f03-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07f03-135">-ResourceGroupName</span></span>
<span data-ttu-id="07f03-136">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="07f03-136">Resource Group Name.</span></span>

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

### <span data-ttu-id="07f03-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="07f03-137">-ResourceId</span></span>
<span data-ttu-id="07f03-138">Entrada de uma ID de Recurso de Compartilhamento de Arquivos.</span><span class="sxs-lookup"><span data-stu-id="07f03-138">Input a File Share Resource Id.</span></span>

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

### <span data-ttu-id="07f03-139">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="07f03-139">-StorageAccount</span></span>
<span data-ttu-id="07f03-140">Objeto de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="07f03-140">Storage account object</span></span>

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

### <span data-ttu-id="07f03-141">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="07f03-141">-StorageAccountName</span></span>
<span data-ttu-id="07f03-142">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="07f03-142">Storage Account Name.</span></span>

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

### <span data-ttu-id="07f03-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="07f03-143">-Confirm</span></span>
<span data-ttu-id="07f03-144">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07f03-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07f03-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07f03-145">-WhatIf</span></span>
<span data-ttu-id="07f03-146">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="07f03-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07f03-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="07f03-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07f03-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07f03-148">CommonParameters</span></span>
<span data-ttu-id="07f03-149">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07f03-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07f03-150">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07f03-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07f03-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="07f03-151">INPUTS</span></span>

### <span data-ttu-id="07f03-152">System.String</span><span class="sxs-lookup"><span data-stu-id="07f03-152">System.String</span></span>

### <span data-ttu-id="07f03-153">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="07f03-153">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="07f03-154">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span><span class="sxs-lookup"><span data-stu-id="07f03-154">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="07f03-155">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="07f03-155">OUTPUTS</span></span>

### <span data-ttu-id="07f03-156">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span><span class="sxs-lookup"><span data-stu-id="07f03-156">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="07f03-157">NOTES</span><span class="sxs-lookup"><span data-stu-id="07f03-157">NOTES</span></span>

## <span data-ttu-id="07f03-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="07f03-158">RELATED LINKS</span></span>
