---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageShare.md
ms.openlocfilehash: 0f2d86fca85364fa71d50c05d83f278bd997252e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118905"
---
# <span data-ttu-id="f28a8-101">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="f28a8-101">Update-AzRmStorageShare</span></span>

## <span data-ttu-id="f28a8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f28a8-102">SYNOPSIS</span></span>
<span data-ttu-id="f28a8-103">Modifica um compartilhamento de arquivo de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="f28a8-103">Modifies a Storage file share.</span></span>

## <span data-ttu-id="f28a8-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f28a8-104">SYNTAX</span></span>

### <span data-ttu-id="f28a8-105">Nomeda Conta (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f28a8-105">AccountName (Default)</span></span>
```
Update-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-QuotaGiB <Int32>] [-Metadata <Hashtable>] [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f28a8-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="f28a8-106">AccountObject</span></span>
```
Update-AzRmStorageShare -Name <String> -StorageAccount <PSStorageAccount> [-QuotaGiB <Int32>]
 [-Metadata <Hashtable>] [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f28a8-107">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="f28a8-107">ShareResourceId</span></span>
```
Update-AzRmStorageShare [-ResourceId] <String> [-QuotaGiB <Int32>] [-Metadata <Hashtable>]
 [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f28a8-108">ShareObject</span><span class="sxs-lookup"><span data-stu-id="f28a8-108">ShareObject</span></span>
```
Update-AzRmStorageShare -InputObject <PSShare> [-QuotaGiB <Int32>] [-Metadata <Hashtable>]
 [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f28a8-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="f28a8-109">DESCRIPTION</span></span>
<span data-ttu-id="f28a8-110">O **cmdlet New-AzRmStorageShare** modifica um compartilhamento de arquivo de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="f28a8-110">The **New-AzRmStorageShare** cmdlet modifies a Storage file share.</span></span>

## <span data-ttu-id="f28a8-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f28a8-111">EXAMPLES</span></span>

### <span data-ttu-id="f28a8-112">Exemplo 1: modifica os metadados de um compartilhamento de arquivo de armazenamento e a cota de compartilhamento com o nome da conta de armazenamento e o nome do compartilhamento</span><span class="sxs-lookup"><span data-stu-id="f28a8-112">Example 1: Modifies a Storage file share's metadata and share quota with Storage account name and share name</span></span>
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

<span data-ttu-id="f28a8-113">Esse comando modifica os metadados de um compartilhamento de arquivo de armazenamento e cota de compartilhamento com o nome da conta de armazenamento e o nome do compartilhamento, e mostra o resultado de modificação com o objeto de compartilhamento de arquivo retornado.</span><span class="sxs-lookup"><span data-stu-id="f28a8-113">This command modifies a Storage file share's metadata and share quota with Storage account name and share name, and show the modify result with the returned file share object.</span></span>

### <span data-ttu-id="f28a8-114">Exemplo 2: modifica metadados em um compartilhamento de arquivos de armazenamento com o objeto de conta de armazenamento e o nome do compartilhamento</span><span class="sxs-lookup"><span data-stu-id="f28a8-114">Example 2: Modifies metadata on a Storage file share with Storage account object and share name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount"
PS C:\>$share = Update-AzRmStorageShare -StorageAccount $accountObject -Name "myshare" -Metadata @{tag0="value0";tag1="value1"}
```

<span data-ttu-id="f28a8-115">Esse comando modifica metadados em um compartilhamento de arquivos de armazenamento com o objeto de conta de armazenamento e o nome do compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="f28a8-115">This command modifies metadata on a Storage file share with Storage account object and share name.</span></span>

### <span data-ttu-id="f28a8-116">Exemplo 3: modifica a cota de compartilhamento para todos os compartilhamentos de arquivos de armazenamento em uma conta de armazenamento com pipeline</span><span class="sxs-lookup"><span data-stu-id="f28a8-116">Example 3: Modifies share quota for all Storage file shares in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" | Update-AzRmStorageShare -QuotaGiB 5000

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
share1   5000
share2   5000
```

<span data-ttu-id="f28a8-117">Esse comando modifica a cota de compartilhamento como 5.000 GiB para todos os compartilhamentos de arquivos de armazenamento em uma conta de Armazenamento com pipeline.</span><span class="sxs-lookup"><span data-stu-id="f28a8-117">This command modifies share quota as 5000 GiB for all Storage file shares in a Storage account with pipeline.</span></span>

### <span data-ttu-id="f28a8-118">Exemplo 4: Modificar um compartilhamento de arquivos de armazenamento com o accesstier as Cool</span><span class="sxs-lookup"><span data-stu-id="f28a8-118">Example 4: Modify a Storage file share with accesstier as Cool</span></span>
```
PS C:\>$share = Update-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -AccessTier Cool

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocols AccessTier Deleted Version ShareUsageBytes
----     -------- ---------------- ---------- ------- ------- ---------------
myshare                            Cool
```

<span data-ttu-id="f28a8-119">Esse comando modifica um compartilhamento de arquivo de armazenamento com o accesstier como Cool.</span><span class="sxs-lookup"><span data-stu-id="f28a8-119">This command modifies a Storage file share with accesstier as Cool.</span></span>

## <span data-ttu-id="f28a8-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f28a8-120">PARAMETERS</span></span>

### <span data-ttu-id="f28a8-121">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="f28a8-121">-AccessTier</span></span>
<span data-ttu-id="f28a8-122">Nível do Access para compartilhamento específico.</span><span class="sxs-lookup"><span data-stu-id="f28a8-122">Access tier for specific share.</span></span> <span data-ttu-id="f28a8-123">A conta StorageV2 pode escolher entre TransactionOptimized (padrão), Hot e Cool.</span><span class="sxs-lookup"><span data-stu-id="f28a8-123">StorageV2 account can choose between TransactionOptimized (default), Hot, and Cool.</span></span> <span data-ttu-id="f28a8-124">A conta FileStorage pode escolher Premium.</span><span class="sxs-lookup"><span data-stu-id="f28a8-124">FileStorage account can choose Premium.</span></span>

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

### <span data-ttu-id="f28a8-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f28a8-125">-DefaultProfile</span></span>
<span data-ttu-id="f28a8-126">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f28a8-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f28a8-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f28a8-127">-InputObject</span></span>
<span data-ttu-id="f28a8-128">Objeto Compartilhamento de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="f28a8-128">Storage Share object</span></span>

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

### <span data-ttu-id="f28a8-129">-Metadados</span><span class="sxs-lookup"><span data-stu-id="f28a8-129">-Metadata</span></span>
<span data-ttu-id="f28a8-130">Compartilhar Metadados</span><span class="sxs-lookup"><span data-stu-id="f28a8-130">Share Metadata</span></span>

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

### <span data-ttu-id="f28a8-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="f28a8-131">-Name</span></span>
<span data-ttu-id="f28a8-132">Compartilhar Nome</span><span class="sxs-lookup"><span data-stu-id="f28a8-132">Share Name</span></span>

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

### <span data-ttu-id="f28a8-133">-QuotaGiB</span><span class="sxs-lookup"><span data-stu-id="f28a8-133">-QuotaGiB</span></span>
<span data-ttu-id="f28a8-134">Compartilhar Cota no Gibibyte.</span><span class="sxs-lookup"><span data-stu-id="f28a8-134">Share Quota in Gibibyte.</span></span>

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

### <span data-ttu-id="f28a8-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f28a8-135">-ResourceGroupName</span></span>
<span data-ttu-id="f28a8-136">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f28a8-136">Resource Group Name.</span></span>

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

### <span data-ttu-id="f28a8-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f28a8-137">-ResourceId</span></span>
<span data-ttu-id="f28a8-138">Inserir uma ID de Recurso de Compartilhamento de Arquivo.</span><span class="sxs-lookup"><span data-stu-id="f28a8-138">Input a File Share Resource Id.</span></span>

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

### <span data-ttu-id="f28a8-139">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="f28a8-139">-StorageAccount</span></span>
<span data-ttu-id="f28a8-140">Objeto de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="f28a8-140">Storage account object</span></span>

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

### <span data-ttu-id="f28a8-141">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f28a8-141">-StorageAccountName</span></span>
<span data-ttu-id="f28a8-142">Nome da Conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="f28a8-142">Storage Account Name.</span></span>

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

### <span data-ttu-id="f28a8-143">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="f28a8-143">-Confirm</span></span>
<span data-ttu-id="f28a8-144">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f28a8-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f28a8-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f28a8-145">-WhatIf</span></span>
<span data-ttu-id="f28a8-146">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="f28a8-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f28a8-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f28a8-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f28a8-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f28a8-148">CommonParameters</span></span>
<span data-ttu-id="f28a8-149">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f28a8-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f28a8-150">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f28a8-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f28a8-151">Entradas</span><span class="sxs-lookup"><span data-stu-id="f28a8-151">INPUTS</span></span>

### <span data-ttu-id="f28a8-152">System.String</span><span class="sxs-lookup"><span data-stu-id="f28a8-152">System.String</span></span>

### <span data-ttu-id="f28a8-153">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f28a8-153">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="f28a8-154">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span><span class="sxs-lookup"><span data-stu-id="f28a8-154">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="f28a8-155">Saídas</span><span class="sxs-lookup"><span data-stu-id="f28a8-155">OUTPUTS</span></span>

### <span data-ttu-id="f28a8-156">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span><span class="sxs-lookup"><span data-stu-id="f28a8-156">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="f28a8-157">Notas</span><span class="sxs-lookup"><span data-stu-id="f28a8-157">NOTES</span></span>

## <span data-ttu-id="f28a8-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f28a8-158">RELATED LINKS</span></span>
