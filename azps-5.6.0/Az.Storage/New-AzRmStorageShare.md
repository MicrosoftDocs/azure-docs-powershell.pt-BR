---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageShare.md
ms.openlocfilehash: dcb4819a3ac13056acd1b51dde2ee67774d51693
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890915"
---
# <span data-ttu-id="5461a-101">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="5461a-101">New-AzRmStorageShare</span></span>

## <span data-ttu-id="5461a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5461a-102">SYNOPSIS</span></span>
<span data-ttu-id="5461a-103">Cria um compartilhamento de arquivo de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="5461a-103">Creates a Storage file share.</span></span>

## <span data-ttu-id="5461a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="5461a-104">SYNTAX</span></span>

### <span data-ttu-id="5461a-105">AccountName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="5461a-105">AccountName (Default)</span></span>
```
New-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-QuotaGiB <Int32>] [-Metadata <Hashtable>] [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5461a-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="5461a-106">AccountObject</span></span>
```
New-AzRmStorageShare -StorageAccount <PSStorageAccount> -Name <String> [-QuotaGiB <Int32>]
 [-Metadata <Hashtable>] [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5461a-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="5461a-107">DESCRIPTION</span></span>
<span data-ttu-id="5461a-108">O cmdlet **New-AzRmStorageShare** cria um compartilhamento de arquivo de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="5461a-108">The **New-AzRmStorageShare** cmdlet creates a Storage file share.</span></span>

## <span data-ttu-id="5461a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5461a-109">EXAMPLES</span></span>

### <span data-ttu-id="5461a-110">Exemplo 1: Criar um compartilhamento de arquivos de armazenamento com o nome da conta de armazenamento e o nome do compartilhamento, com metadados e cota de compartilhamento como 100 GiB.</span><span class="sxs-lookup"><span data-stu-id="5461a-110">Example 1: Create a Storage file share with Storage account name and share name, with metadata and share quota as 100 GiB.</span></span>
```
PS C:\>New-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -QuotaGiB 100 -Metadata @{"tag1" = "value1"; "tag2" = "value2" } 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare
```

<span data-ttu-id="5461a-111">Este comando cria um compartilhamento de arquivos de armazenamento com metadados e cota de compartilhamento como 100 GiB.</span><span class="sxs-lookup"><span data-stu-id="5461a-111">This command creates a Storage file share with metadata and share quota as 100 GiB.</span></span>

### <span data-ttu-id="5461a-112">Exemplo 2: Criar um compartilhamento de arquivos de armazenamento com o objeto de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="5461a-112">Example 2: Create a Storage file share with Storage account object</span></span>
```
Get-AzStorageAccount -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" | New-AzRmStorageShare -Name "myshare"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare
```

<span data-ttu-id="5461a-113">Este comando cria um compartilhamento de arquivo de armazenamento com o objeto de conta de armazenamento e o nome do compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="5461a-113">This command creates a Storage file share with Storage account object and share name.</span></span>

### <span data-ttu-id="5461a-114">Exemplo 3: Criar um compartilhamento de arquivos de armazenamento com accesstier como Hot</span><span class="sxs-lookup"><span data-stu-id="5461a-114">Example 3: Create a Storage file share with accesstier as Hot</span></span>
```
PS C:\>$share = New-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -AccessTier Hot

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocols AccessTier Deleted Version ShareUsageBytes
----     -------- ---------------- ---------- ------- ------- ---------------
myshare                            Hot
```

<span data-ttu-id="5461a-115">Este comando cria um compartilhamento de arquivo de armazenamento com accesstier como Hot.</span><span class="sxs-lookup"><span data-stu-id="5461a-115">This command creates a Storage file share with accesstier as Hot.</span></span>

## <span data-ttu-id="5461a-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="5461a-116">PARAMETERS</span></span>

### <span data-ttu-id="5461a-117">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="5461a-117">-AccessTier</span></span>
<span data-ttu-id="5461a-118">Camada de acesso para compartilhamento específico.</span><span class="sxs-lookup"><span data-stu-id="5461a-118">Access tier for specific share.</span></span> <span data-ttu-id="5461a-119">A conta StorageV2 pode escolher entre TransactionOptimized (padrão), Hot e Cool.</span><span class="sxs-lookup"><span data-stu-id="5461a-119">StorageV2 account can choose between TransactionOptimized (default), Hot, and Cool.</span></span> <span data-ttu-id="5461a-120">A conta FileStorage pode escolher Premium.</span><span class="sxs-lookup"><span data-stu-id="5461a-120">FileStorage account can choose Premium.</span></span>

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

### <span data-ttu-id="5461a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5461a-121">-DefaultProfile</span></span>
<span data-ttu-id="5461a-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5461a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5461a-123">-Metadados</span><span class="sxs-lookup"><span data-stu-id="5461a-123">-Metadata</span></span>
<span data-ttu-id="5461a-124">Compartilhar metadados</span><span class="sxs-lookup"><span data-stu-id="5461a-124">Share Metadata</span></span>

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

### <span data-ttu-id="5461a-125">-Name</span><span class="sxs-lookup"><span data-stu-id="5461a-125">-Name</span></span>
<span data-ttu-id="5461a-126">Nome do compartilhamento de arquivo do Azure</span><span class="sxs-lookup"><span data-stu-id="5461a-126">Azure File share name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, ShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5461a-127">-QuotaGiB</span><span class="sxs-lookup"><span data-stu-id="5461a-127">-QuotaGiB</span></span>
<span data-ttu-id="5461a-128">Cota de Compartilhamento em Gibibyte.</span><span class="sxs-lookup"><span data-stu-id="5461a-128">Share Quota in Gibibyte.</span></span>

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

### <span data-ttu-id="5461a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5461a-129">-ResourceGroupName</span></span>
<span data-ttu-id="5461a-130">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="5461a-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="5461a-131">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="5461a-131">-StorageAccount</span></span>
<span data-ttu-id="5461a-132">Objeto de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="5461a-132">Storage account object</span></span>

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

### <span data-ttu-id="5461a-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="5461a-133">-StorageAccountName</span></span>
<span data-ttu-id="5461a-134">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="5461a-134">Storage Account Name.</span></span>

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

### <span data-ttu-id="5461a-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5461a-135">-Confirm</span></span>
<span data-ttu-id="5461a-136">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5461a-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5461a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5461a-137">-WhatIf</span></span>
<span data-ttu-id="5461a-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5461a-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5461a-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5461a-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5461a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5461a-140">CommonParameters</span></span>
<span data-ttu-id="5461a-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5461a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5461a-142">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5461a-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5461a-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5461a-143">INPUTS</span></span>

### <span data-ttu-id="5461a-144">System.String</span><span class="sxs-lookup"><span data-stu-id="5461a-144">System.String</span></span>

### <span data-ttu-id="5461a-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5461a-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="5461a-146">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="5461a-146">OUTPUTS</span></span>

### <span data-ttu-id="5461a-147">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span><span class="sxs-lookup"><span data-stu-id="5461a-147">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="5461a-148">NOTES</span><span class="sxs-lookup"><span data-stu-id="5461a-148">NOTES</span></span>

## <span data-ttu-id="5461a-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5461a-149">RELATED LINKS</span></span>
