---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageShare.md
ms.openlocfilehash: 4dc3914e4a8bc9113dd16ab431db53ddcf00ab5a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94282127"
---
# <span data-ttu-id="c648b-101">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="c648b-101">New-AzRmStorageShare</span></span>

## <span data-ttu-id="c648b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c648b-102">SYNOPSIS</span></span>
<span data-ttu-id="c648b-103">Cria um compartilhamento de arquivos de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c648b-103">Creates a Storage file share.</span></span>

## <span data-ttu-id="c648b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c648b-104">SYNTAX</span></span>

### <span data-ttu-id="c648b-105">AccountName (padrão)</span><span class="sxs-lookup"><span data-stu-id="c648b-105">AccountName (Default)</span></span>
```
New-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-QuotaGiB <Int32>] [-Metadata <Hashtable>] [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c648b-106">Accountobject</span><span class="sxs-lookup"><span data-stu-id="c648b-106">AccountObject</span></span>
```
New-AzRmStorageShare -StorageAccount <PSStorageAccount> -Name <String> [-QuotaGiB <Int32>]
 [-Metadata <Hashtable>] [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c648b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c648b-107">DESCRIPTION</span></span>
<span data-ttu-id="c648b-108">O cmdlet **New-AzRmStorageShare** cria um compartilhamento de arquivos de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c648b-108">The **New-AzRmStorageShare** cmdlet creates a Storage file share.</span></span>

## <span data-ttu-id="c648b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c648b-109">EXAMPLES</span></span>

### <span data-ttu-id="c648b-110">Exemplo 1: criar um compartilhamento de arquivo de armazenamento com o nome da conta de armazenamento e o nome do compartilhamento, com metadados e cota de compartilhamento como 100 GiB.</span><span class="sxs-lookup"><span data-stu-id="c648b-110">Example 1: Create a Storage file share with Storage account name and share name, with metadata and share quota as 100 GiB.</span></span>
```
PS C:\>New-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -QuotaGiB 100 -Metadata @{"tag1" = "value1"; "tag2" = "value2" } 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare
```

<span data-ttu-id="c648b-111">Esse comando cria um compartilhamento de arquivos de armazenamento com metadados e cota de compartilhamento como 100 GiB.</span><span class="sxs-lookup"><span data-stu-id="c648b-111">This command creates a Storage file share with metadata and share quota as 100 GiB.</span></span>

### <span data-ttu-id="c648b-112">Exemplo 2: criar um compartilhamento de arquivos de armazenamento com objeto da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="c648b-112">Example 2: Create a Storage file share with Storage account object</span></span>
```
Get-AzStorageAccount -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" | New-AzRmStorageShare -Name "myshare"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare
```

<span data-ttu-id="c648b-113">Esse comando cria um compartilhamento de arquivos de armazenamento com o objeto da conta de armazenamento e o nome do compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="c648b-113">This command creates a Storage file share with Storage account object and share name.</span></span>

### <span data-ttu-id="c648b-114">Exemplo 3: criar um compartilhamento de arquivos de armazenamento com o accesstier como quente</span><span class="sxs-lookup"><span data-stu-id="c648b-114">Example 3: Create a Storage file share with accesstier as Hot</span></span>
```
PS C:\>$share = New-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -AccessTier Hot

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocols AccessTier Deleted Version ShareUsageBytes
----     -------- ---------------- ---------- ------- ------- ---------------
myshare                            Hot
```

<span data-ttu-id="c648b-115">Esse comando cria um compartilhamento de arquivos de armazenamento com o accesstier como quente.</span><span class="sxs-lookup"><span data-stu-id="c648b-115">This command creates a Storage file share with accesstier as Hot.</span></span>

## <span data-ttu-id="c648b-116">OS</span><span class="sxs-lookup"><span data-stu-id="c648b-116">PARAMETERS</span></span>

### <span data-ttu-id="c648b-117">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="c648b-117">-AccessTier</span></span>
<span data-ttu-id="c648b-118">Camada de acesso para compartilhamento específico.</span><span class="sxs-lookup"><span data-stu-id="c648b-118">Access tier for specific share.</span></span> <span data-ttu-id="c648b-119">StorageV2 conta pode escolher entre TransactionOptimized (padrão), quente e legal.</span><span class="sxs-lookup"><span data-stu-id="c648b-119">StorageV2 account can choose between TransactionOptimized (default), Hot, and Cool.</span></span> <span data-ttu-id="c648b-120">Conta de armazenamento de armazenamento pode escolher Premium.</span><span class="sxs-lookup"><span data-stu-id="c648b-120">FileStorage account can choose Premium.</span></span>

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

### <span data-ttu-id="c648b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c648b-121">-DefaultProfile</span></span>
<span data-ttu-id="c648b-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c648b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c648b-123">-Metadados</span><span class="sxs-lookup"><span data-stu-id="c648b-123">-Metadata</span></span>
<span data-ttu-id="c648b-124">Compartilhar metadados</span><span class="sxs-lookup"><span data-stu-id="c648b-124">Share Metadata</span></span>

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

### <span data-ttu-id="c648b-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="c648b-125">-Name</span></span>
<span data-ttu-id="c648b-126">Nome do compartilhamento de arquivos do Azure</span><span class="sxs-lookup"><span data-stu-id="c648b-126">Azure File share name</span></span>

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

### <span data-ttu-id="c648b-127">-QuotaGiB</span><span class="sxs-lookup"><span data-stu-id="c648b-127">-QuotaGiB</span></span>
<span data-ttu-id="c648b-128">Compartilhe a cota no Gibibyte.</span><span class="sxs-lookup"><span data-stu-id="c648b-128">Share Quota in Gibibyte.</span></span>

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

### <span data-ttu-id="c648b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c648b-129">-ResourceGroupName</span></span>
<span data-ttu-id="c648b-130">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c648b-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="c648b-131">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="c648b-131">-StorageAccount</span></span>
<span data-ttu-id="c648b-132">Objeto da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="c648b-132">Storage account object</span></span>

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

### <span data-ttu-id="c648b-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c648b-133">-StorageAccountName</span></span>
<span data-ttu-id="c648b-134">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c648b-134">Storage Account Name.</span></span>

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

### <span data-ttu-id="c648b-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c648b-135">-Confirm</span></span>
<span data-ttu-id="c648b-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c648b-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c648b-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c648b-137">-WhatIf</span></span>
<span data-ttu-id="c648b-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c648b-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c648b-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c648b-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c648b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c648b-140">CommonParameters</span></span>
<span data-ttu-id="c648b-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c648b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c648b-142">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c648b-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c648b-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c648b-143">INPUTS</span></span>

### <span data-ttu-id="c648b-144">System. String</span><span class="sxs-lookup"><span data-stu-id="c648b-144">System.String</span></span>

### <span data-ttu-id="c648b-145">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c648b-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="c648b-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c648b-146">OUTPUTS</span></span>

### <span data-ttu-id="c648b-147">Microsoft. Azure. Commands. Management. Storage. Models. PSShare</span><span class="sxs-lookup"><span data-stu-id="c648b-147">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="c648b-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c648b-148">NOTES</span></span>

## <span data-ttu-id="c648b-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c648b-149">RELATED LINKS</span></span>
